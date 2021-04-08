---
description: Die renderingschnittstellen für Direct3D bestehen aus Methoden zum Rendern von primitiven aus Scheitelpunkt Daten, die in einem oder mehreren Daten Puffern gespeichert sind.
ms.assetid: e89eae14-f480-470c-b301-f7ff316ad339
title: Vertex-Datenströme (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd45fc3f645de49060cd201a6a6e9e238712338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746104"
---
# <a name="vertex-data-streams-direct3d-9"></a>Vertex-Datenströme (Direct3D 9)

Die renderingschnittstellen für Direct3D bestehen aus Methoden zum Rendern von primitiven aus Scheitelpunkt Daten, die in einem oder mehreren Daten Puffern gespeichert sind. Vertex-Daten bestehen aus Vertex-Elementen, die zum bilden von Scheitelpunkt Komponenten kombiniert werden. Vertex-Elemente, die kleinste Einheit eines Scheitel Punkts, stellen Entitäten dar, z. b. Position, normal oder Farbe.

Bei Scheitelpunkt Komponenten handelt es sich um ein oder mehrere Vertex-Elemente, die in einem einzelnen Speicherpuffer zusammenhängend (verschachtelt pro Scheitelpunkt) gespeichert sind. Ein kompletter Scheitelpunkt besteht aus einer oder mehreren Komponenten, wobei sich jede Komponente in einem separaten Speicherpuffer befindet. Zum Rendering eines primitiven werden mehrere Scheitelpunkt Komponenten gelesen und zusammengestellt, sodass für die Vertexverarbeitung umfassende Scheitel Punkte verfügbar sind. Das folgende Diagramm zeigt den Prozess des Renderings primitiver mithilfe von Scheitelpunkt Komponenten.

![Diagramm des Prozesses zum Rendering von primitiven mithilfe von Scheitelpunkt Komponenten](images/vertexdata.png)

Das Rendern von primitiven besteht aus zwei Schritten. Richten Sie zuerst einen oder mehrere Scheitelpunkt-komponentenstreams ein. Rufen Sie zweitens eine [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) -Methode auf, um diese Datenströme zu Rendering. Die Identifizierung der Scheitelpunkt Elemente innerhalb dieser komponentenstreams wird vom Vertexshader angegeben.

Die [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) -Methoden geben einen Offset in den Vertex-Datenströmen an, sodass eine beliebige zusammenhängende Teilmenge der primitiven innerhalb eines Satzes von Scheitelpunkt Daten mit jedem Zeichnen-Aufruf gerendert werden kann. Dies ermöglicht es Ihnen, den Renderingzustand des Geräts zwischen Gruppen primitiver Elemente zu ändern, die aus denselben Scheitelpunkt Puffern gerendert werden.

Indizierte und nicht indizierte Zeichnungs Methoden werden unterstützt. Weitere Informationen finden Sie unter [Rendering from Scheitelpunkt and Index Buffers (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern von primitiven](rendering-primitives.md)
</dt> </dl>

 

 
