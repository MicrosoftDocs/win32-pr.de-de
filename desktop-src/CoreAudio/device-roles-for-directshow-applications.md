---
description: Geräte Rollen für DirectShow-Anwendungen
ms.assetid: 54f42bda-b4a0-465c-9ce6-9102d2908776
title: Geräte Rollen für DirectShow-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df8b43ddd56870b65fc9ec1e3bb600e8e6b79528
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482758"
---
# <a name="device-roles-for-directshow-applications"></a>Geräte Rollen für DirectShow-Anwendungen

> [!Note]  
> Die [mmdevice-API](mmdevice-api.md) unterstützt Geräte Rollen. Die Benutzeroberfläche in Windows Vista implementiert jedoch keine Unterstützung für dieses Feature. Die Unterstützung von Benutzeroberflächen für Geräte Rollen kann in einer zukünftigen Version von Windows implementiert werden. Weitere Informationen finden Sie unter [Geräte Rollen in Windows Vista](device-roles-in-windows-vista.md).

 

Die DirectShow-API bietet keine Möglichkeit für eine Anwendung, das [audioendpunktgerät](audio-endpoint-devices.md) auszuwählen, das einer bestimmten [Geräte Rolle](device-roles.md)zugewiesen ist. In Windows Vista können die Kerndatei-APIs jedoch in Verbindung mit einer DirectShow-Anwendung verwendet werden, um die Geräteauswahl basierend auf der Geräte Rolle zu aktivieren. Mit der Hilfe der kernaudioapis kann die Anwendung folgende Aktionen ausführen:

-   Identifizieren Sie das audioendpunktgerät, das der Benutzer einer bestimmten Geräte Rolle zugewiesen hat.
-   Erstellen eines DirectShow-audiorenderingfilters mit einer [**ibasefilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) -Schnittstelle, die das audioendpunktgerät kapselt.
-   Erstellen Sie ein DirectShow-Diagramm, das den Filter enthält.

Weitere Informationen zu DirectShow und [**ibasefilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter)finden Sie in der Windows SDK-Dokumentation.

Im folgenden Codebeispiel wird gezeigt, wie ein DirectShow-audiorenderingfilter erstellt wird, der das renderingendpunktgerät kapselt, das einer bestimmten Geräte Rolle zugewiesen ist:


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



Im vorangehenden Codebeispiel nimmt die Funktion "-Funktion" eine Geräte Rolle (econsole, emultimedia oder eCommunications) als Eingabeparameter an. Der zweite Parameter ist ein Zeiger, über den die-Funktion die Adresse einer [**ibasefilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) -Schnittstellen Instanz schreibt. Außerdem wird in diesem Beispiel gezeigt, wie die Methode " [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) " verwendet wird, um den Audiostream in der Instanz von " **ibasefilter** " einer prozessübergreifenden Audiositzung mit einer anwendungsspezifischen Sitzungs-GUID zuzuweisen (angegeben durch die **guidaudiosessionid** -Konstante). Der dritte Parameter im **Aktivierungs** Befehl verweist auf eine-Struktur, die die Sitzungs-GUID und das prozessübergreifende Flag enthält. Wenn der Benutzer mehrere Instanzen der Anwendung ausführt, verwenden die Audiodatenströme aus allen Instanzen die gleiche Sitzungs-GUID und gehören somit zur gleichen Sitzung.

Alternativ kann der Aufrufer **null** als dritten Parameter im [**Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) Aufruf angeben, um den Stream der Standard Sitzung als prozessspezifische Sitzung mit dem GUID-Wert der Sitzungs-GUID \_ null zuzuweisen. Weitere Informationen finden Sie unter **immdevice:: Aktivieren**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Interoperabilität mit Legacy-audioapis](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
