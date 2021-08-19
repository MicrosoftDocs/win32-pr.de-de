---
title: Erstellen einer XMR-Lizenz
description: Erstellen einer XMR-Lizenz
ms.assetid: c43e4913-82a6-4dd0-9d1f-1fb237ecbb30
keywords:
- Windows Medienformat-SDK, DRM-Import
- Windows Medienformat-SDK,Importieren
- Windows Media Format SDK, XMR-Lizenzen
- Windows Medienformat-SDK, Lizenzen
- Windows Medienformat-SDK, Erweiterbare Medienrechte (XMR)
- Digital Rights Management (DRM), Importieren
- DRM (Verwaltung digitaler Rechte),Importieren
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), XMR-Lizenzen
- DRM (Digital Rights Management), XMR-Lizenzen
- Digital Rights Management (DRM), Erweiterbare Medienrechte (XMR)
- DRM (Verwaltung digitaler Rechte),Erweiterbare Medienrechte (XMR)
- Erweiterte APIs des DRM-Clients, Importieren
- Erweiterte Client-APIs, Importieren
- Erweiterte DRM-Client-APIs, XMR-Lizenzen
- Erweiterte Client-APIs, XMR-Lizenzen
- Erweiterte APIs des DRM-Clients, Lizenzen
- Erweiterte Client-APIs, Lizenzen
- Erweiterte DRM-Client-APIs, Erweiterbare Medienrechte (XMR)
- Erweiterte Client-APIs, Erweiterbare Medienrechte (XMR)
- licenses,XMR
- Erweiterbare Medienrechte (XMR)
- XMR (Erweiterbare Medienrechte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a73406d36c6ec7903ee7966f162811336aaecccaac5093e6d467e02c1a56ec71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881401"
---
# <a name="building-an-xmr-license"></a>Erstellen einer XMR-Lizenz

Um eine Lizenz für die Verarbeitung Windows Media DRM zu generieren, müssen Sie das binäre XMR-Schema (Extensible Media Rights) verwenden. XMR ist ein Schema zum Vermitteln von Mediennutzungsrechten und -einschränkungen und muss separat lizenziert werden.

Das wichtige Material in einer Lizenz wird mit dem öffentlichen Schlüssel in der Windows Media DRM-Zertifikatsammlung verschlüsselt, sodass es nur für das Windows Media DRM Client Extended API-Subsystem sichtbar ist. .

Es liegt in Ihrer Verantwortung, sicherzustellen, dass die Lizenzstruktur und die Richtlinieneinstellungen gültig und mit der Absicht des Lizenzausstellers übereinstimmen und dass sie den Konformitätsregeln entsprechen.

Lesen Sie die Kompatibilitätsregeln für den Windows Media DRM-Import, um den vollständigen Satz von XMR-Objekten zu erfahren, die in der Lizenz vorhanden sein müssen.

Um die XMR-Lizenz an das DRM-Subsystem zu übergeben, rufen Sie die [**IWMDRMLicenseManagement::StoreLicense-Methode**](iwmdrmlicensemanagement-storelicense.md) auf. Verwenden Sie das folgende Format, um die Lizenz im *bstrLicenseResponse-Parameter* zu übergeben:


```C++
<LICENSERESPONSE>
    <LICENSE version="3.0.0.0">insert base64-encoded XMR license here</LICENSE>
</LICENSERESPONSE>
```



Diese Zeichenfolge muss im Unicode-Format (UTF-16) vorliegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DRM-Import**](drm-import.md)
</dt> </dl>

 

 




