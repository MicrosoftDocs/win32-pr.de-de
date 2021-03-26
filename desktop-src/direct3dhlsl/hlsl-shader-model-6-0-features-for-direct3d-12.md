---
title: HLSL-Shader-Modell 6,0
description: Beschreibt die systeminternen Wellen Vorgangs Funktionen, die dem HLSL-Shader-Modell 6,0 hinzugefügt werden.
ms.assetid: BF968CD3-AC67-48DB-B93F-EF54B680106F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2d082fc131c7cd08db9eb1861c4af39d600f40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976705"
---
# <a name="hlsl-shader-model-60"></a>HLSL-Shader-Modell 6,0

Beschreibt die systeminternen Wellen Vorgangs Funktionen, die dem HLSL-Shader-Modell 6,0 hinzugefügt werden.

- [Shadermodell 6,0](#shader-model-60)
- [Terminologie](#terminology)
- [Intrinsische Funktionen für Schattierungs Sprache](#shading-language-intrinsics)
    - [Wave-Abfrage](#wave-query)
    - [Wave Vote](#wave-vote)
    - [Wave-Broadcast](#wave-broadcast)
    - [Wave-Reduzierung](#wave-reduction)
    - [Wellen Scan und Präfix](#wave-scan-and-prefix)
    - [Quad-weite shuffle-Vorgänge](#quad-wide-shuffle-operations)
- [Hardware Funktion](#hardware-capability)
- [Zugehörige Themen](#related-topics)

## <a name="shader-model-60"></a>Shadermodell 6,0

Bei früheren shadermodellen macht die HLSL-Programmierung nur einen einzigen Ausführungs Thread verfügbar. Neue Wellen ebenenvorgänge werden ab dem Modell 6,0 bereitgestellt, um die Parallelität der aktuellen GPUs explizit zu nutzen. viele Threads können gleichzeitig in einem Sperr Schritt desselben Kerns ausgeführt werden. Beispielsweise ermöglichen die systeminternen Modelle von Modell 6,0 die Beseitigung von sperrkonstrukten, wenn der Bereich der Synchronisierung innerhalb der Breite des SIMD-Prozessors liegt, oder eine andere Gruppe von Threads, die als atomarisch bezeichnet werden.

Mögliche Anwendungsfälle: Stream-Komprimierung,-Reduzierung, Block Umwandlung, bitonische Sortierung oder schnelle Fourier-Transformationen (FFT), Klassifizierungen, Deduplizierung von Datenströmen und ähnliche Szenarien.

Die meisten systeminternen Funktionen werden in Pixel-Shadern und Compute-Shadern angezeigt, es gibt jedoch einige Ausnahmen (für jede Funktion angegeben). Die Funktionen wurden den Anforderungen für die DirectX-Funktionsebene 12,0 unter API-Ebene 12 hinzugefügt.

Der *<type>* -Parameter und der Rückgabewert für diese Funktionen sind der Typ des Ausdrucks, die unterstützten Typen sind die in der folgenden Liste, die *auch* im Ziel-Shader-Modell für Ihre APP vorhanden sind:

- half, half2, half3, half4
- float, float2, float3, float4
- Double, Double2, double3, double4
- int, int2, int3, INT4
- uint, uint2, uint3, uint4
- Short, short2, short3, short4
- ushort, ushort2, ushort3, ushort4
- UInt64 \_ t, UInt64 \_ T2, UInt64 \_ T3, UInt64 \_ T4

Einige Vorgänge (z. b. die bitweisen Operatoren) unterstützen nur die ganzzahligen Typen.

## <a name="terminology"></a>Terminologie

| | |
|-|-|
| **Begriff** | **Definition** |
| Bereich | Ein einzelner Ausführungs Thread. Die Shader-Modelle vor Version 6,0 machen nur eine dieser Versionen auf Sprachebene verfügbar, sodass die Erweiterung auf die parallele SIMD-Verarbeitung vollständig auf die Implementierung beschränkt wird. |
| Wave | Eine Reihe von Bereichen (Threads), die gleichzeitig im Prozessor ausgeführt werden. Es sind keine expliziten Barrieren erforderlich, um sicherzustellen, dass Sie parallel ausgeführt werden. Ähnliche Konzepte sind "Warp" und "Wavefront". |
| Inaktive Spur | Eine Spur, die nicht ausgeführt wird, z. b. aufgrund der Ablauf Steuerung oder unzureichende Arbeit, um die minimale Größe der Welle auszufüllen. |
| Aktive Strecke | Eine Spur, für die die Ausführung ausgeführt wird. In Pixel-Shadern kann es beliebige hilfspixelbereiche enthalten. |
| Quad | Ein Satz von vier angrenzenden Bereichen, die Pixel entsprechen, die in einem 2 x 2-Quadrat angeordnet sind. Sie werden verwendet, um Farbverläufe durch Differenzierung in x oder y zu schätzen. Eine Welle kann aus mehreren Quads bestehen. Alle Pixel in einem aktiven Quad werden ausgeführt (und sind möglicherweise "aktive Bereiche"), aber diejenigen, die keine sichtbaren Ergebnisse liefern, werden als "hilfsbereiche" bezeichnet. |
| Hilfsbereich | Eine Spur, die ausschließlich für Farbverläufe in Pixel-Shader-Quads ausgeführt wird. Die Ausgabe einer solchen Spur wird verworfen und wird daher nicht auf der Ziel Oberfläche Rendering. |

## <a name="shading-language-intrinsics"></a>Intrinsische Funktionen für Schattierungs Sprache

Alle Vorgänge dieses Shader-Modells wurden in einem Bereich intrinsischer Funktionen hinzugefügt.

### <a name="wave-query"></a>Wave-Abfrage

Die intrinsie zum Abfragen einer einzelnen Welle.

| | | | |
|-|-|-|-|
| **Intrinsic** | **Beschreibung** | **Pixel-Shader** | **Compute-Shader** |
| [**Wavegetlanecount**](wavegetlanecount.md) | Gibt die Anzahl der Bereiche in der aktuellen Welle zurück. | \* | \* |
| [**Wavegetlaneingedex**](wavegetlaneindex.md) | Gibt den Index der aktuellen Lane innerhalb der aktuellen Wave zurück. | \* | \* |
| [**Waveisfirstlane**](waveisfirstlane.md) | Gibt "true" nur für die aktive Spur in der aktuellen Wave mit dem kleinsten Index zurück. | \* | \* |

### <a name="wave-vote"></a>Wave Vote

Diese Gruppe von systeminternen Funktionen vergleicht Werte über Threads, die derzeit von der aktuellen Welle aus aktiv sind.

| | | | |
|-|-|-|-|
| **Intrinsic** | **Beschreibung** | **Pixel-Shader** | **Compute-Shader** |
| [**Waveactiveanytrue**](waveanytrue.md) | Gibt "true" zurück, wenn der Ausdruck in einer beliebigen aktiven Strecke in der aktuellen Wave "true" ist. | \* | \* |
| [**Waveactivealltrue**](wavealltrue.md) | Gibt "true" zurück, wenn der Ausdruck in allen aktiven Bereichen in der aktuellen Wave "true" ist. | \* | \* |
| [**Waveactiveballot**](waveballot.md) | Gibt eine ganzzahlige Bitmaske für eine 64-Bit-Ganzzahl ohne Vorzeichen der Auswertung des booleschen Ausdrucks für alle aktiven Bereiche in der angegebenen Wave zurück. | \* | \* |

### <a name="wave-broadcast"></a>Wave-Broadcast

Diese systeminternen Funktionen ermöglichen allen aktiven Bereichen in der aktuellen Wave, den Wert von der angegebenen Strecke zu empfangen und effektiv zu senden. Der Rückgabewert einer ungültigen Spur ist nicht definiert.

| | | | |
|-|-|-|-|
| **Intrinsic** | **Beschreibung** | **Pixel-Shader** | **Compute-Shader** |
| [**Wavereadlaneat**](wavereadlaneat.md) | Gibt den Wert des Ausdrucks für den angegebenen Lane-Index innerhalb der angegebenen Wave zurück. | \* | \* |
| [**Wavereadlanefirst**](wavereadfirstlane.md) | Gibt den Wert des Ausdrucks für die aktive Spur der aktuellen Welle mit dem kleinsten Index zurück. | \* | \* |

### <a name="wave-reduction"></a>Wave-Reduzierung

Diese systeminternen Funktionen berechnen den angegebenen Vorgang für alle aktiven Bereiche in der Wave und übertragen das Endergebnis an alle aktiven Bereiche. Daher ist die endgültige Ausgabe in der gesamten Wave garantiert.

| | | | |
|-|-|-|-|
| **Intrinsic** | **Beschreibung** | **Pixel-Shader** | **Compute-Shader** |
| [**Waveactiveallequal**](waveactiveallequal.md) | Gibt true zurück, wenn der Ausdruck für jede aktive Strecke in der aktuellen Wave identisch ist (und somit einheitlich ist). | \* | \* |
| [**Waveactivebitand**](waveallbitand.md) | Gibt das bitweise and aller Werte des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zurück und repliziert das Ergebnis in alle Bereiche in der Wave. | \* | \* |
| [**Waveactivebitor**](waveallbitor.md) | Gibt das bitweise OR aller Werte des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zurück und repliziert das Ergebnis in alle Bereiche in der Wave. | \* | \* |
| [**Waveactivebitxor**](waveallbitxor.md) | Gibt das bitweise exklusive OR aller Werte des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zurück und repliziert das Ergebnis in alle Bereiche in der Wave. | \* | \* |
| [**Waveactivezählbits**](waveactivecountbits.md) | Zählt die Anzahl von booleschen Variablen, die für alle aktiven Bereiche in der aktuellen Wave als true ausgewertet werden, und repliziert das Ergebnis in alle Bereiche in der Wave. | \* | \* |
| [**Waveactivemax**](waveallmax.md) | Berechnet den maximalen Wert des Ausdrucks für alle aktiven Bereiche in der aktuellen Welle und repliziert das Ergebnis in alle Bereiche in der Wave. | \* | \* |
| [**Waveactivemin**](waveallmin.md) | Berechnet den minimalen Wert des Ausdrucks für alle aktiven Bereiche in der aktuellen Welle und repliziert das Ergebnis in alle Bereiche in der Wave. | \* | \* |
| [**Waveactiveproduct**](waveallproduct.md) | Multipliziert die Werte des Ausdrucks über alle aktiven Bereiche in der aktuellen Welle und repliziert das Ergebnis in alle Bereiche in der Wave. | \* | \* |
| [**Waveactivesum**](waveallsum.md) | Fasst den Wert des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zusammen und repliziert Sie auf alle Bereiche in der aktuellen Welle und repliziert das Ergebnis in alle Bereiche in der Wave. | \* | \* |

### <a name="wave-scan-and-prefix"></a>Wellen Scan und Präfix

Diese systeminternen Funktionen wenden den-Vorgang auf jede Spur an und lassen jedes Teilergebnis der Berechnung in der entsprechenden-Spalte.

| | | | |
|-|-|-|-|
| **Intrinsic** | **Beschreibung** | **Pixel-Shader** | **Compute-Shader** |
| [**Waveprefixzählbits**](waveprefixcountbytes.md) | Gibt die Summe aller angegebenen booleschen Variablen für alle aktiven Bereiche mit Indizes zurück, die kleiner als die aktuelle Seite sind. | \* | \* |
| [**Waveprefixsum**](waveprefixsum.md) | Gibt die Summe aller Werte in den aktiven Bereichen mit kleineren Indizes als dieser zurück. | \* | \* |
| [**Waveprefixproduct**](waveprefixproduct.md) | Gibt das Produkt aller Werte in den Bereichen vor diesem einer der angegebenen Wave zurück. | \* | \* |

### <a name="quad-wide-shuffle-operations"></a>Quad-weite shuffle-Vorgänge

Diese systeminternen Funktionen führen Austausch Vorgänge für die Werte in einer Wave aus, die bekanntermaßen Pixel-Shader-Quads enthalten, wie hier definiert. Die Indizes der Pixel im Quad werden in der Scan-oder Lesefolge definiert, wobei die Koordinaten innerhalb eines viervieres sind:

+---------> X 

| [0] [1] 

| [2] [3] 

v 

J 


Diese Routinen funktionieren entweder in Compute-Shader oder Pixel-Shadern. In Compute-Shadern arbeiten Sie mit Quads, die als gleichmäßig verteilte Gruppen von 4 innerhalb einer SIMD-Welle definiert sind. In Pixel-Shadern sollten Sie für von wavequadlanes erfasste Wellen verwendet werden. andernfalls sind die Ergebnisse nicht definiert.

| | | | |
|-|-|-|-|
| **Intrinsic** | **Beschreibung** | **Pixel-Shader** | **Compute-Shader** |
| [**Quadumeat**](quadreadlaneat.md) | Gibt den angegebenen Quellwert zurück, der aus dem Bereich des aktuellen Quad gelesen wird, das durch quadlaneid \[ 0.. 3 identifiziert \] wird, das über das Vierfache einheitlich sein muss. | \* | |
| [**Quad-acrossdiagonal**](quadreadacrossdiagonal.md) | Gibt den angegebenen lokalen Wert zurück, der aus der Diagonal umgekehrten Spur in diesem Quad gelesen wird. | \* | |
| [**Quad-acrossx**](quadswapx.md) | Gibt den angegebenen Quellwert zurück, der von der anderen Strecke in diesem Quad in der X-Richtung gelesen wird. | \* | |
| [**Quad-acrossy**](quadswapy.md) | Gibt den angegebenen Quellwert zurück, der von der anderen Strecke in diesem Quad in der Y-Richtung gelesen wird. | \* | |

## <a name="hardware-capability"></a>Hardware Funktion

Um zu überprüfen, ob die Wellen Vorgangs Features auf einer bestimmten Hardware verfügbar sind, wenden Sie [**ID3D12Device:: checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)an, und notieren Sie sich die Beschreibung und die Verwendung der [**D3D12 \_ Feature \_ Data \_ D3D12 \_ OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1) -Struktur.

## <a name="related-topics"></a>Zugehörige Themen

* [Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
* [Systeminterne Funktionen von Shader Model 6](shader-model-6-0.md)