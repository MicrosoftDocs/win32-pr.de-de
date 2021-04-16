---
description: Textur Format DXT1 ist für Texturen, die nicht transparent sind oder eine einzelne transparente Farbe aufweisen.
ms.assetid: a890ed0a-1f68-45b8-93cb-b621d1908d9f
title: Undurchsichtige und 1-Bit-Alpha Texturen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f629eff594d28d9a807021c0b9df0bd05ea66c3
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104553148"
---
# <a name="opaque-and-1-bit-alpha-textures-direct3d-9"></a>Undurchsichtige und 1-Bit-Alpha Texturen (Direct3D 9)

Textur Format DXT1 ist für Texturen, die nicht transparent sind oder eine einzelne transparente Farbe aufweisen.

Für jeden opaken oder 1-Bit-Alpha Block werden 2 16-Bit-Werte (RGB 5:6:5-Format) und eine 4X4-Bitmap mit 2 Bits pro Pixel gespeichert. Dies ergibt 64 Bits für 16 texeln oder vier Bits pro textteln. In der Block Bitmap gibt es zwei Bits pro Texttypen, die zwischen den vier Farben ausgewählt werden sollen, von denen zwei in den codierten Daten gespeichert sind. Die anderen beiden Farben werden von diesen gespeicherten Farben durch lineare Interpolationen abgeleitet. Dieses Layout ist im folgenden Diagramm dargestellt.

![Diagramm des Bitmap-Layouts](images/colors1.png)

Das 1-Bit-Alpha Format unterscheidet sich vom nicht transparenten Format durch Vergleichen der im-Block gespeicherten 2 16-Bit-Farbwerte. Sie werden als ganze Zahlen ohne Vorzeichen behandelt. Wenn die erste Farbe größer als die zweite ist, bedeutet dies, dass nur nicht transparente texeln definiert werden. Dies bedeutet, dass vier Farben zur Darstellung der Texels verwendet werden. Bei der vierfarbigen Codierung gibt es zwei abgeleitete Farben, und alle vier Farben sind gleichmäßig im RGB-Farbraum verteilt. Dieses Format entspricht dem RGB-5:6:5-Format. Andernfalls werden für eine 1-Bit-Alpha Transparenz drei Farben verwendet, und die vierte ist für die Darstellung transparenter texeln reserviert.

Bei der drei-Farben-Codierung gibt es eine abgeleitete Farbe, und der vierte 2-Bit-Code ist für die Angabe einer transparenten Texttyp (Alpha Information) reserviert. Dieses Format entspricht RGBA 5:5:5:1, wobei das abschließende Bit zum Codieren der Alpha Maske verwendet wird.

Das folgende Codebeispiel veranschaulicht den Algorithmus für die Entscheidung, ob drei-oder vierfarbige Codierungen ausgewählt sind:


```
if (color_0 > color_1) 
{
    // Four-color block: derive the other two colors.    
    // 00 = color_0, 01 = color_1, 10 = color_2, 11 = color_3
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block.
    color_2 = (2 * color_0 + color_1 + 1) / 3;
    color_3 = (color_0 + 2 * color_1 + 1) / 3;
}    
else
{ 
    // Three-color block: derive the other color.
    // 00 = color_0,  01 = color_1,  10 = color_2,  
    // 11 = transparent.
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block. 
    color_2 = (color_0 + color_1) / 2;    
    color_3 = transparent;    

}
```



Es wird empfohlen, vor dem mischen die RGBA-Komponenten des Transparenz Pixels auf 0 (null) festzulegen.

In den folgenden Tabellen wird das Speicher Layout für den 8-Byte-Block angezeigt. Es wird davon ausgegangen, dass der erste Index der y-Koordinate entspricht und der zweite der x-Koordinate entspricht. Beispielsweise verweist Texel \[ 1 \] \[ 2 \] auf das Textur Karten Pixel bei (x, y) = (2, 1).

Diese Tabelle enthält das Speicher Layout für den 8-Byte-Block (64 Bit).



| Word-Adresse | 16-Bit-Wort    |
|--------------|----------------|
| 0            | Farbe \_ 0       |
| 1            | Farbe \_ 1       |
| 2            | Bitmap Wort \_ 0 |
| 3            | Bitmap Word \_ 1 |



 

Farbe \_ 0 und Farbe \_ 1, die Farben in den zwei extremen, werden wie folgt angeordnet:



| Bits        | Color                 |
|-------------|-----------------------|
| 4:0 (LSB \* ) | Blaue Farbkomponente  |
| 10:5        | Grüne Farbkomponente |
| 15:11       | Rote Farbkomponente   |



 

\*unbedeutsames Bit

Das Bitmap-Wort \_ 0 wird wie folgt festgelegt:



| Bits          | Texel           |
|---------------|-----------------|
| 1:0 (LSB)     | Texel \[ 0 \] \[ 0\] |
| 3:2           | Texel \[ 0 \] \[ 1\] |
| 5:4           | Texel \[ 0 \] \[ 2\] |
| 7:6           | Texel \[ 0 \] \[ 3\] |
| 9:8           | Texel \[ 1 \] \[ 0\] |
| 11:10         | Texel \[ 1 \] \[ 1\] |
| 13:12         | Texel \[ 1 \] \[ 2\] |
| 15:14 (MSB \* ) | Texel \[ 1 \] \[ 3\] |



 

\*signifikantes Bit (MSB)

Bitmap Word \_ 1 wird wie folgt angeordnet:



| Bits        | Texel           |
|-------------|-----------------|
| 1:0 (LSB)   | Texel \[ 2 \] \[ 0\] |
| 3:2         | Texel \[ 2 \] \[ 1\] |
| 5:4         | Texel \[ 2 \] \[ 2\] |
| 7:6         | Texel \[ 2 \] \[ 3\] |
| 9:8         | Texel \[ 3 \] \[ 0\] |
| 11:10       | Texel \[ 3 \] \[ 1\] |
| 13:12       | Texel \[ 3 \] \[ 2\] |
| 15:14 (MSB) | Texel \[ 3 \] \[ 3\] |



 

## <a name="example-of-opaque-color-encoding"></a>Beispiel für nicht transparente Farbcodierung

Nehmen Sie als Beispiel für die nicht transparente Codierung an, dass die Farben rot und schwarz die extreme sind. Rot ist Farbe \_ 0, schwarz ist Farbe \_ 1. Es gibt vier interpoliert Farben, die den gleichmäßig verteilten Farbverlauf zwischen Ihnen bilden. Zum Ermitteln der Werte für die 4X4-Bitmap werden die folgenden Berechnungen verwendet:


```
00 ? color_0
01 ? color_1
10 ? 2/3 color_0 + 1/3 color_1
11 ? 1/3 color_0 + 2/3 color_1
```



Die Bitmap sieht dann wie im folgenden Diagramm aus.

![Diagramm, das das erweiterte bitmaplayout anzeigt.](images/colors2.png)

Dies sieht wie die folgende veranschaulichte Reihe von Farben aus.

> [!Note]  
> In einem Bild wird Pixel (0,0) oben links angezeigt.

 

![Abbildung eines opaken codierten Farbverlaufs](images/redsquares.png)

## <a name="example-of-1-bit-alpha-encoding"></a>Beispiel für 1-Bit-Alpha Codierung

Dieses Format wird ausgewählt, wenn die 16-Bit-Ganzzahl ohne Vorzeichen (Farbe \_ 0) kleiner als die 16-Bit-Ganzzahl ohne Vorzeichen (Farbe 1) ist \_ . Ein Beispiel für die Verwendung dieses Formats ist die Blätter in einer Struktur, die für einen blauen Himmel angezeigt wird. Einige texeln können als transparent gekennzeichnet werden, während drei grüne Schattierungen weiterhin für die Blätter verfügbar sind. Zwei Farben korrigieren das Extreme, das dritte ist eine interinterpolierte Farbe.

In der folgenden Abbildung ist ein Beispiel für ein solches Bild dargestellt.

![Abbildung der 1-Bit-Alpha Codierung](images/greenthing.png)

Beachten Sie, dass die textelist als transparent codiert werden, wenn das Bild als weiß angezeigt wird. Beachten Sie auch, dass die RGBA-Komponenten der transparenten texeln vor dem Mischen auf 0 (null) festgelegt werden sollen.

Die Bitmap-Codierung für die Farben und Transparenz wird anhand der folgenden Berechnungen bestimmt.


```
00 ? color_0
01 ? color_1
10 ? 1/2 color_0 + 1/2 color_1
11   ?   Transparent
```



Die Bitmap sieht dann wie im folgenden Diagramm aus.

![Diagramm des erweiterten bitmaplayouts](images/colors3.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komprimierte Textur Ressourcen](compressed-texture-resources.md)
</dt> </dl>

 

 



