---
title: Beleuchtungseffekt „Entfernt-Spiegelnd“
description: Verwenden Sie den Lichteffekt "Entferntes Glanzlicht", um ein Bild zu erstellen, das eine reflektierende Oberfläche zu sein scheint, auf der die Lichtquelle scheinbar aus einer langen Entfernung stammt (z. B. die Sonnen- oder Überkopflichter).
ms.assetid: 74D71A2D-8D1D-4FDE-898A-2D2F5A8D5D31
keywords:
- entfernte Glanzlichter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a02bbf6e928691f88de3adc41fc3ae84cbc1e7df69b3b5998ca903a7556d29d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768850"
---
# <a name="distant-specular-lighting-effect"></a>Beleuchtungseffekt „Entfernt-Spiegelnd“

Verwenden Sie den Lichteffekt "Entferntes Glanzlicht", um ein Bild zu erstellen, das eine reflektierende Oberfläche zu sein scheint, auf der die Lichtquelle scheinbar aus einer langen Entfernung stammt (z. B. die Sonnen- oder Überkopflichter). Dieser Effekt verwendet den Alphakanal als Höhenkarte und strahlt das Bild mit einer entfernten Lichtquelle aus.

Die Farbe der Ausgabebitmap ist das Ergebnis von Lichtfarbe, Lichtposition und Oberflächengeometrie. Die Alphakanalausgabe für jedes Pixel mit Glanzlicht ist das Maximum der Rot-, Grün- und Blaukanalausgaben für dieses Pixel.

Die CLSID für diesen Effekt ist CLSID \_ D2D1DistantSpeular.

-   [Beispielbild](#example-image)
-   [Entfernte Lichtquelle](#distant-light-source)
-   [Effect-Eigenschaften](#effect-properties)
-   [Skalierungsmodi](#scale-modes)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Das folgende Beispiel zeigt die Ein- und Ausgabebilder des fernen Glanzlichteffekts.

![Beispielscreenshot des Effekts, der die Ein- und Ausgabebilder des entfernten Glanzlichteffekts zeigt. ](images/distant-spec-example.png)

Die endgültige Ausgabebitmap kann mithilfe der folgenden Gleichungen berechnet werden.

![Ausgabebitmapberechnung](images/distant-spec-formula1.png)

where <dl> K? = Glanzlichtkonstante.  
![Normales Surface-Symbol. ](images/point-spec-mathchar-n.png) = normaler Oberflächeneinheitsvektor.  
![Halbvektorsymbol. ](images/point-spec-mathchar-h.png) = "halbwegs" Einheitenvektor zwischen Augeneinheitsvektor und Lichteinheitsvektor.  
C<sub>r</sub>, C<sub>g</sub>, C<sub>b</sub> = die helle Farbe in RGB-Komponenten.  
</dl>

## <a name="distant-light-source"></a>Entfernte Lichtquelle

Die Abbildung hier zeigt ein Beispiel für die Richtung des Lichts von einer entfernten Lichtquelle.

![entfernte Lichtquelle](images/distant-spec-lightsource.png)

Der Effekt berechnet den Lichtvektor mithilfe der Parameter azizim und elevation. ![l vector.](images/distant-spec-mathchar-l.png) mithilfe der folgenden Gleichungen:

![Berechnung des Lichtvektors](images/distant-spec-formula2.png)

wobei Light?, Light<sub>y</sub>und Light<sub>z</sub> die Eingabewerte für die Lichtposition sind.

## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azimut<br/> D2D1 \_ DISTANTSPEULAR \_ PROP \_ AZIAKUS<br/>                       | Der Richtungswinkel der Lichtquelle in der XY-Ebene relativ zur X-Achse in der Indikatoruhrrichtung. Die Einheiten sind in Grad und müssen zwischen 0 und 360 Grad liegen.<br/> Der Typ ist FLOAT.<br/> Der Standardwert ist 0,0f.<br/>                                                                                                                                                                              |
| Elevation<br/> D2D1 \_ ENTFERNTSPEULAR \_ PROP \_ ELEVATION<br/>                   | Der Richtungswinkel der Lichtquelle in der YZ-Ebene relativ zur Y-Achse in der taktweisen Richtung des Indikators. Die Einheiten sind in Grad und müssen zwischen 0 und 360 Grad liegen. <br/> Der Typ ist FLOAT.<br/> Der Standardwert ist 0,0f.<br/>                                                                                                                                                                             |
| SpecularExponent<br/> D2D1 \_ ENTFERNTSPEULAR \_ PROP \_ SPECULAR \_ EXPONENT<br/>   | Der Exponent für den Glanzbegriff in der Phong-Beleuchtungsgleichung. Ein größerer Wert entspricht einer reflektierenderen Oberfläche. Der Wert ist einheitenlos und muss zwischen 1,0 und 128 sein. Der Typ ist FLOAT.<br/> Der Standardwert ist 1,0f.<br/>                                                                                                                                                                                          |
| SpecularConstant<br/> D2D1 \_ \_ \_ -ARTIGE PROP-SPECULAR-KONSTANTE (2D1) \_<br/>   | Das Verhältnis der Glanzreflektion zum eingehenden Licht. Der Wert ist einheitenlos und muss zwischen 0 und 10.000 sein. Der Typ ist FLOAT.<br/> Der Standardwert ist 1,0f.<br/>                                                                                                                                                                                                                                                             |
| SurfaceScale<br/> D2D1 \_ – \_ SKALA DER \_ PROP-OBERFLÄCHE IM ENTFERNTEN MAß \_<br/>           | Der Skalierungsfaktor in Z-Richtung. Der Wert ist einheitenlos und muss zwischen 0 und 10.000 sein. Der Typ ist FLOAT.<br/> Der Standardwert ist 1,0f.<br/>                                                                                                                                                                                                                                                                                |
| Color<br/> D2D1 \_ FARSPEULAR \_ PROP \_ COLOR<br/>                           | Die Farbe des eingehenden Lichts. Diese Eigenschaft wird als D2D1 \_ VECTOR \_ 3F (R, G, B) verfügbar gemacht und zum Berechnen von L<sub>R,</sub>L<sub>G,</sub>L<sub>B</sub>verwendet. Der Typ ist D2D1 \_ VECTOR \_ 3F.<br/> Der Standardwert ist {1.0f, 1.0f, 1.0f}.<br/>                                                                                                                                                                                       |
| KernelUnitLength<br/> D2D1 \_ ENTFERNTSPEULAR \_ PROP KERNEL UNIT \_ \_ \_ LENGTH<br/> | Die Größe eines Elements im Sobel-Kernel, das verwendet wird, um die Oberflächennormale in X- und Y-Richtung zu generieren. Diese Eigenschaft ist ein D2D1 \_ VECTOR \_ 2F (Kernel Unit Length X, Kernel Unit Length Y) und wird in (geräteunabhängige Pixel (DIPs)/Kernel Unit) definiert. Der Effekt verwendet die bilineare Interpolation, um die Bitmap entsprechend der Größe von Kernelelementen zu skalieren. Der Typ ist D2D1 \_ VECTOR \_ 2F.<br/> Der Standardwert ist {1.0f, 1.0f}.<br/> |
| Scalemode<br/> D2D1 \_ – \_ \_ SKALARERSPEKULAR-PROP-SKALIERUNGSMODUS \_<br/>                 | Der Interpolationsmodus, den der Effekt verwendet, um das Bild auf die entsprechende Kerneleinheitlänge zu skalieren. Es gibt sechs Skalierungsmodi, die in Qualität und Geschwindigkeit reichen.<br/> Der Typ ist D2D1 \_ DISTANTSPEULAR \_ SCALE \_ MODE.<br/> Der Standardwert ist D2D1 \_ DISTANTSPEULAR \_ SCALE \_ MODE \_ LINEAR.<br/>                                                                                                                                 |



 

## <a name="scale-modes"></a>Skalierungsmodi



| Enumeration                                               | Beschreibung                                                                                                                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ NEARSPEULAR \_ SCALE MODE \_ \_ NEAREST \_ NEIGHBOR     | Probieren Sie den nächstgelegenen einzelnen Punkt aus, und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das Bild mit der niedrigsten Qualität aus.                                                                           |
| D2D1 \_ \_ SKALARER SKALAMODUS "ENTFERNT" \_ \_ LINEAR                | Verwendet eine Vier-Punkt-Stichprobe und lineare Interpolation. Dieser Modus gibt ein Bild mit höherer Qualität als der nächste Nachbar aus.                                                                                   |
| D2D1 \_ - \_ SKALARER SKALARMODUS IM ENTFERNTEN MAßSTAB \_ \_ KUBISCH                 | Verwendet einen kubischen Kernel mit 16 Beispielen für die Interpolation. Dieser Modus verwendet die meiste Verarbeitungszeit, gibt jedoch ein Bild höherer Qualität aus.                                                                        |
| D2D1 \_ ENTFERNTERSPEKULÄRER \_ \_ SKALIERUNGSMODUS \_ MULTI SAMPLE \_ \_ LINEAR | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für ein gutes Edge-Antialiasing. Dieser Modus ist gut für das herunterskalieren um kleine Mengen auf Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ ENTFERNTERPECULARER \_ \_ SKALIERUNGSMODUS \_ ANISOTROP           | Verwendet die anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu beproben.                                                                                                     |
| D2D1 \_ ENTFERNTSPECULAR \_ SCALE MODE HIGH QUALITY \_ \_ \_ \_ KUBISCH  | Verwendet einen kubischen Kernel mit hoher Qualität in variabler Größe, um ein Vorabskalieren des Images durchzuführen, wenn eine Downskalierung an der Transformationsmatrix beteiligt ist. Verwendet dann den kubischen Interpolationsmodus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf D2D1 \_ DISTANTSPECULAR \_ SCALE MODE LINEAR \_ \_ festgelegt.

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

 

