---
description: Das folgende Diagramm zeigt den Pfad, der von den Texturkoordinaten ihrer Quelle, durch Verarbeitung und für den Rasterizer übernommen wird.
ms.assetid: a6126946-8f75-4b3a-b017-d1014e917e9c
title: Verarbeitung von Texturkoordinaten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a161d3675a5859702368a62719124aa029ee455
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041282"
---
# <a name="texture-coordinate-processing-direct3d-9"></a>Verarbeitung von Texturkoordinaten (Direct3D 9)

Das folgende Diagramm zeigt den Pfad, der von den Texturkoordinaten ihrer Quelle, durch Verarbeitung und für den Rasterizer übernommen wird.

![Diagramm des Pfads für Texturkoordinaten von einer Quelle zum Raster](images/tex-processing.png)

Es gibt zwei Quellen, aus denen das System Texturkoordinaten zeichnen kann. Für eine bestimmte Textur Phase können Sie im Vertex-Format (D3DFVF \_ TEX1 through D3DFVF TEX8) enthaltene Texturkoordinaten verwenden \_ , oder Sie können die von Direct3D automatisch generierten Texturkoordinaten verwenden. Ausführliche Informationen zum letzteren Fall finden Sie unter [automatisch generierte Texturkoordinaten (Direct3D 9)](automatically-generated-texture-coordinates.md). Wenn der D3DTSS \_ texturetransformflags-Textur Phasen Zustand für die aktuelle Textur Phase auf D3DTTFF \_ deaktiviert (Standardeinstellung) festgelegt ist, werden die eingabekoordinaten nicht transformiert. Wenn D3DTSS \_ texturetransformflags> auf einen anderen Wert festgelegt ist, wird die Transformationsmatrix für diese Phase auf die eingabekoordinaten angewendet.

Der [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) -enumerierte Typ definiert gültige Werte für den D3DTSS \_ texturetransformflags-Textur Zustand. Mit Ausnahme des \_ Flag D3DTTFF deaktivieren, das die Texturkoordinaten Transformation umgeht, konfigurieren die in dieser Enumeration definierten Werte die Anzahl der Ausgabe Koordinaten, die das System an den Rasterizer übergibt. Die D3DTTFF \_ COUNT1 through D3DTTFF \_ COUNT4-Flags weisen das System an, ein, zwei, drei oder vier Elemente von den Ausgabe Koordinaten an den Rasterizer zu übergeben.

Das D3DTTFF- \_ projizierte Flag ist besonders: Es weist das System an, dass die Texturkoordinaten für eine projizierte Textur sind. Kombinieren Sie das D3DTTFF \_ projizierte Flag mit einem anderen Member von [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) , um den Raster anzuweisen, alle Elemente durch das letzte Element zu unterteilen, bevor die rasterisierung stattfindet. Wenn Sie z. b. explizit drei-Element-Texturkoordinaten verwenden oder wenn die Transformation zu einer drei-Element-Textur Koordinate führt, können Sie die D3DTTFF \_ COUNT3-und D3DTTFF-projizierten Flags kombinieren, damit \_ der Raster die ersten beiden Elemente durch die letzte teilt, sodass 2D-Texturkoordinaten zur Adressierung einer 2D-Textur erforderlich sind.

> [!Note]  
> Mit Ausnahme von kubischen Umgebungs Zuordnungen und volumetexturen können Rasterizers keine Texturen mithilfe von Texturkoordinaten mit mehr als zwei Elementen adressieren. Wenn Sie mehr Elemente angeben, als mit der aktuellen Textur für diese Phase adressiert werden können, werden die überflüssigen Elemente ignoriert. Dies gilt auch, wenn 2D-Texturkoordinaten für eine 1D-Textur verwendet werden.

 

Weitere Informationen finden Sie in den folgenden Themen.

-   [Automatisch generierte Texturkoordinaten (Direct3D 9)](automatically-generated-texture-coordinates.md)
-   [Transformationen für Texturkoordinaten (Direct3D 9)](texture-coordinate-transformations.md)
-   [Besondere Effekte (Direct3D 9)](special-effects.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturkoordinaten](texture-coordinates.md)
</dt> </dl>

 

 
