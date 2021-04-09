---
description: Geräte Rollen für DirectSound-Anwendungen
ms.assetid: 7d82d67f-aad8-4e5b-ac65-87d75774e613
title: Geräte Rollen für DirectSound-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3829817f8b00c7288aceb8d0b6d418d5793ae580
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958144"
---
# <a name="device-roles-for-directsound-applications"></a>Geräte Rollen für DirectSound-Anwendungen

> [!Note]  
> Die [mmdevice-API](mmdevice-api.md) unterstützt Geräte Rollen. Die Benutzeroberfläche in Windows Vista implementiert jedoch keine Unterstützung für dieses Feature. Die Unterstützung von Benutzeroberflächen für Geräte Rollen kann in einer zukünftigen Version von Windows implementiert werden. Weitere Informationen finden Sie unter [Geräte Rollen in Windows Vista](device-roles-in-windows-vista.md).

 

Die DirectSound-API bietet keine Möglichkeit für eine Anwendung, das [audioendpunktgerät](audio-endpoint-devices.md) auszuwählen, das dem Benutzer einer bestimmten [Geräte Rolle](device-roles.md)zugewiesen wurde. In Windows Vista können die kernaudio-APIs jedoch in Verbindung mit einer DirectSound-Anwendung verwendet werden, um die Geräteauswahl basierend auf der Geräte Rolle zu aktivieren. Mithilfe der kernaudio-APIs kann die Anwendung das audioendpunktgerät identifizieren, das einer bestimmten Rolle zugewiesen ist, die DirectSound-Geräte-GUID für das Endpunktgerät abrufen und die Funktion **directsoundcreate** oder **directsoundcaptucreate** aufrufen, um eine **idirectsound** -oder **idirectsoundcapture** -Schnittstellen Instanz zu erstellen, die das Endpunkt Gerät kapselt Weitere Informationen zu DirectSound finden Sie in der Windows SDK-Dokumentation.

Das folgende Codebeispiel zeigt, wie Sie die DirectSound-Geräte-GUID für das Rendering-oder Aufzeichnungsgerät abrufen, das zurzeit einer bestimmten Geräte Rolle zugewiesen ist:


```C++
//-----------------------------------------------------------
// Get the DirectSound or DirectSoundCapture device GUID for
// an audio endpoint device. If flow = eRender, the function
// gets the DirectSound device GUID for the rendering device
// with the specified device role. If flow = eCapture, the
// function gets the DirectSoundCapture device GUID for the
// capture device with the specified device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

HRESULT GetDirectSoundGuid(EDataFlow flow, ERole role, GUID* pDevGuid)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IPropertyStore *pProps = NULL;

    PROPVARIANT var;
    PropVariantInit(&var);

    if (pDevGuid == NULL)
    {
        return E_POINTER;
    }

    // Get a device enumerator for the audio endpoint
    // devices in the system.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get the endpoint device with the specified dataflow
    // direction (eRender or eCapture) and device role.
    hr = pEnumerator->GetDefaultAudioEndpoint(flow, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->OpenPropertyStore(STGM_READ, &pProps);
    EXIT_ON_ERROR(hr)

    // Get the DirectSound or DirectSoundCapture device GUID
    // (in WCHAR string format) for the endpoint device.
    hr = pProps->GetValue(PKEY_AudioEndpoint_GUID, &var);
    EXIT_ON_ERROR(hr)

    // Convert the WCHAR string to a GUID structure.
    hr = CLSIDFromString(var.pwszVal, pDevGuid);
    EXIT_ON_ERROR(hr)

Exit:
    PropVariantClear(&var);
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    SAFE_RELEASE(pProps);
    return hr;
}
```



Im vorangehenden Codebeispiel akzeptiert die getdirectsoundguid-Funktion eine Datenfluss Richtung (eRender oder ecapture) und eine Geräte Rolle (econsole, emultimedia oder eCommunications) als Eingabeparameter. Der dritte Parameter ist ein Zeiger, über den die-Funktion eine Geräte-GUID schreibt, die die Anwendung als Eingabeparameter für die **directsoundcreate** -oder **directsoundcaptuup** -Funktion bereitstellen kann.

Im vorangehenden Codebeispiel wird die DirectSound-Geräte-GUID wie folgt abgerufen:

-   Erstellen einer [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstellen Instanz, die das audioendpunktgerät darstellt, das über die angegebene Datenfluss Richtung und die angegebene Geräte Rolle verfügt.
-   Öffnen des Eigenschaften Speicher des audioendpunktgeräts.
-   Die [**pkey \_ audioendpoint- \_ GUID**](pkey-audioendpoint-guid.md) -Eigenschaft wird aus dem Eigenschaften Speicher erhalten. Der Eigenschafts Wert ist eine Zeichen folgen Darstellung der DirectSound-Geräte-GUID für das audioendpunktgerät.
-   Aufrufen der [**CLSIDFromString**](https://www.bing.com/search?q=**CLSIDFromString**) -Funktion zum Konvertieren der Zeichen folgen Darstellung der Geräte-GUID in eine GUID-Struktur. Weitere Informationen zu **CLSIDFromString** finden Sie in der Windows SDK-Dokumentation.

Nachdem Sie eine Geräte-GUID von der getdirectsoundguid-Funktion erhalten haben, kann die Anwendung **directsoundcreate** oder **directsoundcaptuneu** mit dieser GUID aufrufen, um das DirectSound-Rendering oder das Erfassungsgerät zu erstellen, das das audioendpunktgerät kapselt. Wenn DirectSound ein Gerät auf diese Weise erstellt, wird der Audiostream des Geräts immer der Standard Sitzung zugewiesen – der prozessspezifischen Audiositzung, die durch den Sitzungs-GUID-Wert GUID NULL identifiziert wird \_ .

Wenn die Anwendung DirectSound erfordert, um den Stream einer prozessübergreifenden Audiositzung oder einer Sitzung mit einer Sitzungs-GUID ungleich **null** zuzuweisen, sollte die Methode " [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) " aufgerufen werden, um ein **idirectsound** -oder **idirectsoundcapture** -Objekt zu erstellen, anstatt die im vorangehenden Codebeispiel gezeigte Technik zu verwenden. Ein Codebeispiel, in dem veranschaulicht wird, wie Sie die Methode " **aktivieren** " verwenden, um eine prozessübergreifende Audiositzung oder eine Sitzungs-GUID ungleich **null** für einen Stream anzugeben, finden Sie unter [Geräte Rollen für DirectShow-Anwendungen](device-roles-for-directshow-applications.md). Das Codebeispiel in diesem Abschnitt zeigt, wie ein DirectShow-Filter erstellt wird, aber mit geringfügigen Änderungen kann der Code angepasst werden, um ein DirectSound-Gerät zu erstellen.

Die Funktion "getdirectsoundguid" im vorangehenden Codebeispiel ruft die [**cokreatinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion auf, um einen Enumerator für die audioendpunktgeräte im System zu erstellen. Wenn das aufrufende Programm die [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) -Funktion oder die [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) -Funktion nicht zum Initialisieren der com-Bibliothek aufgerufen hat, tritt beim **CoCreateInstance** -Aufruf ein Fehler auf. Weitere Informationen zu **cokreateinstance**, **CoInitialize** und **CoInitializeEx** finden Sie in der Windows SDK-Dokumentation.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Interoperabilität mit Legacy-audioapis](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
