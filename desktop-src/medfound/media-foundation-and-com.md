---
description: Microsoft Media Foundation verwendet eine Mischung aus COM-Konstrukten, ist aber keine vollständig COM-basierte API.
ms.assetid: d58ca46f-8f3a-4a12-b948-1ea7ab568788
title: Media Foundation und COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb43fa29063da453a17275fca0b5c441e89f75aab8016a1abcf1702f5433fd71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974212"
---
# <a name="media-foundation-and-com"></a>Media Foundation und COM

Microsoft Media Foundation verwendet eine Mischung aus COM-Konstrukten, ist aber keine vollständig COM-basierte API. In diesem Thema wird die Interaktion zwischen COM und Media Foundation beschrieben. Außerdem werden einige bewährte Methoden für die Entwicklung Media Foundation Plug-In-Komponenten definiert. Wenn Sie diese Methoden befolgen, können Sie einige häufig auftretende, aber geringfügige Programmierfehler vermeiden.

-   [Bewährte Methoden für Anwendungen](#best-practices-for-applications)
-   [Bewährte Methoden für Media Foundation-Komponenten](#best-practices-for-media-foundation-components)
-   [Zusammenfassung](#summary)
-   [Zugehörige Themen](#related-topics)

## <a name="best-practices-for-applications"></a>Bewährte Methoden für Anwendungen

In Media Foundation werden asynchrone Verarbeitung und Rückrufe von [Arbeitswarteschlangen](work-queues.md)verarbeitet. Arbeitswarteschlangen verfügen immer über Multithread-Apartmentthreads (MTA), sodass eine Anwendung eine einfachere Implementierung hat, wenn sie auch in einem MTA-Thread ausgeführt wird. Aus diesem Grund wird empfohlen, [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) mit dem **FLAG COINIT \_ MULTITHREADED** aufzurufen.

Media Foundation marshallt keine STA-Objekte (Singlethreaded Apartment) in Arbeitswarteschlangenthreads. Es wird auch nicht sichergestellt, dass STA-Invarianten beibehalten werden. Daher muss eine STA-Anwendung darauf achten, keine STA-Objekte oder Proxys an Media Foundation APIs zu übergeben. Objekte, die nur STA sind, werden in Media Foundation nicht unterstützt.

Wenn Sie über einen STA-Proxy für ein MTA- oder Freethread-Objekt verfügen, kann das Objekt mithilfe eines Work-Queue-Rückrufs an einen MTA-Proxy gemarshallt werden. Die [**CoCreateInstance-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) kann je nach dem in der Registrierung für diese CLSID definierten Objektmodell entweder einen rohen Zeiger oder einen STA-Proxy zurückgeben. Wenn ein STA-Proxy zurückgegeben wird, dürfen Sie den Zeiger nicht an eine Media Foundation-API übergeben.

Angenommen, Sie möchten einen **IPropertyStore-Zeiger** an die [**METHODE POINTERSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) übergeben. Sie können **PSCreateMemoryPropertyStore** aufrufen, um den **IPropertyStore-Zeiger** zu erstellen. Wenn Sie aus einem STA aufrufen, müssen Sie den Zeiger marshallen, bevor Sie ihn an **BeginCreateObjectFromURL** übergeben.

Der folgende Code zeigt, wie ein STA-Proxy an eine Media Foundation-API gemarshallt wird.


```C++
class CCreateSourceMarshalCallback
    : public IMFAsyncCallback
{
public:
    CCreateSourceMarshalCallback(
        LPCWSTR szURL, 
        IMFSourceResolver* pResolver, 
        IPropertyStore* pSourceProps, 
        IMFAsyncCallback* pCompletionCallback, 
        HRESULT& hr
        )
        : m_szURL(szURL), 
          m_pResolver(pResolver), 
          m_pCompletionCallback(pCompletionCallback),
          m_pGIT(NULL),
          m_cRef(1)
    {
        hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable, NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGIT));

        if(SUCCEEDED(hr))
        {
            hr = m_pGIT->RegisterInterfaceInGlobal(
                pSourceProps, IID_IPropertyStore, &m_dwInterfaceCookie);
        }
    }
    ~CCreateSourceMarshalCallback()
    {
        SafeRelease(&m_pResolver);
        SafeRelease(&m_pCompletionCallback);
        SafeRelease(&m_pGIT);
    }


    STDMETHOD_(ULONG, AddRef)()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHOD_(ULONG, Release)()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (0 == cRef)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHOD(QueryInterface)(REFIID riid, LPVOID* ppvObject)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCreateSourceMarshalCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppvObject);

    }

    STDMETHOD(GetParameters)(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHOD(Invoke)(IMFAsyncResult* pResult)
    {
        IPropertyStore *pSourceProps = NULL;

        HRESULT hr = m_pGIT->GetInterfaceFromGlobal(
            m_dwInterfaceCookie, 
            IID_PPV_ARGS(&pSourceProps)
            );

        if(SUCCEEDED(hr))
        {
            hr = m_pResolver->BeginCreateObjectFromURL(
                m_szURL, MF_RESOLUTION_MEDIASOURCE, pSourceProps, NULL, 
                m_pCompletionCallback, NULL);
        }

        SafeRelease(&pSourceProps);
        return hr;
    }

private:
    LPCWSTR m_szURL;
    IMFSourceResolver *m_pResolver;
    IMFAsyncCallback *m_pCompletionCallback;
    IGlobalInterfaceTable *m_pGIT;
    DWORD m_dwInterfaceCookie;
    LONG m_cRef;
};
```



Weitere Informationen zur globalen Schnittstellentabelle finden Sie unter [**IGlobalInterfaceTable.**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable)

Wenn Sie Media Foundation in-Process verwenden, sind objekte, die von Media Foundation Methoden und Funktionen zurückgegeben werden, direkte Zeiger auf das Objekt. Für prozessübergreifende Media Foundation können diese Objekte MTA-Proxys sein und sollten bei Bedarf in einen STA-Thread gemarshallt werden. Ebenso sind Objekte, die innerhalb eines Rückrufs abgerufen werden , z. B. eine Topologie aus dem [MESessionTopologyStatus-Ereignis,](mesessiontopologystatus.md) direkte Zeiger, wenn Media Foundation prozessübergreifend verwendet wird, aber MTA-Proxys, wenn Media Foundation prozessübergreifend verwendet wird.

> [!Note]  
> Das gängigste Szenario für die Verwendung Media Foundation prozessübergreifenden Vorgangs ist der [Geschützte Medienpfad (Protected Media Path,](protected-media-path.md) PMP). Diese Hinweise gelten jedoch für alle Situationen, in denen Media Foundation-APIs über RPC verwendet werden.

 

Alle Implementierungen von [**AWAITAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) sollten MTA-kompatibel sein. Diese Objekte müssen überhaupt keine COM-Objekte sein. Wenn dies dere ist, können sie nicht im STA ausgeführt werden. Die [**FUNKTION AWAITAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) wird für einen MTA-Arbeitsqueuethread aufgerufen, und das bereitgestellte OBJEKT VOM 16. [**16. IST**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) entweder ein direkter Objektzeiger oder ein MTA-Proxy.

## <a name="best-practices-for-media-foundation-components"></a>Bewährte Methoden für Media Foundation-Komponenten

Es gibt zwei Kategorien von Media Foundation Objekten, die sich Gedanken über COM machen müssen. Einige Komponenten, z. B. Transformationen oder Bytestreamhandler, sind vollständige COM-Objekte, die von CLSID erstellt werden. Diese Objekte müssen den Regeln für COM-Apartments entsprechen, sowohl für prozess- als auch prozessübergreifende Media Foundation. Andere Media Foundation-Komponenten sind keine vollständigen COM-Objekte, benötigen jedoch COM-Proxys für die prozessübergreifende Wiedergabe. Objekte in dieser Kategorie umfassen Medienquellen und Aktivierungsobjekte. Diese Objekte können Apartmentprobleme ignorieren, wenn sie nur für prozessbearbeitende Media Foundation verwendet werden.

Obwohl nicht alle Media Foundation-Objekte COM-Objekte sind, werden alle Media Foundation Schnittstellen von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)abgeleitet. Daher müssen alle Media Foundation-Objekte **IUnknown** gemäß COM-Spezifikationen implementieren, einschließlich der Regeln für die Verweiszählung und [**QueryInterface.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) Alle Referenzzählungsobjekte sollten auch sicherstellen, dass [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) das Entladen des Moduls nicht zulässt, während die Objekte weiterhin beibehalten werden.

Media Foundation Komponenten können keine STA-Objekte sein. Viele Media Foundation-Objekte müssen überhaupt keine COM-Objekte sein. Wenn dies dere ist, können sie nicht im STA ausgeführt werden. Alle Media Foundation Komponenten müssen threadsicher sein. Einige Media Foundation-Objekte müssen auch freethreaded oder apartmentneutral sein. In der folgenden Tabelle werden die Anforderungen für benutzerdefinierte Schnittstellenimplementierungen angegeben:



| Schnittstelle                                                          | Kategorie            | Erforderliches Apartment       |
|--------------------------------------------------------------------|---------------------|--------------------------|
| [**ÜBER DIE AKTIONAKTIVIEREN**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)                                 | Prozessübergreifender Proxy | Freethreading oder neutral |
| [**GIGABYTEByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)               | COM-Objekt          | MTA                      |
| [**CONTENTContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) | Prozessübergreifender Proxy | Freethreading oder neutral |
| [**MANAGERSQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)                     | COM-Objekt          | Freethreading oder neutral |
| [**WFMEDIASOURCE**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                           | Prozessübergreifender Proxy | Freethreading oder neutral |
| [**MERSCHEMEHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)                       | COM-Objekt          | MTA                      |
| [**ÜBERLADENTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)                             | COM-Objekt          | Freethreading oder neutral |
| [**ÜBERTRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                               | COM-Objekt          | MTA                      |



 

Je nach Implementierung gibt es möglicherweise zusätzliche Anforderungen. Wenn eine Mediensenke beispielsweise eine andere Schnittstelle implementiert, die es der Anwendung ermöglicht, direkte Funktionsaufrufe an die Senke auszuführen, muss die Senke frei oder neutral sein, damit sie direkte prozessübergreifende Aufrufe verarbeiten kann. Jedes Objekt kann ein Freethreading sein. In dieser Tabelle werden die Mindestanforderungen angegeben.

Die empfohlene Methode zum Implementieren von Freethread-Objekten oder neutralen Objekten besteht darin, den Freethread-Marshaller zu aggregieren. Weitere Informationen finden Sie in der MSDN-Dokumentation zu [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler). In Übereinstimmung mit der Anforderung, STA-Objekte oder Proxys nicht an Media Foundation-APIs zu übergeben, müssen sich Freethread-Objekte nicht um das Marshallen von STA-Eingabezeigern in Freethread-Komponenten kümmern.

Komponenten, die die Long-Function-Arbeitswarteschlange **(MFASYNC \_ CALLBACK \_ QUEUE LONG \_ \_ FUNCTION)** verwenden, müssen mehr Sorgfalt walten. Threads in der long-Funktion workqueue erstellen ein eigenes STA. Komponenten, die die lange Funktion workqueue für Rückrufe verwenden, sollten das Erstellen von COM-Objekten in diesen Threads vermeiden und bei Bedarf darauf achten, Proxys an das STA zu marshallen.

## <a name="summary"></a>Zusammenfassung

Anwendungen haben eine einfachere Zeit, wenn sie mit Media Foundation aus einem MTA-Thread interagieren, aber es ist mit einiger Sorgfalt möglich, Media Foundation aus einem STA-Thread zu verwenden. Media Foundation keine STA-Komponenten verarbeitet, und Anwendungen sollten darauf achten, keine STA-Objekte an Media Foundation APIs zu übergeben. Einige Objekte haben zusätzliche Anforderungen, insbesondere Objekte, die in einer prozessübergreifenden Situation ausgeführt werden. Wenn Sie diese Richtlinien befolgen, können COM-Fehler, Deadlocks und unerwartete Verzögerungen bei der Medienverarbeitung vermieden werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Platform-APIs](media-foundation-platform-apis.md)
</dt> <dt>

[Media Foundation-Architektur](media-foundation-architecture.md)
</dt> </dl>

 

 
