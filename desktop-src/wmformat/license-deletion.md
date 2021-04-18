---
title: Löschen von Lizenzen
description: Löschen von Lizenzen
ms.assetid: f941efeb-145d-48a1-a3e2-d12f66b7fdcf
keywords:
- Windows Media-Format-SDK, Lizenzen
- Windows Media-Format-SDK, Löschen von Lizenzen
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), Löschen von Lizenzen
- DRM (Digital Rights Management), Löschen von Lizenzen
- Erweiterte APIs für den DRM-Client, Lizenzen
- Erweiterte Client-APIs, Lizenzen
- Erweiterte APIs für den DRM-Client, Löschen von Lizenzen
- Erweiterte Client-APIs, Löschen von Lizenzen
- Lizenzen, löschen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f297db679ac2c8afe2c836d032fa045d6955665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338591"
---
# <a name="license-deletion"></a><span data-ttu-id="596a3-114">Löschen von Lizenzen</span><span class="sxs-lookup"><span data-stu-id="596a3-114">License Deletion</span></span>

<span data-ttu-id="596a3-115">Alle lokal erstellten Drittanbieter Lizenzen (z. b. über den DRM-Import) können durch Aufrufen der Methode [**iwmdrmlicensmanagement::P rocess licenabdeletionmessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="596a3-115">Any third-party licenses created locally, for example through DRM import, can be deleted by calling the [**IWMDRMLicenseManagement::ProcessLicenseDeletionMessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) method.</span></span> <span data-ttu-id="596a3-116">Die Zeichenfolge, die Sie an diese Methode übergeben, ist eine XMR-Lizenz, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="596a3-116">The string you pass to this method will be an XMR license that resembles the following:</span></span>


```C++
<response type="LRB">
  <DATA>
    <LICENSEDATA>
      <DATA>
        <KID>include Key ID here to revoke certain keys</KID>
        <LID>rights ID</LID
        <META>
          <LGPUBKEY>
            <PublicKey>
              <Modulus>base64 encoded public key</Modulus>
              <Exponent>Exponent in network byte order</Exponent>
            </PublicKey>
          </LGPUBKEY>
          <UID>content-owner-specific user ID</UID>
        </META>
      </DATA>
    </LICENSEDATA>
  </DATA>
</response>
```



<span data-ttu-id="596a3-117">Das Feld Besitzer spezifischer Benutzer-ID (UID) ist optional.</span><span class="sxs-lookup"><span data-stu-id="596a3-117">The owner specific user ID (UID) field is optional.</span></span> <span data-ttu-id="596a3-118">Optionale Felder dürfen nicht in die Lizenz Antwort eingeschlossen werden, wenn Ihnen keine Daten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="596a3-118">Optional fields must not be included in the license response if there is not any data associated with them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="596a3-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="596a3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="596a3-120">**Aufbauen einer XMR-Lizenz**</span><span class="sxs-lookup"><span data-stu-id="596a3-120">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> <dt>

[<span data-ttu-id="596a3-121">**DRM-Import**</span><span class="sxs-lookup"><span data-stu-id="596a3-121">**DRM Import**</span></span>](drm-import.md)
</dt> <dt>

[<span data-ttu-id="596a3-122">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="596a3-122">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




