---
description: How to Get Events from the Network Source
ms.assetid: 46869f52-323c-41ec-95f7-e7e5d177b782
title: How to Get Events from the Network Source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ec85877a928a2f63648ec0dedded1c383988bf80a4182f83062fd296e68bcb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958320"
---
# <a name="how-to-get-events-from-the-network-source"></a>How to Get Events from the Network Source

Mit dem Quellre resolver kann eine Anwendung eine Netzwerkquelle erstellen und eine Verbindung mit einer bestimmten URL herstellen. Die Netzwerkquelle löst Ereignisse aus, um den Anfang und das Ende des asynchronen Vorgangs zum Öffnen einer Verbindung zu markieren. Eine Anwendung kann sich für diese Ereignisse registrieren, indem [**sie die BENUTZEROBERFLÄCHENQUELLEOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) verwendet.

Diese Schnittstelle macht die [**METHODE ASYNCHRONOUSSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) verfügbar, die die Netzwerkquelle direkt aufruft, wenn sie die URL asynchron öffnet. Die Netzwerkquelle benachrichtigt die Anwendung, wenn sie mit dem Öffnen der URL beginnt, indem sie das [MEConnectStart-Ereignis ausdrängt.](meconnectstart.md) Die Netzwerkquelle löst dann das [MEConnectEnd-Ereignis](meconnectend.md) aus, wenn der Open-Vorgang abgeschlossen ist.

> [!Note]  
> Um diese Ereignisse an die Anwendung zu senden, verwendet die Netzwerkquelle nicht die [**BENUTZEROBERFLÄCHEMEDIAEventGenerator-Schnittstelle,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) da diese Ereignisse ausgelöst werden, bevor die Netzwerkquelle erstellt wird. Die Anwendung kann alle anderen Netzwerkquellenereignisse mithilfe der **MEDIAMediaEventGenerator-Schnittstelle** der Media Session erhalten.

 

## <a name="to-get-events-from-the-network-source"></a>So erhalten Sie Ereignisse aus der Netzwerkquelle

1.  Implementieren Sie [**die SCHNITTSTELLE VERFSourceOpenMonitor.**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) Gehen Sie in Ihrer [**Implementierung der METHODE DURCHSOURCEOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) wie folgt vor:
    1.  Rufen Sie den Ereignisstatus ab, indem [**Sie DENKMediaEvent::GetStatus aufrufen.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) Diese Methode gibt an, ob der Vorgang, der das Ereignis ausgelöst hat, z. B. ein Aufruf der Quellrelösermethode, erfolgreich war. Wenn der Vorgang nicht erfolgreich ist, ist der Status ein Fehlercode.
    2.  Verarbeiten Sie das Ereignis basierend auf dem [Ereignistyp: MEConnectStart](meconnectstart.md) oder [MEConnectEnd,](meconnectend.md)den die Anwendung durch Aufrufen von [**ZUEgeMediaEvent::GetType erhalten kann.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype)
2.  Konfigurieren Sie ein Schlüssel-Wert-Paar in einem Eigenschaftsspeicherobjekt, um einen Zeiger auf die IN Schritt 1 beschriebene [**IMPLEMENTIERUNG VON DURCHSSOURCEOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) zu speichern.
    1.  Erstellen Sie ein Eigenschaftenspeicherobjekt, indem Sie die **PSCreateMemoryPropertyStore-Funktion** aufrufen.
    2.  Legen Sie die [**MFPKEY \_ SourceOpenMonitor-Eigenschaft**](mfpkey-sourceopenmonitor-property.md) in einer **PROPERTYKEY-Struktur** fest.
    3.  Geben Sie den VT UNKNOWN-Typdatenwert in einer PROPVARIANT-Struktur an, indem Sie den IUnknown-Zeiger auf die Anwendungsimplementierung der \_ [**BESSOURCEOpenMonitor-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)  festlegen. 
    4.  Legen Sie das Schlüssel-Wert-Paar im Eigenschaftenspeicher fest, indem **Sie IPropertyStore::SetValue aufrufen.**
3.  Übergeben Sie den Eigenschaftsspeicherzeiger an die Methoden des Quellresolvers, die die Anwendung zum Erstellen der Netzwerkquelle verwendet, z. B. [**DURCHSOURCEResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) und andere.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt, wie sie die [**BENUTZEROBERFLÄCHESourceOpenMonitor-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) implementiert, um Ereignisse aus der Netzwerkquelle zu erhalten.


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



Das folgende Beispiel zeigt, wie die [**MFPKEY \_ SourceOpenMonitor-Eigenschaft**](mfpkey-sourceopenmonitor-property.md) für die Netzwerkquelle festgelegt wird, wenn Sie die URL öffnen:


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

 

 



