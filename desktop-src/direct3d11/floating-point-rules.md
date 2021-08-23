---
title: Gleitkommaregeln (Direct3D 11)
description: Direct3D 11 unterstützt mehrere Gleitkommadarstellungen. Alle Gleitkommaberechnungen werden unter einer definierten Teilmenge der IEEE 754 32-Bit-Gleitkommaregeln mit einfacher Genauigkeit ausgeführt.
ms.assetid: 33F21BD0-FDF8-4D35-95C0-0A3920814CB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d802c3ebc682ced58ceddbe3db0091755d0b30bb79ffbfc9ddb454d5d4d383
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677110"
---
# <a name="floating-point-rules-direct3d-11"></a>Gleitkommaregeln (Direct3D 11)

Direct3D 11 unterstützt mehrere Gleitkommadarstellungen. Alle Gleitkommaberechnungen werden unter einer definierten Teilmenge der IEEE 754 32-Bit-Gleitkommaregeln mit einfacher Genauigkeit ausgeführt.

-   [32-Bit-Gleitkommaregeln](#32-bit-floating-point-rules)
    -   [Berücksichtigte IEEE-754-Regeln](#honored-ieee-754-rules)
    -   [Abweichungen oder zusätzliche Anforderungen von IEEE-754-Regeln](#deviations-or-additional-requirements-from-ieee-754-rules)
-   [64-Bit-Gleitkommaregeln (mit doppelter Genauigkeit)](#64-bit-double-precision-floating-point-rules)
-   [16-Bit-Gleitkommaregeln](#16-bit-floating-point-rules)
-   [11-Bit- und 10-Bit-Gleitkommaregeln](#11-bit-and-10-bit-floating-point-rules)
-   [Zugehörige Themen](#related-topics)

## <a name="32-bit-floating-point-rules"></a>32-Bit-Gleitkommaregeln

Es gibt zwei Sätze von Regeln: diejenigen, die IEEE-754 entsprechen, und diejenigen, die vom Standard abweichen.

### <a name="honored-ieee-754-rules"></a>Berücksichtigte IEEE-754-Regeln

Einige dieser Regeln sind eine einzelne Option, bei der IEEE-754 Optionen bietet.

-   Dividiert durch 0 erzeugt +/- INF, mit Ausnahme von 0/0, was zu NaN führt.
-   Das Protokoll von (+/-) 0 erzeugt -INF. Das Protokoll eines negativen Werts (mit Ausnahme von -0) erzeugt NaN.
-   Die reziproke Quadratwurzel (rsq) oder die Quadratwurzel (sqrt) einer negativen Zahl erzeugt NaN. Die Ausnahme ist -0. sqrt(-0) erzeugt -0, und rsq(-0) erzeugt -INF.
-   INF – INF = NaN
-   (+/-) INF/(+/-)INF = NaN
-   (+/-) INF \* 0 = NaN
-   NaN (any OP) any-value = NaN
-   Die Vergleiche EQ, GT, GE, LT und LE, wenn entweder oder beide Operanden NaN sind, geben **FALSE** zurück.
-   Vergleiche ignorieren das Vorzeichen 0 (also entspricht +0 -0).
-   Die Vergleichs-NE, wenn entweder oder beide Operanden NaN ist, gibt **TRUE** zurück.
-   Vergleiche eines beliebigen Nicht-NaN-Werts mit +/- INF geben das richtige Ergebnis zurück.

### <a name="deviations-or-additional-requirements-from-ieee-754-rules"></a>Abweichungen oder zusätzliche Anforderungen von IEEE-754-Regeln

-   IEEE-754 erfordert Gleitkommaoperationen, um ein Ergebnis zu erzeugen, das dem unendlich präzisen Ergebnis, das als "round-to-nearest-even" bezeichnet wird, der nächstgelegene darstellbare Wert ist. Direct3D 11 definiert die gleiche Anforderung: 32-Bit-Gleitkommavorgänge erzeugen ein Ergebnis, das sich innerhalb von 0,5 Einheiten an letzter Stelle (Unit-Last-Place, ULP) des unendlich präzisen Ergebnisses befindet. Dies bedeutet beispielsweise, dass die Hardware Ergebnisse auf 32-Bit abschneiden darf, anstatt eine Rundung auf die nächste Gerade durchzuführen, da dies zu einem Fehler von höchstens 0,5 ULP führen würde. Diese Regel gilt nur für Addition, Subtraktion und Multiplikation.
-   Gleitkommaausnahmen, Statusbits oder Traps werden nicht unterstützt.
-   Denormen werden bei der Eingabe und Ausgabe beliebiger mathematischer Gleitkommaoperationen zur vorzeichenbehaltenen Null geleert. Ausnahmen werden für E/A- oder Datenbewegungs-Vorgänge vorgenommen, die die Daten nicht bearbeiten.
-   Zustände, die Gleitkommawerte enthalten, z. B. Viewport MinDepth/MaxDepth, BorderColor-Werte, können als denormale Werte bereitgestellt werden und können geleert werden, bevor sie von der Hardware verwendet werden.
-   Min oder max operations flush denorms for comparison, but the result may or not be denorm flushed.
-   Die NaN-Eingabe für einen Vorgang erzeugt immer NaN bei der Ausgabe. Das genaue Bitmuster des NaN ist jedoch nicht erforderlich, um gleich zu bleiben (es sei denn, der Vorgang ist eine unformatierte Verschiebungsanweisung, die keine Daten ändert).
-   Min- oder max-Vorgänge, für die nur ein Operand NaN ist, geben den anderen Operanden als Ergebnis zurück (im Gegensatz zu vergleichsregeln, die wir weiter oben betrachtet haben). Dies ist eine IEEE 754R-Regel.

    Die IEEE-754R-Spezifikation für Gleitkomma-Vorgänge vom Wert min und max gibt an, dass das Ergebnis des Vorgangs der andere Parameter ist, wenn eine der Eingaben für min oder max ein stiller QNaN-Wert ist. Beispiel:

    ```C++
    min(x,QNaN) == min(QNaN,x) == x (same for max)
    ```

    

    Eine Revision der IEEE-754R-Spezifikation hat ein anderes Verhalten für min und max übernommen, wenn eine Eingabe ein "signalierender" SNaN-Wert im Vergleich zu einem QNaN-Wert ist:

    ```C++
    min(x,SNaN) == min(SNaN,x) == QNaN (same for max)
     
    ```

    

    Im Allgemeinen folgt Direct3D den Standards für arithmetische Daten: IEEE-754 und IEEE-754R. In diesem Fall gibt es jedoch eine Abweichung.

    Die arithmetischen Regeln in Direct3D 10 und höher unterscheiden nicht zwischen stillen und signalisierenden NaN-Werten (QNaN im Vergleich zu SNaN). Alle NaN-Werte werden auf die gleiche Weise behandelt. Im Fall von min und max entspricht das Direct3D-Verhalten für jeden NaN-Wert der Behandlung von QNaN in der IEEE-754R-Definition. (Zur Vollständigkeit: Wenn beide Eingaben NaN sind, wird ein beliebiger NaN-Wert zurückgegeben.)

-   Eine weitere IEEE 754R-Regel ist, dass min(-0,+0) == min(+0,-0) == -0 und max(-0,+0) == max(+0,-0) == +0 das Vorzeichen berücksichtigt, im Gegensatz zu den Vergleichsregeln für null (wie zuvor gesehen). Direct3D empfiehlt hier das IEEE 754R-Verhalten, erzwingt es jedoch nicht. es ist zulässig, dass das Ergebnis des Vergleichs von Nullen von der Reihenfolge der Parameter abhängig ist, indem ein Vergleich verwendet wird, der die Vorzeichen ignoriert.
-   x \* 1.0f führt immer zu x (außer denorm flushed).
-   x/1.0f führt immer zu x (außer denorm flushed).
-   x +/- 0.0f führt immer zu x (außer denorm flushed). Aber -0 + 0 = +0.
-   Fused-Vorgänge (z.B. mad, dp3) erzeugen Ergebnisse, die nicht weniger genau sind als die schlechteste mögliche serielle Reihenfolge der Auswertung der nicht verborgenen Erweiterung des Vorgangs. Die Definition der schlechtesten möglichen Reihenfolge zum Zweck der Toleranz ist keine feste Definition für einen bestimmten Fused-Vorgang. sie hängt von den jeweiligen Werten der Eingaben ab. Die einzelnen Schritte in der nicht verborgenen Erweiterung sind jeweils 1 ULP-Toleranz zulässig (oder für anweisungen, die Direct3D mit einer laxeren Toleranz als 1 ULP aufruft, desto mehr Laxtoleranz ist zulässig).
-   Fused-Vorgänge entsprechen den gleichen NaN-Regeln wie nicht fused-Vorgänge.
-   sqrt und rcp weisen eine ULP-Toleranz auf. Die Shaderanweisungen [**rcp**](/previous-versions/windows/desktop/legacy/hh447205(v=vs.85)) und [**rsq**](/windows/desktop/direct3dhlsl/rsq--sm4---asm-)weisen eine eigene gelockerte Genauigkeitsanforderung auf.
-   Multiplizieren und dividieren Sie jeden Betrieb auf der 32-Bit-Gleitkommagenauigkeitsebene (Genauigkeit auf 0,5 ULP für Multiplikation, 1,0 ULP für Kehrwert). Wenn x/y direkt implementiert wird, müssen die Ergebnisse größer oder gleich der Genauigkeit einer zweistufigen Methode sein.

## <a name="64-bit-double-precision-floating-point-rules"></a>64-Bit-Gleitkommaregeln (mit doppelter Genauigkeit)

Hardware- und Anzeigetreiber unterstützen optional Gleitkomma mit doppelter Genauigkeit. Wenn Sie [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) mit [**D3D11 \_ FEATURE \_ DOUBLES**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)aufrufen, legt der Treiber **DoublePrecisionFloatShaderOps** von [**D3D11 \_ FEATURE DATA \_ \_ DOUBLES**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles) auf TRUE fest, um die Unterstützung anzugeben. Treiber und Hardware müssen dann alle Gleitkommaanweisungen mit doppelter Genauigkeit unterstützen.

Anweisungen mit doppelter Genauigkeit folgen den Ieee 754R-Verhaltensanforderungen.

Unterstützung für die Generierung denormalisierter Werte ist für Daten mit doppelter Genauigkeit erforderlich (kein Leerungs-zu-Null-Verhalten). Ebenso lesen Anweisungen denormalisierte Daten nicht als Null mit Vorzeichen, sie beachten den Denormwert.

## <a name="16-bit-floating-point-rules"></a>16-Bit-Gleitkommaregeln

Direct3D 11 unterstützt auch 16-Bit-Darstellungen von Gleitkommazahlen.

Format:

-   1 Vorzeichenbit (s) an der MSB-Bitposition
-   5 Bits eines voreingenommenen Exponenten (e)
-   10 Bits fraction (f) mit einem zusätzlichen ausgeblendeten Bit

Ein float16-Wert (v) folgt diesen Regeln:

-   wenn e == 31 und f != 0, dann ist v naN, unabhängig von s
-   , wenn e == 31 und f == 0, dann v = (-1)s \* unendlich (unendlich mit Vorzeichen)
-   wenn e zwischen 0 und 31 liegt, dann v = (-1)s \* 2(e-15) \* (1.f)
-   , wenn e == 0 und f != 0, dann v = (-1)s \* 2(e-14) \* (0.f) (denormalisierte Zahlen)
-   , wenn e == 0 und f == 0, dann v = (-1)s \* 0 (null mit Vorzeichen)

32-Bit-Gleitkommaregeln enthalten auch 16-Bit-Gleitkommazahlen, angepasst an das zuvor beschriebene Bitlayout. Ausnahmen bilden die folgenden Fälle:

-   Genauigkeit: Nicht verborgene Vorgänge für 16-Bit-Gleitkommazahlen erzeugen ein Ergebnis, das dem unendlich präzisen Ergebnis den nächsten darstellbaren Wert darstellt (gerundet auf die nächste Gerade, gemäß IEEE-754, angewendet auf 16-Bit-Werte). 32-Bit-Gleitkommaregeln entsprechen 1 ULP-Toleranz, 16-Bit-Gleitkommaregeln 0,5 ULP für nicht verborgene Vorgänge und 0,6 ULP für fused-Vorgänge.
-   16-Bit-Gleitkommazahlen behalten Denormen bei.

## <a name="11-bit-and-10-bit-floating-point-rules"></a>11-Bit- und 10-Bit-Gleitkommaregeln

Direct3D 11 unterstützt auch 11-Bit- und 10-Bit-Gleitkommaformate.

Format:

-   Kein Vorzeichenbit
-   5 Bits eines voreingenommenen Exponenten (e)
-   6 Bits fraction (f) für ein 11-Bit-Format, 5 Bits fraction (f) für ein 10-Bit-Format mit einem zusätzlichen ausgeblendeten Bit in beiden Fällen.

Ein float11/float10-Wert (v) folgt den folgenden Regeln:

-   wenn e == 31 und f != 0, dann ist v NaN
-   , wenn e == 31 und f == 0, dann v = +infinity
-   wenn e zwischen 0 und 31 liegt, dann v = 2(e-15) \* (1.f)
-   wenn e == 0 und f != 0, dann v = \* 2(e-14) \* (0.f) (denormalisierte Zahlen)
-   wenn e == 0 und f == 0, dann v = 0 (null)

32-Bit-Gleitkommaregeln gelten auch für 11-Bit- und 10-Bit-Gleitkommazahlen, angepasst an das zuvor beschriebene Bitlayout. Zu den Ausnahmen zählen:

-   Genauigkeit: 32-Bit-Gleitkommaregeln entsprechen 0,5 ULP.
-   10/11-Bit-Gleitkommazahlen behalten Denormale bei.
-   Jeder Vorgang, der zu einer Zahl kleiner als 0 (null) führen würde, wird an 0 (null) geklammert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen](overviews-direct3d-11-resources.md)
</dt> <dt>

[Texturen](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 