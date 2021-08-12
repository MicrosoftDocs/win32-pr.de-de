---
description: Die Renderingschnittstellen für Direct3D bestehen aus Methoden, die Primitive aus Scheitelpunktdaten rendern, die in einem oder mehreren Datenpuffern gespeichert sind.
ms.assetid: e89eae14-f480-470c-b301-f7ff316ad339
title: Vertex Data Streams (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f154621da4ba03f78beee87767130e37da9e9ab9ba899af737b968fb20f0609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290384"
---
# <a name="vertex-data-streams-direct3d-9"></a>Vertex Data Streams (Direct3D 9)

Die Renderingschnittstellen für Direct3D bestehen aus Methoden, die Primitive aus Scheitelpunktdaten rendern, die in einem oder mehreren Datenpuffern gespeichert sind. Scheitelpunktdaten bestehen aus Scheitelpunktelementen, die zu Scheitelpunktkomponenten kombiniert werden. Scheitelpunktelemente, die kleinste Einheit eines Scheitelpunkts, stellen Entitäten wie Position, Normal oder Farbe dar.

Scheitelpunktkomponenten sind ein oder mehrere Vertexelemente, die zusammenhängend (verleaved pro Scheitelpunkt) in einem einzelnen Speicherpuffer gespeichert sind. Ein vollständiger Scheitelpunkt besteht aus mindestens einer Komponente, wobei sich jede Komponente in einem separaten Speicherpuffer befindet. Zum Rendern eines Primitiven werden mehrere Scheitelpunktkomponenten gelesen und zusammengestellt, sodass vollständige Scheitelpunkte für die Scheitelpunktverarbeitung verfügbar sind. Das folgende Diagramm zeigt den Prozess des Renderns von Primitiven mithilfe von Scheitelpunktkomponenten.

![Diagramm des Prozesses zum Rendern von Primitiven mithilfe von Scheitelpunktkomponenten](images/vertexdata.png)

Renderingprimitive bestehen aus zwei Schritten. Richten Sie zunächst einen oder mehrere Scheitelpunktkomponentenstreams ein. Rufen Sie zweitens eine [**IDirect3DDevice9::D rawPrimitive-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) auf, um aus diesen Streams zu rendern. Die Identifizierung von Scheitelpunktelementen in diesen Komponentenstreams wird vom Vertex-Shader angegeben.

Die [**IDirect3DDevice9::D rawPrimitive-Methoden**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) geben einen Offset in den Scheitelpunktdatenströmen an, sodass bei jedem Zeichnen-Aufruf eine beliebige zusammenhängende Teilmenge der Primitive in einem Satz von Scheitelpunktdaten gerendert werden kann. Dadurch können Sie den Renderingzustand des Geräts zwischen Gruppen von Primitiven ändern, die aus denselben Scheitelpunktpuffern gerendert werden.

Sowohl indizierte als auch nicht indizierte Zeichnungsmethoden werden unterstützt. Weitere Informationen finden Sie unter [Rendern von Scheitelpunkt- und Indexpuffern (Direct3D 9).](rendering-from-vertex-and-index-buffers.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern von Primitiven](rendering-primitives.md)
</dt> </dl>

 

 
