---
description: Eine Punkt Liste ist eine Sammlung von Vertices, die als isolierte Punkte gerendert werden. Die Anwendung kann Sie in 3D-Szenen für sternfelder oder gepunktete Linien auf der Oberfläche eines Polygons verwenden.
ms.assetid: 82866b07-5043-433f-974a-0a301d4b5491
title: Punkt Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57086a445209d9e60173910e07166a6149e0b8d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746777"
---
# <a name="point-lists"></a><span data-ttu-id="a929a-104">Punkt Listen</span><span class="sxs-lookup"><span data-stu-id="a929a-104">Point Lists</span></span>

<span data-ttu-id="a929a-105">Eine Punkt Liste ist eine Sammlung von Vertices, die als isolierte Punkte gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="a929a-105">A point list is a collection of vertices that are rendered as isolated points.</span></span> <span data-ttu-id="a929a-106">Die Anwendung kann Sie in 3D-Szenen für sternfelder oder gepunktete Linien auf der Oberfläche eines Polygons verwenden.</span><span class="sxs-lookup"><span data-stu-id="a929a-106">Your application can use them in 3D scenes for star fields, or dotted lines on the surface of a polygon.</span></span>

<span data-ttu-id="a929a-107">In der folgenden Abbildung wird eine Liste gerenderter Punkte dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a929a-107">The following illustration depicts a rendered point list.</span></span>

![Abbildung einer Punkt Liste](images/pointlst.png)

<span data-ttu-id="a929a-109">Die Anwendung kann Materialien und Texturen auf eine Punkt Liste anwenden.</span><span class="sxs-lookup"><span data-stu-id="a929a-109">Your application can apply materials and textures to a point list.</span></span> <span data-ttu-id="a929a-110">Die Farben in dem Material oder der Textur werden nur an den Punkten angezeigt, die gezeichnet werden, und nicht an einer beliebigen Stelle zwischen den Punkten.</span><span class="sxs-lookup"><span data-stu-id="a929a-110">The colors in the material or texture appear only at the points drawn, and not anywhere between the points.</span></span>

<span data-ttu-id="a929a-111">Der folgende Code zeigt, wie Scheitel Punkte für diese Punkt Liste erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a929a-111">The following code shows how to create vertices for this point list.</span></span>


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



<span data-ttu-id="a929a-112">Das folgende Codebeispiel zeigt, wie Sie diese Punkt Liste in Direct3D 9 mit [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)Rendering.</span><span class="sxs-lookup"><span data-stu-id="a929a-112">The code example below shows how to render this point list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_POINTLIST, 0, 6 );
```



## <a name="related-topics"></a><span data-ttu-id="a929a-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a929a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a929a-114">Primitive</span><span class="sxs-lookup"><span data-stu-id="a929a-114">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
