---
title: Durchführen der DRM-Individualisierung
description: Durchführen der DRM-Individualisierung
ms.assetid: daad1a31-f0a7-43ab-b920-94b9f050a44e
keywords:
- Windows Media-Format-SDK, erweiterte DRM-Client-APIs
- Windows Media-Format-SDK, erweiterte Client-APIs
- Windows Media-Format-SDK, erweiterte APIs
- SDK für Windows Media-Format, APIs
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Windows Media-Format-SDK, DRM-Individualisierung
- Windows Media-Format-SDK, Individualisierung
- Digital Rights Management (DRM), erweiterte Client-APIs
- DRM (Digital Rights Management), erweiterte Client-APIs
- Digital Rights Management (DRM), erweiterte APIs
- DRM (Digital Rights Management), erweiterte APIs
- Digital Rights Management (DRM), APIs
- DRM (Digital Rights Management), APIs
- Digital Rights Management (DRM), Individualisierung
- DRM (Digital Rights Management), Individualisierung
- Digital Rights Management (DRM), DRM-Individualisierung
- DRM (Digital Rights Management), DRM-Individualisierung
- Erweiterte APIs für den DRM-Client, Individualisierung
- Erweiterte Client-APIs, Individualisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d8f7f04add4ed626985651d5220e69ea713e4d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310896"
---
# <a name="performing-drm-individualization"></a><span data-ttu-id="7923d-122">Durchführen der DRM-Individualisierung</span><span class="sxs-lookup"><span data-stu-id="7923d-122">Performing DRM Individualization</span></span>

<span data-ttu-id="7923d-123">Die Individualisierung ist der Prozess, bei dem die DRM-Komponente auf dem Client Computer aktualisiert, verschlüsselt und eindeutig gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="7923d-123">Individualization is the process of updating the DRM component on the client computer, encrypting it, and making it unique.</span></span> <span data-ttu-id="7923d-124">Wenn ein Computer individuell ist, ist die DRM-Komponente an den Computer gebunden und kann keinen Inhalt auf einem anderen Computer decodieren.</span><span class="sxs-lookup"><span data-stu-id="7923d-124">When a computer is individualized, the DRM component is tied to the computer and will not be able to decode content on any other computer.</span></span> <span data-ttu-id="7923d-125">Die erweiterten APIs des Windows Media DRM-Clients bieten Unterstützung für die individuelle Bereitstellung der DRM-Komponente auf Client Computern.</span><span class="sxs-lookup"><span data-stu-id="7923d-125">The Windows Media DRM Client Extended APIs provide support for individualizing the DRM component on client computers.</span></span>

<span data-ttu-id="7923d-126">Die Individualisierung wird durch Aufrufen der Methode [**iwmdrmsecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="7923d-126">Individualization is performed by calling the [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method.</span></span> <span data-ttu-id="7923d-127">Sie können " **performsecurityupdate** " so aufzurufen, dass es nur dann individualisiert wird, wenn die Version auf dem Server neuer ist als die auf dem Client Computer installierte Version, oder Sie können die individuelle Personalisierung ohne Berücksichtigung der relativen Sicherheits Versionen erzwingen.</span><span class="sxs-lookup"><span data-stu-id="7923d-127">You can call **PerformSecurityUpdate** so that it will individualize only if the version on the server is newer than the one installed on the client computer, or you can force individualization without regard to the relative security versions.</span></span> <span data-ttu-id="7923d-128">Das Flag für die Bedarfs gesteuerte Individualisierung ist WMDRM \_ Security \_ Durchführen von \_ indiv.</span><span class="sxs-lookup"><span data-stu-id="7923d-128">The flag for as-needed individualization is WMDRM\_SECURITY\_PERFORM\_INDIV.</span></span> <span data-ttu-id="7923d-129">Das Flag für die erzwungene Individual alisierung ist WMDRM \_ Security do \_ \_ Force \_ indiv.</span><span class="sxs-lookup"><span data-stu-id="7923d-129">The flag for forced individualization is WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV.</span></span>

<span data-ttu-id="7923d-130">**Performsecurityupdate** ist ein asynchroner-Befehl.</span><span class="sxs-lookup"><span data-stu-id="7923d-130">**PerformSecurityUpdate** is an asynchronous call.</span></span> <span data-ttu-id="7923d-131">Sie wird schnell zurückgegeben und generiert dann Ereignisse, um Statusinformationen zum Individualisierungsprozess bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7923d-131">It will return quickly and then generate events to provide status information about the individualization process.</span></span> <span data-ttu-id="7923d-132">Die Mehrzahl der generierten Ereignisse sind **mewmdrmindividualizationprogress** -Ereignisse, und jede verfügt über eine zugehörige [**iwmdrmindividualizationstatus**](iwmdrmindividualizationstatus.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7923d-132">The majority of the events generated will be **MEWMDRMIndividualizationProgress** events, and each has an associated [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interface.</span></span> <span data-ttu-id="7923d-133">Zum Abrufen der Status Schnittstelle müssen Sie **imfmediaevent:: GetValue** aufrufen, um einen **IUnknown** -Zeiger abzurufen, der sich auf dem gleichen Objekt befindet, und ihn dann für **iwmdrmindividualizationstatus** Abfragen.</span><span class="sxs-lookup"><span data-stu-id="7923d-133">To get the status interface, you must call **IMFMediaEvent::GetValue** to retrieve an **IUnknown** pointer that is on the same object and then query it for **IWMDRMIndividualizationStatus**.</span></span>

<span data-ttu-id="7923d-134">Sie können Daten für eine [**WM \_ Individual- \_ Status**](drmwm-individualize-status.md) Struktur abrufen, indem Sie [**iwmdrmindividualizestatus:: GetStatus**](iwmdrmindividualizationstatus-getstatus.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7923d-134">You can get data for a [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure by calling [**IWMDRMIndividualizeStatus::GetStatus**](iwmdrmindividualizationstatus-getstatus.md).</span></span> <span data-ttu-id="7923d-135">Jedes Ereignis, das generiert wird, verfügt über ein eigenes Objekt mit dem Status. Sie müssen daher jedes Mal den Ereignis Wert abrufen und die Status Schnittstelle Abfragen.</span><span class="sxs-lookup"><span data-stu-id="7923d-135">Each event that is generated has its own object with status, so you must go through the process of getting the event value and querying for the status interface every time.</span></span>

<span data-ttu-id="7923d-136">Abhängig von der Größe des Downloads können Dutzende oder Hunderte von **mewmdrmindividualizationprogress** -Ereignissen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="7923d-136">Depending on the size of the download, there may be dozens or hundreds of **MEWMDRMIndividualizationProgress** events.</span></span> <span data-ttu-id="7923d-137">Wenn der Individualisierungsprozess abgeschlossen ist, wird ein **mewmdrmindividualizationabgeschlossene** -Ereignis generiert.</span><span class="sxs-lookup"><span data-stu-id="7923d-137">When the individualization process is finished, an **MEWMDRMIndividualizationCompleted** event is generated.</span></span>

<span data-ttu-id="7923d-138">Wenn die Individualisierung abgeschlossen ist, sind die einzigen Objekte, die den neuen, individualisierten Zustand widerspiegeln, diejenigen, die von [**iwmdrmsecurity**](iwmdrmsecurity.md)erben.</span><span class="sxs-lookup"><span data-stu-id="7923d-138">When individualization is completed, the only existing objects that will reflect the new individualized state are those that inherit from [**IWMDRMSecurity**](iwmdrmsecurity.md).</span></span> <span data-ttu-id="7923d-139">Alle anderen vorhandenen Objekte werden nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7923d-139">All other existing objects will not be updated.</span></span> <span data-ttu-id="7923d-140">Sie müssen alle anderen Objekte freigeben und neu erstellen, damit Sie den neuen, individualisierten Zustand widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="7923d-140">You must release and re-create any other objects so that they will reflect the new individualized state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7923d-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7923d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7923d-142">**Beispiel für DRM-Individualisierung**</span><span class="sxs-lookup"><span data-stu-id="7923d-142">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="7923d-143">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="7923d-143">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="7923d-144">**Verwenden des Media Foundation-Ereignis Modells**</span><span class="sxs-lookup"><span data-stu-id="7923d-144">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> <dt>

<span data-ttu-id="7923d-145">[Bewährte Methoden für die Windows Media DRM-Individualisierung](/previous-versions/ms867216(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7923d-145">[Windows Media DRM Individualization Best Practices](/previous-versions/ms867216(v=msdn.10))</span></span>
</dt> </dl>

 

 




