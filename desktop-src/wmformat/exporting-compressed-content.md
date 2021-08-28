---
title: Exportieren von komprimierten Inhalten
description: Exportieren von komprimierten Inhalten
ms.assetid: b312aa5e-d693-4d0a-9d74-b443713cec8c
keywords:
- Windows Medienformat-SDK, DRM-Export
- Windows Medienformat-SDK, Exportieren
- Windows Medienformat-SDK, komprimierter Inhalt
- Digital Rights Management (DRM), Export
- DRM (Digital Rights Management),Export
- Digital Rights Management (DRM), komprimierter Inhalt
- DRM (Digital Rights Management), komprimierter Inhalt
- Erweiterte APIs des DRM-Clients, komprimierter Inhalt
- Erweiterte Client-APIs, komprimierter Inhalt
- Erweiterte DRM-Client-APIs, Exportieren
- Erweiterte Client-APIs, Exportieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e7e8e6d71e4104d65336b131d0e15d5eaedd8b2fba4b7715f5e60aa6083544
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055500"
---
# <a name="exporting-compressed-content"></a>Exportieren von komprimierten Inhalten

In diesem Abschnitt wird beschrieben, wie Windows durch Medien-DRM geschützte Medien in eine Windows Mediendatei exportiert werden, in der die Anwendung komprimierte digitale Mediendaten empfängt. Hierzu muss Ihre Anwendung die Inlineentschlüsselung aller Windows Media DRM-verschlüsselten Nutzlasten in einer ASF-Datei durchführen.

> [!Note]  
> Eine ASF-Analysebibliothek wird Ihnen im Rahmen der Windows Medien-DRM-Exportvereinbarung zur Verfügung gestellt.

 

Die wichtigsten Schritte beim Exportieren komprimierter Inhalte sind:

1.  Führen Sie bei Bedarf eine DRM-Individualisierung durch.
2.  Vergewissern Sie sich, dass das Zielinhaltsschutzschema explizit zulässig ist.
3.  Erstellen Sie ein Entschlüsselungsobjekt, um jede ASF-Nutzlast zu entschlüsseln.
4.  Das DRM-System verschlüsselt jede ASF-Nutzlast von Windows Medien-DRM in RC4, bevor es an Ihre Anwendung übergeben wird.

Wenn Ihre Anwendung die Größe einer ASF-Nutzlast während der Transcryption ändert, müssen Sie auch die ASF-Datei neu erstellen.

Übergeben Sie ein Windows Medien-DRM-Exportanwendungszertifikat an die Stubbibliothek. Das Zertifikat wird überprüft, und wenn es gültig ist, generiert das DRM-System einen Initialisierungsvektor und verschlüsselt es mit RSA OAEP.

-   Ein RC4-Sitzungsschlüssel wird für jede Nutzlast erstellt, indem der Initialisierungsvektor und ein Salt-Wert verkettet werden. Sie stellen den Salt-Wert für die Entschlüsselungs-API bereit und müssen ihn für jede Nutzlast um einen positiven ganzzahligen Wert ungleich 0 erhöhen.

Im Rahmen der Windows Media DRM-Exportvereinbarung wird Ihnen von Microsoft ein Tool bereitgestellt, mit dem Sie Ihr eigenes RSA-Schlüsselpaar aus öffentlichem und privatem Schlüssel generieren können. Sie senden den öffentlichen Schlüssel an Microsoft, wo Microsoft ihn in ein signiertes Windows Media DRM-Anwendungszertifikat integriert und zurückgibt.

Jede Nutzlast, nachdem sie mit dem RC4-Entschlüsselungsschlüssel entschlüsselt wurde, muss sofort im Ausgabe-CPS verschlüsselt werden. Es gibt weitere Einschränkungen bei der Behandlung unverschlüsselter Nutzlasten, die in den Robustheits- und Konformitätsregeln beschrieben sind, die mit dem Windows Media DRM Export Agreement einhergehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ASF-Nutzlastentschlüsselung und erneute Verschlüsselung**](asf-payload-decryption-and-re-encryption.md)
</dt> <dt>

[**DRM-Export**](drm-export.md)
</dt> <dt>

[**Durchführen der DRM-Individualisierung**](performing-drm-individualization.md)
</dt> <dt>

[**Überprüfung und Initialisierung**](verification-and-initialization.md)
</dt> </dl>

 

 




