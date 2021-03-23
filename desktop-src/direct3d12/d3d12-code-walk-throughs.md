---
title: D3D12-Code Walk-Throughs
description: Dieser Abschnitt enthält Code für Beispielszenarien. Viele der exemplarischen Vorgehensweisen enthalten Informationen dazu, welche Codierung einem einfachen Beispiel hinzugefügt werden muss, um zu vermeiden, dass der Grundkomponenten Code für jedes Szenario wiederholt wird.
ms.assetid: 1F37FD3A-385C-4DD5-B04C-980F078D90D0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdea9b519e2a0adac9dc346d6bee455af0018da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103982"
---
# <a name="d3d12-code-walk-throughs"></a>D3D12-Code Walk-Throughs

Dieser Abschnitt enthält Code für Beispielszenarien. Viele der exemplarischen Vorgehensweisen enthalten Informationen dazu, welche Codierung einem einfachen Beispiel hinzugefügt werden muss, um zu vermeiden, dass der Grundkomponenten Code für jedes Szenario wiederholt wird.

Eine grundlegende Komponente finden Sie im Abschnitt [Creating a Basic Direct3D 12 Component](creating-a-basic-direct3d-12-component.md) . In den folgenden exemplarischen Vorgehensweisen werden erweiterte Szenarios beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                           | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [D2D mit D3D11on12](d2d-using-d3d11on12.md)<br/>                                       | Das **D3D1211on12** -Beispiel veranschaulicht das Rendering von D2D-Inhalt über D3D12-Inhalt, indem Ressourcen zwischen einem 11 basierten Gerät und einem 12-basierten Gerät gemeinsam genutzt werden. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [N-Text-Schwerkraft Simulation mit mehreren Modulen](multi-engine-n-body-gravity-simulation.md)<br/> | Das **D3D12nBodyGravity** -Beispiel veranschaulicht, wie Compute-Arbeit asynchron ausgeführt wird. Das Beispiel startet eine Reihe von Threads, die jeweils über eine COMPUTE-Befehls Warteschlange verfügen, und plant Compute-Arbeit auf der GPU, die eine n-Text-Schwerkraft Simulation ausführt. Jeder Thread arbeitet mit zwei Puffer, die sich aus der Position und den Geschwindigkeitsdaten zusammen befinden. Bei jeder Iterationen liest der COMPUTE-Shader die aktuellen Positions-und Geschwindigkeitsdaten aus einem Puffer und schreibt die nächste Iterationen in den anderen Puffer. Wenn die Iterationen abgeschlossen sind, tauscht der COMPUTE-Shader aus, welcher Puffer der SRV zum Lesen von Positions-/Velocity-Daten ist. dabei handelt es sich um die UAV zum Schreiben von Positions-/Velocity-Updates durch Ändern des Ressourcen Zustands für jeden Puffer.<br/> |
| [Prädikationsabfragen](predication-queries.md)<br/>                                       | Das **D3D12PredicationQueries** -Beispiel veranschaulicht die Verschleierung von Okklusion mithilfe von DirectX 12-Abfrage Heaps und-Prädikaten. In der exemplarischen Vorgehensweise wird der zusätzliche Code beschrieben, der zum Erweitern des **helloconstbuffer** -Beispiels für die Behandlung von prädikationsabfragen <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Dynamische Indizierung mit HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)<br/>               | Das **D3D12DynamicIndexing** -Beispiel veranschaulicht einige der neuen HLSL-Features, die im Shader-Modell 5,1 verfügbar sind, insbesondere dynamische Indizierung und ungebundene Arrays, um das gleiche Mesh mehrmals zu rendern, wobei jedes Mal ein dynamisch ausgewähltes Material gerendert wird. Bei der dynamischen Indizierung können Shader jetzt in ein Array indizieren, ohne den Wert des Indexes zur Kompilierzeit zu kennen. In Kombination mit unbegrenzten Arrays wird dadurch eine weitere dereferenzierungsstufe und Flexibilität für Shader-Autoren und Kunst Pipelines hinzugefügt.<br/>                                                                                                                                                                                  |
| [Indirektes zeichnen und GPU-culult](indirect-drawing-and-gpu-culling-.md)<br/>            | Das D3D12ExecuteIndirect-Beispiel veranschaulicht, wie indirekte Befehle zum Zeichnen von Inhalten verwendet werden. Außerdem wird veranschaulicht, wie diese Befehle auf der GPU in einem Compute-Shader bearbeitet werden können, bevor Sie ausgegeben werden. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Direct3D 12-Programmier Handbuch](directx-12-programming-guide.md)
</dt> <dt>

[Video-Tutorials zu DirectX Advanced Learning](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
</dt> <dt>

[Beispiel Code in der D3D12-Referenz](notes-on-example-code.md)
</dt> <dt>

[Funktionierende Beispiele](working-samples.md)
</dt> </dl>

 

 





