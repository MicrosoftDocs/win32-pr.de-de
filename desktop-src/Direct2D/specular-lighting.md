---
title: Beleuchtungseffekt „Scheinwerfer-Spiegelnd“
description: Verwenden Sie den Glanz der Lichtquelle, um ein Bild zu erstellen, das eine reflektierende Oberfläche ist, bei der die Lichtquelle auf einen gerichteten Lichtkegel beschränkt ist.
ms.assetid: B6E24036-1548-4B9E-A8FE-8B87D4DBF97A
keywords:
- Glanz Beleuchtung erkennen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f2482d9631de7383c26e791d13f1571f247fa6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040481"
---
# <a name="spot-specular-lighting-effect"></a>Beleuchtungseffekt „Scheinwerfer-Spiegelnd“

Verwenden Sie den Glanz der Lichtquelle, um ein Bild zu erstellen, das eine reflektierende Oberfläche ist, bei der die Lichtquelle auf einen gerichteten Lichtkegel beschränkt ist. Dieser Effekt verwendet den Alphakanal als Höhen Zuordnung und beleuchtet das Bild mit einer Punktlicht Quelle.

Die Farbe der Ausgabe Bitmap ist das Ergebnis der hellen Farbe, der Lichtposition, der Kegel Richtung und der Oberflächengeometrie entsprechend dem Glanz Bereich des Phong-Beleuchtungs Modells. Die Alphakanal Ausgabe für jedes Pixel mit Glanz Beleuchtung ist der Höchstwert der roten, grünen und blauen Kanal Ausgaben für dieses Pixel.

Die CLSID für diesen Effekt ist CLSID \_ D2D1SpotSpecular.

-   [Beispiel Bild](#example-image)
-   [Light-Quelle ermitteln](#spot-light-source)
-   [Effekt Eigenschaften](#effect-properties)
-   [Skalierungs Modi](#scale-modes)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Im folgenden Beispiel werden die Eingabe-und Ausgabe Bilder des Glanzlicht Effekts angezeigt.

![Screenshot des Effekts-Beispiels.](images/spot-spec-example.png)

Glanzlicht bezieht sich auf Licht, das in eine bestimmte Richtung reflektiert wird.

![ein Diagramm der Vektoren, die verwendet werden, um eine Glanzlicht Ausgabe für eine Bitmap zu verwenden.](images/point-spec-reflected1.png)

Der Effekt berechnet die endgültigen Ausgabe Pixelwerte werden mithilfe der Gleichungen hier berechnet:

![Ausgabe Pixel Gleichungen.](images/spot-formula1.png)

where

![Variablen Definitionen.](images/spot-formula2.png)

## <a name="spot-light-source"></a>Light-Quelle ermitteln

Eine Spot Light-Quelle gibt Licht in einem Kegel in einer bestimmten Richtung aus und gibt kein Licht außerhalb des Kegel aus.

Die Spot Light-Quelle berechnet den hellen Vektor L und den halben Vektor H auf die gleiche Weise wie der [Punkt](point-specular.md) Glanzeffekt.

Der Effekt berechnet die helle Farbe l<sub>r</sub>, l<sub>g</sub>, l<sub>b</sub>als Funktion der Position der Lichtquelle, wie hier gezeigt:

![Gleichung für Spot Light Source](images/spot-formula3.png)

Der Vektor ![hell Vektorsymbol.](images/spot-mathchar-l.png) wird durch diese Gleichungen definiert:

![Gleichung: Vektor](images/spot-formula4.png)

Der Vektor ![t-Vektorsymbol](images/spot-mathchar-t.png) wird durch diese Gleichungen definiert:

![Gleichung: Vektor 2](images/spot-formula5.png)

## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lightposition<br/> D2D1 \_ spotspecweightprop- \_ \_ Licht \_ Position<br/>             | Die helle Position der Punktlicht Quelle. Die-Eigenschaft ist ein \_ \_ als (x, y, z) definiertes D2D1 Vector 3f. Die Einheiten befinden sich in geräteunabhängigen Pixeln (Dips) und sind unbegrenzt. Der Typ ist "D2D1 \_ Vector \_ 3F".<br/> Der Standardwert ist {0,0 f, 0,0 f, 0,0 f}.<br/>                                                                                                                                                                                                              |
| Point<br/> D2D1 \_ spotglanz- \_ Stütz \_ Punkte \_ bei<br/>                       | Wo sich das Spot Licht im Fokus befindet. Die-Eigenschaft wird als D2D1 \_ Vector \_ 3F mit (x, y, z) verfügbar gemacht. Die Einheiten befinden sich in Dips, und die Werte sind unbegrenzt. Der Typ ist "D2D1 \_ Vector \_ 3F".<br/> Der Standardwert ist {0,0 f, 0,0 f, 0,0 f}.<br/>                                                                                                                                                                                                                                     |
| Fokus<br/> D2D1 \_ spotspecfeiner \_ \_ Fokus<br/>                               | Der Fokus des Spot Lichts. Diese Eigenschaft ist unitless und wird zwischen 0 und 200 definiert. Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                          |
| Limit-Konfigurations Winkel<br/> D2D1-Glanz Glanz, der den \_ \_ \_ \_ \_ Kegel \_ Winkel einschränkt<br/> | Der Kegelwinkel, der den Bereich einschränkt, in dem das Licht projiziert wird. Kein Licht wird außerhalb des Kegel projiziert. Der Begrenzungs Kegelwinkel ist der Winkel zwischen der Spot-Light-Achse (die Achse zwischen den *lightposition* -und *pointsat* -Eigenschaften) und dem Spot Light-Kegel. Diese Eigenschaft wird in Grad definiert und muss zwischen 0 und 90 Grad liegen. Der Typ ist "float".<br/> Der Standardwert ist 90,0 f.<br/>                                                               |
| Specularexponent<br/> D2D1 \_ spotspecfeiner \_ Prop- \_ \_ Exponent<br/>       | Der Exponent für den Glanz Ausdruck in der Phong-Beleuchtungs Gleichung. Ein größerer Wert entspricht einer stärker reflektierenden Oberfläche. Dieser Wert ist unitless und muss zwischen 1,0 und 128 liegen. Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                               |
| Specularconstant<br/> D2D1 \_ spotspecarität-Konstante, Glanz \_ \_ \_ Konstante<br/>       | Das Verhältnis der Glanz Reflektion zum eingehenden Licht. Der Wert ist unitless und muss zwischen 0 und 10.000 liegen. Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                                   |
| Surfakescale<br/> D2D1 \_ spotspecvertikale \_ Prop- \_ Oberflächen \_ Skala<br/>               | Der Skalierungsfaktor in der Z-Richtung zum Erstellen einer Höhen Zuordnung. Der Wert ist unitless und muss zwischen 0 und 10.000 liegen. Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                          |
| Color<br/> D2D1 \_ spotspecfeiner \_ Prop- \_ Farbe<br/>                               | Die Farbe des eingehenden Lichts. Diese Eigenschaft wird als Vektor 3 (R, G, B) verfügbar gemacht und zum Berechnen von l<sub>R</sub>, l<sub>G</sub>, l<sub>b</sub>verwendet. Der Typ ist "D2D1 \_ Vector \_ 3F".<br/> Der Standardwert ist {1.0 f, 1.0 f, 1.0 f}.<br/>                                                                                                                                                                                                                                     |
| Kernelunitlength<br/> D2D1 \_ spotspecfeiner \_ Prop \_ -Kernel \_ Einheits \_ Länge<br/>     | Die Größe eines Elements im Sobel-Kernel, das verwendet wird, um die Oberflächen normale in der X-und Y-Richtung zu generieren. Diese Eigenschaft wird den DX-und dy-Werten im Sobel-Farbverlauf zugeordnet. Diese Eigenschaft ist ein D2D1 \_ Vector \_ 2F (Kernel Unit Length X, Kernel Unit Length Y) und wird in (Dips/Kernel Unit) definiert. Der Effekt verwendet die bilineare interpolung, um die Bitmap so zu skalieren, dass Sie mit der Größe der Kernel-Elemente Der Typ ist "D2D1 \_ Vector \_ 2F".<br/> Der Standardwert ist {1.0 f, 1.0 f}.<br/> |
| Skalemode<br/> D2D1 \_ \_ \_ spotspecscale \_ Mode<br/>                     | Der Interpolations Modus, mit dem das Bild auf die entsprechende Kernel Einheitslänge skaliert wird. Es gibt sechs Skalierungs Modi mit hoher Qualität und Geschwindigkeit. Weitere Informationen finden Sie unter [Skalierungs Modi](#scale-modes) . <br/> Der Typ ist der \_ Modus "D2D1 \_ spotspecscale" \_ .<br/> Der Standardwert ist D2D1 \_ \_ spotspecscale \_ Mode \_ linear.<br/>                                                                                                                             |



 

## <a name="scale-modes"></a>Skalierungs Modi



| Enumeration                                            | Beschreibung                                                                                                                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ spotspecfeiner \_ Skalierungs \_ Modus \_ Nächster \_ Nachbar     | Verwendet den nächsten einzelnen Punkt und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das niedrigste Qualitätsbild aus.                                                                           |
| D2D1 \_ spotspecfeiner \_ Skalierungs \_ Modus \_ linear                | Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung. In diesem Modus wird ein Image mit höherer Qualität als nächster Nachbar ausgegeben.                                                                                   |
| D2D1 \_ spotspecfeiner \_ Skalierungs \_ Modus ( \_ kubisch)                 | Verwendet einen 16-beispielkubischen Kernel für Interpolationen. In diesem Modus wird die meiste Verarbeitungszeit verwendet, es wird jedoch ein Image mit höherer Qualität ausgegeben.                                                                        |
| D2D1 \_ spotspecfeiner \_ Skalierungs \_ Modus \_ \_ Multisample \_ linear | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für eine gute Edge-Antialiasing. Dieser Modus eignet sich gut zum horizontalen Herunterskalieren um kleine Beträge in Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ spotspecfeiner \_ Skalierungs \_ Modus \_ anisotrope           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu modellieren.                                                                                                     |
| D2D1 \_ spotspecfeiner \_ Skalierungs \_ Modus \_ High \_ Quality \_ kubisch  | Verwendet einen kubischen Kernel mit hoher Qualität für eine Variable Größe, um das Abbild vorab zu skalieren, wenn eine downstreamingmatrix an der Transformationsmatrix beteiligt ist. Verwendet dann den kubischen Interpolations Modus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf den D2D1-Modus \_ \_ linear skaliert \_ \_ .

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

 

