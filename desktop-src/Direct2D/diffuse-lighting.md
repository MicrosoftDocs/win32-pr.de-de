---
title: Beleuchtungseffekt „Scheinwerfer-Diffus“
description: Verwenden Sie den Spot-Diffuse-Beleuchtungseffekt, um ein Bild zu erstellen, das eine nicht reflektierende Oberfläche zu sein scheint, bei der die Lichtquelle auf einen gerichteten Lichtkegel beschränkt ist und das Licht in alle Richtungen verteilt ist.
ms.assetid: 9048D664-28DB-4DB6-9B95-3A61A1EDF5EC
keywords:
- Spot diffuser Beleuchtungseffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ee0032351ce5409aabf75eaa36cd79362b8e51b85edb26d2d1d06ca9346bfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075379"
---
# <a name="spot-diffuse-lighting-effect"></a>Beleuchtungseffekt „Scheinwerfer-Diffus“

Verwenden Sie den Spot-Diffuse-Beleuchtungseffekt, um ein Bild zu erstellen, das eine nicht reflektierende Oberfläche zu sein scheint, bei der die Lichtquelle auf einen gerichteten Lichtkegel beschränkt ist und das Licht in alle Richtungen verteilt ist. Dieser Effekt verwendet den Alphakanal als Höhenkarte und leuchtet das Bild mit einer Spotlichtquelle.

Die Farbe der Ausgabebitmap ist das Ergebnis von helle Farbe, Lichtposition und Oberflächengeometrie. Die Alphakanalausgabe für jedes Pixel mit diffuser Beleuchtung ist immer 1,0.

Die CLSID für diesen Effekt ist CLSID \_ D2D1SpotDiffuse.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Skalierungsmodi](#scale-modes)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Das hier gezeigte Beispiel zeigt die Ein- und Ausgabebilder des Spot-diffusen Beleuchtungseffekts.

![Screenshot des Effect-Beispiels, der zeigt ](images/spot-diffuse-example.png)

Der Effekt berechnet, dass die endgültigen Ausgabepixelwerte mithilfe der folgenden Gleichungen berechnet werden:

![Ausgabebitmapberechnung](images/spot-diffuse-formula.png)

Hierbei gilt:<dl> k<sub>d</sub> = diffuse Beleuchtungskonst constant. Wird vom Benutzer angegeben.  
![Normales Vektorsymbol.](images/point-spec-mathchar-n.png) = Normaleinheitsvektor der Oberfläche, eine Funktion von x und y.  
![Lichtvektorsymbol.](images/distant-spec-mathchar-l.png) = Einheitenvektor, der von der Oberfläche auf das Lichtzeigt.  
L<sub>r,</sub>L<sub>g,</sub>L<sub>b</sub> = die helle Farbe in RGB-Komponenten.  
</dl>

## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                                     | Typ und Standardwert                                                                      | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ LIGHT \_ POSITION<br/>           | D2D1 \_ VECTOR \_ 3F<br/> {0.0f, 0.0f, 0.0f}<br/>                                   | Die Lichtposition der Punktlichtquelle. Die -Eigenschaft ist ein D2D1 \_ VECTOR \_ 3F, der als (x, y, z) definiert ist. Die Einheiten befinden sich in geräteunabhängigen Pixeln (DIPs) und sind ungebunden.<br/>                                                                                                                                                                                                                   |
| PointsAt<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ POINTS \_ AT<br/>                     | D2D1 \_ VECTOR \_ 3F<br/> {0.0f, 0.0f, 0.0f}<br/>                                   | Wo das Spotlicht den Fokus hat. Die -Eigenschaft wird als D2D1 \_ VECTOR \_ 3F mit (x, y, z) verfügbar gemacht. Die Einheiten befinden sich in DIPs, und die Werte sind ungebunden.<br/>                                                                                                                                                                                                                                          |
| Fokus<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ FOCUS<br/>                             | GLEITKOMMAZAHL<br/> 1.0f<br/>                                                            | Der Fokus des Spotlichts. Diese Eigenschaft ist unitlos und wird zwischen 0 und 200 definiert.<br/>                                                                                                                                                                                                                                                                                                      |
| LimitingConeAngle<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ LIMITING \_ CONE \_ ANGLE<br/> | GLEITKOMMAZAHL<br/> 90.0f<br/>                                                           | Der Kegelwinkel, der den Bereich einschränkt, in den das Licht projiziert wird. Außerhalb des Kegels wird kein Licht projiziert. Der begrenzende Kegelwinkel ist der Winkel zwischen der Spot-Lichtachse (der Achse zwischen den *Eigenschaften LightPosition* und *PointsAt)* und dem Spot-Lichtkegel. Diese Eigenschaft wird in Grad definiert und muss zwischen 0 und 90 Grad liegen.<br/>                                            |
| DiffuseConstant<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ DIFFUSE \_ CONSTANT<br/>       | GLEITKOMMAZAHL<br/> 1.0f<br/>                                                            | Das Verhältnis von diffuser Reflektion zur Menge des eingehenden Lichts. Diese Eigenschaft muss zwischen 0 und 10.000 liegen und ist komponentenlos. <br/>                                                                                                                                                                                                                                                                     |
| SurfaceScale<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ SURFACE \_ SCALE<br/>             | GLEITKOMMAZAHL<br/> 1.0f<br/>                                                            | Der Skalierungsfaktor in Z-Richtung. Die Oberflächenskala ist einheitslos und muss zwischen 0 und 10.000 liegen.<br/>                                                                                                                                                                                                                                                                                          |
| Color<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ COLOR<br/>                             | D2D1 \_ VECTOR \_ 3F<br/> {1.0f, 1.0f, 1.0f}<br/>                                   | Die Farbe des eingehenden Lichts. Diese Eigenschaft wird als Vektor 3 (R, G, B) verfügbar gemacht und zum Berechnen von L<sub>R,</sub>L<sub>G,</sub>L<sub>B verwendet.</sub> <br/>                                                                                                                                                                                                                                         |
| KernelUnitLength<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ KERNEL \_ UNIT \_ LENGTH<br/>   | D2D1 \_ VECTOR \_ 2F<br/> {1.0f, 1.0f}<br/>                                         | Die Größe eines Elements im Sobel-Kernel, das zum Generieren der Oberflächennormale in X- und Y-Richtung verwendet wird. Diese Eigenschaft wird den Dx- und Dy-Werten im Sobel-Farbverlauf zu. Diese Eigenschaft ist ein D2D1 \_ VECTOR \_ 2F (Kernel Unit Length X, Kernel Unit Length Y) und wird in (DIPs/Kernel Unit) definiert. Der Effekt verwendet die bilineare Interpolation, um die Bitmap so zu skalieren, dass sie mit der Größe der Kernelelemente übereinstimmen kann.<br/> |
| Scalemode<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ SCALE \_ MODE<br/>                   | D2D1 \_ \_ SPOTDIFFUSE-SKALIERUNGSMODUS \_<br/> D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ LINEAR<br/> | Der Interpolationsmodus, den der Effekt verwendet, um das Bild auf die entsprechende Länge der Kerneleinheit zu skalieren. Es gibt sechs Skalierungsmodi, die in Qualität und Geschwindigkeit reichen. Weitere [Informationen finden Sie](#scale-modes) unter Skalierungsmodi.<br/>                                                                                                                                                                                  |



 

## <a name="scale-modes"></a>Skalierungsmodi



| Enumeration                                           | Beschreibung                                                                                                                                                                                          |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ NEAREST \_ NEIGHBOR     | Stichprobenentnahme für den nächstgelegenen einzelnen Punkt und Verwendung dieses Punkts. Dieser Modus verbraucht weniger Verarbeitungszeit, gibt jedoch das Image mit der niedrigsten Qualität aus.                                                                           |
| D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ LINEAR                | Verwendet eine Stichprobe mit vier Punkt und eine lineare Interpolation. Dieser Modus gibt ein Bild mit höherer Qualität als der nächste Nachbar aus.                                                                                   |
| D2D1 \_ SPOTDIFFUSE \_ SCALE MODE \_ \_ KUBISCH                 | Verwendet einen kubischen 16-Beispielkernel für die Interpolation. Dieser Modus verwendet die meiste Verarbeitungszeit, gibt jedoch ein Image mit höherer Qualität aus.                                                                        |
| D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für ein gutes Edge-Antialiasing. Dieser Modus ist gut für das herunterskalieren um kleine Mengen auf Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ ANISOTROPIC           | Verwendet die anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu beproben.                                                                                                     |
| D2D1 \_ SPOTDIFFUSE \_ SCALE MODE HIGH QUALITY \_ \_ \_ \_ KUBISCH  | Verwendet einen kubischen Kernel mit hoher Qualität in variabler Größe, um ein Vorabskalieren des Images durchzuführen, wenn eine Downskalierung an der Transformationsmatrix beteiligt ist. Verwendet dann den kubischen Interpolationsmodus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf D2D1 \_ SPOTDIFFUSE \_ SCALE MODE LINEAR \_ \_ festgelegt.

 

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

 

