---
description: WPD \_ CONTENT \_ TYPE \_ CONTACT
ms.assetid: 3ff6191f-d3c0-4bd3-946e-c3fbf68f368c
title: WPD_CONTENT_TYPE_CONTACT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8354aa444f476e7c0b64d2e3d14d474c6eea02f90e8313c20073db2d0368fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083334"
---
# <a name="wpd_content_type_contact"></a>WPD \_ CONTENT \_ TYPE \_ CONTACT

Ein Objekt, das seinen Typ als WPD \_ CONTENT \_ TYPE CONTACT \_ beschreibt, stellt persönliche Kontaktdaten dar.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



| Eigenschaftsname                                                                                                                   | Erforderlich oder optional                                                           |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [\_WPD-OBJEKT-ID \_](object-properties.md)                                                                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft nicht festlegen, auch nicht zum Zeitpunkt der Erstellung. |
| [ÜBERGEORDNETE ID DES \_ \_ WPD-OBJEKTS \_](object-properties.md)                                                           | Erforderlich.                                                                      |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                                      | Erforderlich, wenn das -Objekt eine Datei darstellt.                                      |
| [PERSISTENTE EINDEUTIGE ID \_ DES WPD-OBJEKTS \_ \_ \_](object-properties.md)                                    | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft nicht festlegen, auch nicht zum Zeitpunkt der Erstellung. |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                                  | Erforderlich.                                                                      |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                                     | Erforderlich.                                                                      |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                              | Erforderlich, wenn das Objekt ausgeblendet ist.                                              |
| [\_WPD-OBJEKT \_ ISSYSTEM](object-properties.md)                                                              | Erforderlich, wenn das -Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).          |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                                      | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                              |
| [\_WPD-OBJEKT \_ \_ URSPRÜNGLICHER \_ DATEINAME](object-properties.md)                                        | Erforderlich, wenn das -Objekt eine Datei darstellt.                                      |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                                 | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.          |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                          | Erforderlich, wenn das -Objekt Verweise auf andere Objekte enthält.                        |
| [\_WPD-OBJEKTSCHLÜSSELWÖRTER \_](object-properties.md)                                                              | Optional.                                                                      |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                               | Optional.                                                                      |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                            | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt ist.                         |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                                     | Optional.                                                                      |
| [\_WPD-OBJEKTDATUM \_ \_ GEÄNDERT](object-properties.md)                                                   | Empfohlen.                                                                   |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                                   | Optional.                                                                      |
| [WPD \_ OBJECT BACK REFERENCES (WPD-OBJEKTVERWEISE \_ \_ ZURÜCK)](object-properties.md)                                                                          | Wird empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.                     |
| [\_ \_ WPD-OBJEKTCONTAINER \_ FUNKTIONALE \_ \_ OBJEKT-ID](object-properties.md)               | Optional.                                                                      |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHT AUS \_ RESSOURCE](object-properties.md)           | Optional.                                                                      |
| [\_ \_ WPD-KONTAKTANZEIGENAME \_](contact-properties.md)                                                  | Erforderlich.                                                                      |
| [\_WPD-OBJEKT \_ KANN LÖSCHEN \_](object-properties.md)                                                                               | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                      |
| [WPD \_ OBJECT \_ LANGUAGE \_ LOCALE](object-properties.md)                                                                          | Optional.                                                                      |
| [\_ \_ WPD-KONTAKTANZEIGENAME \_](contact-properties.md)                                                                           | Erforderlich.                                                                      |
| [\_ \_ WPD-KONTAKTNAME \_](contact-properties.md)                                                      | Empfohlen.                                                                   |
| [WPD \_ CONTACT \_ MIDDLE \_ NAMES](contact-properties.md)                                                  | Empfohlen.                                                                   |
| [WPD \_ CONTACT \_ LAST \_ NAME](contact-properties.md)                                                        | Empfohlen.                                                                   |
| [\_ \_ WPD-KONTAKTPRÄFIX](contact-properties.md)                                                               | Empfohlen.                                                                   |
| [\_WPD-KONTAKTSUFFIX \_](contact-properties.md)                                                               | Empfohlen.                                                                   |
| [WPD \_ CONTACT \_ PHONETIC FIRST NAME (PHONETISCHER VORNAME DES \_ \_ WPD-KONTAKTS)](contact-properties.md)                                   | Optional.                                                                      |
| [WPD \_ CONTACT \_ PHONETIC LAST NAME (PHONETISCHER \_ NACHNAME DES \_ WPD-KONTAKTS)](contact-properties.md)                                     | Optional.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ FULL \_ POSTAL \_ ADDRESS](contact-properties.md)                | Empfohlen.                                                                   |
| [WPD \_ CONTACT \_ PERSONAL \_ POSTAL \_ ADDRESS \_ LINE1](contact-properties.md)              | Optional.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ POSTAL \_ ADDRESS \_ LINE2](contact-properties.md)              | Optional.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ POSTAL \_ ADDRESS \_ CITY](contact-properties.md)                | Optional.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ POSTAL \_ ADDRESS \_ REGION](contact-properties.md)            | Optional.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ POSTAL \_ ADDRESS \_ POSTAL \_ CODE](contact-properties.md) | Optional.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ POSTAL \_ ADDRESS \_ COUNTRY](contact-properties.md)          | Optional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ FULL \_ POSTAL \_ ADDRESS](contact-properties.md)                | Optional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ POSTAL \_ ADDRESS \_ LINE1](contact-properties.md)              | Optional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ POSTAL \_ ADDRESS \_ LINE2](contact-properties.md)              | Optional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ POSTAL \_ ADDRESS \_ CITY](contact-properties.md)                | Optional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ POSTAL \_ ADDRESS \_ REGION](contact-properties.md)            | Optional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ POSTAL \_ ADDRESS \_ POSTAL \_ CODE](contact-properties.md) | Optional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ POSTAL \_ ADDRESS \_ COUNTRY](contact-properties.md)          | Optional.                                                                      |
| [WPD \_ CONTACT OTHER FULL POSTAL ADDRESS (WPD-KONTAKT MIT ANDERER VOLLSTÄNDIGER \_ \_ \_ \_ POSTADRESSE)](contact-properties.md)                      | Optional.                                                                      |
| [WPD \_ CONTACT \_ OTHER \_ POSTAL \_ ADDRESS \_ LINE1](contact-properties.md)                    | Optional.                                                                      |
| [WPD \_ CONTACT \_ OTHER \_ POSTAL \_ ADDRESS \_ LINE2](contact-properties.md)                    | Optional.                                                                      |
| [WPD \_ CONTACT \_ OTHER \_ POSTAL \_ ADDRESS \_ CITY](contact-properties.md)                      | Optional.                                                                      |
| [WPD CONTACT OTHER POSTAL ADDRESS REGION (WPD \_ KONTAKT MIT EINER ANDEREN \_ \_ \_ \_ POSTANSCHRIFTSREGION)](contact-properties.md)                  | Optional.                                                                      |
| [WPD CONTACT OTHER POSTAL ADDRESS POSTAL CODE (WPD \_ KONTAKT \_ MIT ANDERER \_ \_ \_ \_ POSTLEITZAHL)](contact-properties.md)       | Optional.                                                                      |
| [WPD \_ CONTACT \_ OTHER \_ POSTAL \_ ADDRESS \_ POSTAL \_ COUNTRY](contact-properties.md) | Optional.                                                                      |
| [\_WPD-KONTAKT PRIMÄRE \_ \_ E-MAIL-ADRESSE \_](contact-properties.md)                               | Empfohlen.                                                                   |
| [WPD CONTACT PERSONAL EMAIL (PERSÖNLICHE \_ \_ \_ E-MAIL-ADRESSE DES WPD-KONTAKT](contact-properties.md)                                              | Optional.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ EMAIL2](contact-properties.md)                                            | Optional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ EMAIL](contact-properties.md)                                              | Optional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ EMAIL2](contact-properties.md)                                            | Optional.                                                                      |
| [WPD \_ KONTAKT MIT ANDEREN \_ \_ E-MAILS](contact-properties.md)                                                  | Optional.                                                                      |
| [WPD \_ CONTACT \_ PRIMARY \_ PHONE](contact-properties.md)                                                | Empfohlen.                                                                   |
| [WPD \_ CONTACT \_ PERSONAL \_ PHONE](contact-properties.md)                                              | Optional.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ PHONE2](contact-properties.md)                                            | Optional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ PHONE](contact-properties.md)                                              | Optional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ PHONE2](contact-properties.md)                                            | Optional.                                                                      |
| [\_WPD-KONTAKT \_ MOBILTELEFON \_](contact-properties.md)                                                  | Optional.                                                                      |
| [WPD \_ CONTACT \_ MOBILE \_ PHONE2](contact-properties.md)                                                | Optional.                                                                      |
| [WPD \_ CONTACT \_ PERSONAL \_ FAX](contact-properties.md)                                                  | Optional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ FAX](contact-properties.md)                                                  | Optional.                                                                      |
| [WPD \_ CONTACT \_ PAGER](contact-properties.md)                                                                 | Optional.                                                                      |
| [WPD \_ KONTAKT MIT ANDEREN \_ \_ TELEFONEN](contact-properties.md)                                                  | Optional.                                                                      |
| [WPD \_ CONTACT \_ PRIMARY \_ WEB \_ ADDRESS](contact-properties.md)                                   | Empfohlen.                                                                   |
| [WPD CONTACT PERSONAL WEB ADDRESS (PERSÖNLICHE \_ \_ WEBADRESSE DES \_ \_ WPD-KONTAKTS)](contact-properties.md)                                 | Optional.                                                                      |
| [WPD \_ CONTACT \_ BUSINESS \_ WEB \_ ADDRESS](contact-properties.md)                                 | Optional.                                                                      |
| [WPD \_ CONTACT \_ INSTANT \_ MESSENGER](contact-properties.md)                                        | Empfohlen                                                                    |
| [WPD \_ CONTACT \_ INSTANT \_ MESSENGER2](contact-properties.md)                                      | Optional.                                                                      |
| [WPD \_ CONTACT \_ INSTANT \_ MESSENGER3](contact-properties.md)                                      | Optional.                                                                      |
| [\_WPD-KONTAKTNAME \_ DES \_ UNTERNEHMENS](contact-properties.md)                                                  | Optional.                                                                      |
| [WPD \_ CONTACT \_ PHONETIC \_ COMPANY \_ NAME](contact-properties.md)                               | Optional                                                                       |
| [\_WPD-KONTAKTROLLE \_](contact-properties.md)                                                                   | Optional.                                                                      |
| [WPD \_ CONTACT \_ BIRTHDATE](contact-properties.md)                                                         | Optional.                                                                      |
| [WPD \_ CONTACT \_ PRIMARY \_ FAX](contact-properties.md)                                                                            | Optional.                                                                      |
| [\_WPD-KONTAKTKONTAKT \_](contact-properties.md)                                                                                  | Optional.                                                                      |
| [WPD \_ CONTACT \_ CHILDREN](contact-properties.md)                                                                                | Optional.                                                                      |
| [WPD \_ CONTACT \_ ASSISTANT](contact-properties.md)                                                                               | Optional.                                                                      |
| [WPD \_ CONTACT \_ ANNIVERSARY \_ DATE](contact-properties.md)                                                                       | Optional.                                                                      |
| [WPD \_ CONTACT \_ RINGTONE](contact-properties.md)                                                                                | Optional.                                                                      |
| [WPD \_ – ALLGEMEINE INFORMATIONEN \_ \_ HINWEISE](object-properties.md)                                                                        | Optional.                                                                      |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                                       | Erforderlich oder optional       | Beschreibung                        |
|---------------------------------------------------------------------|----------------------------|------------------------------------|
| [**WPD \_ RESOURCE \_ DEFAULT**](wpd-resource-default.md)              | Optional.                  | Enthält die Kontaktdaten.         |
| [**WPD \_ RESOURCE \_ CONTACT \_ PHOTO**](wpd-resource-contact-photo.md) | Empfohlen, falls verfügbar. | Enthält ein Bild des Kontakts. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



