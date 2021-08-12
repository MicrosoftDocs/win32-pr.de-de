---
description: Es gibt zwei Möglichkeiten, Texturzuordnungen zu codieren, die eine komplexere Transparenz aufweisen.
ms.assetid: cae788f6-60f1-4987-8f06-bf4256bccd9b
title: Texturen mit Alphakanälen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 934660a62c0257de1549ccec09f9bb77e5c02c4c22baf1e1dc9cc8dffef03f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290525"
---
# <a name="textures-with-alpha-channels-direct3d-9"></a>Texturen mit Alphakanälen (Direct3D 9)

Es gibt zwei Möglichkeiten, Texturzuordnungen zu codieren, die eine komplexere Transparenz aufweisen. In jedem Fall steht ein -Block, der die Transparenz beschreibt, vor dem bereits beschriebenen 64-Bit-Block. Die Transparenz wird entweder als 4x4-Bitmap mit 4 Bits pro Pixel (explizite Codierung) oder mit weniger Bits und linearer Interpolation dargestellt, die dem entspricht, was für die Farbcodierung verwendet wird.

Der Transparenzblock und der Farbblock werden wie in der folgenden Tabelle dargestellt angeordnet.



| Word-Adresse | 64-Bit-Block                      |
|--------------|-----------------------------------|
| 3:0          | Transparenzblock                |
| 7:4          | Zuvor beschriebener 64-Bit-Block |



 

## <a name="explicit-texture-encoding"></a>Explizite Texturcodierung

Für die explizite Texturcodierung (DXT2- und DXT3-Formate) werden die Alphakomponenten der Texel, die Transparenz beschreiben, in einer 4x4-Bitmap mit 4 Bits pro Texel codiert. Diese vier Bits können mithilfe einer Vielzahl von Möglichkeiten wie Dithering oder mithilfe der vier wichtigsten Bits der Alphadaten erreicht werden. Sie werden jedoch genauso verwendet, wie sie sind, ohne jegliche Form von Interpolation.

Das folgende Diagramm zeigt einen 64-Bit-Transparenzblock.

![Diagramm eines 64-Bit-Transparenzblocks](images/colors4.png)

> [!Note]  
> Die Komprimierungsmethode von Direct3D verwendet die vier wichtigsten Bits.

 

Die folgenden Tabellen veranschaulichen, wie die Alphainformationen für jedes 16-Bit-Wort im Arbeitsspeicher angeordnet werden.

Diese Tabelle enthält das Layout für Wort 0.



| Bits          | Alpha      |
|---------------|------------|
| 3:0 (LSB \* )   | \[0 \] \[ 0\] |
| 7:4           | \[0 \] \[ 1\] |
| 11:8          | \[0 \] \[ 2\] |
| 15:12 (MSB \* ) | \[0 \] \[ 3\] |



 

\*Am wenigsten signifikantes Bit, wichtigstes Bit (MSB)

Diese Tabelle enthält das Layout für Wort 1.



| Bits        | Alpha      |
|-------------|------------|
| 3:0 (LSB)   | \[1 \] \[ 0\] |
| 7:4         | \[1 \] \[ 1\] |
| 11:8        | \[1 \] \[ 2\] |
| 15:12 (MSB) | \[1 \] \[ 3\] |



 

Diese Tabelle enthält das Layout für Wort 2.



| Bits        | Alpha      |
|-------------|------------|
| 3:0 (LSB)   | \[2 \] \[ 0\] |
| 7:4         | \[2 \] \[ 1\] |
| 11:8        | \[2 \] \[ 2\] |
| 15:12 (MSB) | \[2 \] \[ 3\] |



 

Diese Tabelle enthält das Layout für Wort 3.



| Bits        | Alpha      |
|-------------|------------|
| 3:0 (LSB)   | \[3 \] \[ 0\] |
| 7:4         | \[3 \] \[ 1\] |
| 11:8        | \[3 \] \[ 2\] |
| 15:12 (MSB) | \[3 \] \[ 3\] |



 

Der Unterschied zwischen DXT2 und DXT3 besteht darin, dass im DXT2-Format davon ausgegangen wird, dass die Farbdaten durch Alpha prämultipliziert wurden. Im DXT3-Format wird davon ausgegangen, dass die Farbe nicht durch Alpha prämultipliziert wird. Diese beiden Formate sind erforderlich, da zum Zeitpunkt der Verwendung einer Textur in den meisten Fällen die Untersuchung der Daten nicht ausreicht, um festzustellen, ob die Farbwerte mit alpha multipliziert wurden. Da diese Informationen zur Laufzeit benötigt werden, werden die beiden FOURCC-Codes verwendet, um diese Fälle zu unterscheiden. Die für diese beiden Formate verwendete Daten- und Interpolationsmethode ist jedoch identisch.

Der Farbvergleich, der in DXT1 verwendet wird, um zu bestimmen, ob das Texel transparent ist, wird in diesem Format nicht verwendet. Es wird davon ausgegangen, dass die Farbdaten ohne Farbvergleich immer wie im 4-Farbmodus behandelt werden. Anders ausgedrückt: Die if-Anweisung am Anfang des DXT1-Codes sollte wie folgt sein:


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="three-bit-linear-alpha-interpolation"></a>Three-Bit lineare Alphainterpolation

Die Codierung der Transparenz für die Formate DXT4 und DXT5 basiert auf einem Konzept, das der linearen Codierung für Farben ähnelt. Zwei 8-Bit-Alphawerte und eine 4x4-Bitmap mit drei Bits pro Pixel werden in den ersten acht Bytes des Blocks gespeichert. Die repräsentativen Alphawerte werden verwendet, um Alphazwischenwerte zu interpolieren. Zusätzliche Informationen sind in der Art und Weise verfügbar, wie die beiden Alphawerte gespeichert werden. Wenn Alpha \_ 0 größer als Alpha \_ 1 ist, werden von der Interpolation sechs Alphazwischenwerte erstellt. Andernfalls werden vier Alpha-Zwischenwerte zwischen den angegebenen Alphaext extreme-Werten interpoliert. Die beiden zusätzlichen impliziten Alphawerte sind 0 (vollständig transparent) und 255 (vollständig deckend).

Im folgenden Codebeispiel wird dieser Algorithmus veranschaulicht.


```
// 8-alpha or 6-alpha block?    
if (alpha_0 > alpha_1) {    
    // 8-alpha block:  derive the other six alphas.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (6 * alpha_0 + 1 * alpha_1 + 3) / 7;    // bit code 010
    alpha_3 = (5 * alpha_0 + 2 * alpha_1 + 3) / 7;    // bit code 011
    alpha_4 = (4 * alpha_0 + 3 * alpha_1 + 3) / 7;    // bit code 100
    alpha_5 = (3 * alpha_0 + 4 * alpha_1 + 3) / 7;    // bit code 101
    alpha_6 = (2 * alpha_0 + 5 * alpha_1 + 3) / 7;    // bit code 110
    alpha_7 = (1 * alpha_0 + 6 * alpha_1 + 3) / 7;    // bit code 111  
}    
else {  
    // 6-alpha block.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (4 * alpha_0 + 1 * alpha_1 + 2) / 5;    // Bit code 010
    alpha_3 = (3 * alpha_0 + 2 * alpha_1 + 2) / 5;    // Bit code 011
    alpha_4 = (2 * alpha_0 + 3 * alpha_1 + 2) / 5;    // Bit code 100
    alpha_5 = (1 * alpha_0 + 4 * alpha_1 + 2) / 5;    // Bit code 101
    alpha_6 = 0;                                      // Bit code 110
    alpha_7 = 255;                                    // Bit code 111
}
```



Das Speicherlayout des Alphablocks sieht wie folgt aus:



| Byte | Alpha                                                          |
|------|----------------------------------------------------------------|
| 0    | Alpha \_ 0                                                       |
| 1    | Alpha \_ 1                                                       |
| 2    | \[0 \] \[ 2 \] (2 MSB), \[ 0 \] \[ 1 \] , \[ 0 \] \[ 0\]                    |
| 3    | \[1 \] \[ 1 \] (1 MSB), \[ 1 \] \[ 0 \] , \[ 0 \] \[ 3 \] , \[ 0 \] \[ 2 \] (1 LSB) |
| 4    | \[1 \] \[ 3 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 1 \] (2 LSBs)                    |
| 5    | \[2 \] \[ 2 \] (2 MSBs), \[ 2 \] \[ 1 \] , \[ 2 \] \[ 0\]                    |
| 6    | \[3 \] \[ 1 \] (1 MSB), \[ 3 \] \[ 0 \] , \[ 2 \] \[ 3 \] , \[ 2 \] \[ 2 \] (1 LSB) |
| 7    | \[3 \] \[ 3 \] , \[ 3 \] \[ 2 \] , \[ 3 \] \[ 1 \] (2 LSBs)                    |



 

Der Unterschied zwischen DXT4 und DXT5 besteht darin, dass im DXT4-Format davon ausgegangen wird, dass die Farbdaten durch Alpha prämultipliziert wurden. Im DXT5-Format wird davon ausgegangen, dass die Farbe nicht durch Alpha prämultipliziert wird. Diese beiden Formate sind erforderlich, da zum Zeitpunkt der Verwendung einer Textur in den meisten Fällen die Untersuchung der Daten nicht ausreicht, um festzustellen, ob die Farbwerte mit alpha multipliziert wurden. Da diese Informationen zur Laufzeit benötigt werden, werden die beiden FOURCC-Codes verwendet, um diese Fälle zu unterscheiden. Die für diese beiden Formate verwendete Daten- und Interpolationsmethode ist jedoch identisch.

Der Farbvergleich, der in DXT1 verwendet wird, um zu bestimmen, ob das Texel transparent ist, wird nicht mit diesen Formaten verwendet. Es wird davon ausgegangen, dass die Farbdaten ohne Farbvergleich immer wie im 4-Farbmodus behandelt werden. Mit anderen Worten: Die if-Anweisung am Anfang des DXT1-Codes sollte wie folgend sein:


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komprimierte Texturressourcen](compressed-texture-resources.md)
</dt> </dl>

 

 



