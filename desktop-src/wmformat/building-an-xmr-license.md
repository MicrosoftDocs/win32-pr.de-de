---
title: Aufbauen einer XMR-Lizenz
description: Aufbauen einer XMR-Lizenz
ms.assetid: c43e4913-82a6-4dd0-9d1f-1fb237ecbb30
keywords:
- Windows Media-Format-SDK, DRM-Import
- SDK für Windows Media-Format, importieren
- Windows Media-Format-SDK, XMR-Lizenzen
- Windows Media-Format-SDK, Lizenzen
- Windows Media-Format-SDK, erweiterbare Medienrechte (XMR)
- Digital Rights Management (DRM), importieren
- DRM (Digital Rights Management), importieren
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), XMR-Lizenzen
- DRM-(Digital Rights Management), XMR-Lizenzen
- Digital Rights Management (DRM), erweiterbare Medienrechte (XMR)
- DRM (Digital Rights Management), erweiterbare Medienrechte (XMR)
- Erweiterte APIs für den DRM-Client, Import
- Erweiterte Client-APIs, importieren
- Erweiterte APIs für den DRM-Client, XMR-Lizenzen
- Erweiterte Client-APIs, XMR-Lizenzen
- Erweiterte APIs für den DRM-Client, Lizenzen
- Erweiterte Client-APIs, Lizenzen
- Erweiterte APIs für den DRM-Client, erweiterbare Medienrechte (XMR)
- Erweiterte Client-APIs, erweiterbare Medienrechte (XMR)
- Lizenzen, XMR
- Erweiterbare Medienrechte (XMR)
- XMR (erweiterbare Medienrechte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc275419116362c08cabe4dc70aa227687705fdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387979"
---
# <a name="building-an-xmr-license"></a><span data-ttu-id="37397-127">Aufbauen einer XMR-Lizenz</span><span class="sxs-lookup"><span data-stu-id="37397-127">Building an XMR License</span></span>

<span data-ttu-id="37397-128">Wenn Sie eine Lizenz für die Verarbeitung von Windows Media DRM generieren möchten, müssen Sie das Binär Schema erweiterbare Medienrechte (XMR) verwenden.</span><span class="sxs-lookup"><span data-stu-id="37397-128">To generate a license for Windows Media DRM to process, you must use the Extensible Media Rights (XMR) binary schema.</span></span> <span data-ttu-id="37397-129">XMR ist ein Schema zum Übermitteln von Nutzungsrechten und Einschränkungen für Medien und muss separat lizenziert werden.</span><span class="sxs-lookup"><span data-stu-id="37397-129">XMR is a schema for conveying media usage rights and restrictions and needs to be licensed separately.</span></span>

<span data-ttu-id="37397-130">Das wichtige Material in einer Lizenz wird mithilfe des öffentlichen Schlüssels in der Windows Media DRM-Zertifikat Sammlung verschlüsselt, sodass es nur für das erweiterte API-Subsystem des Windows Media DRM-Clients sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="37397-130">The important material in a license is encrypted using the public key in the Windows Media DRM certificate collection, so it is visible only to the Windows Media DRM Client Extended API subsystem.</span></span> <span data-ttu-id="37397-131">.</span><span class="sxs-lookup"><span data-stu-id="37397-131">.</span></span>

<span data-ttu-id="37397-132">Es liegt in ihrer Verantwortung, sicherzustellen, dass die Lizenzstruktur und die Richtlinien Einstellungen gültig und mit der Absicht des Lizenz Ausstellers übereinstimmen und dass Sie den Konformitäts Regeln entsprechen.</span><span class="sxs-lookup"><span data-stu-id="37397-132">It is your responsibility to ensure that the license structure and policy settings are valid and consistent with the license issuer's intent, and that they conform to the compliance rules.</span></span>

<span data-ttu-id="37397-133">Lesen Sie die Windows Media DRM-Regeln zum Importieren von Kompatibilitäts Regeln, um den gesamten Satz von XMR-Objekten zu erlernen, die in der Lizenz vorhanden sein müssen.</span><span class="sxs-lookup"><span data-stu-id="37397-133">You should read the Windows Media DRM import compliance rules to learn the complete set of XMR objects that must be present in the license.</span></span>

<span data-ttu-id="37397-134">Um die XMR-Lizenz an das DRM-Subsystem zu übergeben, rufen Sie die [**iwmdrmlicenpasmanagement:: storelicense**](iwmdrmlicensemanagement-storelicense.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="37397-134">To pass the XMR license to the DRM subsystem, call the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span> <span data-ttu-id="37397-135">Verwenden Sie das folgende Format, um die Lizenz im *bstranlicenseresponse* -Parameter zu übergeben:</span><span class="sxs-lookup"><span data-stu-id="37397-135">Use the following format to pass the license in the *bstrLicenseResponse* parameter:</span></span>


```C++
<LICENSERESPONSE>
    <LICENSE version="3.0.0.0">insert base64-encoded XMR license here</LICENSE>
</LICENSERESPONSE>
```



<span data-ttu-id="37397-136">Diese Zeichenfolge muss im Unicode-Format (UTF-16) vorliegen.</span><span class="sxs-lookup"><span data-stu-id="37397-136">This string must be in Unicode format (UTF-16).</span></span>

## <a name="related-topics"></a><span data-ttu-id="37397-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="37397-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37397-138">**DRM-Import**</span><span class="sxs-lookup"><span data-stu-id="37397-138">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




