---
description: Informationen zu YUV-Video
ms.assetid: 089f42f2-1e5b-4d4b-98a4-9ef0ca2823c1
title: Informationen zu YUV-Video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499a8adfe1a43a22fe9bdd9ff4e576b7a14c398a9dafc0b945647d7225ad581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118744243"
---
# <a name="about-yuv-video"></a>Informationen zu YUV-Video

Digitale Videos werden häufig in einem *YUV-Format* codiert. In diesem Artikel werden die allgemeinen Konzepte von YUV-Videos sowie einige Terminologie erläutert, ohne sich mit der Mathematik der YUV-Videoverarbeitung vertraut zu machen.

Wenn Sie mit Computergrafiken gearbeitet haben, sind Sie wahrscheinlich mit RGB-Farben vertraut. Eine RGB-Farbe wird mit drei Werten codiert: rot, grün und blau. Diese Werte entsprechen direkt Teilen des sichtbaren Spektrums. Die drei RGB-Werte bilden ein mathematisches Koordinatensystem, das als *Farbraum* bezeichnet wird. Die rote Komponente definiert eine Achse dieses Koordinatensystems, blau die zweite und grün die dritte, wie in der folgenden Abbildung dargestellt. Jede gültige RGB-Farbe liegt an einer beliebigen Stelle innerhalb dieses Farbraums. Beispielsweise ist reine Magenta 100 % blau, 100 % rot und 0 % grün.

![Diagramm mit rgb-Farbraum](images/8ec60365-ed5c-41f7-9da9-be46aa82896a.gif)

Obwohl RGB eine gängige Methode zum Darstellen von Farben ist, sind andere Koordinatensysteme möglich. Der Begriff *YUV* bezieht sich auf eine Familie von Farbräumen, die alle Helligkeitsinformationen getrennt von Farbinformationen codieren. Wie RGB verwendet YUV drei Werte, um eine beliebige Farbe darzustellen. Diese Werte werden als "Y", "U" und "V" bezeichnet. (Tatsächlich ist diese Verwendung des Begriffs "YUV" technisch ungenau. Im Computervideo bezieht sich der Begriff YUV fast immer auf einen bestimmten Farbraum namens Y'CbCr, der später erläutert wird. YUV wird jedoch häufig als allgemeiner Begriff für jeden Farbraum verwendet, der nach den gleichen Prinzipien wie Y'CbCr funktioniert.)

Die Y-Komponente, auch *luma* genannt, stellt den Helligkeitswert der Farbe dar. Das Primsymbol (') wird verwendet, um luma von einem eng verwandten Wert zu unterscheiden, *Der Leuchtdichte*, der als Y bezeichnet wird. Die Leuchtdichte wird von *linearen* RGB-Werten abgeleitet, während luma von *nicht linearen RGB-Werten* (gammakorrigiert) abgeleitet wird. Die Leuchtdichte ist ein genaueres Maß für die tatsächliche Helligkeit, aber luma ist aus technischen Gründen praktischer zu verwenden. Das Primsymbol wird häufig ausgelassen, aber YUV-Farbräume verwenden immer Luma, nicht Leuchtdichte.

Luma wird von einer RGB-Farbe abgeleitet, indem ein gewichteter Durchschnitt der roten, grünen und blauen Komponenten genommen wird. Für Fernsehsendungen mit Standarddefinition wird die folgende Formel verwendet:

`Y' = 0.299R + 0.587G + 0.114B`

Diese Formel spiegelt die Tatsache wider, dass das menschliche Auge gegenüber bestimmten Lichtlichtungen sensibler ist als andere, was sich auf die wahrgenommene Helligkeit einer Farbe auswirkt. Blaues Licht erscheint am dunkelsten, Grün am hellsten, und Rot befindet sich zwischendurch. Diese Formel spiegelt auch die physischen Merkmale der Inserenten wider, die in frühen Fernsehgeräten verwendet werden. Eine neuere Formel wird unter Berücksichtigung moderner Fernsehtechnologie für High-Definition-Fernsehsendungen verwendet:

`Y' = 0.2125R + 0.7154G + 0.0721B`

Die Lumagleichung für Standarddefinitions-Fernsehgerät ist in einer Spezifikation mit dem Namen ITU-R BT.601 definiert. Für High-Definition-Fernsehsendungen ist die relevante Spezifikation ITU-R BT.709.

Die Komponenten "you" und "V", die auch als *Farbunterschiede* oder *Farbunterschiede* bezeichnet werden, werden abgeleitet, indem der Y-Wert von den roten und blauen Komponenten der ursprünglichen RGB-Farbe subtrahiert wird:

`U = B - Y'`

`V = R - Y'`

Zusammen enthalten diese Werte genügend Informationen, um den ursprünglichen RGB-Wert wiederherzustellen.

## <a name="benefits-of-yuv"></a>Vorteile von YUV

Analoge Fernsehgeräte verwenden YUV teilweise aus historischen Gründen. Analoge Farb-Tv-Signale wurden so konzipiert, dass sie abwärtskompatibel mit Schwarz-Weiß-Fernsehgeräten sind. Das farbliche Fernsehsignal enthält die Farbinformationen (Sie und V), die auf dem Luma-Signal überlagert sind. Schwarz-Weiß-Fernsehgeräte ignorieren das Farbchen und zeigen das kombinierte Signal als Graustufenbild an. (Das Signal ist so konzipiert, dass das Lumasignal nicht erheblich beeinträchtigt wird.) Farblichter können das Extraktionszeichen extrahieren und das Signal wieder in RGB konvertieren.

YUV bietet einen weiteren Vorteil, der heute relevanter ist. Das menschliche Auge reagiert weniger empfindlich auf Änderungen im Farbton als auf Helligkeitsänderungen. Daher kann ein Bild weniger Informationen enthalten als luma-Informationen, ohne die wahrgenommene Qualität des Bilds zu einbußen. Es ist z. B. üblich, die Werte der Mischungen mit der Hälfte der horizontalen Auflösung der Luma-Stichproben abzutasten. Anders ausgedrückt: Für alle zwei Luma-Stichproben in einer Zeile mit Pixeln gibt es eine U-Stichprobe und eine V-Stichprobe. Wenn 8 Bits zum Codieren jedes Werts verwendet werden, werden für alle zwei Pixel (zwei Y', ein U und ein V) insgesamt 4 Bytes benötigt, durchschnittlich 16 Bits pro Pixel oder 30 % weniger als die entsprechende 24-Bit-RGB-Codierung.

YUV ist von Natur aus nicht kompakter als RGB. Ein YUV-Pixel hat die gleiche Größe wie ein RGB-Pixel, es sei denn, der Farbverlauf ist verknöpft. Außerdem ist die Konvertierung von RGB in YUV nicht verlustig. Wenn kein Downsampling vorhanden ist, kann ein YUV-Pixel ohne Informationsverlust wieder in RGB konvertiert werden. Downsampling macht ein YUV-Bild kleiner und verliert auch einige der Farbinformationen. Bei korrekter Leistung ist der Verlust jedoch nicht wahrnehmbar signifikant.

## <a name="yuv-in-computer-video"></a>YUV im Computervideo

Die zuvor für YUV aufgeführten Formeln sind nicht die genauen Konvertierungen, die in digitalen Videos verwendet werden. Digitale Videos verwenden im Allgemeinen eine Form von YUV namens Y'CbCr. Im Wesentlichen skaliert Y'CbCr die YUV-Komponenten auf die folgenden Bereiche:



| Komponente | Range                              |
|-----------|------------------------------------|
| Y'        | 16–235                             |
| Cb/Cr     | 16–240, wobei 128 0 (null) darstellt |



 

Diese Bereiche setzen 8 Bit Genauigkeit für die Y'CbCr-Komponenten voraus. Hier ist die genaue Ableitung von Y'CbCr mithilfe der BT.601-Definition von luma:

1.  Beginnen Sie mit RGB-Werten im Bereich \[ 0...1 \] . Mit anderen Worten: Reines Schwarz ist 0 und reines Weiß ist 1. Wichtig: Hierbei handelt es sich um nicht lineare RGB-Werte (gammakorriert).
2.  Berechnen Sie das Luma. Für BT.601, Y' = 0,299R + 0,587G + 0,114B, wie zuvor beschrieben.
3.  Berechnen Sie die Differenzwerte für Zwischenstufen (B - Y' ) und (R - Y'). Diese Werte haben einen Bereich von +/- 0,886 für (B - Y') und +/- 0,701 für (R - Y').
4.  Skalieren Sie die Differenzwerte wie folgt:

    Pb = (0,5 / (1 - 0,114)) × (B - Y')

    Pr = (0,5 / (1 - 0,299)) × (R - Y')

    Diese Skalierungsfaktoren sind so konzipiert, dass beide Werte den gleichen numerischen Bereich (+/- 0,5) erhalten. Zusammen definieren sie einen YUV-Farbraum mit dem Namen Y'PbPr. Dieser Farbraum wird in analogen Komponentenvideos verwendet.

5.  Skalieren Sie die Y'PbPr-Werte, um die endgültigen Y'CbCr-Werte abzurufen:

    Y' = 16 + 219 × Y'

    Cb = 128 + 224 × Pb

    Cr = 128 + 224 × Pr

Diese letzten Skalierungsfaktoren erzeugen den Wertebereich, der in der vorherigen Tabelle aufgeführt ist. Natürlich können Sie RGB direkt in Y'CbCr konvertieren, ohne die Zwischenergebnisse zu speichern. Die Schritte sind hier separat aufgeführt, um zu zeigen, wie Y'CbCr von den ursprünglichen YUV-Gleichungen abgeleitet wird, die am Anfang dieses Artikels angegeben wurden.

Die folgende Tabelle zeigt RGB- und YCbCr-Werte für verschiedene Farben, wobei wiederum die BT.601-Definition von luma verwendet wird.



| Color   | R   | G   | B   | Y'  | Cb  | Cr  |
|---------|-----|-----|-----|-----|-----|-----|
| Schwarz   | 0   | 0   | 0   | 16  | 128 | 128 |
| Red     | 255 | 0   | 0   | 81  | 90  | 240 |
| Grün   | 0   | 255 | 0   | 145 | 54  | 34  |
| Blau    | 0   | 0   | 255 | 41  | 240 | 110 |
| Cyan    | 0   | 255 | 255 | 170 | 166 | 16  |
| Magenta | 255 | 0   | 255 | 106 | 202 | 222 |
| Gelb  | 255 | 255 | 0   | 210 | 16  | 146 |
| Weiß   | 255 | 255 | 255 | 235 | 128 | 128 |



 

Wie diese Tabelle zeigt, entsprechen Cb und Cr nicht intuitiven Ideen zur Farbe. Beispielsweise enthalten sowohl reines Weiß als auch reines Schwarz neutrale Ebenen von Cb und Cr (128). Die höchsten und niedrigsten Werte für Cb sind blau bzw. gelb. Für Cr sind die höchsten und niedrigsten Werte Rot und Zyan.

## <a name="for-more-information"></a>Weitere Informationen

-   [Empfohlene 8-Bit-YUV-Formate für video rendering](recommended-8-bit-yuv-formats-for-video-rendering.md)
-   Keith Jack. Video Demystified, Fünfte Edition. Newnes, 2007.
-   Charles A. Poynton. Eine technische Einführung in digitales Video. Wiley, 1996.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videomedientypen](video-media-types.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 



