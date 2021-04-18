---
description: Geräte Ereignisse
ms.assetid: b31500d6-a79d-4e6e-878e-6bd77055f1ad
title: Geräte Ereignisse (Core-audioapis)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0513fc49ee5f3cb2bfe95ca2330cb79b74720923
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344936"
---
# <a name="device-events-core-audio-apis"></a>Geräte Ereignisse (Core-audioapis)

Ein Geräte Ereignis benachrichtigt Clients über eine Änderung des Status eines [audioendpunktgeräts](audio-endpoint-devices.md) im System. Im folgenden finden Sie Beispiele für Geräte Ereignisse:

-   Der Benutzer aktiviert oder deaktiviert ein audioendpunktgerät von Device Manager oder von der Windows-Multimedia-Systemsteuerung Mmsys.cpl.
-   Der Benutzer fügt dem System einen Audioadapter hinzu oder entfernt einen Audioadapter aus dem System.
-   Der Benutzer bindet ein audioendpunktgerät mit der Erkennung von Jack-Presence in einen audiowagen ein oder entfernt ein audioendpunktgerät von einem solchen Jack.
-   Der Benutzer ändert die [Geräte Rolle](device-roles.md) , die einem Gerät zugewiesen ist.
-   Der Wert einer [Eigenschaft eines Geräts](device-properties.md) ändert sich.

Das Hinzufügen oder Entfernen eines audioadapters generiert Geräte Ereignisse für alle audioendpunktgeräte, die eine Verbindung mit dem Adapter herstellen. Die ersten vier Elemente in der vorangehenden Liste sind Beispiele für Gerätestatus Änderungen. Weitere Informationen zu den Geräte Zuständen von audioendpunktgeräten finden Sie unter [Geräte \_ Status xxx- \_ Konstanten](device-state-xxx-constants.md). Weitere Informationen zur Erkennung von Jack-Presence finden Sie unter [audioendpunktgeräte](audio-endpoint-devices.md).

Ein Client kann sich registrieren, um beim Auftreten von Geräte Ereignissen benachrichtigt zu werden. Als Reaktion auf diese Benachrichtigungen kann der Client die Art und Weise, in der ein bestimmtes Gerät verwendet wird, dynamisch ändern oder ein anderes Gerät auswählen, das für einen bestimmten Zweck verwendet werden soll.

Wenn eine Anwendung z. b. eine Audiospur über einen Satz von USB-sprechenden spielen und der Benutzer die Lautsprecher mit dem USB-Connector trennt, empfängt die Anwendung eine Benachrichtigung über das Geräte Ereignis. Wenn die Anwendung in Reaktion auf das Ereignis erkennt, dass eine Gruppe von Desktop Referenten mit dem integrierten Audioadapter auf der System-Hauptplatine verbunden ist, kann die Anwendung die Audiospur über die Desktop Referenten fortsetzen. In diesem Beispiel erfolgt der Übergang von USB-sprechenden zu Desktop Referenten automatisch, ohne dass der Benutzer eingreifen muss, indem er die Anwendung explizit umleitet.

Um sich für den Empfang von Geräte Benachrichtigungen zu registrieren, Ruft ein Client die [**immdeviceenumerator:: registerendpointnotificationcallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) -Methode auf. Wenn der Client keine Benachrichtigungen mehr erfordert, wird er durch Aufrufen der [**immdeviceenumerator:: unregisterendpointnotificationcallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) -Methode abgebrochen. Beide Methoden akzeptieren einen Eingabeparameter mit dem Namen " *pnotify*", bei dem es sich um einen Zeiger auf eine [**immnotificationclient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) -Schnittstellen Instanz handelt.

Die **immnotificationclient** -Schnittstelle wird von einem Client implementiert. Die-Schnittstelle enthält mehrere Methoden, von denen jede als Rückruf Routine für eine bestimmte Art von Geräte Ereignis fungiert. Wenn ein Geräte Ereignis in einem audioendpunktgerät auftritt, ruft das mmdevice-Modul die entsprechende Methode in der **immnotificationclient** -Schnittstelle jedes Clients auf, der zurzeit für den Empfang von Benachrichtigungen über Geräte Ereignisse registriert ist. Diese Aufrufe übergeben eine Beschreibung des Ereignisses an die Clients. Weitere Informationen finden Sie unter [**immnotificationclient-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).

Ein Client, der für den Empfang von Benachrichtigungen über Geräte Ereignisse registriert ist, erhält Benachrichtigungen zu allen Arten von Geräte Ereignissen, die auf allen audioendpunktgeräten im System auftreten. Wenn ein Client nur an bestimmten Ereignis Typen oder auf bestimmten Geräten interessiert ist, sollten die Methoden in der **immnotificationclient** -Implementierung die Ereignisse entsprechend filtern.

Die Windows SDK enthält Beispiele, die mehrere Implementierungen für die [**immnotificationclient-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient)enthalten. Weitere Informationen finden Sie unter [SDK-Beispiele, die die Kerndatei-APIs verwenden](sdk-samples-that-use-the-core-audio-apis.md).

Im folgenden Codebeispiel wird eine mögliche Implementierung der **immnotificationclient** -Schnittstelle veranschaulicht:


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



Die cmmnotificationclient-Klasse im vorangehenden Codebeispiel ist eine Implementierung der **immnotificationclient** -Schnittstelle. Da **immnotificationclient** von **IUnknown** erbt, enthält die Klassendefinition Implementierungen der **IUnknown** -Methoden **adressf**, **Release** und **QueryInterface**. Die übrigen öffentlichen Methoden in der Klassendefinition sind spezifisch für die **immnotificationclient** -Schnittstelle. Diese Methoden werden im Anschluss beschrieben:

-   **Ondefaultdevicechanged**, das aufgerufen wird, wenn der Benutzer die Geräte Rolle eines audioendpunktgeräts ändert.
-   **Ondeviceadded**, das aufgerufen wird, wenn der Benutzer dem System ein audioendpunktgerät hinzufügt.
-   **Ondeviceremoved**, das aufgerufen wird, wenn der Benutzer ein audioendpunktgerät aus dem System entfernt.
-   **Ondevicestatechanged**, das aufgerufen wird, wenn sich der Gerätestatus eines audioendpunktgeräts ändert. (Weitere Informationen zu Geräte Zuständen finden Sie unter [Geräte \_ Status \_ xxx-Konstanten](device-state-xxx-constants.md).)
-   **OnPropertyValueChanged**, das aufgerufen wird, wenn sich der Wert einer Eigenschaft eines audioendpunkt-Geräts ändert.

Jede dieser Methoden nimmt einen Eingabeparameter ( *pwstraudeviceid*) an, der ein Zeiger auf eine Endpunkt-ID-Zeichenfolge ist. Die Zeichenfolge identifiziert das audioendpunktgerät, in dem das Geräte Ereignis aufgetreten ist.

Im vorangehenden Codebeispiel \_ ist printdevicename eine private Methode in der cmmnotificationclient-Klasse, die den anzeigen amen des Geräts ausgibt. \_Printdevicename nimmt die Endpunkt-ID-Zeichenfolge als Eingabeparameter an. Sie übergibt die Zeichenfolge an die [**immdeviceenumerator:: getdevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) -Methode. **Getdevice** erstellt ein Endpunkt-Geräte Objekt zur Darstellung des Geräts und stellt die [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle für dieses Objekt bereit. Als nächstes \_ Ruft printdevicename die Methode " [**immdevice:: openpropertystore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) " auf, um die **IPropertyStore** -Schnittstelle in den Eigenschaften Speicher des Geräts abzurufen. Zum Schluss \_ Ruft printdevicename die **IPropertyStore:: GetItem** -Methode auf, um die Eigenschaft "Anzeige Name" des Geräts zu erhalten. Weitere Informationen zu **IPropertyStore** finden Sie in der Windows SDK-Dokumentation.

Zusätzlich zu den Geräte Ereignissen können Clients sich registrieren, um Benachrichtigungen über audiositzungsereignisse und Ereignisse von Endpunkt Ereignissen zu empfangen. Weitere Informationen finden Sie unter [**iaudiosessionevents-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) und [**iaudioendpointvolumecallback-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioendpunktgeräte](audio-endpoint-devices.md)
</dt> </dl>

 

 



