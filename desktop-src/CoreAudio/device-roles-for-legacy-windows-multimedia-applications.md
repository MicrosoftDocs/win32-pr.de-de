---
description: Geräte Rollen für ältere Windows-Multimediaanwendungen
ms.assetid: 54dcaa0e-2652-406d-ba24-c8885924acc6
title: Geräte Rollen für ältere Windows-Multimediaanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a4ad6728659e4c865aed773575268844fe330e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354278"
---
# <a name="device-roles-for-legacy-windows-multimedia-applications"></a><span data-ttu-id="87ece-103">Geräte Rollen für ältere Windows-Multimediaanwendungen</span><span class="sxs-lookup"><span data-stu-id="87ece-103">Device Roles for Legacy Windows Multimedia Applications</span></span>

> [!Note]  
> <span data-ttu-id="87ece-104">Die mmdevice-API unterstützt Geräte Rollen.</span><span class="sxs-lookup"><span data-stu-id="87ece-104">The MMDevice API supports device roles.</span></span> <span data-ttu-id="87ece-105">Die Benutzeroberfläche in Windows Vista implementiert jedoch keine Unterstützung für dieses Feature.</span><span class="sxs-lookup"><span data-stu-id="87ece-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="87ece-106">Die Unterstützung von Benutzeroberflächen für Geräte Rollen kann in einer zukünftigen Version von Windows implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="87ece-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="87ece-107">Weitere Informationen finden Sie unter [Geräte Rollen in Windows Vista](device-roles-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="87ece-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="87ece-108">Die Legacy Funktionen von Windows Multimedia **waveoutxxx** und **waveinixxx** bieten keine Möglichkeit für eine Anwendung, das [audioendpunktgerät](audio-endpoint-devices.md) auszuwählen, das dem Benutzer einer bestimmten [Geräte Rolle](device-roles.md)zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="87ece-108">The legacy Windows multimedia **waveOutXxx** and **waveInXxx** functions provide no means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that the user has assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="87ece-109">In Windows Vista können die Kerndatei-APIs jedoch in Verbindung mit einer Windows-Multimediaanwendung verwendet werden, um die Geräteauswahl basierend auf der Geräte Rolle zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="87ece-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a Windows multimedia application to enable device selection based on device role.</span></span> <span data-ttu-id="87ece-110">Mithilfe der [mmdevice-API](mmdevice-api.md)kann eine **waveoutxxx** -Anwendung z. b. das audioendpunktgerät identifizieren, das einer Rolle zugewiesen ist, das entsprechende Wellenform-Ausgabegerät identifiziert und die **WaveOutOpen** -Funktion aufruft, um eine Instanz des Geräts zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="87ece-110">For example, with the help of the [MMDevice API](mmdevice-api.md), a **waveOutXxx** application can identify the audio endpoint device that is assigned to a role, identify the corresponding waveform output device, and call the **waveOutOpen** function to open an instance of the device.</span></span> <span data-ttu-id="87ece-111">Weitere Informationen zu **waveoutxxx** und **waveinxxx** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="87ece-111">For more information about **waveOutXxx** and **waveInXxx**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="87ece-112">Im folgenden Codebeispiel wird veranschaulicht, wie Sie die Wellenform-Geräte-ID für das renderingendpunktgerät abrufen, das einer bestimmten Geräte Rolle zugewiesen ist:</span><span class="sxs-lookup"><span data-stu-id="87ece-112">The following code example shows how to obtain the waveform device ID for the rendering endpoint device that is assigned to a particular device role:</span></span>


```C++
//-----------------------------------------------------------
// This function gets the waveOut ID of the audio endpoint
// device that is currently assigned to the specified device
// role. The caller can use the waveOut ID to open the
// waveOut device that corresponds to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

HRESULT GetWaveOutId(ERole role, int *pWaveOutId)
{
    HRESULT hr;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    WCHAR *pstrEndpointIdKey = NULL;
    WCHAR *pstrEndpointId = NULL;

    if (pWaveOutId == NULL)
    {
        return E_POINTER;
    }

    // Create an audio endpoint device enumerator.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get the audio endpoint device that the user has
    // assigned to the specified device role.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    // Get the endpoint ID string of the audio endpoint device.
    hr = pDevice->GetId(&pstrEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Get the size of the endpoint ID string.
    size_t  cbEndpointIdKey;

    hr = StringCbLength(pstrEndpointIdKey,
                        STRSAFE_MAX_CCH * sizeof(WCHAR),
                        &cbEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Include terminating null in string size.
    cbEndpointIdKey += sizeof(WCHAR);

    // Allocate a buffer for a second string of the same size.
    pstrEndpointId = (WCHAR*)CoTaskMemAlloc(cbEndpointIdKey);
    if (pstrEndpointId == NULL)
    {
        EXIT_ON_ERROR(hr = E_OUTOFMEMORY)
    }

    // Each for-loop iteration below compares the endpoint ID
    // string of the audio endpoint device to the endpoint ID
    // string of an enumerated waveOut device. If the strings
    // match, then we've found the waveOut device that is
    // assigned to the specified device role.
    int waveOutId;
    int cWaveOutDevices = waveOutGetNumDevs();

    for (waveOutId = 0; waveOutId < cWaveOutDevices; waveOutId++)
    {
        MMRESULT mmr;
        size_t cbEndpointId;

        // Get the size (including the terminating null) of
        // the endpoint ID string of the waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEIDSIZE,
                             (DWORD_PTR)&cbEndpointId, NULL);
        if (mmr != MMSYSERR_NOERROR ||
            cbEndpointIdKey != cbEndpointId)  // do sizes match?
        {
            continue;  // not a matching device
        }

        // Get the endpoint ID string for this waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEID,
                             (DWORD_PTR)pstrEndpointId,
                             cbEndpointId);
        if (mmr != MMSYSERR_NOERROR)
        {
            continue;
        }

        // Check whether the endpoint ID string of this waveOut
        // device matches that of the audio endpoint device.
        if (lstrcmpi(pstrEndpointId, pstrEndpointIdKey) == 0)
        {
            *pWaveOutId = waveOutId;  // found match
            hr = S_OK;
            break;
        }
    }

    if (waveOutId == cWaveOutDevices)
    {
        // We reached the end of the for-loop above without
        // finding a waveOut device with a matching endpoint
        // ID string. This behavior is quite unexpected.
        hr = E_UNEXPECTED;
    }

Exit:
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    CoTaskMemFree(pstrEndpointIdKey);  // NULL pointer okay
    CoTaskMemFree(pstrEndpointId);
    return hr;
}
```



<span data-ttu-id="87ece-113">Im vorangehenden Codebeispiel akzeptiert die getwaveoutid-Funktion eine Geräte Rolle (econsole, emultimedia oder eCommunications) als Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="87ece-113">In the preceding code example, the GetWaveOutId function accepts a device role (eConsole, eMultimedia, or eCommunications) as an input parameter.</span></span> <span data-ttu-id="87ece-114">Der zweite Parameter ist ein Zeiger, über den die-Funktion die Wellenform-Geräte-ID für das Wellenform-Ausgabegerät schreibt, das der angegebenen Rolle zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="87ece-114">The second parameter is a pointer through which the function writes the waveform device ID for the waveform output device that is assigned to the specified role.</span></span> <span data-ttu-id="87ece-115">Die Anwendung kann dann **WaveOutOpen** mit dieser ID anrufen, um das Gerät zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="87ece-115">The application can then call **waveOutOpen** with this ID to open the device.</span></span>

<span data-ttu-id="87ece-116">Die Hauptschleife im vorangehenden Codebeispiel enthält zwei Aufrufe der **waveoutmessage** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="87ece-116">The main loop in the preceding code example contains two calls to the **waveOutMessage** function.</span></span> <span data-ttu-id="87ece-117">Der erste-Befehl sendet eine drv- \_ queryfunctioninstanceidsize-Nachricht, um die Größe der Endpunkt- [ID-Zeichenfolge](endpoint-id-strings.md) des Wellenform-Geräts, die durch den *waveoutid* -Parameter identifiziert wird, in Bytes abzurufen.</span><span class="sxs-lookup"><span data-stu-id="87ece-117">The first call sends a DRV\_QUERYFUNCTIONINSTANCEIDSIZE message to retrieve the size, in bytes, of the [endpoint ID string](endpoint-id-strings.md) of the waveform device that is identified by the *waveOutId* parameter.</span></span> <span data-ttu-id="87ece-118">(Die Endpunkt-ID-Zeichenfolge identifiziert das audioendpunktgerät, das der Wellenform-Geräte Abstraktion zugrunde liegt.) Die von diesem-Befehl gemeldete Größe schließt den Platz für das abschließende Null-Zeichen am Ende der Zeichenfolge ein.</span><span class="sxs-lookup"><span data-stu-id="87ece-118">(The endpoint ID string identifies the audio endpoint device that underlies the waveform device abstraction.) The size reported by this call includes the space for the terminating null character at the end of the string.</span></span> <span data-ttu-id="87ece-119">Das Programm kann die Größen Informationen verwenden, um einen Puffer zuzuordnen, der groß genug ist, um die gesamte Endpunkt-ID-Zeichenfolge zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="87ece-119">The program can use the size information to allocate a buffer that is large enough to contain the entire endpoint ID string.</span></span>

<span data-ttu-id="87ece-120">Der zweite aufrut von **waveoutmessage** sendet eine drv \_ -queryfunctioninstanceid-Meldung, um die Geräte-ID-Zeichenfolge des Wellenform-Ausgabegeräts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="87ece-120">The second call to **waveOutMessage** sends a DRV\_QUERYFUNCTIONINSTANCEID message to retrieve the device ID string of the waveform output device.</span></span> <span data-ttu-id="87ece-121">Der Beispielcode vergleicht diese Zeichenfolge mit der Geräte-ID-Zeichenfolge des audioendpunktgeräts mit der angegebenen Geräte Rolle.</span><span class="sxs-lookup"><span data-stu-id="87ece-121">The example code compares this string to the device ID string of the audio endpoint device with the specified device role.</span></span> <span data-ttu-id="87ece-122">Wenn die Zeichen folgen Stimmen, schreibt die Funktion die Wellenform-Geräte-ID in den Speicherort, auf den der Parameter *pwaveoutid* zeigt.</span><span class="sxs-lookup"><span data-stu-id="87ece-122">If the strings match, then the function writes the waveform device ID to the location pointed to by parameter *pWaveOutId*.</span></span> <span data-ttu-id="87ece-123">Der Aufrufer kann diese ID verwenden, um das Wellenform-Ausgabegerät zu öffnen, das über die angegebene Geräte Rolle verfügt.</span><span class="sxs-lookup"><span data-stu-id="87ece-123">The caller can use this ID to open the waveform output device that has the specified device role.</span></span>

<span data-ttu-id="87ece-124">Windows Vista unterstützt die \_ Nachrichten drv queryfunctioninstanceidsize und drv \_ queryfunctioninstanceid.</span><span class="sxs-lookup"><span data-stu-id="87ece-124">Windows Vista supports the DRV\_QUERYFUNCTIONINSTANCEIDSIZE and DRV\_QUERYFUNCTIONINSTANCEID messages.</span></span> <span data-ttu-id="87ece-125">Sie werden in früheren Versionen von Windows, einschließlich Windows Server 2003, Windows XP und Windows 2000, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="87ece-125">They are not supported in earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000.</span></span>

<span data-ttu-id="87ece-126">Die Funktion im vorangehenden Codebeispiel erhält die Wellenform-Geräte-ID für ein renderinggerät, aber mit einigen Änderungen kann Sie angepasst werden, um die Wellenform-Geräte-ID für ein Erfassungsgerät zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="87ece-126">The function in the preceding code example obtains the waveform device ID for a rendering device, but, with a few modifications, it can be adapted to obtain the waveform device ID for a capture device.</span></span> <span data-ttu-id="87ece-127">Die Anwendung kann dann **waveinopen** mit dieser ID anrufen, um das Gerät zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="87ece-127">The application can then call **waveInOpen** with this ID to open the device.</span></span> <span data-ttu-id="87ece-128">Gehen Sie folgendermaßen vor, um das vorangehende Codebeispiel zu ändern, um die Wellenform-Geräte-ID für das Gerät für die audioerfassungs-Endpunkt zu erhalten, das einer bestimmten Rolle zugewiesen ist:</span><span class="sxs-lookup"><span data-stu-id="87ece-128">To change the preceding code example to get the waveform device ID for the audio-capture endpoint device that is assigned to a particular role, do the following:</span></span>

-   <span data-ttu-id="87ece-129">Ersetzen Sie alle **waveoutxxx** -Funktionsaufrufe im vorangehenden Beispiel durch die entsprechenden **Wavin xxx** -Funktionsaufrufe.</span><span class="sxs-lookup"><span data-stu-id="87ece-129">Replace all of the **waveOutXxx** function calls in the preceding example with the corresponding **waveInXxx** function calls.</span></span>
-   <span data-ttu-id="87ece-130">Ändern Sie den Handle-Typ hwaveout in hwaader.</span><span class="sxs-lookup"><span data-stu-id="87ece-130">Change handle type HWAVEOUT to HWAVEIN.</span></span>
-   <span data-ttu-id="87ece-131">Ersetzen Sie [**erole-Enumerationskonstante**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) Ausdrucks durch ecapture.</span><span class="sxs-lookup"><span data-stu-id="87ece-131">Replace [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration constant eRender with eCapture.</span></span>

<span data-ttu-id="87ece-132">In Windows Vista weisen die Funktionen **WaveOutOpen** und **waveinopen** stets die von Ihnen erstellten Audiostreams der Standard Sitzung zu – die prozessspezifische Sitzung, die durch den Sitzungs-GUID-Wert GUID NULL identifiziert wird \_ .</span><span class="sxs-lookup"><span data-stu-id="87ece-132">In Windows Vista, the **waveOutOpen** and **waveInOpen** functions always assign the audio streams that they create to the default session—the process-specific session that is identified by the session GUID value GUID\_NULL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87ece-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="87ece-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87ece-134">Interoperabilität mit Legacy-audioapis</span><span class="sxs-lookup"><span data-stu-id="87ece-134">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



