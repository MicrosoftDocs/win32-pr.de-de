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
# <a name="license-deletion"></a>Löschen von Lizenzen

Alle lokal erstellten Drittanbieter Lizenzen (z. b. über den DRM-Import) können durch Aufrufen der Methode [**iwmdrmlicensmanagement::P rocess licenabdeletionmessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) gelöscht werden. Die Zeichenfolge, die Sie an diese Methode übergeben, ist eine XMR-Lizenz, die der folgenden ähnelt:


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



Das Feld Besitzer spezifischer Benutzer-ID (UID) ist optional. Optionale Felder dürfen nicht in die Lizenz Antwort eingeschlossen werden, wenn Ihnen keine Daten zugeordnet sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aufbauen einer XMR-Lizenz**](building-an-xmr-license.md)
</dt> <dt>

[**DRM-Import**](drm-import.md)
</dt> <dt>

[**Programmierhandbuch**](drm-programming-guide.md)
</dt> </dl>

 

 




