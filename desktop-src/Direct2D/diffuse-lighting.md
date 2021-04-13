---
title: Beleuchtungseffekt „Scheinwerfer-Diffus“
description: Verwenden Sie den Effekt "Spot-diffuse Beleuchtung", um ein Bild zu erstellen, das eine nicht reflektierende Oberfläche ist, bei der die Lichtquelle auf einen gerichteten Lichtkegel beschränkt ist und das Licht in alle Richtungen verteilt ist.
ms.assetid: 9048D664-28DB-4DB6-9B95-3A61A1EDF5EC
keywords:
- diffusen Beleuchtungs Effekt erkennen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d085e43f161275cbe46d5b8eeb03f0ad13ff5f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104555177"
---
# <a name="spot-diffuse-lighting-effect"></a>Beleuchtungseffekt „Scheinwerfer-Diffus“

Verwenden Sie den Effekt "Spot-diffuse Beleuchtung", um ein Bild zu erstellen, das eine nicht reflektierende Oberfläche ist, bei der die Lichtquelle auf einen gerichteten Lichtkegel beschränkt ist und das Licht in alle Richtungen verteilt ist. Dieser Effekt verwendet den Alphakanal als Höhen Zuordnung und beleuchtet das Bild mit einer Spot Light-Quelle.

Die Farbe der Ausgabe Bitmap ist das Ergebnis der hellen Farbe, der hellen Position und der Oberflächengeometrie. Die Alphakanal Ausgabe für jedes Pixel mit diffuses Beleuchtung ist immer 1,0.

Die CLSID für diesen Effekt ist CLSID \_ D2D1SpotDiffuse.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Skalierungs Modi](#scale-modes)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Im folgenden Beispiel werden die Eingabe-und Ausgabe Bilder des Lichteffekts der Spot-diffuses angezeigt.

![Screenshot des Effekts-Beispiels ](images/spot-diffuse-example.png)

Der Effekt berechnet die endgültigen Ausgabe Pixelwerte werden mithilfe dieser Gleichungen berechnet:

![Ausgabe Bitmap-Berechnung](images/spot-diffuse-formula.png)

Hierbei gilt:<dl> k<sub>d</sub> = diffuses Beleuchtungs Konstante. Wird vom Benutzer angegeben.  
![normales Vektorsymbol.](images/point-spec-mathchar-n.png) = Oberflächen normaler Einheits Vektor, eine Funktion von x und y.  
![hell Vektorsymbol.](images/distant-spec-mathchar-l.png) = Einheits Vektor, der von der Oberfläche auf das Licht zeigt.  
L<sub>r</sub>, l<sub>g</sub>, l<sub>b</sub> = die helle Farbe in RGB-Komponenten.  
</dl>

## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                                     | Typ und Standardwert                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lightposition<br/> D2D1 \_ spotdiffuse \_ - \_ Licht \_ Position<br/>           | D2D1 \_ Vector \_ 3F<br/> {0,0 f, 0,0 f, 0,0 f}<br/>                                   | Die helle Position der Punktlicht Quelle. Die-Eigenschaft ist ein \_ \_ als (x, y, z) definiertes D2D1 Vector 3f. Die Einheiten befinden sich in geräteunabhängigen Pixeln (Dips) und sind unbegrenzt.<br/>                                                                                                                                                                                                                   |
| Point<br/> D2D1 \_ spotdiffuse- \_ Stütz \_ Punkte \_ unter<br/>                     | D2D1 \_ Vector \_ 3F<br/> {0,0 f, 0,0 f, 0,0 f}<br/>                                   | Wo sich das Spot Licht im Fokus befindet. Die-Eigenschaft wird als D2D1 \_ Vector \_ 3F mit (x, y, z) verfügbar gemacht. Die Einheiten befinden sich in Dips, und die Werte sind unbegrenzt.<br/>                                                                                                                                                                                                                                          |
| Fokus<br/> D2D1 \_ spotdiffuse- \_ Prop- \_ Fokus<br/>                             | GLEITKOMMAZAHL<br/> 1.0 f<br/>                                                            | Der Fokus des Spot Lichts. Diese Eigenschaft ist unitless und wird zwischen 0 und 200 definiert.<br/>                                                                                                                                                                                                                                                                                                      |
| Limit-Konfigurations Winkel<br/> D2D1 \_ spotdiffuse \_ , \_ begrenzen des \_ Kegel \_ Winkels<br/> | GLEITKOMMAZAHL<br/> 90,0 f<br/>                                                           | Der Kegelwinkel, der den Bereich einschränkt, in dem das Licht projiziert wird. Kein Licht wird außerhalb des Kegel projiziert. Der Begrenzungs Kegelwinkel ist der Winkel zwischen der Spot-Light-Achse (die Achse zwischen den *lightposition* -und *pointsat* -Eigenschaften) und dem Spot Light-Kegel. Diese Eigenschaft wird in Grad definiert und muss zwischen 0 und 90 Grad liegen.<br/>                                            |
| Diffseconstant<br/> D2D1 \_ \_ \_ spotdiffdiffuse \_ Konstante<br/>       | GLEITKOMMAZAHL<br/> 1.0 f<br/>                                                            | Das Verhältnis zwischen diffuses Reflektion und eingehender Lichtmenge. Diese Eigenschaft muss zwischen 0 und 10.000 liegen und ist unitless. <br/>                                                                                                                                                                                                                                                                     |
| Surfakescale<br/> D2D1 \_ spotdiffuse \_ Prop- \_ Oberflächen \_ Skala<br/>             | GLEITKOMMAZAHL<br/> 1.0 f<br/>                                                            | Der Skalierungsfaktor in der Z-Richtung. Die Oberflächen Skala ist unitless und muss zwischen 0 und 10.000 liegen.<br/>                                                                                                                                                                                                                                                                                          |
| Color<br/> D2D1 \_ spotdiffuse- \_ Prop- \_ Farbe<br/>                             | D2D1 \_ Vector \_ 3F<br/> {1.0 f, 1.0 f, 1.0 f}<br/>                                   | Die Farbe des eingehenden Lichts. Diese Eigenschaft wird als Vektor 3 (R, G, B) verfügbar gemacht und zum Berechnen von l<sub>R</sub>, l<sub>G</sub>, l<sub>b</sub>verwendet. <br/>                                                                                                                                                                                                                                         |
| Kernelunitlength<br/> D2D1 \_ spotdiffus \_ \_ - \_ kerneleinheits \_ Länge<br/>   | D2D1 \_ Vector \_ 2F<br/> {1.0 f, 1.0 f}<br/>                                         | Die Größe eines Elements im Sobel-Kernel, das verwendet wird, um die Oberflächen normale in der X-und Y-Richtung zu generieren. Diese Eigenschaft wird den DX-und dy-Werten im Sobel-Farbverlauf zugeordnet. Diese Eigenschaft ist ein D2D1 \_ Vector \_ 2F (Kernel Unit Length X, Kernel Unit Length Y) und wird in (Dips/Kernel Unit) definiert. Der Effekt verwendet die bilineare interpolung, um die Bitmap so zu skalieren, dass Sie mit der Größe der Kernel-Elemente<br/> |
| Skalemode<br/> D2D1 \_ spotdiffuse- \_ Prop- \_ Skalierungs \_ Modus<br/>                   | D2D1 \_ spotdiffuse- \_ Skalierungs \_ Modus<br/> D2D1 \_ spotdiffuse- \_ Skalierungs \_ Modus \_ linear<br/> | Der Interpolations Modus, mit dem das Bild auf die entsprechende Kernel Einheitslänge skaliert wird. Es gibt sechs Skalierungs Modi mit hoher Qualität und Geschwindigkeit. Weitere Informationen finden Sie unter [Skalierungs Modi](#scale-modes) .<br/>                                                                                                                                                                                  |



 

## <a name="scale-modes"></a>Skalierungs Modi



| Enumeration                                           | Beschreibung                                                                                                                                                                                          |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ spotdiffuse- \_ Skalierungs \_ Modus \_ Nächster \_ Nachbar     | Verwendet den nächsten einzelnen Punkt und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das niedrigste Qualitätsbild aus.                                                                           |
| D2D1 \_ spotdiffuse- \_ Skalierungs \_ Modus \_ linear                | Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung. In diesem Modus wird ein Image mit höherer Qualität als nächster Nachbar ausgegeben.                                                                                   |
| D2D1 \_ spotdiffuse \_ Skalierungs \_ Modus ( \_ kubisch)                 | Verwendet einen 16-beispielkubischen Kernel für Interpolationen. In diesem Modus wird die meiste Verarbeitungszeit verwendet, es wird jedoch ein Image mit höherer Qualität ausgegeben.                                                                        |
| D2D1 \_ spotdiffuse \_ Skalierungs \_ Modus \_ \_ Multisample \_ linear | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für eine gute Edge-Antialiasing. Dieser Modus eignet sich gut zum horizontalen Herunterskalieren um kleine Beträge in Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ spotdiffer \_ Skalierungs \_ Modus \_ anisotrope           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu modellieren.                                                                                                     |
| D2D1 \_ spotdiffuse \_ Skalierungs \_ Modus \_ High \_ Quality \_ kubisch  | Verwendet einen kubischen Kernel mit hoher Qualität für eine Variable Größe, um das Abbild vorab zu skalieren, wenn eine downstreamingmatrix an der Transformationsmatrix beteiligt ist. Verwendet dann den kubischen Interpolations Modus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf den D2D1- \_ \_ Modus Lineare Skalierung linear skaliert \_ \_ .

 

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

 

