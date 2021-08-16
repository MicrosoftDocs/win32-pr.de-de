---
description: Geräteereignisse
ms.assetid: b31500d6-a79d-4e6e-878e-6bd77055f1ad
title: Geräteereignisse (Core Audio APIs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61538bd7d8d297b52a321f446bb11c3e1365e549a3c2947b55538730c1660c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407028"
---
# <a name="device-events-core-audio-apis"></a>Geräteereignisse (Core Audio APIs)

Ein Geräteereignis benachrichtigt Clients über eine Änderung des Status eines [Audioendpunktgeräts](audio-endpoint-devices.md) im System. Im Folgenden sind Beispiele für Geräteereignisse aufgeführt:

-   Der Benutzer aktiviert oder deaktiviert ein Audioendpunktgerät über Geräte-Manager oder über die Windows Multimedia-Systemsteuerung Mmsys.cpl.
-   Der Benutzer fügt dem System einen Audioadapter hinzu oder entfernt einen Audioadapter aus dem System.
-   Der Benutzer schließt ein Audioendpunktgerät an eine Audiobuchse mit Jack-Presence-Erkennung an oder entfernt ein Audioendpunktgerät aus einer solchen Buchse.
-   Der Benutzer ändert die [Geräterolle,](device-roles.md) die einem Gerät zugewiesen ist.
-   Der Wert einer [Eigenschaft eines Geräts](device-properties.md) ändert sich.

Das Hinzufügen oder Entfernen eines Audioadapters generiert Geräteereignisse für alle Audioendpunktgeräte, die eine Verbindung mit dem Adapter herstellen. Die ersten vier Elemente in der obigen Liste sind Beispiele für Gerätezustandsänderungen. Weitere Informationen zu den Gerätezuständen von Audioendpunktgeräten finden Sie unter [DEVICE \_ STATE \_ XXX-Konstanten.](device-state-xxx-constants.md) Weitere Informationen zur Erkennung von Jack-Presence finden Sie unter [Audioendpunktgeräte.](audio-endpoint-devices.md)

Ein Client kann registriert werden, um benachrichtigt zu werden, wenn Geräteereignisse auftreten. Als Reaktion auf diese Benachrichtigungen kann der Client dynamisch ändern, wie er ein bestimmtes Gerät verwendet, oder ein anderes Gerät auswählen, das für einen bestimmten Zweck verwendet werden soll.

Wenn eine Anwendung beispielsweise eine Audiospur über eine Reihe von USB-Lautsprechern wiedergibt und der Benutzer die Lautsprecher vom USB-Connector trennt, empfängt die Anwendung eine Geräteereignisbenachrichtigung. Wenn die Anwendung als Reaktion auf das Ereignis erkennt, dass eine Gruppe von Desktoplautsprechenden mit dem integrierten Audioadapter auf der Hauptplatine des Systems verbunden ist, kann die Anwendung die Wiedergabe der Audiospur über die Desktoplaute fortsetzen. In diesem Beispiel erfolgt der Übergang von USB-Lautsprechern zu Desktop-Lautsprechern automatisch, ohne dass der Benutzer eingreifen muss, indem er die Anwendung explizit umleitet.

Um sich für den Empfang von Gerätebenachrichtigungen zu registrieren, ruft ein Client die [**IMMDeviceEnumerator::RegisterEndpointNotificationCallback-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) auf. Wenn der Client keine Benachrichtigungen mehr benötigt, bricht er sie ab, indem er die [**IMMDeviceEnumerator::UnregisterEndpointNotificationCallback-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) aufruft. Beide Methoden verwenden einen Eingabeparameter namens *pNotify,* der ein Zeiger auf eine [**IMMNotificationClient-Schnittstelleninstanz**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) ist.

Die **IMMNotificationClient-Schnittstelle** wird von einem Client implementiert. Die -Schnittstelle enthält mehrere Methoden, von denen jede als Rückrufroutine für einen bestimmten Geräteereignistyp dient. Wenn ein Geräteereignis auf einem Audioendpunktgerät auftritt, ruft das MMDevice-Modul die entsprechende Methode in der **IMMNotificationClient-Schnittstelle** jedes Clients auf, der derzeit für den Empfang von Geräteereignisbenachrichtigungen registriert ist. Diese Aufrufe übergeben eine Beschreibung des Ereignisses an die Clients. Weitere Informationen finden Sie unter [**IMMNotificationClient-Schnittstelle.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient)

Ein Client, der für den Empfang von Geräteereignisbenachrichtigungen registriert ist, empfängt Benachrichtigungen aller Arten von Geräteereignissen, die auf allen Audioendpunktgeräten im System auftreten. Wenn ein Client nur an bestimmten Ereignistypen oder an bestimmten Geräten interessiert ist, sollten die Methoden in seiner **IMMNotificationClient-Implementierung** die Ereignisse entsprechend filtern.

Das Windows SDK enthält Beispiele, die mehrere Implementierungen für die [**IMMNotificationClient-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient)enthalten. Weitere Informationen finden Sie unter [SDK-Beispiele, die die Core Audio-APIs verwenden.](sdk-samples-that-use-the-core-audio-apis.md)

Das folgende Codebeispiel zeigt eine mögliche Implementierung der **IMMNotificationClient-Schnittstelle:**


```C++
//-----------------------------------------------------------
// Example implementation of IMMNotificationClient interface.
// When the status of audio endpoint devices change, the
// MMDevice module calls these methods to notify the client.
//-----------------------------------------------------------

#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

class CMMNotificationClient : public IMMNotificationClient
{
    LONG _cRef;
    IMMDeviceEnumerator *_pEnumerator;

    // Private function to print device-friendly name
    HRESULT _PrintDeviceName(LPCWSTR  pwstrId);

public:
    CMMNotificationClient() :
        _cRef(1),
        _pEnumerator(NULL)
    {
    }

    ~CMMNotificationClient()
    {
        SAFE_RELEASE(_pEnumerator)
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(
                                REFIID riid, VOID **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IMMNotificationClient) == riid)
        {
            AddRef();
            *ppvInterface = (IMMNotificationClient*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Callback methods for device-event notifications.

    HRESULT STDMETHODCALLTYPE OnDefaultDeviceChanged(
                                EDataFlow flow, ERole role,
                                LPCWSTR pwstrDeviceId)
    {
        char  *pszFlow = "?????";
        char  *pszRole = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (flow)
        {
        case eRender:
            pszFlow = "eRender";
            break;
        case eCapture:
            pszFlow = "eCapture";
            break;
        }

        switch (role)
        {
        case eConsole:
            pszRole = "eConsole";
            break;
        case eMultimedia:
            pszRole = "eMultimedia";
            break;
        case eCommunications:
            pszRole = "eCommunications";
            break;
        }

        printf("  -->New default device: flow = %s, role = %s\n",
               pszFlow, pszRole);
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceAdded(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Added device\n");
        return S_OK;
    };

    HRESULT STDMETHODCALLTYPE OnDeviceRemoved(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Removed device\n");
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceStateChanged(
                                LPCWSTR pwstrDeviceId,
                                DWORD dwNewState)
    {
        char  *pszState = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (dwNewState)
        {
        case DEVICE_STATE_ACTIVE:
            pszState = "ACTIVE";
            break;
        case DEVICE_STATE_DISABLED:
            pszState = "DISABLED";
            break;
        case DEVICE_STATE_NOTPRESENT:
            pszState = "NOTPRESENT";
            break;
        case DEVICE_STATE_UNPLUGGED:
            pszState = "UNPLUGGED";
            break;
        }

        printf("  -->New device state is DEVICE_STATE_%s (0x%8.8x)\n",
               pszState, dwNewState);

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnPropertyValueChanged(
                                LPCWSTR pwstrDeviceId,
                                const PROPERTYKEY key)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Changed device property "
               "{%8.8x-%4.4x-%4.4x-%2.2x%2.2x-%2.2x%2.2x%2.2x%2.2x%2.2x%2.2x}#%d\n",
               key.fmtid.Data1, key.fmtid.Data2, key.fmtid.Data3,
               key.fmtid.Data4[0], key.fmtid.Data4[1],
               key.fmtid.Data4[2], key.fmtid.Data4[3],
               key.fmtid.Data4[4], key.fmtid.Data4[5],
               key.fmtid.Data4[6], key.fmtid.Data4[7],
               key.pid);
        return S_OK;
    }
};

// Given an endpoint ID string, print the friendly device name.
HRESULT CMMNotificationClient::_PrintDeviceName(LPCWSTR pwstrId)
{
    HRESULT hr = S_OK;
    IMMDevice *pDevice = NULL;
    IPropertyStore *pProps = NULL;
    PROPVARIANT varString;

    CoInitialize(NULL);
    PropVariantInit(&varString);

    if (_pEnumerator == NULL)
    {
        // Get enumerator for audio endpoint devices.
        hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                              NULL, CLSCTX_INPROC_SERVER,
                              __uuidof(IMMDeviceEnumerator),
                              (void**)&_pEnumerator);
    }
    if (hr == S_OK)
    {
        hr = _pEnumerator->GetDevice(pwstrId, &pDevice);
    }
    if (hr == S_OK)
    {
        hr = pDevice->OpenPropertyStore(STGM_READ, &pProps);
    }
    if (hr == S_OK)
    {
        // Get the endpoint device's friendly-name property.
        hr = pProps->GetValue(PKEY_Device_FriendlyName, &varString);
    }
    printf("----------------------\nDevice name: \"%S\"\n"
           "  Endpoint ID string: \"%S\"\n",
           (hr == S_OK) ? varString.pwszVal : L"null device",
           (pwstrId != NULL) ? pwstrId : L"null ID");

    PropVariantClear(&varString);

    SAFE_RELEASE(pProps)
    SAFE_RELEASE(pDevice)
    CoUninitialize();
    return hr;
}
```



Die CMMNotificationClient-Klasse im vorherigen Codebeispiel ist eine Implementierung der **IMMNotificationClient-Schnittstelle.** Da **IMMNotificationClient** von **IUnknown** erbt, enthält die Klassendefinition Implementierungen der **IUnknown-Methoden** **AddRef,** **Release** und **QueryInterface.** Die verbleibenden öffentlichen Methoden in der Klassendefinition sind spezifisch für die **IMMNotificationClient-Schnittstelle.** Diese Methoden werden im Anschluss beschrieben:

-   **OnDefaultDeviceChanged**, das aufgerufen wird, wenn der Benutzer die Geräterolle eines Audioendpunktgeräts ändert.
-   **OnDeviceAdded**, das aufgerufen wird, wenn der Benutzer dem System ein Audioendpunktgerät hinzufügt.
-   **OnDeviceRemoved**, das aufgerufen wird, wenn der Benutzer ein Audioendpunktgerät aus dem System entfernt.
-   **OnDeviceStateChanged**, das aufgerufen wird, wenn sich der Gerätestatus eines Audioendpunktgeräts ändert. (Weitere Informationen zu Gerätezuständen finden Sie unter [DEVICE \_ STATE \_ XXX-Konstanten.)](device-state-xxx-constants.md)
-   **OnPropertyValueChanged**, das aufgerufen wird, wenn sich der Wert einer Eigenschaft eines Audioendpunktgeräts ändert.

Jede dieser Methoden verwendet einen Eingabeparameter, *pwstrDeviceId,* der ein Zeiger auf eine Endpunkt-ID-Zeichenfolge ist. Die Zeichenfolge identifiziert das Audioendpunktgerät, in dem das Geräteereignis aufgetreten ist.

Im vorherigen Codebeispiel \_ ist PrintDeviceName eine private Methode in der CMMNotificationClient-Klasse, die den Anzeigenamen des Geräts ausdrückt. \_PrintDeviceName verwendet die Endpunkt-ID-Zeichenfolge als Eingabeparameter. Die Zeichenfolge wird an die [**IMMDeviceEnumerator::GetDevice-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) übergeben. **GetDevice** erstellt ein Endpunktgeräteobjekt, das das Gerät darstellt, und stellt die [**IMMDevice-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) für dieses Objekt bereit. Als Nächstes \_ ruft PrintDeviceName die [**IMMDevice::OpenPropertyStore-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) auf, um die **IPropertyStore-Schnittstelle** in den Eigenschaftenspeicher des Geräts abzurufen. Schließlich \_ ruft PrintDeviceName die **IPropertyStore::GetItem-Methode** auf, um die Anzeigenameneigenschaft des Geräts abzurufen. Weitere Informationen zu **IPropertyStore** finden Sie in der Windows SDK-Dokumentation.

Zusätzlich zu Geräteereignissen können sich Clients registrieren, um Benachrichtigungen über Audiositzungsereignisse und Endpunktvolumeereignisse zu empfangen. Weitere Informationen finden Sie unter [**IAudioSessionEvents-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) und [**IAudioEndpointVolumeCallback-Schnittstelle.**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioendpunktgeräte](audio-endpoint-devices.md)
</dt> </dl>

 

 



