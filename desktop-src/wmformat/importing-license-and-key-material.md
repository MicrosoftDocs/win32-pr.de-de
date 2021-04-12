---
title: Importieren von Lizenz-und Schlüssel Material
description: Importieren von Lizenz-und Schlüssel Material
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- Windows Media-Format-SDK, DRM-Import
- SDK für Windows Media-Format, importieren
- Windows Media-Format-SDK, Lizenzen
- Digital Rights Management (DRM), importieren
- DRM (Digital Rights Management), importieren
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), Schlüsselmaterial
- DRM (Digital Rights Management), Schlüsselmaterial
- Erweiterte APIs für den DRM-Client, Import
- Erweiterte Client-APIs, importieren
- Erweiterte APIs für den DRM-Client, Lizenzen
- Erweiterte Client-APIs, Lizenzen
- Erweiterte APIs für den DRM-Client, Schlüsselmaterial
- Erweiterte Client-APIs, Schlüsselmaterial
- Lizenzen, importieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a142d0087916a45b6dd8661b67f7e42eaed245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207304"
---
# <a name="importing-license-and-key-material"></a><span data-ttu-id="734f1-119">Importieren von Lizenz-und Schlüssel Material</span><span class="sxs-lookup"><span data-stu-id="734f1-119">Importing License and Key Material</span></span>

<span data-ttu-id="734f1-120">Wenn Sie über Medieninhalte verfügen, die mit einem Drittanbieter-Inhalts Schutzsystem verschlüsselt wurden, und Sie die Lizenz und das Schlüsselmaterial in Windows Media DRM importieren möchten, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="734f1-120">If you have media content that was encrypted using a third-party content protection system and you want to import the license and key material into Windows Media DRM, follow these steps:</span></span>

1.  <span data-ttu-id="734f1-121">Rufen Sie die Zertifikat Sammlung des Windows Media DRM-Computers durch Aufrufen der [**iwmdrmsecurity:: getmachinecertificate**](iwmdrmsecurity-getmachinecertificate.md) -Methode ab.</span><span class="sxs-lookup"><span data-stu-id="734f1-121">Retrieve the Windows Media DRM machine certificate collection by calling the [**IWMDRMSecurity::GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md) method.</span></span>
2.  <span data-ttu-id="734f1-122">Analysieren Sie die Zertifikat Sammlung, und stellen Sie sicher, dass Sie ordnungsgemäß signiert und mit einem bekannten öffentlichen Microsoft-Stamm Schlüssel überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="734f1-122">Parse the certificate collection, ensuring that it is signed correctly and is validated to a known Microsoft root public key.</span></span> <span data-ttu-id="734f1-123">Die Zertifikat Sammlung entspricht dem XMR-Schema.</span><span class="sxs-lookup"><span data-stu-id="734f1-123">The certificate collection conforms to the XMR schema.</span></span> <span data-ttu-id="734f1-124">Weitere Informationen finden Sie unter [Building a XMR License](building-an-xmr-license.md).</span><span class="sxs-lookup"><span data-stu-id="734f1-124">For more information, see [Building an XMR License](building-an-xmr-license.md).</span></span>
3.  <span data-ttu-id="734f1-125">Optional: Extrahieren Sie die Sperr Liste, indem Sie die [**iwmdrmsecurity:: getrevocationdata**](iwmdrmsecurity-getrevocationdata.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="734f1-125">Optional: Extract the revocation list by calling the [**IWMDRMSecurity::GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) method.</span></span>
4.  <span data-ttu-id="734f1-126">Optional: Stellen Sie sicher, dass kein Zertifikat in der Sammlung widerrufen wird.</span><span class="sxs-lookup"><span data-stu-id="734f1-126">Optional: Insure that no certificate in the collection is revoked.</span></span> <span data-ttu-id="734f1-127">Weitere Informationen finden Sie unter über [Prüfen der Zertifikat](checking-certificate-revocation.md)Sperrung.</span><span class="sxs-lookup"><span data-stu-id="734f1-127">For more information, see [Checking Certificate Revocation](checking-certificate-revocation.md).</span></span>
5.  <span data-ttu-id="734f1-128">Generieren Sie eine Lizenz im XMR-Format, die die Richtlinien Anforderungen für den Import Inhalt darstellt und das entsprechende Windows Media DRM-Schlüsselmaterial enthält.</span><span class="sxs-lookup"><span data-stu-id="734f1-128">Generate a license in the XMR format that represents the policy requirements for the import content and contains the appropriate Windows Media DRM key material.</span></span> <span data-ttu-id="734f1-129">Weitere Informationen finden Sie im Thema zum [aufbauen einer XMR-Lizenz](building-an-xmr-license.md).</span><span class="sxs-lookup"><span data-stu-id="734f1-129">For more information, see the topic [Building an XMR License](building-an-xmr-license.md).</span></span>
6.  <span data-ttu-id="734f1-130">Übergeben Sie die XMR-Lizenz zur Verarbeitung an das Windows Media DRM-System, indem Sie die [**iwmdrmlicenpasmanagement:: storelicense**](iwmdrmlicensemanagement-storelicense.md) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="734f1-130">Pass the XMR license to the Windows Media DRM system for processing, by using the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="734f1-131">Details zum XMR-Schema werden Ihnen bei der Lizenzierung von Windows Media DRM bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="734f1-131">Details about the XMR schema will be provided to you when you license Windows Media DRM.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="734f1-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="734f1-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="734f1-133">**Zertifikat Sperrung wird überprüft**</span><span class="sxs-lookup"><span data-stu-id="734f1-133">**Checking Certificate Revocation**</span></span>](checking-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="734f1-134">**Aufbauen einer XMR-Lizenz**</span><span class="sxs-lookup"><span data-stu-id="734f1-134">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> <dt>

[<span data-ttu-id="734f1-135">**DRM-Import**</span><span class="sxs-lookup"><span data-stu-id="734f1-135">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




