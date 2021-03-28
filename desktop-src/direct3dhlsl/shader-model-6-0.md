---
title: Shader-Modell 6
description: Shadermodell 6,0 fügt eine Reihe von systeminternen Wellen Vorgangs Funktionen für die Pixel-und Compute-Shader hinzu.
ms.assetid: 2F28F86D-F599-47EA-90D7-6833ABA976FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33eb4eab2a92e929bdefdc1df0f9cb1e0d84909a
ms.sourcegitcommit: 39fe65a8a7c1cbea382c78820663c548f4e77079
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104102550"
---
# <a name="shader-model-6"></a>Shader-Modell 6

Alle nicht-Quad-bezogenen Wave-Funktionen sind in allen shaderphasen verfügbar. Systeminterne Quad-Wave-Funktionen sind nur in Pixel-und Compute-Shadern verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                 | BESCHREIBUNG                                                                                                                                                               |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Quad-acrossdiagonal**](quadreadacrossdiagonal.md)<br/> | Gibt den angegebenen lokalen Wert zurück, der aus der Diagonal umgekehrten Spur in diesem Quad gelesen wird.<br/>                                                                |
| [**Quadumeat**](quadreadlaneat.md)<br/>                   | Gibt den angegebenen Quellwert aus der durch die Lane-ID im aktuellen Quad identifizierten Spur zurück.<br/>                                                            |
| [**Quad-acrossx**](quadswapx.md)<br/>                      | Gibt den angegebenen lokalen Wert zurück, der von der anderen Strecke in diesem Quad in der X-Richtung gelesen wird.<br/>                                                                    |
| [**Quad-acrossy**](quadswapy.md)<br/>                      | Gibt den angegebenen Quellwert zurück, der von der anderen Strecke in diesem Quad in der Y-Richtung gelesen wird.<br/>                                                                   |
| [**Waveactiveallequal**](waveactiveallequal.md)<br/>           | Gibt true zurück, wenn der Ausdruck für jede aktive Strecke in der aktuellen Wave identisch ist (und somit einheitlich ist).<br/>                                             |
| [**Waveactivebitand**](waveallbitand.md)<br/>                  | Gibt das bitweise and aller Werte des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zurück und repliziert Sie zurück in alle aktiven Bereiche. <br/>           |
| [**Waveactivebitor**](waveallbitor.md)<br/>                    | Gibt das bitweise OR aller Werte des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zurück und repliziert Sie zurück in alle aktiven Bereiche. <br/>            |
| [**Waveactivebitxor**](waveallbitxor.md)<br/>                  | Gibt das bitweise XOR aller Werte des Ausdrucks über alle aktiven Bereiche in der aktuellen Wave zurück und repliziert Sie zurück in alle aktiven Bereiche. <br/>           |
| [**Waveactivezählbits**](waveactivecountbits.md)<br/>         | Zählt die Anzahl von booleschen Variablen, die für alle aktiven Bereiche in der aktuellen Wave als true ausgewertet werden, und repliziert das Ergebnis in alle Bereiche in der Wave.<br/> |
| [**Waveactivemax**](waveallmax.md)<br/>                        | Gibt den maximalen Wert des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zurück und repliziert Sie zurück in alle aktiven Bereiche. <br/>                           |
| [**Waveactivemin**](waveallmin.md)<br/>                        | Gibt den minimalen Wert des Ausdrucks über alle aktiven Bereiche in der aktuellen Wave zurück, die auf alle aktiven Bereiche repliziert werden. <br/>                               |
| [**Waveactiveproduct**](waveallproduct.md)<br/>                | Multipliziert die Werte des Ausdrucks über alle aktiven Bereiche in der aktuellen Welle und repliziert Sie zurück in alle aktiven Bereiche.<br/>                       |
| [**Waveactivesum**](waveallsum.md)<br/>                        | Fasst den Wert des Ausdrucks für alle aktiven Bereiche in der aktuellen Wave zusammen und repliziert Sie in allen Bereichen in der aktuellen Wave.<br/>                            |
| [**Waveactivealltrue**](wavealltrue.md)<br/>                   | Gibt "true" zurück, wenn der Ausdruck in allen aktiven Bereichen in der aktuellen Wave "true" ist.<br/>                                                                                |
| [**Waveactiveanytrue**](waveanytrue.md)<br/>                   | Gibt "true" zurück, wenn der Ausdruck in einer der aktiven Bereiche in der aktuellen Wave "true" ist.<br/>                                                                         |
| [**Waveactiveballot**](waveballot.md)<br/>                     | Gibt eine ganzzahlige Bitmaske für eine 4-Bit-Ganzzahl ohne Vorzeichen der Auswertung des booleschen Ausdrucks für alle aktiven Bereiche in der angegebenen Wave zurück. <br/>                              |
| [**Wavegetlanecount**](wavegetlanecount.md)<br/>               | Gibt die Anzahl der Bereiche in einer Welle für diese Architektur zurück. <br/>                                                                                                   |
| [**Wavegetlaneingedex**](wavegetlaneindex.md)<br/>               | Gibt den Index der aktuellen Lane innerhalb der aktuellen Wave zurück. <br/>                                                                                                |
| [**Waveisfirstlane**](waveisfirstlane.md)<br/>                 | Gibt nur für die aktive Spur in der aktuellen Wave mit dem kleinsten Index true zurück. <br/>                                                                            |
| [**Waveprefixzählbits**](waveprefixcountbytes.md)<br/>        | Gibt die Summe aller angegebenen booleschen Variablen für alle aktiven Bereiche mit Indizes zurück, die kleiner als die aktuelle Seite sind. <br/>                        |
| [**Waveprefixproduct**](waveprefixproduct.md)<br/>             | Gibt das Produkt aller Werte in den aktiven Bereichen in dieser Welle mit Indizes zurück, die kleiner sind als diese Strecke.<br/>                                                    |
| [**Waveprefixsum**](waveprefixsum.md)<br/>                     | Gibt die Summe aller Werte in den aktiven Bereichen mit kleineren Indizes als dieser zurück.<br/>                                                                   |
| [**Wavereadlanefirst**](wavereadfirstlane.md)<br/>             | Gibt den Wert des Ausdrucks für die aktive Spur der aktuellen Welle mit dem kleinsten Index zurück. <br/>                                                          |
| [**Wavereadlaneat**](wavereadlaneat.md)<br/>                   | Gibt den Wert des Ausdrucks für den angegebenen Lane-Index innerhalb der angegebenen Wave zurück.<br/>                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Shader-Modell 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader-Modelle vs shaderprofile](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 





