---
title: WMDM-Referenz
description: Das Windows Media Geräte-Manager SDK besteht aus einer Auflistung von Schnittstellen, Strukturen, Enumerationen und Konstanten. Verwenden Sie diese Referenzartikel.
ms.assetid: 1d2260a8-bc9f-41b3-a3b0-0176b45fff1f
keywords:
- Windows Media Geräte-Manager,Programmierreferenz
- Geräte-Manager, Programmierreferenz
- Windows Media Geräte-Manager,Desktopanwendungen
- Geräte-Manager,Desktopanwendungen
- Windows Media Geräte-Manager, Dienstanbieter
- Geräte-Manager,Dienstanbieter
- Desktopanwendungen,Programmierreferenz
- Dienstanbieter, Programmierreferenz
- Programmierreferenz,Desktopanwendungen
- Programmierreferenz,Dienstanbieter
- Programmierreferenz,Windows Media Geräte-Manager
- Referenz für Windows Media Geräte-Manager,About
- Referenz für Windows Media Geräte-Manager,Desktopanwendungen
- Referenz für Windows Media Geräte-Manager,Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e624bbc445d5d5e376cad926248ae4ee4db17a6e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406523"
---
# <a name="wmdm-reference"></a><span data-ttu-id="3f5cd-118">WMDM-Referenz</span><span class="sxs-lookup"><span data-stu-id="3f5cd-118">WMDM reference</span></span>

<span data-ttu-id="3f5cd-119">Das Windows Media Geräte-Manager SDK besteht aus einer Auflistung von Schnittstellen, Strukturen, Enumerationen und Konstanten.</span><span class="sxs-lookup"><span data-stu-id="3f5cd-119">The Windows Media Device Manager SDK consists of a collection of interfaces, structures, enumerations, and constants.</span></span> <span data-ttu-id="3f5cd-120">Im Verweisabschnitt werden die Schnittstellen entsprechend dem Objekttyp, der sie verwendet, in Gruppen unterteilt.</span><span class="sxs-lookup"><span data-stu-id="3f5cd-120">The reference section divides the interfaces into groups according to the type of object that uses them.</span></span>



| <span data-ttu-id="3f5cd-121">`Section`</span><span class="sxs-lookup"><span data-stu-id="3f5cd-121">Section</span></span>                                                                                                    | <span data-ttu-id="3f5cd-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f5cd-122">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f5cd-123">Schnittstellen für Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3f5cd-123">Interfaces for Applications</span></span>](interfaces-for-applications.md)                                             | <span data-ttu-id="3f5cd-124">Beschreibt Schnittstellen, die nur von Desktopanwendungen, Windows Media Player Plug-Ins oder COM-Objekten verwendet oder implementiert werden, die zugriff auf ein portables Gerät auf hoher Ebene benötigen.</span><span class="sxs-lookup"><span data-stu-id="3f5cd-124">Describes interfaces that are used or implemented only by desktop applications, Windows Media Player plug-ins, or COM objects that need high-level access to a portable device.</span></span>                     |
| [<span data-ttu-id="3f5cd-125">Schnittstellen für Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="3f5cd-125">Interfaces for Service Providers</span></span>](interfaces-for-service-providers.md)                                   | <span data-ttu-id="3f5cd-126">Beschreibt Schnittstellen, die nur von Dienstanbietern verwendet oder implementiert werden, die die tatsächliche Kommunikation auf niedriger Ebene mit einem portablen Gerät verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="3f5cd-126">Describes interfaces that are used or implemented only by service providers, which handle the actual low-level communication with a portable device.</span></span>                                                |
| [<span data-ttu-id="3f5cd-127">Windows Media DRM-Implemented Interfaces</span><span class="sxs-lookup"><span data-stu-id="3f5cd-127">Windows Media DRM-Implemented Interfaces</span></span>](windows-media-drm-implemented-interfaces.md)                   | <span data-ttu-id="3f5cd-128">Beschreibt Schnittstellen, die nicht von Drittanbietern implementiert werden sollen, sondern intern vom Windows Media DRM- und Windows Media-Geräte-Manager implementiert und aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3f5cd-128">Describes interfaces that are not intended to be implemented by third-party service providers, but are implemented and called internally by the Windows Media DRM and Windows Media Device Manager.</span></span> |
| [<span data-ttu-id="3f5cd-129">Schnittstellen für Dienstanbieter und Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3f5cd-129">Interfaces for Service Providers and Applications</span></span>](interfaces-for-service-providers-and-applications.md) | <span data-ttu-id="3f5cd-130">Beschreibt Schnittstellen, die von Anwendungen oder Dienstanbietern verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3f5cd-130">Describes interfaces that can be used either by applications or by service providers.</span></span>                                                                                                               |
| [<span data-ttu-id="3f5cd-131">Schnittstellen für sichere Inhaltsanbieter</span><span class="sxs-lookup"><span data-stu-id="3f5cd-131">Interfaces for Secure Content Providers</span></span>](interfaces-for-secure-content-providers.md)                     | <span data-ttu-id="3f5cd-132">Beschreibt Schnittstellen, die von einem Gerät oder einer Anwendung implementiert werden müssen, die DRM-geschützte Inhalte verwenden.</span><span class="sxs-lookup"><span data-stu-id="3f5cd-132">Describes interfaces that must be implemented by a device or application that will use DRM-protected content.</span></span>                                                                                       |
| [<span data-ttu-id="3f5cd-133">Strukturen</span><span class="sxs-lookup"><span data-stu-id="3f5cd-133">Structures</span></span>](structures.md)                                                                               | <span data-ttu-id="3f5cd-134">Beschreibt Strukturen, die für Windows Media Geräte-Manager-Methoden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f5cd-134">Describes structures used for Windows Media Device Manager methods.</span></span>                                                                                                                                 |
| [<span data-ttu-id="3f5cd-135">Enumerationstypen</span><span class="sxs-lookup"><span data-stu-id="3f5cd-135">Enumeration Types</span></span>](enumeration-types.md)                                                                 | <span data-ttu-id="3f5cd-136">Beschreibt Enumerationen, die für Windows Media Geräte-Manager-Methoden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f5cd-136">Describes enumerations used for Windows Media Device Manager methods.</span></span>                                                                                                                               |
| [<span data-ttu-id="3f5cd-137">Metadatenkonstanten</span><span class="sxs-lookup"><span data-stu-id="3f5cd-137">Metadata Constants</span></span>](metadata-constants.md)                                                               | <span data-ttu-id="3f5cd-138">Beschreibt die Konstanten, die vom Windows Media Geräte-Manager SDK zum Festlegen oder Abrufen verschiedener Metadateneigenschaften für ein Gerät oder Objekt auf dem Gerät definiert werden.</span><span class="sxs-lookup"><span data-stu-id="3f5cd-138">Describes the constants defined by the Windows Media Device Manager SDK for setting or retrieving various metadata properties for a device or object on the device.</span></span>                                 |
| [<span data-ttu-id="3f5cd-139">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3f5cd-139">Error Codes</span></span>](error-codes.md)                                                                             | <span data-ttu-id="3f5cd-140">Beschreibt die Fehlercodes, die von Windows Media Geräte-Manager SDK-Methoden zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="3f5cd-140">Describes the error codes that can be returned by Windows Media Device Manager SDK methods.</span></span>                                                                                                         |



 

 

 




