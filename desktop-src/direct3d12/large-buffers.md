---
title: Unterzuweisung innerhalb von Puffern
description: Puffer verfügen über alle Features, die in D3D12 erforderlich sind, damit Anwendungen einen großen Bereich vorübergehender Daten von der CPU auf die GPU übertragen können. In diesem Abschnitt werden vier gängige Szenarien für die Verwendung und Verwaltung von Ressourcen und Puffern behandelt.
ms.assetid: 359E377A-8E16-4BB5-9055-09617335AB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63175bdb8b3937a01abe3ffc57032db78ea978768ee19e2c31d0c50db4103573
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123813"
---
# <a name="suballocation-within-buffers"></a>Unterzuweisung innerhalb von Puffern

Puffer verfügen über alle Features, die in D3D12 erforderlich sind, damit Anwendungen einen großen Bereich vorübergehender Daten von der CPU auf die GPU übertragen können. In diesem Abschnitt werden vier gängige Szenarien für die Verwendung und Verwaltung von Ressourcen und Puffern behandelt.

Ähnlich wie bei D3D11 müssen Anwendungen in D3D12 die Speicherauslastung bei der Zuweisung von Puffern in D3D12 im Vergleich zu dynamischen/Stagingressourcen in D3D11 deklarieren, aber in D3D12 haben Entwickler mehr Flexibilität und eine strengere Kontrolle über die Speicherauslastung. Puffer verfügen über eine untergeordnete Speicherzuweisung über alle Features, die für die Speicherverwaltung auf niedriger Ebene erforderlich sind.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                        | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Hochladen verschiedener Arten von Ressourcen](uploading-resources.md)<br/>                 | Zeigt, wie Sie einen Puffer verwenden, um sowohl konstante Pufferdaten als auch Scheitelpunktpufferdaten auf die GPU hochzuladen, und wie Sie Daten ordnungsgemäß unterteilen und in Puffern platzieren. Die Verwendung eines einzelnen Puffers erhöht die Flexibilität bei der Speicherauslastung und bietet Anwendungen eine strengere Steuerung der Speicherauslastung. Zeigt auch die Unterschiede zwischen den Modellen D3D11 und D3D12 zum Hochladen verschiedener Ressourcentypen an.<br/> |
| [Hochladen von Texturdaten über Puffer](upload-and-readback-of-texture-data.md)<br/> | Das Hochladen von 2D- oder 3D-Texturdaten ähnelt dem Hochladen von 1D-Daten, mit der Ausnahme, dass Anwendungen die Datenausrichtung im Zusammenhang mit der Zeilenhöhe genauer beachten müssen. Puffer können orthogonal und gleichzeitig aus mehreren Teilen der Grafikpipeline verwendet werden und sind sehr flexibel. <br/>                                                                                                                       |
| [Zurücklesen von Daten über einen Puffer](readback-data-using-heaps.md)<br/>                    | Das Zurücklesen von Daten von der GPU, z. B. das Erfassen eines Screenshots, umfasst die Verwendung des Rückleseheaps. <br/>                                                                                                                                                                                                                                                                                                     |
| [Fence-basierte Ressourcenverwaltung](fence-based-resource-management.md)<br/>            | Zeigt, wie Die Lebensdauer von Ressourcendaten durch Nachverfolgen des GPU-Fortschritts über Fences verwaltet wird. Arbeitsspeicher kann effektiv mit Zäunen wiederverwendet werden, um die Verfügbarkeit des freien Speicherplatzes im Arbeitsspeicher sorgfältig zu verwalten, z. B. in einer Ringpufferimplementierung für einen Hochladen Heap. <br/>                                                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Speicherverwaltung](memory-management.md)
</dt> </dl>

 

 





