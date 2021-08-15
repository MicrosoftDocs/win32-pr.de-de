---
description: Geräterollen für DirectSound-Anwendungen
ms.assetid: 7d82d67f-aad8-4e5b-ac65-87d75774e613
title: Geräterollen für DirectSound-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3037b767d7ddfb96d892c789608f23523efed465535258c336496f3f23d82f19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957329"
---
# <a name="device-roles-for-directsound-applications"></a>Geräterollen für DirectSound-Anwendungen

> [!Note]  
> Die [MMDevice-API unterstützt](mmdevice-api.md) Geräterollen. Die Benutzeroberfläche in Windows Vista implementiert jedoch keine Unterstützung für dieses Feature. Die Benutzeroberflächenunterstützung für Geräterollen wird möglicherweise in einer zukünftigen Version von Windows. Weitere Informationen finden Sie unter [Geräterollen in Windows Vista](device-roles-in-windows-vista.md).

 

Die DirectSound-API bietet einer Anwendung keine [](audio-endpoint-devices.md) Möglichkeit, das Audioendpunktgerät auszuwählen, das der Benutzer einer bestimmten [Geräterolle zugewiesen hat.](device-roles.md) In Windows Vista können die Kernaudio-APIs jedoch in Verbindung mit einer DirectSound-Anwendung verwendet werden, um die Geräteauswahl basierend auf der Geräterolle zu aktivieren. Mithilfe der Kernaudio-APIs kann die Anwendung das Audioendpunktgerät identifizieren, das einer bestimmten Rolle zugewiesen ist, die DirectSound-Geräte-GUID für das Endpunktgerät erhalten und die **DirectSoundCreate-** oder **DirectSoundCaptureCreate-Funktion** aufrufen, um eine **IDirectSound-** oder **IDirectSoundCapture-Schnittstelleninstanz** zu erstellen, die das Endpunktgerät kapselt. Weitere Informationen zu DirectSound finden Sie in der dokumentation Windows SDK.

Das folgende Codebeispiel zeigt, wie Sie die DirectSound-Geräte-GUID für das Rendering- oder Erfassungsgerät abrufen, das derzeit einer bestimmten Geräterolle zugewiesen ist:


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



Im vorherigen Codebeispiel akzeptiert die GetDirectSoundGuid-Funktion eine Datenflussrichtung (eRender oder eCapture) und eine Geräterolle (eConsole, eMultimedia oder eCommunications) als Eingabeparameter. Der dritte Parameter ist ein Zeiger, über den die Funktion eine Geräte-GUID schreibt, die die Anwendung als Eingabeparameter für die **DirectSoundCreate-** oder **DirectSoundCaptureCreate-Funktion angeben** kann.

Im vorangehenden Codebeispiel wird die DirectSound-Geräte-GUID durch Folgendes erhalten:

-   Erstellen einer [**IMMDevice-Schnittstelleninstanz,**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) die das Audioendpunktgerät darstellt, das über die angegebene Datenflussrichtung und Geräterolle verfügt.
-   Öffnen des Eigenschaftenspeichers des Audioendpunktgeräts.
-   Abrufen der [**PKEY \_ AudioEndpoint \_ GUID-Eigenschaft**](pkey-audioendpoint-guid.md) aus dem Eigenschaftenspeicher. Der Eigenschaftswert ist eine Zeichenfolgendarstellung der DirectSound-Geräte-GUID für das Audioendpunktgerät.
-   Aufrufen der [**CLSIDFromString-Funktion,**](https://www.bing.com/search?q=**CLSIDFromString**) um die Zeichenfolgendarstellung der Geräte-GUID in eine GUID-Struktur zu konvertieren. Weitere Informationen zu **CLSIDFromString finden** Sie in der Windows SDK-Dokumentation.

Nach dem Abrufen einer Geräte-GUID aus der GetDirectSoundGuid-Funktion kann die Anwendung **DirectSoundCreate** oder **DirectSoundCaptureCreate** mit dieser GUID aufrufen, um das DirectSound-Rendering- oder -Erfassungsgerät zu erstellen, das das Audioendpunktgerät kapselt. Wenn DirectSound auf diese Weise ein Gerät erstellt, wird der Audiodatenstrom des Geräts immer der Standardsitzung zugewiesen– der prozessspezifischen Audiositzung, die durch den GUID-Wert GUID NULL der Sitzung identifiziert \_ wird.

Wenn die Anwendung erfordert, dass DirectSound den Stream einer prozessübergreifenden Audiositzung oder einer Sitzung mit einer Nicht-NULL-Sitzungs-GUID zuweisst, sollte sie die [**IMMDevice::Activate-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) aufrufen, um ein **IDirectSound-** oder **IDirectSoundCapture-Objekt** zu erstellen, anstatt die im vorherigen Codebeispiel gezeigte Technik zu verwenden. Ein Codebeispiel, das zeigt, wie die **Activate-Methode** zum Angeben einer prozessübergreifenden Audiositzung oder einer Sitzungs-GUID ohne NULL für einen Stream verwendet wird, finden Sie unter Geräterollen für [DirectShow-Anwendungen.](device-roles-for-directshow-applications.md) Das Codebeispiel in diesem Abschnitt zeigt, wie Sie einen DirectShow-Filter erstellen, aber mit geringfügigen Änderungen kann der Code angepasst werden, um ein DirectSound-Gerät zu erstellen.

Die GetDirectSoundGuid-Funktion im vorherigen Codebeispiel ruft die [**CoCreateInstance-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um einen Enumerator für die Audioendpunktgeräte im System zu erstellen. Sofern das aufrufende Programm zuvor weder die [**CoInitialize-**](/windows/desktop/api/objbase/nf-objbase-coinitialize) noch [**die CoInitializeEx-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) aufgerufen hat, um die COM-Bibliothek zu initialisieren, ist der **CoCreateInstance-Aufruf** nicht fehlgeschlagen. Weitere Informationen zu **CoCreateInstance,** **CoInitialize** und **CoInitializeEx** finden Sie in der Windows SDK-Dokumentation.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Interoperabilität mit Legacyaudio-APIs](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
