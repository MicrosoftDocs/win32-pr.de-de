---
description: Ein Zeilen Streifen ist ein primitiver, der aus verbundenen Liniensegmenten besteht.
ms.assetid: 73905718-a4c6-4f73-beef-4cccac7eea8c
title: Zeilen Streifen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dee7eb79b583ad04dc0ed576a7d9426e8dda9fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521952"
---
# <a name="line-strips"></a><span data-ttu-id="8de9f-103">Zeilen Streifen</span><span class="sxs-lookup"><span data-stu-id="8de9f-103">Line Strips</span></span>

<span data-ttu-id="8de9f-104">Ein Zeilen Streifen ist ein primitiver, der aus verbundenen Liniensegmenten besteht.</span><span class="sxs-lookup"><span data-stu-id="8de9f-104">A line strip is a primitive that is composed of connected line segments.</span></span> <span data-ttu-id="8de9f-105">Die Anwendung kann Zeilen Streifen zum Erstellen von Polygonen verwenden, die nicht geschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="8de9f-105">Your application can use line strips for creating polygons that are not closed.</span></span> <span data-ttu-id="8de9f-106">Ein geschlossenes Polygon ist ein Polygon, dessen letzter Scheitelpunkt durch ein Liniensegment mit dem ersten Scheitelpunkt verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="8de9f-106">A closed polygon is a polygon whose last vertex is connected to its first vertex by a line segment.</span></span> <span data-ttu-id="8de9f-107">Wenn Ihre Anwendung Polygone auf Basis von Zeilen Streifen erstellt, sind die Scheitel Punkte nicht garantiert Coplanar.</span><span class="sxs-lookup"><span data-stu-id="8de9f-107">If your application makes polygons based on line strips, the vertices are not guaranteed to be coplanar.</span></span>

<span data-ttu-id="8de9f-108">Die folgende Abbildung zeigt einen gerenderten Zeilen Streifen.</span><span class="sxs-lookup"><span data-stu-id="8de9f-108">The following illustration shows a rendered line strip.</span></span>

![Abbildung eines Zeilen Streifens](images/linstrip.gif)

<span data-ttu-id="8de9f-110">Der folgende Code zeigt, wie Vertices für diesen Zeilen Streifen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8de9f-110">The following code shows how to create vertices for this line strip.</span></span>


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



<span data-ttu-id="8de9f-111">Das folgende Codebeispiel zeigt, wie Sie einen Zeilen Streifen in Direct3D 9 mit [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) Renderern.</span><span class="sxs-lookup"><span data-stu-id="8de9f-111">The code example below shows how to render a line strip in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINESTRIP, 0, 5 );
```



## <a name="related-topics"></a><span data-ttu-id="8de9f-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8de9f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8de9f-113">Primitive</span><span class="sxs-lookup"><span data-stu-id="8de9f-113">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
