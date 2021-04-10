---
description: In Windows Vista wurde eine geschützte benutzermodusaudiodatei (Puma) eingeführt, die Benutzermodus-Audioengine in der geschützten Umgebung (PE), die eine sicherere Umgebung für die Audioverarbeitung und das Rendering bereitstellt.
ms.assetid: 27a50026-9e48-48b1-9249-7528a97333c9
title: Geschützter benutzermodusaudiodatei (Puma)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233dc82109feb66472e66e4235031696937d70d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861567"
---
# <a name="protected-user-mode-audio-puma"></a><span data-ttu-id="604d0-103">Geschützter benutzermodusaudiodatei (Puma)</span><span class="sxs-lookup"><span data-stu-id="604d0-103">Protected User Mode Audio (PUMA)</span></span>

<span data-ttu-id="604d0-104">In Windows Vista wurde eine geschützte benutzermodusaudiodatei (Puma) eingeführt, die Benutzermodus-Audioengine in der geschützten Umgebung (PE), die eine sicherere Umgebung für die Audioverarbeitung und das Rendering bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="604d0-104">Windows Vista introduced Protected User Mode Audio (PUMA), the user-mode audio engine in the Protected Environment (PE) that provides a safer environment for audio processing and rendering.</span></span> <span data-ttu-id="604d0-105">Dadurch können nur die zulässigen Audioausgaben aktiviert werden, und es wird sichergestellt, dass die Ausgaben zuverlässig deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="604d0-105">It allows only the acceptable audio outputs to be enabled and ensures that the outputs are disabled reliably.</span></span> <span data-ttu-id="604d0-106">Weitere Informationen zu PUMA finden Sie unter [Output Content Protection und Windows Vista](https://download.microsoft.com/download/5/D/6/5D6EAF2B-7DDF-476B-93DC-7CF0072878E6/output_protect.doc).</span><span class="sxs-lookup"><span data-stu-id="604d0-106">For more information about PUMA, see [Output Content Protection and Windows Vista](https://download.microsoft.com/download/5/D/6/5D6EAF2B-7DDF-476B-93DC-7CF0072878E6/output_protect.doc).</span></span>

<span data-ttu-id="604d0-107">Puma wurde für Windows 7 aktualisiert, um die folgenden Features bereitzustellen:</span><span class="sxs-lookup"><span data-stu-id="604d0-107">PUMA has been updated for Windows 7 to provide the following features:</span></span>

-   <span data-ttu-id="604d0-108">Festlegen von Bits (Serial Copy Management System) an S/PDIF-Endpunkten und HDCP-Bits (High-Bandwidth Digital Content Protection) auf High-Definition Multimedia Interface (HDMI)-Endpunkten.</span><span class="sxs-lookup"><span data-stu-id="604d0-108">Setting Serial Copying Management System (SCMS) bits on S/PDIF endpoints and High-bandwidth Digital Content Protection (HDCP) bits on High-Definition Multimedia Interface (HDMI) endpoints.</span></span>
-   <span data-ttu-id="604d0-109">Aktivieren von SCMS-und HDMI-Schutzsteuer Elementen außerhalb einer geschützten Umgebung (PE).</span><span class="sxs-lookup"><span data-stu-id="604d0-109">Enabling SCMS and HDMI protection controls outside of a Protected Environment (PE).</span></span>

## <a name="drm-protection-in-audio-drivers"></a><span data-ttu-id="604d0-110">DRM-Schutz in Audiotreibern</span><span class="sxs-lookup"><span data-stu-id="604d0-110">DRM Protection in Audio Drivers</span></span>

<span data-ttu-id="604d0-111">Digital Rights Management (DRM) bietet die Möglichkeit, Mediendaten in einem sicheren Container zu verpacken und Verwendungs Regeln an den Inhalt anzufügen.</span><span class="sxs-lookup"><span data-stu-id="604d0-111">Digital Rights Management (DRM) provides the ability to package media data in a secure container and attach usage rules to the content.</span></span> <span data-ttu-id="604d0-112">Beispielsweise kann der Inhaltsanbieter den **Kopierschutz** oder die **digitale Ausgabe deaktivieren** , um direkte digitale Kopien oder die Übertragung aus dem PC-System zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="604d0-112">For example, the content provider might use **Copy Protection** or **Digital Output Disable** to disable direct digital copies or transmission out of the PC system.</span></span>

<span data-ttu-id="604d0-113">Der audiostapel in bestimmten Microsoft-Produkten unterstützt DRM durch Implementierung der Verwendungs Regeln, die die Wiedergabe des Audioinhalts steuern.</span><span class="sxs-lookup"><span data-stu-id="604d0-113">The audio stack in certain Microsoft products supports DRM by implementing the usage rules that govern playback of the audio content.</span></span> <span data-ttu-id="604d0-114">Der zugrunde liegende Audiotreiber muss ein *vertrauenswürdiger Treiber* sein, damit der geschützte Inhalt wiedergegeben werden kann. Das heißt, dass der Treiber für drmlevel 1300 Logo zertifiziert werden muss.</span><span class="sxs-lookup"><span data-stu-id="604d0-114">To play the protected content, the underlying audio driver must be a *trusted driver*; that is, the driver must be logo-certified for DRMLevel 1300.</span></span> <span data-ttu-id="604d0-115">Weitere Informationen zum entwickeln vertrauenswürdiger Treiber finden Sie unter Verwenden von Schnittstellen, die im Windows 2000-Treiber Development Kit ("DDK") oder später definiert sind.</span><span class="sxs-lookup"><span data-stu-id="604d0-115">For information about developing trusted drivers, you can use interfaces that are defined in the Windows 2000 Driver Development Kit ("DDK") or later.</span></span> <span data-ttu-id="604d0-116">Mit dem DDK entwickelte Treiber implementieren die erforderlichen Schnittstellen für DRM.</span><span class="sxs-lookup"><span data-stu-id="604d0-116">Drivers developed with the DDK will implement the necessary interfaces to DRM.</span></span> <span data-ttu-id="604d0-117">Weitere Informationen finden Sie unter [Digital Rights Management](/windows-hardware/drivers/audio/digital-rights-management).</span><span class="sxs-lookup"><span data-stu-id="604d0-117">For more information, see [Digital Rights Management](/windows-hardware/drivers/audio/digital-rights-management).</span></span>

<span data-ttu-id="604d0-118">Um den geschützten Inhalt zu renderten, muss der vertrauenswürdige Treiber prüfen, ob der **Kopierschutz** und die **Deaktivierung Digitaler Ausgaben** für den Inhalt festgelegt sind, der durch den audiostapel fließt, und auf die Einstellungen entsprechend reagieren.</span><span class="sxs-lookup"><span data-stu-id="604d0-118">To render the protected content, the trusted driver must check whether **Copy Protection** and **Digital Output Disable** are set on the content flowing through the audio stack, and respond to the settings accordingly.</span></span>

### <a name="copy-protection-rule"></a><span data-ttu-id="604d0-119">Schutzregel kopieren</span><span class="sxs-lookup"><span data-stu-id="604d0-119">Copy Protection Rule</span></span>

<span data-ttu-id="604d0-120">Der **Kopierschutz** gibt an, dass direkte digitale Kopien auf dem System nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="604d0-120">**Copy Protection** indicates that direct digital copies are not allowed on the system.</span></span> <span data-ttu-id="604d0-121">Die "B"-Version des WHQL-Test Vertrags wurde aktualisiert und zeigt die neuen Erwartungen und Anforderungen eines Treibers an, wenn der **Kopierschutz** für den Inhalt festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="604d0-121">Exhibit B to the WHQL Testing Agreement has been updated to reflect the new expectations and requirements of a driver when **Copy Protection** is set on the content.</span></span> <span data-ttu-id="604d0-122">Für Windows 7 erfüllt der integrierte HD-audioklassentreiber die neuesten Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="604d0-122">For Windows 7, the built-in HD audio class driver complies with the latest requirements.</span></span>

<span data-ttu-id="604d0-123">Zusätzlich zur Sicherstellung, dass Inhalte nicht an eine andere Komponente übergeben werden dürfen oder nicht auf einem nicht flüchtigen Speichermedium gespeichert werden dürfen, das nicht vom DRM-System authentifiziert wird, führt der Audiotreiber die folgenden Aufgaben aus, wenn der **Kopierschutz** festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="604d0-123">In addition to ensuring that content is not allowed to pass to another component or be stored on any nonvolatile storage medium that is not authenticated by the DRM system, the audio driver performs the following tasks when **Copy Protection** is set:</span></span>

-   <span data-ttu-id="604d0-124">Der Treiber aktiviert HDCP auf den HDMI-Endpunkten.</span><span class="sxs-lookup"><span data-stu-id="604d0-124">The driver enables HDCP on HDMI endpoints.</span></span>
-   <span data-ttu-id="604d0-125">Bei S/PDIF-Schnittstellen überprüft der Treiber, ob die Kombination aus L, CP und kategoriecodebits den SCMS-Status "Copy Never" angibt, wie in IEC 60958 definiert.</span><span class="sxs-lookup"><span data-stu-id="604d0-125">For S/PDIF interfaces, the driver validates that the combination of L, Cp and Category Code bits indicates an SCMS state of "Copy Never", as defined in IEC 60958.</span></span>
-   <span data-ttu-id="604d0-126">Das L-Bit ist auf 0 festgelegt, und der Kategoriecode ist auf "Digital Signal Mixer" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="604d0-126">The L bit is set to 0 and the Category Code is set to "Digital Signal Mixer".</span></span>

<span data-ttu-id="604d0-127">Die **drmrights** -Struktur, die von vertrauenswürdigen Audiotreibern verwendet wird, gibt die DRM-Inhalts Rechte an, die einer-audiopin oder einem Streamobjekt eines portklassentreibers zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="604d0-127">The **DRMRIGHTS** structure, used by trusted audio drivers, specifies the DRM content rights assigned to a KS audio pin or to a port-class driver's stream object.</span></span> <span data-ttu-id="604d0-128">Der **CopyProtect** -Member gibt an, ob der **Kopierschutz** für den Audioinhalt festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="604d0-128">The **CopyProtect** member indicates whether **Copy Protection** is set on the audio content.</span></span>

<span data-ttu-id="604d0-129">Für Windows 7 ist die Verwendung von **CopyProtect** strenger.</span><span class="sxs-lookup"><span data-stu-id="604d0-129">For Windows 7, the use of **CopyProtect** is stricter.</span></span> <span data-ttu-id="604d0-130">Der Treiber stellt sicher, dass die Schutzsteuer Elemente für die Audioschnittstellen festgelegt sind, HDCP für die Codec-Ausgabe festgelegt ist und SCMS für die S/PDIF-Ausgabe festgelegt wird, indem der Status auf "Copy Never" festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="604d0-130">The driver ensures that the protection controls are set on the audio interfaces, HDCP is set for HDMI output, and SCMS is set for S/PDIF output by setting the state to "Copy Never".</span></span>

### <a name="digital-output-disable-rule"></a><span data-ttu-id="604d0-131">Regel für die Deaktivierung Digitaler Ausgaben</span><span class="sxs-lookup"><span data-stu-id="604d0-131">Digital Output Disable Rule</span></span>

<span data-ttu-id="604d0-132">Die **digitale Ausgabe deaktiviert** gibt an, dass der Inhalt nicht aus dem System übertragen werden darf.</span><span class="sxs-lookup"><span data-stu-id="604d0-132">**Digital Output Disable** indicates that the content is not allowed to be transmitted out of the system.</span></span> <span data-ttu-id="604d0-133">In Windows 7 antwortet der integrierte HD-audioklassentreiber auf diese Einstellung, indem er HDCP auf den HDMI-Endpunkten aktiviert.</span><span class="sxs-lookup"><span data-stu-id="604d0-133">In Windows 7, the built-in HD audio class driver responds to this setting by enabling HDCP on HDMI endpoints.</span></span> <span data-ttu-id="604d0-134">Dies ähnelt der Reaktion des Treibers auf die Einstellung zum **Kopieren des Schutzes** .</span><span class="sxs-lookup"><span data-stu-id="604d0-134">This is similar to the driver's response to the **Copy Protection** setting.</span></span>

## <a name="enabling-content-protection-mechanisms-outside-of-a-protected-environment"></a><span data-ttu-id="604d0-135">Aktivieren von Mechanismen zum Schutz von Inhalten außerhalb einer geschützten Umgebung</span><span class="sxs-lookup"><span data-stu-id="604d0-135">Enabling Content-Protection Mechanisms Outside of a Protected Environment</span></span>

<span data-ttu-id="604d0-136">PUMA befindet sich in einem separaten Prozess in der geschützten Umgebung (Protected Environment, PE).</span><span class="sxs-lookup"><span data-stu-id="604d0-136">PUMA resides in a separate process in the Protected Environment (PE).</span></span> <span data-ttu-id="604d0-137">In Windows Vista muss sich eine Medien Anwendung in einer PE befinden, um die von PUMA angebotenen Steuerelemente für den audioinhaltstyp zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="604d0-137">In Windows Vista, to use the audio content protection controls offered by PUMA, a media application must be in a PE.</span></span> <span data-ttu-id="604d0-138">Da nur Media Foundation APIs mit einer PE interagieren können, sind die Steuerelemente für den Inhalts Schutz auf Anwendungen beschränkt, die Media Foundation-APIs verwenden, um Audioinhalte zu streamen.</span><span class="sxs-lookup"><span data-stu-id="604d0-138">Because only Media Foundation APIs can interact with a PE, the content protection controls are limited to applications using Media Foundation APIs to stream audio content.</span></span>

<span data-ttu-id="604d0-139">In Windows 7 kann jede Anwendung auf die Content Protection-Steuerelemente zugreifen, die von der PUMA Output Trust Authority (OTA) bereitgestellt werden, unabhängig davon, ob Sie sich in einer PE befinden oder Media Foundation-APIs für die Audiowiedergabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="604d0-139">In Windows 7, any application can access the content protection controls provided by the PUMA Output Trust Authority (OTA), regardless of whether they are in a PE or using Media Foundation APIs for audio playback.</span></span>

## <a name="implementation-instructions"></a><span data-ttu-id="604d0-140">Implementierungsanweisungen</span><span class="sxs-lookup"><span data-stu-id="604d0-140">Implementation Instructions</span></span>

<span data-ttu-id="604d0-141">Die folgenden Schritte sind erforderlich, damit eine Audioanwendung den SCMS-oder HDCP-Inhalts Schutz auf einem audioendpunkt steuert.</span><span class="sxs-lookup"><span data-stu-id="604d0-141">The following steps are required for an audio application to control SCMS or HDCP content protection on an audio endpoint.</span></span> <span data-ttu-id="604d0-142">Unterstützte Audio-APIs sind DirectShow, DirectSound und WASAPI.</span><span class="sxs-lookup"><span data-stu-id="604d0-142">Supported Audio APIs are DirectShow, DirectSound, and WASAPI.</span></span>

<span data-ttu-id="604d0-143">In diesem Beispielcode werden die folgenden Schnittstellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="604d0-143">This example code uses the following interfaces.</span></span>

-   [<span data-ttu-id="604d0-144">**Immdeviceenumerator**</span><span class="sxs-lookup"><span data-stu-id="604d0-144">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [<span data-ttu-id="604d0-145">**Immdevice**</span><span class="sxs-lookup"><span data-stu-id="604d0-145">**IMMDevice**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [<span data-ttu-id="604d0-146">**Iaudioclient**</span><span class="sxs-lookup"><span data-stu-id="604d0-146">**IAudioClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)
-   [<span data-ttu-id="604d0-147">**Immde vicecollection**</span><span class="sxs-lookup"><span data-stu-id="604d0-147">**IMMDeviceCollection**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
-   [<span data-ttu-id="604d0-148">**IMF-Treuhänder Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="604d0-148">**IMFTrustedOutput**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput)
-   [<span data-ttu-id="604d0-149">**IMF outputpolicy**</span><span class="sxs-lookup"><span data-stu-id="604d0-149">**IMFOutputPolicy**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy)

<span data-ttu-id="604d0-150">Die Medien Anwendung muss die folgenden Tasks ausführen.</span><span class="sxs-lookup"><span data-stu-id="604d0-150">The media application must perform the following tasks.</span></span>

1.  <span data-ttu-id="604d0-151">Richten Sie die Entwicklungsumgebung ein.</span><span class="sxs-lookup"><span data-stu-id="604d0-151">Set up the development environment.</span></span>
    -   <span data-ttu-id="604d0-152">Verweisen Sie auf die erforderlichen Schnittstellen, und schließen Sie die im folgenden Code gezeigten Header ein.</span><span class="sxs-lookup"><span data-stu-id="604d0-152">Reference the required interfaces, include the headers shown in the following code.</span></span>
        ```cpp
        #include <MMdeviceapi.h>        // Device endpoint definitions
        #include <Mfidl.h>              // OTA interface definitions
        ```

        

    -   <span data-ttu-id="604d0-153">Verknüpfen Sie die mfuuid. lib, um die OTA-Schnittstellen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="604d0-153">Link to the Mfuuid.lib to use the OTA interfaces.</span></span>
    -   <span data-ttu-id="604d0-154">Deaktivieren Sie den Kernel Debugger und die Treiber Überprüfung, um Authentifizierungs Überprüfungs Fehler zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="604d0-154">Disable the kernel debugger and driver verifier to avoid any authentication checking errors.</span></span>
2.  <span data-ttu-id="604d0-155">Zählen Sie alle Endpunkte im System auf, und wählen Sie den Ziel Endpunkt aus der Endpunkt Auflistung aus, wie im folgenden Code dargestellt.</span><span class="sxs-lookup"><span data-stu-id="604d0-155">Enumerate all endpoints in the system and select the target endpoint from the endpoint collection, as shown in the following code.</span></span> <span data-ttu-id="604d0-156">Weitere Informationen zum Auflisten von Geräten finden Sie unter Auflisten von [Audiogeräten](/previous-versions//ms678716(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="604d0-156">For more information about enumerating devices, see [Enumerating Audio Devices](/previous-versions//ms678716(v=vs.85)).</span></span>
    ```cpp
    BOOL IsDigitalEndpoint(IMMDevice *pDevice)
    {
       PROPVARIANT         var;
       IPropertyStore      *pProperties = NULL;
       EndpointFormFactor  formfactor;
       BOOL                bResult = FALSE;
       HRESULT             hr = S_OK;
       PropVariantInit(&var);
       // Open endpoint properties
       hr = pDevice->OpenPropertyStore(STGM_READ, &pProperties);
       IF_FAILED_JUMP(hr, Exit);

       // get form factor 
       hr = pProperties->GetValue(PKEY_AudioEndpoint_FormFactor, &var);
       IF_FAILED_JUMP(hr, Exit);
       formfactor = (EndpointFormFactor)var.uiVal;
       // DigitalAudioDisplayDevice is defined same as HDMI formfactor
       if ((SPDIF == formfactor) || (DigitalAudioDisplayDevice == formfactor))
       {
           bResult = TRUE;
       }

    Exit:
       PropVariantClear(&var);
       SAFE_RELEASE(pProperties);
       return bResult;
    }
    ```

    

    ```cpp
    /******************************************************************
    *                                                                 *
    *  GetDevice:  Selects an endpoint that meets the requirements.   *
    *                                                                 *
    *  ppDevice: Receives a pointer to an IMMDevice interface of      *
    *            the device's endpoint object                         *                                             *                                            *
    *                                                                 *
    ******************************************************************/
    HRESULT GetDevice(IMMDevice** ppDevice)
    {
       IMMDeviceEnumerator    *pEnumerator = NULL;
       IMMDevice              *pDevice = NULL;
       IMMDeviceCollection    *pEndpoints = NULL;
       UINT                    cEndpoints = 0;

       const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
       const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

       // Get enumerator for audio endpoint devices
       hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, 
           NULL,
           CLSCTX_ALL, 
           IID_IMMDeviceEnumerator,
           (void**)&pEnumerator));


       EXIT_ON_ERROR(hr)

       // Enumerate all active endpoints,
       hr = pEnumerator->EnumAudioEndpoints (
           eRender,
           DEVICE_STATE_ACTIVE,
           &pEndpoints);
       EXIT_ON_ERROR(hr)

       hr = pEndpoints->GetCount(&cEndpoints);
       EXIT_ON_ERROR(hr)

       for (UINT i = 0; i < cEndpoints; i++)
       {
           hr = pEndpoints->Item(i, &pDevice);
           IF_FAILED_JUMP(hr, Exit);
           {
               // Select the endpoint that meets the requirements.
               // For example, SPDIF analog output or HDMI
               if (IsDigitalEndpoint(pDevice))
               {
                   *(ppDevice) = pDevice;
                   (*ppDevice)->AddRef();
                   break;
               }
           }
           SAFE_RELEASE(pDevice);
       }
    Exit:
       if (FAILED(hr))
       {
           // Notify error.
           // Not Shown.
       }
       SAFE_RELEASE(pEndpoints);
       SAFE_RELEASE(pEnumerator);
    }
    ```

    

3.  <span data-ttu-id="604d0-157">Verwenden Sie den [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Zeiger auf den Endpunkt, der vom enumerationsprozess zurückgegeben wird, um die gewünschte Audiostreaming-API zu aktivieren und das Streaming vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="604d0-157">Use the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) pointer to the endpoint returned by the enumeration process to activate the desired audio streaming API and prepare for streaming.</span></span> <span data-ttu-id="604d0-158">Unterschiedliche audioapis erfordern eine etwas andere Vorbereitung.</span><span class="sxs-lookup"><span data-stu-id="604d0-158">Different audio APIs require slightly different preparation.</span></span>
    -   <span data-ttu-id="604d0-159">Für DShow-Audioanwendungen:</span><span class="sxs-lookup"><span data-stu-id="604d0-159">For DShow audio applications:</span></span>
        1.  <span data-ttu-id="604d0-160">Erstellen Sie ein DirectShow-com-Objekt, indem Sie [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) aufrufen und IID \_ ibasefilter als Schnittstellen Bezeichner angeben.</span><span class="sxs-lookup"><span data-stu-id="604d0-160">Create a DirectShow COM object by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) and specifying IID\_IBaseFilter as the interface identifier.</span></span>
            ```cpp
            IUnknown *pDShowFilter = NULL;
            ...
            hr = pDevice->Activate (
                              IID_IBaseFilter,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pDShowFilter));
            ```

            

        2.  <span data-ttu-id="604d0-161">Erstellen Sie ein DirectShow-Filter Diagramm mit diesem com-Objekt, das vom Gerät aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="604d0-161">Build a DirectShow filter graph with this COM object activated by the device.</span></span> <span data-ttu-id="604d0-162">Weitere Informationen zu diesem Prozess finden Sie unter "Aufbau des Filter Diagramms" in der DirectShow-SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="604d0-162">For more information about this process, see "Building the Filter Graph" in DirectShow SDK documentation.</span></span>
    -   <span data-ttu-id="604d0-163">Für DSound-Audioanwendungen:</span><span class="sxs-lookup"><span data-stu-id="604d0-163">For DSound audio applications:</span></span>
        1.  <span data-ttu-id="604d0-164">Erstellen Sie ein DSound com-Objekt durch Aufrufen von [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) und Angeben von IID \_ IDirectSound8 als Schnittstellen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="604d0-164">Create a DSound COM object by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) and specifying IID\_IDirectSound8 as the interface identifier.</span></span>
            ```cpp
            IDirectSound8  *pDSSound8;
            ...
            hr = pDevice->Activate (
                              IID_IDirectSound8,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pDSSound8));
            ```

            

        2.  <span data-ttu-id="604d0-165">Verwenden Sie das zuvor erstellte DSound-Objekt, um DSound für das Streaming zu programmieren.</span><span class="sxs-lookup"><span data-stu-id="604d0-165">Use DSound object created above to program DSound for steaming.</span></span> <span data-ttu-id="604d0-166">Weitere Informationen zu diesem Prozess finden Sie unter [DirectSound](/previous-versions//bb219818(v=vs.85)) auf MSDN.</span><span class="sxs-lookup"><span data-stu-id="604d0-166">For more information about this process, see [DirectSound](/previous-versions//bb219818(v=vs.85)) on MSDN.</span></span>
    -   <span data-ttu-id="604d0-167">Für WASAPI:</span><span class="sxs-lookup"><span data-stu-id="604d0-167">For WASAPI:</span></span>
        1.  <span data-ttu-id="604d0-168">Erstellen Sie ein [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) com-Objekt durch Aufrufen von [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) und Angeben von IID \_ iaudioclient als Schnittstellen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="604d0-168">Create an [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) COM object by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) and specifying IID\_IAudioClient as the interface identifier.</span></span>
            ```cpp
            IAudioClient *pIAudioClient = NULL;
            ...
            hr = pDevice->Activate (
                              IID_IAudioClient,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pIAudioClient));
            ```

            

        2.  <span data-ttu-id="604d0-169">Öffnen Sie den Audiodatenstrom.</span><span class="sxs-lookup"><span data-stu-id="604d0-169">Open the audio stream.</span></span>
            ```cpp
            hr = pIAudioClient->Initialize(...);
            ```

            
4.  <span data-ttu-id="604d0-170">Starten Sie Audiostreaming.</span><span class="sxs-lookup"><span data-stu-id="604d0-170">Start audio streaming.</span></span>
5.  <span data-ttu-id="604d0-171">Legen Sie die Schutzrichtlinie für den Stream fest.</span><span class="sxs-lookup"><span data-stu-id="604d0-171">Set the protection policy on the stream.</span></span>
    1.  <span data-ttu-id="604d0-172">Rufen Sie für WASAPI-Clients einen Verweis auf die [**imftrustdoutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) -Schnittstelle des Objekts der Output Trust Authority (OTA) für den Datenstrom ab, indem Sie [**iaudioclient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) aufrufen und IID \_ imftrustdoutput als Schnittstellen Bezeichner angeben.</span><span class="sxs-lookup"><span data-stu-id="604d0-172">For WASAPI clients, get a reference to the [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) interface of the output trust authority (OTA) object for the stream by calling [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) and specifying IID\_IMFTrustedOutput as the interface identifier.</span></span>
        ```cpp
        IMFTrustedOutput*       pTrustedOutput = NULL;
        hr = pIAudioClient>GetService(
                       __uuidof(IMFTrustedOutput),
                       (void**)& pTrustedOutput);
        ```

        

    2.  <span data-ttu-id="604d0-173">Rufen Sie die Anzahl der verfügbaren OTA-Objekte durch Aufrufen von [**imftreudoutput:: getoutputtrustautoritycount**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritycount)ab.</span><span class="sxs-lookup"><span data-stu-id="604d0-173">Get a count of the available OTA objects by calling [**IMFTrustedOutput::GetOutputTrustAuthorityCount**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritycount).</span></span>
        ```cpp
        hr = pTrustedOutput->GetOutputTrustAuthorityCount(&m_dwCountOTA);
        ```

        

    3.  <span data-ttu-id="604d0-174">Auflisten der OTA-Auflistung und erhalten eines Verweises auf das OTA-Objekt, das die Aktion "Peer Action Play" unterstützt \_ .</span><span class="sxs-lookup"><span data-stu-id="604d0-174">Enumerate the OTA collection and get a reference to the OTA object that supports the action PEACTION\_PLAY.</span></span> <span data-ttu-id="604d0-175">Alle OTAS machen die [**IMF outputtrustauthority**](/windows/win32/api/mfidl/nn-mfidl-imfoutputtrustauthority) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="604d0-175">All OTAs expose the [**IMFOutputTrustAuthority**](/windows/win32/api/mfidl/nn-mfidl-imfoutputtrustauthority) interface.</span></span>
        ```cpp
        hr = pMFTrustedOutput->GetOutputTrustAuthorityByIndex(I, &pMFOutputTrustAuthority);
        hr = pMFOutputTrustAuthority->GetAction(&action) 
        ```

        

    4.  <span data-ttu-id="604d0-176">Verwenden Sie die [**imftreudoutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) -Schnittstelle, um die Schutzrichtlinie für den Stream festzulegen.</span><span class="sxs-lookup"><span data-stu-id="604d0-176">Use the [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) interface to set the protection policy on the stream.</span></span>

        ```cpp
        hr = pTrustedOutput ->SetPolicy(&pPolicy, nPolicy, &pbTicket, &cbTicket);
        ```

        

        > [!Note]
        > <span data-ttu-id="604d0-177">Wenn Sie den EVR verwenden, löst [**setpolicy**](/windows/win32/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) das [MEPolicySet](../medfound/mepolicyset.md) -Ereignis aus und gibt den Wert \_ von MF S \_ Wait \_ for \_ Policy Set aus, \_ um anzugeben, dass die OTA die Richtlinie asynchron erzwingen wird.</span><span class="sxs-lookup"><span data-stu-id="604d0-177">If you are using the EVR, [**SetPolicy**](/windows/win32/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) raises the [MEPolicySet](../medfound/mepolicyset.md) event and returns MF\_S\_WAIT\_FOR\_POLICY\_SET to indicate that the OTA will enforce the policy asynchronously.</span></span> <span data-ttu-id="604d0-178">In diesem Beispielcode ist die Anwendung jedoch ein direkter WASAPI-Client, der das OTA-Objekt aus dem AudioClient abgerufen hat (Schritt 5 a).</span><span class="sxs-lookup"><span data-stu-id="604d0-178">However, in this example code, the application is a direct WASAPI client that retrieved the OTA object from the audio client (Step 5 a).</span></span> <span data-ttu-id="604d0-179">Im Gegensatz zum EVR implementieren ein AudioClient und andere WASAPI-Objekte keine Medienereignis Generatoren.</span><span class="sxs-lookup"><span data-stu-id="604d0-179">Unlike the EVR, an audio client and other WASAPI objects do not implement media event generators.</span></span> <span data-ttu-id="604d0-180">Ohne Medienereignis Generatoren gibt **IMF commitdoutput:: setpolicy** nicht den Wert \_ von MF S \_ Wait \_ for \_ Policy Set zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="604d0-180">Without media event generators, **IMFTrustedOutput::SetPolicy** does not return MF\_S\_WAIT\_FOR\_POLICY\_SET.</span></span>
        >
        > <span data-ttu-id="604d0-181">Die audiorichtlinieneinstellungen müssen festgelegt werden, nachdem das Audiostreaming gestartet wurde; andernfalls tritt bei [**IMF-Fehler ein Fehler**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritybyindex) auf.</span><span class="sxs-lookup"><span data-stu-id="604d0-181">The audio policy settings must be set after audio streaming starts, otherwise [**IMFTrustedOutput::GetOutputTrustAuthorityByIndex**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritybyindex) fails.</span></span> <span data-ttu-id="604d0-182">Außerdem muss der zugrunde liegende Audiotreiber ein *vertrauenswürdiger Treiber* sein, um diese Funktion zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="604d0-182">Also, to support this feature, the underlying audio driver must be a *trusted driver*.</span></span>

         

        <span data-ttu-id="604d0-183">Im Beispielcode ist *pPolicy* ein Zeiger auf die [**imfoutputpolicy**](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) -Schnittstelle eines vom Client implementierten Richtlinien Objekts.</span><span class="sxs-lookup"><span data-stu-id="604d0-183">In the example code, *pPolicy* is a pointer to the [**IMFOutputPolicy**](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) interface of a client-implemented policy object.</span></span> <span data-ttu-id="604d0-184">Weitere Informationen finden Sie unter [Media Foundation SDK](../medfound/microsoft-media-foundation-sdk.md) -Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="604d0-184">For information, see [Media Foundation SDK](../medfound/microsoft-media-foundation-sdk.md) documentation.</span></span>

        <span data-ttu-id="604d0-185">In der Implementierung der [**IMF outputpolicy:: generaterequiredschemas**](/windows/win32/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) -Methode muss eine Sammlung der Ausgabe Schutzsysteme (Schemas) generiert werden, die die OTA erzwingen muss.</span><span class="sxs-lookup"><span data-stu-id="604d0-185">In the implementation of the [**IMFOutputPolicy::GenerateRequiredSchemas**](/windows/win32/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) method, a collection of the output protection systems (schemas) must be generated that the OTA must enforce.</span></span> <span data-ttu-id="604d0-186">Jedes Schema wird durch eine GUID identifiziert und enthält Konfigurationsdaten für das Schutzsystem.</span><span class="sxs-lookup"><span data-stu-id="604d0-186">Each schema is identified by a GUID and contains configuration data for the protection system.</span></span> <span data-ttu-id="604d0-187">Stellen Sie sicher, dass die Schutzsysteme in der Sammlung auf die Verwendung vertrauenswürdiger Audiotreiber beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="604d0-187">Make sure that the protection systems in the collection are restricted to using trusted audio drivers.</span></span> <span data-ttu-id="604d0-188">Diese Einschränkung wird durch die GUID, den **MF-Schutz " \_ Treuhänder**", "deaktivieren" oder "Configuration Manager" identifiziert.</span><span class="sxs-lookup"><span data-stu-id="604d0-188">This restriction is identified by the GUID, **MFPROTECTION\_TRUSTEDAUDIODRIVERS**,DISABLE, or CONSTRICTAUDIO.</span></span> <span data-ttu-id="604d0-189">Bei Verwendung von MF Protection Trust- \_ diodrivers werden die Konfigurationsdaten für dieses Schema als DWORD bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="604d0-189">If MFPROTECTION\_TRUSTEDAUDIODRIVERS is used, the configuration data for this schema is a DWORD.</span></span> <span data-ttu-id="604d0-190">Weitere Informationen zu den Schemas und den zugehörigen Konfigurationsdaten finden Sie in der Dokumentation zum SDK für geschützte Umgebungen.</span><span class="sxs-lookup"><span data-stu-id="604d0-190">For more information about the schemas and the related configuration data, see Protected Environment SDK documentation.</span></span>

        <span data-ttu-id="604d0-191">Der Client muss auch die Schema Definition bereitstellen, indem er die [**IMF OutputSchema**](/windows/win32/api/mfidl/nn-mfidl-imfoutputschema) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="604d0-191">The client must also provide the schema definition, by implementing the [**IMFOutputSchema**](/windows/win32/api/mfidl/nn-mfidl-imfoutputschema) interface.</span></span> <span data-ttu-id="604d0-192">[**IMF OutputSchema:: GetSchemaType**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getschematype) ruft **MF Protection- \_ Treuhänder** als Schema-GUID ab.</span><span class="sxs-lookup"><span data-stu-id="604d0-192">[**IMFOutputSchema::GetSchemaType**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getschematype) retrieves **MFPROTECTION\_TRUSTEDAUDIODRIVERS** as the schema GUID.</span></span> <span data-ttu-id="604d0-193">[**Imfoutputschema:: GetConfigurationData**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getconfigurationdata) gibt einen Zeiger auf die Konfigurationsdaten des Schemas zurück.</span><span class="sxs-lookup"><span data-stu-id="604d0-193">[**IMFOutputSchema::GetConfigurationData**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getconfigurationdata) returns a pointer to the schema's configuration data.</span></span>

6.  <span data-ttu-id="604d0-194">Audiostreaming fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="604d0-194">Continue audio streaming.</span></span>
7.  <span data-ttu-id="604d0-195">Stellen Sie sicher, dass die Schutzrichtlinie vor dem Beenden des Streamings eindeutig ist</span><span class="sxs-lookup"><span data-stu-id="604d0-195">Make sure the protection policy is clear before stopping streaming.</span></span>

    <span data-ttu-id="604d0-196">Geben Sie die zugehörigen Verweise der Richtlinien Schnittstellen weiter oben frei.</span><span class="sxs-lookup"><span data-stu-id="604d0-196">Release the related policy interface references above.</span></span>

    <span data-ttu-id="604d0-197">Die releaseaufrufe löschen die zuvor festgelegten Richtlinien Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="604d0-197">The release calls clear the previously set policy settings.</span></span>

    > [!Note]  
    > <span data-ttu-id="604d0-198">Jedes Mal, wenn ein Stream neu gestartet wird, muss die Schutzrichtlinie erneut für den Datenstrom festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="604d0-198">Every time a stream is restarted, the protection policy must be set again on the stream.</span></span> <span data-ttu-id="604d0-199">Die Prozedur wird in Schritt 5-d beschrieben.</span><span class="sxs-lookup"><span data-stu-id="604d0-199">The procedure is described in step 5-d.</span></span>

    ```cpp
    pMFOutputTrustAuthority->Release()
    pMFTrustedOutput->Release()
    ```
  

<span data-ttu-id="604d0-200">Die folgenden Codebeispiele zeigen eine Beispiel Implementierung der Richtlinien-und Schema Objekte.</span><span class="sxs-lookup"><span data-stu-id="604d0-200">The following code examples show a sample implementation of the policy and schema objects.</span></span>


```cpp
//OTADsoundSample.cpp
#include <stdio.h>
#include <tchar.h>
#include <initguid.h>
#include <windows.h>
#include <mmreg.h>
#include <dsound.h>

#include <mfidl.h>
#include <Mmdeviceapi.h>
#include <AVEndpointKeys.h>
#include "OTADSoundSample.h"

#define STATIC_KSDATAFORMAT_SUBTYPE_AC3\
    DEFINE_WAVEFORMATEX_GUID(WAVE_FORMAT_DOLBY_AC3_SPDIF)
DEFINE_GUIDSTRUCT("00000092-0000-0010-8000-00aa00389b71", KSDATAFORMAT_SUBTYPE_AC3);
#define KSDATAFORMAT_SUBTYPE_AC3 DEFINE_GUIDNAMED(KSDATAFORMAT_SUBTYPE_AC3)


HRESULT SetOTAPolicy(IMMDevice *_pMMDevice,
                     DWORD _dwConfigData,
                     IMFTrustedOutput **_ppMFTrustedOutput,
                     IMFOutputTrustAuthority **ppMFOutputTrustAuthority,
                     IMFOutputPolicy **_ppMFOutputPolicy);
HRESULT ClearOTAPolicy(IMFTrustedOutput *_pMFTrustedOutput,
                       IMFOutputTrustAuthority *_pMFOutputTrustAuthority,
                       IMFOutputPolicy *_pMFOutputPolicy);


const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

BOOL IsDigitalEndpoint(IMMDevice *pDevice)
{
    PROPVARIANT         var;
    IPropertyStore      *pProperties = NULL;
    EndpointFormFactor  formfactor;
    BOOL                bResult = FALSE;
    HRESULT             hr = S_OK;
    PropVariantInit(&var);

    // Open endpoint properties
    hr = pDevice->OpenPropertyStore(STGM_READ, &pProperties);
    IF_FAILED_JUMP(hr, Exit);

    // get form factor 
    hr = pProperties->GetValue(PKEY_AudioEndpoint_FormFactor, &var);
    IF_FAILED_JUMP(hr, Exit);

    formfactor = (EndpointFormFactor)var.uiVal;
    if ((SPDIF == formfactor) || (DigitalAudioDisplayDevice == formfactor))
    {
        bResult = TRUE;
    }

Exit:
    PropVariantClear(&var);
    SAFE_RELEASE(pProperties);

    return bResult;
}


HRESULT GetDigitalAudioEndpoint(IMMDevice** ppDevice)
{
    IMMDeviceEnumerator    *pEnumerator = NULL;
    IMMDevice              *pDevice = NULL;
    IMMDeviceCollection    *pEndpoints = NULL;
    UINT                    cEndpoints = 0;
    HRESULT hr = S_OK;

    *ppDevice = NULL;
    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(CLSID_MMDeviceEnumerator, NULL,
                          CLSCTX_ALL, IID_IMMDeviceEnumerator,
                          (void**)&pEnumerator);
    IF_FAILED_JUMP(hr, Exit);

    // Enumerate all active render endpoints, 
    hr = pEnumerator->EnumAudioEndpoints(eRender, DEVICE_STATE_ACTIVE, &pEndpoints);
    IF_FAILED_JUMP(hr, Exit);

    hr = pEndpoints->GetCount(&cEndpoints);
    IF_FAILED_JUMP(hr, Exit);

    for (UINT i = 0; i < cEndpoints; i++)
    {
        hr = pEndpoints->Item(i, &pDevice);
        IF_FAILED_JUMP(hr, Exit);
        // Select the endpoint that meets the requirements.
        // For example, SPDIF analog output or HDMI
        // Not Shown.
        if (IsDigitalEndpoint(pDevice))
        {
            *ppDevice = pDevice;
            (*ppDevice)->AddRef();
            break;
        }
        SAFE_RELEASE(pDevice);
    }
Exit:
    if (FAILED(hr))
    {
        // Notify error.
        // Not Shown.
    }
    SAFE_RELEASE(pEndpoints);
    SAFE_RELEASE(pEnumerator);
    return hr; 
}


//-------------------------------------------------------------------
int __cdecl wmain(int argc, char* argv[])
{
    IMMDevice *pEndpoint=NULL;
    HRESULT hr = S_OK;

    // DSound related variables
    IDirectSound8*          DSSound8 = NULL; 
    IDirectSoundBuffer*     DSBuffer = NULL; 
    DSBUFFERDESC            DSBufferDesc;
    WAVEFORMATEXTENSIBLE    wfext;
    WORD nChannels = 2;
    DWORD nSamplesPerSec = 48000;
    WORD wBitsPerSample = 16;

    // OTA related variables
    IMFTrustedOutput *pMFTrustedOutput=NULL;
    IMFOutputPolicy *pMFOutputPolicy=NULL;
    IMFOutputTrustAuthority *pMFOutputTrustAuthority=NULL;
    DWORD dwConfigData=0;

    // Initialize COM
    hr = CoInitialize(NULL);
    IF_FAILED_JUMP(hr, Exit);

    printf("OTA test app for DSound\n");

    hr = GetDigitalAudioEndpoint(&pEndpoint);
    IF_FAILED_JUMP(hr, Exit);

    if (pEndpoint)
    {
        printf("Found digital audio endpoint.\n");
    }
    //
    // Active DSound interface
    //
    hr = pEndpoint->Activate(IID_IDirectSound8, CLSCTX_INPROC_SERVER, NULL, reinterpret_cast<void **>(&DSSound8));
    IF_FAILED_JUMP(hr, Exit);

    nChannels = 2;
    nSamplesPerSec = 48000;
    wBitsPerSample = 16;

    ZeroMemory(&wfext, sizeof(wfext));
    wfext.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
    wfext.Format.nChannels = nChannels;
    wfext.Format.nSamplesPerSec = nSamplesPerSec;
    wfext.Format.wBitsPerSample = wBitsPerSample;
    wfext.Format.nBlockAlign = (nChannels * wBitsPerSample) / 8;
    wfext.Format.nAvgBytesPerSec = nSamplesPerSec * ((nChannels * wBitsPerSample) / 8);
    wfext.Format.cbSize = 22;
    wfext.Samples.wValidBitsPerSample = wBitsPerSample;
    wfext.dwChannelMask = 0x3;
    wfext.SubFormat = KSDATAFORMAT_SUBTYPE_PCM;
#if 1 
    wfext.SubFormat = KSDATAFORMAT_SUBTYPE_AC3;
#endif

    ZeroMemory(&DSBufferDesc, sizeof(DSBufferDesc));
    DSBufferDesc.dwSize = sizeof(DSBufferDesc);
    DSBufferDesc.dwFlags = DSBCAPS_GLOBALFOCUS | DSBCAPS_LOCSOFTWARE | DSBCAPS_GETCURRENTPOSITION2;
    DSBufferDesc.lpwfxFormat = (WAVEFORMATEX *)&wfext;
    DSBufferDesc.dwBufferBytes = wfext.Format.nAvgBytesPerSec / 100;

    HWND hwnd = GetForegroundWindow();
    hr = DSSound8->SetCooperativeLevel(hwnd, DSSCL_PRIORITY);
    IF_FAILED_JUMP(hr, Exit);

    hr = DSSound8->CreateSoundBuffer(&DSBufferDesc, &DSBuffer, NULL);
    IF_FAILED_JUMP(hr, Exit);

    hr = DSBuffer->Play(0, 0, DSBPLAY_LOOPING);
    IF_FAILED_JUMP(hr, Exit);

    printf("Will set the following audio policy:\n");
    printf("Test Certificate Enable: %s\n", TRUE ? "True" : "False");
    printf("Copy OK: %s\n", FALSE ? "True" : "False");
    printf("Digital Output Disable: %s\n", FALSE ? "True" : "False");
    printf("DRM Level: %u\n", 1300);

    // Set policy when the stream is in RUN state
    dwConfigData = MAKE_MFPROTECTIONDATA_TRUSTEDAUDIODRIVERS2(TRUE, /*_bTestCertificateEnable*/ 
                                                              FALSE, /*_bDigitalOutputDisable*/ 
                                                              FALSE, /*_bCopyOK*/ 
                                                              1300 /*_dwDrmLevel*/);

    hr = SetOTAPolicy(pEndpoint,dwConfigData, &pMFTrustedOutput, &pMFOutputTrustAuthority,&pMFOutputPolicy); 
    IF_FAILED_JUMP(hr, Exit);

    //
    // Perform all the necessary streaming operations here.
    //

    // stop audio streaming
    DSBuffer->Stop();

    // In order for the stream to restart successfully 
    // Need to release the following OutputTrust* interface to release audio endpoint
    hr = ClearOTAPolicy(pMFTrustedOutput,pMFOutputTrustAuthority,pMFOutputPolicy);
    IF_FAILED_JUMP(hr, Exit);

    // After above release operations, the following Play() will succeed without without device-in-use error message 0x8889000A
    DSBuffer->SetCurrentPosition(0);
    hr = DSBuffer->Play(0, 0, DSBPLAY_LOOPING);
    IF_FAILED_JUMP(hr, Exit);

    // Need to reset the new audio protection state because previous settings were gone with the ClearOTAPolicy call.
    dwConfigData = MAKE_MFPROTECTIONDATA_TRUSTEDAUDIODRIVERS2(TRUE, /*_bTestCertificateEnable*/ 
                                                              FALSE, /*_bDigitalOutputDisable*/ 
                                                              FALSE, /*_bCopyOK*/ 
                                                              1300 /*_dwDrmLevel*/);

    hr = SetOTAPolicy(pEndpoint,dwConfigData, &pMFTrustedOutput, &pMFOutputTrustAuthority,&pMFOutputPolicy); 
    IF_FAILED_JUMP(hr, Exit);

    // Clean up setting before leaving your streaming app.
    hr = ClearOTAPolicy(pMFTrustedOutput,pMFOutputTrustAuthority,pMFOutputPolicy);
    IF_FAILED_JUMP(hr, Exit);

    DSBuffer->SetCurrentPosition(0);

Exit:
    SAFE_RELEASE(DSBuffer);
    SAFE_RELEASE(DSSound8);

    SAFE_RELEASE(pEndpoint);

    CoUninitialize();

    return 0;
}
```




```cpp
//OTADSoundSample.h
// Macro defines
#define IF_FAILED_JUMP(_hresult, label)                         \
    if(FAILED(_hresult))                                        \
    {                                                           \
        goto label;                                             \
    }

#define SAFE_RELEASE(p) \
    if (NULL != p) { \
        (p)->Release(); \
        (p) = NULL; \
    }

#define IF_TRUE_ACTION_JUMP(condition, action, label)           \
    if(condition)                                               \
    {                                                           \
        action;                                                 \
        goto label;                                             \
    }
```




```cpp
// outputpolicy.h

class CTrustedAudioDriversOutputPolicy : public CMFAttributesImpl<IMFOutputPolicy> 
{
friend
    HRESULT CreateTrustedAudioDriversOutputPolicy(DWORD dwConfigData, IMFOutputPolicy **ppMFOutputPolicy);
private:
    ULONG m_cRefCount;
    DWORD m_dwConfigData;
    GUID m_guidOriginator;
    IMFOutputSchema *m_pOutputSchema;
    
    CTrustedAudioDriversOutputPolicy(DWORD dwConfigData, HRESULT &hr);
    ~CTrustedAudioDriversOutputPolicy();

public:
    // IUnknown methods
    HRESULT STDMETHODCALLTYPE QueryInterface(/* [in] */ REFIID riid,/* [out] */ LPVOID *ppvObject);
    ULONG STDMETHODCALLTYPE AddRef();
    ULONG STDMETHODCALLTYPE Release();
    
    // IMFOutputPolicy methods
    HRESULT STDMETHODCALLTYPE
        GenerateRequiredSchemas( 
            /* [in] */ DWORD dwAttributes,
            /* [in] */ GUID guidOutputSubType,
            /* [in] */ GUID *rgGuidProtectionSchemasSupported,
            /* [in] */ DWORD cProtectionSchemasSupported,
            /* [annotation][out] */ 
            __out  IMFCollection **ppRequiredProtectionSchemas);

    HRESULT STDMETHODCALLTYPE GetOriginatorID(/* [annotation][out] */ __out  GUID *pguidOriginatorID);

    HRESULT STDMETHODCALLTYPE GetMinimumGRLVersion(/* [annotation][out] */ __out  DWORD *pdwMinimumGRLVersion);
}; // CTrustedAudioDriversOutputPolicy

class CTrustedAudioDriversOutputSchema : public CMFAttributesImpl<IMFOutputSchema> 
{

friend
    HRESULT CreateTrustedAudioDriversOutputSchema(
        DWORD dwConfigData,
        GUID guidOriginatorID,
        IMFOutputSchema **ppMFOutputSchema
    );

private:
    CTrustedAudioDriversOutputSchema(DWORD dwConfigData, GUID guidOriginatorID);
    ~CTrustedAudioDriversOutputSchema();

    ULONG m_cRefCount;
    DWORD m_dwConfigData;
    GUID m_guidOriginatorID;
    
public:
    // IUnknown methods
    HRESULT STDMETHODCALLTYPE QueryInterface(
       /* [in] */ REFIID riid,
       /* [out] */ LPVOID *ppvObject
    );
    ULONG STDMETHODCALLTYPE AddRef();
    ULONG STDMETHODCALLTYPE Release();

    // IMFOutputSchema methods
    HRESULT STDMETHODCALLTYPE GetConfigurationData(__out DWORD *pdwVal);
    HRESULT STDMETHODCALLTYPE GetOriginatorID(__out GUID *pguidOriginatorID);
    HRESULT STDMETHODCALLTYPE GetSchemaType(__out GUID *pguidSchemaType);

}; // CTrustedAudioDriversOutputSchema
```




```cpp
// outputpolicy.cpp

#include <windows.h>
#include <tchar.h>
#include <mfidl.h>
#include <atlstr.h>
#include <attributesbase.h>
#include "OTADSoundSample.h"

#include <Mmdeviceapi.h>
#include "OutputPolicy.h"

#define RETURN_INTERFACE(T, iid, ppOut) \
    if (IsEqualIID(__uuidof(T), (iid))) { \
        this->AddRef(); \
        *(ppOut) = static_cast<T *>(this); \
        return S_OK; \
    } else {} (void)0

//--------------------------------------------------------------------------
// Implementation for CTrustedAudioDriversOutputPolicy
//--------------------------------------------------------------------------
// constructor
CTrustedAudioDriversOutputPolicy::CTrustedAudioDriversOutputPolicy(DWORD dwConfigData, HRESULT &hr)
: m_cRefCount(1), m_dwConfigData(dwConfigData), m_pOutputSchema(NULL)
{
    hr = CoCreateGuid(&m_guidOriginator);
    IF_FAILED_JUMP(hr, Exit);

    hr = CreateTrustedAudioDriversOutputSchema(dwConfigData, m_guidOriginator, &m_pOutputSchema);
    IF_FAILED_JUMP(hr, Exit);

Exit:
    if (FAILED(hr))
    {
        printf("CreateTrustedAudioDriversOutputSchema failed: hr = 0x%08x", hr);
    }
    return;
}

// destructor
CTrustedAudioDriversOutputPolicy::~CTrustedAudioDriversOutputPolicy()
{
    if (NULL != m_pOutputSchema) 
    {
        m_pOutputSchema->Release();
    }
}


// IUnknown::QueryInterface
HRESULT STDMETHODCALLTYPE
    CTrustedAudioDriversOutputPolicy::QueryInterface(
        /* [in] */ REFIID riid,
        /* [out] */ LPVOID *ppvObject)
{
    HRESULT hr = E_NOINTERFACE;

    IF_TRUE_ACTION_JUMP((NULL == ppvObject), hr = E_POINTER, Exit);

    *ppvObject = NULL;

    RETURN_INTERFACE(IUnknown, riid, ppvObject);
    RETURN_INTERFACE(IMFAttributes, riid, ppvObject);
    RETURN_INTERFACE(IMFOutputPolicy, riid, ppvObject);    

Exit:
    return hr;
}

// IUnknown::AddRef
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::AddRef() 
{
    ULONG uNewRefCount = InterlockedIncrement(&m_cRefCount);
    return uNewRefCount;
}

// IUnknown::Release
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::Release() 
{
    ULONG uNewRefCount = InterlockedDecrement(&m_cRefCount);
    if (0 == uNewRefCount) 
    {
        delete this;
    }
    return uNewRefCount;
}

// IMFOutputPolicy::GenerateRequiredSchemas
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::GenerateRequiredSchemas
( 
        /* [in] */ DWORD dwAttributes,
        /* [in] */ GUID guidOutputSubType,
        /* [in] */ GUID *rgGuidProtectionSchemasSupported,
        /* [in] */ DWORD cProtectionSchemasSupported,
        /* [annotation][out] */ 
        __out  IMFCollection **ppRequiredProtectionSchemas
)
{
    HRESULT hr = S_OK;
    bool bTrustedAudioDriversSupported = false;
    // if we've made it this far then the Output Trust Authority supports Trusted Audio Drivers
    // create a collection and put our output policy in it
    // then give that collection to the caller
    CComPtr<IMFCollection> pMFCollection;

    // sanity checks
    IF_TRUE_ACTION_JUMP((NULL == ppRequiredProtectionSchemas), hr = E_POINTER, Exit); 
    *ppRequiredProtectionSchemas = NULL;

    IF_TRUE_ACTION_JUMP((NULL == rgGuidProtectionSchemasSupported) && (0 != cProtectionSchemasSupported), 
                    hr = E_POINTER, Exit); 

    // log all the supported protection schemas
    for (DWORD i = 0; i < cProtectionSchemasSupported; i++) 
    {
        if (IsEqualIID(MFPROTECTION_TRUSTEDAUDIODRIVERS, rgGuidProtectionSchemasSupported[i])) 
        {
            bTrustedAudioDriversSupported = true;
        }
    }

    if (!bTrustedAudioDriversSupported) 
    {
        return HRESULT_FROM_WIN32(ERROR_RANGE_NOT_FOUND);
    }


    // create the collection
    hr = MFCreateCollection(&pMFCollection);
    if (FAILED(hr)) 
    {
        return hr;
    }

    // add our output policy to the collection
    hr = pMFCollection->AddElement(m_pOutputSchema);
    if (FAILED(hr)) 
    {
        return hr;
    }
Exit:
    // give the collection to the caller
    return pMFCollection.CopyTo(ppRequiredProtectionSchemas); // increments refcount
}// GenerateRequiredSchemas

HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::GetOriginatorID(__out  GUID *pguidOriginatorID) 
{
    if (NULL == pguidOriginatorID) 
    {
        return E_POINTER;
    }
    *pguidOriginatorID = m_guidOriginator;
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::GetMinimumGRLVersion(__out  DWORD *pdwMinimumGRLVersion) 
{
    if (NULL == pdwMinimumGRLVersion) 
    {
        return E_POINTER;
    }
    *pdwMinimumGRLVersion = 0;
    return S_OK;
}

//--------------------------------------------------------------------------
// Implementation for CTrustedAudioDriversOutputSchema
//--------------------------------------------------------------------------
// constructor
CTrustedAudioDriversOutputSchema::CTrustedAudioDriversOutputSchema
(    
    DWORD dwConfigData, 
    GUID guidOriginatorID
)
: m_cRefCount(1)
, m_dwConfigData(dwConfigData)
, m_guidOriginatorID(guidOriginatorID)
{}

// destructor
CTrustedAudioDriversOutputSchema::~CTrustedAudioDriversOutputSchema() {}

// IUnknown::QueryInterface
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::QueryInterface
(
        /* [in] */ REFIID riid,
        /* [out] */ LPVOID *ppvObject
) 
{
    HRESULT hr = E_NOINTERFACE;

    IF_TRUE_ACTION_JUMP((NULL == ppvObject), hr = E_POINTER, Exit);
    *ppvObject = NULL;

    RETURN_INTERFACE(IUnknown, riid, ppvObject);
    RETURN_INTERFACE(IMFAttributes, riid, ppvObject);
    RETURN_INTERFACE(IMFOutputSchema, riid, ppvObject);

Exit:
    return hr;
}

// IUnknown::AddRef
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::AddRef() 
{
    ULONG uNewRefCount = InterlockedIncrement(&m_cRefCount);
    return uNewRefCount;
}

// IUnknown::Release
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::Release() 
{
    ULONG uNewRefCount = InterlockedDecrement(&m_cRefCount);
    if (0 == uNewRefCount) 
    {
        delete this;
    }
    return uNewRefCount;
}
// IMFOutputSchema::GetConfigurationData
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::GetConfigurationData(__out DWORD *pdwVal) 
{
    if (NULL == pdwVal) { return E_POINTER; }
    *pdwVal = m_dwConfigData;
    return S_OK;
}

// IMFOutputSchema::GetOriginatorID
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::GetOriginatorID(__out GUID *pguidOriginatorID) 
{
    if (NULL == pguidOriginatorID) { return E_POINTER; }
    *pguidOriginatorID = m_guidOriginatorID;
    return S_OK;
}
// IMFOutputSchema::GetSchemaType
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::GetSchemaType(__out GUID *pguidSchemaType) 
{
    if (NULL == pguidSchemaType) { return E_POINTER; }
    *pguidSchemaType = MFPROTECTION_TRUSTEDAUDIODRIVERS;
    return S_OK;
}

//---------------------------------------------------------------------------------------------------
//
// Other subroutine declarations
//
//---------------------------------------------------------------------------------------------------
HRESULT CreateTrustedAudioDriversOutputPolicy(DWORD dwConfigData, IMFOutputPolicy **ppMFOutputPolicy) 
{
    if (NULL == ppMFOutputPolicy) 
    {
        return E_POINTER;
    }

    *ppMFOutputPolicy = NULL;

    HRESULT hr = S_OK;
    CTrustedAudioDriversOutputPolicy *pPolicy = new CTrustedAudioDriversOutputPolicy(dwConfigData, hr);
    if (NULL == pPolicy) 
    {
        return E_OUTOFMEMORY;
    }
    if (FAILED(hr)) 
    {
        delete pPolicy;
        return hr;
    }
    *ppMFOutputPolicy = static_cast<IMFOutputPolicy *>(pPolicy);
    return S_OK;
}// CreateTrustedAudioDriversOutputPolicy

HRESULT CreateTrustedAudioDriversOutputSchema
(
    DWORD dwConfigData,
    GUID guidOriginatorID,
    IMFOutputSchema **ppMFOutputSchema) 
{
    if (NULL == ppMFOutputSchema) 
    {
        return E_POINTER;
    }

    *ppMFOutputSchema = NULL;

    CTrustedAudioDriversOutputSchema *pSchema =
        new CTrustedAudioDriversOutputSchema(dwConfigData, guidOriginatorID);

    if (NULL == pSchema) 
    {
        return E_OUTOFMEMORY;
    }

    *ppMFOutputSchema = static_cast<IMFOutputSchema *>(pSchema);

    return S_OK;
}// CreateTrustedAudioDriversOutputSchema



HRESULT SetOTAPolicy(IMMDevice *_pMMDevice,
                     DWORD _dwConfigData,
                     IMFTrustedOutput **_ppMFTrustedOutput,
                     IMFOutputTrustAuthority **ppMFOutputTrustAuthority,
                     IMFOutputPolicy **_ppMFOutputPolicy)
{
    HRESULT hr = S_OK;

    DWORD dwCountOfOTAs = 0;
    bool bRet = false;

    hr = CreateTrustedAudioDriversOutputPolicy(_dwConfigData, _ppMFOutputPolicy);
    IF_FAILED_JUMP(hr, Exit);

    // activate IMFTrustedOutput
    hr = _pMMDevice->Activate(__uuidof(IMFTrustedOutput), CLSCTX_ALL, NULL,
                             (void**)_ppMFTrustedOutput);
    IF_FAILED_JUMP(hr, Exit);

    // get count of Output Trust Authorities on this trusted output
    hr = (*_ppMFTrustedOutput)->GetOutputTrustAuthorityCount(&dwCountOfOTAs);
    IF_FAILED_JUMP(hr, Exit);

    // sanity check - fail on endpoints with no output trust authorities
    IF_TRUE_ACTION_JUMP((0 == dwCountOfOTAs), hr = E_NOTFOUND, Exit);

    printf("dwCountOfOTAs = %d\n", dwCountOfOTAs);

     
    // loop over each output trust authority on the endpoint
    for (DWORD i = 0; i < dwCountOfOTAs; i++) 
    {
        // get the output trust authority
        hr = (*_ppMFTrustedOutput)->GetOutputTrustAuthorityByIndex(i, ppMFOutputTrustAuthority);
        IF_FAILED_JUMP(hr, Exit);


        // log the purpose of the output trust authority
        MFPOLICYMANAGER_ACTION action;
        hr = (*ppMFOutputTrustAuthority)->GetAction(&action);
        if (FAILED(hr)) 
        {
            return hr;
        }

        printf(" It's %s.", (PEACTION_PLAY==action) ? "PEACTION_PLAY" :
                            (PEACTION_COPY==action) ? "PEACTION_COPY" :
                            "Others");
 
        // only PEACTION_PLAY Output Trust Authorities are relevant
        if (PEACTION_PLAY != action) 
        {
            printf("Skipping as the OTA action is not PEACTION_PLAY");
            SAFE_RELEASE(*ppMFOutputTrustAuthority);
            continue;
        }

        BYTE *pbTicket = NULL;
        DWORD cbTicket = 0;
        // audio ota does not support ticket, leaving it NULL is ok.
        hr = (*ppMFOutputTrustAuthority)->SetPolicy(_ppMFOutputPolicy, 1, &pbTicket, &cbTicket);
        IF_FAILED_JUMP(hr, Exit);
        printf("SetPolicy succeeded.\n");

        bRet = true;
        break;

    }// for each output trust authority

Exit:
    if (bRet)
    {
        hr = S_OK;
    }
    if (FAILED(hr))
    {
        printf("failure code is 0x%0x\n", hr);
        SAFE_RELEASE(*ppMFOutputTrustAuthority);
        SAFE_RELEASE(*_ppMFTrustedOutput);
        if (*_ppMFOutputPolicy)
        {
            delete (*_ppMFOutputPolicy);
        }
    }

    return hr;
}


HRESULT ClearOTAPolicy(IMFTrustedOutput *_pMFTrustedOutput,
                       IMFOutputTrustAuthority *_pMFOutputTrustAuthority,
                       IMFOutputPolicy *_pMFOutputPolicy)
{
    SAFE_RELEASE(_pMFOutputTrustAuthority);
    SAFE_RELEASE(_pMFTrustedOutput);
    if (_pMFOutputPolicy)
    {
        delete _pMFOutputPolicy;
    }
    return S_OK;
}
```




```cpp
//OTADSoundSample.rc
#include "windows.h"

/////////////////////////////////////////////////////////////////////////////
// Version
#include <ntverp.h>

#define VER_FILETYPE                VFT_DLL
#define VER_FILESUBTYPE             VFT2_UNKNOWN
#define VER_FILEDESCRIPTION_STR     "Default Device Heuristic Dumper"
#define VER_INTERNALNAME_STR        "DefaultDeviceDump.exe"
#define VER_ORIGINALFILENAME_STR    "DefaultDeviceDump.exe"

#include "common.ver"
```




```cpp
Sources file:

TARGETNAME=OTADSoundSample
TARGETTYPE=PROGRAM
TARGET_DESTINATION=retail
UMTYPE=console
UMENTRY=wmain
UMBASE=0x1000000
#_NT_TARGET_VERSION=$(_NT_TARGET_VERSION_VISTA)
MSC_WARNING_LEVEL=$(MSC_WARNING_LEVEL) /WX
USE_ATL=1
ATL_VER=70
USE_NATIVE_EH=1
USE_MSVCRT=1
C_DEFINES=-DUNICODE -D_UNICODE
INCLUDES=$(INCLUDES);  

SOURCES=OTADSoundSample.cpp \
        OTADSoundSample.rc \
        outputpolicy.cpp\

TARGETLIBS=\
       $(SDK_LIB_PATH)\advapi32.lib         \
       $(SDK_LIB_PATH)\kernel32.lib         \
       $(SDK_LIB_PATH)\User32.lib           \
       $(SDK_LIB_PATH)\shlwapi.lib          \
       $(SDK_LIB_PATH)\ole32.lib            \
       $(SDK_LIB_PATH)\oleaut32.lib         \
       $(SDK_LIB_PATH)\rpcrt4.lib           \
       $(SDK_LIB_PATH)\strmiids.lib         \
       $(SDK_LIB_PATH)\uuid.lib             \
       $(SDK_LIB_PATH)\SetupAPI.lib         \
       $(SDK_LIB_PATH)\mfplat.lib \
```



## <a name="related-topics"></a><span data-ttu-id="604d0-201">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="604d0-201">Related topics</span></span>

[<span data-ttu-id="604d0-202">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="604d0-202">Programming Guide</span></span>](programming-guide.md)

[<span data-ttu-id="604d0-203">Benutzermodusaudiokomponenten</span><span class="sxs-lookup"><span data-stu-id="604d0-203">User-Mode Audio Components</span></span>](user-mode-audio-components.md)
