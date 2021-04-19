---
description: Kontakt zum WPD- \_ \_ Inhaltstyp \_
ms.assetid: 3ff6191f-d3c0-4bd3-946e-c3fbf68f368c
title: WPD_CONTENT_TYPE_CONTACT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fed10e0abb36a482141e5c796f5494b00b99f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351438"
---
# <a name="wpd_content_type_contact"></a>Kontakt zum WPD- \_ \_ Inhaltstyp \_

Ein-Objekt, das den Typ als WPD- \_ \_ Inhaltstyp Kontakt beschreibt, \_ stellt persönliche Kontaktdaten dar.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



| Eigenschaftsname                                                                                                                   | Erforderlich oder optional                                                           |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [WPD- \_ Objekt- \_ ID](object-properties.md)                                                                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen. |
| [übergeordnete WPD- \_ Objekt- \_ \_ ID](object-properties.md)                                                           | Erforderlich.                                                                      |
| [WPD- \_ Objekt \_ Name](object-properties.md)                                                                      | Erforderlich, wenn das-Objekt eine Datei darstellt.                                      |
| [\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](object-properties.md)                                    | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen. |
| [WPD- \_ Objekt \_ Format](object-properties.md)                                                                  | Erforderlich.                                                                      |
| [Inhaltstyp für WPD- \_ Objekt \_ \_](object-properties.md)                                                     | Erforderlich.                                                                      |
| [WPD- \_ Objekt \_ IsHidden](object-properties.md)                                                              | Erforderlich, wenn das Objekt ausgeblendet ist.                                              |
| [WPD- \_ Objekt \_ IsSystem](object-properties.md)                                                              | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).          |
| [WPD- \_ Objekt \_ Größe](object-properties.md)                                                                      | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                              |
| [\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts](object-properties.md)                                        | Erforderlich, wenn das-Objekt eine Datei darstellt.                                      |
| [WPD- \_ Objekt \_ nicht \_ verwendbar](object-properties.md)                                                 | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.          |
| [Verweise auf WPD- \_ Objekte \_](object-properties.md)                                                          | Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.                        |
| [WPD- \_ Objekt \_ Schlüsselwörter](object-properties.md)                                                              | Dies ist optional.                                                                      |
| [WPD- \_ Objekt \_ Synchronisierungs- \_ ID](object-properties.md)                                                               | Dies ist optional.                                                                      |
| [WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt](object-properties.md)                                            | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.                         |
| [\_ \_ Erstellungsdatum des WPD-Objekts \_](object-properties.md)                                                     | Dies ist optional.                                                                      |
| [Datum des WPD- \_ Objekts \_ \_ geändert](object-properties.md)                                                   | Empfohlen.                                                                   |
| [erstelltes WPD- \_ Objekt \_ Datum \_](object-properties.md)                                                   | Dies ist optional.                                                                      |
| [\_ \_ zurück \_ Verweise auf WPD-Objekte](object-properties.md)                                                                          | Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.                     |
| [\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers](object-properties.md)               | Dies ist optional.                                                                      |
| [WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource](object-properties.md)           | Dies ist optional.                                                                      |
| [\_ \_ Anzeige \_ Name des WPD-Kontakts](contact-properties.md)                                                  | Erforderlich.                                                                      |
| [WPD- \_ Objekt \_ kann \_ Löschen](object-properties.md)                                                                               | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                      |
| [Gebiets Schema der WPD- \_ Objekt \_ Sprache \_](object-properties.md)                                                                          | Dies ist optional.                                                                      |
| [\_ \_ Anzeige \_ Name des WPD-Kontakts](contact-properties.md)                                                                           | Erforderlich.                                                                      |
| [Vorname des WPD- \_ Kontakts \_ \_](contact-properties.md)                                                      | Empfohlen.                                                                   |
| [WPD- \_ Kontakt- \_ Middle- \_ Namen](contact-properties.md)                                                  | Empfohlen.                                                                   |
| [Nachname des WPD- \_ Kontakts \_ \_](contact-properties.md)                                                        | Empfohlen.                                                                   |
| [WPD- \_ Kontakt \_ Präfix](contact-properties.md)                                                               | Empfohlen.                                                                   |
| [WPD- \_ Kontakt \_ Suffix](contact-properties.md)                                                               | Empfohlen.                                                                   |
| [WPD- \_ Kontakt \_ Phonetic- \_ Vorname \_](contact-properties.md)                                   | Dies ist optional.                                                                      |
| [\_ \_ phonetischer \_ Nachname für WPD-Kontakt \_](contact-properties.md)                                     | Dies ist optional.                                                                      |
| [\_ \_ persönliche \_ vollständige \_ Post \_ Anschrift für WPD-Kontakt](contact-properties.md)                | Empfohlen.                                                                   |
| [WPD \_ Contact \_ private \_ Postal \_ Address \_ Zeile 1](contact-properties.md)              | Dies ist optional.                                                                      |
| [WPD \_ Contact \_ private \_ Postal \_ Address \_ Zeile 2](contact-properties.md)              | Dies ist optional.                                                                      |
| [WPD \_ Contact \_ private \_ Postal \_ Address \_ City](contact-properties.md)                | Dies ist optional.                                                                      |
| [\_ \_ persönliche \_ Post \_ Adress \_ Region für WPD-Kontakt](contact-properties.md)            | Dies ist optional.                                                                      |
| [WPD \_ Contact \_ private \_ Postal \_ Address \_ Postal \_ Code](contact-properties.md) | Dies ist optional.                                                                      |
| [WPD \_ Contact \_ private \_ Postal \_ Address \_ Land](contact-properties.md)          | Dies ist optional.                                                                      |
| [WPD \_ Contact \_ Business \_ Full \_ Postal \_ Address](contact-properties.md)                | Dies ist optional.                                                                      |
| [WPD \_ Contact \_ Business \_ Postal \_ Address \_ Zeile 1](contact-properties.md)              | Dies ist optional.                                                                      |
| [WPD \_ Contact \_ Business \_ Postal \_ Address \_ Zeile 2](contact-properties.md)              | Dies ist optional.                                                                      |
| [WPD \_ Contact \_ Business \_ Postal \_ Address \_ City](contact-properties.md)                | Dies ist optional.                                                                      |
| [WPD- \_ Kontakt \_ Region "Business \_ Postal \_ Address \_ "](contact-properties.md)            | Dies ist optional.                                                                      |
| [Postleitzahl für WPD- \_ Kontakt \_ \_ Post \_ Anschrift \_ \_](contact-properties.md) | Dies ist optional.                                                                      |
| [WPD \_ Contact \_ Business \_ Postal \_ Address \_ Land](contact-properties.md)          | Dies ist optional.                                                                      |
| [WPD \_ kontaktiert \_ andere \_ vollständige \_ Post \_ Anschrift](contact-properties.md)                      | Dies ist optional.                                                                      |
| [WPD \_ kontaktiert \_ andere \_ Post \_ Anschrift \_ Zeile 1](contact-properties.md)                    | Dies ist optional.                                                                      |
| [WPD \_ kontaktiert \_ andere \_ Post \_ Anschrift \_ Zeile 2](contact-properties.md)                    | Dies ist optional.                                                                      |
| [WPD \_ kontaktiert \_ andere \_ Post \_ Anschrift \_ City](contact-properties.md)                      | Dies ist optional.                                                                      |
| [WPD- \_ Kontakt \_ andere \_ Post \_ Adress \_ Region](contact-properties.md)                  | Dies ist optional.                                                                      |
| [WPD \_ kontaktiert \_ \_ \_ \_ Postleitzahl für andere Postanschrift \_](contact-properties.md)       | Dies ist optional.                                                                      |
| [WPD \_ kontaktiert \_ andere \_ Post \_ Anschrift \_ Post \_ Country](contact-properties.md) | Dies ist optional.                                                                      |
| [\_ \_ primäre \_ e-Mail- \_ Adresse für WPD](contact-properties.md)                               | Empfohlen.                                                                   |
| [\_ \_ persönliche \_ e-Mail von WPD](contact-properties.md)                                              | Dies ist optional.                                                                      |
| [WPD \_ Contact \_ Personal \_ EMAIL2](contact-properties.md)                                            | Dies ist optional.                                                                      |
| [\_ \_ Geschäfts \_ -e-Mail für WPD](contact-properties.md)                                              | Dies ist optional.                                                                      |
| [WPD \_ Contact \_ Business \_ EMAIL2](contact-properties.md)                                            | Dies ist optional.                                                                      |
| [WPD \_ \_ andere \_ e-Mails kontaktieren](contact-properties.md)                                                  | Dies ist optional.                                                                      |
| [WPD- \_ Kontakt- \_ primär \_ Telefon](contact-properties.md)                                                | Empfohlen.                                                                   |
| [WPD \_ Contact \_ private \_ Phone](contact-properties.md)                                              | Dies ist optional.                                                                      |
| [WPD \_ Contact \_ Personal \_ PHONE2](contact-properties.md)                                            | Dies ist optional.                                                                      |
| [WPD \_ - \_ Kontakt \_ Telefon (geschäftlich)](contact-properties.md)                                              | Dies ist optional.                                                                      |
| [WPD \_ Contact \_ Business \_ PHONE2](contact-properties.md)                                            | Dies ist optional.                                                                      |
| [WPD- \_ Kontakt \_ Mobil \_ Telefon](contact-properties.md)                                                  | Dies ist optional.                                                                      |
| [WPD \_ Contact \_ Mobile \_ PHONE2](contact-properties.md)                                                | Dies ist optional.                                                                      |
| [privates WPD- \_ Kontakt- \_ \_ Fax](contact-properties.md)                                                  | Dies ist optional.                                                                      |
| [WPD \_ Contact- \_ Geschäfts \_ Fax](contact-properties.md)                                                  | Dies ist optional.                                                                      |
| [WPD- \_ Kontakt- \_ Pager](contact-properties.md)                                                                 | Dies ist optional.                                                                      |
| [WPD \_ \_ andere \_ Telefone kontaktieren](contact-properties.md)                                                  | Dies ist optional.                                                                      |
| [\_ \_ primäre \_ \_ Webadresse für WPD-Kontakte](contact-properties.md)                                   | Empfohlen.                                                                   |
| [\_ \_ persönliche \_ \_ Webadresse für WPD-Kontakt](contact-properties.md)                                 | Dies ist optional.                                                                      |
| [Webadresse für WPD- \_ Kontakt \_ geschäftliche \_ \_ Webadresse](contact-properties.md)                                 | Dies ist optional.                                                                      |
| [WPD \_ Contact \_ Instant \_ Messenger](contact-properties.md)                                        | Empfohlen                                                                    |
| [WPD- \_ Kontakt \_ Instant \_ MESSENGER2](contact-properties.md)                                      | Dies ist optional.                                                                      |
| [WPD- \_ Kontakt \_ Instant \_ MESSENGER3](contact-properties.md)                                      | Dies ist optional.                                                                      |
| [\_ \_ Firmen \_ Name für WPD-Kontakt](contact-properties.md)                                                  | Dies ist optional.                                                                      |
| [WPD- \_ Kontakt \_ Phonetic- \_ Firmen \_ Name](contact-properties.md)                               | Optional                                                                       |
| [WPD- \_ Kontakt \_ Rolle](contact-properties.md)                                                                   | Dies ist optional.                                                                      |
| [Geburtsdatum des WPD- \_ Kontakts \_](contact-properties.md)                                                         | Dies ist optional.                                                                      |
| [\_ \_ Primäres Fax für WPD-Kontakt \_](contact-properties.md)                                                                            | Dies ist optional.                                                                      |
| [WPD- \_ Kontakt- \_ Ehepartner](contact-properties.md)                                                                                  | Dies ist optional.                                                                      |
| [WPD-Kontakt untergeordnete Elemente \_ \_](contact-properties.md)                                                                                | Dies ist optional.                                                                      |
| [WPD- \_ Kontakt- \_ Assistent](contact-properties.md)                                                                               | Dies ist optional.                                                                      |
| [Datum der WPD- \_ Kontaktaufnahme \_ \_](contact-properties.md)                                                                       | Dies ist optional.                                                                      |
| [WPD- \_ Kontakt- \_ Rington](contact-properties.md)                                                                                | Dies ist optional.                                                                      |
| [\_Allgemeine Informationen zu \_ WPD \_](object-properties.md)                                                                        | Dies ist optional.                                                                      |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                                       | Erforderlich oder optional       | BESCHREIBUNG                        |
|---------------------------------------------------------------------|----------------------------|------------------------------------|
| [**WPD- \_ Ressourcen \_ Standard**](wpd-resource-default.md)              | Dies ist optional.                  | Enthält die Kontaktdaten.         |
| [**WPD- \_ Ressourcen \_ Kontakt \_ Foto**](wpd-resource-contact-photo.md) | Empfohlen, falls verfügbar. | Enthält ein Bild des Kontakts. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



