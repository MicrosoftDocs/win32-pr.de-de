---
title: SVG-Unterstützung
description: Ab Windows 10 Anniversary Update unterstützt Direct2D renderingfarbschriftarten, die SVG-Symbol Umschriften enthalten, wie in der OpenType-Spezifikation beschrieben (siehe die "SVG"-Tabelle).
ms.assetid: 5cb4cb7c-9b96-e110-bff9-d75ad1980010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678c5d9ef42a53c854bb2f175fac63816345c519
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390363"
---
# <a name="svg-support"></a>SVG-Unterstützung

Ab Windows 10 Anniversary Update unterstützt Direct2D renderingfarbschriftarten, die SVG-Glyphe-Kontur enthalten, wie in der [OpenType-Spezifikation](/typography/opentype/spec/) beschrieben (siehe [SVG-Tabelle](/typography/opentype/spec/svg)). [](../directwrite/color-fonts.md) Ab Windows 10 Creators Update unterstützt Direct2D auch das Rendern eigenständiger SVG-Images. Bestimmte SVG-Features sind innerhalb von OpenType SVG-Schriftarten jedoch nicht zulässig, und bestimmte SVG-Funktionen werden derzeit von Direct2D nicht unterstützt.  

In diesem Thema wird der Satz der [SVG 1,1](https://www.w3.org/TR/SVG11/) -Features beschrieben, die von Direct2D in Windows 10 Anniversary Update und höher unterstützt werden. Dieses Dokument gilt für SVG in OpenType-Schriftarten sowie eigenständige SVG-Images.

## <a name="supported-svg-elements-and-attributes"></a>Unterstützte SVG-Elemente und-Attribute

Direct2D unterstützt das Rendering der folgenden SVG-Elemente und der zugeordneten Attribute für jedes Element. Andere Elemente und reguläre Attribute werden ignoriert.



| Element                                                                                  | Unterstützte reguläre Attribute                                                             |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Kreisen](https://www.w3.org/TR/SVG11/shapes.mdl#circleelement)                           | ID, Stil, Transformation, CX, CY, r                                                          |
| [clipPath](https://www.w3.org/TR/SVG11/masking.mdl#clippathelement)                      | ID, Stil, Transformation, clippathunits                                                      |
| [defs](https://www.w3.org/TR/SVG11/struct.mdl#defselement)                               | ID, Stil, Transformation                                                                     |
| [DESC](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup>  | id                                                                                       |
| [Ellipse](https://www.w3.org/TR/SVG11/shapes.mdl#ellipseelement)                         | ID, Stil, Transformation, CX, CY, RX, Ry                                                     |
| [g](https://www.w3.org/TR/SVG11/struct.mdl#gelement)                                     | ID, Stil, Transformation                                                                     |
| [image](https://www.w3.org/TR/SVG11/struct.mdl#imageelement)                             | ID, Style, Transform, x, y, Width, Height, preserveaspectratio, XLink: href               |
| [line](https://www.w3.org/TR/SVG11/shapes.mdl#lineelement)                               | ID, Style, Transform, x1, Y1, x2, Y2                                                     |
| [LinearGradient](https://www.w3.org/TR/SVG11/pservers.mdl#lineargradientelement)         | ID, Style, x1, Y1, x2, Y2, gradientunits, gradienttransform, SpreadMethod, XLink: href    |
| [path](https://www.w3.org/TR/SVG11/paths.mdl#pathelement)                                | ID, Stil, Transformation, d                                                                  |
| [Polygon](https://www.w3.org/TR/SVG11/shapes.mdl#polygonelement)                         | ID, Stil, Transformation, Punkte                                                             |
| [Polylinie](https://www.w3.org/TR/SVG11/shapes.mdl#polylineelement)                       | ID, Stil, Transformation, Punkte                                                             |
| [radialGradient](https://www.w3.org/TR/SVG11/pservers.mdl#radialgradientelement)         | ID, Style, CX, CY, r, FX, fy, gradientunits, gradienttransform, SpreadMethod, XLink: href |
| [Rect](https://www.w3.org/TR/SVG11/shapes.mdl#rectelement)                               | ID, Stil, Transformation, x, y, Breite, Höhe, RX, Ry                                        |
| [stop](https://www.w3.org/TR/SVG11/pservers.mdl#stopelement)                             | ID, Stil, Offset                                                                        |
| [Events](https://www.w3.org/TR/SVG11/struct.mdl#svgelement)                                 | ID, Style, x, y, Width, Height, Viewbox, preserveaspectratio                             |
| [Tel](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup> | id                                                                                       |
| [use](https://www.w3.org/TR/SVG11/struct.mdl#useelement)                                 | ID, Style, Transform, x, y, Width, Height, XLink: href                                    |



 

<sup>\*</sup> Wird nur in Windows 10 Creators Update und höher unterstützt.

## <a name="supported-svg-presentation-attributes"></a>Unterstützte SVG-Präsentations Attribute

Direct2D unterstützt auch die folgenden Präsentations Attribute. Diese können für alle SVG-Elemente angegeben werden, Sie wirken sich jedoch nur auf die Darstellung bestimmter Elemente aus, wie in der SVG-Spezifikation beschrieben (siehe [Präsentations Attribute](https://www.w3.org/TR/SVG11/attindex.mdl#presentationattributes)).

-   Clip-Pfad
-   Clip-Regel
-   color
-   ausgestellten<sup>\*</sup>
-   fill
-   Füll Deckkraft
-   Füll Regel
-   Durchlässigkeit
-   Überlauf
-   Endfarbe
-   Beendigung der Durchlässigkeit
-   stroke
-   Strich-dasharray
-   Stroke-DashOffset
-   Stroke-LineCap
-   Stroke-LineJoin
-   Stroke-miterLimit
-   Strich-Deckkraft
-   Strichbreite
-   Transparenz<sup>\*</sup>

<sup>\*</sup> Wird nur in Windows 10 Creators Update und höher unterstützt.

## <a name="unsupported-svg-features"></a>Nicht unterstützte SVG-Features

### <a name="unsupported-elements-and-attributes"></a>Nicht unterstützte Elemente und Attribute

Alle Elemente oder Attribute, die nicht in den obigen Listen enthalten sind, werden von Direct2D als nicht unterstützt angesehen. Beim Durchführen von SVG-Inhalten, die ein nicht unterstütztes Element oder Attribut enthalten, wird die nicht unterstützte Entität ignoriert. Der restliche Inhalt wird so untreu wie möglich gerendert.

### <a name="unsupported-length-units"></a>Nicht unterstützte Längeneinheiten

Ab Windows 10 Anniversary Update unterstützt Direct2D nur die Längenwerte für den Benutzerbereich und die Werte für die prozentuale Länge. Längen mit Einheiten Suffixen, wie z. b. "mm" oder "em", werden nicht unterstützt.

Ab Windows 10 Fall Creators Update unterstützt Direct2D auch absolute Einheiten Bezeichner: px, PT, PC, cm, mm und in. Relative Einheiten Bezeichner (em, ex) werden nicht unterstützt.

### <a name="unsupported-image-sources"></a>Nicht unterstützte Bildquellen

Das Image-Element wird nur unterstützt, wenn das zugehörige XLink: href-Attribut auf ein Base64-codiertes Bild festgelegt ist. Remote Verweise werden nicht unterstützt.

 

 