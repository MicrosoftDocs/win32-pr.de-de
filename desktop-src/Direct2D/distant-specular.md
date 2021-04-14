---
title: Beleuchtungseffekt „Entfernt-Spiegelnd“
description: Verwenden Sie den Wert für die Entfernungs weite Beleuchtung, um ein Bild zu erstellen, das eine reflektierende Oberfläche ist, bei der die helle Quelle aus einer langen Distanz (z. b. der Sonne oder der Oberfläche) stammt.
ms.assetid: 74D71A2D-8D1D-4FDE-898A-2D2F5A8D5D31
keywords:
- entfernte Glanz Beleuchtung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32fa21553e36839f854b4567b2aa2a3805406380
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392141"
---
# <a name="distant-specular-lighting-effect"></a>Beleuchtungseffekt „Entfernt-Spiegelnd“

Verwenden Sie den Wert für die Entfernungs weite Beleuchtung, um ein Bild zu erstellen, das eine reflektierende Oberfläche ist, bei der die helle Quelle aus einer langen Distanz (z. b. der Sonne oder der Oberfläche) stammt. Dieser Effekt verwendet den Alphakanal als Höhen Zuordnung und beleuchtet das Bild mit einer entfernten Lichtquelle.

Die Farbe der Ausgabe Bitmap ist das Ergebnis der hellen Farbe, der hellen Position und der Oberflächengeometrie. Die Alphakanal Ausgabe für jedes Pixel mit Glanz Beleuchtung ist der Höchstwert der roten, grünen und blauen Kanal Ausgaben für dieses Pixel.

Die CLSID für diesen Effekt ist CLSID \_ D2D1DistantSpecular.

-   [Beispiel Bild](#example-image)
-   [Entfernte Lichtquelle](#distant-light-source)
-   [Effekt Eigenschaften](#effect-properties)
-   [Skalierungs Modi](#scale-modes)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Im folgenden Beispiel werden die Eingabe-und Ausgabe Bilder des entfernteren Beleuchtungs Effekts veranschaulicht.

![ein Screenshot mit Beispiel Effekten zeigt die Eingabe-und Ausgabe Bilder des entfernten Glanzlicht Effekts. ](images/distant-spec-example.png)

Die endgültige Ausgabe Bitmap kann mithilfe der folgenden Gleichungen berechnet werden.

![Ausgabe Bitmap-Berechnung](images/distant-spec-formula1.png)

where <dl> km? = Glanz Beleuchtungs Konstante.  
![Oberflächen normales Symbol. ](images/point-spec-mathchar-n.png) = Oberflächen normaler Einheits Vektor.  
![halbes Vektorsymbol. ](images/point-spec-mathchar-h.png) = "halber" Einheits Vektor zwischen dem Augen Einheiten Vektor und dem hellen Einheits Vektor.  
C<sub>r</sub>, c<sub>g</sub>, c<sub>b</sub> = die helle Farbe in RGB-Komponenten.  
</dl>

## <a name="distant-light-source"></a>Entfernte Lichtquelle

Das Bild hier zeigt ein Beispiel für die Richtung des Lichts von einer entfernten Lichtquelle.

![entfernte Lichtquelle](images/distant-spec-lightsource.png)

Der Effekt verwendet die Parameter Azimuth und Erhöhung, um den Licht Vektor zu berechnen. ![l-Vektor.](images/distant-spec-mathchar-l.png) mithilfe der folgenden Gleichungen:

![helle Vektor Berechnung](images/distant-spec-formula2.png)

Where Light?, Light<sub>y</sub>und Light<sub>z</sub> sind die Werte für die Eingabe Lichtposition.

## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azimuth<br/> D2D1 \_ distantspecfeiner \_ Prop- \_ Azimuth<br/>                       | Der Richtungs Winkel der Lichtquelle in der XY-Ebene relativ zur X-Achse in der punktuturdirektionale Richtung. Die Einheiten liegen in Grad und müssen zwischen 0 und 360 Grad liegen.<br/> Der Typ ist "float".<br/> Der Standardwert ist 0,0 f.<br/>                                                                                                                                                                              |
| Elevation<br/> D2D1 \_ distantspecfeiner Prop-herauf Stufung \_ \_<br/>                   | Der Richtungs Winkel der Lichtquelle in der YZ-Ebene relativ zur Y-Achse in der punktuturdirektionale Richtung. Die Einheiten liegen in Grad und müssen zwischen 0 und 360 Grad liegen. <br/> Der Typ ist "float".<br/> Der Standardwert ist 0,0 f.<br/>                                                                                                                                                                             |
| Specularexponent<br/> D2D1 \_ distantspecdistende \_ Prop- \_ \_ Exponent<br/>   | Der Exponent für den Glanz Ausdruck in der Phong-Beleuchtungs Gleichung. Ein größerer Wert entspricht einer stärker reflektierenden Oberfläche. Der Wert ist unitless und muss zwischen 1,0 und 128 liegen. Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                          |
| Specularconstant<br/> D2D1 \_ distantspecdistkonstante, Glanz \_ \_ \_ Konstante<br/>   | Das Verhältnis der Glanz Reflektion zum eingehenden Licht. Der Wert ist unitless und muss zwischen 0 und 10.000 liegen. Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                             |
| Surfakescale<br/> D2D1 \_ distantspecarität- \_ Prop- \_ Oberflächen \_ Skala<br/>           | Der Skalierungsfaktor in der Z-Richtung. Der Wert ist unitless und muss zwischen 0 und 10.000 liegen. Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                |
| Color<br/> D2D1 \_ distantspecarität- \_ Prop- \_ Farbe<br/>                           | Die Farbe des eingehenden Lichts. Diese Eigenschaft wird als D2D1 \_ Vector \_ 3F (R, G, B) verfügbar gemacht und zum Berechnen von l<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>verwendet. Der Typ ist "D2D1 \_ Vector \_ 3F".<br/> Der Standardwert ist {1.0 f, 1.0 f, 1.0 f}.<br/>                                                                                                                                                                                       |
| Kernelunitlength<br/> D2D1 \_ distantspeclength \_ \_ -Länge der Kernel \_ Einheiten \_<br/> | Die Größe eines Elements im Sobel-Kernel, das verwendet wird, um die Oberflächen normale in der X-und Y-Richtung zu generieren. Diese Eigenschaft ist ein D2D1 \_ Vector \_ 2F (Kernel Unit Length X, Kernel Unit Length Y) und wird in (geräteunabhängige Pixel (Dips)/Kernel Unit) definiert. Der Effekt verwendet die bilineare interpolung, um die Bitmap so zu skalieren, dass Sie mit der Größe der Kernel-Elemente Der Typ ist "D2D1 \_ Vector \_ 2F".<br/> Der Standardwert ist {1.0 f, 1.0 f}.<br/> |
| Skalemode<br/> D2D1 \_ distantspecfeiner- \_ Prop- \_ Skalierungs \_ Modus<br/>                 | Der Interpolations Modus, mit dem das Bild auf die entsprechende Kernel Einheitslänge skaliert wird. Es gibt sechs Skalierungs Modi mit hoher Qualität und Geschwindigkeit.<br/> Der Typ ist der D2D1 \_ distantspecarität- \_ Skalierungs \_ Modus.<br/> Der Standardwert ist D2D1 \_ \_ distantspecdistscale \_ Mode \_ linear.<br/>                                                                                                                                 |



 

## <a name="scale-modes"></a>Skalierungs Modi



| Enumeration                                               | Beschreibung                                                                                                                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ \_ distantspecdistscale \_ Mode \_ Nächster \_ Nachbar     | Verwendet den nächsten einzelnen Punkt und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das niedrigste Qualitätsbild aus.                                                                           |
| D2D1 \_ \_ distantspecdistalskalierungsmodus \_ \_ linear                | Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung. In diesem Modus wird ein Image mit höherer Qualität als nächster Nachbar ausgegeben.                                                                                   |
| D2D1 \_ distantspecfeiner \_ Skalierungs \_ Modus ( \_ kubisch)                 | Verwendet einen 16-beispielkubischen Kernel für Interpolationen. In diesem Modus wird die meiste Verarbeitungszeit verwendet, es wird jedoch ein Image mit höherer Qualität ausgegeben.                                                                        |
| D2D1 \_ \_ distantspecdistscale \_ Mode \_ \_ Multisample \_ linear | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für eine gute Edge-Antialiasing. Dieser Modus eignet sich gut zum horizontalen Herunterskalieren um kleine Beträge in Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ distantspecarität- \_ Skalierungs \_ Modus \_ anisotrope           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu modellieren.                                                                                                     |
| D2D1 \_ distantspecfeiner \_ Skalierungs \_ Modus \_ High \_ Quality \_ kubisch  | Verwendet einen kubischen Kernel mit hoher Qualität für eine Variable Größe, um das Abbild vorab zu skalieren, wenn eine downstreamingmatrix an der Transformationsmatrix beteiligt ist. Verwendet dann den kubischen Interpolations Modus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf D2D1 \_ distantspecdistscale \_ \_ Mode \_ linear.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Header                   | d2d1effects. h                                                                      |
| Bibliothek                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

