---
title: Microsoft Windows Media DRM-Client Programmier Handbuch
description: Microsoft Windows Media DRM-Client Programmier Handbuch
ms.assetid: e7b179b3-ed14-4ea0-9a00-9d96557a2e2e
keywords:
- Windows Media-Format-SDK, erweiterte DRM-Client-APIs
- Windows Media-Format-SDK, erweiterte Client-APIs
- Windows Media-Format-SDK, erweiterte APIs
- SDK für Windows Media-Format, APIs
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Windows Media-Format-SDK, Programmier Handbuch
- Digital Rights Management (DRM), erweiterte Client-APIs
- DRM (Digital Rights Management), erweiterte Client-APIs
- Digital Rights Management (DRM), erweiterte APIs
- DRM (Digital Rights Management), erweiterte APIs
- Digital Rights Management (DRM), APIs
- DRM (Digital Rights Management), APIs
- Digital Rights Management (DRM), Programmier Handbuch
- DRM (Digital Rights Management), Programmier Handbuch
- Erweiterte APIs für den DRM-Client, Informationen zu
- Erweiterte Client-APIs, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b338ea6ebd9cb132c8e6b1c76c8e1d7f6c6aa182
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474886"
---
# <a name="microsoft-windows-media-drm-client-programming-guide"></a><span data-ttu-id="ed931-119">Microsoft Windows Media DRM-Client Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="ed931-119">Microsoft Windows Media DRM Client Programming Guide</span></span>

<span data-ttu-id="ed931-120">Dieses Handbuch enthält Informationen zur Verwendung der Features der erweiterten APIs des Windows Media DRM-Clients in Ihren Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="ed931-120">This guide provides information about using the features of the Windows Media DRM Client Extended APIs in your applications.</span></span> <span data-ttu-id="ed931-121">In den folgenden Abschnitten werden die Schritte zum Implementieren von DRM-Features ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="ed931-121">The following sections explain, in detail, the steps involved in implementing DRM features.</span></span>



| <span data-ttu-id="ed931-122">`Section`</span><span class="sxs-lookup"><span data-stu-id="ed931-122">Section</span></span>                                                                                                                          | <span data-ttu-id="ed931-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed931-123">Description</span></span>                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed931-124">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="ed931-124">Getting Started</span></span>](drm-getting-started.md)                                                                                       | <span data-ttu-id="ed931-125">Enthält Informationen zum Einrichten von C++-Projekten, die erweiterte APIs für den Windows Media DRM-Client verwenden.</span><span class="sxs-lookup"><span data-stu-id="ed931-125">Provides information about setting up C++ projects that use the Windows Media DRM Client Extended APIs.</span></span>    |
| [<span data-ttu-id="ed931-126">Erwerben von Lizenzen</span><span class="sxs-lookup"><span data-stu-id="ed931-126">Acquiring Licenses</span></span>](acquiring-licenses.md)                                                                                     | <span data-ttu-id="ed931-127">Hier wird beschrieben, wie Sie Lizenzen auf dem Client Computer erhalten.</span><span class="sxs-lookup"><span data-stu-id="ed931-127">Describes how to get licenses on the client computer.</span></span>                                                      |
| [<span data-ttu-id="ed931-128">Informationen aus Lizenzen im lokalen Lizenz Speicher erhalten</span><span class="sxs-lookup"><span data-stu-id="ed931-128">Getting Information from Licenses in the Local License Store</span></span>](getting-information-from-licenses-in-the-local-license-store.md) | <span data-ttu-id="ed931-129">Hier wird beschrieben, wie Sie Informationen zu Rechten für geschützte Inhalte erhalten.</span><span class="sxs-lookup"><span data-stu-id="ed931-129">Describes how to get information about rights for protected content.</span></span>                                       |
| [<span data-ttu-id="ed931-130">Durchführen der DRM-Individualisierung</span><span class="sxs-lookup"><span data-stu-id="ed931-130">Performing DRM Individualization</span></span>](performing-drm-individualization.md)                                                         | <span data-ttu-id="ed931-131">Hier wird beschrieben, wie Sie die DRM-Komponente auf dem Client Computer aktualisieren und individualisieren, um Sie sicherer zu machen.</span><span class="sxs-lookup"><span data-stu-id="ed931-131">Describes how to update and individualize the DRM component on the client computer to make it more secure.</span></span> |
| [<span data-ttu-id="ed931-132">DRM-Export</span><span class="sxs-lookup"><span data-stu-id="ed931-132">DRM Export</span></span>](drm-export.md)                                                                                                     | <span data-ttu-id="ed931-133">Hier wird beschrieben, wie von Windows Media DRM geschützte Inhalte exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="ed931-133">Describes how to export content protected by Windows Media DRM.</span></span>                                            |
| [<span data-ttu-id="ed931-134">DRM-Import</span><span class="sxs-lookup"><span data-stu-id="ed931-134">DRM Import</span></span>](drm-import.md)                                                                                                     | <span data-ttu-id="ed931-135">Hier wird beschrieben, wie von Windows Media DRM geschützte Inhalte importiert werden.</span><span class="sxs-lookup"><span data-stu-id="ed931-135">Describes how to import content protected by Windows Media DRM.</span></span>                                            |
| [<span data-ttu-id="ed931-136">Lizenz Sperrung</span><span class="sxs-lookup"><span data-stu-id="ed931-136">License Revocation</span></span>](drm-license-revocation.md)                                                                                 | <span data-ttu-id="ed931-137">Hier wird beschrieben, wie Lizenzen aus dem lokalen Lizenz Speicher entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="ed931-137">Describes how to remove licenses from the local license store.</span></span>                                             |
| [<span data-ttu-id="ed931-138">Automatisierte Sperrung und Erneuerung von Komponenten</span><span class="sxs-lookup"><span data-stu-id="ed931-138">Automated Component Revocation and Renewal</span></span>](automated-component-revocation-and-renewal.md)                                     | <span data-ttu-id="ed931-139">Beschreibt das automatisierte Windows Media DRM-Sperr-und Erneuerungssystem mithilfe von Inhalts Enablern.</span><span class="sxs-lookup"><span data-stu-id="ed931-139">Describes the Windows Media DRM automated revocation and renewal system using content enablers.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="ed931-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ed931-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed931-141">**Erweiterte APIs für den Windows Media DRM-Client**</span><span class="sxs-lookup"><span data-stu-id="ed931-141">**Windows Media DRM Client Extended APIs**</span></span>](windows-media-drm-client-extended-apis.md)
</dt> <dt>

<span data-ttu-id="ed931-142">[Windows Media Rights Manager SDK](/previous-versions/ms986509(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="ed931-142">[Windows Media Rights Manager SDK](/previous-versions/ms986509(v=msdn.10))</span></span>
</dt> </dl>

 

 
