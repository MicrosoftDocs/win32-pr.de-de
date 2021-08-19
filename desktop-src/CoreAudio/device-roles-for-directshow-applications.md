---
description: Geräterollen für DirectShow-Anwendungen
ms.assetid: 54f42bda-b4a0-465c-9ce6-9102d2908776
title: Geräterollen für DirectShow-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e22a86e5537f11b6b4153753841a2682b5ac77a043a3fa74538714a2540377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957359"
---
# <a name="device-roles-for-directshow-applications"></a>Geräterollen für DirectShow-Anwendungen

> [!Note]  
> Die [MMDevice-API unterstützt](mmdevice-api.md) Geräterollen. Die Benutzeroberfläche in Windows Vista implementiert jedoch keine Unterstützung für dieses Feature. Die Benutzeroberflächenunterstützung für Geräterollen wird möglicherweise in einer zukünftigen Version von Windows. Weitere Informationen finden Sie unter [Geräterollen in Windows Vista](device-roles-in-windows-vista.md).

 

Die DirectShow-API bietet einer Anwendung keine [](audio-endpoint-devices.md) Möglichkeit, das Audioendpunktgerät auszuwählen, das einer bestimmten [Geräterolle zugewiesen ist.](device-roles.md) In Windows Vista können die Kernaudio-APIs jedoch in Verbindung mit einer DirectShow-Anwendung verwendet werden, um die Geräteauswahl basierend auf der Geräterolle zu aktivieren. Mithilfe der Kernaudio-APIs kann die Anwendung:

-   Identifizieren Sie das Audioendpunktgerät, das der Benutzer einer bestimmten Geräterolle zugewiesen hat.
-   Erstellen Sie einen DirectShow-Audiorenderingfilter mit einer [**IBaseFilter-Schnittstelle,**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) die das Audioendpunktgerät kapselt.
-   Erstellen Sie ein DirectShow-Diagramm, das den Filter enthält.

Weitere Informationen zu DirectShow und [**IBaseFilter finden**](/windows/desktop/api/strmif/nn-strmif-ibasefilter)Sie in der Windows SDK-Dokumentation.

Das folgende Codebeispiel zeigt, wie Sie einen DirectShow-Audiorenderingfilter erstellen, der das Renderingendpunktgerät kapselt, das einer bestimmten Geräterolle zugewiesen ist:


```C++
//-----------------------------------------------------------
// Create a DirectShow audio rendering filter that
// encapsulates the audio endpoint device that is currently
// assigned to the specified device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

// This application's audio session GUID
const GUID guidAudioSessionId = {
    0xb13ff52e, 0xa5cf, 0x4fca,
    {0x9f, 0xc3, 0x42, 0x26, 0x5b, 0x0b, 0x14, 0xfb}
};

HRESULT CreateAudioRenderer(ERole role, IBaseFilter** ppAudioRenderer)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;

    if (ppAudioRenderer == NULL)
    {
        return E_POINTER;
    }

    // Activate the IBaseFilter interface on the
    // audio renderer with the specified role.
    hr = CoCreateInstance(CLSID_MMDeviceEnumerator,
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    DIRECTX_AUDIO_ACTIVATION_PARAMS  daap;
    daap.cbDirectXAudioActivationParams = sizeof(daap);
    daap.guidAudioSession = guidAudioSessionId;
    daap.dwAudioStreamFlags = AUDCLNT_STREAMFLAGS_CROSSPROCESS;

    PROPVARIANT  var;
    PropVariantInit(&var);

    var.vt = VT_BLOB;
    var.blob.cbSize = sizeof(daap);
    var.blob.pBlobData = (BYTE*)&daap;

    hr = pDevice->Activate(__uuidof(IBaseFilter),
                           CLSCTX_ALL, &var,
                           (void**)ppAudioRenderer);
    EXIT_ON_ERROR(hr)

Exit:
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    return hr;
}
```



Im vorherigen Codebeispiel akzeptiert die CreateAudioRenderer-Funktion eine Geräterolle (eConsole, eMultimedia oder eCommunications) als Eingabeparameter. Der zweite Parameter ist ein Zeiger, über den die Funktion die Adresse einer [**IBaseFilter-Schnittstelleninstanz**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) schreibt. Darüber hinaus zeigt das Beispiel, wie sie die [**IMMDevice::Activate-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) verwendet, um den Audiostream in der **IBaseFilter-Instanz** einer prozessübergreifenden Audiositzung mit einer anwendungsspezifischen Sitzungs-GUID (angegeben durch die **guidAudioSessionId-Konstante)** zu zuweisen. Der dritte Parameter im **Activate-Aufruf** verweist auf eine -Struktur, die die Sitzungs-GUID und das prozessübergreifende Flag enthält. Wenn der Benutzer mehrere Instanzen der Anwendung ausgeführt, verwenden die Audiostreams von allen Instanzen dieselbe Sitzungs-GUID und gehören somit zur gleichen Sitzung.

Alternativ kann der Aufrufer  NULL als dritten Parameter im [**Activate-Aufruf**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) angeben, um den Stream der Standardsitzung als prozessspezifische Sitzung mit dem Sitzungs-GUID-Wert GUID \_ NULL zu zuweisen. Weitere Informationen finden Sie unter **IMMDevice::Activate**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Interoperabilität mit Legacyaudio-APIs](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
