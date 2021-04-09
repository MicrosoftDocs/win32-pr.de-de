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
# <a name="device-roles-for-directsound-applications"></a><span data-ttu-id="9387d-103">Geräte Rollen für DirectSound-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="9387d-103">Device Roles for DirectSound Applications</span></span>

> [!Note]  
> <span data-ttu-id="9387d-104">Die [mmdevice-API](mmdevice-api.md) unterstützt Geräte Rollen.</span><span class="sxs-lookup"><span data-stu-id="9387d-104">The [MMDevice API](mmdevice-api.md) supports device roles.</span></span> <span data-ttu-id="9387d-105">Die Benutzeroberfläche in Windows Vista implementiert jedoch keine Unterstützung für dieses Feature.</span><span class="sxs-lookup"><span data-stu-id="9387d-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="9387d-106">Die Unterstützung von Benutzeroberflächen für Geräte Rollen kann in einer zukünftigen Version von Windows implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="9387d-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="9387d-107">Weitere Informationen finden Sie unter [Geräte Rollen in Windows Vista](device-roles-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="9387d-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="9387d-108">Die DirectSound-API bietet keine Möglichkeit für eine Anwendung, das [audioendpunktgerät](audio-endpoint-devices.md) auszuwählen, das dem Benutzer einer bestimmten [Geräte Rolle](device-roles.md)zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="9387d-108">The DirectSound API does not provide a means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that the user has assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="9387d-109">In Windows Vista können die kernaudio-APIs jedoch in Verbindung mit einer DirectSound-Anwendung verwendet werden, um die Geräteauswahl basierend auf der Geräte Rolle zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9387d-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a DirectSound application to enable device selection based on device role.</span></span> <span data-ttu-id="9387d-110">Mithilfe der kernaudio-APIs kann die Anwendung das audioendpunktgerät identifizieren, das einer bestimmten Rolle zugewiesen ist, die DirectSound-Geräte-GUID für das Endpunktgerät abrufen und die Funktion **directsoundcreate** oder **directsoundcaptucreate** aufrufen, um eine **idirectsound** -oder **idirectsoundcapture** -Schnittstellen Instanz zu erstellen, die das Endpunkt Gerät kapselt</span><span class="sxs-lookup"><span data-stu-id="9387d-110">With the help of the core audio APIs, the application can identify the audio endpoint device that is assigned to a particular role, get the DirectSound device GUID for the endpoint device, and call the **DirectSoundCreate** or **DirectSoundCaptureCreate** function to create an **IDirectSound** or **IDirectSoundCapture** interface instance that encapsulates the endpoint device.</span></span> <span data-ttu-id="9387d-111">Weitere Informationen zu DirectSound finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="9387d-111">For more information about DirectSound, see the Windows SDK documentation.</span></span>

<span data-ttu-id="9387d-112">Das folgende Codebeispiel zeigt, wie Sie die DirectSound-Geräte-GUID für das Rendering-oder Aufzeichnungsgerät abrufen, das zurzeit einer bestimmten Geräte Rolle zugewiesen ist:</span><span class="sxs-lookup"><span data-stu-id="9387d-112">The following code example shows how to obtain the DirectSound device GUID for the rendering or capture device that is currently assigned to a particular device role:</span></span>


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



<span data-ttu-id="9387d-113">Im vorangehenden Codebeispiel akzeptiert die getdirectsoundguid-Funktion eine Datenfluss Richtung (eRender oder ecapture) und eine Geräte Rolle (econsole, emultimedia oder eCommunications) als Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="9387d-113">In the preceding code example, the GetDirectSoundGuid function accepts a data-flow direction (eRender or eCapture) and a device role (eConsole, eMultimedia, or eCommunications) as input parameters.</span></span> <span data-ttu-id="9387d-114">Der dritte Parameter ist ein Zeiger, über den die-Funktion eine Geräte-GUID schreibt, die die Anwendung als Eingabeparameter für die **directsoundcreate** -oder **directsoundcaptuup** -Funktion bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="9387d-114">The third parameter is a pointer through which the function writes a device GUID that the application can supply as an input parameter to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function.</span></span>

<span data-ttu-id="9387d-115">Im vorangehenden Codebeispiel wird die DirectSound-Geräte-GUID wie folgt abgerufen:</span><span class="sxs-lookup"><span data-stu-id="9387d-115">The preceding code example obtains the DirectSound device GUID by:</span></span>

-   <span data-ttu-id="9387d-116">Erstellen einer [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstellen Instanz, die das audioendpunktgerät darstellt, das über die angegebene Datenfluss Richtung und die angegebene Geräte Rolle verfügt.</span><span class="sxs-lookup"><span data-stu-id="9387d-116">Creating an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface instance that represents the audio endpoint device that has the specified data-flow direction and device role.</span></span>
-   <span data-ttu-id="9387d-117">Öffnen des Eigenschaften Speicher des audioendpunktgeräts.</span><span class="sxs-lookup"><span data-stu-id="9387d-117">Opening the property store of the audio endpoint device.</span></span>
-   <span data-ttu-id="9387d-118">Die [**pkey \_ audioendpoint- \_ GUID**](pkey-audioendpoint-guid.md) -Eigenschaft wird aus dem Eigenschaften Speicher erhalten.</span><span class="sxs-lookup"><span data-stu-id="9387d-118">Getting the [**PKEY\_AudioEndpoint\_GUID**](pkey-audioendpoint-guid.md) property from the property store.</span></span> <span data-ttu-id="9387d-119">Der Eigenschafts Wert ist eine Zeichen folgen Darstellung der DirectSound-Geräte-GUID für das audioendpunktgerät.</span><span class="sxs-lookup"><span data-stu-id="9387d-119">The property value is a string representation of the DirectSound device GUID for the audio endpoint device.</span></span>
-   <span data-ttu-id="9387d-120">Aufrufen der [**CLSIDFromString**](https://www.bing.com/search?q=**CLSIDFromString**) -Funktion zum Konvertieren der Zeichen folgen Darstellung der Geräte-GUID in eine GUID-Struktur.</span><span class="sxs-lookup"><span data-stu-id="9387d-120">Calling the [**CLSIDFromString**](https://www.bing.com/search?q=**CLSIDFromString**) function to convert the string representation of the device GUID to a GUID structure.</span></span> <span data-ttu-id="9387d-121">Weitere Informationen zu **CLSIDFromString** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="9387d-121">For more information about **CLSIDFromString**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="9387d-122">Nachdem Sie eine Geräte-GUID von der getdirectsoundguid-Funktion erhalten haben, kann die Anwendung **directsoundcreate** oder **directsoundcaptuneu** mit dieser GUID aufrufen, um das DirectSound-Rendering oder das Erfassungsgerät zu erstellen, das das audioendpunktgerät kapselt.</span><span class="sxs-lookup"><span data-stu-id="9387d-122">After obtaining a device GUID from the GetDirectSoundGuid function, the application can call **DirectSoundCreate** or **DirectSoundCaptureCreate** with this GUID to create the DirectSound rendering or capture device that encapsulates the audio endpoint device.</span></span> <span data-ttu-id="9387d-123">Wenn DirectSound ein Gerät auf diese Weise erstellt, wird der Audiostream des Geräts immer der Standard Sitzung zugewiesen – der prozessspezifischen Audiositzung, die durch den Sitzungs-GUID-Wert GUID NULL identifiziert wird \_ .</span><span class="sxs-lookup"><span data-stu-id="9387d-123">When DirectSound creates a device in this way, it always assigns the device's audio stream to the default session—the process-specific audio session that is identified by the session GUID value GUID\_NULL.</span></span>

<span data-ttu-id="9387d-124">Wenn die Anwendung DirectSound erfordert, um den Stream einer prozessübergreifenden Audiositzung oder einer Sitzung mit einer Sitzungs-GUID ungleich **null** zuzuweisen, sollte die Methode " [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) " aufgerufen werden, um ein **idirectsound** -oder **idirectsoundcapture** -Objekt zu erstellen, anstatt die im vorangehenden Codebeispiel gezeigte Technik zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9387d-124">If the application requires DirectSound to assign the stream to a cross-process audio session or to a session with a non-**NULL** session GUID, it should call the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to create an **IDirectSound** or **IDirectSoundCapture** object instead of using the technique shown in the preceding code example.</span></span> <span data-ttu-id="9387d-125">Ein Codebeispiel, in dem veranschaulicht wird, wie Sie die Methode " **aktivieren** " verwenden, um eine prozessübergreifende Audiositzung oder eine Sitzungs-GUID ungleich **null** für einen Stream anzugeben, finden Sie unter [Geräte Rollen für DirectShow-Anwendungen](device-roles-for-directshow-applications.md).</span><span class="sxs-lookup"><span data-stu-id="9387d-125">For a code example that shows how to use the **Activate** method to specify a cross-process audio session or a non-**NULL** session GUID for a stream, see [Device Roles for DirectShow Applications](device-roles-for-directshow-applications.md).</span></span> <span data-ttu-id="9387d-126">Das Codebeispiel in diesem Abschnitt zeigt, wie ein DirectShow-Filter erstellt wird, aber mit geringfügigen Änderungen kann der Code angepasst werden, um ein DirectSound-Gerät zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9387d-126">The code example in that section shows how to create a DirectShow filter, but, with minor modifications, the code can be adapted to create a DirectSound device.</span></span>

<span data-ttu-id="9387d-127">Die Funktion "getdirectsoundguid" im vorangehenden Codebeispiel ruft die [**cokreatinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion auf, um einen Enumerator für die audioendpunktgeräte im System zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9387d-127">The GetDirectSoundGuid function in the preceding code example calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="9387d-128">Wenn das aufrufende Programm die [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) -Funktion oder die [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) -Funktion nicht zum Initialisieren der com-Bibliothek aufgerufen hat, tritt beim **CoCreateInstance** -Aufruf ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="9387d-128">Unless the calling program previously called either the [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="9387d-129">Weitere Informationen zu **cokreateinstance**, **CoInitialize** und **CoInitializeEx** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="9387d-129">For more information about **CoCreateInstance**, **CoInitialize**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9387d-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9387d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9387d-131">Interoperabilität mit Legacy-audioapis</span><span class="sxs-lookup"><span data-stu-id="9387d-131">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
