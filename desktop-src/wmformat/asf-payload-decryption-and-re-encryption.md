---
title: ASF-Nutzlastentschlüsselung und erneute Verschlüsselung
description: ASF-Nutzlastentschlüsselung und erneute Verschlüsselung
ms.assetid: 0a8c996d-2167-483a-93af-6fe22f0efaf1
keywords:
- Windows Medienformat-SDK, ASF-Nutzlastentschlüsselung und erneute Verschlüsselung
- Windows Medienformat-SDK, Nutzlastentschlüsselung und erneute Verschlüsselung
- Windows Medienformat-SDK,Entschlüsselung
- Windows Medienformat-SDK, erneute Verschlüsselung
- Digital Rights Management (DRM), ASF-Nutzlastentschlüsselung und erneute Verschlüsselung
- DRM (Digital Rights Management), ASF-Nutzlastentschlüsselung und erneute Verschlüsselung
- Digital Rights Management (DRM), Nutzlastentschlüsselung und erneute Verschlüsselung
- DRM (Digital Rights Management), Nutzlastentschlüsselung und erneute Verschlüsselung
- Digital Rights Management (DRM), Entschlüsselung
- DRM (Verwaltung digitaler Rechte),Entschlüsselung
- Digital Rights Management (DRM), erneute Verschlüsselung
- DRM (Digital Rights Management), erneute Verschlüsselung
- Erweiterte DRM-Client-APIs, ASF-Nutzlastentschlüsselung und erneute Verschlüsselung
- Erweiterte Client-APIs, ASF-Nutzlastentschlüsselung und erneute Verschlüsselung
- Erweiterte APIs des DRM-Clients, Nutzlastentschlüsselung und erneute Verschlüsselung
- Erweiterte Client-APIs, Nutzlastentschlüsselung und erneute Verschlüsselung
- Erweiterte APIs des DRM-Clients, Entschlüsselung
- Erweiterte Client-APIs,Entschlüsselung
- Erweiterte DRM-Client-APIs, erneute Verschlüsselung
- Erweiterte Client-APIs, erneute Verschlüsselung
- Advanced Systems Format (ASF), erneute Verschlüsselung
- ASF (Advanced Systems Format), erneute Verschlüsselung
- Advanced Systems Format (ASF), Entschlüsselung
- ASF (Advanced Systems Format), Entschlüsselung
- Advanced Systems Format (ASF), Nutzlastentschlüsselung und erneute Verschlüsselung
- ASF (Advanced Systems Format), Nutzlastentschlüsselung und erneute Verschlüsselung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c60469ff0b1408fcf51cb3dde899559980790a09c01b6619b3ff2ba797554a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007110"
---
# <a name="asf-payload-decryption-and-re-encryption"></a>ASF-Nutzlastentschlüsselung und erneute Verschlüsselung

In den folgenden Schritten werden die Aktionen beschrieben, die eine Anwendung ausführen muss, um jede Nutzlast zu entschlüsseln und erneut zu verschlüsseln:

1.  Erhöhen Sie den Salt-Wert.
2.  Übergeben Sie die Nutzlast (verschlüsselt mit Windows Media DRM) und den Salt-Wert an die Entschlüsselungsfunktion [**IWMDRMDecrypt::D ecrypt,**](iwmdrmdecrypt-decrypt.md)die die Nutzlast zurückgibt, die mit dem öffentlichen RC4-Schlüssel verschlüsselt wurde.
3.  Leiten Sie einen vorübergehenden RC4-Schlüssel ab, indem Sie einen SHA-1-Hash des Initialisierungsvektors anwenden, der mit dem Salt-Wert verkettet ist.
4.  Verwenden Sie Ihren vorübergehenden Schlüssel, um die Nutzlast zu entschlüsseln.
5.  Verschlüsseln Sie die Nutzlast sofort mit dem autorisierten Inhaltsschutzschema gemäß den Regeln für die Konformität und Stabilität des drm-Exports für Windows Medien-DRM.
6.  Suchen Sie die nächste Nutzlast.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Exportieren von komprimierten Inhalten**](exporting-compressed-content.md)
</dt> </dl>

 

 




