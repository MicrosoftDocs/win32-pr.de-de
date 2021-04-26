---
title: HLSL-Shadermodell 6.0
description: Beschreibt die systeminternen Wellenvorgangsfunktionen, die dem HLSL-Shadermodell 6.0 hinzugefügt wurden.
ms.assetid: BF968CD3-AC67-48DB-B93F-EF54B680106F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7e55661e3f91125597c8c7842a1be16129cefe0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995467"
---
# <a name="hlsl-shader-model-60"></a>HLSL-Shadermodell 6.0

Beschreibt die systeminternen Wellenvorgangsfunktionen, die dem HLSL-Shadermodell 6.0 hinzugefügt wurden.

- [Shadermodell 6.0](#shader-model-60)
- [Terminologie](#terminology)
- [Intrinsische Schattierungssprache](#shading-language-intrinsics)
    - [Wave-Abfrage](#wave-query)
    - [Wave Vote](#wave-vote)
    - [Wave Broadcast](#wave-broadcast)
    - [Wellenreduzierung](#wave-reduction)
    - [Wellenscan und Präfix](#wave-scan-and-prefix)
    - [Quad-wide Shuffle-Vorgänge](#quad-wide-shuffle-operations)
- [Hardwarefunktion](#hardware-capability)
- [Zugehörige Themen](#related-topics)

## <a name="shader-model-60"></a>Shadermodell 6.0

Bei früheren Shadermodellen macht die HLSL-Programmierung nur einen einzigen Ausführungsthread verfügbar. Ab Modell 6.0 werden neue Vorgänge auf Wellenebene bereitgestellt, um die Parallelität der aktuellen GPUs explizit zu nutzen. Viele Threads können gleichzeitig in Lockstep auf demselben Kern ausgeführt werden. Beispielsweise ermöglichen die systeminternen Funktionen des Modells 6.0 die Beseitigung von Barrierekonstrukten, wenn der Synchronisierungsbereich innerhalb der Breite des SIMD-Prozessors oder einiger anderer Threads liegt, die bekanntermaßen atomar relativ zueinander sind.

Mögliche Anwendungsfälle sind: Stream-Komprimierung, Reduzierungen, Blocktransponierung, bitonische Sortierung oder schnelle Fouriertransformationen (FFT), Binning, Datenstromdeduplizierung und ähnliche Szenarien.

Die meisten systeminternen Funktionen werden in Pixel-Shadern und Compute-Shadern angezeigt, es gibt jedoch einige Ausnahmen (für jede Funktion notiert). Die Funktionen wurden den Anforderungen für DirectX-Featureebene 12.0 unter API-Ebene 12 hinzugefügt.

Der -Parameter und der Rückgabewert für diese Funktionen impliziert den Typ des Ausdrucks. Die unterstützten Typen sind die typen aus der folgenden Liste, die auch im Ziel-Shadermodell für Ihre App *<type>* vorhanden sind: 

- half, half2, half3, half4
- float, float2, float3, float4
- double, double2, double3, double4
- int, int2, int3, int4
- uint, uint2, uint3, uint4
- short, short2, short3, short4
- ushort, ushort2, ushort3, ushort4
- uint64 \_ t, uint64 \_ t2, uint64 \_ t3, uint64 \_ t4

Einige Vorgänge (z. B. bitweise Operatoren) unterstützen nur die ganzzahligen Typen.

## <a name="terminology"></a>Terminologie

| **Begriff** | **Definition** |
|-|-|
| Bereich | Ein einzelner Ausführungsthread. Die Shadermodelle vor Version 6.0 machen nur eines dieser Modelle auf Sprachebene verfügbar, was die Erweiterung zur parallelen SIMD-Verarbeitung vollständig bis zur Implementierung überlässt. |
| Wave | Ein Satz von Lanes (Threads), die gleichzeitig im Prozessor ausgeführt werden. Es sind keine expliziten Barrieren erforderlich, um zu gewährleisten, dass sie parallel ausgeführt werden. Ähnliche Konzepte sind "warp" und "wavefront". |
| Inaktive Lane | Eine Spur, die nicht ausgeführt wird, z. B. aufgrund des Flusses der Steuerung oder unzureichender Arbeit, um die Mindestgröße der Welle zu füllen. |
| Active Lane | Eine Spur, für die die Ausführung ausgeführt wird. In Pixel-Shadern kann es alle Hilfspixelspuren enthalten. |
| Viereck | Eine Gruppe von vier angrenzenden Lanes, die Pixeln entsprechen, die in einem 2x2-Quadrat angeordnet sind. Sie werden verwendet, um Farbverläufe zu schätzen, indem sie sich in x oder y unterscheiden. Eine Welle kann aus mehreren Quadern bestehen. Alle Pixel in einem aktiven Quader werden ausgeführt (und können "Aktive Lanes" sein), aber diejenigen, die keine sichtbaren Ergebnisse erzeugen, werden als "Hilfsspuren" bezeichnet. |
| Helper Lane | Eine Lane, die ausschließlich für Farbverläufe in Pixel-Shader-Quadern ausgeführt wird. Die Ausgabe einer solchen Spur wird verworfen und daher nicht auf der Zieloberfläche gerendert. |

## <a name="shading-language-intrinsics"></a>Intrinsische Schattierungssprache

Alle Vorgänge dieses Shadermodells wurden in einer Reihe von systeminternen Funktionen hinzugefügt.

### <a name="wave-query"></a>Wave-Abfrage

Die systeminternen Funktionen zum Abfragen einer einzelnen Welle.

| **Intrinsic** | **Beschreibung** | **Pixel-Shader** | **Compute-Shader** |
|-|-|-|-|
| [**WaveGetLaneCount**](wavegetlanecount.md) | Gibt die Anzahl der Lanes in der aktuellen Welle zurück. | \* | \* |
| [**WaveGetLaneIndex**](wavegetlaneindex.md) | Gibt den Index der aktuellen Lane innerhalb der aktuellen Welle zurück. | \* | \* |
| [**WaveIsFirstLane**](waveisfirstlane.md) | Gibt nur true für die aktive Lane in der aktuellen Welle mit dem kleinsten Index zurück. | \* | \* |

### <a name="wave-vote"></a>Wave Vote

Diese Gruppe von systeminternen Eigenschaften vergleicht Werte über Threads hinweg, die derzeit von der aktuellen Welle aus aktiv sind.

| **Intrinsic** | **Beschreibung** | **Pixel-Shader** | **Compute-Shader** |
|-|-|-|-|
| [**WaveActiveAnyTrue**](waveanytrue.md) | Gibt TRUE zurück, wenn der Ausdruck in einer beliebigen aktiven Lane in der aktuellen Welle true ist. | \* | \* |
| [**WaveActiveAllTrue**](wavealltrue.md) | Gibt TRUE zurück, wenn der Ausdruck in allen aktiven Lanes in der aktuellen Welle true ist. | \* | \* |
| [**WaveActiveBallot**](waveballot.md) | Gibt eine 64-Bit-Ganzzahlbitmaske ohne Vorzeichen der Auswertung des booleschen Ausdrucks für alle aktiven Lanes in der angegebenen Welle zurück. | \* | \* |

### <a name="wave-broadcast"></a>Wave Broadcast

Diese systeminternen Eigenschaften ermöglichen es allen aktiven Lanes in der aktuellen Welle, den Wert von der angegebenen Spur zu empfangen und effektiv zu übertragen. Der Rückgabewert einer ungültigen Lane ist nicht definiert.

| **Intrinsic** | **Beschreibung** | **Pixel-Shader** | **Compute-Shader** |
|-|-|-|-|
| [**WaveReadLaneAt**](wavereadlaneat.md) | Gibt den Wert des Ausdrucks für den angegebenen Lane-Index innerhalb der angegebenen Welle zurück. | \* | \* |
| [**WaveReadLaneFirst**](wavereadfirstlane.md) | Gibt den Wert des Ausdrucks für die aktive Spur der aktuellen Welle mit dem kleinsten Index zurück. | \* | \* |

### <a name="wave-reduction"></a>Wellenverringerung

Diese systeminternen Eigenschaften berechnen den angegebenen Vorgang auf allen aktiven Spuren in der Welle und übertragen das Endergebnis an alle aktiven Lanes. Daher ist die endgültige Ausgabe garantiert einheitlich über die gesamte Welle hinweg.

| **Intrinsic** | **Beschreibung** | **Pixel-Shader** | **Compute-Shader** |
|-|-|-|-|
| [**WaveActiveAllEqual**](waveactiveallequal.md) | Gibt TRUE zurück, wenn der Ausdruck für jede aktive Kurve in der aktuellen Welle gleich ist (und somit einheitlich ist). | \* | \* |
| [**WaveActiveBitAnd**](waveallbitand.md) | Gibt den bitweisen AND-Wert aller Werte des Ausdrucks über alle aktiven Lanes in der aktuellen Welle zurück und repliziert das Ergebnis auf alle Lanes in der Welle. | \* | \* |
| [**WaveActiveBitOr**](waveallbitor.md) | Gibt das bitweise OR aller Werte des Ausdrucks über alle aktiven Lanes in der aktuellen Welle zurück und repliziert das Ergebnis auf alle Lanes in der Welle. | \* | \* |
| [**WaveActiveBitXor**](waveallbitxor.md) | Gibt das bitweise exklusive OR aller Werte des Ausdrucks über alle aktiven Lanes in der aktuellen Welle zurück und repliziert das Ergebnis auf alle Lanes in der Welle. | \* | \* |
| [**WaveActiveCountBits**](waveactivecountbits.md) | Zählt die Anzahl der booleschen Variablen, die für alle aktiven Lanes in der aktuellen Welle als TRUE ausgewertet werden, und repliziert das Ergebnis auf alle Lanes in der Welle. | \* | \* |
| [**WaveActiveMax**](waveallmax.md) | Berechnet den maximalen Wert des Ausdrucks für alle aktiven Lanes in der aktuellen Welle und repliziert das Ergebnis auf alle Lanes in der Welle. | \* | \* |
| [**WaveActiveMin**](waveallmin.md) | Berechnet den Minimalwert des Ausdrucks für alle aktiven Lanes in der aktuellen Welle und repliziert das Ergebnis auf alle Lanes in der Welle. | \* | \* |
| [**WaveActiveProduct**](waveallproduct.md) | Multipliziert die Werte des Ausdrucks auf allen aktiven Lanes in der aktuellen Welle und repliziert das Ergebnis auf alle Lanes in der Welle. | \* | \* |
| [**WaveActiveSum**](waveallsum.md) | Summiert den Wert des Ausdrucks für alle aktiven Lanes in der aktuellen Welle und repliziert ihn auf alle Lanes in der aktuellen Welle und repliziert das Ergebnis auf alle Lanes in der Welle. | \* | \* |

### <a name="wave-scan-and-prefix"></a>Wellenscan und Präfix

Diese systeminternen Funktionen wenden den Vorgang auf jede Spur an und belassen jedes Teilergebnis der Berechnung in der entsprechenden Lane.

| **Intrinsic** | **Beschreibung** | **Pixel-Shader** | **Compute-Shader** |
|-|-|-|-|
| [**WavePrefixCountBits**](waveprefixcountbytes.md) | Gibt die Summe aller angegebenen booleschen Variablen zurück, die für alle aktiven Lanes mit Indizes, die kleiner als die aktuelle Spur sind, auf TRUE festgelegt sind. | \* | \* |
| [**WavePrefixSum**](waveprefixsum.md) | Gibt die Summe aller Werte in den aktiven Lanes mit kleineren Indizes als dieser zurück. | \* | \* |
| [**WavePrefixProduct**](waveprefixproduct.md) | Gibt das Produkt aller Werte in den Lanes vor dieser angegebenen Welle zurück. | \* | \* |

### <a name="quad-wide-shuffle-operations"></a>Vierfache Shufflevorgänge

Diese systeminternen Funktionen führen Austauschvorgänge für die Werte über eine Welle aus, die bekannte Pixel-Shader-Quads enthält, wie hier definiert. Die Indizes der Pixel im Quader werden in der Scanzeilen- oder Lese reihenfolge definiert, wobei die Koordinaten innerhalb eines Quad-Quadrats wie die folgenden sind:

+---------> X 

| [0] [1] 

| [2] [3] 

v 

J 


Diese Routinen funktionieren entweder in Compute-Shadern oder Pixel-Shadern. In Compute-Shadern werden sie in Quads betrieben, die als gleichmäßig geteilte Gruppen von 4 innerhalb einer SIMD-Welle definiert sind. In Pixel-Shadern sollten sie auf Wellen verwendet werden, die von WaveQuadLanes erfasst wurden. Andernfalls sind die Ergebnisse nicht definiert.

| **Intrinsic** | **Beschreibung** | **Pixel-Shader** | **Compute-Shader** |
|-|-|-|-|
| [**QuadReadLaneAt**](quadreadlaneat.md) | Gibt den angegebenen Quellwert zurück, der von der Spur des aktuellen Quads gelesen wird, das durch quadLaneID 0..3 identifiziert wird und auf dem Quad einheitlich \[ \] sein muss. | \* | |
| [**QuadReadAcrossDi wie**](quadreadacrossdiagonal.md) | Gibt den angegebenen lokalen Wert zurück, der von der diagonal gegenüberliegenden Kurve in diesem Quader gelesen wird. | \* | |
| [**QuadReadAcrossX**](quadswapx.md) | Gibt den angegebenen Quellwert zurück, der von der anderen Fahrspur in diesem Quader in X-Richtung gelesen wurde. | \* | |
| [**QuadReadAcrossY**](quadswapy.md) | Gibt den angegebenen Quellwert zurück, der von der anderen Fahrspur in diesem Quader in Y-Richtung gelesen wurde. | \* | |

## <a name="hardware-capability"></a>Hardwarefunktion

Rufen Sie [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)auf, um zu überprüfen, ob die Wavevorgangsfunktionen auf einer bestimmten Hardware verfügbar sind. Notieren Sie dabei die Beschreibung und Verwendung der [**D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS1-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1)

## <a name="related-topics"></a>Zugehörige Themen

* [Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
* [Intrinsische Funktionen des Shadermodells 6](shader-model-6-0.md)
