---
description: Empfohlene 8-Bit-YUV-Formate für video rendering
ms.assetid: 675d4c60-4c58-4f15-9bae-ffb0c389c608
title: Empfohlene 8-Bit-YUV-Formate für video rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6e30f33c59bedf9a2e842d2d33328bd97d8078d21bda90ae84af9af00ec113
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722077"
---
# <a name="recommended-8-bit-yuv-formats-for-video-rendering"></a>Empfohlene 8-Bit-YUV-Formate für video rendering

Gary Soll und Stephen Estrop

Microsoft Corporation

April 2002, aktualisiert november 2008

In diesem Thema werden die 8-Bit-YUV-Farbformate beschrieben, die für das Rendern von Videos im Windows empfohlen werden. In diesem Artikel werden Techniken zum Konvertieren zwischen YUV- und RGB-Formaten sowie Verfahren zum Upsampling von YUV-Formaten beschrieben. Dieser Artikel richtet sich an alle Personen, die mit YUV-Videodecodierung oder -rendering in Windows.

## <a name="introduction"></a>Einführung

Zahlreiche YUV-Formate sind in der gesamten Videobranche definiert. In diesem Artikel werden die 8-Bit-YUV-Formate beschrieben, die für das Rendern von Videos in der Windows. Decoderanbietern und Anzeigeanbietern wird empfohlen, die in diesem Artikel beschriebenen Formate zu unterstützen. In diesem Artikel werden keine anderen Verwendungsmöglichkeiten der YUV-Farbe behandelt, wie z. B. noch Immer-Färbung.

Die in diesem Artikel beschriebenen Formate verwenden jeweils 8 Bits pro Pixelposition, um den Y-Kanal (auch als Lumakanal bezeichnet) zu codieren, und verwenden 8 Bits pro Stichprobe, um jedes U- oder V-Beispiel zu codieren. Die meisten YUV-Formate verwenden jedoch im Durchschnitt weniger als 24 Bits pro Pixel, da sie weniger Stichproben von Ihnen und V als Y enthalten. In diesem Artikel werden keine YUV-Formate mit 10-Bit- oder höheren Y-Kanälen behandelt.

> [!Note]  
> Für die Zwecke dieses Artikels entspricht der Begriff U Cb, und der Begriff V entspricht Cr.

 

In diesem Artikel werden die folgenden Themen behandelt:

-   [YUV Sampling](#yuv-sampling). Beschreibt die gängigsten YUV-Stichprobenverfahren.
-   [Oberflächendefinitionen](#surface-definitions). Beschreibt die empfohlenen YUV-Formate.
-   [Farbraum- und Samplingratenkonvertierungen](#color-space-and-chroma-sampling-rate-conversions). Enthält einige Richtlinien für die Konvertierung zwischen YUV- und RGB-Formaten sowie für die Konvertierung zwischen verschiedenen YUV-Formaten.
-   [Identifizieren von YUV-Formaten in Media Foundation](#identifying-yuv-formats-in-media-foundation). Erläutert das Beschreiben von YUV-Formattypen in Media Foundation.

## <a name="yuv-sampling"></a>YUV-Stichprobenentnahme

Kanalkanäle können eine niedrigere Samplingrate als der Lumakanal haben, ohne dass die wahrnehmliche Qualität drastisch verloren geht. Eine Notation namens "A:B:C" wird verwendet, um zu beschreiben, wie oft sie und V relativ zu Y stichprobeniert werden:

-   4:4:4 bedeutet kein Downsampling der Senderkanäle.
-   4:2:2 bedeutet 2:1 horizontales Downsampling ohne vertikales Downsampling. Jede Scanzeile enthält vier Y-Stichproben für alle zwei U- oder V-Beispiele.
-   4:2:0 bedeutet 2:1 horizontales Downsampling, mit 2:1 vertikalem Downsampling.
-   4:1:1 bedeutet 4:1 horizontales Downsampling ohne vertikales Downsampling. Jede Scanzeile enthält vier Y-Stichproben für jedes Ihrer und jedes V-Beispiel. 4:1:1 Sampling ist weniger üblich als andere Formate und wird in diesem Artikel nicht ausführlich erläutert.

Die folgenden Diagramme zeigen, wie für jede der Downsamplingraten Stichproben entnommen werden. Luma-Beispiele werden durch ein Kreuz dargestellt, und Musterbeispiele werden durch einen Kreis dargestellt.

![Abbildung 1: - Sampling](images/yuv-sampling-grids.png)

Die dominante Form der 4:2:2-Stichprobenentnahme ist in der ITU-R-Empfehlung BT.601 definiert. Es gibt zwei gängige Varianten der 4:2:0-Stichprobenentnahme. Eine davon wird im MPEG-2-Video und die andere in MPEG-1 und in ITU-T Empfehlungen H.261 und H.263 verwendet.

Im Vergleich zum MPEG-1-Schema ist es einfacher, zwischen dem MPEG-2-Schema und den Samplingrastern zu konvertieren, die für die Formate 4:2:2 und 4:4:4 definiert sind. Aus diesem Grund wird das MPEG-2-Schema in Windows bevorzugt und sollte als Standardinterpretation von 4:2:0-Formaten betrachtet werden.

## <a name="surface-definitions"></a>Oberflächendefinitionen

In diesem Abschnitt werden die 8-Bit-YUV-Formate beschrieben, die für das Videorendering empfohlen werden. Diese lassen sich in verschiedene Kategorien unterteilen:

-   [4:4:4 Formate, 32 Bits pro Pixel](#444-formats-32-bits-per-pixel)
-   [4:2:2 Formate, 16 Bits pro Pixel](#422-formats-16-bits-per-pixel)
-   [4:2:0 Formate, 16 Bits pro Pixel](#420-formats-16-bits-per-pixel)
-   [4:2:0 Formate, 12 Bits pro Pixel](#420-formats-12-bits-per-pixel)

Zunächst sollten Sie die folgenden Konzepte kennen, um zu verstehen, was folgt:

-   *Surface Origin*. Für die in diesem Artikel beschriebenen YUV-Formate ist der Ursprung (0,0) immer die obere linke Ecke der Oberfläche.
-   *Stride*. Der Strich einer Oberfläche, manchmal auch als Tonhöhe bezeichnet, ist die Breite der Oberfläche in Bytes. Bei einem Oberflächenhersprung in der oberen linken Ecke ist der Schritt immer positiv.
-   *Ausrichtung*. Die Ausrichtung einer Oberfläche liegt im Ermessen des Grafikanzeigetreibers. Die Oberfläche muss immer DWORD-ausgerichtet sein. Das heißt, dass einzelne Linien innerhalb der Oberfläche garantiert von einer 32-Bit-Grenze (DWORD) stammen. Die Ausrichtung kann jedoch je nach Hardwareanforderungen größer als 32 Bit sein.
-   Gepacktes Format im Vergleich zum planaren Format. YUV-Formate sind in *gepackte Formate* und *planare Formate* unterteilt. In einem gepackten Format werden die Komponenten Y, U und V in einem einzelnen Array gespeichert. Pixel sind in Gruppen von Makropixeln organisiert, deren Layout vom Format abhängt. In einem planaren Format werden die Komponenten Y, U und V als drei separate Ebenen gespeichert.

Jedem der in diesem Artikel beschriebenen YUV-Formate ist ein FOURCC-Code zugewiesen. Ein FOURCC-Code ist eine 32-Bit-Ganzzahl ohne Vorzeichen, die durch Verkettung von vier ASCII-Zeichen erstellt wird.

-   4:4:4 (32 bpp)
    -   [AYUV](#ayuv)
-   4:2:2 (16 bpp)
    -   [YUY2](#yuy2)
    -   [UYVIG](#uyvy)
-   4:2:0 (16 bpp)
    -   [IMC1](#imc1)
    -   [IMC3](#imc3)
-   4:2:0 (12 bpp)
    -   [IMC2](#imc2)
    -   [IMC4](#imc4)
    -   [YV12](#yv12)
    -   [NV12](#nv12)

## <a name="444-formats-32-bits-per-pixel"></a>4:4:4 Formate, 32 Bits pro Pixel

### <a name="ayuv"></a>AYUV

Es wird ein einzelnes 4:4:4-Format mit dem FOURCC-Code AYUV empfohlen. Dies ist ein gepacktes Format, bei dem jedes Pixel als vier aufeinander folgende Bytes codiert wird, die in der in der folgenden Abbildung dargestellten Sequenz angeordnet sind.

![Abbildung 2: ayuv-Speicherlayout](images/yuvformats01.gif)

Die als A markierten Bytes enthalten Werte für alpha.

## <a name="422-formats-16-bits-per-pixel"></a>4:2:2 Formate, 16 Bits pro Pixel

Es werden zwei 4:2:2-Formate mit den folgenden FOURCC-Codes empfohlen:

-   YUY2
-   UYAFFINITÄT

Beide sind gepackte Formate, bei denen jedes Makropixel aus zwei Pixeln besteht, die als vier aufeinander folgende Bytes codiert sind. Dies führt zu einem horizontalen Downsampling der Brille um den Faktor 2.

### <a name="yuy2"></a>YUY2

Im YUY2-Format können die Daten als Array  von char-Werten ohne Vorzeichen behandelt werden, wobei das erste Byte das erste Y-Beispiel enthält, das zweite Byte das erste U(Cb)-Beispiel, das dritte Byte das zweite Y-Beispiel und das vierte Byte das erste V -Beispiel (Cr), wie im folgenden Diagramm dargestellt.

![Abbildung 3: yuy2-Speicherlayout](images/yuvformats02.gif)

Wenn das Bild als Array von Little-Endian-WORD-Werten adressiert wird, enthält das erste **WORD** das erste Y-Beispiel in den am wenigsten signifikanten Bits (LSBs) und das erste U -Beispiel (Cb) in den wichtigsten Bits (MSBs).  Das zweite **WORD** enthält das zweite Y-Beispiel in den LSBs und das erste V-Beispiel (Cr) in den MSBs.

YUY2 ist das bevorzugte 4:2:2-Pixelformat für die Microsoft DirectX-Videobeschleunigung (DirectX VA). Es wird erwartet, dass es sich um eine kurzfristige Anforderung für DirectX VA-Accelerators handelt, die 4:2:2-Videos unterstützen.

### <a name="uyvy"></a>UYAFFINITÄT

Dieses Format ist mit dem YUY2-Format identisch, mit der Ausnahme, dass die Byte reihenfolge umgekehrt wird, d. h., die Bytes "yu" und "luma" werden gekippt (Abbildung 4). Wenn das Bild als Array von zwei Little-Endian **WORD-Werten** adressiert wird, enthält das erste **WORD** U in den LSBs und Y0 in den MSBs, und das zweite **WORD** enthält V in den LSBs und Y1 in den MSBs.

![Abbildung 4: uyy arbeitsspeicherlayout](images/yuvformats03.gif)

## <a name="420-formats-16-bits-per-pixel"></a>4:2:0 Formate, 16 Bits pro Pixel

Es werden zwei bpp-Formate (4:2:0, 16 Bit pro Pixel) mit den folgenden FOURCC-Codes empfohlen:

-   IMC1
-   IMC3

Beide YUV-Formate sind planare Formate. Die Farbkanäle werden sowohl in der horizontalen als auch in der vertikalen Dimension um den Faktor 2 subsampelt.

### <a name="imc1"></a>IMC1

Alle Y-Beispiele werden zuerst im Arbeitsspeicher als Array von char-Werten ohne **Vorzeichen** angezeigt. Darauf folgen alle V-Beispiele (Cr) und dann alle U-Beispiele (Cb). Die Ebenen V und U haben denselben Schritt wie die Y-Ebene, was zu nicht verwendeten Speicherbereichen führt, wie in Abbildung 5 dargestellt. Die Du- und V-Ebenen müssen an Speichergrenzen beginnen, die ein Vielfaches von 16 Zeilen sind. Abbildung 5 zeigt den Ursprung von Ihnen und V für einen 352 x 240-Videoframe. Die Startadresse der Sie- und V-Ebenen wird wie folgt berechnet:

``` syntax
BYTE* pV = pY + (((Height + 15) & ~15) * Stride);
BYTE* pU = pY + (((((Height * 3) / 2) + 15) & ~15) * Stride);
```

Dabei *ist pY* ein Bytezeiger auf den Anfang des Speicherarrays, wie im folgenden Diagramm dargestellt.

![Abbildung 5. imc1-Speicherlayout (Beispiel)](images/yuvformats04.gif)

### <a name="imc3"></a>IMC3

Dieses Format ist mit IMC1 identisch, mit der Ausnahme, dass die Sie- und die V-Ebene ausgetauscht werden, wie im folgenden Diagramm dargestellt.

![Abbildung 6: imc3-Speicherlayout](images/yuvformats05.gif)

## <a name="420-formats-12-bits-per-pixel"></a>4:2:0 Formate, 12 Bits pro Pixel

Es werden vier 4:2:0 12-bpp-Formate mit den folgenden FOURCC-Codes empfohlen:

-   IMC2
-   IMC4
-   YV12
-   NV12

In all diesen Formaten werden die Kanalkanäle in horizontalen und vertikalen Dimensionen um den Faktor 2 subsampelt.

### <a name="imc2"></a>IMC2

Dieses Format ist mit IMC1 identisch, mit Ausnahme des folgenden Unterschieds: Die Linien V (Cr) und U (Cb) sind an Halbschrittgrenzen verwebt. Anders ausgedrückt: Jede linie mit voller Stride im Bereich "Lf" beginnt mit einer Zeile mit V-Stichproben, gefolgt von einer Zeile mit U-Stichproben, die an der nächsten Halbschrittgrenze beginnt (Abbildung 7). Dieses Layout nutzt den Adressraum effizienter als IMC1. Sie schneidet den Adressraum der Brille um die Hälfte und somit den gesamten Adressraum um 25 Prozent ab. Unter den Formaten 4:2:0 ist IMC2 nach NV12 das zweit bevorzugte Format. Die folgende Abbildung veranschaulicht diesen Prozess.

![Abbildung 7: imc2-Speicherlayout](images/yuvformats07.gif)

### <a name="imc4"></a>IMC4

Dieses Format ist mit IMC2 identisch, mit der Ausnahme, dass die Linien U (Cb) und V (Cr) ausgetauscht werden, wie in der folgenden Abbildung dargestellt.

![Abbildung 8. imc4-Speicherlayout](images/yuvformats06.gif)

### <a name="yv12"></a>YV12

Alle Y-Beispiele werden zuerst im Arbeitsspeicher als Array von char-Werten ohne **Vorzeichen** angezeigt. Auf dieses Array folgen sofort alle V-Beispiele (Cr). Der Schritt der V-Ebene ist halb so lang wie die Y-Ebene. und die V-Ebene enthält halb so viele Linien wie die Y-Ebene. Auf die V-Ebene folgen sofort alle U-Beispiele (Cb) mit dem gleichen Schritt und der gleichen Anzahl von Linien wie die V-Ebene, wie in der folgenden Abbildung dargestellt.

![Abbildung 9: yv12-Speicherlayout](images/yuvformats08.gif)

### <a name="nv12"></a>NV12

Alle Y-Beispiele werden zuerst im Arbeitsspeicher als  Array von char-Werten ohne Vorzeichen mit einer gleichmäßigen Anzahl von Zeilen angezeigt. Auf die Y-Ebene folgt sofort ein  Array von char-Werten ohne Vorzeichen, das gepackte U-Beispiele (Cb) und V-Stichproben (Cr) enthält. Wenn das kombinierte U-V-Array als Array von  Little-Endian-WORD-Werten adressiert wird, enthalten die LSBs die U-Werte und die MSBs die V-Werte. NV12 ist das bevorzugte 4:2:0-Pixelformat für DirectX VA. Es wird erwartet, dass es sich um eine kurzfristige Anforderung für DirectX VA-Accelerators handelt, die 4:2:0-Videos unterstützen. Die folgende Abbildung zeigt die Y-Ebene und das Array, das gepackte Sie- und V-Beispiele enthält.

![Abbildung 10. nv12-Speicherlayout](images/yuvformats09.gif)

## <a name="color-space-and-chroma-sampling-rate-conversions"></a>Farbraum- und Samplingratenkonvertierungen

Dieser Abschnitt enthält Richtlinien für die Konvertierung zwischen YUV und RGB sowie für die Konvertierung zwischen verschiedenen YUV-Formaten. Wir betrachten in diesem Abschnitt zwei RGB-Codierungsschemas: *8-Bit-Computer RGB*, auch bekannt als sRGB oder "Full-Scale" RGB, und Studiovideo *RGB* oder "RGB mit Hauptraum und Toe-Room". Diese sind wie folgt definiert:

-   Computer RGB verwendet 8 Bits für jede Stichprobe aus Rot, Grün und Blau. Schwarz wird durch R = G = B = 0 und Weiß durch R = G = B = 255 dargestellt.
-   Studio Video RGB verwendet einige Bits N für jede Stichprobe von Rot, Grün und Blau, wobei N 8 oder mehr ist. Studio Video RGB verwendet einen anderen Skalierungsfaktor als Computer RGB und verfügt über einen Offset. Schwarz wird durch R = G = B = 16 \* 2^(N-8) dargestellt, und Weiß wird durch R = G = B = 235 \* 2^(N-8) dargestellt. Tatsächliche Werte können jedoch außerhalb dieses Bereichs liegen.

Studio-Video RGB ist die bevorzugte RGB-Definition für Videos in Windows, während Computer-RGB die bevorzugte RGB-Definition für Nicht-Videoanwendungen ist. In beiden Formen von RGB sind die Koordinaten für dieTicity wie in ITU-R BT.709 für die Definition der RGB-Farbprimitäten angegeben. Die (x,y)-Koordinaten von R, G und B sind (0,64, 0,33), (0,30, 0,60) bzw. (0,15, 0,06). Verweis weiß ist D65 mit Koordinaten (0,3127, 0,3290). Nominale Gammawerte sind 1/0,45 (ca. 2,2), und genaue Gammawerte sind in ITU-R BT.709 ausführlich definiert.

**Konvertierung zwischen RGB und 4:4:4 YUV**

Zunächst wird die Konvertierung zwischen RGB und 4:4:4 YUV beschrieben. Um 4:2:0 oder 4:2:2 YUV in RGB zu konvertieren, empfehlen wir, die YUV-Daten in 4:4:4 YUV und dann von 4:4:4 YUV in RGB zu konvertieren. Das AYUV-Format, das ein 4:4:4-Format ist, verwendet jeweils 8 Bits für die Beispiele Y, U und V. YUV kann auch mit mehr als 8 Bits pro Stichprobe für einige Anwendungen definiert werden.

Zwei dominante YUV-Konvertierungen von RGB wurden für digitale Videos definiert. Beide basieren auf der Spezifikation, die als ITU-R Recommendation BT.709 bezeichnet wird. Die erste Konvertierung ist das ältere YUV-Formular, das für die Verwendung mit 50 Hz in BT.709 definiert ist. Sie ist identisch mit der In itu-R-Empfehlung BT.601 angegebenen Beziehung, die auch unter dem älteren Namen CCIR 601 bekannt ist. Es sollte als bevorzugtes YUV-Format für standardbasierte TV-Auflösung (720 x 576) und Video mit niedrigerer Auflösung betrachtet werden. Sie wird durch die Werte der beiden Konstanten *Kr* und *Kb gekennzeichnet:*

``` syntax
Kr = 0.299
Kb = 0.114
```

Die zweite Konvertierung ist das neuere YUV-Formular, das für die Verwendung mit 60 Hz in BT.709 definiert ist und als bevorzugtes Format für Videoauflösungen über SDTV betrachtet werden sollte. Sie wird durch unterschiedliche Werte für diese beiden Konstanten gekennzeichnet:

``` syntax
Kr = 0.2126
Kb = 0.0722
```

Die Konvertierung von RGB in YUV wird wie folgt definiert:

``` syntax
L = Kr * R + Kb * B + (1 - Kr - Kb) * G
```

Die YUV-Werte werden dann wie folgt ermittelt:

``` syntax
Y =                   floor(2^(M-8) * (219*(L-Z)/S + 16) + 0.5)
U = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(B-L) / ((1-Kb)*S) + 128) + 0.5))
V = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(R-L) / ((1-Kr)*S) + 128) + 0.5))
```

where

-   M ist die Anzahl der Bits pro YUV-Stichprobe (M >= 8).
-   Z ist die Variable auf schwarzer Ebene. Für Computer RGB ist Z gleich 0. Für Studiovideo RGB entspricht Z 16 2^(N-8), wobei N die Anzahl der Bits pro \* RGB-Stichprobe ist (N >= 8).
-   S ist die Skalierungsvariable. Für Computer RGB ist S gleich 255. Für Studio-Video RGB entspricht S 219 \* 2^(N-8).

Die Funktion floor(x) gibt die größte ganze Zahl kleiner oder gleich x zurück. Die Funktion clip3(x, y, z) wird wie folgt definiert:

``` syntax
clip3(x, y, z) = ((z < x) ? x : ((z > y) ? y : z))
```

> [!Note]  
> clip3 sollte als Funktion und nicht als Präprozessormakro implementiert werden. andernfalls werden mehrere Auswertungen der Argumente durchgeführt.

 

Die Y-Stichprobe stellt die Helligkeit dar, und die Beispiele you und V stellen die Farbabweichungen in Richtung Blau bzw. Rot dar. Der nominale Bereich für Y beträgt 16 \* 2^(M-8) bis 235 \* 2^(M-8). Schwarz wird als 16 \* 2^(M-8) und weiß als 235 \* 2^(M-8) dargestellt. Der nominale Bereich für Sie und V liegt bei 16 \* 2^(M-8) bis 240 \* 2^(M-8), wobei der Wert 128 \* 2^(M-8) neutrales Farbmaß darstellt. Tatsächliche Werte können jedoch außerhalb dieser Bereiche liegen.

Für Eingabedaten in Form von Studio Video RGB ist der Clipvorgang erforderlich, um die Werte you und V im Bereich von 0 bis (2^M)-1 zu halten. Wenn es sich bei der Eingabe um computer RGB handelt, ist der Clipvorgang nicht erforderlich, da die Konvertierungsformel keine Werte außerhalb dieses Bereichs erzeugen kann.

Dies sind die genauen Formeln ohne Näherung. Alles, was in diesem Dokument folgt, wird von diesen Formeln abgeleitet. In diesem Abschnitt werden die folgenden Konvertierungen beschrieben:

-   [Konvertieren von RGB888 in YUV 4:4:4](#converting-rgb888-to-yuv-444)
-   [Konvertieren von 8-Bit-YUV in RGB888](#converting-8-bit-yuv-to-rgb888)
-   [Konvertieren von 4:2:0 YUV in 4:2:2 YUV](#converting-420-yuv-to-422-yuv)
-   [Konvertieren von 4:2:2 YUV in 4:4:4 YUV](#converting-422-yuv-to-444-yuv)
-   [Konvertieren von 4:2:0 YUV in 4:4:4 YUV](#converting-420-yuv-to-444-yuv)

## <a name="converting-rgb888-to-yuv-444"></a>Konvertieren von RGB888 in YUV 4:4:4

Im Fall der RGB-Eingabe des Computers und der 8-Bit-AUSGABE von BT.601 YUV sind wir der Meinung, dass die im vorherigen Abschnitt angegebenen Formeln durch Folgendes relativ geschätzt werden können:

``` syntax
Y = ( (  66 * R + 129 * G +  25 * B + 128) >> 8) +  16
U = ( ( -38 * R -  74 * G + 112 * B + 128) >> 8) + 128
V = ( ( 112 * R -  94 * G -  18 * B + 128) >> 8) + 128
```

Diese Formeln erzeugen 8-Bit-Ergebnisse mithilfe von Koeffizienten, die nicht mehr als 8 Bits (ohne Vorzeichen) erfordern. Zwischenergebnisse erfordern bis zu 16 Bit Genauigkeit.

## <a name="converting-8-bit-yuv-to-rgb888"></a>Konvertieren von 8-Bit-YUV in RGB888

Aus den ursprünglichen RGB-zu-YUV-Formeln können die folgenden Beziehungen für BT.601 abgeleitet werden.

``` syntax
Y = round( 0.256788 * R + 0.504129 * G + 0.097906 * B) +  16 
U = round(-0.148223 * R - 0.290993 * G + 0.439216 * B) + 128
V = round( 0.439216 * R - 0.367788 * G - 0.071427 * B) + 128
```

Aus diesem Grund gibt es:

``` syntax
C = Y - 16
D = U - 128
E = V - 128
```

Die Formeln zum Konvertieren von YUV in RGB können wie folgt abgeleitet werden:

``` syntax
R = clip( round( 1.164383 * C                   + 1.596027 * E  ) )
G = clip( round( 1.164383 * C - (0.391762 * D) - (0.812968 * E) ) )
B = clip( round( 1.164383 * C +  2.017232 * D                   ) )
```

, wobei `clip()` clipping auf einen Bereich von \[ 0,.255 \] anschließt. Wir sind der Meinung, dass diese Formeln durch Folgendes relativ geschätzt werden können:

``` syntax
R = clip(( 298 * C           + 409 * E + 128) >> 8)
G = clip(( 298 * C - 100 * D - 208 * E + 128) >> 8)
B = clip(( 298 * C + 516 * D           + 128) >> 8)
```

Diese Formeln verwenden einige Koeffizienten, die mehr als 8 Bit Genauigkeit erfordern, um jedes 8-Bit-Ergebnis zu erzeugen, und Zwischenergebnisse erfordern mehr als 16 Bit Genauigkeit.

Um 4:2:0 oder 4:2:2 YUV in RGB zu konvertieren, empfehlen wir, die YUV-Daten in 4:4:4 YUV und dann von 4:4:4 YUV in RGB zu konvertieren. Die folgenden Abschnitte enthalten einige Methoden zum Konvertieren der Formate 4:2:0 und 4:2:2 in 4:4:4.

## <a name="converting-420-yuv-to-422-yuv"></a>Konvertieren von 4:2:0 YUV in 4:2:2 YUV

Die Konvertierung von 4:2:0 YUV in 4:2:2 YUV erfordert eine vertikale Upconversion um den Faktor 2. In diesem Abschnitt wird eine Beispielmethode zum Ausführen der Upconversion beschrieben. Bei der -Methode wird davon ausgegangen, dass es sich bei den Videobildern um progressive Scans handelt.

> [!Note]  
> Der Prozess für die Konvertierung von 4:2:0 bis 4:2:2 mit Zeilensprung stellt atypische Probleme dar und ist schwer zu implementieren. In diesem Artikel wird das Problem der Konvertierung des Interlacingscans von 4:2:0 in 4:2:2 nicht behandelt.

 

Lassen Sie jede vertikale Linie der Eingabemuster ein Array von `Cin[]` 0 bis N bis 1 sein. Die entsprechende vertikale Linie im Ausgabebild ist ein Array `Cout[]` zwischen 0 und 2N bis 1. Führen Sie den folgenden Prozess aus, um jede vertikale Linie zu konvertieren:

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

dabei steht clip() für clipping für einen Bereich von \[ 0,.255 \] .

> [!Note]  
> Die Gleichungen für die Behandlung der Kanten können mathematisch vereinfacht werden. Sie werden in dieser Form angezeigt, um den klammernden Effekt an den Rändern des Bilds zu veranschaulichen.

 

Tatsächlich berechnet diese Methode jeden fehlenden Wert, indem die Kurve über die vier angrenzenden Pixel interpoliert wird, gewichtet auf die Werte der beiden nächsten Pixel (Abbildung 11). Die spezifische Interpolationsmethode, die in diesem Beispiel verwendet wird, generiert fehlende Stichproben an halbzahligen Positionen mithilfe einer bekannten Methode namens Catmull-Rom Interpolation, die auch als kubische Konvolutionsinterpolation bezeichnet wird.

![Abbildung 11. Diagramm: Upsampling von 4:2:0 bis 4:2:2](images/yuvformats14.gif)

Bei der Signalverarbeitung sollte die vertikale Upconversion idealerweise eine Phasenverschiebungskompensierung enthalten, um den vertikalen Halbpixeloffset (relativ zum Ausgabe-4:2:2-Stichprobenraster) zwischen den Positionen der 4:2:0-Stichprobenlinien und der Position jeder anderen 4:2:2-Stichprobenlinie zu berücksichtigen. Die Einführung dieses Offsets würde jedoch die Verarbeitungsmenge erhöhen, die zum Generieren der Stichproben erforderlich ist, und es unmöglich machen, die ursprünglichen 4:2:0-Stichproben aus dem upsampled 4:2:2-Bild zu rekonstruieren. Es wäre auch unmöglich, Videos direkt in 4:2:2-Oberflächen zu decodieren und diese Oberflächen dann als Referenzbilder zum Decodieren nachfolgender Bilder im Stream zu verwenden. Daher berücksichtigt die hier bereitgestellte Methode die genaue vertikale Ausrichtung der Stichproben nicht. Dies ist bei relativ hohen Bildauflösungen wahrscheinlich nicht visuell schädlich.

Wenn Sie mit einem 4:2:0-Video beginnen, das das in H.261- oder H.263- oder MPEG-1-Video definierte Samplingraster verwendet, wird die Phase der Ausgabestichproben für 4:2:2-Stichproben auch um einen horizontalen Halbpixeloffset relativ zum Abstand auf dem Luma-Samplingraster verschoben (ein Viertelpixeloffset relativ zum Abstand des 4:2:2-Rasters für die Stichprobenentnahme). Die MPEG-2-Form von 4:2:0-Videos wird jedoch wahrscheinlich häufiger auf PCs verwendet und unter diesem Problem nicht beeinträchtigt. Darüber hinaus ist die Unterscheidung bei relativ hohen Bildauflösungen wahrscheinlich nicht visuell schädlich. Der Versuch, dieses Problem zu beheben, würde die gleiche Art von Problemen verursachen, die für den vertikalen Phasenoffset erläutert werden.

## <a name="converting-422-yuv-to-444-yuv"></a>Konvertieren von 4:2:2 YUV in 4:4:4 YUV

Die Konvertierung von 4:2:2 YUV in 4:4:4 YUV erfordert eine horizontale Upconversion um den Faktor 2. Die zuvor für vertikale Upconversion beschriebene Methode kann auch auf horizontale Upconversion angewendet werden. Für MPEG-2- und ITU-R BT.601-Videos erzeugt diese Methode Stichproben mit der richtigen Phasenausrichtung.

## <a name="converting-420-yuv-to-444-yuv"></a>Konvertieren von 4:2:0 YUV in 4:4:4 YUV

Zum Konvertieren von 4:2:0 YUV in 4:4:4 YUV können Sie einfach die beiden zuvor beschriebenen Methoden befolgen. Konvertieren Sie das 4:2:0-Image in 4:2:2 und dann das 4:2:2-Image in 4:4:4. Sie können auch die Reihenfolge der beiden Upconversionsprozesse ändern, da die Reihenfolge des Vorgangs nicht wirklich von der visuellen Qualität des Ergebnisses abweicht.

## <a name="other-yuv-formats"></a>Andere YUV-Formate

Einige andere, weniger gängige YUV-Formate umfassen Folgendes:

-   AI44 ist ein palettisiertes YUV-Format mit 8 Bits pro Stichprobe. Jedes Beispiel enthält einen Index in den vier signifikantesten Bits (MSBs) und einen Alphawert in den 4 LSBs (Least Significant Bits). Der Index bezieht sich auf ein Array von YUV-Paletteneinträgen, die im Medientyp für das Format definiert werden müssen. Dieses Format wird hauptsächlich für Bildunterdrückung verwendet.
-   NV11 ist ein Planarformat von 4:1:1 mit 12 Bits pro Pixel. Die Y-Beispiele werden zuerst im Arbeitsspeicher angezeigt. Auf die Y-Ebene folgt ein Array von gepackten U-Stichproben (Cb) und V -Stichproben (Cr). Wenn das kombinierte U-V-Array als Array von **Little-Endian-WORD-Werten** adressiert wird, sind die U-Stichproben in den LSBs der einzelnen **WORD-Dateien** enthalten, und die V-Beispiele sind in den MSBs enthalten. (Dieses Speicherlayout ähnelt NV12, obwohl sich die Stichprobenentnahme unterscheidet.)
-   Y41P ist ein gepacktes 4:1:1-Format, bei dem Sie und V jedes vierte Pixel horizontal entnommen werden. Jedes Makropixel enthält 8 Pixel in drei Bytes mit dem folgenden Bytelayout: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`
-   Y41T ist identisch mit Y41P, mit der Ausnahme, dass das am wenigsten signifikante Bit jeder Y-Stichprobe den Schlüssel für die Füllung angibt (0 = transparent, 1 = nicht transparent).
-   Y42T ist identisch mit UYVY, mit dem Unterschied, dass das am wenigsten signifikante Bit jeder Y-Stichprobe den Farbschlüssel angibt (0 = transparent, 1 = nicht transparent).
-   YV CSV entspricht YUYV, mit der Ausnahme, dass die Beispiele "You" und "V" ausgetauscht werden.

## <a name="identifying-yuv-formats-in-media-foundation"></a>Identifizieren von YUV-Formaten in Media Foundation

Jedem der in diesem Artikel beschriebenen YUV-Formate ist FOURCC-Code zugewiesen. Ein FOURCC-Code ist eine 32-Bit-Ganzzahl ohne Vorzeichen, die durch Verketten von vier ASCII-Zeichen erstellt wird.

Es gibt verschiedene C/C++-Makros, die das Deklarieren von FOURCC-Werten im Quellcode vereinfachen. Beispielsweise wird das **MAKEFOURCC-Makro** in "Mmsystem.h" und das **FCC-Makro** in "Aviriff.h" deklariert. Verwenden Sie sie wie folgt:

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```

Sie können einen FOURCC-Code auch direkt als Zeichenfolgenliteral deklarieren, indem Sie einfach die Reihenfolge der Zeichen umkehren. Beispiel:

``` syntax
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'
```

Das Umkehren der Reihenfolge ist erforderlich, da das Windows Betriebssystem eine Little-Endian-Architektur verwendet. "Y" = 0x59, "U" = 0x55 und "2" = 0x32, sodass "2REAY" 0x32595559 ist.

In Media Foundation werden Formate durch eine Haupttyp-GUID und eine Untertyp-GUID identifiziert. Der Haupttyp für Computervideoformate ist immer MFMediaType \_ Video . Der Untertyp kann wie folgt erstellt werden, indem der FOURCC-Code einer GUID zugeordnet wird:

``` syntax
XXXXXXXX-0000-0010-8000-00AA00389B71 
```

dabei `XXXXXXXX` ist der FOURCC-Code. Daher lautet der Untertyp GUID für YUY2:

``` syntax
32595559-0000-0010-8000-00AA00389B71 
```

Konstanten für die gängigsten GUIDs im YUV-Format werden in der Headerdatei mfapi.h definiert. Eine Liste dieser Konstanten finden Sie unter [Video-Untertyp-GUIDs.](video-subtype-guids.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu YUV-Video](about-yuv-video.md)
</dt> <dt>

[Videomedientypen](video-media-types.md)
</dt> </dl>

 

 



