---
description: So erhalten Sie Ereignisse aus der Netzwerkquelle
ms.assetid: 46869f52-323c-41ec-95f7-e7e5d177b782
title: So erhalten Sie Ereignisse aus der Netzwerkquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100241b069ae8976c20c68b6055571d5ff1e5c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753584"
---
# <a name="how-to-get-events-from-the-network-source"></a>So erhalten Sie Ereignisse aus der Netzwerkquelle

Der Quell Konflikt Löser ermöglicht einer Anwendung das Erstellen einer Netzwerkquelle und das Öffnen einer Verbindung mit einer bestimmten URL. Die Netzwerkquelle löst Ereignisse aus, um den Anfang und das Ende des asynchronen Vorgangs zum Öffnen einer Verbindung zu markieren. Eine Anwendung kann sich für diese Ereignisse mithilfe der [**IMF sourceopenmonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) -Schnittstelle registrieren.

Diese Schnittstelle macht die [**IMF sourceopenmonitor:: onsourceevent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) -Methode verfügbar, die von der Netzwerkquelle direkt aufgerufen wird, wenn die URL asynchron geöffnet wird. Die Netzwerkquelle benachrichtigt die Anwendung, wenn Sie mit dem Öffnen der URL beginnt, indem das [meconnectstart](meconnectstart.md) -Ereignis aufgerufen wird. Die Netzwerkquelle löst dann das [meconnectend](meconnectend.md) -Ereignis aus, wenn der Öffnungsvorgang abgeschlossen ist.

> [!Note]  
> Um diese Ereignisse an die Anwendung zu senden, verwendet die Netzwerkquelle die [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle nicht, da diese Ereignisse vor der Erstellung der Netzwerkquelle ausgelöst werden. Die Anwendung kann alle anderen Netzwerk Quell Ereignisse mithilfe der **IMF mediaeventgenerator** -Schnittstelle der Medien Sitzung erhalten.

 

## <a name="to-get-events-from-the-network-source"></a>So erhalten Sie Ereignisse aus der Netzwerkquelle

1.  Implementieren Sie die [**IMF sourceopenmonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) -Schnittstelle. Führen Sie in ihrer Implementierung der [**IMF sourceopenmonitor:: onsourceevent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) -Methode die folgenden Schritte aus:
    1.  Rufen Sie den Ereignis Status durch Aufrufen von [**imfmediaevent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus)ab. Diese Methode gibt an, ob der Vorgang, der das Ereignis ausgelöst hat, z. b. ein quellresolver-Methodenaufrufe, erfolgreich war. Wenn der Vorgang nicht erfolgreich ist, ist der Status ein Fehlercode.
    2.  Verarbeiten Sie das Ereignis basierend auf dem Ereignistyp: [meconnectstart](meconnectstart.md) oder [meconnectend](meconnectend.md), den die Anwendung durch Aufrufen von [**imfmediaevent:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype)abrufen kann.
2.  Konfigurieren Sie ein Schlüssel-Wert-Paar in einem Eigenschaften Speicher Objekt zum Speichern eines Zeigers auf die [**imfsourceopenmonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) -Implementierung, die in Schritt 1 beschrieben wird.
    1.  Erstellen Sie ein Eigenschaften Speicher Objekt, indem Sie die **pscreatememorypropertystore** -Funktion aufrufen.
    2.  Legen Sie die [**mfpkey \_ sourceopenmonitor**](mfpkey-sourceopenmonitor-property.md) -Eigenschaft in einer **PropertyKey** -Struktur fest.
    3.  Geben Sie den \_ Wert "VT Unknown Type Data" in einer **PROPVARIANT** -Struktur an, indem Sie den **IUnknown** -Zeiger auf die Implementierung der Anwendung der [**imfsourceopenmonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) -Schnittstelle festlegen.
    4.  Legen Sie das Schlüssel-Wert-Paar im Eigenschaften Speicher durch Aufrufen von **IPropertyStore:: SetValue** fest.
3.  Übergeben Sie den Eigenschafts Speicher Zeiger an die Quell Auflösungs Methoden, die die Anwendung verwendet, um die Netzwerkquelle zu erstellen, z. b. [**imfsourceresolver:: deateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) und andere.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird gezeigt, wie Sie die [**imfsourceopenmonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) -Schnittstelle implementieren, um Ereignisse aus der Netzwerkquelle abzurufen.


```C++
class CSourceOpenMonitor : public IMFSourceOpenMonitor
{
public:
    CSourceOpenMonitor () : m_cRef(1) { }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CSourceOpenMonitor, IMFSourceOpenMonitor),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        // For thread safety, return a temporary variable.
        return cRef;
    }


    STDMETHODIMP OnSourceEvent(IMFMediaEvent* pEvent)
    {
        MediaEventType eventType = MEUnknown;   // Event type
        HRESULT hrStatus = S_OK;                // Event status

        // Get the event type.
        HRESULT hr = pEvent->GetType(&eventType);

        // Get the event status. If the operation that triggered the event
        // did not succeed, the status is a failure code.
        if (SUCCEEDED(hr))
        {
            hr = pEvent->GetStatus(&hrStatus);
        }

        if (FAILED(hrStatus))
        {
            hr = hrStatus;
        }

        if (SUCCEEDED(hr))
        {
            // Switch on the event type.
            switch(eventType)
            {
                case MEConnectStart:
                    // The application does something. (Not shown.)
                    OutputDebugString(L"Connecting...\n");
                    break;

                case MEConnectEnd:
                    // The application does something. (Not shown.)
                    OutputDebugString(L"Connect End.\n");
                    break;
            }
        }
        else
        {
            // Event failed.
            // The application handled a failure. (Not shown.)
        }
        return S_OK;
    }
private:
    long    m_cRef;
};
```



Im folgenden Beispiel wird gezeigt, wie die [**mfpkey \_ sourceopenmonitor**](mfpkey-sourceopenmonitor-property.md) -Eigenschaft in der Netzwerkquelle festgelegt wird, wenn Sie die URL öffnen:


```C++
HRESULT CreateMediaSourceWithSourceOpenMonitor(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CSourceOpenMonitor *pMonitor = new (std::nothrow) CSourceOpenMonitor();

    if (pMonitor == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pMonitor->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(MFPKEY_SourceOpenMonitor, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pMonitor);

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



