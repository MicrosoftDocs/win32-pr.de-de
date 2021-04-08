---
description: In den folgenden Abschnitten wird beschrieben, wie Direct3D Konvertierungen zwischen Datentypen behandelt.
ms.assetid: 454d3fd0-fc0f-46a9-925e-13f8e3c39f02
title: Regeln für die Datenkonvertierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61abdc58811af9155c67d7b32bcd47e9d4b71ea5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748265"
---
# <a name="data-conversion-rules"></a>Regeln für die Datenkonvertierung

In den folgenden Abschnitten wird beschrieben, wie Direct3D Konvertierungen zwischen Datentypen behandelt.

-   [Datentyp Terminologie](#data-type-terminology)
-   [Gleit Komma Konvertierung](#floating-point-conversion)
    -   [Konverting von einer höheren Bereichs Darstellung zu einer unteren Bereichs Darstellung](#conververting-from-a-higher-range-representation-to-a-lower-range-representation)
    -   [Wandeln von einer unteren Bereichs Darstellung in eine Darstellung mit höherem Bereich](#converting-from-a-lower-range-representation-to-a-higher-range-representation)
-   [Ganzzahlige Konvertierung](#integer-conversion)
-   [Konvertierung fester ganzzahliger Zeichen](#fixed-point-integer-conversion)
-   [Zugehörige Themen](#related-topics)

## <a name="data-type-terminology"></a>Datentyp Terminologie

Die folgenden Begriffe werden anschließend verwendet, um verschiedene Formatkonvertierungen zu bezeichnen.



| Begriff  | Definition                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Snorm | Signierte normalisierte Ganzzahl. Dies bedeutet, dass der Höchstwert für die Komplement Nummer eines n-Bit 2 1.0 f bedeutet (z. b. der 5-Bit-Wert 01111 ist 1.0 f), und der Minimalwert bedeutet-1.0 f (z. b. der 5-Bit-Wert 10000 wird-1.0 f zugeordnet). Außerdem wird die zweite Mindestanzahl zu-1.0 f zugeordnet (z. b. wird der 5-Bit-Wert 10001 zu-1.0 f zugeordnet). Folglich gibt es zwei ganzzahlige Darstellungen für-1.0 f. Es gibt eine einzelne Darstellung für 0,0 f und eine einzelne Darstellung für 1.0 f. Dies führt zu einer Reihe von ganzzahligen Darstellungen für Gleit Komma Werte mit gleichmäßiger Abstand im Bereich (-1.0 f... 0,0 f) und auch ein komplementärer Satz von Darstellungen für Zahlen im Bereich (0,0 f... 1.0 f) |
| UNORM | Nicht signierte normalisierte Ganzzahl, d. h. für eine n-Bit-Zahl bedeutet, dass alle 0-Werte 0,0 f sind, und all 1 bedeutet 1.0 f. Eine Sequenz der gleichmäßig im Abstand befindlichen Gleit Komma Werte zwischen 0,0 f und 1.0 f wird dargestellt. ein 2-Bit-unorm stellt beispielsweise 0,0 f, 1/3, 2/3 und 1.0 f dar.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| St  | Ganzzahl mit Vorzeichen. 2 Komplement Integer. Beispielsweise stellt ein 3-Bit-Sint die ganzzahligen Werte-4,-3,-2,-1, 0, 1, 2, 3 dar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| UINT  | Ganzzahl ohne Vorzeichen. Beispielsweise stellt ein 3-Bit-uint die ganzzahligen Werte 0, 1, 2, 3, 4, 5, 6, 7 dar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| GLEITKOMMAZAHL | Ein Gleit Komma Wert in einer der durch Direct3D definierten Darstellungen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| SRGB  | Ähnlich wie bei unorm bedeutet das, dass für eine n-Bit-Zahl 0,0 f bedeutet, und all 1 bedeutet 1.0 f. Im Unterschied zu unorm, mit sRGB, stellen die Sequenz nicht signierter ganzzahliger Codierungen zwischen allen Werten von 0 bis 1 einen nichtlinearen Fortschritt in der Gleit Komma Interpretation der Zahlen dar, zwischen 0,0 f und 1.0 f. Grob gesagt, wenn dieser nichtlineare Fortschritt (sRGB) als Sequenz von Farben angezeigt wird, würde er als eine lineare Bewegung der Helligkeitsstufen zu einem "durchschnittlichen" Beobachter in der Anzeige "Average" (durchschnittliche Anzeige) angezeigt werden. Ausführliche Informationen finden Sie in der sRGB-Farbstandard, IEC 61996-2-1, unter IEC (Internationale Elektrotechnische Kommission).                |



 

## <a name="floating-point-conversion"></a>Gleit Komma Konvertierung

Jedes Mal, wenn eine Gleit Komma Konvertierung zwischen verschiedenen Darstellungen erfolgt, einschließlich zu oder aus nicht Gleit Komma Darstellungen, gelten die folgenden Regeln.

### <a name="conververting-from-a-higher-range-representation-to-a-lower-range-representation"></a>Konverting von einer höheren Bereichs Darstellung zu einer unteren Bereichs Darstellung

-   Round-to-Zero wird während der Konvertierung in ein anderes Float-Format verwendet. Wenn es sich bei dem Ziel um ein ganzzahliges oder festes Punkt Format handelt, wird "roundTo-Next-even" verwendet, es sei denn, die Konvertierung wird explizit als ein anderes Rundungs Verhalten dokumentiert, z. b. "roundTo-Next" für "float" in "snorm", "float" in "unorm Bei anderen Ausnahmen handelt es sich um die ftoi-und ftou-shaderanweisungen, in denen "roundTo NULL" verwendet wird. Zum Schluss haben die von Textur Sampler und Raster verwendeten Konvertierungen vom Datentyp "float-to-Fixed" eine angegebene Toleranz, die in Einheiten-Last-Place von einem unendlich präzisen ideal gemessen wird.
-   Für Quell Werte, die größer sind als der dynamische Bereich des Ziel Formats des unteren Bereichs (z. b. ein großer 32-Bit-Float-Wert wird in ein 16-Bit-Float-renderTarget geschrieben), die maximale darstellbare (entsprechend signierte) Wert Ergebnisse, nicht einschließlich der Bits mit Vorzeichen (aufgrund der oben beschriebenen Runden auf null).
-   NaN wird in einem höheren Bereichs Format in eine Nan-Darstellung im unteren Bereichs Format konvertiert, wenn die Nan-Darstellung im unteren Bereichs Format vorhanden ist. Wenn das untere Format keine Nan-Darstellung hat, ist das Ergebnis 0 (null).
-   Inf in einem höheren Bereichs Format wird im unteren Bereichs Format in INF konvertiert, falls verfügbar. Wenn das untere Format keine INF-Darstellung hat, wird es in den maximalen Wert konvertiert, der darstellbar ist. Das Vorzeichen bleibt erhalten, wenn es im Zielformat verfügbar ist.
-   Denorm in einem höheren Bereichs Format wird in die denorm-Darstellung im unteren Bereichs Format konvertiert, wenn es im unteren Bereichs Format verfügbar und die Konvertierung möglich ist, andernfalls ist das Ergebnis 0. Das Signier Bit wird beibehalten, wenn es im Zielformat verfügbar ist.

### <a name="converting-from-a-lower-range-representation-to-a-higher-range-representation"></a>Wandeln von einer unteren Bereichs Darstellung in eine Darstellung mit höherem Bereich

-   NaN wird in einem niedrigeren Bereichs Format in die Nan-Darstellung im höheren Bereichs Format konvertiert, wenn es im höheren Bereichs Format verfügbar ist. Wenn das höhere Bereichs Format keine Nan-Darstellung hat, wird es in 0 konvertiert.
-   Inf in einem niedrigeren Bereichs Format wird in die INF-Darstellung im Format mit höherem Format konvertiert, wenn es im höheren Bereichs Format verfügbar ist. Wenn das höhere Format keine INF-Darstellung hat, wird es in den maximalen Wert konvertiert ( \_ in diesem Format Max float). Das Vorzeichen bleibt erhalten, wenn es im Zielformat verfügbar ist.
-   Denorm in einem niedrigeren Bereichs Format wird, wenn möglich, in eine normalisierte Darstellung im Format mit höherem Bereich oder andernfalls in eine denorm-Darstellung im höheren Bereichs Format konvertiert, wenn die denorm-Darstellung vorhanden ist. Wenn das höhere Bereichs Format nicht über eine denorm-Darstellung verfügt, wird es in 0 konvertiert. Das Vorzeichen bleibt erhalten, wenn es im Zielformat verfügbar ist. Beachten Sie, dass 32-Bit-Gleit Komma Zahlen als Format ohne denorm-Darstellung gezählt werden (da denorms in Vorgängen auf 32-Bit-Gleit Komma Zahlen zum Signieren beibehalten werden).

## <a name="integer-conversion"></a>Ganzzahlige Konvertierung

In der folgenden Tabelle werden die Konvertierungen von verschiedenen Darstellungen beschrieben, die in anderen Darstellungen beschrieben werden. Nur Konvertierungen, die tatsächlich in Direct3D auftreten, werden angezeigt.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Quell Datentyp</th>
<th>Ziel Datentyp</th>
<th>Konvertierungsregel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Snorm</td>
<td>GLEITKOMMAZAHL</td>
<td>Bei einem n-Bit-ganzzahligen Wert, der den signierten Bereich [-1.0 f bis 1.0 f] darstellt, ist die Konvertierung in den Gleit Komma Wert wie folgt.<br/>
<ul>
<li>Der negativste Wert wird-1.0 f zugeordnet. Beispielsweise wird der 5-Bit-Wert 10000 zu-1.0 f zugeordnet.</li>
<li>Jeder andere Wert wird in einen float-Wert konvertiert (c) und dann result = c * (1.0 f/(2 ⁽ ⁿ ⁻ ¹ ⁾-1)). Beispielsweise wird der 5-Bit-Wert 10001 in-15,0 f konvertiert und dann durch 15,0 f dividiert, was "-1.0 f" ergibt.</li>
</ul></td>
</tr>
<tr class="even">
<td>GLEITKOMMAZAHL</td>
<td>Snorm</td>
<td>Bei einer Gleit Komma Zahl ist die Konvertierung in einen n-Bit-ganzzahligen Wert, der den signierten Bereich [-1.0 f bis 1.0 f] darstellt, wie folgt.<br/>
<ul>
<li>C stellt den Startwert dar.</li>
<li>Wenn c ein NaN-Wert ist, ist das Ergebnis 0.</li>
<li>Wenn c > 1.0 f, einschließlich inf, wird es an 1.0 f gebunden.</li>
<li>Wenn c <-1.0 f, einschließlich-inf, wird es an-1.0 f gebunden.</li>
<li>Konvertieren von float-Skala in eine ganzzahlige Skala: c = c * (2 ⁿ ⁻ ¹-1).</li>
<li>Konvertieren Sie wie folgt in eine ganze Zahl.
<ul>
<li>Wenn c >= 0, dann c = c + 0,5 f, andernfalls c = c-0,5 f.</li>
<li>Löschen Sie den Dezimal Bruch, und der verbleibende Gleit Komma Wert (ganzzahliger Wert) wird direkt in eine ganze Zahl konvertiert.</li>
</ul></li>
</ul>
Für diese Konvertierung ist eine Toleranz von D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_Unit-Last-Place-Einheit-Last-Place (auf der ganzzahligen Seite) zulässig. Dies bedeutet, dass nach der Umstellung von float in eine ganzzahlige Skala jeder Wert innerhalb von D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place eines darstellbaren Ziel Formatwerts diesem Wert zugeordnet werden darf. Durch die zusätzliche Anforderung zur Daten Umkehrung wird sichergestellt, dass die Konvertierung im Bereich nicht abnimmt und alle Ausgabewerte erreichbar sind. (In den hier gezeigten Konstanten sollte <em>xx</em> durch die Direct3D-Version ersetzt werden, z. b. 10, 11 oder 12.)<br/></td>
</tr>
<tr class="odd">
<td>UNORM</td>
<td>GLEITKOMMAZAHL</td>
<td>Der n-Bit-Start Wert wird in float (0,0 f, 1.0 f, 2.0 f usw.) konvertiert und dann dividiert durch (2 ⁿ-1).<br/></td>
</tr>
<tr class="even">
<td>GLEITKOMMAZAHL</td>
<td>UNORM</td>
<td>C stellt den Startwert dar.<br/>
<ul>
<li>Wenn c ein NaN-Wert ist, ist das Ergebnis 0.</li>
<li>Wenn c > 1.0 f, einschließlich inf, wird es an 1.0 f gebunden.</li>
<li>Wenn c < 0,0 f, einschließlich-inf, wird es an 0,0 f gebunden.</li>
<li>Konvertieren von float-Skala in ganzzahlige Skala: c = c * (2 ⁿ-1).</li>
<li>In Integer konvertieren.
<ul>
<li>c = c + 0,5 f.</li>
<li>Der Dezimal Bruch wird gelöscht, und der verbleibende Gleit Komma Wert (ganzzahliger Wert) wird direkt in eine ganze Zahl konvertiert.</li>
</ul></li>
</ul>
Diese Konvertierung ist eine Toleranz von D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place (auf der ganzzahligen Seite) zulässig. Dies bedeutet, dass nach der Umstellung von float in eine ganzzahlige Skala jeder Wert innerhalb von D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place eines darstellbaren Ziel Formatwerts diesem Wert zugeordnet werden darf. Durch die zusätzliche Anforderung zur Daten Umkehrung wird sichergestellt, dass die Konvertierung im Bereich nicht abnimmt und alle Ausgabewerte erreichbar sind.<br/></td>
</tr>
<tr class="odd">
<td>SRGB</td>
<td>GLEITKOMMAZAHL</td>
<td>Im folgenden finden Sie die ideale sRGB to float-Konvertierung.<br/>
<ul>
<li>Nehmen Sie den ersten n-Bit-Wert, konvertieren Sie ihn in einen float-Wert (0,0 f, 1.0 f, 2.0 f usw.); nennen Sie diese c.</li>
<li>c = c * (1.0 f/(2 ⁿ-1))</li>
<li>If (c < = D3D<em>xx</em>_SRGB_TO_FLOAT_THRESHOLD), dann: result = c/D3D<em>xx</em>_SRGB_TO_FLOAT_DENOMINATOR_1, else: result = ((c + D3D<em>xx</em>_SRGB_TO_FLOAT_OFFSET)/D3D<em>xx</em>_SRGB_TO_FLOAT_DENOMINATOR_2) D3D<em>xx</em>_SRGB_TO_FLOAT_EXPONENT</li>
</ul>
Diese Konvertierung ist eine Toleranz von D3D<em>xx</em>_SRGB_TO_FLOAT_TOLERANCE_IN_ULP Unit-Last-Place (auf der sRGB-Seite) zulässig. <br/></td>
</tr>
<tr class="even">
<td>GLEITKOMMAZAHL</td>
<td>SRGB</td>
<td>Im folgenden finden Sie die ideale Konvertierung von float-> sRGB.<br/> Angenommen, die Ziel-sRGB-Farbkomponente hat n Bits:<br/>
<ul>
<li>Angenommen, der Startwert ist c.</li>
<li>Wenn c ein NaN-Wert ist, ist das Ergebnis 0.</li>
<li>Wenn c > 1.0 f, einschließlich inf, an 1.0 f gebunden wird.</li>
<li>Wenn c < 0,0 f, einschließlich-inf, wird es an 0,0 f gebunden.</li>
<li>If (c <= D3D<em>xx</em>_FLOAT_TO_SRGB_THRESHOLD), dann: c = D3D<em>xx</em>_FLOAT_TO_SRGB_SCALE_1 * c, else: c = D3D<em>xx</em>_FLOAT_TO_SRGB_SCALE_2 * c (D3D<em>xx</em>_FLOAT_TO_SRGB_EXPONENT_NUMERATOR/D3D<em>xx</em>_FLOAT_TO_SRGB_EXPONENT_DENOMINATOR)-D3D<em>xx</em>_FLOAT_TO_SRGB_OFFSET</li>
<li>Konvertieren von float-Skala in ganzzahlige Skala: c = c * (2 ⁿ-1).</li>
<li>In Integer konvertieren:
<ul>
<li>c = c + 0,5 f.</li>
<li>Der Dezimal Bruch wird gelöscht, und der verbleibende Gleit Komma Wert (ganzzahliger Wert) wird direkt in eine ganze Zahl konvertiert.</li>
</ul></li>
</ul>
Diese Konvertierung ist eine Toleranz von D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place (auf der ganzzahligen Seite) zulässig. Dies bedeutet, dass nach der Umstellung von float in eine ganzzahlige Skala jeder Wert innerhalb von D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place eines darstellbaren Ziel Formatwerts diesem Wert zugeordnet werden darf. Durch die zusätzliche Anforderung zur Daten Umkehrung wird sichergestellt, dass die Konvertierung im Bereich nicht abnimmt und alle Ausgabewerte erreichbar sind.<br/></td>
</tr>
<tr class="odd">
<td>St</td>
<td>Sint mit mehr Bits</td>
<td>Zum Konvertieren von "Sint" in ein "Sint" mit mehr Bits wird das höchst wertige Bit (MSB) der Anfangszahl &quot; &quot; auf die zusätzlichen Bits, die im Zielformat verfügbar sind, erweitert.<br/></td>
</tr>
<tr class="even">
<td>UINT</td>
<td>Sint mit mehr Bits</td>
<td>Zum Konvertieren von uint in ein Sint mit mehr Bits wird die Zahl in die niedrigsten Bits (LSB) des Ziel Formats kopiert, und zusätzliche MSB-Elemente werden mit 0 aufgefüllt.<br/></td>
</tr>
<tr class="odd">
<td>St</td>
<td>Uint mit mehr Bits</td>
<td>Zum Konvertieren von "Sint" in "uint" mit mehr Bits: bei einem negativen Wert wird der Wert auf 0 (null) geklammert. Andernfalls wird die Zahl in die lsbs des Ziel Formats kopiert, und zusätzliche MSB-Werte werden mit 0 aufgefüllt.<br/></td>
</tr>
<tr class="even">
<td>UINT</td>
<td>Uint mit mehr Bits</td>
<td>Zum Konvertieren von uint in uint mit mehr Bits wird die Zahl in die lsbs des Ziel Formats kopiert, und zusätzliche MSB-Elemente werden mit 0 aufgefüllt.<br/></td>
</tr>
<tr class="odd">
<td>Sint oder uint</td>
<td>Sint oder uint mit weniger oder gleich Bits</td>
<td>Zum Konvertieren von einem Sint oder uint in Sint oder uint mit weniger oder gleicher Bits (und/oder Änderung der Signatur) wird der Startwert einfach an den Bereich des Ziel Formats gebunden.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="fixed-point-integer-conversion"></a>Konvertierung fester ganzzahliger Zeichen

Bei Ganzzahlen mit fester Größe handelt es sich einfach um Ganzzahlen mit einer bitgröße, die einen impliziten Dezimaltrennzeichen an einer festgelegten Position aufweisen.

Der universelle ganzzahlige Datentyp ist ein Sonderfall einer ganzzahligen Ganzzahl mit dem Dezimaltrennzeichen am Ende der Zahl.

Die Darstellungen von fest Komma Zahlen sind wie folgt gekennzeichnet: i. f, wobei es sich um die Anzahl der ganzzahligen Bits und f um die Anzahl der Dezimalstellen handelt. z. b. 16,8 bedeutet 16 Bit Ganzzahl, gefolgt von 8 Bits Bruchteil. Der ganzzahlige Teil wird in einem 2-Komplement gespeichert, zumindest wie hier definiert (er kann jedoch auch für ganze Zahlen ohne Vorzeichen gleich definiert werden). Der Bruchteile wird in einem unsignierten Formular gespeichert. Der Bruchteil der Teile stellt immer den positiven Bruchteil zwischen den beiden nächstliegenden ganzzahligen Werten dar, beginnend bei den meisten negativen.

Additions-und Subtraktions Vorgänge für festgelegte Punktzahlen werden einfach mithilfe der standardmäßigen ganzzahligen Arithmetik ausgeführt, ohne dass dabei berücksichtigt wird, wo das implizite Dezimaltrennzeichen Das Hinzufügen von 1 zu einer 16,8-fixpunktzahl bedeutet nur, dass 256 hinzugefügt wird, da das Dezimaltrennzeichen 8 Stellen in vom am wenigsten signifikanten Ende der Zahl ist. Andere Vorgänge, wie z. b. Multiplikation, können auch einfach ganzzahlige Arithmetik verwendet werden, vorausgesetzt, die Auswirkung auf das fixierte Dezimaltrennzeichen wird berücksichtigt Beispielsweise ergibt die Multiplikation von zwei 16,8-Ganzzahlen mit einer ganzzahligen Multiplikation ein 32,16-Ergebnis.

Ganzzahlige Darstellungen mit fester Zahl werden in Direct3D auf zwei Arten verwendet.

-   Post-clipped-Vertexpositionen im Raster werden an einen Fixed-Punkt angedockt, um die Genauigkeit gleichmäßig über den renderTarget-Bereich zu verteilen. Viele Raster-Vorgänge, einschließlich der Gesichtserkennung als Beispiel, treten an festgelegten Positionen an festgelegtem Punkt auf, während andere Vorgänge, wie z. b. das Attribut interpolatorsetup, Positionen verwenden, die von den fixierten Positionen zurück in Gleit Komma konvertiert wurden.
-   Texturkoordinaten für Samplings werden an einen fixierten Punkt (nach der Skalierung nach Textur Größe) angedockt, um die Genauigkeit gleichmäßig über den Textur Bereich zu verteilen Gewichtungswerte werden zurück in den Gleit Komma Wert konvertiert, bevor die eigentliche Filter Arithmetik ausgeführt wird.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Quell Datentyp</th>
<th>Ziel Datentyp</th>
<th>Konvertierungsregel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GLEITKOMMAZAHL</td>
<td>Ganzzahlige Ganzzahl</td>
<td>Im folgenden wird das allgemeine Verfahren zum umrechnen einer Gleit Komma Zahl n in eine feste Ganzzahl i. f beschrieben. Hierbei handelt es sich um die Anzahl der (signierten) ganzzahligen Bits und f für die Anzahl der Dezimalstellen.<br/>
<ul>
<li>Compute fixedmin =-2 ⁽ ⁱ ⁻ ¹ ⁾</li>
<li>Compute fixedmax = 2 ⁽ ⁱ ⁻ ¹ ⁾-2<sup>(-f)</sup></li>
<li>Wenn n ein NaN ist, Ergebnis = 0; Wenn n + inf ist, Ergebnis = fixedmax * 2<sup>f</sup>; Wenn n "-inf" ist, Ergebnis = fixedmin * 2<sup>f</sup></li>
<li>Wenn n >= fixedmax, result = fixedmax * 2<sup>f</sup>; Wenn n <= fixedmin, result = fixedmin * 2 <sup> f</sup></li>
<li>Andernfalls wird n * 2<sup>f</sup> berechnet und in eine ganze Zahl konvertiert.</li>
</ul>
Implementierungen sind im ganzzahligen Ergebnis anstelle des unendlich präzisen Werts n * 2<sup>f</sup> nach dem letzten Schritt im ganzzahligen Ergebnis zulässig D3D _FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP<em>xx</em>.<br/></td>
</tr>
<tr class="even">
<td>Ganzzahlige Ganzzahl</td>
<td>GLEITKOMMAZAHL</td>
<td>Angenommen, die spezifische, in float konvertierte feste Punkt Darstellung enthält nicht mehr als insgesamt 24 Bits von Informationen, von denen sich nicht mehr als 23 Bits in der Bruchteil-Komponente befinden. Angenommen, eine angegebene fest Komma Zahl, "f XP", befindet sich in "i. f" (i Bit Integer, f Bits Bruchzahl). Die Konvertierung in float ähnelt dem folgenden Pseudocode.<br/> float result = (float) (f XP >> f) +//ganze Zahl extrahieren<br/> <dl> ((float) (SXP & (2<sup>f</sup> - 1))/(2<sup>f</sup>));//Bruchteil extrahieren<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




