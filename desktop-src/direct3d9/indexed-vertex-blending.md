---
description: Indizierte Vertexmischung erweitert die Unterstützung der Vertexmischung in Direct3D, damit Matrizen für das Mischen verwendet werden können.
ms.assetid: d320cb8a-48b6-4a53-a051-d50f239c1aa3
title: Indexed Vertex Blending (Direct3D 9) (Indizierte Vertexmischung (Direct3D 9))
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3d45e3ff72a33cd21265d1e4aa25e237e2a73e473914898d5c1057316d4ca0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728701"
---
# <a name="indexed-vertex-blending-direct3d-9"></a>Indexed Vertex Blending (Direct3D 9) (Indizierte Vertexmischung (Direct3D 9))

Indizierte Vertexmischung erweitert die Unterstützung der Vertexmischung in Direct3D, damit Matrizen für das Mischen verwendet werden können. Auf diese Matrizen wird mithilfe eines Matrixindexes verwiesen. Diese Indizes werden pro Scheitelpunkt bereitgestellt und beziehen sich auf eine Palette von bis zu 256 Matrizen. Jeder Index ist 8 Bit, und jeder Scheitelpunkt kann bis zu vier Indizes aufweisen, wodurch vier Matrizen pro Scheitelpunkt kombiniert werden können. Die Indizes werden in ein DWORD gepackt. Da Indizes pro Scheitelpunkt angegeben werden, können sich bis zu 12 Matrizen auf ein einzelnes Dreieck auswirken, und jede Matrix in der Palette kann sich auf die Scheitelpunkte eines Zeichnen-Aufrufs auswirken. Dieser Ansatz hat die folgenden Vorteile.

-   Sie ermöglicht es mehr Matrizen, sich auf ein einzelnes Dreieck zu auswirken.
-   Sie ermöglicht es, mehr gemischten Dreiecke im gleichen Zeichnen-Aufruf zu übergeben.
-   Die Vertexmischung wird unabhängig von Dreiecksindizes. Dadurch können progressive Gittergitter in Verbindung mit Vertexblending funktionieren.

Ein Nachteil dieses Ansatzes ist, dass er nicht mit Primitiven mit gekrümmten Oberflächen funktioniert, wenn vor der Vertexverarbeitung ein Mosaik auftritt.

Das folgende Diagramm zeigt, wie sich vier Matrizen auf einen Scheitelpunkt auswirken können. Jeder Scheitelpunkt verfügt über bis zu vier Indizes, sodass vier Matrizen pro Scheitelpunkt kombiniert werden können. Das Diagramm verwendet die Matrizen, die bei 0, 2, 5 und 6 indiziert sind.

![Diagramm der indizierten Vertexmischung mit 4 von 256 verfügbaren Matrizen](images/dword1.png)

Das folgende Diagramm zeigt, wie sich bis zu 12 Matrizen auf ein Dreieck auswirken können. Wenn Indizes pro Scheitelpunkt angegeben werden, können sich bis zu 12 Matrizen auf das Dreieck auswirken.

![Diagramm der indizierten Vertexmischung für ein Dreieck unter Verwendung von 12 von 256 verfügbaren Matrizen](images/dword2.png)

Die folgende Gleichung bestimmt den allgemeinen Fall für die Auswirkung von Matrizen auf einen Scheitelpunkt.

![Gleichung der indizierten Vertexmischung](images/indexedvblend.png)

<sub>V-Modell</sub> ist die Position des Eingabemodellbereichs vertex. Index0.. Index3 sind die Pro-Scheitelpunkt-Matrixindizes, die in ein DWORD gepackt sind. M \[ \] ist das Array von Weltmatrizen, in die indiziert wird. b₀. b₂ sind die Mischungsgewichtungen. V<sub>World</sub> ist die Position des Vertex des Ausgaberaums.

Weitere Informationen zum Indizieren von Scheitelpunkten finden Sie unter [Using Indexed Vertex Blending (Direct3D 9) (Verwenden von indizierter Vertexmischung (Direct3D 9)).](using-indexed-vertex-blending.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geometriemischung](geometry-blending.md)
</dt> </dl>

 

 



