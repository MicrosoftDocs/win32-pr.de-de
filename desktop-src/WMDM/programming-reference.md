---
title: WMDM-Referenz
description: Programmierverzeichnis
ms.assetid: 1d2260a8-bc9f-41b3-a3b0-0176b45fff1f
keywords:
- Windows Media-Device Manager, Programmier Referenz
- Device Manager, Programmier Referenz
- Windows Media Device Manager, Desktop Anwendungen
- Device Manager, Desktop Anwendungen
- Windows Media Device Manager, Dienstanbieter
- Device Manager, Dienstanbieter
- Desktop Anwendungen, Programmier Referenz
- Dienstanbieter, Programmier Referenz
- Programmier Referenz, Desktop Anwendungen
- Programmier Referenz, Dienstanbieter
- Programmier Referenz, Windows Media-Device Manager
- Referenz für Windows Media Device Manager, Informationen zu
- Referenz für Windows Media Device Manager, Desktop Anwendungen
- Referenz für Windows Media Device Manager, Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1498d42e65de99abc1d32895f3628d93502c70f
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104389626"
---
# <a name="wmdm-reference"></a><span data-ttu-id="a015b-117">WMDM-Referenz</span><span class="sxs-lookup"><span data-stu-id="a015b-117">WMDM reference</span></span>

<span data-ttu-id="a015b-118">Das Windows Media Device Manager SDK besteht aus einer Auflistung von Schnittstellen, Strukturen, Enumerationen und Konstanten.</span><span class="sxs-lookup"><span data-stu-id="a015b-118">The Windows Media Device Manager SDK consists of a collection of interfaces, structures, enumerations, and constants.</span></span> <span data-ttu-id="a015b-119">Im Referenz Abschnitt werden die Schnittstellen gemäß dem Objekttyp, der Sie verwendet, in Gruppen aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="a015b-119">The reference section divides the interfaces into groups according to the type of object that uses them.</span></span>



| <span data-ttu-id="a015b-120">`Section`</span><span class="sxs-lookup"><span data-stu-id="a015b-120">Section</span></span>                                                                                                    | <span data-ttu-id="a015b-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a015b-121">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a015b-122">Schnittstellen für Anwendungen</span><span class="sxs-lookup"><span data-stu-id="a015b-122">Interfaces for Applications</span></span>](interfaces-for-applications.md)                                             | <span data-ttu-id="a015b-123">Beschreibt Schnittstellen, die nur von Desktop Anwendungen, Windows Media Player-Plug-ins oder COM-Objekten verwendet werden, die Zugriff auf hoher Ebene auf ein tragbares Gerät benötigen.</span><span class="sxs-lookup"><span data-stu-id="a015b-123">Describes interfaces that are used or implemented only by desktop applications, Windows Media Player plug-ins, or COM objects that need high-level access to a portable device.</span></span>                     |
| [<span data-ttu-id="a015b-124">Schnittstellen für Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a015b-124">Interfaces for Service Providers</span></span>](interfaces-for-service-providers.md)                                   | <span data-ttu-id="a015b-125">Beschreibt Schnittstellen, die nur von Dienstanbietern verwendet oder implementiert werden, die die tatsächliche Kommunikation auf niedriger Ebene mit einem tragbaren Gerät verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a015b-125">Describes interfaces that are used or implemented only by service providers, which handle the actual low-level communication with a portable device.</span></span>                                                |
| [<span data-ttu-id="a015b-126">Windows Media DRM-Implemented-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a015b-126">Windows Media DRM-Implemented Interfaces</span></span>](windows-media-drm-implemented-interfaces.md)                   | <span data-ttu-id="a015b-127">Beschreibt Schnittstellen, die nicht für die Implementierung durch Dienstanbieter von Drittanbietern vorgesehen sind, aber intern von Windows Media DRM und Windows Media Device Manager implementiert und aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a015b-127">Describes interfaces that are not intended to be implemented by third-party service providers, but are implemented and called internally by the Windows Media DRM and Windows Media Device Manager.</span></span> |
| [<span data-ttu-id="a015b-128">Schnittstellen für Dienstanbieter und Anwendungen</span><span class="sxs-lookup"><span data-stu-id="a015b-128">Interfaces for Service Providers and Applications</span></span>](interfaces-for-service-providers-and-applications.md) | <span data-ttu-id="a015b-129">Beschreibt Schnittstellen, die von Anwendungen oder Dienstanbietern verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a015b-129">Describes interfaces that can be used either by applications or by service providers.</span></span>                                                                                                               |
| [<span data-ttu-id="a015b-130">Schnittstellen für sichere Inhaltsanbieter</span><span class="sxs-lookup"><span data-stu-id="a015b-130">Interfaces for Secure Content Providers</span></span>](interfaces-for-secure-content-providers.md)                     | <span data-ttu-id="a015b-131">Beschreibt Schnittstellen, die von einem Gerät oder einer Anwendung implementiert werden müssen, das von DRM geschützte Inhalte verwendet.</span><span class="sxs-lookup"><span data-stu-id="a015b-131">Describes interfaces that must be implemented by a device or application that will use DRM-protected content.</span></span>                                                                                       |
| [<span data-ttu-id="a015b-132">Strukturen</span><span class="sxs-lookup"><span data-stu-id="a015b-132">Structures</span></span>](structures.md)                                                                               | <span data-ttu-id="a015b-133">Beschreibt Strukturen, die für Windows Media Device Manager-Methoden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a015b-133">Describes structures used for Windows Media Device Manager methods.</span></span>                                                                                                                                 |
| [<span data-ttu-id="a015b-134">Enumerationstypen</span><span class="sxs-lookup"><span data-stu-id="a015b-134">Enumeration Types</span></span>](enumeration-types.md)                                                                 | <span data-ttu-id="a015b-135">Beschreibt Enumerationen, die für Windows Media Device Manager-Methoden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a015b-135">Describes enumerations used for Windows Media Device Manager methods.</span></span>                                                                                                                               |
| [<span data-ttu-id="a015b-136">Metadatenkonstanten</span><span class="sxs-lookup"><span data-stu-id="a015b-136">Metadata Constants</span></span>](metadata-constants.md)                                                               | <span data-ttu-id="a015b-137">Beschreibt die Konstanten, die vom Windows Media Device Manager SDK zum Festlegen oder Abrufen verschiedener Metadateneigenschaften für ein Gerät oder Objekt auf dem Gerät definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a015b-137">Describes the constants defined by the Windows Media Device Manager SDK for setting or retrieving various metadata properties for a device or object on the device.</span></span>                                 |
| [<span data-ttu-id="a015b-138">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a015b-138">Error Codes</span></span>](error-codes.md)                                                                             | <span data-ttu-id="a015b-139">Beschreibt die Fehlercodes, die von den Windows Media Device Manager SDK-Methoden zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="a015b-139">Describes the error codes that can be returned by Windows Media Device Manager SDK methods.</span></span>                                                                                                         |



 

 

 




