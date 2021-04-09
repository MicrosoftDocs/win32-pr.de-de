---
description: Abschnitt zum WPD- \_ \_ Inhaltstyp \_
ms.assetid: 8680a74b-9594-4271-a511-637f617aa12a
title: WPD_CONTENT_TYPE_SECTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fbb63821f75115c5855653dc811067891652615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050326"
---
# <a name="wpd_content_type_section"></a>Abschnitt zum WPD- \_ \_ Inhaltstyp \_

Ein Objekt, das den Typ als WPD \_ - \_ Inhaltstyp Abschnitt beschreibt, \_ stellt einen Abschnitt von Daten dar, der in einem anderen Objekt enthalten ist. Beispielsweise kann eine große Audiodatei als eine Sammlung mehrerer Kapitel beschrieben werden, und jedes Kapitel kann ein WPD- \_ \_ Inhaltstyp- \_ Abschnitts Objekt sein.

Die WPD \_ \_ -Objekt Verweis Eigenschaft identifiziert das übergeordnete Objekt eines angegebenen Abschnitts.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



|                                                                                                                                  |                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| **Eigenschaftenname**                                                                                                                | **Erforderlich oder optional**                                              |
| [WPD- \_ Objekt- \_ ID](object-properties.md)                                                                           | Erforderlich.                                                             |
| [übergeordnete WPD- \_ Objekt- \_ \_ ID](object-properties.md)                                                            | Erforderlich.                                                             |
| [WPD- \_ Objekt \_ Name](object-properties.md)                                                                       | Erforderlich, wenn das-Objekt eine Datei darstellt.                             |
| [\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](object-properties.md)                                     | Erforderlich.                                                             |
| [WPD- \_ Objekt \_ Format](object-properties.md)                                                                   | Erforderlich.                                                             |
| [Inhaltstyp für WPD- \_ Objekt \_ \_](object-properties.md)                                                      | Erforderlich.                                                             |
| [WPD- \_ Objekt \_ IsHidden](object-properties.md)                                                               | Erforderlich, wenn das Objekt ausgeblendet ist.                                     |
| [WPD- \_ Objekt \_ IsSystem](object-properties.md)                                                               | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar). |
| [WPD- \_ Objekt \_ Größe](object-properties.md)                                                                       | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                     |
| [\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts](object-properties.md)                                         | Erforderlich, wenn das-Objekt eine Datei darstellt.                             |
| [WPD- \_ Objekt \_ nicht \_ verwendbar](object-properties.md)                                                  | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist. |
| [Verweise auf WPD- \_ Objekte \_](object-properties.md)                                                           | Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.               |
| [WPD- \_ Objekt \_ Schlüsselwörter](object-properties.md)                                                               | Dies ist optional.                                                             |
| [WPD- \_ Objekt \_ Synchronisierungs- \_ ID](object-properties.md)                                                                | Dies ist optional.                                                             |
| [WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt](object-properties.md)                                             | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.                |
| [\_ \_ Erstellungsdatum des WPD-Objekts \_](object-properties.md)                                                      | Dies ist optional.                                                             |
| [Datum des WPD- \_ Objekts \_ \_ geändert](object-properties.md)                                                    | Empfohlen.                                                          |
| [erstelltes WPD- \_ Objekt \_ Datum \_](object-properties.md)                                                    | Dies ist optional.                                                             |
| [\_ \_ zurück \_ Verweise auf WPD-Objekte](object-properties.md)                                                | Wird empfohlen, wenn das Objekt Verweise auf andere Objekte hat.            |
| [\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers](object-properties.md)                | Dies ist optional.                                                             |
| [WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource](object-properties.md)            | Dies ist optional.                                                             |
| [WPD- \_ Objekt \_ kann \_ Löschen](object-properties.md)                                                          | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                             |
| [Gebiets Schema der WPD- \_ Objekt \_ Sprache \_](object-properties.md)                                                                           | Dies ist optional.                                                             |
| [\_ \_ Daten \_ Offset für WPD-Abschnitt](section-attribute-properties.md)                                           | Erforderlich.                                                             |
| [\_ \_ Daten \_ Länge des WPD-Abschnitts](section-attribute-properties.md)                                           | Erforderlich.                                                             |
| [\_ \_ Daten \_ Einheiten für WPD-Abschnitt](section-attribute-properties.md)                                             | Empfohlen.                                                          |
| [\_ \_ \_ referenzierte \_ Objekt \_ Ressource für WPD-Abschnitts Daten](section-attribute-properties.md) | Empfohlen.                                                          |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte Hosten in der Regel keine Ressourcen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



