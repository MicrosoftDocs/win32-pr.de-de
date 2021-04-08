---
description: Empfohlene 8-Bit-YUV-Formate für Video Rendering
ms.assetid: 675d4c60-4c58-4f15-9bae-ffb0c389c608
title: Empfohlene 8-Bit-YUV-Formate für Video Rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4505eb17f833040e0148ac98912f16af860b55b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753889"
---
# <a name="recommended-8-bit-yuv-formats-for-video-rendering"></a>Empfohlene 8-Bit-YUV-Formate für Video Rendering

Gary Sullivan und Stephen estrop

Microsoft Corporation

2002. April, aktualisiert: 2008. November

In diesem Thema werden die 8-Bit-YUV-Farb Formate beschrieben, die für Video Rendering im Windows-Betriebssystem empfohlen werden. In diesem Artikel werden die Verfahren für die Typumwandlung zwischen YUV-und RGB-Formaten und Techniken zum Upsampling von YUV-Formaten beschrieben. Dieser Artikel richtet sich an jeden Benutzer, der mit dem Entschlüsseln oder Rendern von YUV-Videos in Windows arbeitet.

## <a name="introduction"></a>Einführung

Viele YUV-Formate werden in der gesamten Videobranche definiert. In diesem Artikel werden die 8-Bit-YUV-Formate beschrieben, die für Video Rendering in Windows empfohlen werden. Decoder-und Anzeige Hersteller werden empfohlen, die in diesem Artikel beschriebenen Formate zu unterstützen. In diesem Artikel werden keine anderen Verwendungsmöglichkeiten von YUV-Farben behandelt, wie z. b. immer noch Fotos.

Die in diesem Artikel beschriebenen Formate verwenden alle 8 Bits pro Pixel-Speicherort, um den Y-Kanal (auch als "Luma Channel" bezeichnet) zu codieren, und verwenden 8 Bits pro Stichprobe, um jedes U-oder V Chroma-Beispiel zu codieren. In den meisten YUV-Formaten werden im Durchschnitt weniger als 24 Bits pro Pixel verwendet, da Sie weniger Stichproben von Ihnen und V als von Y enthalten. In diesem Artikel werden keine YUV-Formate mit 10-Bit-oder höheren Y-Kanälen behandelt.

> [!Note]  
> Für den Zweck dieses Artikels entspricht der Begriff "U" dem Wert von "CB", und der Begriff "V" entspricht CR.

 

In diesem Artikel werden die folgenden Themen behandelt:

-   [YUV-Stichprobenentnahme](#yuv-sampling). Beschreibt die gängigsten YUV-Stichproben Techniken.
-   [Oberflächen Definitionen](#surface-definitions). Beschreibt die empfohlenen YUV-Formate.
-   [Farb Raum-und Chroma-Samplingrate](#color-space-and-chroma-sampling-rate-conversions). Hier finden Sie einige Richtlinien für die Typumwandlung zwischen YUV-und RGB-Formaten sowie für die zwischen unterschiedlichen YUV
-   [Erkennen von YUV-Formaten in Media Foundation](#identifying-yuv-formats-in-media-foundation). Erläutert das Beschreiben von YUV-Format Typen in Media Foundation.

## <a name="yuv-sampling"></a>YUV-Stichprobe

Chroma-Kanäle können eine niedrigere Samplingrate als der Luma-Kanal aufweisen, ohne dass ein dramatischer Verlust der perzeptive Qualität auftritt. Eine Notation mit der Bezeichnung "a:b: C" wird verwendet, um zu beschreiben, wie oft Sie und V in Relation zu Y als Stichprobe verwendet werden:

-   4:4:4 bedeutet, dass die Chroma-Kanäle nicht herabgestuft werden.
-   4:2:2 bedeutet 2:1 horizontale Downsampling ohne vertikale Downsampling. Jede Scanzeile enthält vier Y-Beispiele für alle zwei U-oder V-Beispiele.
-   4:2:0 bedeutet 2:1 horizontale Downsampling mit 2:1 vertikaler Downsampling.
-   4:1:1 bedeutet 4:1 horizontale Downsampling ohne vertikale Downsampling. Jede Scanzeile enthält vier Y-Beispiele für jedes Sie und jede V-Stichprobe. 4:1:1 die Stichprobenentnahme ist weniger häufig als andere Formate und wird in diesem Artikel nicht ausführlich erläutert.

Die folgenden Diagramme zeigen, wie Chroma für jede der Verkleinerung-Raten Stichproben erstellt wird. Luma-Beispiele werden durch ein Kreuz dargestellt, und Chroma-Beispiele werden durch einen Kreis dargestellt.

![Abbildung 1. Chroma-Sampling](images/yuv-sampling-grids.png)

Die vorherrschende Form der 4:2:2-Stichprobenentnahme wird in der ITU-R-Empfehlung BT BT. 601. Es gibt zwei häufige Varianten der 4:2:0-Stichprobenentnahme. Eines dieser werden in MPEG-2-Video und das andere in MPEG-1 und in den ITU-T-Empfehlungen H. 261 und h. 263 verwendet.

Im Vergleich zum MPEG-1-Schema ist es einfacher, zwischen dem MPEG-2-Schema und den für 4:2:2-und 4:4:4-Formaten definierten Samplings zu konvertieren. Aus diesem Grund wird das MPEG-2-Schema in Windows bevorzugt und sollte als Standardinterpretation von 4:2:0-Formaten angesehen werden.

## <a name="surface-definitions"></a>Oberflächen Definitionen

In diesem Abschnitt werden die 8-Bit-YUV-Formate beschrieben, die für Video Rendering empfohlen werden. Diese sind in verschiedene Kategorien unterteilt:

-   [4:4:4 Formate, 32 Bits pro Pixel](#444-formats-32-bits-per-pixel)
-   [4:2:2 Formate, 16 Bits pro Pixel](#422-formats-16-bits-per-pixel)
-   [4:2:0 Formate, 16 Bits pro Pixel](#420-formats-16-bits-per-pixel)
-   [4:2:0 Formate, 12 Bits pro Pixel](#420-formats-12-bits-per-pixel)

Zuerst sollten Sie die folgenden Konzepte kennen, um zu verstehen, was folgt:

-   *Oberflächen Ursprung*. Bei den in diesem Artikel beschriebenen YUV-Formaten steht der Ursprung (0,0) immer in der oberen linken Ecke der Oberfläche.
-   *Stride*. Der Stride einer Oberfläche (manchmal auch als "Tonhöhe" bezeichnet) ist die Breite der Oberfläche (in Bytes). Wenn ein Oberflächen Ursprung in der oberen linken Ecke liegt, ist der Stride immer positiv.
-   *Ausrichtung*. Die Ausrichtung einer Oberfläche liegt im Ermessen des Grafik Anzeige Treibers. Die Oberfläche muss immer DWORD-bündig sein. Das heißt, dass einzelne Zeilen innerhalb der Oberfläche von einer 32-Bit-Grenze (DWORD) ausgehen. Die Ausrichtung kann jedoch je nach den Anforderungen der Hardware größer als 32 Bits sein.
-   Gepacktes Format im Vergleich zum planaren Format. YUV-Formate sind in *gepackte* Formate und *planare* Formate unterteilt. In einem gepackten Format werden die Y-, U-und V-Komponenten in einem einzelnen Array gespeichert. Pixel sind in Gruppen von macropixels organisiert, deren Layout vom Format abhängt. In einem planaren Format werden die Y-, U-und V-Komponenten als drei separate Ebenen gespeichert.

Jedes in diesem Artikel beschriebene YUV-Format verfügt über einen zugewiesenen FourCC-Code. Bei einem FourCC-Code handelt es sich um eine 32-Bit-Ganzzahl ohne Vorzeichen, die durch Verkettung von vier ASCII-Zeichen erstellt wird.

-   4:4:4 (32 bpp)
    -   [Ayuv](#ayuv)
-   4:2:2 (16 bpp)
    -   [Im YUY2](#yuy2)
    -   [UYVY](#uyvy)
-   4:2:0 (16 bpp)
    -   [IMC1](#imc1)
    -   [IMC3](#imc3)
-   4:2:0 (12 BPP)
    -   [IMC2](#imc2)
    -   [IMC4](#imc4)
    -   [YV12](#yv12)
    -   [NV12](#nv12)

## <a name="444-formats-32-bits-per-pixel"></a>4:4:4 Formate, 32 Bits pro Pixel

### <a name="ayuv"></a>Ayuv

Ein einzelnes 4:4:4-Format wird mit dem FourCC-Code ayuv empfohlen. Dabei handelt es sich um ein gepacktes Format, bei dem jedes Pixel in der in der folgenden Abbildung gezeigten Reihenfolge als vier aufeinanderfolgende Bytes codiert wird.

![Abbildung 2. Arbeitsspeicher Layout von ayuv](images/yuvformats01.gif)

Die markierten Bytes enthalten Werte für Alpha.

## <a name="422-formats-16-bits-per-pixel"></a>4:2:2 Formate, 16 Bits pro Pixel

Es werden zwei 4:2:2-Formate mit den folgenden FOURCC-Codes empfohlen:

-   Im YUY2
-   UYVY

Beide sind gepackte Formate, wobei jedes Makro Pixel zwei Pixel als vier aufeinanderfolgende Bytes codiert ist. Dies führt zu einem horizontalen Verkleinerung des Chroma mit einem Faktor von zwei.

### <a name="yuy2"></a>Im YUY2

Im im YUY2-Format können die Daten als Array nicht signierter **char** -Werte behandelt werden, wobei das erste Byte das erste y-Beispiel enthält, das zweite Byte das erste U (CB)-Beispiel, das dritte Byte das zweite y-Beispiel und das vierte Byte das erste V-Beispiel (CR), wie im folgenden Diagramm dargestellt.

![Abbildung 3. im YUY2-Arbeitsspeicher Layout](images/yuvformats02.gif)

Wenn das Bild als Array von Little-enumdian- **Wort** Werten adressiert wird, enthält das erste **Wort** das erste Y-Beispiel in der unwichtigsten Bits (LSB) und das erste U (CB)-Beispiel in den signifikantesten Bits (MSB). Das zweite **Wort** enthält das zweite Y-Beispiel im lssb und das erste V (CR)-Beispiel in MSSB.

Im YUY2 ist das bevorzugte 4:2:2-Pixel-Format für die Microsoft DirectX-Video Beschleunigung (DirectX VA). Es wird erwartet, dass es sich um eine langfristige Anforderung für DirectX VA Accelerators handelt, die 4:2:2-Video unterstützen.

### <a name="uyvy"></a>UYVY

Dieses Format ist mit dem im YUY2-Format identisch, mit dem Unterschied, dass die Byte Reihenfolge umgekehrt ist – d. h., die Chroma-und Luma-Bytes werden gekippt (Abbildung 4). Wenn das Bild als ein Array von zwei Little-enumdian- **Wort** Werten adressiert wird, enthält das erste **Wort** U in den lssb und y0 in den MSSB, und das zweite **Wort** enthält V in den lssb und Y1 in den MSSB.

![Abbildung 4. UYVY-Speicher Layout](images/yuvformats03.gif)

## <a name="420-formats-16-bits-per-pixel"></a>4:2:0 Formate, 16 Bits pro Pixel

Es werden zwei 4:2:0 16-Bits pro Pixel-Format (BPP) mit den folgenden FOURCC-Codes empfohlen:

-   IMC1
-   IMC3

Beide YUV-Formate sind Planare Formate. Die Chroma-Kanäle werden von einem Faktor von zwei in den horizontalen und vertikalen Dimensionen Subsampling.

### <a name="imc1"></a>IMC1

Alle Y-Beispiele werden als erstes im Arbeitsspeicher als Array nicht signierter **char** -Werte angezeigt. Anschließend werden alle V-Beispiele (CR) und dann alle U (CB)-Beispiele angezeigt. Die Flächen "V" und "U" haben den gleichen Schritt wie die Y-Ebene, was zu nicht verwendeten Speicherbereichen führt, wie in Abbildung 5 dargestellt. Die Ebenen "You" und "V" müssen an Speicher Begrenzungen beginnen, die ein Vielfaches von 16 Zeilen sind. Abbildung 5 zeigt den Ursprung von Ihnen und V für einen Video Frame mit 352 x 240. Die Startadresse der Ebenen "You" und "V" wird wie folgt berechnet:

``` syntax
BYTE* pV = pY + (((Height + 15) & ~15) * Stride);
BYTE* pU = pY + (((((Height * 3) / 2) + 15) & ~15) * Stride);
```

Dabei ist *pY* ein Byte Zeiger auf den Anfang des Speicherarrays, wie im folgenden Diagramm dargestellt.

![Abbildung 5. imc1-Arbeitsspeicher Layout (Beispiel)](images/yuvformats04.gif)

### <a name="imc3"></a>IMC3

Dieses Format ist mit IMC1 identisch, mit dem Unterschied, dass Sie und die V-Ebenen ausgetauscht werden, wie im folgenden Diagramm dargestellt.

![Abbildung 6. imc3-Arbeitsspeicher Layout](images/yuvformats05.gif)

## <a name="420-formats-12-bits-per-pixel"></a>4:2:0 Formate, 12 Bits pro Pixel

Vier 4:2:0 12-bpp-Formate werden mit den folgenden FOURCC-Codes empfohlen:

-   IMC2
-   IMC4
-   YV12
-   NV12

In allen diesen Formaten werden die Chroma-Kanäle in den horizontalen und vertikalen Dimensionen durch einen Faktor von zwei Subsampling.

### <a name="imc2"></a>IMC2

Dieses Format ist identisch mit IMC1, mit Ausnahme des folgenden Unterschieds: die Zeilen V (CR) und U (CB) sind über Schneidevorgänge mit halber Stride-Grenze. Mit anderen Worten, jede vollständige Zeile im Bereich Chroma beginnt mit einer Reihe von V-Beispielen, gefolgt von einer Reihe von U-Beispielen, die an der nächsten Hälfte der nächsten Grenze beginnen (Abbildung 7). Mit diesem Layout wird der Adressraum effizienter genutzt als IMC1. Er schneidet den Chroma-Adressraum in der Hälfte ab und somit den gesamten Adressraum um 25 Prozent. Bei 4:2:0-Formaten ist IMC2 das zweitbeliebteste Format nach NV12. Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.

![Abbildung 7: imc2-Arbeitsspeicher Layout](images/yuvformats07.gif)

### <a name="imc4"></a>IMC4

Dieses Format ist mit IMC2 identisch, mit der Ausnahme, dass die Zeilen U (CB) und V (CR) ausgetauscht werden, wie in der folgenden Abbildung dargestellt.

![Abbildung 8. IMC4-Arbeitsspeicher Layout](images/yuvformats06.gif)

### <a name="yv12"></a>YV12

Alle Y-Beispiele werden als erstes im Arbeitsspeicher als Array nicht signierter **char** -Werte angezeigt. Auf dieses Array folgt sofort alle V-Beispiele (CR). Der Schritt der V-Ebene liegt bei der Hälfte des Schrittes der Y-Ebene. und die Ebene "V" enthält die Hälfte der Zeilen in der Y-Ebene. Auf die v-Ebene folgt sofort alle U (CB)-Beispiele mit dem gleichen Schritt und der Anzahl von Zeilen wie die Ebene "v", wie in der folgenden Abbildung dargestellt.

![Abbildung 9. YV12-Arbeitsspeicher Layout](images/yuvformats08.gif)

### <a name="nv12"></a>NV12

Alle Y-Beispiele werden als erstes im Arbeitsspeicher als Array von **char** -Werten ohne Vorzeichen mit einer geraden Anzahl von Zeilen angezeigt. Auf die Y-Ebene folgt unmittelbar ein Array nicht signierter **char** -Werte, das gepackte U (CB)-und V (CR)-Beispiele enthält. Wenn das kombinierte U-V-Array als Array von Little-enumdian- **Wort** Werten adressiert wird, enthalten die lssb die U-Werte, und die MSSB enthalten die V-Werte. NV12 ist das bevorzugte 4:2:0-Pixel-Format für DirectX VA. Es wird erwartet, dass es sich um eine langfristige Anforderung für DirectX VA Accelerators handelt, die 4:2:0-Video unterstützen. In der folgenden Abbildung sind die Y-Ebene und das-Array dargestellt, das gepackte Sie und V-Beispiele enthält.

![Abbildung 10. nv12-Arbeitsspeicher Layout](images/yuvformats09.gif)

## <a name="color-space-and-chroma-sampling-rate-conversions"></a>Farb Raum-und Chroma-Sampling-Raten Konvertierungen

Dieser Abschnitt enthält Richtlinien für die Typumwandlung zwischen YUV und RGB sowie für die Umstellung zwischen einigen unterschiedlichen YUV-Formaten. In diesem Abschnitt werden zwei RGB-Codierungs Schemas in Erwägung gezogen: *8-Bit-Computer RGB*, auch als sRGB oder "vollständig skalierbar" (RGB) und *Studio-Video RGB* oder "RGB mit headraum und Zehen Raum" bezeichnet. Diese werden wie folgt definiert:

-   Computer RGB verwendet 8 Bits für jedes rot, grün und blau. Schwarz wird durch r = g = b = 0 und weiß durch r = g = b = 255 dargestellt.
-   In der Studio-Grafik RGB wird eine beliebige Anzahl von Bits N für jede Stichprobe von rot, grün und Blau verwendet, wobei N 8 oder mehr ist. Studio-Video RGB verwendet einen anderen Skalierungsfaktor als Computer RGB und einen Offset. Schwarz wird durch r = g = b = 16 \* 2 ^ (n-8) und weiß durch r = g = b = 235 \* 2 ^ (n-8) dargestellt. Tatsächliche Werte können jedoch außerhalb dieses Bereichs liegen.

Studio-Video RGB ist die bevorzugte RGB-Definition für Videos in Windows, während Computer RGB die bevorzugte RGB-Definition für nicht-Video-Anwendungen ist. In beiden Formen von RGB werden die Chromaticity-Koordinaten in "ITU-R BT. 709" für die Definition der RGB-Farb Primärwerte angegeben. Die (x, y)-Koordinaten von R, G und B sind (0,64, 0,33), (0,30, 0,60) und (0,15, 0,06) bzw. Der Verweis weiß ist D65 mit Koordinaten (0,3127, 0,3290). Das nominale Gamma ist 1/0.45 (ca. 2,2), wobei präziser Gamma ausführlich in "ITU-R BT. 709" definiert ist.

**Konvertierung zwischen RGB und 4:4:4 YUV**

Zuerst wird die Konvertierung zwischen RGB und 4:4:4 YUV beschrieben. Zum Konvertieren von 4:2:0 oder 4:2:2 YUV in RGB empfiehlt es sich, die YUV-Daten in 4:4:4 YUV zu konvertieren und dann von 4:4:4 YUV in RGB zu konvertieren. Das Format "ayuv", bei dem es sich um ein 4:4:4-Format handelt, verwendet jeweils 8 Bits für die Y-, U-und V-Beispiele. YUV kann auch mit mehr als 8 Bits pro Stichprobe für einige Anwendungen definiert werden.

Zwei vorherrschende YUV-Konvertierungen von RGB wurden für digitales Video definiert. Beide basieren auf der Spezifikation, die als "ITU-R-Empfehlung BT. 709" bezeichnet wird. Die erste Konvertierung ist das ältere YUV-Formular, das für die Verwendung von 50-Hz in BT. 709 definiert ist. Sie ist identisch mit der in der ITU-R-Empfehlung "BT. 601" angegebenen Beziehung, die auch mit dem älteren Namen "CCIR 601" bekannt ist. Er sollte als bevorzugtes YUV-Format für die Standard-Definition-TV-Auflösung (720 x 576) und ein Video mit niedrigerer Auflösung angesehen werden. Dies ist durch die Werte der beiden Konstanten *KR* und *KB* gekennzeichnet:

``` syntax
Kr = 0.299
Kb = 0.114
```

Die zweite Konvertierung ist das neuere YUV-Formular, das für die Verwendung von 60-Hz in BT. 709 definiert ist, und sollte als bevorzugtes Format für Videoauflösungen oberhalb von SDTV angesehen werden. Sie ist durch unterschiedliche Werte für diese beiden Konstanten gekennzeichnet:

``` syntax
Kr = 0.2126
Kb = 0.0722
```

Die Konvertierung von RGB in YUV wird wie folgt definiert:

``` syntax
L = Kr * R + Kb * B + (1 - Kr - Kb) * G
```

Die YUV-Werte werden dann wie folgt abgerufen:

``` syntax
Y =                   floor(2^(M-8) * (219*(L-Z)/S + 16) + 0.5)
U = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(B-L) / ((1-Kb)*S) + 128) + 0.5))
V = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(R-L) / ((1-Kr)*S) + 128) + 0.5))
```

where

-   M ist die Anzahl von Bits pro YUV-Beispiel (m >= 8).
-   Z ist die Variable auf schwarzer Ebene. Für Computer RGB ist Z auf 0 (null). Für Studio-Video RGB entspricht Z dem Wert 16 \* 2 ^ (n-8), wobei N für die Anzahl der Bits pro RGB-Stichprobe (n >= 8) steht.
-   S ist die Skalierungs Variable. Für Computer RGB ist "S" 255. Für Studio-Video RGB ist S auf 219 \* 2 ^ (N-8).

Die Funktionsfläche (x) gibt die größte ganze Zahl zurück, die kleiner oder gleich x ist. Die Clip3-Funktion (x, y, z) ist wie folgt definiert:

``` syntax
clip3(x, y, z) = ((z < x) ? x : ((z > y) ? y : z))
```

> [!Note]  
> Clip3 sollte nicht als Präprozessormakro, sondern als Funktion implementiert werden. Andernfalls werden mehrere Auswertungen der Argumente durchzuführen.

 

Das Y-Beispiel stellt die Helligkeit dar, und die Beispiele für Sie und V stellen die Farbabweichungen in Richtung blau bzw. rot dar. Der nominale Bereich für Y ist 16 \* 2 ^ (m-8) bis 235 \* 2 ^ (m-8). Schwarz wird als 16 \* 2 ^ (m-8) und weiß als 235 \* 2 ^ (m-8) dargestellt. Der nominale Bereich für Sie und V beträgt 16 \* 2 ^ (m-8) bis 240 \* 2 ^ (m-8) mit dem Wert 128 \* 2 ^ (m-8), der neutrales Chroma darstellt. Tatsächliche Werte können jedoch außerhalb dieser Bereiche liegen.

Für Eingabedaten in Form von Studio-Video RGB ist der Clip-Vorgang erforderlich, um die Werte für "You" und "V" im Bereich von 0 bis (2 ^ M)-1 beizubehalten. Wenn es sich bei der Eingabe um Computer RGB handelt, ist der Clip Vorgang nicht erforderlich, da die Konvertierungs Formel keine Werte außerhalb dieses Bereichs verursachen kann.

Dabei handelt es sich um die genauen Formeln ohne Näherungs. Alles, was in diesem Dokument folgt, wird von diesen Formeln abgeleitet. In diesem Abschnitt werden die folgenden Konvertierungen beschrieben:

-   [Wandeln von RGB888 in YUV 4:4:4](#converting-rgb888-to-yuv-444)
-   [Umstellen von 8-Bit-YUV in RGB888](#converting-8-bit-yuv-to-rgb888)
-   [4:2:0 YUV wird in 4:2:2 YUV umgerechnet](#converting-420-yuv-to-422-yuv)
-   [4:2:2 YUV wird in 4:4:4 YUV umgerechnet](#converting-422-yuv-to-444-yuv)
-   [4:2:0 YUV wird in 4:4:4 YUV umgerechnet](#converting-420-yuv-to-444-yuv)

## <a name="converting-rgb888-to-yuv-444"></a>Wandeln von RGB888 in YUV 4:4:4

Im Fall von "Computer RGB Input" und der 8-Bit-Ausgabe "BT. 601 YUV" sind wir der Meinung, dass die im vorherigen Abschnitt angegebenen Formeln in gewisser Weise den folgenden Werten zugewiesen werden können:

``` syntax
Y = ( (  66 * R + 129 * G +  25 * B + 128) >> 8) +  16
U = ( ( -38 * R -  74 * G + 112 * B + 128) >> 8) + 128
V = ( ( 112 * R -  94 * G -  18 * B + 128) >> 8) + 128
```

Diese Formeln liefern 8-Bit-Ergebnisse mithilfe von Koeffizienten, die nicht mehr als 8 Bits der (unsignierten) Genauigkeit erfordern. Zwischenergebnisse erfordern bis zu 16 Bits an Genauigkeit.

## <a name="converting-8-bit-yuv-to-rgb888"></a>Umstellen von 8-Bit-YUV in RGB888

Aus den ursprünglichen RGB-zu-YUV-Formeln kann eine der folgenden Beziehungen für BT. 601 abgeleitet werden.

``` syntax
Y = round( 0.256788 * R + 0.504129 * G + 0.097906 * B) +  16 
U = round(-0.148223 * R - 0.290993 * G + 0.439216 * B) + 128
V = round( 0.439216 * R - 0.367788 * G - 0.071427 * B) + 128
```

Daher gilt Folgendes:

``` syntax
C = Y - 16
D = U - 128
E = V - 128
```

die Formeln zum Konvertieren von YUV in RGB können wie folgt abgeleitet werden:

``` syntax
R = clip( round( 1.164383 * C                   + 1.596027 * E  ) )
G = clip( round( 1.164383 * C - (0.391762 * D) - (0.812968 * E) ) )
B = clip( round( 1.164383 * C +  2.017232 * D                   ) )
```

wobei das `clip()` Clipping auf einen Bereich von \[ 0.. 255 bezeichnet \] . Wir sind der Meinung, dass diese Formeln in gewisser Weise den folgenden folgen:

``` syntax
R = clip(( 298 * C           + 409 * E + 128) >> 8)
G = clip(( 298 * C - 100 * D - 208 * E + 128) >> 8)
B = clip(( 298 * C + 516 * D           + 128) >> 8)
```

Diese Formeln verwenden einige Koeffizienten, bei denen mehr als 8 Bits Genauigkeit erforderlich sind, um jedes 8-Bit-Ergebnis zu erzielen, und Zwischenergebnisse erfordern mehr als 16 Bits an Genauigkeit.

Zum Konvertieren von 4:2:0 oder 4:2:2 YUV in RGB empfiehlt es sich, die YUV-Daten in 4:4:4 YUV zu konvertieren und dann von 4:4:4 YUV in RGB zu konvertieren. Die folgenden Abschnitte enthalten einige Methoden zum Umrechnen von 4:2:0-und 4:2:2-Formaten in 4:4:4.

## <a name="converting-420-yuv-to-422-yuv"></a>4:2:0 YUV wird in 4:2:2 YUV umgerechnet

Die Konvertierung von 4:2:0 YUV in 4:2:2 YUV erfordert eine vertikale upkonvertierung mit einem Faktor von zwei. In diesem Abschnitt wird eine Beispiel Methode zum Ausführen der Upconversion beschrieben. Bei der-Methode wird davon ausgegangen, dass die Videobilder Progressive Scan werden.

> [!Note]  
> Der Konvertierungs Vorgang "4:2:0 bis 4:2:2 Interlacing Scan" stellt atypische Probleme dar und ist schwierig zu implementieren. In diesem Artikel wird das Problem der Umstellung der Zeilen Sprung Überprüfung von 4:2:0 in 4:2:2 nicht behandelt.

 

Jede vertikale Zeile von Eingabe-Chroma-Beispielen ist ein Array `Cin[]` , das zwischen 0 und N-1 liegt. Die entsprechende vertikale Linie des Ausgabe Bilds ist ein Array `Cout[]` , das zwischen 0 und 2n-1 liegt. Um jede vertikale Linie zu konvertieren, führen Sie den folgenden Prozess aus:

``` syntax
Cout[0]     = Cin[0];
Cout[1]     = clip((9 * (Cin[0] + Cin[1]) - (Cin[0] + Cin[2]) + 8) >> 4);
Cout[2]     = Cin[1];
Cout[3]     = clip((9 * (Cin[1] + Cin[2]) - (Cin[0] + Cin[3]) + 8) >> 4);
Cout[4]     = Cin[2]
Cout[5]     = clip((9 * (Cin[2] + Cin[3]) - (Cin[1] + Cin[4]) + 8) >> 4);
...
Cout[2*i]   = Cin[i]
Cout[2*i+1] = clip((9 * (Cin[i] + Cin[i+1]) - (Cin[i-1] + Cin[i+2]) + 8) >> 4);
...
Cout[2*N-3] = clip((9 * (Cin[N-2] + Cin[N-1]) - (Cin[N-3] + Cin[N-1]) + 8) >> 4);
Cout[2*N-2] = Cin[N-1];
Cout[2*N-1] = clip((9 * (Cin[N-1] + Cin[N-1]) - (Cin[N-2] + Cin[N-1]) + 8) >> 4);
```

Where Clip () bezeichnet Clipping auf einen Bereich von \[ 0.. 255 \] .

> [!Note]  
> Die Gleichungen zum Behandeln der Kanten können mathematisch vereinfacht werden. Sie werden in dieser Form angezeigt, um den Spann Effekt an den Rändern des Bilds zu veranschaulichen.

 

Tatsächlich berechnet diese Methode jeden fehlenden Wert durch Interpolation der Kurve über die vier angrenzenden Pixel, die auf die Werte der beiden nächsten Pixel gewichtet werden (Abbildung 11). Die in diesem Beispiel verwendete spezielle Interpolationsmethode generiert fehlende Stichproben an der Hälfte der ganzzahligen Positionen mithilfe einer bekannten Methode namens Catmull-Rom Interpolationsmethode, die auch als kubische intervolution-Interpolationsmethode bezeichnet wird.

![Abbildung 11. Diagramm mit 4:2:0 bis 4:2:2 Upsampling](images/yuvformats14.gif)

In Signal Verarbeitungs Begriffen sollte die vertikale upkonvertierung idealerweise eine Phasen Verschiebungs Kompensation enthalten, um den vertikalen halb Pixel Offset (relativ zum samplingraster der Ausgabe 4:2:2) zwischen den Speicherorten der 4:2:0-Beispiel Zeilen und dem Speicherort jeder anderen 4:2:2-Beispiel Zeile zu berücksichtigen. Durch die Einführung dieses Offsets wird jedoch der Verarbeitungsaufwand für das Generieren der Beispiele erhöht, und es ist nicht möglich, die ursprünglichen 4:2:0-Beispiele aus dem Upsampling-Image 4:2:2 zu rekonstruieren. Außerdem wäre es nicht möglich, Videos direkt in 4:2:2-Oberflächen zu decodieren und diese Oberflächen dann als Referenzbilder für das Decodieren der nachfolgenden Bilder im Stream zu verwenden. Daher berücksichtigt die hier angegebene Methode nicht die präzise vertikale Ausrichtung der Beispiele. Dies ist wahrscheinlich nicht visuell schädlich bei einer relativ großen Bildauflösung.

Wenn Sie mit einem 4:2:0-Video beginnen, das das im h. 261-, h. 263-oder MPEG-1-Video definierte Stichproben Raster verwendet, wird auch die Phase der Ausgabe 4:2:2 Chroma-Beispiele in Relation zum Abstand in der Luma-Samplings-Stichproben 4:2:2 Entnahme um einen horizontalen Halbpixel-Offset verschoben. Die MPEG-2-Form von 4:2:0-Video wird jedoch wahrscheinlich häufiger auf PCs verwendet und wird von diesem Problem nicht beeinträchtigt. Außerdem ist die Unterscheidung wahrscheinlich nicht visuell schädlich, wenn es um eine relativ hohe Bildauflösung geht. Der Versuch, dieses Problem zu beheben, würde die gleiche Art von Problemen erzeugen, die für den vertikalen Phasen Offset erläutert werden.

## <a name="converting-422-yuv-to-444-yuv"></a>4:2:2 YUV wird in 4:4:4 YUV umgerechnet

Die Konvertierung von 4:2:2 YUV in 4:4:4 YUV erfordert eine horizontale upkonvertierung mit einem Faktor von zwei. Die zuvor beschriebene Methode für die vertikale upkonvertierung kann auch auf die horizontale upkonvertierung angewendet werden. Für MPEG-2-und ITU-R BT. 601-Video erstellt diese Methode Beispiele mit der korrekten Phasen Ausrichtung.

## <a name="converting-420-yuv-to-444-yuv"></a>4:2:0 YUV wird in 4:4:4 YUV umgerechnet

Wenn Sie 4:2:0 YUV in 4:4:4 YUV konvertieren möchten, können Sie einfach den oben beschriebenen Methoden folgen. Konvertieren Sie das 4:2:0-Abbild in 4:2:2, und konvertieren Sie dann das 4:2:2-Image in 4:4:4. Sie können auch die Reihenfolge der beiden upkonvertierungsprozesse ändern, da die Reihenfolge der Vorgänge für die visuelle Qualität des Ergebnisses nicht wirklich von Bedeutung ist.

## <a name="other-yuv-formats"></a>Andere YUV-Formate

Einige andere, weniger gängige YUV-Formate umfassen Folgendes:

-   AI44 ist ein im plettisierten YUV-Format mit 8 Bits pro Stichprobe. Jedes Beispiel enthält einen Index in den 4 signifikantesten Bits (MSSB) und einen Alpha-Wert in den 4 geringsten Bits (lssb). Der Index verweist auf ein Array von YUV-paletteneinträgen, die im Medientyp für das Format definiert werden müssen. Dieses Format wird hauptsächlich für Bild Bilder verwendet.
-   NV11 ist ein 4:1:1-planare-Format mit 12 Bits pro Pixel. Die Y-Beispiele werden zuerst im Arbeitsspeicher angezeigt. Auf die Y-Ebene folgt ein Array von gepackten U (CB)-und V-Beispielen (CR). Wenn das kombinierte u-V-Array als Array von Little-enumdian- **Wort** Werten adressiert wird, sind die U-Beispiele in den lssb der einzelnen **Word** enthalten, und die V-Beispiele sind in den MSSB enthalten. (Dieses Speicher Layout ähnelt NV12, obwohl die Chroma-Stichprobe anders ist.)
-   Im y41p ist ein 4:1:1-gepacktes Format, bei dem Sie und V jedes vierte Pixel horizontal abgepackt haben. Jedes Makro Pixel enthält 8 Pixel in drei Bytes mit dem folgenden bytelayout: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`
-   Y41T ist mit im y41p identisch, mit dem Unterschied, dass das unwichtigste Bit jedes Y-Beispiels den Chroma-Schlüssel angibt (0 = transparent, 1 = nicht transparent).
-   Y42T ist mit UYVY identisch, mit dem Unterschied, dass das unwichtigste Bit jedes Y-Beispiels den Chroma-Schlüssel angibt (0 = transparent, 1 = nicht transparent).
-   Yvyu entspricht yuyv, mit dem Unterschied, dass die Beispiele für Sie und V ausgetauscht werden.

## <a name="identifying-yuv-formats-in-media-foundation"></a>Erkennen von YUV-Formaten in Media Foundation

Jedes in diesem Artikel beschriebene YUV-Format verfügt über einen zugewiesenen FourCC-Code. Bei einem FourCC-Code handelt es sich um eine 32-Bit-Ganzzahl ohne Vorzeichen, die durch Verkettung von vier ASCII-Zeichen erstellt wird.

Es gibt verschiedene C/C++-Makros, die das Deklarieren von FourCC-Werten im Quellcode vereinfachen. Beispielsweise wird das **makefourcc** -Makro in MMSYSTEM. h deklariert, und das **FCC** -Makro wird in aviriff. h deklariert. Verwenden Sie diese wie folgt:

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```

Sie können einen FourCC-Code auch direkt als Zeichenfolgenliterale deklarieren, indem Sie einfach die Reihenfolge der Zeichen umkehren. Beispiel:

``` syntax
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'
```

Das Umkehren der Reihenfolge ist erforderlich, da das Windows-Betriebssystem eine Little-Endian-Architektur verwendet. ' Y ' = 0x59, ' U ' = 0x55 und ' 2 ' = 0x32, daher ist ' 2yuy ' 0x32595559.

In Media Foundation werden Formate durch eine GUID des Haupt Typs und eine Untertyp-GUID identifiziert. Der Haupttyp für Computer Videoformate ist immer MF MediaType \_ Video. Der Untertyp kann erstellt werden, indem Sie den FourCC-Code einer GUID wie folgt zuordnet:

``` syntax
XXXXXXXX-0000-0010-8000-00AA00389B71 
```

dabei `XXXXXXXX` ist der FourCC-Code. Folglich lautet die Untertyp-GUID für im YUY2 wie folgt:

``` syntax
32595559-0000-0010-8000-00AA00389B71 
```

Konstanten für die gängigsten GUIDs des YUV-Formats werden in der Header Datei "mfapi. h" definiert. Eine Liste dieser Konstanten finden Sie [unter Video Untertyp-GUIDs](video-subtype-guids.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu YUV-Videos](about-yuv-video.md)
</dt> <dt>

[Video Medientypen](video-media-types.md)
</dt> </dl>

 

 



