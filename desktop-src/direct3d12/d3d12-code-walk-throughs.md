---
title: Exemplarische Vorgehensweisen zu D3D12-Code
description: Dieser Abschnitt enthält Code für Beispielszenarien. Viele der exemplarischen Vorgehensweisen enthalten Details dazu, welche Codierung einem einfachen Beispiel hinzugefügt werden muss, um zu vermeiden, dass der grundlegende Komponentencode für jedes Szenario wiederholt wird.
ms.assetid: 1F37FD3A-385C-4DD5-B04C-980F078D90D0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0fc076657d8a9096d1206adc9c61b6dc16fc95792dc0c0da2fcd636377b7ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497200"
---
# <a name="d3d12-code-walk-throughs"></a>Exemplarische Vorgehensweisen zu D3D12-Code

Dieser Abschnitt enthält Code für Beispielszenarien. Viele der exemplarischen Vorgehensweisen enthalten Details dazu, welche Codierung einem einfachen Beispiel hinzugefügt werden muss, um zu vermeiden, dass der grundlegende Komponentencode für jedes Szenario wiederholt wird.

Die grundlegendste Komponente finden Sie im Abschnitt [Erstellen einer einfachen Direct3D 12-Komponente.](creating-a-basic-direct3d-12-component.md) In den folgenden exemplarischen Abschnitten werden komplexere Szenarien beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                           | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [D2D mit D3D11on12](d2d-using-d3d11on12.md)<br/>                                       | Im Beispiel **D3D1211on12** wird veranschaulicht, wie D2D-Inhalt über D3D12-Inhalt gerendert wird, indem Ressourcen zwischen einem 11-basierten Gerät und einem 12-basierten Gerät gemeinsam verwendet werden. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [N-Körper-Schwerkraftsimulation mit mehreren Modulen](multi-engine-n-body-gravity-simulation.md)<br/> | Das **D3D12nBodyHowity-Beispiel** veranschaulicht, wie Computearbeit asynchron durchgeführt wird. Das Beispiel führt eine Reihe von Threads mit jeweils einer Computebefehlswarteschlange aus und plant Computearbeit auf der GPU, die eine n-Body-Schwerkraftsimulation ausführt. Jeder Thread arbeitet mit zwei Puffern, die mit Positions- und Geschwindigkeitsdaten gefüllt sind. Bei jeder Iteration liest der Compute-Shader die aktuellen Positions- und Geschwindigkeitsdaten aus einem Puffer und schreibt die nächste Iteration in den anderen Puffer. Wenn die Iteration abgeschlossen ist, tauscht der Compute-Shader aus, welcher Puffer der SRV zum Lesen von Positions-/Geschwindigkeitsdaten und welcher UAV zum Schreiben von Positions-/Geschwindigkeitsaktualisierungen ist, indem der Ressourcenzustand für jeden Puffer geändert wird.<br/> |
| [Prädikationsabfragen](predication-queries.md)<br/>                                       | Das **D3D12PredicationQueries-Beispiel** veranschaulicht okklusions-culling mit DirectX 12-Abfrageheaps und Prädikation. In der exemplarischen Vorgehensweise wird der zusätzliche Code beschrieben, der erforderlich ist, um das **HelloConstBuffer-Beispiel** für die Verarbeitung von Prädikationsabfragen zu erweitern. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Dynamische Indizierung mit HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)<br/>               | Das **D3D12DynamicIndexing-Beispiel** veranschaulicht einige der neuen HLSL-Features, die in Shader Model 5.1 verfügbar sind – insbesondere dynamische Indizierung und ungebundene Arrays –, um dasselbe Gittermodell mehrmals zu rendern, jedes Mal, wenn es mit einem dynamisch ausgewählten Material gerendert wird. Mit der dynamischen Indizierung können Shader jetzt in ein Array indiziert werden, ohne den Wert des Indexes zur Kompilierzeit zu kennen. In Kombination mit ungebundenen Arrays wird dadurch eine weitere Dekonstruktion und Flexibilität für Shaderautoren und -pipelines hinzugefügt.<br/>                                                                                                                                                                                  |
| [Indirektes Zeichnen und GPU-Culling](indirect-drawing-and-gpu-culling-.md)<br/>            | Im Beispiel D3D12ExecuteIndirect wird veranschaulicht, wie sie indirekte Befehle verwenden, um Inhalte zu zeichnen. Außerdem wird veranschaulicht, wie diese Befehle auf der GPU in einem Compute-Shader bearbeitet werden können, bevor sie ausgegeben werden. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 12-Programmieranleitung](directx-12-programming-guide.md)
</dt> <dt>

[Videotutorials für erweitertes Lernen mit DirectX](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
</dt> <dt>

[Beispielcode in der D3D12-Referenz](notes-on-example-code.md)
</dt> <dt>

[Funktionierende Beispiele](working-samples.md)
</dt> </dl>

 

 





