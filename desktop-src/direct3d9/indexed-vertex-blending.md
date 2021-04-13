---
description: Indiziertes Vertex-Blending erweitert die Scheitelpunkt Mischungs Unterstützung in Direct3D, damit Matrizen zum Mischen verwendet werden können.
ms.assetid: d320cb8a-48b6-4a53-a051-d50f239c1aa3
title: Indiziertes Vertex-Blending (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cfe7b45831317fdf9e92525ed74bbd27323e99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480715"
---
# <a name="indexed-vertex-blending-direct3d-9"></a>Indiziertes Vertex-Blending (Direct3D 9)

Indiziertes Vertex-Blending erweitert die Scheitelpunkt Mischungs Unterstützung in Direct3D, damit Matrizen zum Mischen verwendet werden können. Auf diese Matrizen wird mithilfe eines Matrix Indexes verwiesen. Diese Indizes werden pro Scheitelpunkt Basis bereitgestellt und verweisen auf eine Palette von bis zu 256 Matrizen. Jeder Index ist 8 Bit, und jeder Scheitelpunkt kann bis zu vier Indizes aufweisen, sodass vier Matrizen pro Scheitelpunkt gemischt werden können. Die Indizes werden in ein DWORD gepackt. Da Indizes pro Scheitelpunkt Basis angegeben werden, können sich bis zu 12 Matrizen auf ein einzelnes Dreieck auswirken, und jede Matrix in der Palette kann die Scheitel Punkte eines zeichnen-Aufrufs beeinflussen. Dieser Ansatz bietet die folgenden Vorteile:

-   Es ermöglicht mehr Matrizen, sich auf ein einzelnes Dreieck zu auswirken.
-   Dadurch können mehr gemischte Dreiecke im selben zeichnen-Befehl weitergegeben werden.
-   Die Vertex-Mischung ist unabhängig von Dreiecks Indizes. Dies ermöglicht die Zusammenarbeit progressiver Netze in Verbindung mit der Vertex-Mischung.

Ein Nachteil dieses Ansatzes besteht darin, dass er nicht mit gekrümmten Oberflächen primitiven funktioniert, wenn das Mosaik vor der Scheitelpunkt Verarbeitung auftritt.

Im folgenden Diagramm wird veranschaulicht, wie sich vier Matrizen auf einen Scheitelpunkt auswirken können. Jeder Scheitelpunkt verfügt über bis zu vier Indizes, sodass vier Matrizen pro Scheitelpunkt gemischt werden können. Das Diagramm verwendet die Matrizen, die bei 0, 2, 5 und 6 indiziert wurden.

![Diagramm der indizierten Vertex-Mischung mithilfe von 4 von 256 verfügbaren Matrizen](images/dword1.png)

Im folgenden Diagramm wird veranschaulicht, wie sich bis zu 12 Matrizen auf ein Dreieck auswirken können. Durch die Verwendung von Indizes, die pro Scheitelpunkt Basis angegeben werden, können bis zu 12 Matrizen das Dreieck beeinflussen.

![Diagramm der indizierten Vertex-Blending für ein Dreieck mithilfe von 12 von 256 verfügbaren Matrizen](images/dword2.png)

Die folgende Gleichung bestimmt den allgemeinen Fall, dass Matrizen einen Scheitelpunkt beeinflussen.

![Gleichung der indizierten Vertex-Blending](images/indexedvblend.png)

V <sub>Model</sub> ist die Vertex-Position des Eingabe Modell Raums. Index0.. Index3 sind die pro-Vertex-Matrix Indizes, die in ein DWORD gepackt werden. M \[ \] ist das Array von Welt Matrizen, die in indiziert werden. b ₀.. b-Gewichtung sind die Blend-Gewichtungen. V<sub>World</sub> ist die Ausgabe Raum-Vertex-Position.

Weitere Informationen zum indizierten Vertex-Blending finden [Sie unter Verwenden der indizierten vertexmischung (Direct3D 9)](using-indexed-vertex-blending.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geometrie Mischung](geometry-blending.md)
</dt> </dl>

 

 



