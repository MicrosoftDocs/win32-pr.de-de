---
description: Direct3D 10 unterstützt mehrere verschiedene Gleit Komma Darstellungen. Alle Gleit Komma Berechnungen arbeiten unter einer definierten Teilmenge des IEEE 754 32-Bit-Gleit Komma Verhaltens mit einfacher Genauigkeit.
ms.assetid: 57221d13-8993-4db3-b1a0-88bdcf6f0167
title: Ffloating-Point-Regeln (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6909d037b11f9098bb3e0dbad0f1846b79b513e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344828"
---
# <a name="floating-point-rules-direct3d-10"></a>Gleit Komma Regeln (Direct3D 10)

Direct3D 10 unterstützt mehrere verschiedene Gleit Komma Darstellungen. Alle Gleit Komma Berechnungen arbeiten unter einer definierten Teilmenge des IEEE 754 32-Bit-Gleit Komma Verhaltens mit einfacher Genauigkeit.

-   [32-Bit-Floating-Point Regeln](#32-bit-floating-point-rules)
    -   [IEEE-754-Regeln wurden berücksichtigt.](#honored-ieee-754-rules)
    -   [Abweichungen oder zusätzliche Anforderungen von IEEE-754-Regeln](#deviations-or-additional-requirements-from-ieee-754-rules)
-   [Regeln für 16-Bit-Floating-Point](#16-bit-floating-point-rules)
-   [11-Bit-und 10-Bit-Floating-Point Regeln](#11-bit-and-10-bit-floating-point-rules)
-   [Zugehörige Themen](#related-topics)

## <a name="32-bit-floating-point-rules"></a>32-Bit-Floating-Point Regeln

Es gibt zwei Sätze von Regeln: die, die IEEE-754 entsprechen, und die Regeln, die vom Standard abweichen.

### <a name="honored-ieee-754-rules"></a>IEEE-754-Regeln wurden berücksichtigt.

Einige dieser Regeln stellen eine einzelne Option dar, bei der IEEE-754 Optionen bietet.

-   Division durch 0 erzeugt +/-inf, mit Ausnahme von 0/0, was zu Nan führt.
-   das Protokoll von (+/-) 0 erzeugt-inf. das Protokoll eines negativen Werts (mit Ausnahme von-0) erzeugt Nan.
-   Die gegenseitige Quadratwurzel (RSQ) oder die Quadratwurzel (sqrt) einer negativen Zahl erzeugt Nan. Die Ausnahme ist-0; SQRT (-0) erzeugt-0, und RSQ (-0) erzeugt-inf.
-   INF-INF = Nan
-   (+/-) Inf/(+/-) INF = Nan
-   (+/-) INF \* 0 = Nan
-   Nan (beliebiger OP) beliebiger Wert = NaN
-   Die Vergleiche EQ, gt, ge, lt und Le, wenn einer oder beide Operanden NaN ist, wird **false** zurückgegeben.
-   Vergleiche ignorieren das Vorzeichen von 0 (also + 0 ist 0).
-   Der Vergleichs-ne, wenn einer oder beide Operanden NaN ist, wird **true** zurückgegeben.
-   Vergleiche eines beliebigen nicht-NaN-Werts mit +/-INF geben das korrekte Ergebnis zurück.

### <a name="deviations-or-additional-requirements-from-ieee-754-rules"></a>Abweichungen oder zusätzliche Anforderungen von IEEE-754-Regeln

-   IEEE-754 erfordert Gleit Komma Vorgänge, um ein Ergebnis zu erhalten, das den nächstgelegenen darstellbaren Wert zu einem unendlich präzisen Ergebnis ist, das auch als "Round-to-Next-even" bezeichnet wird. Direct3D 10 definiert jedoch eine lockere Anforderung: 32-Bit-Gleit Komma Operationen führen zu einem Ergebnis, das sich innerhalb einer Einheits Last Stelle (1 ULP) des unendlich präzisen Ergebnisses befindet. Dies bedeutet, dass Hardware z. b. die Ergebnisse in 32-Bit Abschneiden darf, anstatt Sie durch eine roundTo-Next-even-Methode auszuführen, da dies zu einem Fehler bei höchstens einer ULP führen würde.
-   Es gibt keine Unterstützung für Gleit Komma Ausnahmen, Status Bits oder Traps.
-   Denorms werden bei einem Eingabe-und Ausgabewert einer mathematischen Gleit Komma Operation in die Signierung NULL geleert. Ausnahmen werden für alle e/a-oder Daten Verschiebungs Vorgänge ausgelöst, die die Daten nicht verändern.
-   Zustände, die Gleit Komma Werte enthalten, wie z. b. Viewport mintiefe/maxtiefe, BorderColor-Werte usw., werden möglicherweise als denorm-Werte angegeben und können vor der Verwendung durch die Hardware geleert werden.
-   Bei minimalen oder maximalen Vorgängen werden denorms zum Vergleichen geleert, das Ergebnis kann jedoch nicht mit denorm geleert werden.
-   Die Nan-Eingabe für einen Vorgang erzeugt immer Nan in der Ausgabe, aber das genaue Bitmuster von Nan muss nicht gleich bleiben (es sei denn, der Vorgang ist eine unformatierte Move-Anweisung, die Daten überhaupt nicht ändert.)
-   Minimale oder maximale Vorgänge, für die nur ein Operand NaN ist, geben den anderen Operanden als Ergebnis zurück (im Gegensatz zu den obigen Vergleichs Regeln). Dies ist eine neue IEEE-Regel (IEEE 754r), die in Direct3D 10 erforderlich ist.
-   Eine weitere neue IEEE 754r-Regel ist, dass min (-0, + 0) = = min (+ 0,-0) = =-0 und Max (-0, + 0) = = Max (+ 0,-0) = = + 0, die das Vorzeichen beachten, im Gegensatz zu den Vergleichs Regeln für signed Zero (oben angegeben). Direct3D 10 empfiehlt das IEEE 754r-Verhalten, wird jedoch nicht erzwungen. Es ist zulässig, dass das Ergebnis des Vergleichs von Nullen von der Reihenfolge der Parameter abhängig ist. dabei wird ein Vergleich verwendet, bei dem die Vorzeichen ignoriert werden.
-   x \* 1.0 f ergibt immer x (außer denorm geleert).
-   x/1.0 f ergibt immer x (außer denorm geleert).
-   x +/-0,0 f ergibt immer x (außer denorm geleert). Aber-0 + 0 = + 0.
-   Beim Durchlaufen von Vorgängen (z. b. Mad, DP3) werden Ergebnisse erzeugt, die nicht weniger genau sind als die schlechtesten mögliche serielle Reihenfolge der Auswertung der nicht geschmolzenen Erweiterung des Vorgangs. Beachten Sie, dass die Definition der ungünstigsten Reihenfolge für die Toleranz keine festgelegte Definition für einen bestimmten Fused-Vorgang ist. Dies hängt von den jeweiligen Werten der Eingaben ab. Die einzelnen Schritte in der nicht zugezierten Erweiterung sind jeweils als 1 ULP-Toleranz zulässig (oder für alle Anweisungen Direct3D 10 Aufrufe mit einer weniger Lax-Toleranz als 1 ULP, desto weniger Lax-Toleranz ist zulässig).
-   Bei der durchgeführten Ausführung werden die gleichen Nan-Regeln wie nicht-Fused-Vorgänge befolgt.
-   Multiplizieren und Dividieren jedes Betriebs auf der 32-Bit-Gleit Komma Genauigkeit (Genauigkeit zu 1 ULP).

## <a name="16-bit-floating-point-rules"></a>Regeln für 16-Bit-Floating-Point

Direct3D 10 unterstützt auch 16-Bit-Darstellungen von Gleit Komma Zahlen.

Format:

-   1 Signier Bit (e) an der MSB-Bitposition
-   5 Bits von unparteiischen Exponent (e)
-   10 Bits des Bruchteils (f) mit einem zusätzlichen ausgeblendeten Bit

Ein float16-Wert (v) folgt den folgenden Regeln:

-   Wenn e = = 31 und f! = 0 ist, dann ist v unabhängig von s
-   Wenn e = = 31 und f = = 0, dann v = (-1) s \* unendlich (Vorzeichen unendlich)
-   Wenn e zwischen 0 und 31 liegt, dann v = (-1) s \* 2 (e-15) \* (1. f)
-   Wenn e = = 0 und f! = 0, dann v = (-1) s \* 2 (e-14) \* (0. f) (Denormalisierte Zahlen)
-   Wenn e = = 0 und f = = 0, dann v = (-1) s \* 0 (signierte null)

32-Bit-Gleit Komma Regeln enthalten auch für 16-Bit-Gleit Komma Zahlen, die für das oben beschriebene bitlayout angepasst sind. Ausnahmen bilden die folgenden Fälle:

-   Genauigkeit: bei unfused-Vorgängen für 16-Bit-Gleit Komma Zahlen wird ein Ergebnis erzeugt, bei dem es sich um den nächstgelegenen darstellbaren Wert eines unendlich präzisen Ergebnisses handelt (abgerundet auf den nächstgelegenen Wert, auch pro IEEE-754, auf 16-Bit-Werte angewendet). 32-Bit-Gleit Komma Regeln entsprechen 1 ULP-Toleranz, 16-Bit-Gleit Komma Regeln entsprechen 0,5 ULP für unfused-Vorgänge und 0,6 ULP für Fused-Vorgänge.
-   16-Bit-Gleit Komma Zahlen behalten denorms bei.

## <a name="11-bit-and-10-bit-floating-point-rules"></a>11-Bit-und 10-Bit-Floating-Point Regeln

Direct3D 10 unterstützt auch 11-Bit-und 10-Bit-Gleit Komma Formate.

Format:

-   Kein Signier Bit
-   5 Bits von unparteiischen Exponent (e)
-   6 Bits des Bruchteils (f) für ein 11-Bit-Format, 5 Bits von Bruchteil (f) für ein 10-Bit-Format, mit einem zusätzlichen ausgeblendeten Bit in beiden Fällen.

Ein float11/float10-Wert (v) folgt den folgenden Regeln:

-   Wenn e = = 31 und f! = 0 ist, dann ist v Nan.
-   Wenn e = = 31 und f = = 0, dann v = + unendlich
-   Wenn e zwischen 0 und 31 liegt, dann v = 2 (e-15) \* (1. f)
-   Wenn e = = 0 und f! = 0, dann v = \* 2 (e-14) \* (0. f) (Denormalisierte Zahlen)
-   Wenn e = = 0 und f = = 0, dann v = 0 (null)

32-Bit-Gleit Komma Regeln enthalten auch für 11-Bit-und 10-Bit-Gleit Komma Zahlen, die für das oben beschriebene bitlayout angepasst werden. Zu den Ausnahmen zählen:

-   Genauigkeit: 32-Bit-Gleit Komma Regeln entsprechen 0,5 ULP.
-   10/11-Bit-Gleit Komma Zahlen behalten denorms bei.
-   Jeder Vorgang, der zu einer Zahl kleiner als 0 (null) führt, wird an NULL gebunden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



