---
title: Beleuchtungseffekt „Scheinwerfer-Spiegelnd“
description: Verwenden Sie den Spot-Specular-Beleuchtungseffekt, um ein Bild zu erstellen, das eine reflektierende Oberfläche zu sein scheint, bei der die Lichtquelle auf einen gerichteten Lichtkegel beschränkt ist.
ms.assetid: B6E24036-1548-4B9E-A8FE-8B87D4DBF97A
keywords:
- Spot-Specular-Beleuchtung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9edc4c75eaa17369ba0d0d9f1838d8857053def9aaab3dacceb8bf761b9c04c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000375"
---
# <a name="spot-specular-lighting-effect"></a>Beleuchtungseffekt „Scheinwerfer-Spiegelnd“

Verwenden Sie den Spot-Specular-Beleuchtungseffekt, um ein Bild zu erstellen, das eine reflektierende Oberfläche zu sein scheint, bei der die Lichtquelle auf einen gerichteten Lichtkegel beschränkt ist. Dieser Effekt verwendet den Alphakanal als Höhenkarte und leuchtet das Bild mit einer Punktlichtquelle.

Die Farbe der Ausgabebitmap ist das Ergebnis der lichten Farbe, der Lichtposition, der Richtung des Kegels und der Oberflächengeometrie gemäß dem winkelförmigen Teil des Phong-Beleuchtungsmodells. Die Alphakanalausgabe für jedes Pixel mit specularer Beleuchtung ist das Maximum der roten, grünen und blauen Kanalausgabe für dieses Pixel.

Die CLSID für diesen Effekt ist CLSID \_ D2D1SpotSpecular.

-   [Beispielbild](#example-image)
-   [Spot-Lichtquelle](#spot-light-source)
-   [Effect-Eigenschaften](#effect-properties)
-   [Skalierungsmodi](#scale-modes)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Das hier gezeigte Beispiel zeigt die Ein- und Ausgabebilder des Spot-Specular-Beleuchtungseffekts.

![Screenshot des Effect-Beispiels.](images/spot-spec-example.png)

Specular Light bezieht sich auf Licht, das in einer bestimmten Richtung reflektiert wird.

![Ein Diagramm der Vektoren, die verwendet werden, um eine lichtförmige Beleuchtungsausgabe für eine Bitmap zu optimieren.](images/point-spec-reflected1.png)

Der Effekt berechnet, dass die endgültigen Ausgabepixelwerte mithilfe der folgenden Gleichungen berechnet werden:

![Ausgabepixelgleichungen.](images/spot-formula1.png)

where

![Variablendefinitionen.](images/spot-formula2.png)

## <a name="spot-light-source"></a>Spot-Lichtquelle

Eine Spotlichtquelle gibt Licht in einem Kegel in einer bestimmten Richtung aus und gibt kein Licht außerhalb des Kegels aus.

Die Spot-Lichtquelle berechnet den Light Vector L und den Halfway Vector H auf die gleiche Weise wie der [Punkt-Specular-Effekt.](point-specular.md)

Der Effekt berechnet die helle Farbe L<sub>r</sub>, L<sub>g</sub>, L<sub>b</sub>als Funktion der Position der Lichtquelle, wie in den folgenden Gleichungen gezeigt:

![Gleichung für spot light source](images/spot-formula3.png)

Der Vektor ![Lichtvektorsymbol.](images/spot-mathchar-l.png) wird durch diese Gleichungen definiert:

![Gleichung: Vektor](images/spot-formula4.png)

Der Vektor ![T-Vektorsymbol](images/spot-mathchar-t.png) wird durch diese Gleichungen definiert:

![Gleichung: Vektor 2](images/spot-formula5.png)

## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> D2D1– \_ WINKELSPEZIFISCHE \_ \_ PROP-LICHTPOSITION \_<br/>             | Die Lichtposition der Punktlichtquelle. Die -Eigenschaft ist ein D2D1 \_ VECTOR \_ 3F, der als (x, y, z) definiert ist. Die Einheiten befinden sich in geräteunabhängigen Pixeln (DIPs) und sind ungebunden. Der Typ ist D2D1 \_ VECTOR \_ 3F.<br/> Der Standardwert ist {0.0f, 0.0f, 0.0f}.<br/>                                                                                                                                                                                                              |
| PointsAt<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ \_ AT<br/>                       | Wo das Spotlicht den Fokus hat. Die -Eigenschaft wird als D2D1 \_ VECTOR \_ 3F mit (x, y, z) verfügbar gemacht. Die Einheiten befinden sich in DIPs, und die Werte sind ungebunden. Der Typ ist D2D1 \_ VECTOR \_ 3F.<br/> Der Standardwert ist {0.0f, 0.0f, 0.0f}.<br/>                                                                                                                                                                                                                                     |
| Fokus<br/> D2D1– \_ FOKUS FÜR DIE \_ \_ WINKELSPEZIFISCHEN PROP-DATEN<br/>                               | Der Fokus des Spotlichts. Diese Eigenschaft ist unitlos und wird zwischen 0 und 200 definiert. Der Typ ist FLOAT.<br/> Der Standardwert ist 1,0f.<br/>                                                                                                                                                                                                                                                                                                                          |
| LimitingConeAngle<br/> D2D1 \_ SPOT \_ SPECULAR \_ PROP \_ LIMITING \_ CONE \_ ANGLE<br/> | Der Kegelwinkel, der den Bereich einschränkt, in den das Licht projiziert wird. Außerhalb des Kegels wird kein Licht projiziert. Der begrenzende Kegelwinkel ist der Winkel zwischen der Spot-Lichtachse (der Achse zwischen den *Eigenschaften LightPosition* und *PointsAt)* und dem Spot-Lichtkegel. Diese Eigenschaft wird in Grad definiert und muss zwischen 0 und 90 Grad liegen. Der Typ ist FLOAT.<br/> Der Standardwert ist 90,0f.<br/>                                                               |
| SpecularExponent<br/> \_D2D1–SPECULAR \_ \_ EXPONENT FÜR PPECULAR \_ PROP<br/>       | Der Exponent für den specular-Begriff in der Phong-Beleuchtungsgleichung. Ein größerer Wert entspricht einer reflektierenderen Oberfläche. Dieser Wert ist unitlos und muss zwischen 1,0 und 128 liegen. Der Typ ist FLOAT.<br/> Der Standardwert ist 1,0f.<br/>                                                                                                                                                                                                                               |
| SpecularConstant<br/> \_D2D1–WINKELSPEZIFISCHE \_ \_ PROP-SPEZIFIKATIONSKONSTANTEN \_<br/>       | Das Verhältnis der spiegelförmigen Reflektion zum eingehenden Licht. Der Wert ist einheitslos und muss zwischen 0 und 10.000 liegen. Der Typ ist FLOAT.<br/> Der Standardwert ist 1,0f.<br/>                                                                                                                                                                                                                                                                                                   |
| SurfaceScale<br/> D2D1– \_ WINKELSPEZIFISCHE \_ \_ \_ PROP-OBERFLÄCHENSKALA<br/>               | Der Skalierungsfaktor in Z-Richtung zum Generieren einer Höhenkarte. Der Wert ist einheitslos und muss zwischen 0 und 10.000 liegen. Der Typ ist FLOAT.<br/> Der Standardwert ist 1,0f.<br/>                                                                                                                                                                                                                                                                                          |
| Color<br/> \_D2D1–P2D1-FARBE FÜR \_ P2D1-PUNKTE \_<br/>                               | Die Farbe des eingehenden Lichts. Diese Eigenschaft wird als Vektor 3 (R, G, B) verfügbar gemacht und zum Berechnen von L<sub>R,</sub>L<sub>G,</sub>L<sub>B verwendet.</sub> Der Typ ist D2D1 \_ VECTOR \_ 3F.<br/> Der Standardwert ist {1,0f, 1,0f, 1,0f}.<br/>                                                                                                                                                                                                                                     |
| KernelUnitLength<br/> D2D1– \_ LÄNGE DER \_ \_ PROP-KERNELEINHEIT FÜR P2D1 \_ \_<br/>     | Die Größe eines Elements im Sobel-Kernel, das zum Generieren der Oberflächennormale in X- und Y-Richtung verwendet wird. Diese Eigenschaft wird den Dx- und Dy-Werten im Sobel-Farbverlauf zu. Diese Eigenschaft ist ein D2D1 \_ VECTOR \_ 2F (Kernel Unit Length X, Kernel Unit Length Y) und wird in (DIPs/Kernel Unit) definiert. Der Effekt verwendet die bilineare Interpolation, um die Bitmap so zu skalieren, dass sie mit der Größe der Kernelelemente übereinstimmen kann. Der Typ ist D2D1 \_ VECTOR \_ 2F.<br/> Der Standardwert ist {1.0f, 1.0f}.<br/> |
| Scalemode<br/> \_ \_ D2D1-SPOTPEULAR-PROP-SKALIERUNGSMODUS \_ \_<br/>                     | Der Interpolationsmodus, den der Effekt verwendet, um das Bild auf die entsprechende Kerneleinheitlänge zu skalieren. Es gibt sechs Skalierungsmodi, die in Qualität und Geschwindigkeit reichen. Weitere Informationen finden Sie unter [Skalierungsmodi.](#scale-modes) <br/> Der Typ ist D2D1 \_ SPOTPEULAR \_ SCALE \_ MODE.<br/> Der Standardwert ist D2D1 \_ SPOTPEULAR \_ SCALE \_ MODE \_ LINEAR.<br/>                                                                                                                             |



 

## <a name="scale-modes"></a>Skalierungsmodi



| Enumeration                                            | Beschreibung                                                                                                                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_D2D1-SPOTPEULAR-SKALIERUNGSMODUS \_ \_ NÄCHSTER \_ \_ NACHBAR     | Probieren Sie den nächstgelegenen einzelnen Punkt aus, und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das Bild mit der niedrigsten Qualität aus.                                                                           |
| \_D2D1-SPOTPEULAR-SKALIERUNGSMODUS \_ \_ \_ LINEAR                | Verwendet eine Vier-Punkt-Stichprobe und lineare Interpolation. Dieser Modus gibt ein Bild mit höherer Qualität als der nächste Nachbar aus.                                                                                   |
| \_D2D1-SPOTPEULAR-SKALIERUNGSMODUS \_ \_ \_ KUBISCH                 | Verwendet einen kubischen Kernel mit 16 Beispielen für die Interpolation. Dieser Modus verwendet die meiste Verarbeitungszeit, gibt jedoch ein Bild höherer Qualität aus.                                                                        |
| D2D1 \_ SPOTPEULAR \_ SCALE MODE MULTI SAMPLE \_ \_ \_ \_ LINEAR | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für ein gutes Edge-Antialiasing. Dieser Modus eignet sich gut für das Herunterskalierung um kleine Mengen auf Bildern mit wenigen Pixeln.                                              |
| \_D2D1-SPOTPEULAR-SKALIERUNGSMODUS \_ \_ \_ ANISOTROPE           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap abzubilden.                                                                                                     |
| \_D2D1-SPOTPEULAR-SKALIERUNGSMODUS \_ \_ IN HOHER QUALITÄT \_ \_ \_ KUBISCH  | Verwendet einen kubischen Kernel variabler Größe, um das Bild vorab herunterzuskalieren, wenn die Transformationsmatrix eine Downskalierung umfasst. Verwendet dann den kubischen Interpolationsmodus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf D2D1 \_ SPOTPEULAR \_ SCALE MODE LINEAR \_ \_ (LINEAR) eingestellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 8 und Plattformupdate für Windows 7 \[ Desktop-Apps \| Windows Store Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Plattformupdate für Windows 7 \[ Desktop-Apps \| Windows Store Apps\] |
| Header                   | d2d1effects.h                                                                      |
| Bibliothek                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

