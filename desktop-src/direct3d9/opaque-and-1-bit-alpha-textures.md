---
description: Das Texturformat DXT1 ist für Texturen, die nicht transparent sind oder eine einzelne transparente Farbe aufweisen.
ms.assetid: a890ed0a-1f68-45b8-93cb-b621d1908d9f
title: Nicht transparente und 1-Bit-Alphatextur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda620810e48cba519322f3f2426555443fb696f524f4fbe7752a8c7aaedba73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728188"
---
# <a name="opaque-and-1-bit-alpha-textures-direct3d-9"></a>Nicht transparente und 1-Bit-Alphatextur (Direct3D 9)

Das Texturformat DXT1 ist für Texturen, die nicht transparent sind oder eine einzelne transparente Farbe aufweisen.

Für jeden nicht transparenten oder 1-Bit-Alphablock werden zwei 16-Bit-Werte (RGB-Format 5:6:5) und eine 4x4-Bitmap mit 2 Bits pro Pixel gespeichert. Dies beträgt 64 Bits für 16 Texel bzw. vier Bits pro Texel. In der Blockbitmap gibt es 2 Bits pro Texel, um zwischen den vier Farben auszuwählen, von denen zwei in den codierten Daten gespeichert sind. Die anderen beiden Farben werden von diesen gespeicherten Farben durch lineare Interpolation abgeleitet. Dieses Layout ist im folgenden Diagramm dargestellt.

![Diagramm des Bitmaplayouts](images/colors1.png)

Das 1-Bit-Alphaformat unterscheidet sich vom nicht transparenten Format, indem die beiden im -Block gespeicherten 16-Bit-Farbwerte verglichen werden. Sie werden als ganze Zahlen ohne Vorzeichen behandelt. Wenn die erste Farbe größer als die zweite ist, impliziert dies, dass nur nicht transparente Texel definiert sind. Dies bedeutet, dass vier Farben verwendet werden, um die Texel zu darstellen. Bei der Codierung mit vier Farben gibt es zwei abgeleitete Farben, und alle vier Farben werden gleichmäßig im RGB-Farbraum verteilt. Dieses Format entspricht dem RGB-Format 5:6:5. Andernfalls werden für die 1-Bit-Alphatransparenz drei Farben verwendet, und die vierte farbe ist für die Darstellung transparenter Texel reserviert.

Bei der Codierung mit drei Farben gibt es eine abgeleitete Farbe, und der vierte 2-Bit-Code ist reserviert, um ein transparentes Texel (Alphainformationen) anzugeben. Dieses Format entspricht RGBA 5:5:5:1, wobei das letzte Bit zum Codieren der Alphamaske verwendet wird.

Das folgende Codebeispiel veranschaulicht den Algorithmus für die Entscheidung, ob die Codierung mit drei oder vier Farben ausgewählt ist:


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



Es wird empfohlen, die RGBA-Komponenten des Transparenzpixels vor dem Mischen auf 0 (null) zu setzen.

Die folgenden Tabellen zeigen das Speicherlayout für den 8-Byte-Block. Es wird davon ausgegangen, dass der erste Index der y-Koordinate und der zweite der x-Koordinate entspricht. Texel 1 2 bezieht sich beispielsweise auf das \[ \] \[ \] Texturzuordnungspixel bei (x,y) = (2,1).

Diese Tabelle enthält das Speicherlayout für den 8-Byte-Block (64-Bit).



| Word-Adresse | 16-Bit-Wort    |
|--------------|----------------|
| 0            | Farbe \_ 0       |
| 1            | Farbe \_ 1       |
| 2            | Bitmap Word \_ 0 |
| 3            | Bitmap Word \_ 1 |



 

Farbe 0 und Farbe 1, die Farben an den \_ beiden Extremen, werden wie folgt \_ dargestellt:



| Bits        | Color                 |
|-------------|-----------------------|
| 4:0 (LSB \* ) | Blaufarbenkomponente  |
| 10:5        | Komponente "Grüne Farbe" |
| 15:11       | Komponente "Rote Farbe"   |



 

\*Bit mit der geringsten Bedeutung

Bitmap Word \_ 0 ist wie folgt ausgelegt:



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



 

\*wichtigstes Bit (MSB)

Bitmap Word \_ 1 ist wie folgt ausgelegt:



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



 

## <a name="example-of-opaque-color-encoding"></a>Beispiel für Opaque Color Encoding

Als Beispiel für die opake Codierung wird davon ausgegangen, dass die Farben Rot und Schwarz extrem sind. Rot ist Die \_ Farbe 0 und Schwarz die \_ Farbe 1. Es gibt vier interpolierte Farben, die den gleichmäßig verteilten Farbverlauf zwischen ihnen bilden. Um die Werte für die 4x4-Bitmap zu bestimmen, werden die folgenden Berechnungen verwendet:


```
00 ? color_0
01 ? color_1
10 ? 2/3 color_0 + 1/3 color_1
11 ? 1/3 color_0 + 2/3 color_1
```



Die Bitmap sieht dann wie im folgenden Diagramm aus.

![Diagramm, das das erweiterte Bitmaplayout zeigt.](images/colors2.png)

Dies sieht wie die folgende dargestellte Reihe von Farben aus.

> [!Note]  
> In einem Bild wird pixel (0,0) oben links angezeigt.

 

![Abbildung eines nicht transparenten codierten Farbverlaufs](images/redsquares.png)

## <a name="example-of-1-bit-alpha-encoding"></a>Beispiel für 1-Bit-Alphacodierung

Dieses Format wird ausgewählt, wenn die 16-Bit-Ganzzahl ohne Vorzeichen , Farbe 0, kleiner als die \_ 16-Bit-Ganzzahl ohne Vorzeichen, Farbe \_ 1, ist. Ein Beispiel dafür, wo dieses Format verwendet werden kann, sind Blätter in einer Struktur, die an einem blauen Himmel dargestellt werden. Einige Texel können als transparent markiert werden, während drei Grünschattierungen für die Blätter weiterhin verfügbar sind. Zwei Farben beheben die Extreme, und die dritte ist eine interpolierte Farbe.

Die folgende Abbildung ist ein Beispiel für ein solches Bild.

![Abbildung der 1-Bit-Alphacodierung](images/greenthing.png)

Beachten Sie, dass das Texel als transparent codiert wird, wenn das Bild weiß angezeigt wird. Beachten Sie außerdem, dass die RGBA-Komponenten der transparenten Texel vor dem Mischen auf 0 (null) festgelegt werden sollten.

Die Bitmapcodierung für die Farben und die Transparenz wird mithilfe der folgenden Berechnungen bestimmt.


```
00 ? color_0
01 ? color_1
10 ? 1/2 color_0 + 1/2 color_1
11   ?   Transparent
```



Die Bitmap sieht dann wie im folgenden Diagramm aus.

![Diagramm des erweiterten Bitmaplayouts](images/colors3.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komprimierte Texturressourcen](compressed-texture-resources.md)
</dt> </dl>

 

 



