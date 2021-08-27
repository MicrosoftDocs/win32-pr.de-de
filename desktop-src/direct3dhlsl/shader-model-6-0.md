---
title: Shadermodell 6
description: Shadermodell 6.0 fügt einen Bereich von Systeminternen Wellenvorgang für die Pixel- und Compute-Shader hinzu.
ms.assetid: 2F28F86D-F599-47EA-90D7-6833ABA976FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609f0a9d36fbf7414e724cd31bc05a8e4d6abdefa5c842f30934feba0dffb868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790699"
---
# <a name="shader-model-6"></a>Shadermodell 6

Alle Nicht-Quad-bezogenen systeminternen Wave-Eigenschaften sind in allen Shaderstufen verfügbar. Systeminterne Quad wave-Eigenschaften sind nur in Pixel- und Compute-Shadern verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                 | BESCHREIBUNG                                                                                                                                                               |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QuadReadAcrossDicrossAl**](quadreadacrossdiagonal.md)<br/> | Gibt den angegebenen lokalen Wert zurück, der von der diagonal gegenüberliegenden Spur in diesem Quader gelesen wird.<br/>                                                                |
| [**QuadReadLaneAt**](quadreadlaneat.md)<br/>                   | Gibt den angegebenen Quellwert aus der Spur zurück, die durch die Lane-ID innerhalb des aktuellen Quads identifiziert wird.<br/>                                                            |
| [**QuadReadAcrossX**](quadswapx.md)<br/>                      | Gibt den angegebenen lokalen Wert zurück, der von der anderen Spur in diesem Quad in X-Richtung gelesen wird.<br/>                                                                    |
| [**QuadReadAcrossy**](quadswapy.md)<br/>                      | Gibt den angegebenen Quellwert zurück, der von der anderen Spur in diesem Quad in Y-Richtung gelesen wird.<br/>                                                                   |
| [**WaveActiveAllEqual**](waveactiveallequal.md)<br/>           | Gibt TRUE zurück, wenn der Ausdruck für jede aktive Spur in der aktuellen Welle identisch ist (und somit einheitlich darüber ist).<br/>                                             |
| [**WaveActiveBitAnd**](waveallbitand.md)<br/>                  | Gibt das bitweise AND aller Werte des Ausdrucks auf allen aktiven Spuren in der aktuellen Welle zurück und repliziert es zurück an alle aktiven Lanes. <br/>           |
| [**WaveActiveBitOr**](waveallbitor.md)<br/>                    | Gibt das bitweise OR aller Werte des Ausdrucks auf allen aktiven Spuren in der aktuellen Welle zurück und repliziert es zurück an alle aktiven Lanes. <br/>            |
| [**WaveActiveBitXor**](waveallbitxor.md)<br/>                  | Gibt den bitweise XOR aller Werte des Ausdrucks auf allen aktiven Spuren in der aktuellen Welle zurück und repliziert ihn zurück an alle aktiven Lanes. <br/>           |
| [**WaveActiveCountBits**](waveactivecountbits.md)<br/>         | Zählt die Anzahl der booleschen Variablen, die auf allen aktiven Spuren in der aktuellen Welle als true ausgewertet werden, und repliziert das Ergebnis auf alle Spuren in der Welle.<br/> |
| [**WaveActiveMax**](waveallmax.md)<br/>                        | Gibt den Maximalwert des Ausdrucks über alle aktiven Lanes in der aktuellen Welle hinweg zurück und repliziert ihn zurück an alle aktiven Lanes. <br/>                           |
| [**WaveActiveMin**](waveallmin.md)<br/>                        | Gibt den Minimalwert des Ausdrucks über alle aktiven Lanes in der aktuellen Welle zurück und repliziert ihn zurück an alle aktiven Lanes. <br/>                               |
| [**WaveActiveProduct**](waveallproduct.md)<br/>                | Multipliziert die Werte des Ausdrucks über alle aktiven Lanes in der aktuellen Welle und repliziert sie zurück an alle aktiven Lanes.<br/>                       |
| [**WaveActiveSum**](waveallsum.md)<br/>                        | Summiert den Wert des Ausdrucks über alle aktiven Lanes in der aktuellen Welle hinweg und repliziert ihn auf alle Spuren in der aktuellen Welle.<br/>                            |
| [**WaveActiveAllTrue**](wavealltrue.md)<br/>                   | Gibt TRUE zurück, wenn der Ausdruck in allen aktiven Lanes in der aktuellen Welle true ist.<br/>                                                                                |
| [**WaveActiveAnyTrue**](waveanytrue.md)<br/>                   | Gibt TRUE zurück, wenn der Ausdruck in einer der aktiven Lanes in der aktuellen Welle true ist.<br/>                                                                         |
| [**WaveActiveBallot**](waveballot.md)<br/>                     | Gibt eine 4-Bit-Ganzzahlbitmaske ohne Vorzeichen der Auswertung des booleschen Ausdrucks für alle aktiven Lanes in der angegebenen Welle zurück. <br/>                              |
| [**WaveGetLaneCount**](wavegetlanecount.md)<br/>               | Gibt die Anzahl der Lanes in einer Welle in dieser Architektur zurück. <br/>                                                                                                   |
| [**WaveGetLaneIndex**](wavegetlaneindex.md)<br/>               | Gibt den Index der aktuellen Spur innerhalb der aktuellen Welle zurück. <br/>                                                                                                |
| [**WaveIsFirstLane**](waveisfirstlane.md)<br/>                 | Gibt "true" nur für die aktive Spur in der aktuellen Welle mit dem kleinsten Index zurück. <br/>                                                                            |
| [**WavePrefixCountBits**](waveprefixcountbytes.md)<br/>        | Gibt die Summe aller angegebenen booleschen Variablen zurück, die für alle aktiven Lanes mit Indizes, die kleiner als die aktuelle Spur sind, auf TRUE festgelegt sind. <br/>                        |
| [**WavePrefixProduct**](waveprefixproduct.md)<br/>             | Gibt das Produkt aller Werte in den aktiven Lanes in dieser Welle mit Indizes zurück, die kleiner als diese Spur sind.<br/>                                                    |
| [**WavePrefixSum**](waveprefixsum.md)<br/>                     | Gibt die Summe aller Werte in den aktiven Lanes mit kleineren Indizes als dieser zurück.<br/>                                                                   |
| [**WaveReadLaneFirst**](wavereadfirstlane.md)<br/>             | Gibt den Wert des Ausdrucks für die aktive Spur der aktuellen Welle mit dem kleinsten Index zurück. <br/>                                                          |
| [**WaveReadLaneAt**](wavereadlaneat.md)<br/>                   | Gibt den Wert des Ausdrucks für den angegebenen Lane-Index innerhalb der angegebenen Welle zurück.<br/>                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Shadermodell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shadermodelle im Vergleich zu Shaderprofilen](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 





