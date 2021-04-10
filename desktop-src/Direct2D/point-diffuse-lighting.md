---
title: Beleuchtungseffekt „Punkt-Diffus“
description: Verwenden Sie die Beleuchtung mit Punkt diffuses Beleuchtung, um ein Bild zu erstellen, das eine nicht reflektive Oberfläche ist, bei der das Licht in alle Richtungen verstreut ist. Dieser Effekt verwendet den Alphakanal als Höhen Zuordnung und beleuchtet das Bild mit einer Punktlicht Quelle.
ms.assetid: C98A4962-B9EB-4095-9AC4-F1C32C574892
keywords:
- Punkt diffuses Beleuchtungs Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de97edfa6c2166d5c29649aabfe97761440f8f18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040883"
---
# <a name="point-diffuse-lighting-effect"></a>Beleuchtungseffekt „Punkt-Diffus“

Verwenden Sie die Beleuchtung mit Punkt diffuses Beleuchtung, um ein Bild zu erstellen, das eine nicht reflektive Oberfläche ist, bei der das Licht in alle Richtungen verstreut ist. Dieser Effekt verwendet den Alphakanal als Höhen Zuordnung und beleuchtet das Bild mit einer Punktlicht Quelle.

Die Farbe der Ausgabe Bitmap ist das Ergebnis der hellen Farbe, der hellen Position und der Oberflächengeometrie. Die Alphakanal Ausgabe für jedes Pixel mit diffuses Beleuchtung ist immer 1,0.

Die CLSID für diesen Effekt ist CLSID \_ D2D1PointDiffuse. Um diesen Effekt zu verwenden, fügen Sie dxguid. lib den Linker-Abhängigkeiten hinzu.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Skalierungs Modi](#scale-modes)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Im folgenden Beispiel werden die Eingabe-und Ausgabe Bilder des Punkt diffusen Beleuchtungs Effekts veranschaulicht.

![ein Screenshot mit Beispiel Effekten, der die Eingabe-und Ausgabe Bilder des Lichteffekts der Punkt-diffuses anzeigt.](images/point-diffuse-example.png)

Diffuses Beleuchtung bezieht sich auf Licht, das in mehrere Richtungen reflektiert wird, wie hier gezeigt.

![diffuses Beleuchtungs Licht ist in alle Richtungen verstreut.](images/point-diffuse-lighting.png)

Der Effekt berechnet die endgültigen Ausgabe Pixelwerte werden mithilfe dieser Gleichungen berechnet:

![Ausgabe Bitmap-Berechnungen.](images/point-diffuse-formula1.png)

Hierbei gilt:<dl> k<sub>d</sub> = diffuses Beleuchtungs Konstante. Wird vom Benutzer angegeben.  
![Oberflächen normales Vektorsymbol.](images/point-spec-mathchar-n.png) = Oberflächen normaler Einheits Vektor, eine Funktion von x und y.  
![Einheits Vektorsymbol.](images/distant-spec-mathchar-l.png) = Einheits Vektor, der von der Oberfläche auf das Licht zeigt.  
L<sub>r</sub>, l<sub>g</sub>, l<sub>b</sub> = die helle Farbe in RGB-Komponenten.  
</dl>

## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lightposition<br/> D2D1 \_ pointdiffuse- \_ Prop- \_ Licht \_ Position<br/>         | Die helle Position der Punktlicht Quelle. Die-Eigenschaft ist ein \_ \_ als (x, y, z) definiertes D2D1 Vector 3f. Die Einheiten befinden sich in geräteunabhängigen Pixeln (Dips) und sind unbegrenzt. <br/> Der Typ ist "D2D1 \_ Vector \_ 3F".<br/> Der Standardwert ist {0,0 f, 0,0 f, 0,0 f}.<br/>                                                                                                                                                                                                              |
| Diffseconstant<br/> D2D1 \_ pointdiffuse \_ Prop \_ - \_ Konstante Konstante<br/>     | Das Verhältnis zwischen diffuses Reflektion und eingehender Lichtmenge. Diese Eigenschaft muss zwischen 0 und 10.000 liegen und ist unitless. <br/> Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                          |
| Surfakescale<br/> D2D1 \_ pointdiffuse- \_ Prop- \_ Oberflächen \_ Skala<br/>           | Der Skalierungsfaktor in der Z-Richtung. Die Oberflächen Skala ist unitless und muss zwischen 0 und 10.000 liegen.<br/> Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                                               |
| Color<br/> D2D1 \_ pointdiffuse- \_ Prop- \_ Farbe<br/>                           | Die Farbe des eingehenden Lichts. Diese Eigenschaft wird als Vektor 3 (R, G, B) verfügbar gemacht und zum Berechnen von l<sub>R</sub>, l<sub>G</sub>, l<sub>b</sub>verwendet. <br/> Der Typ ist "D2D1 \_ Vector \_ 3F".<br/> Der Standardwert ist {1.0 f, 1.0 f, 1.0 f}.<br/>                                                                                                                                                                                                                                     |
| Kernelunitlength<br/> D2D1 \_ pointdiffuse \_ Prop \_ -Kernel \_ Einheits \_ Länge<br/> | Die Größe eines Elements im Sobel-Kernel, das verwendet wird, um die Oberflächen normale in der X-und Y-Richtung zu generieren. Diese Eigenschaft wird den DX-und dy-Werten im Sobel-Farbverlauf zugeordnet. Diese Eigenschaft ist ein D2D1 \_ Vector \_ 2F (Kernel Unit Length X, Kernel Unit Length Y) und wird in (Dips/Kernel Unit) definiert. Der Effekt verwendet die bilineare interpolung, um die Bitmap so zu skalieren, dass Sie mit der Größe der Kernel-Elemente <br/> Der Typ ist "D2D1 \_ Vector \_ 2F".<br/> Der Standardwert ist {1.0 f, 1.0 f}.<br/> |
| Skalemode<br/> D2D1 \_ pointdiffuse- \_ Prop- \_ Skalierungs \_ Modus<br/>                 | Der Interpolations Modus, mit dem das Bild auf die entsprechende Kernel Einheitslänge skaliert wird. Es gibt sechs Skalierungs Modi mit hoher Qualität und Geschwindigkeit. Weitere Informationen finden Sie unter [Skalierungs Modi](#scale-modes) . <br/> Der Typ ist der D2D1 \_ pointdiffuse- \_ Skalierungs \_ Modus.<br/> Der Standardwert ist D2D1 \_ pointdiffuse \_ Scale \_ Mode \_ linear.<br/>                                                                                                                                         |



 

## <a name="scale-modes"></a>Skalierungs Modi



| Enumeration                                            | Beschreibung                                                                                                                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ pointdiffuse- \_ Skalierungs \_ Modus \_ Nächster \_ Nachbar     | Verwendet den nächsten einzelnen Punkt und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das niedrigste Qualitätsbild aus.                                                                           |
| D2D1 \_ pointdiffuse- \_ Skalierungs \_ Modus \_ linear                | Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung. In diesem Modus wird ein Image mit höherer Qualität als nächster Nachbar ausgegeben.                                                                                   |
| D2D1 \_ pointdiffuse \_ Skalierungs \_ Modus ( \_ kubisch)                 | Verwendet einen 16-beispielkubischen Kernel für Interpolationen. In diesem Modus wird die meiste Verarbeitungszeit verwendet, es wird jedoch ein Image mit höherer Qualität ausgegeben.                                                                        |
| D2D1 \_ pointdiffuse \_ Scale \_ Mode \_ \_ Multisample \_ linear | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für eine gute Edge-Antialiasing. Dieser Modus eignet sich gut zum horizontalen Herunterskalieren um kleine Beträge in Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ pointdiffer \_ Skalierungs \_ Modus \_ anisotrope           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu modellieren.                                                                                                     |
| D2D1 \_ pointdiffuse \_ Skalierungs \_ Modus \_ High \_ Quality \_ kubisch  | Verwendet einen kubischen Kernel mit hoher Qualität für eine Variable Größe, um das Abbild vorab zu skalieren, wenn eine downstreamingmatrix an der Transformationsmatrix beteiligt ist. Verwendet dann den kubischen Interpolations Modus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf den D2D1 \_ pointdiffuse- \_ Skalierungs \_ Modus linear festgelegt \_ .

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

 

