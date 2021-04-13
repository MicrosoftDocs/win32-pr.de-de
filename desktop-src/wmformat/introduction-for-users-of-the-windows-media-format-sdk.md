---
title: Einführung für Benutzer des SDK für den Windows Media-Format
description: Einführung für Benutzer des SDK für den Windows Media-Format
ms.assetid: 21f06c43-213e-4fbf-a33a-c1890b4b40ce
keywords:
- Windows Media-Format-SDK, erweiterte DRM-Client-APIs
- Windows Media-Format-SDK, erweiterte Client-APIs
- Windows Media-Format-SDK, erweiterte APIs
- SDK für Windows Media-Format, APIs
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Digital Rights Management (DRM), erweiterte Client-APIs
- DRM (Digital Rights Management), erweiterte Client-APIs
- Digital Rights Management (DRM), erweiterte APIs
- DRM (Digital Rights Management), erweiterte APIs
- Digital Rights Management (DRM), APIs
- DRM (Digital Rights Management), APIs
- Erweiterte APIs für den DRM-Client, Informationen zu
- Erweiterte Client-APIs, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538978305e4df952ed97e063b3512ce9fd5cfc34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388354"
---
# <a name="introduction-for-users-of-the-windows-media-format-sdk"></a><span data-ttu-id="24591-116">Einführung für Benutzer des SDK für den Windows Media-Format</span><span class="sxs-lookup"><span data-stu-id="24591-116">Introduction for Users of the Windows Media Format SDK</span></span>

<span data-ttu-id="24591-117">Ein Großteil der Funktionen, die von den erweiterten APIs des Windows Media DRM-Clients bereitgestellt werden, ist identisch mit der Funktionalität, die von den Objekten des Windows Media Format SDK bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="24591-117">Much of the functionality provided by the Windows Media DRM Client Extended APIs is the same as the functionality provided by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="24591-118">Das Windows Media-Format-SDK stellt Entwicklern die Objekte zur Verfügung, die zum Erstellen, zugreifen auf und Bearbeiten von Mediendateien benötigt werden, die die Dateistruktur von Advanced Systems Format (ASF) verwenden.</span><span class="sxs-lookup"><span data-stu-id="24591-118">The Windows Media Format SDK provides developers with the objects needed to create, access, and manipulate media files that use the Advanced Systems Format (ASF) file structure.</span></span> <span data-ttu-id="24591-119">Da Windows Media DRM zum Schutz von ASF-Dateien vorgesehen ist, waren Client seitige DRM-Funktionen im Windows Media-Format-SDK enthalten.</span><span class="sxs-lookup"><span data-stu-id="24591-119">Because Windows Media DRM is intended to protect ASF files, client-side DRM functionality was included in the Windows Media Format SDK.</span></span>

<span data-ttu-id="24591-120">Die erweiterten APIs des Windows Media DRM-Clients werden in Verbindung mit der Microsoft-Plattform der nächsten Generation (Digital Media), dem Microsoft Media Foundation SDK, veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="24591-120">The Windows Media DRM Client Extended APIs are being released in conjunction with Microsoft's next-generation digital media platform, the Microsoft Media Foundation SDK.</span></span> <span data-ttu-id="24591-121">In Media Foundation werden die Funktionen von ASF enthalten sein, die einige der Features des Windows Media SDK überlappen.</span><span class="sxs-lookup"><span data-stu-id="24591-121">Media Foundation will include ASF functionality that overlaps some of the features of the Windows Media Format SDK.</span></span> <span data-ttu-id="24591-122">Da jetzt zwei Microsoft SDKs zur Bearbeitung von ASF-Dateien vorhanden sind, wird die Client seitige DRM-Funktionalität vom Windows Media-Format-SDK in die erweiterten APIs des Windows Media DRM-Clients aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="24591-122">Because there are now two Microsoft SDKs that manipulate ASF files, the client-side DRM functionality is being separated from the Windows Media Format SDK into the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="24591-123">Auf diese APIs kann von Benutzern des Windows Media-Format-SDK und des Media Foundation SDK zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="24591-123">These APIs can be accessed by users of both the Windows Media Format SDK and the Media Foundation SDK.</span></span> <span data-ttu-id="24591-124">Derzeit sind diese APIs als Teil des Windows Media Format SDK-Installationspakets enthalten und werden als Teil des SDK für den Windows Media-Format dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="24591-124">At present, these APIs are included as part of the Windows Media Format SDK installation package and are documented as part of the Windows Media Format SDK.</span></span> <span data-ttu-id="24591-125">Die erweiterten APIs des Windows Media DRM-Clients werden jedoch in ihrer eigenen Bibliothek implementiert und verfügen über eine eigene Header Datei.</span><span class="sxs-lookup"><span data-stu-id="24591-125">However, the Windows Media DRM Client Extended APIs are implemented in their own library and have their own header file.</span></span> <span data-ttu-id="24591-126">Nach der Installation des Windows Media Format SDK können diese APIs einzeln verwendet werden, ohne dass Windows Media Format SDK-Header oder-Bibliotheken in Ihre Anwendung eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="24591-126">After installing the Windows Media Format SDK, these APIs can be used one their own, without including any Windows Media Format SDK headers or libraries in your application.</span></span>

<span data-ttu-id="24591-127">Wenn Sie Anwendungen entwickeln, die das SDK für den Windows Media-Format verwenden, müssen Sie entscheiden, ob die von SDK bereitgestellte DRM-Funktionalität verwendet oder die erweiterten APIs des Windows Media DRM-Clients verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="24591-127">If you develop applications that use the Windows Media Format SDK you must decide whether to use the DRM functionality that SDK provides, or to use the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="24591-128">Obwohl viele der Features dieser beiden sdker sehr ähnlich sind, bieten die erweiterten APIs für den Windows Media DRM-Client die folgenden Features, die für Benutzer der älteren DRM-Routinen nicht verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="24591-128">While many of the features of these two SDKs are very similar, the Windows Media DRM Client Extended APIs offer the following features not available to users of the older DRM routines:</span></span>

-   <span data-ttu-id="24591-129">Möglichkeit zum Importieren von Inhalten, die von einem Drittanbieter-Rechte Verwaltungssystem geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="24591-129">Ability to import content protected by a third-party rights management system.</span></span>
-   <span data-ttu-id="24591-130">Möglichkeit zum Exportieren von Inhalten, die von Windows Media DRM geschützt sind, in ein Rights Management-System von Drittanbietern.</span><span class="sxs-lookup"><span data-stu-id="24591-130">Ability to export content protected by Windows Media DRM to a third-party rights management system.</span></span>
-   <span data-ttu-id="24591-131">Direkte Enumeration von Lizenzen im Lizenz Speicher.</span><span class="sxs-lookup"><span data-stu-id="24591-131">Direct enumeration of licenses in the license store.</span></span>
-   <span data-ttu-id="24591-132">Einfache, aggregierte Rechte Abfragen basierend auf der Schlüssel-ID (es ist nicht erforderlich, die Mediendatei zu laden).</span><span class="sxs-lookup"><span data-stu-id="24591-132">Simple, aggregated rights querying based on key ID (no need to load the media file).</span></span>
-   <span data-ttu-id="24591-133">Möglichkeit zum Erneuern von widerrufenen Komponenten mithilfe der Standard Media Foundation-Schnittstelle **imfcontentenabler**.</span><span class="sxs-lookup"><span data-stu-id="24591-133">Ability to renew revoked components by using the standard Media Foundation interface, **IMFContentEnabler**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24591-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="24591-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24591-135">**Informationen zu den erweiterten APIs für den Windows Media DRM-Client**</span><span class="sxs-lookup"><span data-stu-id="24591-135">**About the Windows Media DRM Client Extended APIs**</span></span>](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




