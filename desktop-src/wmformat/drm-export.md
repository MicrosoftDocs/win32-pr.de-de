---
title: DRM-Export
description: DRM-Export
ms.assetid: 0b44f2e5-e63c-4bdb-8123-097a5d5e3756
keywords:
- Windows Media-Format-SDK, erweiterte DRM-Client-APIs
- Windows Media-Format-SDK, erweiterte Client-APIs
- Windows Media-Format-SDK, erweiterte APIs
- SDK für Windows Media-Format, APIs
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Windows Media-Format-SDK, DRM-Export
- SDK für Windows Media-Format, exportieren
- Digital Rights Management (DRM), erweiterte Client-APIs
- DRM (Digital Rights Management), erweiterte Client-APIs
- Digital Rights Management (DRM), erweiterte APIs
- DRM (Digital Rights Management), erweiterte APIs
- Digital Rights Management (DRM), APIs
- DRM (Digital Rights Management), APIs
- Digital Rights Management (DRM), exportieren
- DRM (Digital Rights Management), exportieren
- Erweiterte APIs für den DRM-Client, exportieren
- Erweiterte Client-APIs, exportieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2917cfd0c9042f4547540618b44ed4c2f324edb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310172"
---
# <a name="drm-export"></a><span data-ttu-id="f932a-120">DRM-Export</span><span class="sxs-lookup"><span data-stu-id="f932a-120">DRM Export</span></span>

<span data-ttu-id="f932a-121">Die Exportfunktion von Windows Media DRM ermöglicht es Ihnen, lizenzierte Anwendungen zu erstellen, die von Windows Media DRM geschützte Inhalte entschlüsseln und in einem von dem zugeordneten Lizenz Aussteller explizit festgelegten Inhalts Schutzschema (CPS) erneut verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="f932a-121">Windows Media DRM export functionality enables you to create licensed applications that decrypt content protected by Windows Media DRM, and re-encrypt in an output content protection scheme (CPS) explicitly specified by the associated license issuer.</span></span> <span data-ttu-id="f932a-122">Der Lizenz Aussteller autorisiert den Export von Inhalten explizit zu einem bestimmten CPS über eine Inklusions Liste.</span><span class="sxs-lookup"><span data-stu-id="f932a-122">The license issuer explicitly authorizes the export of content to a specific CPS through an inclusion list.</span></span>

> [!Note]  
> <span data-ttu-id="f932a-123">Für den Zugriff auf die Exportfunktion müssen Sie ein [Export Anwendungs Zertifikat](export-application-certificate.md) von Microsoft beantragen.</span><span class="sxs-lookup"><span data-stu-id="f932a-123">To access export functionality, you must apply for an [Export Application Certificate](export-application-certificate.md) from Microsoft.</span></span>

 

<span data-ttu-id="f932a-124">Die Exportfunktion von Windows Media DRM wird in den folgenden Abschnitten erläutert.</span><span class="sxs-lookup"><span data-stu-id="f932a-124">Windows Media DRM export functionality is explained in the following sections.</span></span>



| <span data-ttu-id="f932a-125">`Section`</span><span class="sxs-lookup"><span data-stu-id="f932a-125">Section</span></span>                                                                                      | <span data-ttu-id="f932a-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f932a-126">Description</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f932a-127">Anwendungs Zertifikat exportieren</span><span class="sxs-lookup"><span data-stu-id="f932a-127">Export Application Certificate</span></span>](export-application-certificate.md)                         | <span data-ttu-id="f932a-128">Beschreibt ein Anwendungs Zertifikat exportieren.</span><span class="sxs-lookup"><span data-stu-id="f932a-128">Describes an export application certificate.</span></span>                                                        |
| [<span data-ttu-id="f932a-129">Explizite Autorisierungs-und Inklusions Listen</span><span class="sxs-lookup"><span data-stu-id="f932a-129">Explicit Authorization and Inclusion Lists</span></span>](explicit-authorization-and-inclusion-lists.md) | <span data-ttu-id="f932a-130">Erläutert den Prozess der expliziten Autorisierung und die Art und Weise, wie Einschlüsse Aufgaben auflisten.</span><span class="sxs-lookup"><span data-stu-id="f932a-130">Explains the process of explicit authorization, and how inclusions lists work.</span></span>                      |
| [<span data-ttu-id="f932a-131">Exportieren von komprimiertem Inhalt</span><span class="sxs-lookup"><span data-stu-id="f932a-131">Exporting Compressed Content</span></span>](exporting-compressed-content.md)                             | <span data-ttu-id="f932a-132">Hier wird beschrieben, wie Sie komprimierten Inhalt aus geschützten Audiodateien oder Videoinhalten von Windows Media DRM exportieren.</span><span class="sxs-lookup"><span data-stu-id="f932a-132">Describes how to export compressed content from Windows Media DRM protected audio or video content.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f932a-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f932a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f932a-134">**Explizite Autorisierungs-und Inklusions Listen**</span><span class="sxs-lookup"><span data-stu-id="f932a-134">**Explicit Authorization and Inclusion Lists**</span></span>](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[<span data-ttu-id="f932a-135">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="f932a-135">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




