---
title: Beleuchtungseffekt „Entfernt-Diffus“
description: Verwenden Sie das Bild mit der Distanz diffusen Beleuchtung, um ein Bild zu erstellen, das eine nicht reflektierend Bare Oberfläche ist, bei der die helle Quelle aus einer langen Distanz (z. b. der Sonnen-oder Oberfläche) stammt und das Licht in alle Richtungen verstreut ist.
ms.assetid: 981FD58B-0565-4D0E-957C-3ED81BA8A6EB
keywords:
- entfernter diffuses Beleuchtungs Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30d8e7f918c0b1a55e25c18c83e3eff51b75233
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040084"
---
# <a name="distant-diffuse-lighting-effect"></a>Beleuchtungseffekt „Entfernt-Diffus“

Verwenden Sie das Bild mit der Distanz diffusen Beleuchtung, um ein Bild zu erstellen, das eine nicht reflektierend Bare Oberfläche ist, bei der die helle Quelle aus einer langen Distanz (z. b. der Sonnen-oder Oberfläche) stammt und das Licht in alle Richtungen verstreut ist. Dieser Effekt verwendet den Alphakanal als Höhen Zuordnung und beleuchtet das Bild mit einer entfernten Lichtquelle.

Die Farbe der Ausgabe Bitmap ist das Ergebnis der hellen Farbe, der hellen Position und der Oberflächengeometrie des Bilds. Die Alphakanal Ausgabe für jedes Pixel mit diffuses Beleuchtung ist immer 1,0.

Die CLSID für diesen Effekt ist CLSID \_ D2D1DistantDiffuse.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Skalierungs Modi](#scale-modes)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Im folgenden Beispiel werden die Eingabe-und Ausgabe Bilder des entfernter diffusen Beleuchtungs Effekts veranschaulicht.

![Beispiel eines Effekts: Screenshot der Eingabe-und Ausgabe Bilder des entfernten diffusen Beleuchtungs Effekts.](images/distant-diffuse-example.png)

## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azimuth<br/> D2D1 \_ distantdiffuse \_ Prop \_ Azimuth<br/>                       | Der Richtungs Winkel der Lichtquelle in der XY-Ebene relativ zur X-Achse in der punktuturdirektionale Richtung. Die Einheiten liegen in Grad und müssen zwischen 0 und 360 Grad liegen.<br/> Der Typ ist "float".<br/> Der Standardwert ist 0,0 f.<br/>                                                                                                                                                                                                                                                            |
| Elevation<br/> D2D1 \_ distantdiffuse- \_ Prop- \_ herauf Stufung<br/>                   | Der Richtungs Winkel der Lichtquelle in der YZ-Ebene relativ zur Y-Achse in der punktuturdirektionale Richtung. Die Einheiten liegen in Grad und müssen zwischen 0 und 360 Grad liegen. <br/> Der Typ ist "float".<br/> Der Standardwert ist 0,0 f.<br/>                                                                                                                                                                                                                                                           |
| Diffseconstant<br/> D2D1 \_ distantdiffuse- \_ Prop- \_ diff$- \_ Konstante<br/>     | Das Verhältnis zwischen diffuses Reflektion und eingehender Lichtmenge. Diese Eigenschaft muss zwischen 0 und 10.000 liegen und ist unitless. <br/> Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                      |
| Surfakescale<br/> D2D1 \_ distantdiffuse- \_ Prop- \_ Oberflächen \_ Skala<br/>           | Der Skalierungsfaktor in der Z-Richtung. Die Oberflächen Skala ist unitless und muss zwischen 0 und 10.000 liegen.<br/> Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                           |
| Color<br/> D2D1 \_ distantdiffuse- \_ Prop- \_ Farbe<br/>                           | Die Farbe des eingehenden Lichts. Diese Eigenschaft wird als D2D1 \_ Vector \_ 3F (R, G, B) verfügbar gemacht und zum Berechnen von l<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>verwendet. <br/> Der Typ ist "D2D1 \_ Vector \_ 3F".<br/> Der Standardwert ist {1.0 f, 1.0 f, 1.0 f}.<br/>                                                                                                                                                                                                                                                         |
| Kernelunitlength<br/> D2D1 \_ distantdiffuse \_ Prop \_ -Kernel \_ Einheits \_ Länge<br/> | Die Größe eines Elements im Sobel-Kernel, das verwendet wird, um die Oberflächen normale in der X-und Y-Richtung zu generieren. Diese Eigenschaft wird den DX-und dy-Werten im Sobel-Farbverlauf zugeordnet. Diese Eigenschaft ist ein D2D1 \_ Vector \_ 2F (Kernel Unit Length X, Kernel Unit Length Y) und wird in (geräteunabhängige Pixel (Dips)/Kernel Unit) definiert. Der Effekt verwendet die bilineare interpolung, um die Bitmap so zu skalieren, dass Sie mit der Größe der Kernel-Elemente <br/> Der Typ ist "D2D1 \_ Vector \_ 2F".<br/> Der Standardwert ist {1.0 f, 1.0 f}.<br/> |
| Skalemode<br/> D2D1 \_ distantdiffuse- \_ Prop- \_ Skalierungs \_ Modus<br/>                 | Der Interpolations Modus, mit dem das Bild auf die entsprechende Kernel Einheitslänge skaliert wird. Es gibt sechs Skalierungs Modi mit hoher Qualität und Geschwindigkeit.<br/> Der Typ ist der D2D1 \_ distantdiffuse- \_ Skalierungs \_ Modus.<br/> Der Standardwert ist D2D1 \_ distantdiffuse \_ Scale \_ Mode \_ linear.<br/>                                                                                                                                                                                                                 |



 

## <a name="scale-modes"></a>Skalierungs Modi



| Enumeration                                              | Beschreibung                                                                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ distantdiffer \_ Skalierungs \_ Modus \_ Nächster \_ Nachbar     | Verwendet den nächsten einzelnen Punkt und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das niedrigste Qualitätsbild aus.                                                                           |
| D2D1 \_ distantdiffer \_ Skalierungs \_ Modus \_ linear                | Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung. In diesem Modus wird ein Image mit höherer Qualität als nächster Nachbar ausgegeben.                                                                                   |
| D2D1 \_ distantdiffuse \_ Skalierungs \_ Modus ( \_ kubisch)                 | Verwendet einen 16-beispielkubischen Kernel für Interpolationen. In diesem Modus wird die meiste Verarbeitungszeit verwendet, es wird jedoch ein Image mit höherer Qualität ausgegeben.                                                                        |
| D2D1 \_ distantdiffuse \_ \_ Skalierungsmodus- \_ \_ Multisample \_ linear | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für eine gute Edge-Antialiasing. Dieser Modus eignet sich gut zum horizontalen Herunterskalieren um kleine Beträge in Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ distantdiffer \_ Skalierungs \_ Modus \_ anisotrope           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu modellieren.                                                                                                     |
| D2D1 \_ distantdiffuse \_ Skalierungs \_ Modus \_ High \_ Quality \_ kubisch  | Verwendet einen kubischen Kernel mit hoher Qualität für eine Variable Größe, um das Abbild vorab zu skalieren, wenn eine downstreamingmatrix an der Transformationsmatrix beteiligt ist. Verwendet dann den kubischen Interpolations Modus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf D2D1 \_ distantdiffer \_ Scale \_ Mode \_ linear.

 
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

 

