---
description: In den folgenden Abschnitten wird beschrieben, wie Direct3D Konvertierungen zwischen Datentypen behandelt.
ms.assetid: 454d3fd0-fc0f-46a9-925e-13f8e3c39f02
title: Datenkonvertierungsregeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b5ba37305fb7cadc229a614b883519cf6c5f45
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626296"
---
# <a name="data-conversion-rules"></a>Datenkonvertierungsregeln

In den folgenden Abschnitten wird beschrieben, wie Direct3D Konvertierungen zwischen Datentypen behandelt.

-   [Datentypterminologie](#data-type-terminology)
-   [Gleitkommakonvertierung](#floating-point-conversion)
    -   [Konververtierung von einer Darstellung eines höheren Bereichs zu einer Darstellung im unteren Bereich](#conververting-from-a-higher-range-representation-to-a-lower-range-representation)
    -   [Konvertieren von einer Darstellung im unteren Bereich in eine höhere Bereichsdarstellung](#converting-from-a-lower-range-representation-to-a-higher-range-representation)
-   [Ganzzahlkonvertierung](#integer-conversion)
-   [Ganzzahlige Konvertierung mit festem Punkt](#fixed-point-integer-conversion)
-   [Zugehörige Themen](#related-topics)

## <a name="data-type-terminology"></a>Datentypterminologie

Anschließend werden die folgenden Begriffe verwendet, um verschiedene Formatkonvertierungen zu charakterisieren.



| Begriff  | Definition                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNORM | Normalisierte ganze Zahl mit Vorzeichen, d.h. für die Komplementnummer eines n-Bit-2 bedeutet der Höchstwert 1,0f (z.B. wird der 5-Bit-Wert 01111 1,0f zugeordnet), und der Mindestwert bedeutet -1,0f (z.B. der 5-Bit-Wert 10000 entspricht -1,0f). Darüber hinaus wird die zweite Mindestzahl -1,0f zugeordnet (z.B. wird der 5-Bit-Wert 10001 -1,0f zugeordnet). Es gibt also zwei ganzzahlige Darstellungen für -1,0f. Es gibt eine einzelne Darstellung für 0,0f und eine einzelne Darstellung für 1.0f. Dies führt zu einer Reihe von ganzzahligen Darstellungen für gleitkommawerte mit gleichmäßiger Leerstelle im Bereich (-1,0f... 0,0f) und eine ergänzende Gruppe von Darstellungen für Zahlen im Bereich (0,0f... 1.0f) |
| UNORM | Normalisierte ganze Zahl ohne Vorzeichen, was bedeutet, dass für eine n-Bit-Zahl alle 0-Werte 0,0f und alle 1-Werte 1,0f bedeuten. Eine Sequenz von gleitkommawerten mit geradem Abstand von 0,0f bis 1,0f wird dargestellt. Beispielsweise stellt eine 2-Bit-UNORM 0,0f, 1/3, 2/3 und 1,0f dar.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SINT  | Ganze Zahl mit Vorzeichen. Die Komplement-Ganzzahl von 2. Beispielsweise stellt ein 3-Bit-SINT die Ganzzahlwerte -4, -3, -2, -1, 0, 1, 2, 3 dar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| UINT  | Ganze Zahl ohne Vorzeichen. Beispielsweise stellt ein 3-Bit-UINT die Ganzzahlwerte 0, 1, 2, 3, 4, 5, 6, 7 dar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| GLEITKOMMAZAHL | Ein Gleitkommawert in einer der durch Direct3D definierten Darstellungen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| SRGB  | Ähnlich wie bei UNORM bedeutet dies, dass für eine n-Bit-Zahl alle 0(e) 0,0f und alle 1 für 1,0f bedeuten. Im Gegensatz zu UNORM stellt die Sequenz von ganzzahligen Codierungen ohne Vorzeichen zwischen allen 1ern von 0 bis 1 jedoch einen nicht linearen Fortschritt in der Gleitkommainterpretation der Zahlen zwischen 0,0f und 1,0f dar. Wenn dieser nicht lineare Fortschritt (SRGB) in etwa als Sequenz von Farben angezeigt wird, wird er als lineare Rampe von Helligkeitsstufen für einen "durchschnittlichen" Beobachter unter "durchschnittlichen" Anzeigebedingungen auf einer "durchschnittlichen" Anzeige angezeigt. Ausführliche Informationen finden Sie im SRGB-Farbstandard IEC 61996-2-1 unter IEC (Internationale Elektrotechnische Kommission).                |



 

## <a name="floating-point-conversion"></a>Gleitkommakonvertierung

Immer wenn eine Gleitkommakonvertierung zwischen verschiedenen Darstellungen auftritt, einschließlich in oder aus Nicht-Gleitkommadarstellungen, gelten die folgenden Regeln.

### <a name="conververting-from-a-higher-range-representation-to-a-lower-range-representation"></a>Konververtierung von einer Darstellung eines höheren Bereichs zu einer Darstellung im unteren Bereich

-   Round-to-Zero wird während der Konvertierung in ein anderes float-Format verwendet. Wenn das Ziel ein Ganzzahl- oder Festkommaformat ist, wird "Round-to-Nearest-even" verwendet, es sei denn, die Konvertierung wird explizit mit einem anderen Rundungsverhalten dokumentiert, z. B. "Round-to-Nearest" für FLOAT in SNORM, FLOAT in UNORM oder FLOAT in SRGB. Andere Ausnahmen sind die Ftoi- und ftou-Shaderanweisungen, die Round-to-Zero verwenden. Schließlich verfügen die vom Textur sampler und rasterizer verwendeten Gleitkommakonvertierungen in feste Werte über eine angegebene Toleranz, die in Unit-Last-Place von einem unendlich präzisen Ideal aus gemessen wird.
-   Für Quellwerte, die größer als der dynamische Bereich eines Zielformats mit niedrigerem Bereich sind (z. B. Ein großer 32-Bit-Gleitkommawert wird in ein 16-Bit-Float-RenderTarget geschrieben. Dabei handelt es sich um die maximal darstellbaren (entsprechend signierten) Wertergebnisse, DIE NICHT mit Vorzeichen unendlich sind (aufgrund der oben beschriebenen Rundung auf null).
-   NaN in einem höheren Bereichsformat wird in eine NaN-Darstellung im unteren Bereichsformat konvertiert, wenn die NaN-Darstellung im unteren Bereichsformat vorhanden ist. Wenn das untere Format keine NaN-Darstellung hat, ist das Ergebnis 0.
-   INF in einem höheren Bereichsformat wird im unteren Bereichsformat in INF konvertiert, falls verfügbar. Wenn das untere Format keine INF-Darstellung hat, wird es in den maximal darstellbaren Wert konvertiert. Das Vorzeichen wird beibehalten, wenn es im Zielformat verfügbar ist.
-   Denorm in einem höheren Bereichsformat wird in die Denorm-Darstellung im unteren Bereichsformat konvertiert, sofern im unteren Bereichsformat verfügbar, und die Konvertierung ist möglich, andernfalls ist das Ergebnis 0. Das Vorzeichenbit wird beibehalten, wenn es im Zielformat verfügbar ist.

### <a name="converting-from-a-lower-range-representation-to-a-higher-range-representation"></a>Konvertieren von einer Darstellung im unteren Bereich in eine höhere Bereichsdarstellung

-   NaN in einem niedrigeren Bereichsformat wird in die NaN-Darstellung im höheren Bereichsformat konvertiert, sofern im höheren Bereichsformat verfügbar. Wenn das höhere Bereichsformat keine NaN-Darstellung hat, wird es in 0 konvertiert.
-   INF in einem niedrigeren Bereichsformat wird in die INF-Darstellung im höheren Bereichsformat konvertiert, sofern im höheren Bereichsformat verfügbar. Wenn das höhere Format keine INF-Darstellung hat, wird es in den maximal darstellbaren Wert konvertiert (MAX \_ FLOAT in diesem Format). Das Vorzeichen wird beibehalten, wenn es im Zielformat verfügbar ist.
-   Denorm in einem niedrigeren Bereichsformat wird nach Möglichkeit in eine normalisierte Darstellung im höheren Bereichsformat konvertiert, oder in eine Denorm-Darstellung im höheren Bereichsformat, wenn die Denorm-Darstellung vorhanden ist. Wenn das höhere Bereichsformat nicht über eine Denorm-Darstellung verfügt, wird es in 0 konvertiert. Das Vorzeichen wird beibehalten, wenn es im Zielformat verfügbar ist. Beachten Sie, dass 32-Bit-Gleitkommazahlen als Format ohne Denorm-Darstellung zählen (da Denorms in Vorgängen für 32-Bit-Gleitkommawerte leert, um das Vorzeichen beizubehalten 0).

## <a name="integer-conversion"></a>Ganzzahlkonvertierung

In der folgenden Tabelle werden Konvertierungen von verschiedenen oben beschriebenen Darstellungen in andere Darstellungen beschrieben. Es werden nur Konvertierungen angezeigt, die tatsächlich in Direct3D auftreten.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Quelldatentyp</th>
<th>Zieldatentyp</th>
<th>Konvertierungsregel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SNORM</td>
<td>GLEITKOMMAZAHL</td>
<td>Bei einem n-Bit-Ganzzahlwert, der den Bereich mit Vorzeichen [-1,0f bis 1,0f] darstellt, erfolgt die Konvertierung in Gleitkomma wie folgt.<br/>
<ul>
<li>Der negativste Wert wird -1,0f zugeordnet. Beispielsweise wird der 5-Bit-Wert 10000 -1,0f zugeordnet.</li>
<li>Jeder andere Wert wird in einen float-Wert konvertiert (nennen Sie ihn c), und dann result = c * (1,0f / (2⁽ⁿ⁻¹⁾-1)). Beispielsweise wird der 5-Bit-Wert 10001 in -15.0f konvertiert und dann durch 15,0f geteilt und ergibt -1,0f.</li>
</ul></td>
</tr>
<tr class="even">
<td>GLEITKOMMAZAHL</td>
<td>SNORM</td>
<td>Bei einer Gleitkommazahl erfolgt die Konvertierung in einen ganzzahligen n-Bit-Wert, der den Bereich mit Vorzeichen [-1,0f bis 1,0f] darstellt, wie folgt.<br/>
<ul>
<li>Lassen Sie c den Startwert darstellen.</li>
<li>Wenn c naN ist, ist das Ergebnis 0.</li>
<li>Wenn c > 1.0f, einschließlich INF, wird es an 1.0f klammern.</li>
<li>Wenn c -1.0f <, einschließlich -INF, wird es an -1.0f klammern.</li>
<li>Konvertieren von float scale in integer scale: c = c * (2ⁿ⁻¹-1).</li>
<li>Konvertieren Sie wie folgt in eine ganze Zahl.
<ul>
<li>Wenn c >= 0 ist, dann c = c + 0,5f, andernfalls c = c - 0,5f.</li>
<li>Löschen Sie den Dezimalbruch, und der verbleibende Gleitkommawert (ganzzahlig) wird direkt in eine ganze Zahl konvertiert.</li>
</ul></li>
</ul>
Diese Konvertierung lässt eine Toleranz von D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_Unit-Last-Place Unit-Last-Place (ganzzahlig) zu. Dies bedeutet, dass nach der Konvertierung von float in integer scale jeder Wert innerhalb von D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place eines darstellbaren Zielformatwerts diesem Wert zugeordnet werden kann. Die zusätzliche Anforderung an die Datenumkehrbarkeit stellt sicher, dass die Konvertierung im gesamten Bereich nicht dekreasiert wird und alle Ausgabewerte erreichbar sind. (In den hier gezeigten Konstanten sollte <em>xx</em> durch die Direct3D-Version ersetzt werden, z.B. 10, 11 oder 12.)<br/></td>
</tr>
<tr class="odd">
<td>UNORM</td>
<td>GLEITKOMMAZAHL</td>
<td>Der n-Bit-Startwert wird in float (0,0f, 1,0f, 2,0f usw.) konvertiert und dann durch (2ⁿ-1) geteilt.<br/></td>
</tr>
<tr class="even">
<td>GLEITKOMMAZAHL</td>
<td>UNORM</td>
<td>Lassen Sie c den Startwert darstellen.<br/>
<ul>
<li>Wenn c naN ist, ist das Ergebnis 0.</li>
<li>Wenn c > 1.0f, einschließlich INF, wird es an 1.0f klammern.</li>
<li>Wenn c < 0.0f, einschließlich -INF, wird es an 0.0f klammern.</li>
<li>Konvertieren von float scale in integer scale: c = c * (2ⁿ-1).</li>
<li>Konvertieren sie in eine ganze Zahl.
<ul>
<li>c = c + 0,5f.</li>
<li>Der Dezimalbruch wird gelöscht, und der verbleibende Gleitkommawert (ganzzahlig) wird direkt in eine ganze Zahl konvertiert.</li>
</ul></li>
</ul>
Diese Konvertierung ist mit einer Toleranz von D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place (ganzzahlig) zulässig. Dies bedeutet, dass nach der Konvertierung von float in integer scale jeder Wert innerhalb von D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place eines darstellbaren Zielformatwerts diesem Wert zugeordnet werden kann. Die zusätzliche Anforderung an die Datenumkehrbarkeit stellt sicher, dass die Konvertierung im gesamten Bereich nicht dekreasiert wird und alle Ausgabewerte erreichbar sind.<br/></td>
</tr>
<tr class="odd">
<td>SRGB</td>
<td>GLEITKOMMAZAHL</td>
<td>Im Folgenden finden Sie die ideale SRGB- in FLOAT-Konvertierung.<br/>
<ul>
<li>Nehmen Sie den n-Bit-Startwert, und konvertieren Sie ihn in float (0,0f, 1,0f, 2,0f usw.). rufen Sie diese c auf.</li>
<li>c = c * (1,0f / (2ⁿ-1))</li>
<li>Wenn (c < = D3D<em>xx</em>_SRGB_TO_FLOAT_THRESHOLD), dann: result = c / D3D<em>xx</em>_SRGB_TO_FLOAT_DENOMINATOR_1, andernfalls: result = ((c + D3D<em>xx</em>_SRGB_TO_FLOAT_OFFSET)/D3D<em>xx</em>_SRGB_TO_FLOAT_DENOMINATOR_2)D3D<em>xx</em>_SRGB_TO_FLOAT_EXPONENT</li>
</ul>
Für diese Konvertierung ist eine Toleranz von D3D<em>xx</em>_SRGB_TO_FLOAT_TOLERANCE_IN_ULP Unit-Last-Place (auf srgb-Seite) zulässig. <br/></td>
</tr>
<tr class="even">
<td>GLEITKOMMAZAHL</td>
<td>SRGB</td>
<td>Im Folgenden finden Sie die ideale FLOAT -> SRGB-Konvertierung.<br/> Angenommen, die SRGB-Zielfarbkomponente verfügt über n Bits:<br/>
<ul>
<li>Angenommen, der Anfangswert ist c.</li>
<li>Wenn c naN ist, ist das Ergebnis 0.</li>
<li>Wenn c > 1.0f, einschließlich INF, wird an 1.0f klammern.</li>
<li>Wenn c < 0.0f, einschließlich -INF, wird es an 0.0f klammern.</li>
<li>Wenn (c <= D3D<em>xx</em>_FLOAT_TO_SRGB_THRESHOLD), dann: c = D3D<em>xx</em>_FLOAT_TO_SRGB_SCALE_1 * c, andernfalls: c = D3D<em>xx</em>_FLOAT_TO_SRGB_SCALE_2 * c(D3D<em>xx</em>_FLOAT_TO_SRGB_EXPONENT_NUMERATOR/D3D<em>xx</em>_FLOAT_TO_SRGB_EXPONENT_DENOMINATOR) - D3D<em>xx</em>_FLOAT_TO_SRGB_OFFSET</li>
<li>Konvertieren von float scale in integer scale: c = c * (2ⁿ-1).</li>
<li>In ganze Zahl konvertieren:
<ul>
<li>c = c + 0,5f.</li>
<li>Der Dezimalbruch wird gelöscht, und der verbleibende Gleitkommawert (ganzzahlig) wird direkt in eine ganze Zahl konvertiert.</li>
</ul></li>
</ul>
Diese Konvertierung ist mit einer Toleranz von D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place (ganzzahlig) zulässig. Dies bedeutet, dass nach der Konvertierung von float in integer scale jeder Wert innerhalb von D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place eines darstellbaren Zielformatwerts diesem Wert zugeordnet werden kann. Die zusätzliche Anforderung an die Datenumkehrbarkeit stellt sicher, dass die Konvertierung im gesamten Bereich nicht dekreasiert wird und alle Ausgabewerte erreichbar sind.<br/></td>
</tr>
<tr class="odd">
<td>SINT</td>
<td>SINT mit mehr Bits</td>
<td>Um von SINT in ein SINT mit mehr Bits zu konvertieren, wird das wichtigste Bit (MSB) der Startnummer &quot; auf die zusätzlichen Bits erweitert, &quot; die im Zielformat verfügbar sind.<br/></td>
</tr>
<tr class="even">
<td>UINT</td>
<td>SINT mit mehr Bits</td>
<td>Um von UINT in ein SINT mit mehr Bits zu konvertieren, wird die Zahl in die LSBs (Least Significant Bits) des Zielformats kopiert, und zusätzliche MSBs werden mit 0 aufgefüllt.<br/></td>
</tr>
<tr class="odd">
<td>SINT</td>
<td>UINT mit mehr Bits</td>
<td>So konvertieren Sie von SINT in UINT mit mehr Bits: Wenn negativ, wird der Wert an 0 (null) klammern. Andernfalls wird die Zahl in die LSBs des Zielformats kopiert, und zusätzliche MSB-Dateien werden mit 0 aufgefüllt.<br/></td>
</tr>
<tr class="even">
<td>UINT</td>
<td>UINT mit mehr Bits</td>
<td>Zum Konvertieren von UINT in UINT mit mehr Bits wird die Zahl in die LSBs des Zielformats kopiert, und zusätzliche MSBs werden mit 0 aufgefüllt.<br/></td>
</tr>
<tr class="odd">
<td>SINT oder UINT</td>
<td>SINT oder UINT mit weniger oder gleichen Bits</td>
<td>Zum Konvertieren von einem SINT- oder UINT-Wert in SINT oder UINT mit weniger oder gleichen Bits (und/oder Änderung der Vorzeichen) wird der Startwert einfach an den Bereich des Zielformats angepasst.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="fixed-point-integer-conversion"></a>Ganzzahlige Konvertierung mit festem Punkt

Ganzzahlen mit festem Punkt sind einfach ganze Zahlen mit einer Bitgröße, die ein implizites Dezimaltrennzeichen an einer festen Position aufweisen.

Der ubiquitäre Datentyp "integer" ist ein Sonderfall einer ganzzahligen Festkommazahl mit dem Dezimalwert am Ende der Zahl.

Darstellungen von Festkommazahlen sind folgendermaßen gekennzeichnet: i.f, wobei i die Anzahl ganzzahliger Bits und f die Anzahl der Bruchbits ist. Beispielsweise bedeutet 16,8 eine ganze Zahl von 16 Bits gefolgt von 8 Bits fraction. Der ganzzahlige Teil wird im Komplement von 2 gespeichert, zumindest wie hier definiert (obwohl es auch für ganze Zahlen ohne Vorzeichen gleich definiert werden kann). Der Bruchteil wird in nicht signierter Form gespeichert. Der Bruchteil stellt immer den positiven Bruch zwischen den beiden nächsten ganzzahligen Werten dar, beginnend mit dem negativsten.

Additions- und Subtraktionsvorgänge für Festkommazahlen werden einfach mithilfe von ganzzahligen Standardarithmetik durchgeführt, ohne dass berücksichtigt wird, wo die implizite Dezimalzahl liegt. Das Hinzufügen von 1 zu einer festen Punktzahl von 16,8 bedeutet lediglich das Hinzufügen von 256, da die Dezimalzahl 8 Stellen vom am wenigsten signifikanten Ende der Zahl entfernt ist. Andere Vorgänge wie die Multiplikation können auch einfach mit ganzzahliger Arithmetik ausgeführt werden, vorausgesetzt, die Auswirkung auf die feste Dezimalzahl wird berücksichtigt. Die Multiplikation von zwei 16,8 ganzzahligen Zahlen mit einer ganzzahligen Multiplikation führt beispielsweise zu einem Ergebnis von 32,16.

Ganzzahldarstellungen mit Festkommawerten werden in Direct3D auf zwei Arten verwendet.

-   Nachgeschnittene Scheitelpunktpositionen im Rasterizer werden an einem festen Punkt ausgerichtet, um die Genauigkeit gleichmäßig auf den RenderTarget-Bereich zu verteilen. Viele Rasterizervorgänge, z. B. die Gesichtskeulung, treten an fixierten Positionen auf, während andere Vorgänge, z. B. die Einrichtung des Attributinterpolators, Positionen verwenden, die von den fixierten Positionen zurück in Gleitkomma konvertiert wurden.
-   Texturkoordinaten für Samplingvorgänge werden an einem festen Punkt ausgerichtet (nachdem sie durch die Texturgröße skaliert wurden), um die Genauigkeit gleichmäßig auf den Texturraum zu verteilen, indem Die Positionen/Gewichtungen des Filtertippens ausgewählt werden. Gewichtungswerte werden wieder in Gleitkommawerte konvertiert, bevor die eigentliche Filterarithmetik durchgeführt wird.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Quelldatentyp</th>
<th>Zieldatentyp</th>
<th>Konvertierungsregel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GLEITKOMMAZAHL</td>
<td>Ganze Zahl mit festem Punkt</td>
<td>Im Folgenden finden Sie das allgemeine Verfahren zum Konvertieren einer Gleitkommazahl n in eine ganzzahlige Festkommazahl i.f, wobei i die Anzahl der ganzzahligen Bits (mit Vorzeichen) und f die Anzahl der Bruchbits ist.<br/>
<ul>
<li>Compute FixedMin = -2⁽ⁱ⁻¹⁾</li>
<li>Compute FixedMax = 2⁽ⁱ⁻¹⁾ - 2<sup>(-f)</sup></li>
<li>Wenn n ein NaN ist, ist das Ergebnis = 0; , wenn n +Inf ist, result = FixedMax*2<sup>f</sup>; wenn n -Inf ist, result = FixedMin*2<sup>f</sup></li>
<li>Wenn n >= FixedMax, result = Fixedmax*2<sup>f</sup>; , wenn n <= FixedMin, result = FixedMin*2 <sup> f</sup></li>
<li>Berechnen Sie andernfalls n*2<sup>f,</sup> und konvertieren Sie in ganze Zahlen.</li>
</ul>
Implementierungen sind D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place-Toleranz im ganzzahligen Ergebnis zulässig, anstatt den unendlich genauen Wert n*2<sup>f</sup> nach dem letzten Schritt oben.<br/></td>
</tr>
<tr class="even">
<td>Ganze Zahl mit festem Punkt</td>
<td>GLEITKOMMAZAHL</td>
<td>Angenommen, die spezifische Festkommadarstellung, die in float konvertiert wird, enthält nicht mehr als insgesamt 24 Bits an Informationen, von denen sich nicht mehr als 23 Bits in der Bruchteilkomponente befinden. Angenommen, eine angegebene feste Punktzahl, fxp, hat die Form i.f (i bits integer, f bits fraction). Die Konvertierung in float ähnelt dem folgenden Pseudocode.<br/> float result = (float)(fxp >> f) + / extract integer<br/> <dl> ((float)(fxp & (2<sup>f</sup> - 1)) / (2<sup>f</sup>)); / extract fraction<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




