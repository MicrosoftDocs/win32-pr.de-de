---
title: Untergeordnete Zuordnung innerhalb von Puffern
description: Puffer verfügen über alle Features, die in D3D12 erforderlich sind, damit Anwendungen einen großen Bereich vorübergehender Daten von der CPU auf die GPU übertragen können. In diesem Abschnitt werden vier häufige Szenarien für die Verwendung und Verwaltung von Ressourcen und Puffern behandelt.
ms.assetid: 359E377A-8E16-4BB5-9055-09617335AB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64944cb11507b8dc437d075938fad419f333433
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104462"
---
# <a name="suballocation-within-buffers"></a>Untergeordnete Zuordnung innerhalb von Puffern

Puffer verfügen über alle Features, die in D3D12 erforderlich sind, damit Anwendungen einen großen Bereich vorübergehender Daten von der CPU auf die GPU übertragen können. In diesem Abschnitt werden vier häufige Szenarien für die Verwendung und Verwaltung von Ressourcen und Puffern behandelt.

Ähnlich wie bei D3D11 müssen Anwendungen in D3D12 weiterhin die Verwendung des Arbeitsspeichers deklarieren, wenn Puffer in D3D12 im Vergleich zu dynamischen/stagingressourcen in D3D11 zugeordnet werden, aber in D3D12 haben Entwickler mehr Flexibilität und eine strengere Kontrolle über die Speicherauslastung. Puffer über die unter Zuweisung verfügen über alle Features, die für die Speicherverwaltung auf niedriger Ebene erforderlich sind.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                        | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Hochladen verschiedener Arten von Ressourcen](uploading-resources.md)<br/>                 | Zeigt, wie ein Puffer verwendet wird, um sowohl Konstante Puffer Daten als auch Vertex-Puffer Daten in die GPU hochzuladen und Daten in Puffern ordnungsgemäß zuzuordnen und zu platzieren. Die Verwendung eines einzelnen Puffers steigert die Flexibilität der Speicherauslastung und bietet Anwendungen eine strengere Kontrolle der Speicherauslastung. Zeigt außerdem die Unterschiede zwischen den D3D11-und D3D12-Modellen zum Hochladen unterschiedlicher Ressourcentypen.<br/> |
| [Hochladen von Textur Daten über Puffer](upload-and-readback-of-texture-data.md)<br/> | Das Hochladen von 2D-oder 3D-Textur Daten ähnelt dem Hochladen von 1D-Daten, mit dem Unterschied, dass Anwendungen die Daten Ausrichtung im Zusammenhang mit der Zeilen Tonhöhe genauer berücksichtigen müssen. Puffer können von mehreren Teilen der Grafik Pipeline orthogonell und gleichzeitig verwendet werden und sind sehr flexibel. <br/>                                                                                                                       |
| [Zurück Lesen von Daten über einen Puffer](readback-data-using-heaps.md)<br/>                    | Beim Lesen von Daten aus der GPU, z. b. beim Aufzeichnen eines Screenshots, wird der readback-Heap verwendet. <br/>                                                                                                                                                                                                                                                                                                     |
| [Auf der Fence basierende Ressourcenverwaltung](fence-based-resource-management.md)<br/>            | Zeigt, wie die Lebensdauer von Ressourcen Daten verwaltet wird, indem der GPU-Status über Zäune nachverfolgt wird. Der Arbeitsspeicher kann mit der Verwendung von Zäunen, die die Verfügbarkeit von freiem Speicherplatz im Arbeitsspeicher sorgfältig verwalten, wie z. b. in einer Ringpuffer Implementierung für einen uploadheap <br/>                                                                                                                                                     |



 

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Speicherverwaltung](memory-management.md)
</dt> </dl>

 

 





