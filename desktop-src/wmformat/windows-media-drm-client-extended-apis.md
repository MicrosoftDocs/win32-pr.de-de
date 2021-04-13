---
title: Erweiterte APIs für den Windows Media DRM-Client
description: Erweiterte APIs für den Windows Media DRM-Client
ms.assetid: c0397aa8-1f5a-48f5-a96b-555079e9a292
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
ms.openlocfilehash: 01c33ef3649f2cda63713ebd22a0116fdd025144
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390396"
---
# <a name="windows-media-drm-client-extended-apis"></a><span data-ttu-id="ab564-116">Erweiterte APIs für den Windows Media DRM-Client</span><span class="sxs-lookup"><span data-stu-id="ab564-116">Windows Media DRM Client Extended APIs</span></span>

<span data-ttu-id="ab564-117">\[Das Windows Media DRM-Feature ist veraltet und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab564-117">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="ab564-118">Verwenden Sie stattdessen [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="ab564-118">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="ab564-119">In dieser Dokumentation werden die erweiterten Anwendungs Programmierschnittstellen (Application Programming Interfaces, APIs) von Microsoft Windows Media Digital Rights Management (DRM) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ab564-119">This documentation describes the Microsoft Windows Media Digital Rights Management (DRM) Client Extended Application Programming Interfaces (APIs).</span></span> <span data-ttu-id="ab564-120">Die erweiterten APIs des Windows Media DRM-Clients enthalten Objekte, die zum Verwalten von Windows Media Digital Rights Management (DRM)-Vorgängen auf einem Client Computer verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ab564-120">The Windows Media DRM Client Extended APIs include objects that can be used to manage Windows Media Digital Rights Management (DRM) operations on a client computer.</span></span>

<span data-ttu-id="ab564-121">Der Hauptschwerpunkt dieser APIs ist die Verwaltung von Lizenzen für den Inhalt geschützter digitaler Medien.</span><span class="sxs-lookup"><span data-stu-id="ab564-121">The primary focus of these APIs is the management of licenses for protected digital media content.</span></span> <span data-ttu-id="ab564-122">Außerdem können die APIs zum Aktualisieren der DRM-Komponenten auf dem Client Computer und zum Erstellen von Anwendungen verwendet werden, die Inhalte mithilfe von Windows Media DRM für Netzwerkgeräte übertragen.</span><span class="sxs-lookup"><span data-stu-id="ab564-122">In addition, the APIs can be used to update the DRM components on the client computer and to create applications that transmit content using Windows Media DRM for Network Devices.</span></span>

<span data-ttu-id="ab564-123">Diese APIs bilden das Client seitige Pendant zum Windows Media Rights Manager SDK.</span><span class="sxs-lookup"><span data-stu-id="ab564-123">These APIs constitute the client-side counterpart to the Windows Media Rights Manager SDK.</span></span> <span data-ttu-id="ab564-124">Wenn mithilfe von Windows Media Rights Manager Onlinedienste erstellt wird, mit denen Dateien geschützt und Lizenzen ausgestellt werden, werden die erweiterten APIs des Windows Media DRM-Clients verwendet, um Anwendungen zu erstellen, die diese Inhalte nutzen.</span><span class="sxs-lookup"><span data-stu-id="ab564-124">Where Windows Media Rights Manager is used to create online services that protect files and issue licenses, the Windows Media DRM Client Extended APIs are used to create applications that consume that content.</span></span>

<span data-ttu-id="ab564-125">Dieses Dokument enthält die folgenden Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="ab564-125">This document includes the following sections.</span></span>



| <span data-ttu-id="ab564-126">`Section`</span><span class="sxs-lookup"><span data-stu-id="ab564-126">Section</span></span>                                                                                                  | <span data-ttu-id="ab564-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab564-127">Description</span></span>                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab564-128">Informationen zu den erweiterten APIs für den Windows Media DRM-Client</span><span class="sxs-lookup"><span data-stu-id="ab564-128">About the Windows Media DRM Client Extended APIs</span></span>](about-the-windows-media-drm-client-extended-apis.md) | <span data-ttu-id="ab564-129">Enthält eine Übersicht und Hintergrundinformationen, mit denen Sie vertraut sein sollten, bevor Sie Anwendungen entwickeln, die die-APIs verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab564-129">Provides overview and background information that you should be familiar with before developing applications that use the APIs.</span></span>                                                        |
| [<span data-ttu-id="ab564-130">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="ab564-130">Programming Guide</span></span>](drm-programming-guide.md)                                                           | <span data-ttu-id="ab564-131">Bietet ausführliche Anweisungen zum Ausführen verschiedener Client seitiger DRM-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="ab564-131">Provides detailed instructions for performing various client-side DRM operations.</span></span>                                                                                                      |
| [<span data-ttu-id="ab564-132">Programmierverzeichnis</span><span class="sxs-lookup"><span data-stu-id="ab564-132">Programming Reference</span></span>](drm-programming-reference.md)                                                   | <span data-ttu-id="ab564-133">Enthält Referenzinformationen zu den Schnittstellen, Methoden, Funktionen, Strukturen, Enumerationstypen und Konstanten, die in den erweiterten APIs des Windows Media DRM-Clients enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ab564-133">Provides reference information about the interfaces, methods, functions, structures, enumeration types, and constants that are included in the Windows Media DRM Client Extended APIs.</span></span> |



 

 

 