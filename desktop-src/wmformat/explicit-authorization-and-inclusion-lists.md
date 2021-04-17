---
title: Explizite Autorisierungs-und Inklusions Listen
description: Explizite Autorisierungs-und Inklusions Listen
ms.assetid: b2e1cdd4-ea3c-4b05-a53a-2cdc12440645
keywords:
- Windows Media-Format-SDK, DRM-Export
- SDK für Windows Media-Format, exportieren
- Windows Media-Format-SDK, explizite Autorisierungs-und Inklusions Listen
- Windows Media-Format-SDK, Autorisierungs Listen
- Windows Media-Format-SDK, Inklusions Listen
- Digital Rights Management (DRM), exportieren
- DRM (Digital Rights Management), exportieren
- Digital Rights Management (DRM), explizite Autorisierung und Inklusions Listen
- DRM-(Digital Rights Management), explizite Autorisierungs-und Inklusions Listen
- Digital Rights Management (DRM), Autorisierungs Listen
- DRM (Digital Rights Management), Autorisierungs Listen
- Digital Rights Management (DRM), Inklusions Listen
- DRM (Digital Rights Management), Inklusions Listen
- Erweiterte APIs für den DRM-Client, explizite Autorisierung und Inklusions Listen
- Erweiterte Client-APIs, explizite Autorisierungs-und Inklusions Listen
- Erweiterte APIs für den DRM-Client, Autorisierungs Listen
- Erweiterte Client-APIs, Autorisierungs Listen
- Erweiterte APIs für den DRM-Client, Inklusions Listen
- Erweiterte Client-APIs, Inklusions Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2309bed28ffd3add2a75c1cd90488b9ef454659b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389854"
---
# <a name="explicit-authorization-and-inclusion-lists"></a><span data-ttu-id="80e24-122">Explizite Autorisierungs-und Inklusions Listen</span><span class="sxs-lookup"><span data-stu-id="80e24-122">Explicit Authorization and Inclusion Lists</span></span>

<span data-ttu-id="80e24-123">Lizenzen können eine Inklusions Liste enthalten, um den Export von Inhalten, die von Windows Media DRM geschützt werden, explizit in andere Inhalts Schutz Schemas (CPS) zu autorisieren.</span><span class="sxs-lookup"><span data-stu-id="80e24-123">Licenses can contain an inclusion list to explicitly authorize the exporting of content protected by Windows Media DRM to other content protection schemes (CPS).</span></span> <span data-ttu-id="80e24-124">Gemäß den Bedingungen des Lizenzvertrags, den Sie bei Microsoft eingegeben haben, um den DRM-Export zu aktivieren, können Sie nur in ein gültiges CPS exportieren, das in der Inklusions Liste einer Lizenz angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="80e24-124">As per the terms of the license agreement you enter into with Microsoft to enable DRM Export you can export only to a valid CPS that is identified in the inclusion list of a license.</span></span>

<span data-ttu-id="80e24-125">Eine Inklusions Liste ist ein begrenztes Array von GUIDs (Global Unique Identifier), die jeweils ein bestimmtes autorisiertes CPS darstellen, in das der Inhalt exportiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="80e24-125">An inclusion list is a bounded array of globally unique identifiers (GUIDs) that each represents a specific authorized CPS to which the content can be exported.</span></span> <span data-ttu-id="80e24-126">Die in einer Inklusions Liste aufgeführten GUIDs sind unabhängig von den Ausgabe Schutz Ebenen (OPL) und Content Protection Levels (CPL).</span><span class="sxs-lookup"><span data-stu-id="80e24-126">The GUIDs listed in an inclusion list are independent of the output protection levels (OPL) and content protection levels (CPL).</span></span> <span data-ttu-id="80e24-127">Die Durchsetzung dieser Einschränkungen ist die Verantwortung ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="80e24-127">Enforcing these restrictions is the responsibility of your application.</span></span>

> [!Note]  
> <span data-ttu-id="80e24-128">Wenn Sie den Windows Media DRM-Export in komprimiertem Inhalt durchführen, greifen Sie über die [**iwmdrmlicense:: getinclusionlist**](iwmdrmlicense-getinclusionlist.md) -Methode auf die Aufnahme Liste zu.</span><span class="sxs-lookup"><span data-stu-id="80e24-128">When performing Windows Media DRM Export on compressed content, you access the inclusion list through the [**IWMDRMLicense::GetInclusionList**](iwmdrmlicense-getinclusionlist.md) method.</span></span> <span data-ttu-id="80e24-129">Wenn Sie den Windows Media DRM-Export auf nicht komprimierten Inhalt durchführen, verwenden Sie die [**IWMDRMReader3:: getinclusionlist**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) -Methode.</span><span class="sxs-lookup"><span data-stu-id="80e24-129">When performing Windows Media DRM Export on uncompressed content, use the [**IWMDRMReader3::GetInclusionList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) method.</span></span>

 

<span data-ttu-id="80e24-130">Wenden Sie sich an, um ein neues Inhalts Schutzsystem als Windows Media DRM zu registrieren, das in den Windows Media DRM-Export Kompatibilitäts Regeln zulässig ist wmla@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="80e24-130">To register a new content protection system as a Windows Media DRM Permitted Export in the Windows Media DRM export compliance rules, please contact wmla@microsoft.com.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80e24-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="80e24-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80e24-132">**DRM-Export**</span><span class="sxs-lookup"><span data-stu-id="80e24-132">**DRM Export**</span></span>](drm-export.md)
</dt> </dl>

 

 




