---
title: Lizenzlöschung
description: Lizenzlöschung
ms.assetid: f941efeb-145d-48a1-a3e2-d12f66b7fdcf
keywords:
- Windows Medienformat-SDK, Lizenzen
- Windows Medienformat-SDK, Löschen von Lizenzen
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), Löschen von Lizenzen
- DRM (Digital Rights Management), Löschen von Lizenzen
- ERWEITERTE APIs für DEN DRM-Client, Lizenzen
- Erweiterte Client-APIs,Lizenzen
- Erweiterte APIs für DEN DRM-Client, Löschen von Lizenzen
- Erweiterte Client-APIs, Löschen von Lizenzen
- licenses,deleting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd1e20c0e98fd2129b807cf11f27f5975701d851d9301eda894ccb24015360a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808300"
---
# <a name="license-deletion"></a>Lizenzlöschung

Alle lokal erstellten Drittanbieterlizenzen, z. B. durch DRM-Import, können durch Aufrufen der [**IWMDRMLicenseManagement::P rocessLicenseDeletionMessage-Methode**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) gelöscht werden. Die Zeichenfolge, die Sie an diese Methode übergeben, ist eine XMR-Lizenz, die der folgenden ähnelt:


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



Das Feld für die besitzerspezifische Benutzer-ID (UID) ist optional. Optionale Felder dürfen nicht in der Lizenzantwort enthalten sein, wenn ihnen keine Daten zugeordnet sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen einer XMR-Lizenz**](building-an-xmr-license.md)
</dt> <dt>

[**DRM-Import**](drm-import.md)
</dt> <dt>

[**Programmierhandbuch**](drm-programming-guide.md)
</dt> </dl>

 

 




