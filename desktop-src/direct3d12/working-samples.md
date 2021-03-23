---
title: Funktionierende Beispiele
description: Funktionierende Beispiele sind zum Herunterladen verfügbar und zeigen die Verwendung einer Reihe von Features von Direct3D 12.
ms.assetid: 4C4475D4-534F-484F-8D60-9ACEA09AC109
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1b61ec374e21c9173797121ee90ec72e789de8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104240"
---
# <a name="working-samples"></a>Funktionierende Beispiele

Funktionierende Beispiele sind zum Herunterladen verfügbar und zeigen die Verwendung einer Reihe von Features von Direct3D 12.

## <a name="working-samples"></a>Funktionierende Beispiele

Funktionierende Beispiele (in Form von Visual Studio 2015-Projekten) können von [GitHub/Microsoft/DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples)heruntergeladen werden.

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
<td>HelloWorld<dl> Hellowindow<br />
Hellodreieck<br />
Hellobundles<br />
"Helloconstbuffers"<br />
Hellotexture<br />
</dl></td>
<td>Die "HelloWorld"-Beispiel Gruppe enthält die folgenden einfachen Projekte, die Ihnen beim Einstieg in Direct3D 12 helfen.<dl> Erstellt ein Fenster zur Vorbereitung des Renderings von Direct3D 12-Inhalt.<br />
Rendert ein einfaches Dreieck mithilfe von Direct3D 12.<br />
Veranschaulicht die Verwendung eines Pakets zum Rendern mit Direct3D 12.<br />
Veranschaulicht, wie Konstante Puffer verwendet werden, um Daten an die GPU zu übergeben, die in Direct3D 12 zum Rendern verwendet wird.<br />
Veranschaulicht, wie eine Textur mithilfe von Direct3D 12 auf ein Dreieck angewendet wird.<br />
</dl></td>
<td>J</td>
<td>J</td>
<td><a href="creating-a-basic-direct3d-12-component.md">Erstellen einer einfachen Direct3D 12-Komponente</a></td>
</tr>
<tr class="even">
<td>D3D12Bundles</td>
<td>Veranschaulicht die bewährten Methoden für Frame Pufferung und Synchronisierung sowie das Rendern eines einfachen Netzes mithilfe von bündeln.</td>
<td>J</td>
<td>J</td>

</tr>
<tr class="odd">
<td>D3D12Multithreading</td>
<td>Ein Beispiel für das Erstellen einer Multithread fähigen Anwendung.</td>
<td>J</td>
<td>N</td>

</tr>
<tr class="even">
<td>D3D12nBodyGravity</td>
<td>Veranschaulicht, wie die multiengine verwendet werden kann, um asynchrone computeaufgaben parallel zu 3D-Aufgaben auf derselben GPU auszuführen.</td>
<td>J</td>
<td>J</td>
<td><a href="multi-engine-n-body-gravity-simulation.md">N-Text-Schwerkraft Simulation mit mehreren Modulen</a></td>
</tr>
<tr class="odd">
<td>D3D12PredicationQueries</td>
<td>Veranschaulicht die Verschleierung von Okklusion mithilfe von Abfrage Heaps und Prädikaten.</td>
<td>J</td>
<td>J</td>
<td><a href="predication-queries.md">Prädikationsabfragen</a></td>
</tr>
<tr class="even">
<td>D3D12DynamicIndexing</td>
<td>Veranschaulicht die dynamischen Indizierungs Funktionen von DirectX 12 und HLSL.</td>
<td>J</td>
<td>J</td>
<td><a href="dynamic-indexing-using-hlsl-5-1.md">Dynamische Indizierung mit HLSL 5.1</a></td>
</tr>
<tr class="odd">
<td>D3D1211on12</td>
<td>Veranschaulicht die grundlegende Verwendung der 11on12-Ebene. In diesem Beispiel wird Text mithilfe von D2D mithilfe der Direct3D 11-API auf einem Direct3D 12 11on12-Gerät gerendert.</td>
<td>J</td>
<td>J</td>
<td><a href="d2d-using-d3d11on12.md">D2D mit D3D11on12</a></td>
</tr>
<tr class="even">
<td>D3D12ExecuteIndirect</td>
<td>Veranschaulicht das Berechnen von computemodulen in Verbindung mit der Funktion "indirekte ausführen", um nur Objekte zu renderten, die den culck-Test bestehen.</td>
<td>J</td>
<td>J</td>
<td><a href="indirect-drawing-and-gpu-culling-.md">Indirektes zeichnen und GPU-culult</a></td>
</tr>
<tr class="odd">
<td>D3D12PipelineStateCache</td>
<td>Veranschaulicht das Zwischenspeichern von Pipeline Zustands Objekten (PSO).</td>
<td>J</td>
<td>J</td>

</tr>
<tr class="even">
<td>D3D12Fullscreen</td>
<td>Veranschaulicht die Behandlung von voll Bild Vorgängen und Fenstergröße in DirectX 12.</td>
<td>J</td>
<td>J</td>

</tr>
<tr class="odd">
<td>D3D12HeterogeneousMultiadapter</td>
<td>Veranschaulicht das Freigeben von Arbeits Auslastungen für mehrere heterogene GPUs mithilfe von freigegebenen Heaps.</td>
<td>J</td>
<td>J</td>

</tr>
<tr class="even">
<td>D3D12ReservedResources</td>
<td>Veranschaulicht die Verwendung reservierter (gekachelter) Ressourcen. In diesem Beispiel wird ein Quad mit einer reservierten Ressource mit einer vollständigen MIP-Kette texturiert.</td>
<td>J</td>
<td>J</td>

</tr>
<tr class="odd">
<td>D3D12Residency</td>
<td>Dies ist als Lösung für die kostenlose Integration für die Verwaltung Ihrer Direct3D 12 Heaps und für das committet von Ressourcen mit Speicher Verwaltungsverfahren von Direct3D 11 gedacht.</td>
<td>J</td>
<td>J</td>

</tr>
<tr class="even">
<td>D3D12SmallResources</td>
<td>Veranschaulicht die Verwendung von kleinen bereitstellten Ressourcen und zeigt die potenziellen Speicher Einsparungen, die durch die Verwendung von bereitstellten Ressourcen (mit einer Ausrichtung von 4K) über zugesicherte und reservierte Ressourcen (mit einer Ausrichtung von 64K) erzielt wurden.</td>
<td>J</td>
<td>J</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Direct3D 12-Programmier Handbuch](directx-12-programming-guide.md)
</dt> <dt>

[D3D12-Code Exemplarische Vorgehensweisen](d3d12-code-walk-throughs.md)
</dt> </dl>

 

 




