---
title: Entschlüsselung und erneute Verschlüsselung von ASF-Nutzlast
description: Entschlüsselung und erneute Verschlüsselung von ASF-Nutzlast
ms.assetid: 0a8c996d-2167-483a-93af-6fe22f0efaf1
keywords:
- SDK für Windows Media-Format, ASF-Nutz Last Entschlüsselung und erneute Verschlüsselung
- Windows Media-Format-SDK, Nutzlast entschlüsseln und erneute Verschlüsselung
- SDK für Windows Media-Format, Entschlüsselung
- SDK für Windows Media-Format, erneute Verschlüsselung
- Digital Rights Management (DRM), ASF-Nutz Last Entschlüsselung und erneute Verschlüsselung
- DRM (Digital Rights Management), ASF-Nutz Last Entschlüsselung und erneute Verschlüsselung
- Digital Rights Management (DRM), Nutzlast entschlüsseln und erneute Verschlüsselung
- DRM (Digital Rights Management), Nutzlast entschlüsseln und erneute Verschlüsselung
- Digital Rights Management (DRM), Entschlüsselung
- DRM (Digital Rights Management), Entschlüsselung
- Digital Rights Management (DRM), erneute Verschlüsselung
- DRM (Digital Rights Management), erneute Verschlüsselung
- Erweiterte APIs für den DRM-Client, die Entschlüsselung der ASF-Nutzlast und die erneute Verschlüsselung
- Erweiterte Client-APIs, ASF-Nutz Last Entschlüsselung und erneute Verschlüsselung
- Erweiterte APIs für den DRM-Client, Nutzlast entschlüsseln und erneute Verschlüsselung
- Erweiterte Client-APIs, Nutzlast entschlüsseln und erneute Verschlüsselung
- Erweiterte APIs für den DRM-Client, Entschlüsselung
- Erweiterte Client-APIs, Entschlüsselung
- Erweiterte APIs für den DRM-Client, erneute Verschlüsselung
- Erweiterte Client-APIs, erneute Verschlüsselung
- Advanced Systems Format (ASF), erneute Verschlüsselung
- ASF (Advanced Systems Format), erneute Verschlüsselung
- Advanced Systems Format (ASF), Entschlüsselung
- ASF (Advanced Systems Format), Entschlüsselung
- Advanced Systems Format (ASF), Nutzlast entschlüsseln und erneute Verschlüsselung
- ASF (Advanced Systems Format), Nutzlast entschlüsseln und erneute Verschlüsselung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c6dcab1d483b737b6b05636b51b8af0502350
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707866"
---
# <a name="asf-payload-decryption-and-re-encryption"></a>Entschlüsselung und erneute Verschlüsselung von ASF-Nutzlast

In den folgenden Schritten werden die Aktionen beschrieben, die eine Anwendung zum Entschlüsseln und erneuten Verschlüsseln der einzelnen Nutzlasten ausführen muss:

1.  Erhöhen Sie den Salt-Wert.
2.  Übergeben Sie die mit Windows Media DRM verschlüsselte Nutzlast (mit Windows Media DRM) und den Salt-Wert an die Entschlüsselungs Funktion [**iwmdrmentschlüsseln::D ecrypt**](iwmdrmdecrypt-decrypt.md), die die Nutzlast zurückgibt, die mithilfe des öffentlichen RC4-Schlüssels verschlüsselt wird.
3.  Leiten Sie einen vorübergehendes RC4-Schlüssel ab, indem Sie einen SHA-1-Hash des Initialisierungs Vektors anwenden, der mit dem Salt-Wert verkettet ist.
4.  Verwenden Sie Ihren vorübergehendes-Schlüssel, um die Nutzlast zu entschlüsseln.
5.  Erneutes Verschlüsseln der Nutzlast mit dem autorisierten Inhalts Schutzschema gemäß den Windows Media DRM-Regeln zum Exportieren von Konformität und Stabilität.
6.  Suchen Sie die nächste Nutzlast.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Exportieren von komprimiertem Inhalt**](exporting-compressed-content.md)
</dt> </dl>

 

 




