---
description: Es gibt zwei Möglichkeiten, Textur Karten zu codieren, die komplexere Transparenz aufweisen.
ms.assetid: cae788f6-60f1-4987-8f06-bf4256bccd9b
title: Texturen mit Alpha Kanälen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c361b0335ef4f36b4efc9c90c71270e855f5db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104560981"
---
# <a name="textures-with-alpha-channels-direct3d-9"></a>Texturen mit Alpha Kanälen (Direct3D 9)

Es gibt zwei Möglichkeiten, Textur Karten zu codieren, die komplexere Transparenz aufweisen. In jedem Fall wird ein-Block, der die Transparenz vor dem 64-Bit-Block beschreibt, bereits beschrieben. Die Transparenz wird entweder als 4 x 4-Bitmap mit 4 Bits pro Pixel (explizite Codierung) oder mit weniger Bits und linearer Interpolationen dargestellt, die analog zu den für die Farbcodierung verwendeten Funktionen sind.

Der Transparenz Block und der Farbblock werden wie in der folgenden Tabelle dargestellt.



| Word-Adresse | 64-Bit-Block                      |
|--------------|-----------------------------------|
| 3:0          | Transparenz Block                |
| 7:4          | Zuvor beschriebene 64-Bit-Block |



 

## <a name="explicit-texture-encoding"></a>Explizite Textur Codierung

Bei expliziten Textur Codierungen (DXT2-und DXT3-Format) werden die Alpha Komponenten der texeln, die Transparenz beschreiben, in einer 4 x 4-Bitmap mit 4 Bits pro Textteile codiert. Diese vier Bits können durch eine Vielzahl von Methoden erreicht werden, wie z. b. das Dithering oder die Verwendung der vier wichtigsten Bits der Alpha Daten. Sie werden jedoch erstellt, Sie werden genauso wie Sie verwendet, ohne dass eine Interpolations Form vorhanden ist.

Das folgende Diagramm zeigt einen 64-Bit-Transparenz Block.

![Diagramm eines 64-Bit-Transparenz Blocks](images/colors4.png)

> [!Note]  
> Bei der Komprimierungs Methode von Direct3D werden die vier signifikantesten Bits verwendet.

 

Die folgenden Tabellen veranschaulichen, wie die Alpha Informationen für jedes 16-Bit-Wort im Arbeitsspeicher angeordnet werden.

Diese Tabelle enthält das Layout für Word 0.



| Bits          | Alpha      |
|---------------|------------|
| 3:0 (LSB \* )   | \[0 \] \[ 0\] |
| 7:4           | \[0 \] \[ 1\] |
| 11:8          | \[0 \] \[ 2\] |
| 15:12 (MSB \* ) | \[0 \] \[ 3\] |



 

\*am wenigsten signifikantes Bit, höchst wichtiges Bit (MSB)

Diese Tabelle enthält das Layout für Word 1.



| Bits        | Alpha      |
|-------------|------------|
| 3:0 (LSB)   | \[1 \] \[ 0\] |
| 7:4         | \[1 \] \[ 1\] |
| 11:8        | \[1 \] \[ 2\] |
| 15:12 (MSB) | \[1 \] \[ 3\] |



 

Diese Tabelle enthält das Layout für Word 2.



| Bits        | Alpha      |
|-------------|------------|
| 3:0 (LSB)   | \[2 \] \[ 0\] |
| 7:4         | \[2 \] \[ 1\] |
| 11:8        | \[2 \] \[ 2\] |
| 15:12 (MSB) | \[2 \] \[ 3\] |



 

Diese Tabelle enthält das Layout für Word 3.



| Bits        | Alpha      |
|-------------|------------|
| 3:0 (LSB)   | \[3 \] \[ 0\] |
| 7:4         | \[3 \] \[ 1\] |
| 11:8        | \[3 \] \[ 2\] |
| 15:12 (MSB) | \[3 \] \[ 3\] |



 

Der Unterschied zwischen DXT2 und DXT3 besteht darin, dass im DXT2-Format angenommen wird, dass die Farbdaten mit Alpha multipliziert wurden. Im Format "DXT3" wird davon ausgegangen, dass die Farbe nicht mit Alpha multipliziert ist. Diese beiden Formate sind erforderlich, da in den meisten Fällen bis zur Zeit, in der eine Textur verwendet wird, die Untersuchung der Daten nicht ausreicht, um zu ermitteln, ob die Farbwerte mit Alpha multipliziert wurden. Da diese Informationen zur Laufzeit benötigt werden, werden die beiden FOURCC-Codes verwendet, um diese Fälle zu unterscheiden. Die für diese beiden Formate verwendeten Daten-und Interpolations Methoden sind jedoch identisch.

Der Farbvergleich, der in DXT1 verwendet wird, um zu bestimmen, ob der Texel transparent ist, wird in diesem Format nicht verwendet. Es wird davon ausgegangen, dass die Farbdaten ohne den Farbvergleich immer so behandelt werden, als wären Sie im 4-Farben-Modus. Anders ausgedrückt: die if-Anweisung am Anfang des DXT1-Codes sollte wie folgt lauten:


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="three-bit-linear-alpha-interpolation"></a>Three-Bit Lineare Alpha interpolung

Die Codierung der Transparenz für die Formate DXT4 und DXT5 basiert auf einem Konzept, das der für Farbe verwendeten linearen Codierung ähnelt. 2 8-Bit-Alpha Werte und eine 4X4-Bitmap mit drei Bits pro Pixel werden in den ersten acht Bytes des Blocks gespeichert. Die repräsentativen Alpha Werte werden zum interpolieren von zwischen Alpha Werten verwendet. Weitere Informationen finden Sie in der Art und Weise, in der die beiden Alpha Werte gespeichert werden. Wenn Alpha \_ 0 größer als Alpha \_ 1 ist, werden sechs zwischen Alpha Werte von der Interpolations Zeit erstellt. Andernfalls werden vier zwischenalpha Werte zwischen den angegebenen Alpha extremen interpoliert. Die zwei zusätzlichen impliziten Alpha Werte sind 0 (vollständig transparent) und 255 (vollständig deckend).

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



Das Speicher Layout des Alpha-Blocks lautet wie folgt:



| Byte | Alpha                                                          |
|------|----------------------------------------------------------------|
| 0    | Alpha \_ 0                                                       |
| 1    | Alpha \_ 1                                                       |
| 2    | \[0 \] \[ 2 \] (2 MSSB), \[ 0 \] \[ 1 \] , \[ 0 \] \[ 0\]                    |
| 3    | \[1 \] \[ 1 \] (1 MSB), \[ 1 \] \[ 0 \] , \[ 0 \] \[ 3 \] , \[ 0 \] \[ 2 \] (1 LSB) |
| 4    | \[1 \] \[ 3 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 1 \] (2 lssb)                    |
| 5    | \[2 \] \[ 2 \] (2 MSSB), \[ 2 \] \[ 1 \] , \[ 2 \] \[ 0\]                    |
| 6    | \[3 \] \[ 1 \] (1 MSB), \[ 3 \] \[ 0 \] , \[ 2 \] \[ 3 \] , \[ 2 \] \[ 2 \] (1 LSB) |
| 7    | \[3 3 \] \[ \] , \[ 3, \] \[ \] \[ 3 \] \[ 1 \] (2 lssb)                    |



 

Der Unterschied zwischen DXT4 und DXT5 besteht darin, dass im DXT4-Format angenommen wird, dass die Farbdaten mit Alpha multipliziert wurden. Im Format "DXT5" wird davon ausgegangen, dass die Farbe nicht mit Alpha aufgefüllt wird. Diese beiden Formate sind erforderlich, da in den meisten Fällen bis zur Zeit, in der eine Textur verwendet wird, die Untersuchung der Daten nicht ausreicht, um zu ermitteln, ob die Farbwerte mit Alpha multipliziert wurden. Da diese Informationen zur Laufzeit benötigt werden, werden die beiden FOURCC-Codes verwendet, um diese Fälle zu unterscheiden. Die für diese beiden Formate verwendeten Daten-und Interpolations Methoden sind jedoch identisch.

Der Farbvergleich, der in DXT1 verwendet wird, um zu bestimmen, ob der Texel transparent ist, wird in diesen Formaten nicht verwendet. Es wird davon ausgegangen, dass die Farbdaten ohne den Farbvergleich immer so behandelt werden, als wären Sie im 4-Farben-Modus. Anders ausgedrückt: die if-Anweisung am Anfang des DXT1-Codes sollte wie folgt lauten:


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komprimierte Textur Ressourcen](compressed-texture-resources.md)
</dt> </dl>

 

 



