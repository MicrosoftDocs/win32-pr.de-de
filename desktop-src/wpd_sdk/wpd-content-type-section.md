---
description: '\_ \_ \_ WPD-INHALTSTYPABSCHNITT'
ms.assetid: 8680a74b-9594-4271-a511-637f617aa12a
title: WPD_CONTENT_TYPE_SECTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84294ff9949418ecc12f55472da202dddcc8f06c
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423780"
---
# <a name="wpd_content_type_section"></a>\_ \_ \_ WPD-INHALTSTYPABSCHNITT

Ein Objekt, das seinen Typ als WPD \_ CONTENT \_ TYPE SECTION \_ beschreibt, stellt einen Datenabschnitt dar, der in einem anderen Objekt enthalten ist. Beispielsweise kann eine große Audiodatei als Eine Sammlung mehrerer Kapitel beschrieben werden, und jedes Kapitel kann ein WPD \_ CONTENT \_ TYPE \_ SECTION-Objekt sein.

Die WPD \_ OBJECT \_ REFERENCES-Eigenschaft identifiziert das übergeordnete Objekt eines bestimmten Abschnitts.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



| Eigenschaftsname       | Erforderlich oder optional             |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [\_ \_ WPD-OBJEKT-ID](object-properties.md)                                                                           | Erforderlich.                                                             |
| [ÜBERGEORDNETE \_ \_ \_ WPD-OBJEKT-ID](object-properties.md)                                                            | Erforderlich.                                                             |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                                       | Erforderlich, wenn das -Objekt eine Datei darstellt.                             |
| [\_PERSISTENTE EINDEUTIGE ID DES \_ \_ \_ WPD-OBJEKTS](object-properties.md)                                     | Erforderlich.                                                             |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                                   | Erforderlich.                                                             |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                                      | Erforderlich.                                                             |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                               | Erforderlich, wenn das Objekt ausgeblendet ist.                                     |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                               | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar). |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                                       | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                     |
| [\_WPD-OBJEKT \_ \_ URSPRÜNGLICHER \_ DATEINAME](object-properties.md)                                         | Erforderlich, wenn das -Objekt eine Datei darstellt.                             |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                                  | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist. |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                           | Erforderlich, wenn das -Objekt Verweise auf andere Objekte enthält.               |
| [\_WPD-OBJEKTSCHLÜSSELWÖRTER \_](object-properties.md)                                                               | Dies ist optional.                                                             |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                                | Dies ist optional.                                                             |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                             | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt ist.                |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                                      | Dies ist optional.                                                             |
| [\_WPD-OBJEKTDATUM \_ \_ GEÄNDERT](object-properties.md)                                                    | Empfohlen.                                                          |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                                    | Dies ist optional.                                                             |
| [WPD \_ OBJECT BACK REFERENCES (WPD-OBJEKTVERWEISE \_ \_ ZURÜCK)](object-properties.md)                                                | Wird empfohlen, wenn das -Objekt Verweise auf andere Objekte enthält.            |
| [\_ \_ WPD-OBJEKTCONTAINER \_ FUNKTIONALE \_ \_ OBJEKT-ID](object-properties.md)                | Dies ist optional.                                                             |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHT AUS \_ RESSOURCE](object-properties.md)            | Dies ist optional.                                                             |
| [\_WPD-OBJEKT \_ KANN LÖSCHEN \_](object-properties.md)                                                          | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                             |
| [\_GEBIETSSCHEMA DER WPD-OBJEKTSPRACHE \_ \_](object-properties.md)                                                                           | Dies ist optional.                                                             |
| [\_DATENOFFSET DES WPD-ABSCHNITTS \_ \_](section-attribute-properties.md)                                           | Erforderlich.                                                             |
| [\_DATENLÄNGE DES WPD-ABSCHNITTS \_ \_](section-attribute-properties.md)                                           | Erforderlich.                                                             |
| [\_DATENEINHEITEN IM WPD-ABSCHNITT \_ \_](section-attribute-properties.md)                                             | Empfohlen.                                                          |
| [OBJEKTRESSOURCE IM \_ WPD-ABSCHNITTSDATENVERWEIS \_ \_ \_ \_](section-attribute-properties.md) | Empfohlen.                                                          |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte hosten in der Regel keine Ressourcen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



