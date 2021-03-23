---
title: Hardware Tarife
description: Die Hardware Ebenen von Ebene 1 bis Ebene 3 verbessern die Ressourcen, die für die Pipeline verfügbar sind.
ms.assetid: 5A640BA9-3914-4481-9A0C-E18B52BD8AFE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38773412d135aa4068f0f843c1a6ef64af06a841
ms.sourcegitcommit: 9d7585cb0b840d0d1a2b7fd02135181e69d0dc9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/15/2020
ms.locfileid: "104548638"
---
# <a name="hardware-tiers"></a>Hardware Tarife

Die Hardware Ebenen von Ebene 1 bis Ebene 3 verbessern die Ressourcen, die für die Pipeline verfügbar sind.

-   [Von hardwareabhängige Beschränkungen](#limits-dependant-on-hardware)
-   [Invariablenlimits](#invariable-limits)
-   [Verwandte Themen](#related-topics)

## <a name="limits-dependant-on-hardware"></a>Von hardwareabhängige Beschränkungen



| Verfügbare Ressourcen für die Pipeline                                                                                                              | Ebene 1                                                                   | Ebene 2        | Ebene 3        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------|---------------|
| Featureebenen                                                                                                                                   | 11.0 und höher                                                                    | 11.0 und höher         | 11.1 +         |
| Maximale Anzahl von Deskriptoren in einer Konstanten Puffer Ansicht (CBV), Shader Ressourcenansicht (SRV) oder unsortierter Zugriffs Ansicht-Heap (UAV), der für das Rendering verwendet wird | 1\.000.000                                                                | 1\.000.000     | 1000000 +    |
| Maximale Anzahl konstanter Puffer Sichten in allen deskriptortabellen pro Shader-Stufe                                                                | 14                                                                       | 14            | **vollständiger Heap** |
| Maximale Anzahl von Shader-Ressourcen Sichten in allen deskriptortabellen pro Shader-Stufe                                                                | 128                                                                      | **vollständiger Heap** | vollständiger Heap     |
| Maximale Anzahl von ungeordneten Zugriffs Sichten in allen deskriptortabellen in allen Phasen                                                              | 64 für Funktionsebenen 11.1 und höher<br/> 8 für Featureebene 11<br/> | 64            | **vollständiger Heap** |
| Maximale Anzahl von Samplern in allen deskriptortabellen pro Shader-Phase                                                                             | 16                                                                       | **2048** | 2048     |



 

In **fetten** Einträgen werden deutliche Verbesserungen gegenüber der vorherigen Ebene hervorgehoben.

Es gibt eine zusätzliche Einschränkung für die Hardware der Ebene 1, die für alle Heaps gilt. und auf Ebene 2-Hardware, die für CBV und UAV-Heaps gilt, dass alle deskriptorheap-Einträge, die von deskriptortabellen in der Stamm Signatur abgedeckt werden, beim Ausführen des Shaders mit Deskriptoren aufgefüllt werden *müssen* , selbst wenn der Shader (möglicherweise aufgrund einer Verzweigung) den Deskriptor nicht benötigt. Es gibt keine Einschränkung für die Hardware der Ebene 3. Eine Entschärfung für diese Einschränkung ist die sorgfältige Verwendung von [null-Deskriptoren](descriptors.md).

## <a name="invariable-limits"></a>Invariablenlimits

Die maximale Anzahl von Samplern in einem sichtbaren Shader-deskriptorheap ist 2048.

Die maximale Anzahl von eindeutigen statischen Samplern in Live Stamm Signaturen beträgt 2032 (bei Treibern, die eigene Samplern benötigen), wird der Wert "16" beibehalten.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Deskriptorheaps](descriptor-heaps.md)
</dt> <dt>

[Hardware Funktionsebenen](hardware-feature-levels.md)
</dt> </dl>

 

 





