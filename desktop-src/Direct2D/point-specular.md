---
title: Beleuchtungseffekt „Punkt-Spiegelnd“
description: Verwenden Sie den Punkt Glanz der Beleuchtung, um ein Bild zu erstellen, das zu einer reflektierenden Oberfläche erscheint.
ms.assetid: 89E22FD0-BB7F-465F-A79C-056CA9F14F5D
keywords:
- Glanz der Punkt Glanz Beleuchtung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 355c573888604af8dfac443f4f53554a8a780071
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956785"
---
# <a name="point-specular-lighting-effect"></a>Beleuchtungseffekt „Punkt-Spiegelnd“

Verwenden Sie den Punkt Glanz der Beleuchtung, um ein Bild zu erstellen, das zu einer reflektierenden Oberfläche erscheint. Der Effekt verwendet den Alpha-Kanal des Bilds als Höhen Zuordnung und eine Point Light-Quelle, die Sie positionieren, und berechnet die Reflektion und das Licht entsprechend dem Glanz Bereich des Phong-Beleuchtungs Modells.

Die Farbe der Ausgabe Bitmap ist das Ergebnis der hellen Farbe, der hellen Position und der Oberflächengeometrie. Die Alphakanal Ausgabe für jedes Pixel mit Glanz Beleuchtung ist der Höchstwert der roten, grünen und blauen Kanal Ausgaben für dieses Pixel.

Die CLSID für diesen Effekt ist CLSID \_ D2D1PointSpecular.

-   [Beispiel Bild](#example-image)
-   [Point Light-Quelle](#point-light-source)
-   [Height Map und normaler Vektor](#height-map-and-normal-vector)
-   [Glanz Beleuchtungs Konstante und Exponent](#specular-lighting-constant-and-exponent)
-   [Effekt Eigenschaften](#effect-properties)
-   [Skalierungs Modi](#scales-modes)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Im folgenden Beispiel werden die Eingabe-und Ausgabe Bilder des Punkt-Glanz-Beleuchtungs Effekts veranschaulicht.

![Bildschirm Abbildung des Effekts Beispiels, das die Eingabe-und Ausgabe Bilder des Glanzlicht Effekts der Punkte zeigt.](images/point-spec-example.png)

Glanzlicht bezieht sich auf das Licht, das in einer bestimmten Richtung entsprechend dem Phong-Beleuchtungsmodell reflektiert wird.

![ein Diagramm der Vektoren, die verwendet werden, um eine Glanzlicht Ausgabe für eine Bitmap zu verwenden.](images/point-spec-reflected1.png)

Der Effekt berechnet die endgültigen Ausgabe Pixelwerte mithilfe der Gleichungen hier:

![die Gleichungen zum Berechnen der endgültigen Pixelwerte. ](images/point-spec-formula-output.png)

where<dl> km? = Glanz Beleuchtungs Konstante.  
![das Oberflächen normale Einheits Vektorsymbol. ](images/point-spec-mathchar-n.png) = Oberflächen normaler Einheits Vektor, der eine Funktion von x und y ist. Die Berechnungen finden Sie unter [height Map und normaler Vektor](#height-map-and-normal-vector) .  
![das Symbol für die halbe Einheits Vektor. ](images/point-spec-mathchar-h.png) = "halber" Einheits Vektor zwischen dem Augen Einheiten Vektor und dem hellen Einheits Vektor. Die Berechnungen finden Sie unter [Point Light Source](#point-light-source) .  
L<sub>r</sub>, l<sub>g</sub>, l<sub>b</sub> = die helle Farbe in RGB-Komponenten.  
</dl>

Sie legen die Glanzlicht Konstante als " *specularconstant* "-Eigenschaft und die helle Farbe als *Farb* Eigenschaft fest.

## <a name="point-light-source"></a>Point Light-Quelle

Eine Point Light-Quelle gibt Licht in alle Richtungen wie im Bild aus.

![ein Punktlicht, das Licht in alle Richtungen ausgibt.](images/point-spec-light.png)

Sie legen die Position der Lichtquelle mithilfe der *lightposition* -Eigenschaft fest. Der Effekt berechnet den hellen Vektor L für eine Punktlicht Quelle mithilfe der Gleichungen hier:

![die helle Vektor Gleichung.](images/point-spec-formula3.png)

Where Light?, Light<sub>y</sub>und Light<sub>z</sub> sind die Eingabe Lichtposition. Der Effekt berechnet den halb Vektor, das ![ halbe Vektorsymbol.](images/point-spec-mathchar-h.png) wie im Phong-Beleuchtungsmodell definiert, mit der Gleichung hier. Das Beleuchtungsmodell geht davon aus, dass sich der Augen Vektor, ![ das Augen Vektorsymbol ](images/point-spec-mathchar-e.png) , unter (0, 0, 1) befindet.

![halbe Vektor Gleichung.](images/point-spec-formula4.png)

Sowohl L als auch H werden zu Vektoren der Einheitslänge normalisiert.

## <a name="height-map-and-normal-vector"></a>Height Map und normaler Vektor

Der Effekt generiert eine Höhen Zuordnung für das Eingabebild basierend auf seinem Alphakanal.

Die Height (Z)-Komponente wird mit der Gleichung berechnet:

![die Gleichung für die Berechnung der Höhe (z) der Oberfläche.](images/point-spec-formula6.png)

Der Effekt berechnet die Oberflächen normale, ![das normale Vektorsymbol.](images/point-spec-mathchar-n.png), für die Eingabe Bitmap mithilfe eines Sobel-Farbverlaufs.

## <a name="specular-lighting-constant-and-exponent"></a>Glanz Beleuchtungs Konstante und Exponent

Glanzlicht stellt das Licht dar, das sich von der Oberfläche der Bild Höhen Zuordnung widerspiegelt. Sie geben die *specularexponent* -Eigenschaft an, die den Umfang der Glanz Reflektion aus der Bitmap bestimmt.

Größere Exponenten stellen shinier Ende Objekte dar und reflektieren das Licht in einer stärker fokussierten Form.

Die *specularconstant* -Eigenschaft K? definiert den Umfang der reflektierten Beleuchtung als Verhältnis des eingehenden Lichts.

## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lightposition<br/> D2D1 \_ pointspecweightprop- \_ \_ Licht \_ Position<br/>         | Die helle Position der Punktlicht Quelle. Die-Eigenschaft ist ein \_ \_ als (x, y, z) definiertes D2D1 Vector 3f. Die Einheiten befinden sich in geräteunabhängigen Pixeln (Dips), und die Werte sind unitless und unbegrenzt. Der Typ ist "D2D1 \_ Vector \_ 3F".<br/> Der Standardwert ist {0,0 f, 0,0 f, 0,0 f}.<br/>                                                                                                                                                                                      |
| Specularexponent<br/> D2D1 \_ pointspecfeiner \_ Prop- \_ \_ Exponent<br/>   | Der Exponent für den Glanz Ausdruck in der Phong-Beleuchtungs Gleichung. Ein größerer Wert entspricht einer stärker reflektierenden Oberfläche. Dieser Wert ist unitless und muss zwischen 1,0 und 128 liegen. Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                               |
| Specularconstant<br/> D2D1 \_ pointspecarität-Konstante, Glanz \_ \_ \_ Konstante<br/>   | Das Verhältnis der Glanz Reflektion zum eingehenden Licht. Der Wert ist unitless und muss zwischen 0 und 10.000 liegen. Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                                   |
| Surfakescale<br/> D2D1 \_ pointspecfeiner \_ Prop- \_ Oberflächen \_ Skala<br/>           | Der Skalierungsfaktor in der Z-Richtung zum Erstellen einer Höhen Zuordnung. Der Wert ist unitless und muss zwischen 0 und 10.000 liegen. Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                          |
| Color<br/> D2D1 \_ pointspecfeiner \_ Prop- \_ Farbe<br/>                           | Die Farbe des eingehenden Lichts. Diese Eigenschaft wird als D2D1 \_ Vector \_ 3F (R, G, B) verfügbar gemacht und zum Berechnen von l<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>verwendet. Der Typ ist "D2D1 \_ Vector \_ 3F".<br/> Der Standardwert ist {1.0 f, 1.0 f, 1.0 f}.<br/>                                                                                                                                                                                                                             |
| Kernelunitlength<br/> D2D1 \_ pointspecfeiner \_ Prop \_ -Kernel \_ Einheits \_ Länge<br/> | Die Größe eines Elements im Sobel-Kernel, das verwendet wird, um die Oberflächen normale in der X-und Y-Richtung zu generieren. Diese Eigenschaft wird den DX-und dy-Werten im Sobel-Farbverlauf zugeordnet. Diese Eigenschaft ist ein D2D1 \_ Vector \_ 2F (Kernel Unit Length X, Kernel Unit Length Y) und wird in (Dips/Kernel Unit) definiert. Der Effekt verwendet die bilineare interpolung, um die Bitmap so zu skalieren, dass Sie mit der Größe der Kernel-Elemente Der Typ ist "D2D1 \_ Vector \_ 2F".<br/> Der Standardwert ist {1.0 f, 1.0 f}.<br/> |
| Skalemode<br/> D2D1 \_ pointspecfeiner- \_ Prop- \_ Skalierungs \_ Modus<br/>                 | Der Interpolations Modus, mit dem das Bild auf die entsprechende Kernel Einheitslänge skaliert wird. Es gibt sechs Skalierungs Modi mit hoher Qualität und Geschwindigkeit. Weitere Informationen finden Sie unter [Skalierungs Modi](#scales-modes) . <br/> Der Typ ist der D2D1 \_ pointspecarität- \_ Skalierungs \_ Modus.<br/> Der Standardwert ist D2D1 \_ pointspecscale \_ \_ Mode \_ linear.<br/>                                                                                                                          |



 

## <a name="scales-modes"></a>Skalierungs Modi



| Enumeration                                             | Beschreibung                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ pointspecstem \_ Scale \_ Mode \_ Nächster \_ Nachbar     | Verwendet den nächsten einzelnen Punkt und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das niedrigste Qualitätsbild aus.                                                                           |
| D2D1 \_ pointspecscale \_ \_ Mode \_ linear                | Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung. In diesem Modus wird ein Image mit höherer Qualität als nächster Nachbar ausgegeben.                                                                                   |
| D2D1 \_ pointspecfeiner \_ Skalierungs \_ Modus ( \_ kubisch)                 | Verwendet einen 16-beispielkubischen Kernel für Interpolationen. In diesem Modus wird die meiste Verarbeitungszeit verwendet, es wird jedoch ein Image mit höherer Qualität ausgegeben.                                                                        |
| D2D1 \_ pointspecfeiner \_ Scale \_ Mode \_ \_ Multisample \_ linear | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für eine gute Edge-Antialiasing. Dieser Modus eignet sich gut zum horizontalen Herunterskalieren um kleine Beträge in Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ pointspecarität- \_ Skalierungs \_ Modus \_ anisotrope           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu modellieren.                                                                                                     |
| D2D1 \_ pointspecscale \_ \_ Mode \_ High \_ Quality \_ kubisch  | Verwendet einen kubischen Kernel mit hoher Qualität für eine Variable Größe, um das Abbild vorab zu skalieren, wenn eine downstreamingmatrix an der Transformationsmatrix beteiligt ist. Verwendet dann den kubischen Interpolations Modus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf D2D1 \_ \_ pointspecscale \_ Mode \_ linear festgelegt.

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

 

