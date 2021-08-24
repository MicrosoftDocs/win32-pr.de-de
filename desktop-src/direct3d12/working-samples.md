---
title: Funktionierende Beispiele
description: Arbeitsbeispiele stehen zum Download zur Verfügung, die die Verwendung einer Reihe von Features von Direct3D 12 zeigen.
ms.assetid: 4C4475D4-534F-484F-8D60-9ACEA09AC109
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6f8bad1d20729f4caa78952feda22378ad37526b33b668e79260ef9658da53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631882"
---
# <a name="working-samples"></a>Funktionierende Beispiele

Arbeitsbeispiele stehen zum Download zur Verfügung, die die Verwendung einer Reihe von Features von Direct3D 12 zeigen.

## <a name="working-samples"></a>Arbeitsbeispiele

Arbeitsbeispiele (in Form von Visual Studio 2015-Projekten) können unter [GitHub/Microsoft/DirectX-Graphics-Samples heruntergeladen werden.](https://github.com/Microsoft/DirectX-Graphics-Samples)

> [!Note]  
> Die genaue Liste der an diesem Speicherort verfügbaren Beispiele variiert, wenn Beispiele hinzugefügt und aktualisiert werden.

 



<table>
<thead>
<tr class="header">
<th>Beispieltitel</th>
<th>BESCHREIBUNG</th>
<th>Desktop</th>
<th>UWP</th>
<th>Exemplarische Vorgehensweise</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>HelloWorld<dl> HelloWindow<br />
HelloTringle<br />
HelloBundles<br />
HelloConstBuffers<br />
HelloTexture<br />
</dl></td>
<td>Der HelloWorld-Beispielsatz enthält die folgenden einfachen Projekte für die ersten Schritte mit Direct3D 12.<dl> Erstellt ein Fenster zur Vorbereitung des Renderns von Direct3D 12-Inhalten.<br />
Rendert ein einfaches Dreieck mit Direct3D 12.<br />
Veranschaulicht die Verwendung eines Bündels für das Rendering mit Direct3D 12.<br />
Veranschaulicht, wie konstante Puffer verwendet werden, um Daten an die GPU zu übergeben, die für das Rendering in Direct3D 12 verwendet wird.<br />
Veranschaulicht, wie eine Textur mit Direct3D 12 auf ein Dreieck angewendet wird.<br />
</dl></td>
<td>J</td>
<td>J</td>
<td><a href="creating-a-basic-direct3d-12-component.md">Erstellen einer einfachen Direct3D 12-Komponente</a></td>
</tr>
<tr class="even">
<td>D3D12Bundles</td>
<td>Veranschaulicht bewährte Methoden für Framepufferung und -synchronisierung sowie das Rendern eines einfachen Gitters mithilfe von Bündeln.</td>
<td>J</td>
<td>J</td>

</tr>
<tr class="odd">
<td>D3D12Multithreading</td>
<td>Ein Beispiel für das Erstellen einer Multithreadanwendung.</td>
<td>J</td>
<td>N</td>

</tr>
<tr class="even">
<td>D3D12nBodyIty</td>
<td>Veranschaulicht, wie multi-engine verwendet werden kann, um asynchrone Computearbeit zusammen mit 3D-Arbeiten auf derselben GPU zu ermöglichen.</td>
<td>J</td>
<td>J</td>
<td><a href="multi-engine-n-body-gravity-simulation.md">N-Körper-Schwerkraftsimulation mit mehreren Modulen</a></td>
</tr>
<tr class="odd">
<td>D3D12PredicationQueries</td>
<td>Veranschaulicht okklusion culling mithilfe von Abfragehaps und Prädication.</td>
<td>J</td>
<td>J</td>
<td><a href="predication-queries.md">Prädikationsabfragen</a></td>
</tr>
<tr class="even">
<td>D3D12DynamicIndexing</td>
<td>Veranschaulicht die dynamischen Indizierungsfunktionen von DirectX 12 und HLSL.</td>
<td>J</td>
<td>J</td>
<td><a href="dynamic-indexing-using-hlsl-5-1.md">Dynamische Indizierung mit HLSL 5.1</a></td>
</tr>
<tr class="odd">
<td>D3D1211on12</td>
<td>Veranschaulicht die grundlegende Verwendung der Ebene 11on12. In diesem Beispiel wird Text mithilfe von D2D mithilfe der Direct3D 11-API auf einem Direct3D 12 11on12-Gerät gerendert.</td>
<td>J</td>
<td>J</td>
<td><a href="d2d-using-d3d11on12.md">D2D mit D3D11on12</a></td>
</tr>
<tr class="even">
<td>D3D12ExecuteIndirect</td>
<td>Veranschaulicht das Compute-Engine-Culling in Verbindung mit dem Indirekten Ausführungsfeature, um nur Objekte zu rendern, die den Cullingtest bestehen.</td>
<td>J</td>
<td>J</td>
<td><a href="indirect-drawing-and-gpu-culling-.md">Indirektes Zeichnen und GPU-Culling</a></td>
</tr>
<tr class="odd">
<td>D3D12PipelineStateCache</td>
<td>Veranschaulicht das Zwischenspeichern von Pipelinezustandsobjekten (PIPELINE State Object, PSO).</td>
<td>J</td>
<td>J</td>

</tr>
<tr class="even">
<td>D3D12Fullscreen</td>
<td>Veranschaulicht, wie Der Vollbildmodus in DirectX 12 mit Fensterübergängen und Deren Größe geändert wird.</td>
<td>J</td>
<td>J</td>

</tr>
<tr class="odd">
<td>D3D12Adapter</td>
<td>Veranschaulicht, wie Workloads mithilfe von freigegebenen Heaps für mehrere heterogene GPUs freigegeben werden.</td>
<td>J</td>
<td>J</td>

</tr>
<tr class="even">
<td>D3D12ReservedResources</td>
<td>Veranschaulicht die Verwendung reservierter (gekachelter) Ressourcen. In diesem Beispiel wird ein Quad mit einer reservierten Ressource texturiert, die eine vollständige MIP-Kette enthält.</td>
<td>J</td>
<td>J</td>

</tr>
<tr class="odd">
<td>D3D12Residency</td>
<td>Dies ist als kostengünstige Lösung für die Verwaltung Ihrer Direct3D 12-Heaps und -Ressourcen mithilfe von Speicherverwaltungstechniken von Direct3D 11 vorgesehen.</td>
<td>J</td>
<td>J</td>

</tr>
<tr class="even">
<td>D3D12SmallResources</td>
<td>Veranschaulicht die Verwendung von kleinen platzierten Ressourcen und zeigt die potenziellen Speichereinsparungen, die durch platzierte Ressourcen (mit einer 4K-Ausrichtung) gegenüber gebundenen und reservierten Ressourcen (mit einer 64K-Ausrichtung) erzielt wurden.</td>
<td>J</td>
<td>J</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 12-Programmieranleitung](directx-12-programming-guide.md)
</dt> <dt>

[Exemplarische Vorgehensweisen zu D3D12-Code](d3d12-code-walk-throughs.md)
</dt> </dl>

 

 




