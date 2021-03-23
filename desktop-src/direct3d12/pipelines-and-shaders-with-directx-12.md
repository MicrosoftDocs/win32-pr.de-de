---
title: Pipelines und Shader mit Direct3D 12
description: Die programmierbare Pipeline Direct3D 12 erhöht die Renderingleistung im Vergleich zu den Schnittstellen Schnittstellen für die Grafik Programmierung.
ms.assetid: 329882F5-D2A9-4D6D-AC3B-29F370D22C97
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2c392b3915443da2f287a5511f3959cbb7179f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104548671"
---
# <a name="pipelines-and-shaders-with-direct3d-12"></a>Pipelines und Shader mit Direct3D 12

Die programmierbare Pipeline Direct3D 12 erhöht die Renderingleistung im Vergleich zu den Schnittstellen Schnittstellen für die Grafik Programmierung.

-   [Direct3D 12-Grafik Pipeline](#direct3d-12-graphics-pipeline)
-   [Pipeline Zustands Objekte](#pipeline-state-objects)
-   [Direct3D 12 Compute-Pipeline](#direct3d-12-compute-pipeline)
-   [Verwandte Themen](#related-topics)

## <a name="direct3d-12-graphics-pipeline"></a>Direct3D 12-Grafik Pipeline

Im folgenden Diagramm werden die Direct3D 12-Grafik Pipeline und der-Zustand veranschaulicht.

![Diagramm zur Veranschaulichung von Direct3D 12 Pipeline und Status](images/pipeline.png)

Eine Grafik Pipeline ist der sequenzielle Fluss von Dateneingaben und-Ausgaben, wenn die GPU Frames rendert. Aufgrund des Pipeline Zustands und der Eingaben führt die GPU eine Reihe von Vorgängen aus, um die resultierenden Images zu erstellen. Eine Grafik Pipeline enthält Shader, die programmierbare renderingoffekte und Berechnungen ausführen, sowie fixierte Funktions Vorgänge.

Beachten Sie beim Verweis auf das Pipeline Status Diagramm Folgendes:

-   Die deskriptortabellen und Heaps können beliebig angeordnet werden: Srvs, cbvs und UAVs können referenziert und in beliebiger Reihenfolge zugeordnet werden.
-   Einige Vorgänge der Pipeline sind konfigurierbar. Beispielsweise wird bei der Ausgabe Zusammenführung in der Regel eine Lese-/Schreib-Schreibweise mit den Ansichten "Renderziel" und "tiefen Schablone" angewendet. Die Pipeline kann jedoch so konfiguriert werden, dass beide Sichten schreibgeschützt oder schreibgeschützt sind.
-   Statische Samplern sind nicht Teil der root-Argumente, da Sie statisch sind.

## <a name="pipeline-state-objects"></a>Pipeline Zustands Objekte

Direct3D 12 führt das Pipeline State Object (PSO) ein. Anstatt den Pipeline Zustand für eine große Anzahl von Objekten auf hoher Ebene zu speichern und darzustellen, werden die Zustände von Pipeline Komponenten wie der Eingabe Assembler, der Rasterizer, der Pixelshader und die Ausgabe Zusammenführung in einem PSO gespeichert. Bei einem PSO handelt es sich um ein einheitliches Pipeline Zustands Objekt, das nach der Erstellung unveränderlich ist. Das aktuell ausgewählte PSO kann schnell und dynamisch geändert werden, und die Hardware und Treiber können ein PSO direkt in systemeigene Hardware Anweisungen und den Status konvertieren, indem Sie die GPU für die Grafik Verarbeitung lesen. Zum Anwenden eines PSO wird von der Hardware eine minimale Menge vorberechneter Zustände direkt in die Hardware Register kopiert. Dadurch entfällt der Aufwand, der durch den Grafiktreiber aufgrund der aktuellen Rendering-und Pipeline Einstellungen durch den Grafiktreiber ständig neu berechnet wird. Das Ergebnis ist erheblich Reduzierter Aufwand für den Draw-Aufruf, eine höhere Leistung und mehr Draw-Aufrufe pro Frame.

Der aktuell angewendete PSO definiert und verbindet alle Shader, die in der Renderingpipeline verwendet werden. [Microsoft High Level Shader Language (HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) wird in Shader-Objekte vorkompiliert, die dann zur Laufzeit als Eingabe für Pipeline Zustands Objekte verwendet werden. Weitere Informationen zur Funktionsweise von PSO in der Grafik Pipeline finden Sie unter [Verwalten des Grafik Pipeline Zustands in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

## <a name="direct3d-12-compute-pipeline"></a>Direct3D 12 Compute-Pipeline

Das folgende Diagramm veranschaulicht die Compute-Pipeline und den Direct3D 12-computebereich.

![Diagramm, das die Direct3D 12-Compute-Pipeline anzeigt.](images/compute-pipeline.png)

Diese Pipeline enthält keine Fixed-Funktionseinheiten, aber deskriptorheaps, samplingheaps und statische Samplern sind weiterhin in Compute verfügbar.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Arbeits Übermittlung in Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

 