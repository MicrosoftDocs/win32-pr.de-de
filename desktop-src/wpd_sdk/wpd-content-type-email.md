---
description: e-Mail zum WPD \_ \_ -Inhaltstyp \_
ms.assetid: 96f81477-5ec9-49c1-987a-348a92a7e638
title: WPD_CONTENT_TYPE_EMAIL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0cb274fdd4b4e9bd3e4d02d20afeda1ef871143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529819"
---
# <a name="wpd_content_type_email"></a>e-Mail zum WPD \_ \_ -Inhaltstyp \_

Ein Objekt, das den Typ beschreibt, als WPD \_ \_ -Inhaltstyp \_ -e-Mail eine e-Mail darstellt.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



| Eigenschaftsname                                                                                                         | Erforderlich oder optional                                                           |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [WPD- \_ Objekt- \_ ID](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen. |
| [übergeordnete WPD- \_ Objekt- \_ \_ ID](object-properties.md)                                                 | Erforderlich.                                                                      |
| [WPD- \_ Objekt \_ Name](object-properties.md)                                                            | Erforderlich, wenn das-Objekt eine Datei darstellt.                                      |
| [\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen. |
| [WPD- \_ Objekt \_ Format](object-properties.md)                                                        | Erforderlich.                                                                      |
| [Inhaltstyp für WPD- \_ Objekt \_ \_](object-properties.md)                                           | Erforderlich.                                                                      |
| [WPD- \_ Objekt \_ IsHidden](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                              |
| [WPD- \_ Objekt \_ IsSystem](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).          |
| [WPD- \_ Objekt \_ Größe](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                              |
| [\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts](object-properties.md)                              | Erforderlich, wenn das-Objekt eine Datei darstellt.                                      |
| [WPD- \_ Objekt \_ nicht \_ verwendbar](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.          |
| [Verweise auf WPD- \_ Objekte \_](object-properties.md)                                                | Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.                        |
| [WPD- \_ Objekt \_ Schlüsselwörter](object-properties.md)                                                    | Dies ist optional.                                                                      |
| [WPD- \_ Objekt \_ Synchronisierungs- \_ ID](object-properties.md)                                                     | Dies ist optional.                                                                      |
| [WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt](object-properties.md)                                  | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.                         |
| [\_ \_ Erstellungsdatum des WPD-Objekts \_](object-properties.md)                                           | Dies ist optional.                                                                      |
| [Datum des WPD- \_ Objekts \_ \_ geändert](object-properties.md)                                         | Empfohlen.                                                                   |
| [erstelltes WPD- \_ Objekt \_ Datum \_](object-properties.md)                                         | Dies ist optional.                                                                      |
| [\_ \_ zurück \_ Verweise auf WPD-Objekte](object-properties.md)                                                                | Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.                     |
| [\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers](object-properties.md)     | Dies ist optional.                                                                      |
| [WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource](object-properties.md) | Dies ist optional.                                                                      |
| [WPD- \_ Objekt \_ kann \_ Löschen](object-properties.md)                                                                     | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                      |
| [häufig verwendeter WPD- \_ \_ Informations \_ Betreff](object-properties.md)                                                            | Erforderlich.                                                                      |
| [Text für den allgemeinen WPD- \_ \_ Informations \_ \_ Text](object-properties.md)                                                         | Empfohlen.                                                                   |
| [Allgemeine WPD- \_ \_ Informations \_ Priorität](object-properties.md)                                                           | Empfohlen.                                                                   |
| [Gebiets Schema der WPD- \_ Objekt \_ Sprache \_](object-properties.md)                                                                | Dies ist optional.                                                                      |
| [WPD \_ -e-Mail \_ an \_ Zeile](email-properties.md)                                                        | Erforderlich.                                                                      |
| [WPD \_ -e-Mail- \_ \_ Leitung](email-properties.md)                                                        | Dies ist optional.                                                                      |
| [WPD \_ -e-Mail \_ Bcc- \_ Zeile](email-properties.md)                                                      | Dies ist optional.                                                                      |
| [WPD \_ -e-Mail \_ \_ wurde \_ gelesen](email-properties.md)                                           | Dies ist optional.                                                                      |
| [\_empfangene WPD-e-Mail \_ \_](email-properties.md)                                            | Dies ist optional.                                                                      |
| [WPD \_ -e-Mail \_ enthält \_ Anlagen](email-properties.md)                                        | Dies ist optional.                                                                      |
| [WPD \_ -e-Mail \_ \_](email-properties.md)                                          | Erforderlich.                                                                      |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte Hosten in der Regel keine Ressourcen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



