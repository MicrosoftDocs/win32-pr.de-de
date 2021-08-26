---
title: SVG-Unterstützung
description: Ab Windows 10 Anniversary Update unterstützt Direct2D das Rendern von Farbschriftarten, die SVG-Glyphengliederungen enthalten, wie in der OpenType-Spezifikation beschrieben (siehe Tabelle "SVG").
ms.assetid: 5cb4cb7c-9b96-e110-bff9-d75ad1980010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8c5f34531264f95c3617d1324079895b6444cbdbc776d5468fe51fc9890992
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917100"
---
# <a name="svg-support"></a>SVG-Unterstützung

Ab Windows 10 Anniversary Update unterstützt Direct2D das Rendern von [Farbschriftarten,](../directwrite/color-fonts.md) die SVG-Glyphengliederungen enthalten, wie in der [OpenType-Spezifikation](/typography/opentype/spec/) beschrieben (siehe [Die SVG-Tabelle](/typography/opentype/spec/svg)). Ab Windows 10 Creators Update unterstützt Direct2D auch das Rendern eigenständiger SVG-Bilder. Bestimmte SVG-Features sind in OpenType-SVG-Schriftarten jedoch nicht zulässig, und bestimmte SVG-Features werden derzeit von Direct2D nicht unterstützt.  

In diesem Thema werden die [SVG 1.1-Features](https://www.w3.org/TR/SVG11/) beschrieben, die von Direct2D in Windows 10 Anniversary Update und neuer unterstützt werden. Dieses Dokument gilt für SVG in OpenType-Schriftarten sowie für eigenständige SVG-Images.

## <a name="supported-svg-elements-and-attributes"></a>Unterstützte SVG-Elemente und -Attribute

Direct2D unterstützt das Rendern der folgenden SVG-Elemente und der zugeordneten Attribute für jedes Element. Andere Elemente und reguläre Attribute werden ignoriert.



| Element                                                                                  | Unterstützte reguläre Attribute                                                             |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Kreis](https://www.w3.org/TR/SVG11/shapes.mdl#circleelement)                           | id, style, transform, cx, cy, r                                                          |
| [clipPath](https://www.w3.org/TR/SVG11/masking.mdl#clippathelement)                      | id, style, transform, clipPathUnits                                                      |
| [Defs](https://www.w3.org/TR/SVG11/struct.mdl#defselement)                               | id, style, transform                                                                     |
| [Desc](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup>  | id                                                                                       |
| [ellipse](https://www.w3.org/TR/SVG11/shapes.mdl#ellipseelement)                         | id, style, transform, cx, cy, rx, ry                                                     |
| [g](https://www.w3.org/TR/SVG11/struct.mdl#gelement)                                     | id, style, transform                                                                     |
| [image](https://www.w3.org/TR/SVG11/struct.mdl#imageelement)                             | id, style, transform, x, y, width, height, preserveAspectRatio, xlink:href               |
| [Linie](https://www.w3.org/TR/SVG11/shapes.mdl#lineelement)                               | id, style, transform, x1, y1, x2, y2                                                     |
| [linearGradient](https://www.w3.org/TR/SVG11/pservers.mdl#lineargradientelement)         | id, style, x1, y1, x2, y2, gradientUnits, gradientTransform, spreadMethod, xlink:href    |
| [path](https://www.w3.org/TR/SVG11/paths.mdl#pathelement)                                | id, style, transform, d                                                                  |
| [Polygon](https://www.w3.org/TR/SVG11/shapes.mdl#polygonelement)                         | id, style, transform, points                                                             |
| [Polylinie](https://www.w3.org/TR/SVG11/shapes.mdl#polylineelement)                       | id, style, transform, points                                                             |
| [radialGradient](https://www.w3.org/TR/SVG11/pservers.mdl#radialgradientelement)         | id, style, cx, cy, r, fx, fy, gradientUnits, gradientTransform, spreadMethod, xlink:href |
| [Rect](https://www.w3.org/TR/SVG11/shapes.mdl#rectelement)                               | id, style, transform, x, y, width, height, rx, ry                                        |
| [stop](https://www.w3.org/TR/SVG11/pservers.mdl#stopelement)                             | id, style, offset                                                                        |
| [Svg](https://www.w3.org/TR/SVG11/struct.mdl#svgelement)                                 | id, style, x, y, width, height, viewBox, preserveAspectRatio                             |
| [Titel](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup> | id                                                                                       |
| [use](https://www.w3.org/TR/SVG11/struct.mdl#useelement)                                 | id, style, transform, x, y, width, height, xlink:href                                    |



 

<sup>\*</sup>Nur in Windows 10 Creators Update und neueren Versionen unterstützt

## <a name="supported-svg-presentation-attributes"></a>Unterstützte SVG-Präsentationsattribute

Direct2D unterstützt auch die folgenden Präsentationsattribute. Diese können für alle SVG-Elemente angegeben werden, wirken sich jedoch nur auf die Darstellung bestimmter Elemente aus, wie in der SVG-Spezifikation beschrieben (siehe [Präsentationsattribute](https://www.w3.org/TR/SVG11/attindex.mdl#presentationattributes)).

-   Clippfad
-   Clip-Rule
-   color
-   Anzeigen<sup>\*</sup>
-   fill
-   Fill-Opacity
-   fill-rule
-   Durchlässigkeit
-   Überlauf
-   Stop-Color
-   stop-opacity
-   stroke
-   stroke-dasharray
-   stroke-dasstrichset
-   stroke-linecap
-   stroke-linejoin
-   stroke-miterlimit
-   Strichdurchlässigkeit
-   Strichbreite
-   Sichtbarkeit<sup>\*</sup>

<sup>\*</sup>Nur in Windows 10 Creators Update und neueren Versionen unterstützt

## <a name="unsupported-svg-features"></a>Nicht unterstützte SVG-Features

### <a name="unsupported-elements-and-attributes"></a>Nicht unterstützte Elemente und Attribute

Alle Elemente oder Attribute, die nicht in den obigen Listen enthalten sind, werden von Direct2D als nicht unterstützt betrachtet. Beim Analysieren von SVG-Inhalt, der ein nicht unterstütztes Element oder Attribut enthält, wird die nicht unterstützte Entität ignoriert. Der Rest des Inhalts wird so mäßig wie möglich gerendert.

### <a name="unsupported-length-units"></a>Nicht unterstützte Längeneinheiten

Ab Windows 10 Anniversary Update unterstützt Direct2D nur Werte für die Länge des Benutzerbereichs und Prozentwerte. Längen mit Einheitensuffixen wie "mm" oder "em" werden nicht unterstützt.

Ab Windows 10 Fall Creators Update unterstützt Direct2D auch absolute Einheitenbezeichner: px, pt, pc, cm, mm und in. Relative Einheitenbezeichner (em, ex) werden nicht unterstützt.

### <a name="unsupported-image-sources"></a>Nicht unterstützte Bildquellen

Das Imageelement wird nur unterstützt, wenn sein xlink:href-Attribut auf ein Base64-codiertes Bild festgelegt ist. Remoteverweise werden nicht unterstützt.

 

 