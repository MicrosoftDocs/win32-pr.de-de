---
title: Pipelines und Shader mit Direct3D 12
description: Die programmierbare Direct3D 12-Pipeline erhöht die Renderingleistung im Vergleich zu Grafikprogrammierschnittstellen der vorherigen Generation erheblich.
ms.assetid: 329882F5-D2A9-4D6D-AC3B-29F370D22C97
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd4ab60573fca9b9dce6759b5f87969199f83aed08aaa44a01f1501c402080e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952929"
---
# <a name="pipelines-and-shaders-with-direct3d-12"></a>Pipelines und Shader mit Direct3D 12

Die programmierbare Direct3D 12-Pipeline erhöht die Renderingleistung im Vergleich zu Grafikprogrammierschnittstellen der vorherigen Generation erheblich.

-   [Direct3D 12-Grafikpipeline](#direct3d-12-graphics-pipeline)
-   [Pipelinezustandsobjekte](#pipeline-state-objects)
-   [Direct3D 12-Computepipeline](#direct3d-12-compute-pipeline)
-   [Zugehörige Themen](#related-topics)

## <a name="direct3d-12-graphics-pipeline"></a>Direct3D 12-Grafikpipeline

Das folgende Diagramm veranschaulicht die Direct3D 12-Grafikpipeline und den Zustand.

![Diagramm zur Veranschaulichung der Pipeline und des Zustands von Direct3d 12](images/pipeline.png)

Eine Grafikpipeline ist der sequenzielle Fluss von Dateneingaben und -ausgaben, während die GPU Frames rendert. Angesichts des Pipelinestatus und der Eingaben führt die GPU eine Reihe von Vorgängen aus, um die resultierenden Bilder zu erstellen. Eine Grafikpipeline enthält Shader, die programmierbare Renderingeffekte und Berechnungen sowie feste Funktionsvorgänge ausführen.

Beachten Sie Beim Verweisen auf das Pipelinezustandsdiagramm Folgendes:

-   Die Deskriptortabellen und Heaps können beliebig angeordnet werden: SRVs, CBVs und UAVs können in beliebiger Reihenfolge referenziert und zugeordnet werden.
-   Einige Vorgänge der Pipeline können konfiguriert werden. Beispielsweise erfolgt die Ausgabezusammenführung in der Regel auf Lese-/Änderungs-/Schreibbasis mit den Renderziel- und Tiefenschablonenansichten. Die Pipeline kann jedoch so konfiguriert werden, dass eine dieser Ansichten schreibgeschützt oder schreibgeschützt ist.
-   Statische Sampler sind nicht Teil der Stammargumente, da sie statisch sind.

## <a name="pipeline-state-objects"></a>Pipelinezustandsobjekte

Direct3D 12 führt das Pipelinezustandsobjekt (Pipeline State Object, PSO) ein. Anstatt den Pipelinezustand in einer großen Anzahl von objekten auf hoher Ebene zu speichern und darzustellen, werden die Zustände von Pipelinekomponenten wie Eingabeassembler, Rasterizer, Pixel-Shader und Ausgabezusammenführung in einem PSO gespeichert. Ein PSO ist ein vereinheitlichtes Pipelinezustandsobjekt, das nach der Erstellung unveränderlich ist. Der derzeit ausgewählte PSO kann schnell und dynamisch geändert werden, und die Hardware und Treiber können einen PSO direkt in systemeigene Hardwareanweisungen und -zustände konvertieren, um die GPU für die Grafikverarbeitung vorzubereiten. Um einen PSO anzuwenden, kopiert die Hardware eine minimale Menge an vorab berechnetem Zustand direkt in die Hardwareregister. Dadurch entfällt der Mehraufwand, der dadurch verursacht wird, dass der Grafiktreiber den Hardwarezustand basierend auf allen derzeit anwendbaren Rendering- und Pipelineeinstellungen kontinuierlich neu berechnet. Das Ergebnis ist ein erheblich reduzierter Mehraufwand für Zeichnen-Aufrufe, eine höhere Leistung und mehr Zeichnen-Aufrufe pro Frame.

Der derzeit angewendete PSO definiert und verbindet alle Shader, die in der Renderingpipeline verwendet werden. [Microsoft High Level Shader Language (HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) wird in Shaderobjekte vorkompiliert, die dann zur Laufzeit als Eingabe für Pipelinezustandsobjekte verwendet werden. Weitere Informationen zur Funktionsweise der PSO in der Grafikpipeline finden Sie unter Verwalten des [Grafikpipelinezustands in Direct3D 12.](managing-graphics-pipeline-state-in-direct3d-12.md)

## <a name="direct3d-12-compute-pipeline"></a>Direct3D 12-Computepipeline

Das folgende Diagramm veranschaulicht die Direct3D 12-Computepipeline und den Zustand.

![Diagramm, das die Direct3D 12-Computepipeline zeigt.](images/compute-pipeline.png)

Es gibt keine festen Funktionseinheiten in dieser Pipeline, aber Deskriptorheaps, Samplerheaps und statische Sampler sind weiterhin in Compute verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeitsübermittlung in Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

 