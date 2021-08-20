---
title: Beleuchtungseffekt „Punkt-Spiegelnd“
description: Verwenden Sie den Point-Specular-Beleuchtungseffekt, um ein Bild zu erstellen, das eine reflektierende Oberfläche zu sein scheint.
ms.assetid: 89E22FD0-BB7F-465F-A79C-056CA9F14F5D
keywords:
- Point Specular Lighting Effect
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37adb0c6ea0ca946abf819730dcc378f421bf2c220dc0ab8d41916f570501d0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075141"
---
# <a name="point-specular-lighting-effect"></a>Beleuchtungseffekt „Punkt-Spiegelnd“

Verwenden Sie den Point-Specular-Beleuchtungseffekt, um ein Bild zu erstellen, das eine reflektierende Oberfläche zu sein scheint. Der Effekt verwendet den Alphakanal des Bilds als Höhenkarte und eine Punktlichtquelle, die Sie positionieren, und berechnet die Reflektion und das Licht entsprechend dem spiegelförmigen Teil des Phong-Beleuchtungsmodells.

Die Farbe der Ausgabebitmap ist das Ergebnis von helle Farbe, Lichtposition und Oberflächengeometrie. Die Alphakanalausgabe für jedes Pixel mit specularer Beleuchtung ist das Maximum der roten, grünen und blauen Kanalausgabe für dieses Pixel.

Die CLSID für diesen Effekt ist CLSID \_ D2D1PointSpecular.

-   [Beispielbild](#example-image)
-   [Punktlichtquelle](#point-light-source)
-   [Höhenzuordnung und Normalvektor](#height-map-and-normal-vector)
-   [Specular lighting constant and exponent](#specular-lighting-constant-and-exponent)
-   [Effect-Eigenschaften](#effect-properties)
-   [Skalierungsmodi](#scales-modes)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Das hier gezeigte Beispiel zeigt die Ein- und Ausgabebilder des Point-Specular-Beleuchtungseffekts.

![Screenshot des Effektbeispiels, der die Ein- und Ausgabebilder des Point Specular Lighting-Effekts zeigt.](images/point-spec-example.png)

Specular Light bezieht sich auf Licht, das gemäß dem Phong-Beleuchtungsmodell in einer bestimmten Richtung reflektiert wird.

![Ein Diagramm der Vektoren, die verwendet werden, um eine lichtförmige Beleuchtungsausgabe für eine Bitmap zu optimieren.](images/point-spec-reflected1.png)

Der Effekt berechnet die endgültigen Ausgabepixelwerte mithilfe der folgenden Gleichungen:

![die Gleichungen zum Berechnen der endgültigen Pixelwerte. ](images/point-spec-formula-output.png)

where<dl> K? = Specular Lighting-Konstante.  
![das Symbol für den normalen Einheitenvektor der Oberfläche. ](images/point-spec-mathchar-n.png) = Normaleinheitsvektor der Oberfläche, der eine Funktion von x und y ist. Die [Berechnungen finden Sie unter Höhenzuordnung](#height-map-and-normal-vector) und Normalvektor.  
![das Symbol für den Einheitenvektor in der Mitte. ](images/point-spec-mathchar-h.png) = "halber" Einheitenvektor zwischen Augeneinheitsvektor und lichten Einheitenvektor. Die [Berechnungen finden Sie unter](#point-light-source) Punktlichtquelle.  
L<sub>r,</sub>L<sub>g,</sub>L<sub>b</sub> = die helle Farbe in RGB-Komponenten.  
</dl>

Sie legen die lichtförmige Beleuchtungskonstante als *SpecularConstant-Eigenschaft* und die helle Farbe als *Color-Eigenschaft* fest.

## <a name="point-light-source"></a>Punktlichtquelle

Eine Punktlichtquelle gibt Licht in alle Richtungen aus, wie in der Abbildung hier.

![ein Punktlicht, das Licht in alle Richtungen austrägt.](images/point-spec-light.png)

Sie legen die Position der Lichtquelle mithilfe der *LightPosition-Eigenschaft* fest. Der Effekt berechnet den Lichtvektor L für eine Punktlichtquelle mithilfe der hier dargestellten Gleichungen:

![die Lichtvektorgleichung.](images/point-spec-formula3.png)

wobei Light?, Light<sub>y</sub>und Light<sub>z</sub> die Eingabelichtposition sind. Der Effekt berechnet den Halbvektor, das ![ Symbol für den Halbvektor.](images/point-spec-mathchar-h.png) wie im Phong-Beleuchtungsmodell mithilfe der hier beschriebenen Gleichung definiert. Das Beleuchtungsmodell geht davon aus, dass sich der Augenvektor, das Augenvektorsymbol, bei ![ ](images/point-spec-mathchar-e.png) (0,0,1) befindet.

![Halfway Vector-Gleichung.](images/point-spec-formula4.png)

Sowohl L als auch H werden in Vektoren mit Einheitenlänge normalisiert.

## <a name="height-map-and-normal-vector"></a>Höhenzuordnung und Normalvektor

Der Effekt generiert eine Höhenzuordnung für das Eingabebild basierend auf seinem Alphakanal.

Die Höhe (Z)-Komponente wird mithilfe der Gleichung berechnet:

![die Gleichung zum Berechnen der Höhe (z) der Oberfläche.](images/point-spec-formula6.png)

Der Effekt berechnet den Oberflächennorm normal, ![das normale Vektorsymbol.](images/point-spec-mathchar-n.png)für die Eingabebitmap mit einem Sobel-Farbverlauf.

## <a name="specular-lighting-constant-and-exponent"></a>Specular lighting constant and exponent

Specular Light stellt das Licht dar, das von der Oberfläche des der Bildhöhenkarte reflektiert wird. Sie geben die *SpecularExponent-Eigenschaft* an, die die Menge an spiegelförmiger Reflektion aus der Bitmap bestimmt.

Größere Exponenten stellen umfangreichere Objekte dar und reflektieren Licht in einer fokussierteren Form.

Die *SpecularConstant-Eigenschaft* K? definiert die Menge des reflektierten Lichts als Verhältnis des eingehenden Lichts.

## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ LIGHT \_ POSITION<br/>         | Die Lichtposition der Punktlichtquelle. Die -Eigenschaft ist ein D2D1 \_ VECTOR \_ 3F, der als (x, y, z) definiert ist. Die Einheiten befinden sich in geräteunabhängigen Pixeln (DEVICE-Independent Pixels, DIPs), und die Werte sind einheitslos und ungebunden. Der Typ ist D2D1 \_ VECTOR \_ 3F.<br/> Der Standardwert ist {0.0f, 0.0f, 0.0f}.<br/>                                                                                                                                                                                      |
| SpecularExponent<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ SPECULAR \_ EXPONENT<br/>   | Der Exponent für den specular-Begriff in der Phong-Beleuchtungsgleichung. Ein größerer Wert entspricht einer reflektierenderen Oberfläche. Dieser Wert ist unitlos und muss zwischen 1,0 und 128 liegen. Der Typ ist FLOAT.<br/> Der Standardwert ist 1,0f.<br/>                                                                                                                                                                                                                               |
| SpecularConstant<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ SPECULAR \_ CONSTANT<br/>   | Das Verhältnis der spiegelförmigen Reflektion zum eingehenden Licht. Der Wert ist einheitslos und muss zwischen 0 und 10.000 liegen. Der Typ ist FLOAT.<br/> Der Standardwert ist 1,0f.<br/>                                                                                                                                                                                                                                                                                                   |
| SurfaceScale<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ SURFACE \_ SCALE<br/>           | Der Skalierungsfaktor in Z-Richtung zum Generieren einer Höhenkarte. Der Wert ist einheitslos und muss zwischen 0 und 10.000 liegen. Der Typ ist FLOAT.<br/> Der Standardwert ist 1,0f.<br/>                                                                                                                                                                                                                                                                                          |
| Color<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ COLOR<br/>                           | Die Farbe des eingehenden Lichts. Diese Eigenschaft wird als D2D1 \_ VECTOR \_ 3F (R, G, B)<sub></sub><sub></sub>verfügbar gemacht und zum Berechnen von L R, L G, L<sub>B verwendet.</sub> Der Typ ist D2D1 \_ VECTOR \_ 3F.<br/> Der Standardwert ist {1,0f, 1,0f, 1,0f}.<br/>                                                                                                                                                                                                                             |
| KernelUnitLength<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ KERNEL \_ UNIT \_ LENGTH<br/> | Die Größe eines Elements im Sobel-Kernel, das zum Generieren der Normalenoberfläche in X- und Y-Richtung verwendet wird. Diese Eigenschaft wird den Dx- und Dy-Werten im Sobel-Farbverlauf zu. Diese Eigenschaft ist ein D2D1 \_ VECTOR \_ 2F (Kernel Unit Length X, Kernel Unit Length Y) und wird in (DIPs/Kernel Unit) definiert. Der Effekt verwendet die bilineare Interpolation, um die Bitmap so zu skalieren, dass sie mit der Größe der Kernelelemente übereinstimmen kann. Der Typ ist D2D1 \_ VECTOR \_ 2F.<br/> Der Standardwert ist {1,0f, 1,0f}.<br/> |
| Scalemode<br/> \_D2D1-PUNKTEPE PROP \_ SCALE \_ \_ MODE<br/>                 | Der Interpolationsmodus, den der Effekt verwendet, um das Bild auf die entsprechende Kerneleinheitlänge zu skalieren. Es gibt sechs Skalierungsmodi, die in Qualität und Geschwindigkeit reichen. Weitere Informationen finden Sie unter [Skalierungsmodi.](#scales-modes) <br/> Der Typ ist D2D1 \_ POINTSPEULAR \_ SCALE \_ MODE.<br/> Der Standardwert ist D2D1 \_ POINTSPEULAR \_ SCALE \_ MODE \_ LINEAR.<br/>                                                                                                                          |



 

## <a name="scales-modes"></a>Skalierungsmodi



| Enumeration                                             | Beschreibung                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ POINTSPEULAR \_ SCALE MODE \_ \_ NEAREST \_ NEIGHBOR     | Probieren Sie den nächstgelegenen einzelnen Punkt aus, und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das Bild mit der niedrigsten Qualität aus.                                                                           |
| D2D1 \_ POINTSPEULAR \_ SCALE MODE \_ \_ LINEAR                | Verwendet eine Vier-Punkt-Stichprobe und lineare Interpolation. Dieser Modus gibt ein Bild mit höherer Qualität als der nächste Nachbar aus.                                                                                   |
| \_D2D1-PUNKTEPEULARER \_ \_ SKALIERUNGSMODUS \_ KUBISCH                 | Verwendet einen kubischen Kernel mit 16 Beispielen für die Interpolation. Dieser Modus verwendet die meiste Verarbeitungszeit, gibt jedoch ein Bild höherer Qualität aus.                                                                        |
| D2D1 \_ POINTSPEULAR \_ SCALE MODE MULTI SAMPLE \_ \_ \_ \_ LINEAR | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für ein gutes Edge-Antialiasing. Dieser Modus eignet sich gut für das Herunterskalierung um kleine Mengen auf Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ POINTSPEULAR \_ SCALE MODE \_ \_ ANISOTROP           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap abzubilden.                                                                                                     |
| D2D1 \_ POINTSPEULAR \_ SCALE MODE HIGH QUALITY \_ \_ \_ \_ CUBIC  | Verwendet einen kubischen Kernel variabler Größe, um das Bild vorab herunterzuskalieren, wenn die Transformationsmatrix eine Downskalierung umfasst. Verwendet dann den kubischen Interpolationsmodus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, lautet der Effekt standardmäßig D2D1 \_ POINTSPEULAR \_ SCALE \_ MODE \_ LINEAR.

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

 

