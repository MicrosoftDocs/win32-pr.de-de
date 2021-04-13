---
title: Erwerben von Lizenzen
description: Erwerben von Lizenzen
ms.assetid: dde33d57-6c63-4e1a-8398-5db466fb22fa
keywords:
- Windows Media-Format-SDK, erweiterte DRM-Client-APIs
- Windows Media-Format-SDK, erweiterte Client-APIs
- Windows Media-Format-SDK, erweiterte APIs
- SDK für Windows Media-Format, APIs
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Windows Media-Format-SDK, erwerben von Lizenzen
- Windows Media-Format-SDK, Lizenzen
- Digital Rights Management (DRM), erweiterte Client-APIs
- DRM (Digital Rights Management), erweiterte Client-APIs
- Digital Rights Management (DRM), erweiterte APIs
- DRM (Digital Rights Management), erweiterte APIs
- Digital Rights Management (DRM), APIs
- DRM (Digital Rights Management), APIs
- Digital Rights Management (DRM), erwerben von Lizenzen
- DRM (Digital Rights Management), erwerben von Lizenzen
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Erweiterte APIs für den DRM-Client, erwerben von Lizenzen
- Erweiterte Client-APIs, Erwerb von Lizenzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c024789823ca0cd1b38959d78535ce71e2514897
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387998"
---
# <a name="acquiring-licenses"></a><span data-ttu-id="02381-122">Erwerben von Lizenzen</span><span class="sxs-lookup"><span data-stu-id="02381-122">Acquiring Licenses</span></span>

<span data-ttu-id="02381-123">Ein häufiges Szenario für den Erwerb von Lizenzen ist, wenn ein Benutzer über eine geschützte Windows Media-Datei verfügt und versucht, zum ersten Mal auf den Inhalt zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="02381-123">A common scenario for acquiring licenses is when a user has a protected Windows Media file and tries to access the content for the first time.</span></span> <span data-ttu-id="02381-124">Da die erweiterten APIs des Windows Media DRM-Clients von der Datei Behandlungs Routinen von ASF getrennt sind, erfordert das grundlegende Lizenz Erwerbs Szenario, unterstützt, mehr API-Aufrufe als das Windows Media-Format-SDK und das Media Foundation SDK.</span><span class="sxs-lookup"><span data-stu-id="02381-124">Because the Windows Media DRM Client Extended APIs are separate from ASF file handling routines, the basic license acquisition scenario, while supported, requires more API calls than using the Windows Media Format SDK and the Media Foundation SDK.</span></span>

<span data-ttu-id="02381-125">In diesem Abschnitt wird beschrieben, wie Sie die erweiterten APIs des Windows Media DRM-Clients zum Abrufen von Lizenzen verwenden, die im lokalen Lizenz Speicher auf einem Client Computer gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="02381-125">This section describes how to use the Windows Media DRM Client Extended APIs to acquire licenses that are stored in the local license store on a client computer.</span></span> <span data-ttu-id="02381-126">Es enthält die folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="02381-126">It contains the following topics.</span></span>



| <span data-ttu-id="02381-127">Thema</span><span class="sxs-lookup"><span data-stu-id="02381-127">Topic</span></span>                                                                | <span data-ttu-id="02381-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02381-128">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02381-129">Automatische Lizenz Beschaffung</span><span class="sxs-lookup"><span data-stu-id="02381-129">Silent License Acquisition</span></span>](silent-license-acquisition.md)         | <span data-ttu-id="02381-130">Hier wird beschrieben, wie Sie Lizenzen ohne Benutzereingriff erwerben.</span><span class="sxs-lookup"><span data-stu-id="02381-130">Describes how to acquire licenses without user intervention.</span></span>                                                                               |
| [<span data-ttu-id="02381-131">Nicht automatische Lizenz Beschaffung</span><span class="sxs-lookup"><span data-stu-id="02381-131">Non-Silent License Acquisition</span></span>](non-silent-license-acquisition.md) | <span data-ttu-id="02381-132">Hier wird beschrieben, wie Sie Lizenzen erwerben, wenn ein Benutzereingriff erforderlich ist (z. b. das bezahlen für den Inhalt).</span><span class="sxs-lookup"><span data-stu-id="02381-132">Describes how to acquire licenses when user intervention (such as paying for the content) is required.</span></span>                                     |
| [<span data-ttu-id="02381-133">Vorab Bereitstellung von Lizenzen</span><span class="sxs-lookup"><span data-stu-id="02381-133">License Pre-Delivery</span></span>](license-pre-delivery.md)                     | <span data-ttu-id="02381-134">Beschreibt das Abrufen von Lizenzen von einem Lizenzserver an einen Client Computer.</span><span class="sxs-lookup"><span data-stu-id="02381-134">Describes how to pull licenses from a license server to a client computer.</span></span>                                                                 |
| [<span data-ttu-id="02381-135">Lokales Erstellen von Lizenzen</span><span class="sxs-lookup"><span data-stu-id="02381-135">Creating Licenses Locally</span></span>](creating-licenses-locally.md)           | <span data-ttu-id="02381-136">Hier wird beschrieben, wie Sie Ihre eigenen Lizenzen erstellen, ohne Sie von einem Lizenzserver herunterzuladen und im lokalen Lizenz Speicher zu speichern.</span><span class="sxs-lookup"><span data-stu-id="02381-136">Describes how to create your own licenses without downloading them from a license server and how to store them in the local license store.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="02381-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="02381-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02381-138">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="02381-138">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




