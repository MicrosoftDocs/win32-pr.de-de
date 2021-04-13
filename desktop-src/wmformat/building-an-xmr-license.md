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
# <a name="building-an-xmr-license"></a>Aufbauen einer XMR-Lizenz

Wenn Sie eine Lizenz für die Verarbeitung von Windows Media DRM generieren möchten, müssen Sie das Binär Schema erweiterbare Medienrechte (XMR) verwenden. XMR ist ein Schema zum Übermitteln von Nutzungsrechten und Einschränkungen für Medien und muss separat lizenziert werden.

Das wichtige Material in einer Lizenz wird mithilfe des öffentlichen Schlüssels in der Windows Media DRM-Zertifikat Sammlung verschlüsselt, sodass es nur für das erweiterte API-Subsystem des Windows Media DRM-Clients sichtbar ist. .

Es liegt in ihrer Verantwortung, sicherzustellen, dass die Lizenzstruktur und die Richtlinien Einstellungen gültig und mit der Absicht des Lizenz Ausstellers übereinstimmen und dass Sie den Konformitäts Regeln entsprechen.

Lesen Sie die Windows Media DRM-Regeln zum Importieren von Kompatibilitäts Regeln, um den gesamten Satz von XMR-Objekten zu erlernen, die in der Lizenz vorhanden sein müssen.

Um die XMR-Lizenz an das DRM-Subsystem zu übergeben, rufen Sie die [**iwmdrmlicenpasmanagement:: storelicense**](iwmdrmlicensemanagement-storelicense.md) -Methode auf. Verwenden Sie das folgende Format, um die Lizenz im *bstranlicenseresponse* -Parameter zu übergeben:


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

 

 




