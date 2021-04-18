---
title: Behandeln geschützter Inhalte in der Anwendung
description: Behandeln geschützter Inhalte in der Anwendung
ms.assetid: b59d4abc-e59d-47a7-8d91-825ac20ae2eb
keywords:
- Windows Media Device Manager, Zertifikate
- Device Manager, Zertifikate
- Programmier Handbuch, Zertifikate
- Desktop Anwendungen, Zertifikate
- Erstellen von Windows Media Device Manager-Anwendungen,-Zertifikaten
- certificates
- Windows Media Device Manager, DRM-geschützter Inhalt
- Device Manager, DRM-geschützter Inhalt
- Programmier Handbuch, DRM-geschützter Inhalt
- Desktop Anwendungen, DRM-geschützter Inhalt
- Erstellen von Windows Media Device Manager-Anwendungen, DRM-geschütztem Inhalt
- DRM-geschützter Inhalt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc354e78b9c937db339f5bf6a167f504986fbb64
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340516"
---
# <a name="handling-protected-content-in-the-application"></a><span data-ttu-id="eb6f9-115">Behandeln geschützter Inhalte in der Anwendung</span><span class="sxs-lookup"><span data-stu-id="eb6f9-115">Handling Protected Content in the Application</span></span>

<span data-ttu-id="eb6f9-116">\[Das Windows Media DRM-Feature ist veraltet und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb6f9-116">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="eb6f9-117">Verwenden Sie stattdessen [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="eb6f9-117">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="eb6f9-118">Eine Anwendung muss über ein Übertragungs Zertifikat verfügen, um durch DRM geschützte Inhalte verarbeiten zu können.</span><span class="sxs-lookup"><span data-stu-id="eb6f9-118">An application must have a transfer certificate to be able to handle DRM-protected content.</span></span> <span data-ttu-id="eb6f9-119">Informationen dazu, wo Sie dieses Zertifikat erhalten, finden Sie unter [Tools für die Entwicklung](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f9-119">To learn where to get this certificate, see [Tools for Development](tools-for-development.md).</span></span> <span data-ttu-id="eb6f9-120">Zum Verarbeiten von ungeschütztem Inhalt können Sie ein dummyzertifikat verwenden, wie unter [Authentifizieren der Anwendung](authenticating-the-application.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="eb6f9-120">For handling unprotected content, you can use a dummy certificate as described in [Authenticating the Application](authenticating-the-application.md).</span></span>

<span data-ttu-id="eb6f9-121">Vor der Verwendung eines Geräts sollte Ihre Anwendung bestimmen, ob das Gerät Windows Media DRM 10 für tragbare Geräte unterstützt, und wenn ja, dass die DRM-Komponenten aktuell sind.</span><span class="sxs-lookup"><span data-stu-id="eb6f9-121">Before using a device, your application should determine whether the device supports Windows Media DRM 10 for Portable Devices, and if so, that the DRM components are current.</span></span> <span data-ttu-id="eb6f9-122">(Aktuell bedeutet das, dass die sichere Uhr korrekt ist und dass das Gerät ordnungsgemäß individualisiert wurde.) Wenn das Gerät diese DRM-Version nicht unterstützt, oder wenn es nicht aktualisiert werden kann, können Sie weiterhin Dateien an das Gerät senden, Sie können jedoch je nach Lizenz Version möglicherweise nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb6f9-122">(Current means that the secure clock is correct and that the device has been properly individualized.) If the device does not support this version of DRM, or if it cannot be updated, you can still send files to the device, but they might not be playable, depending on the license version.</span></span>

> [!Note]  
> <span data-ttu-id="eb6f9-123">Die individuelle Personalisierung von Geräten wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eb6f9-123">Individualization of devices is not currently supported.</span></span>

 

<span data-ttu-id="eb6f9-124">Wenn Ihre Anwendung mit den Windows Media-Format-SDK-Methoden verknüpft ist, muss Sie mit der Windows Media-Format Bibliothek wmstubdrm. lib verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="eb6f9-124">If your application will link to Windows Media Format SDK methods, it will need to link to the Windows Media Format library WMStubDRM.lib.</span></span> <span data-ttu-id="eb6f9-125">Weitere Informationen zum Aufrufen von Windows Media-Methoden auf DRM-geschützten Inhalten finden Sie unter "Aktivieren der DRM-Unterstützung" in der Dokumentation zum Windows Media-Format-SDK.</span><span class="sxs-lookup"><span data-stu-id="eb6f9-125">For more information on calling Windows Media Format methods on DRM-protected content, see "Enabling DRM Support" in the Windows Media Format SDK documentation.</span></span> <span data-ttu-id="eb6f9-126">Beachten Sie, dass ein Problem mit dem Verknüpfen mit mssachlp. lib und wmstubdrm. lib vorliegt.</span><span class="sxs-lookup"><span data-stu-id="eb6f9-126">Note that there is a problem with linking to both Mssachlp.lib and WMStubDRM.lib.</span></span> <span data-ttu-id="eb6f9-127">Dies wird im [KB-Artikel 890079 auf MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079)behandelt.</span><span class="sxs-lookup"><span data-stu-id="eb6f9-127">This is covered in [KB article 890079 on MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).</span></span>

<span data-ttu-id="eb6f9-128">Im folgenden C++-Codebeispiel wird festgelegt, ob ein Gerät ein Windows Media DRM 10-Gerät ist, und wenn dies der Fall ist, ist die Uhr auf dem neuesten Stand.</span><span class="sxs-lookup"><span data-stu-id="eb6f9-128">The following C++ code example determines whether a device is a Windows Media DRM 10 device and, if so, that its clock is up to date.</span></span>

`HRESULT IsDRMClockUpToDate()`


```C++
{
    HRESULT hr = S_OK;

    // Create the DRM handler class.
    CComPtr<IWMDRMDeviceApp> pDRM;
    hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

    // Find out first if the device is a WMDRM 10 device, and if so,
    // whether it requires clock updates.
    DWORD status = 0;
    hr = pDRM->QueryDeviceStatus(pDevice, &status);

    if (FAILED(hr)
       || (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. 
       || (status & WMDRM_DEVICE_REVOKED))   // Device is revoked.
    {
        return E_FAIL;
    }
    else if (status & WMDRM_DEVICE_NEEDCLOCK || 
        status & WMDRM_DEVICE_REFRESHCLOCK)
    {
        // Attempt update. See following example.
        hr = UpdateDRM(status);
    }
    return hr;
}
```



<span data-ttu-id="eb6f9-129">Wenn das Gerät Windows Media DRM 10 für tragbare Geräte unterstützt und aktualisiert werden muss (das heißt, wenn der Wert des *Status* im vorherigen Beispiel nicht einfach WMDM- \_ Gerät \_ iswmdrm ist), sollte die Anwendung [**iwmdrmdeviceapp:: acquiredevicedata**](iwmdrmdeviceapp-acquiredevicedata.md) aufrufen und den Wert von *Status* übergeben, um die erforderlichen Updates auszuführen.</span><span class="sxs-lookup"><span data-stu-id="eb6f9-129">If the device does support Windows Media DRM 10 for Portable Devices, and needs to be updated (that is, if the value of *status* in the previous example is not simply WMDM\_DEVICE\_ISWMDRM), the application should call [**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass in the value of *status* to perform the required updates.</span></span> <span data-ttu-id="eb6f9-130">Der Desktop Computer muss mit dem Internet verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="eb6f9-130">The desktop computer must be connected to the Internet.</span></span>

<span data-ttu-id="eb6f9-131">Die folgende C++-Beispiel Funktion versucht, ein DRM-Gerät zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="eb6f9-131">The following C++ example function attempts to update a DRM device.</span></span>


```C++
HRESULT UpdateDRM(DWORD status)
{
    HRESULT hr = S_OK;
    hr = pDRM->AcquireDeviceData(pDevice, this, status, &result);
    if (hr != S_OK || result != 0)
    {
            return E_FAIL;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="eb6f9-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eb6f9-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb6f9-133">**Erstellen einer Windows Media Device Manager-Anwendung**</span><span class="sxs-lookup"><span data-stu-id="eb6f9-133">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[<span data-ttu-id="eb6f9-134">**Behandeln geschützter Inhalte**</span><span class="sxs-lookup"><span data-stu-id="eb6f9-134">**Handling Protected Content**</span></span>](handling-protected-content.md)
</dt> </dl>

 

 