---
title: Exportieren von komprimiertem Inhalt
description: Exportieren von komprimiertem Inhalt
ms.assetid: b312aa5e-d693-4d0a-9d74-b443713cec8c
keywords:
- Windows Media-Format-SDK, DRM-Export
- SDK für Windows Media-Format, exportieren
- Windows Media-Format-SDK, komprimierter Inhalt
- Digital Rights Management (DRM), exportieren
- DRM (Digital Rights Management), exportieren
- Digital Rights Management (DRM), komprimierter Inhalt
- DRM (Digital Rights Management), komprimierter Inhalt
- Erweiterte APIs für den DRM-Client, komprimierter Inhalt
- Erweiterte Client-APIs, komprimierter Inhalt
- Erweiterte APIs für den DRM-Client, exportieren
- Erweiterte Client-APIs, exportieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37781d5575dbffb7103f07307a149f4bd5e9e4fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855919"
---
# <a name="exporting-compressed-content"></a>Exportieren von komprimiertem Inhalt

In diesem Abschnitt wird das Exportieren von Windows Media DRM-geschützten Medien in eine Windows Media-Datei beschrieben, in der die Anwendung komprimierte digitale Mediendaten empfängt. Zu diesem Zweck muss Ihre Anwendung die Inline Entschlüsselung sämtlicher verschlüsselter Nutzlasten von Windows Media DRM in einer ASF-Datei durchführen.

> [!Note]  
> Eine DRM-Bibliotheks Bibliothek wird Ihnen als Teil des Windows Media DRM-Export Vertrags bereitgestellt.

 

Die wichtigsten Schritte zum Exportieren komprimierter Inhalte sind:

1.  Führen Sie bei Bedarf DRM-Individualisierung durch.
2.  Vergewissern Sie sich, dass das Ziel Inhalts Schutz-Schema explizit zulässig ist.
3.  Erstellen Sie ein Entschlüsselungs-Objekt, um jede ASF-Nutzlast zu entschlüsseln.
4.  Das DRM-System durchläuft die einzelnen ASF-Nutzlasten von Windows Media DRM in RC4, bevor es an die Anwendung übergeben wird.

Wenn die Größe einer ASF-Nutzlast von der Anwendung während der Durchgängen geändert wird, müssen Sie auch die ASF-Datei neu angleichen.

Übergeben Sie an die Stub-Bibliothek ein Windows Media DRM-Export Anwendungs Zertifikat. Das Zertifikat wird überprüft. wenn es gültig ist, generiert das DRM-System einen Initialisierungs Vektor und verschlüsselt es mit RSA OAEP.

-   Ein RC4-Sitzungsschlüssel wird für jede Nutzlast erstellt, indem der Initialisierungs Vektor und ein Salt-Wert verkettet werden. Sie geben den Salt-Wert für die Entschlüsselungs-API an, und Sie müssen ihn durch einen positiven ganzzahligen Wert ungleich 0 (null) für jede Nutzlast erhöhen.

Sie werden ein Tool von Microsoft als Teil des Windows Media DRM-Export Vertrags bereitstellen, mit dem Sie Ihr eigenes RSA-Schlüsselpaar aus öffentlichem und privatem Schlüssel generieren können. Der öffentliche Schlüssel wird an Microsoft gesendet, wobei Microsoft ihn in ein signiertes Windows Media DRM-Anwendungs Zertifikat integrieren und zurückgeben wird.

Jede Nutzlast, nachdem Sie mit dem RC4-Entschlüsselungsschlüssel entschlüsselt wurde, muss sofort in die Ausgabe-CPS verschlüsselt werden. Es gibt weitere Einschränkungen bei der Behandlung unverschlüsselter Nutzlasten, die in den Regeln für Stabilität und Konformität beschrieben werden, die mit dem Windows Media DRM-Export Vertrag einhergehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Entschlüsselung und erneute Verschlüsselung von ASF-Nutzlast**](asf-payload-decryption-and-re-encryption.md)
</dt> <dt>

[**DRM-Export**](drm-export.md)
</dt> <dt>

[**Durchführen der DRM-Individualisierung**](performing-drm-individualization.md)
</dt> <dt>

[**Überprüfung und Initialisierung**](verification-and-initialization.md)
</dt> </dl>

 

 




