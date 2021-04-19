---
description: Microsoft Media Foundation verwendet eine Mischung aus com-Konstrukten, ist aber keine vollständig com-basierte API.
ms.assetid: d58ca46f-8f3a-4a12-b948-1ea7ab568788
title: Media Foundation und com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb7d05bac6a3f4deef2c004c6980ef1351c3823
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106353260"
---
# <a name="media-foundation-and-com"></a>Media Foundation und com

Microsoft Media Foundation verwendet eine Mischung aus com-Konstrukten, ist aber keine vollständig com-basierte API. In diesem Thema wird die Interaktion zwischen com und Media Foundation beschrieben. Außerdem werden einige bewährte Methoden für die Entwicklung von Media Foundation-Plug-in-Komponenten definiert. Die folgenden Vorgehensweisen helfen Ihnen, einige häufige, aber feine Programmierfehler zu vermeiden.

-   [Bewährte Methoden für Anwendungen](#best-practices-for-applications)
-   [Bewährte Methoden für Media Foundation Komponenten](#best-practices-for-media-foundation-components)
-   [Zusammenfassung](#summary)
-   [Zugehörige Themen](#related-topics)

## <a name="best-practices-for-applications"></a>Bewährte Methoden für Anwendungen

In Media Foundation werden die asynchrone Verarbeitung und Rückrufe von [Arbeits Warteschlangen](work-queues.md)verarbeitet. Arbeits Warteschlangen verfügen immer über Multithread-Apartment-Threads (MTA), sodass eine Anwendung eine einfachere Implementierung hat, wenn Sie auch in einem MTA-Thread ausgeführt wird. Daher wird empfohlen, [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) mit dem **coinit- \_ Multithreaded** -Flag aufzurufen.

Mit Media Foundation werden keine STA-Objekte (Single Thread Apartment) in Arbeitswarteschlangen-Threads gemarshallt. Außerdem wird nicht sichergestellt, dass STA-invarianten verwaltet werden. Daher muss eine STA-Anwendung darauf achten, STA-Objekte oder-Proxys nicht an Media Foundation-APIs zu übergeben. Objekte, die nur STA-Objekte sind, werden in Media Foundation nicht unterstützt.

Wenn Sie über einen STA-Proxy für einen MTA oder ein frei Thread Objekt verfügen, kann das Objekt mithilfe eines Arbeits Warteschlangen Rückrufs an einen MTA-Proxy gemarshallt werden. Abhängig vom Objektmodell, das in der Registrierung für diese CLSID definiert ist, kann die [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion entweder einen Rohdaten Zeiger oder einen STA-Proxy zurückgeben. Wenn ein STA-Proxy zurückgegeben wird, dürfen Sie den Zeiger nicht an eine Media Foundation-API übergeben.

Angenommen, Sie möchten einen **IPropertyStore** -Zeiger an die [**imfsourceresolver:: beginkreateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) -Methode übergeben. Sie können **pscreatememorypropertystore** aufrufen, um den **IPropertyStore** -Zeiger zu erstellen. Wenn Sie von einem STA aufrufen, müssen Sie den Zeiger vor dem übergeben an **begincreateobjectfromurl** Mars Hallen.

Der folgende Code zeigt, wie ein STA-Proxy in eine Media Foundation-API gemarshallt wird.


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



Weitere Informationen zur globalen Schnittstellen Tabelle finden Sie unter [**iglobalinterfaketable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).

Wenn Sie Media Foundation Prozess intern verwenden, sind Objekte, die von Media Foundation Methoden und Funktionen zurückgegeben werden, direkte Zeiger auf das-Objekt. Bei prozessübergreifenden Media Foundation handelt es sich bei diesen Objekten möglicherweise um MTA-Proxys, die bei Bedarf in einen STA-Thread gemarshallt werden sollen. Ebenso sind Objekte, die innerhalb eines Rückrufs abgerufen werden – z. b. eine Topologie aus dem [mesessiontopologystatus](mesessiontopologystatus.md) -Ereignis – direkte Zeiger, wenn Media Foundation Prozess intern verwendet wird, aber MTA-Proxys sind, wenn Media Foundation Prozess übergreifend verwendet wird.

> [!Note]  
> Das häufigste Szenario für die Verwendung von Media Foundation Prozess übergreifender Prozess ist der [geschützte Medien Pfad](protected-media-path.md) (PMP). Diese Hinweise gelten jedoch für jede Situation, in der Media Foundation APIs über RPC verwendet werden.

 

Alle Implementierungen von [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) sollten MTA-kompatibel sein. Diese Objekte müssen überhaupt keine COM-Objekte sein. Wenn dies der Fall ist, können Sie nicht im STA ausgeführt werden. Die [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) -Funktion wird für einen MTA-Arbeits Warteschlangen Thread aufgerufen, und das angegebene [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) -Objekt ist entweder ein direkter Objekt Zeiger oder ein MTA-Proxy.

## <a name="best-practices-for-media-foundation-components"></a>Bewährte Methoden für Media Foundation Komponenten

Es gibt zwei Kategorien von Media Foundation-Objekten, die sich mit com befassen müssen. Einige Komponenten, z. b. Transformationen oder Byte Datenstrom Handler, sind vollständige COM-Objekte, die von der CLSID erstellt werden. Diese Objekte müssen den Regeln für com-Apartments für Prozess interne und prozessübergreifende Media Foundation entsprechen. Andere Media Foundation Komponenten sind keine vollständigen com-Objekte, benötigen aber com-Proxys für die prozessübergreifende Wiedergabe. Zu den Objekten in dieser Kategorie zählen Medienquellen und Aktivierungs Objekte. Diese Objekte können Apartment Probleme ignorieren, wenn Sie nur für Prozess interne Media Foundation verwendet werden.

Obwohl es sich nicht bei allen Media Foundation Objekten um COM-Objekte handelt, werden alle Media Foundation Schnittstellen von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)abgeleitet. Daher müssen alle Media Foundation Objekte **IUnknown** gemäß com-Spezifikationen implementieren, einschließlich der Regeln für die Verweis Zählung und [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Alle Verweis gezählten Objekte sollten außerdem sicherstellen, dass [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) das Entladen des Moduls nicht zulässt, während die Objekte weiterhin persistent gespeichert werden.

Media Foundation Komponenten können keine STA-Objekte sein. Viele Media Foundation Objekte müssen überhaupt keine COM-Objekte sein. Wenn dies der Fall ist, können Sie nicht im STA ausgeführt werden. Alle Media Foundation Komponenten müssen Thread sicher sein. Einige Media Foundation Objekte müssen auch frei Thread-oder Apartment neutral sein. In der folgenden Tabelle sind die Anforderungen für benutzerdefinierte Schnittstellen Implementierungen angegeben:



| Schnittstelle                                                          | Category            | Benötigtes Apartment       |
|--------------------------------------------------------------------|---------------------|--------------------------|
| [**Imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)                                 | Prozess übergreifender Proxy | Free-Thread oder neutral |
| [**IMF bytestreamhandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)               | COM-Objekt          | MTA                      |
| [**IMF contentprotection Manager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) | Prozess übergreifender Proxy | Free-Thread oder neutral |
| [**IMF-Manager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)                     | COM-Objekt          | Free-Thread oder neutral |
| [**Imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                           | Prozess übergreifender Proxy | Free-Thread oder neutral |
| [**IMF Schema Handler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)                       | COM-Objekt          | MTA                      |
| [**Imftopoloader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)                             | COM-Objekt          | Free-Thread oder neutral |
| [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                               | COM-Objekt          | MTA                      |



 

Abhängig von der Implementierung sind möglicherweise weitere Anforderungen erforderlich. Wenn eine Medien Senke z. b. eine andere Schnittstelle implementiert, die der Anwendung das Ausführen direkter Funktionsaufrufe an die Senke ermöglicht, muss die Senke frei Thread oder neutral sein, damit direkte prozessübergreifende Aufrufe möglich sind. Jedes Objekt ist möglicherweise frei Thread; in dieser Tabelle sind die Mindestanforderungen angegeben.

Die empfohlene Vorgehensweise zum Implementieren von frei Thread-oder neutralen Objekten besteht darin, den frei Hand Thread-Mars Haller zu aggregierten. Weitere Informationen finden Sie in der MSDN-Dokumentation zu [**cokreatefreethreadedmarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler). In Übereinstimmung mit der Anforderung, STA-Objekte oder-Proxys nicht an Media Foundation-APIs zu übergeben, müssen sich frei Thread Objekte keine Gedanken über das Marshalling von STA-Eingabe Zeigern in frei Thread Komponenten machen.

Komponenten, die die Arbeits Warteschlange für lange funktionsfähig verwenden (**mfasync- \_ Rückruf \_ Warteschlange \_ Long- \_ Funktion**), müssen mehr Sorgfalt walten lassen Threads in der Arbeits Warteschlange Long Function erstellen einen eigenen Sta. Komponenten, die die Long-Funktions Arbeits Warteschlange für Rückrufe verwenden, sollten das Erstellen von COM-Objekten in diesen Threads vermeiden und bei Bedarf darauf achten, Proxys auf dem STA zu Mars Hallen.

## <a name="summary"></a>Zusammenfassung

Anwendungen haben einen einfacheren Zeit, wenn Sie mit Media Foundation über einen MTA-Thread interagieren, aber es ist möglich, Media Foundation von einem STA-Thread zu verwenden. Media Foundation verarbeitet STA-Komponenten nicht, und Anwendungen sollten darauf achten, STA-Objekte nicht an Media Foundation-APIs zu übergeben. Einige Objekte haben zusätzliche Anforderungen, insbesondere Objekte, die in einer prozessübergreifenden Situation ausgeführt werden. Die folgenden Richtlinien helfen dabei, com-Fehler, Deadlocks und unerwartete Verzögerungen bei der Medienverarbeitung zu vermeiden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Plattform-APIs](media-foundation-platform-apis.md)
</dt> <dt>

[Media Foundation-Architektur](media-foundation-architecture.md)
</dt> </dl>

 

 
