---
description: Informationen zu YUV-Videos
ms.assetid: 089f42f2-1e5b-4d4b-98a4-9ef0ca2823c1
title: Informationen zu YUV-Videos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b57b4a453870af34c221683bdaf613b5038081d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526012"
---
# <a name="about-yuv-video"></a>Informationen zu YUV-Videos

Digitales Video wird häufig in einem *YUV* -Format codiert. In diesem Artikel werden die allgemeinen Konzepte von YUV-Videos zusammen mit einigen Begriffen erläutert, ohne dass Sie sich eingehend mit der Mathematik der YUV-Videoverarbeitung beschäftigen.

Wenn Sie mit Computergrafiken gearbeitet haben, sind Sie wahrscheinlich mit der RGB-Farbe vertraut. Eine RGB-Farbe wird mit drei Werten codiert: rot, grün und blau. Diese Werte entsprechen direkt den Teilen des sichtbaren Spektrums. Die drei RGB-Werte bilden ein mathematisches Koordinatensystem, das als *Farbraum* bezeichnet wird. Die rote Komponente definiert eine Achse dieses Koordinatensystems, Blau definiert das zweite und grün definiert das dritte, wie in der folgenden Abbildung dargestellt. Jede gültige RGB-Farbe fällt irgendwo in diesen Farbraum. Beispielsweise ist reiner Magenta 100% Blue, 100% Red und 0% grün.

![Diagramm mit RGB-Farbraum](images/8ec60365-ed5c-41f7-9da9-be46aa82896a.gif)

Obwohl RGB eine gängige Methode zur Darstellung von Farben ist, sind andere Koordinatensysteme möglich. Der Begriff " *YUV* " bezieht sich auf eine Familie von Farbräumen, die alle Informationen zur Helligkeit unabhängig von den Farbinformationen codieren. Wie bei RGB verwendet YUV drei Werte, um beliebige Farben darzustellen. Diese Werte werden als "Y", "U" und "V" bezeichnet. (tatsächlich ist diese Verwendung des Begriffs "YUV" technisch ungenau. In Computer Videos bezieht sich der Begriff YUV fast immer auf einen bestimmten Farbraum namens y' CbCr, der später erläutert wird. Allerdings wird YUV häufig als allgemeiner Begriff für jeden Farbraum verwendet, der gemeinsam mit den gleichen Prinzipien wie ' CbCr ' funktioniert.

Die Y-Komponente, auch als " *Luma*" bezeichnet, stellt den Helligkeitswert der Farbe dar. Das primsymbol (') wird zur Unterscheidung von Luma von einem eng verknüpften Wert, einer "Y"- *Beleuchtung* verwendet. "Leuchtkraft" wird von *linearen* RGB-Werten abgeleitet, während "Luma" von *nichtlinearen* RGB-Werten (Gamma korrigiert) abgeleitet wird. Die Leuchtkraft ist ein genaueres Maß an echter Helligkeit, aber die Verwendung von "Luma" ist aus technischen Gründen praktischer. Das primsymbol wird häufig ausgelassen, aber YUV-Farbbereiche verwenden immer "Luma", nicht "Leuchtkraft".

Der Wert von "Luma" wird aus einer RGB-Farbe abgeleitet, indem ein gewichteter Durchschnitt der roten, grünen und blauen Komponenten übernommen wird. Für das Standard-Definitions Fernsehen wird die folgende Formel verwendet:

`Y' = 0.299R + 0.587G + 0.114B`

Diese Formel spiegelt die Tatsache wider, dass das menschliche Auge für bestimmte Wellen Wellen besser sensibel ist als andere, was sich auf die wahrgenommene Helligkeit einer Farbe auswirkt. Blaues Licht wird als dimmest angezeigt, grün wird am hellsten angezeigt, und rot befindet sich irgendwo dazwischen. Diese Formel spiegelt auch die physischen Merkmale der in frühen Fernsehgeräten verwendeten Phosphors wider. Eine neuere Formel, die die moderne Fernsehtechnologie berücksichtigt, wird für das hochauflösende Fernsehen verwendet:

`Y' = 0.2125R + 0.7154G + 0.0721B`

Die Luma-Gleichung für das Standard-Definitions Fernsehen ist in einer Spezifikation mit dem Namen "ITU-R BT. 601" definiert. Für das hoch Definitions Fernsehen lautet die relevante Spezifikation "ITU-R BT. 709".

Die Komponenten "You" und "V", auch als " *Chroma* -Werte" oder " *Farbunterschied* " bezeichnet, werden durch Subtraktion des Y-Werts von den roten und blauen Komponenten der ursprünglichen RGB-Farbe abgeleitet:

`U = B - Y'`

`V = R - Y'`

Diese Werte enthalten gemeinsame Informationen, um den ursprünglichen RGB-Wert wiederherzustellen.

## <a name="benefits-of-yuv"></a>Vorteile von YUV

Das analoge Fernsehen verwendet YUV zum Teil aus historischen Gründen. Die Signale des analogen Farb Fernsehers wurden für die Abwärtskompatibilität mit schwarzen und weißen Fernsehgeräten entwickelt. Das Color-TV-Signal enthält die Chroma-Informationen (Sie und V), die auf das Luma-Signal über gestellt werden. Schwarze und weiße Fernsehgeräte ignorieren den Chroma und zeigen das kombinierte Signal als Graustufenbild an. (Das Signal ist so konzipiert, dass die Chroma das Luma-Signal nicht signifikant beeinträchtigt.) Farb-Fernsehgeräte können den Chroma extrahieren und das Signal zurück in RGB konvertieren.

YUV bietet einen anderen Vorteil, der heute relevanter ist. Das menschliche Auge ist weniger sensibel für Änderungen im Farbton als Änderungen an der Helligkeit. Folglich kann ein Image weniger Chroma-Informationen als Luma-Informationen aufweisen, ohne die wahrgenommene Qualität des Bilds zu beeinträchtigen. Beispielsweise ist es üblich, die Chroma-Werte mit der Hälfte der horizontalen Auflösung der Luma-Beispiele zu testen. Anders ausgedrückt: für jedes zwei Luma-Beispiele in einer Zeile mit Pixeln gibt es ein U-Beispiel und ein V-Beispiel. Vorausgesetzt, dass 8 Bits zum Codieren der einzelnen Werte verwendet werden, werden insgesamt 4 Bytes für alle zwei Pixel benötigt (zwei Y-Werte, ein U und ein V), für einen durchschnittlichen Wert von 16 Bits pro Pixel oder 30% kleiner als die entsprechende 24-Bit-RGB-Codierung.

YUV ist von Natur aus nicht kompakter als RGB. Ein YUV-Pixel hat dieselbe Größe wie ein RGB-Pixel, es sei denn, für den Chroma wird ein Downsampling durchgeführt. Außerdem ist die Konvertierung von RGB in YUV nicht verlustfrei. Wenn keine Downsampling vorhanden ist, kann ein YUV-Pixel ohne Informationsverlust wieder in RGB konvertiert werden. Durch das Downsampling wird ein YUV-Image kleiner, und es werden auch einige der Farbinformationen verloren. Wenn Sie jedoch ordnungsgemäß ausgeführt wird, ist der Verlust nicht perperell signifikant.

## <a name="yuv-in-computer-video"></a>Video zu YUV in Computer

Die zuvor für YUV aufgeführten Formeln sind nicht die exakten Konvertierungen, die in digitalen Videos verwendet werden. Digitales Video verwendet in der Regel die Form "YUV" mit dem Namen "y' CbCr". Im wesentlichen funktioniert y' CbCr, indem die YUV-Komponenten auf die folgenden Bereiche skaliert werden:



| Komponente | Range                              |
|-----------|------------------------------------|
| Teenie        | 16 – 235                             |
| CB/CR     | 16 – 240, wobei 128 0 (null) darstellt |



 

Diese Bereiche setzen 8 Bits an Genauigkeit für die ' CbCr '-Komponenten ein. Im folgenden finden Sie die genaue Ableitung von "y' CbCr" mithilfe der BT. 601-Definition von "Luma":

1.  Beginnen Sie mit RGB-Werten im Bereich von \[ 0... 1 \] . Das heißt, "Pure Black" ist 0, und pure weiß ist 1. Wichtig ist, dass es sich hierbei um nichtlineare (Gamma korrigierte) RGB-Werte handelt.
2.  Berechnen Sie den "Luma". Für BT. 601, Y ' = 0.299 r + 0.587 g + 0.114 b, wie zuvor beschrieben.
3.  Berechnen Sie die zwischen Menge der Chroma-Differenz Werte (B-Y ') und (R-y '). Diese Werte haben einen Bereich von +/-0,886 für (B-y ') und +/-0,701 für (R-y ').
4.  Skalieren Sie die Chroma-Differenz Werte wie folgt:

    PB = (0,5/(1-0,114)) × (B-Y ')

    PR = (0,5/(1-0,299)) × (R-Y ')

    Diese Skalierungsfaktoren sind so konzipiert, dass beide Werte denselben numerischen Bereich haben, +/-0,5. In der Zwischenzeit definieren Sie einen YUV-Farbraum mit dem Namen "y' pbpr". Dieser Farbraum wird in einem Video der analogen Komponente verwendet.

5.  Skalieren Sie die "y' pbpr-Werte, um die endgültigen ' ' CbCr-Werte zu erhalten:

    Y "= 16 + 219 × y"

    CB = 128 + 224 × PB

    CR = 128 + 224 × PR

Diese letzten Skalierungsfaktoren ergeben den Wertebereich, der in der vorherigen Tabelle aufgeführt ist. Natürlich können Sie RGB direkt in "y' CbCr konvertieren, ohne die Zwischenergebnisse zu speichern. Die Schritte werden hier separat aufgelistet, um zu veranschaulichen, wie "CbCr" von den ursprünglichen YUV-Gleichungen abgeleitet ist, die zu Beginn dieses Artikels angegeben wurden.

In der folgenden Tabelle werden RGB-und YCbCr-Werte für verschiedene Farben angezeigt, wobei die BT. 601-Definition von Luma verwendet wird.



| Color   | R   | G   | B   | Teenie  | Betrieben  | Cr  |
|---------|-----|-----|-----|-----|-----|-----|
| Schwarz   | 0   | 0   | 0   | 16  | 128 | 128 |
| Red     | 255 | 0   | 0   | 81  | 90  | 240 |
| Grün   | 0   | 255 | 0   | 145 | 54  | 34  |
| Blau    | 0   | 0   | 255 | 41  | 240 | 110 |
| Cyan    | 0   | 255 | 255 | 170 | 166 | 16  |
| Magenta | 255 | 0   | 255 | 106 | 202 | 222 |
| Gelb  | 255 | 255 | 0   | 210 | 16  | 146 |
| Weiß   | 255 | 255 | 255 | 235 | 128 | 128 |



 

Wie diese Tabelle zeigt, entsprechen CB und CR nicht den intuitiven Ideen zu Color. Beispielsweise enthalten "Pure weiß" und "Pure Black" die neutralen Ebenen "CB" und "CR" (128). Die höchsten und niedrigsten Werte für CB sind blau bzw. gelb. Bei CR sind der höchste und der niedrigste Wert "Red" und "Cyan".

## <a name="for-more-information"></a>Weitere Informationen

-   [Empfohlene 8-Bit-YUV-Formate für Video Rendering](recommended-8-bit-yuv-formats-for-video-rendering.md)
-   Keith Jack. Ein Video entmystifiziert, Fünfte Edition. Newnes, 2007.
-   Charles A. Poynton. Eine technische Einführung in digitales Video. Wiley, 1996.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Video Medientypen](video-media-types.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 



