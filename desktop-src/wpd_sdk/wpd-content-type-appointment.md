---
description: WPD \_ - \_ Inhaltstyp \_ Termin
ms.assetid: d41c26ef-9f51-4ba7-b1a4-57abec91925e
title: WPD_CONTENT_TYPE_APPOINTMENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b1ec4a316690241372bc7d0fa13789731dde925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349610"
---
# <a name="wpd_content_type_appointment"></a>WPD \_ - \_ Inhaltstyp \_ Termin

Ein Objekt, das seinen Typ als WPD \_ - \_ Inhaltstyp Termin beschreibt, \_ stellt einen Termin in einem Kalender dar.

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
| [WPD- \_ Termin \_ Speicherort](appointment-properties.md)                                     | Erforderlich.                                                                      |
| [WPD- \_ Objekt \_ kann \_ Löschen](object-properties.md)                                                                     | Erforderlich, wenn das Objekt gelöscht werden kann.                                         |
| [Gebiets Schema der WPD- \_ Objekt \_ Sprache \_](object-properties.md)                                                                | Dies ist optional.                                                                      |
| [häufig verwendeter WPD- \_ \_ Informations \_ Betreff](object-properties.md)                                                            | Erforderlich.                                                                      |
| [Text für den allgemeinen WPD- \_ \_ Informations \_ \_ Text](object-properties.md)                                                         | Empfohlen.                                                                   |
| [Allgemeine WPD- \_ \_ Informations \_ Priorität](object-properties.md)                                                           | Empfohlen.                                                                   |
| [WPD- \_ allgemeine \_ Informationen \_ Start \_ DateTime](object-properties.md)                                                    | Empfohlen.                                                                   |
| [DateTime-Wert für WPD- \_ allgemeine \_ Informationen \_ \_](object-properties.md)                                                      | Empfohlen.                                                                   |
| [\_Allgemeine Informationen zu \_ WPD \_](object-properties.md)                                                              | Dies ist optional.                                                                      |
| [WPD- \_ Termin \_ Speicherort](object-properties.md)                                                                   | Erforderlich.                                                                      |
| [WPD \_ - \_ ereigtentyp](appointment-properties.md)                                             | Dies ist optional.                                                                      |
| [für WPD- \_ Termin \_ erforderliche \_ Teilnehmer](appointment-properties.md)                | Dies ist optional.                                                                      |
| [\_ \_ optionale \_ Teilnehmer für WPD-Termin](appointment-properties.md)                | Dies ist optional.                                                                      |
| [der WPD- \_ Termin \_ akzeptierte \_ Teilnehmer](appointment-properties.md)                | Dies ist optional.                                                                      |
| [WPD- \_ Termin \_ Ressourcen](appointment-properties.md)                                   | Dies ist optional.                                                                      |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte Hosten in der Regel keine Ressourcen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



