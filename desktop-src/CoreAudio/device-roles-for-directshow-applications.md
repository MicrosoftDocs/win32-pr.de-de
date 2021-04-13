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
# <a name="device-roles-for-directshow-applications"></a><span data-ttu-id="99abe-103">Geräte Rollen für DirectShow-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="99abe-103">Device Roles for DirectShow Applications</span></span>

> [!Note]  
> <span data-ttu-id="99abe-104">Die [mmdevice-API](mmdevice-api.md) unterstützt Geräte Rollen.</span><span class="sxs-lookup"><span data-stu-id="99abe-104">The [MMDevice API](mmdevice-api.md) supports device roles.</span></span> <span data-ttu-id="99abe-105">Die Benutzeroberfläche in Windows Vista implementiert jedoch keine Unterstützung für dieses Feature.</span><span class="sxs-lookup"><span data-stu-id="99abe-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="99abe-106">Die Unterstützung von Benutzeroberflächen für Geräte Rollen kann in einer zukünftigen Version von Windows implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="99abe-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="99abe-107">Weitere Informationen finden Sie unter [Geräte Rollen in Windows Vista](device-roles-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="99abe-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="99abe-108">Die DirectShow-API bietet keine Möglichkeit für eine Anwendung, das [audioendpunktgerät](audio-endpoint-devices.md) auszuwählen, das einer bestimmten [Geräte Rolle](device-roles.md)zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="99abe-108">The DirectShow API does not provide a means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that is assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="99abe-109">In Windows Vista können die Kerndatei-APIs jedoch in Verbindung mit einer DirectShow-Anwendung verwendet werden, um die Geräteauswahl basierend auf der Geräte Rolle zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="99abe-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a DirectShow application to enable device selection based on device role.</span></span> <span data-ttu-id="99abe-110">Mit der Hilfe der kernaudioapis kann die Anwendung folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="99abe-110">With the help of the core audio APIs, the application can:</span></span>

-   <span data-ttu-id="99abe-111">Identifizieren Sie das audioendpunktgerät, das der Benutzer einer bestimmten Geräte Rolle zugewiesen hat.</span><span class="sxs-lookup"><span data-stu-id="99abe-111">Identify the audio endpoint device that the user has assigned to a particular device role.</span></span>
-   <span data-ttu-id="99abe-112">Erstellen eines DirectShow-audiorenderingfilters mit einer [**ibasefilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) -Schnittstelle, die das audioendpunktgerät kapselt.</span><span class="sxs-lookup"><span data-stu-id="99abe-112">Create a DirectShow audio rendering filter with an [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) interface that encapsulates the audio endpoint device.</span></span>
-   <span data-ttu-id="99abe-113">Erstellen Sie ein DirectShow-Diagramm, das den Filter enthält.</span><span class="sxs-lookup"><span data-stu-id="99abe-113">Build a DirectShow graph that incorporates the filter.</span></span>

<span data-ttu-id="99abe-114">Weitere Informationen zu DirectShow und [**ibasefilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter)finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="99abe-114">For more information about DirectShow and [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter), see the Windows SDK documentation.</span></span>

<span data-ttu-id="99abe-115">Im folgenden Codebeispiel wird gezeigt, wie ein DirectShow-audiorenderingfilter erstellt wird, der das renderingendpunktgerät kapselt, das einer bestimmten Geräte Rolle zugewiesen ist:</span><span class="sxs-lookup"><span data-stu-id="99abe-115">The following code example shows how to create a DirectShow audio rendering filter that encapsulates the rendering endpoint device that is assigned to a particular device role:</span></span>


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



<span data-ttu-id="99abe-116">Im vorangehenden Codebeispiel nimmt die Funktion "-Funktion" eine Geräte Rolle (econsole, emultimedia oder eCommunications) als Eingabeparameter an.</span><span class="sxs-lookup"><span data-stu-id="99abe-116">In the preceding code example, the CreateAudioRenderer function accepts a device role (eConsole, eMultimedia, or eCommunications) as an input parameter.</span></span> <span data-ttu-id="99abe-117">Der zweite Parameter ist ein Zeiger, über den die-Funktion die Adresse einer [**ibasefilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) -Schnittstellen Instanz schreibt.</span><span class="sxs-lookup"><span data-stu-id="99abe-117">The second parameter is a pointer through which the function writes the address of an [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) interface instance.</span></span> <span data-ttu-id="99abe-118">Außerdem wird in diesem Beispiel gezeigt, wie die Methode " [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) " verwendet wird, um den Audiostream in der Instanz von " **ibasefilter** " einer prozessübergreifenden Audiositzung mit einer anwendungsspezifischen Sitzungs-GUID zuzuweisen (angegeben durch die **guidaudiosessionid** -Konstante).</span><span class="sxs-lookup"><span data-stu-id="99abe-118">In addition, the example shows how to use the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to assign the audio stream in the **IBaseFilter** instance to a cross-process audio session with an application-specific session GUID (specified by the **guidAudioSessionId** constant).</span></span> <span data-ttu-id="99abe-119">Der dritte Parameter im **Aktivierungs** Befehl verweist auf eine-Struktur, die die Sitzungs-GUID und das prozessübergreifende Flag enthält.</span><span class="sxs-lookup"><span data-stu-id="99abe-119">The third parameter in the **Activate** call points to a structure that contains the session GUID and cross-process flag.</span></span> <span data-ttu-id="99abe-120">Wenn der Benutzer mehrere Instanzen der Anwendung ausführt, verwenden die Audiodatenströme aus allen Instanzen die gleiche Sitzungs-GUID und gehören somit zur gleichen Sitzung.</span><span class="sxs-lookup"><span data-stu-id="99abe-120">If the user runs multiple instances of the application, then the audio streams from all the instances use the same session GUID and thus belong to the same session.</span></span>

<span data-ttu-id="99abe-121">Alternativ kann der Aufrufer **null** als dritten Parameter im [**Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) Aufruf angeben, um den Stream der Standard Sitzung als prozessspezifische Sitzung mit dem GUID-Wert der Sitzungs-GUID \_ null zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="99abe-121">Alternatively, the caller can specify **NULL** as the third parameter in the [**Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) call to assign the stream to the default session as the process-specific session with session GUID value GUID\_NULL.</span></span> <span data-ttu-id="99abe-122">Weitere Informationen finden Sie unter **immdevice:: Aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="99abe-122">For more information, see **IMMDevice::Activate**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99abe-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="99abe-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99abe-124">Interoperabilität mit Legacy-audioapis</span><span class="sxs-lookup"><span data-stu-id="99abe-124">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
