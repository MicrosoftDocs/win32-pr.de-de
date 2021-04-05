---
title: DRM-Import
description: DRM-Import
ms.assetid: 5e67a721-830b-4d99-9f90-4cb2d7c61104
keywords:
- Windows Media-Format-SDK, erweiterte DRM-Client-APIs
- Windows Media-Format-SDK, erweiterte Client-APIs
- Windows Media-Format-SDK, erweiterte APIs
- SDK für Windows Media-Format, APIs
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Windows Media-Format-SDK, DRM-Import
- SDK für Windows Media-Format, importieren
- Windows Media-Format-SDK, Content Protection System (CPS)
- Digital Rights Management (DRM), erweiterte Client-APIs
- DRM (Digital Rights Management), erweiterte Client-APIs
- Digital Rights Management (DRM), erweiterte APIs
- DRM (Digital Rights Management), erweiterte APIs
- Digital Rights Management (DRM), APIs
- DRM (Digital Rights Management), APIs
- Digital Rights Management (DRM), importieren
- DRM (Digital Rights Management), importieren
- Digital Rights Management (DRM), Content Protection System (CPS)
- DRM (Digital Rights Management), Content Protection System (CPS)
- Erweiterte APIs für den DRM-Client, Import
- Erweiterte Client-APIs, importieren
- Erweiterte APIs für den DRM-Client, Content Protection System (CPS)
- Erweiterte Client-APIs, Content Protection System (CPS)
- Content Protection System (CPS)
- CPS (Content Protection System)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fc20cfd682df975c10a8f39785c0e8d69610d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711129"
---
# <a name="drm-import"></a><span data-ttu-id="26f7d-127">DRM-Import</span><span class="sxs-lookup"><span data-stu-id="26f7d-127">DRM Import</span></span>

<span data-ttu-id="26f7d-128">In den folgenden Abschnitten wird erläutert, wie Medieninhalte von einem Drittanbieter-CPS (Content Protection System) in Windows Media DRM konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="26f7d-128">The following sections explain how to convert media content from a third-party content protection system (CPS) to Windows Media DRM.</span></span> <span data-ttu-id="26f7d-129">Dieser Prozess wird als DRM-Import bezeichnet und besteht im Wesentlichen aus den folgenden Schritten:</span><span class="sxs-lookup"><span data-stu-id="26f7d-129">This process is known as DRM Import and consists essentially of the following steps:</span></span>

1.  <span data-ttu-id="26f7d-130">Die ASF-Datei wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="26f7d-130">Creating the ASF file.</span></span>
2.  <span data-ttu-id="26f7d-131">Die Lizenz wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="26f7d-131">Creating the license.</span></span>
3.  <span data-ttu-id="26f7d-132">Optional können Sie die Lizenz löschen.</span><span class="sxs-lookup"><span data-stu-id="26f7d-132">Optionally deleting the license.</span></span>

<span data-ttu-id="26f7d-133">Der DRM-Import wird in den folgenden Abschnitten erläutert.</span><span class="sxs-lookup"><span data-stu-id="26f7d-133">DRM Import is explained in the following sections.</span></span>



| <span data-ttu-id="26f7d-134">`Section`</span><span class="sxs-lookup"><span data-stu-id="26f7d-134">Section</span></span>                                                                              | <span data-ttu-id="26f7d-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26f7d-135">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="26f7d-136">Importieren von Lizenz-und Schlüssel Material</span><span class="sxs-lookup"><span data-stu-id="26f7d-136">Importing License and Key Material</span></span>](importing-license-and-key-material.md)         | <span data-ttu-id="26f7d-137">Hier wird beschrieben, wie Lizenzen lokal ausgestellt und in Windows Media DRM importiert werden.</span><span class="sxs-lookup"><span data-stu-id="26f7d-137">Describes how to issue licenses locally and import them into Windows Media DRM.</span></span>      |
| [<span data-ttu-id="26f7d-138">Zertifikat Sperrung wird überprüft</span><span class="sxs-lookup"><span data-stu-id="26f7d-138">Checking Certificate Revocation</span></span>](checking-certificate-revocation.md)               | <span data-ttu-id="26f7d-139">Hier wird beschrieben, wie Sie die Zertifikat Sperrung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="26f7d-139">Describes how to check certificate revocation.</span></span>                                       |
| [<span data-ttu-id="26f7d-140">Aufbauen einer XMR-Lizenz</span><span class="sxs-lookup"><span data-stu-id="26f7d-140">Building an XMR License</span></span>](building-an-xmr-license.md)                               | <span data-ttu-id="26f7d-141">Beschreibt, wie eine XMR-Lizenz erstellt und an das DRM-Subsystem übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="26f7d-141">Describes how to create an XMR license and pass it to the DRM subsystem.</span></span>             |
| [<span data-ttu-id="26f7d-142">Erstellen und Initialisieren eines DRM-Writers</span><span class="sxs-lookup"><span data-stu-id="26f7d-142">Creating and Initializing a DRM Writer</span></span>](creating-and-initializing-a-drm-writer.md) | <span data-ttu-id="26f7d-143">Beschreibt, wie ein ASF-Writer-Objekt für die Vorbereitung des DRM-Imports initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="26f7d-143">Describes how to initialize an ASF writer object to prepare for DRM Import.</span></span>          |
| [<span data-ttu-id="26f7d-144">Verschlüsseln und Importieren von Medien Beispielen</span><span class="sxs-lookup"><span data-stu-id="26f7d-144">Encrypting and Importing Media Samples</span></span>](encrypting-and-importing-media-samples.md) | <span data-ttu-id="26f7d-145">Hier wird beschrieben, wie einzelne Medien Beispiele in Windows Media DRM verschlüsselt und importiert werden.</span><span class="sxs-lookup"><span data-stu-id="26f7d-145">Describes how to encrypt and import individual media samples into Windows Media DRM.</span></span> |
| [<span data-ttu-id="26f7d-146">Löschen von Lizenzen</span><span class="sxs-lookup"><span data-stu-id="26f7d-146">License Deletion</span></span>](license-deletion.md)                                             | <span data-ttu-id="26f7d-147">Hier wird beschrieben, wie lokal erstellte Lizenzen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="26f7d-147">Describes how to delete locally created licenses.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="26f7d-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26f7d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26f7d-149">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="26f7d-149">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




