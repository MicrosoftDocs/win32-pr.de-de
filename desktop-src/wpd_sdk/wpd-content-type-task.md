---
description: '\_ \_ WPD-INHALTSTYPTASK \_'
ms.assetid: 503d0b11-2113-4df4-8b6b-250f24d09b1f
title: WPD_CONTENT_TYPE_TASK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6823a6707cac184ca5e04eda90a036f39f7b89a8
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424320"
---
# <a name="wpd_content_type_task"></a>\_ \_ WPD-INHALTSTYPTASK \_

Ein Objekt, das seinen Typ als WPD \_ CONTENT \_ TYPE TASK \_ beschreibt, stellt eine Aufgabe dar, z. B. ein Element in einer Aufgabenliste.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



| Eigenschaftsname       | Erforderlich oder optional         |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [\_ \_ WPD-OBJEKT-ID](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zur Erstellungszeit nicht festlegen. |
| [ÜBERGEORDNETE \_ \_ \_ WPD-OBJEKT-ID](object-properties.md)                                                 | Erforderlich.                                                                      |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                            | Erforderlich, wenn das -Objekt eine Datei darstellt.                                      |
| [\_PERSISTENTE EINDEUTIGE ID DES \_ \_ \_ WPD-OBJEKTS](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zur Erstellungszeit nicht festlegen. |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                        | Erforderlich.                                                                      |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                           | Erforderlich.                                                                      |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                              |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).          |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                              |
| [\_WPD-OBJEKT \_ \_ URSPRÜNGLICHER \_ DATEINAME](object-properties.md)                              | Erforderlich, wenn das -Objekt eine Datei darstellt.                                      |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.          |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                | Erforderlich, wenn das -Objekt Verweise auf andere Objekte enthält.                        |
| [\_WPD-OBJEKTSCHLÜSSELWÖRTER \_](object-properties.md)                                                    | Dies ist optional.                                                                      |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                     | Dies ist optional.                                                                      |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                  | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt ist.                         |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                           | Dies ist optional.                                                                      |
| [\_WPD-OBJEKTDATUM \_ \_ GEÄNDERT](object-properties.md)                                         | Empfohlen.                                                                   |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Dies ist optional.                                                                      |
| [WPD \_ OBJECT BACK REFERENCES (WPD-OBJEKTVERWEISE \_ \_ ZURÜCK)](object-properties.md)                                                                | Wird empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.                     |
| [\_ \_ WPD-OBJEKTCONTAINER \_ FUNKTIONALE \_ \_ OBJEKT-ID](object-properties.md)     | Dies ist optional.                                                                      |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHT AUS \_ RESSOURCE](object-properties.md) | Dies ist optional.                                                                      |
| [\_WPD-OBJEKT \_ KANN GELÖSCHT \_ WERDEN](object-properties.md)                                                                     | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                      |
| [\_GEBIETSSCHEMA DER WPD-OBJEKTSPRACHE \_ \_](object-properties.md)                                                                | Dies ist optional.                                                                      |
| [WPD \_ COMMON \_ INFORMATION \_ SUBJECT](object-properties.md)                                                            | Erforderlich.                                                                      |
| [WPD \_ COMMON \_ INFORMATION \_ BODY \_ TEXT](object-properties.md)                                                         | Empfohlen.                                                                   |
| [WPD \_ COMMON \_ INFORMATION \_ PRIORITY](object-properties.md)                                                           | Empfohlen.                                                                   |
| [WPD \_ COMMON \_ INFORMATION \_ START \_ DATETIME](object-properties.md)                                                    | Empfohlen.                                                                   |
| [WPD \_ COMMON \_ INFORMATION \_ END \_ DATETIME](object-properties.md)                                                      | Empfohlen.                                                                   |
| [\_WPD – ALLGEMEINE \_ \_ INFORMATIONSHINWEISE](object-properties.md)                                                              | Dies ist optional.                                                                      |
| [\_WPD-AUFGABENSTATUS \_](task-properties.md)                                                              | Dies ist optional.                                                                      |
| [\_WPD-AUFGABE \_ IN PROZENT \_ ABGESCHLOSSEN](task-properties.md)                                         | Dies ist optional.                                                                      |
| [ERINNERUNGSDATUM DES WPD-TASKS \_ \_ \_](task-properties.md)                                               | Dies ist optional.                                                                      |
| [\_WPD-AUFGABENBESITZER \_](task-properties.md)                                                                | Dies ist optional.                                                                      |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte hosten in der Regel keine Ressourcen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



