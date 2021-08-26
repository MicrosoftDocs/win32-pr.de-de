---
description: '\_ \_ \_ WPD-INHALTSTYPABSCHNITT'
ms.assetid: 8680a74b-9594-4271-a511-637f617aa12a
title: WPD_CONTENT_TYPE_SECTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be521313b2401166e4af1be06bf0e5bbe611de3a247a202177d7564f0c759bc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927700"
---
# <a name="wpd_content_type_section"></a>\_ \_ \_ WPD-INHALTSTYPABSCHNITT

Ein Objekt, das seinen Typ als WPD CONTENT TYPE SECTION beschreibt, stellt einen Datenabschnitt \_ \_ \_ dar, der in einem anderen -Objekt enthalten ist. Beispielsweise kann eine große Audiodatei als Sammlung mehrerer Kapitel beschrieben werden, und jedes Kapitel kann ein WPD \_ CONTENT \_ TYPE \_ SECTION-Objekt sein.

Die WPD \_ OBJECT \_ REFERENCES-Eigenschaft identifiziert das übergeordnete Objekt eines bestimmten Abschnitts.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



| Eigenschaftsname       | Erforderlich oder optional             |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [\_WPD-OBJEKT-ID \_](object-properties.md)                                                                           | Erforderlich.                                                             |
| [ÜBERGEORDNETE ID DES \_ \_ WPD-OBJEKTS \_](object-properties.md)                                                            | Erforderlich.                                                             |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                                       | Erforderlich, wenn das -Objekt eine Datei darstellt.                             |
| [PERSISTENTE EINDEUTIGE ID \_ DES WPD-OBJEKTS \_ \_ \_](object-properties.md)                                     | Erforderlich.                                                             |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                                   | Erforderlich.                                                             |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                                      | Erforderlich.                                                             |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                               | Erforderlich, wenn das Objekt ausgeblendet ist.                                     |
| [\_WPD-OBJEKT \_ ISSYSTEM](object-properties.md)                                                               | Erforderlich, wenn das -Objekt ein Systemobjekt ist (stellt eine Systemdatei dar). |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                                       | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                     |
| [\_WPD-OBJEKT \_ \_ URSPRÜNGLICHER \_ DATEINAME](object-properties.md)                                         | Erforderlich, wenn das -Objekt eine Datei darstellt.                             |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                                  | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist. |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                           | Erforderlich, wenn das -Objekt Verweise auf andere Objekte enthält.               |
| [\_WPD-OBJEKTSCHLÜSSELWÖRTER \_](object-properties.md)                                                               | Optional.                                                             |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                                | Optional.                                                             |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                             | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt ist.                |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                                      | Optional.                                                             |
| [\_WPD-OBJEKTDATUM \_ \_ GEÄNDERT](object-properties.md)                                                    | Empfohlen.                                                          |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                                    | Optional.                                                             |
| [WPD \_ OBJECT BACK REFERENCES (WPD-OBJEKTVERWEISE \_ \_ ZURÜCK)](object-properties.md)                                                | Wird empfohlen, wenn das -Objekt Verweise auf andere Objekte enthält.            |
| [\_ \_ WPD-OBJEKTCONTAINER \_ FUNKTIONALE \_ \_ OBJEKT-ID](object-properties.md)                | Optional.                                                             |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHT AUS \_ RESSOURCE](object-properties.md)            | Optional.                                                             |
| [\_WPD-OBJEKT \_ KANN LÖSCHEN \_](object-properties.md)                                                          | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                             |
| [WPD \_ OBJECT \_ LANGUAGE \_ LOCALE](object-properties.md)                                                                           | Optional.                                                             |
| [\_WPD-ABSCHNITT \_ – \_ DATENOFFSET](section-attribute-properties.md)                                           | Erforderlich.                                                             |
| [\_WPD-ABSCHNITT \_ – \_ DATENLÄNGE](section-attribute-properties.md)                                           | Erforderlich.                                                             |
| [\_ \_ WPD-ABSCHNITTSDATENEINHEITEN \_](section-attribute-properties.md)                                             | Empfohlen.                                                          |
| [\_WPD-ABSCHNITTSDATEN, \_ \_ AUF DIE \_ OBJEKTRESSOURCE VERWIESEN \_ WIRD](section-attribute-properties.md) | Empfohlen.                                                          |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte hosten in der Regel keine Ressourcen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



