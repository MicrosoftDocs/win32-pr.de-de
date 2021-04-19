---
description: Eine Dreiecks Liste ist eine Liste isolierter Dreiecke. Sie sind möglicherweise nah beieinander. Eine Dreiecks Liste muss mindestens drei Scheitel Punkte enthalten, und die Gesamtzahl der Scheitel Punkte muss von drei Scheitel Punkten unterschieden werden.
ms.assetid: e5c3470f-361c-458a-a42a-3549c51d8794
title: Dreiecks Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230cac9b4120d31821d70db022ab50d311d7b73e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346422"
---
# <a name="triangle-lists"></a><span data-ttu-id="69815-105">Dreiecks Listen</span><span class="sxs-lookup"><span data-stu-id="69815-105">Triangle Lists</span></span>

<span data-ttu-id="69815-106">Eine Dreiecks Liste ist eine Liste isolierter Dreiecke.</span><span class="sxs-lookup"><span data-stu-id="69815-106">A triangle list is a list of isolated triangles.</span></span> <span data-ttu-id="69815-107">Sie sind möglicherweise nah beieinander.</span><span class="sxs-lookup"><span data-stu-id="69815-107">They might or might not be near each other.</span></span> <span data-ttu-id="69815-108">Eine Dreiecks Liste muss mindestens drei Scheitel Punkte enthalten, und die Gesamtzahl der Scheitel Punkte muss von drei Scheitel Punkten unterschieden werden.</span><span class="sxs-lookup"><span data-stu-id="69815-108">A triangle list must have at least three vertices and the total number of vertices must be divisible by three.</span></span>

<span data-ttu-id="69815-109">Verwenden Sie Dreiecks Listen, um ein Objekt zu erstellen, das aus zusammenhängenden Teilen besteht.</span><span class="sxs-lookup"><span data-stu-id="69815-109">Use triangle lists to create an object that is composed of disjoint pieces.</span></span> <span data-ttu-id="69815-110">Beispielsweise besteht eine Möglichkeit zum Erstellen einer Force-Field-Wand in einem 3D-Spiel darin, eine große Liste kleiner, nicht verbundener Dreiecke anzugeben.</span><span class="sxs-lookup"><span data-stu-id="69815-110">For instance, one way to create a force-field wall in a 3D game is to specify a large list of small, unconnected triangles.</span></span> <span data-ttu-id="69815-111">Wenden Sie dann ein Material und eine Textur an, mit denen ein Licht an die Dreiecks Liste ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="69815-111">Then apply a material and texture that appears to emit light to the triangle list.</span></span> <span data-ttu-id="69815-112">Jedes Dreieck in der Wand scheint zu leuchten.</span><span class="sxs-lookup"><span data-stu-id="69815-112">Each triangle in the wall appears to glow.</span></span> <span data-ttu-id="69815-113">Die Szene hinter der Wand wird durch die Lücken zwischen den Dreiecken teilweise sichtbar, da ein Spieler bei der Betrachtung eines Force-Felds möglicherweise erwartet.</span><span class="sxs-lookup"><span data-stu-id="69815-113">The scene behind the wall becomes partially visible through the gaps between the triangles, as a player might expect when looking at a force field.</span></span>

<span data-ttu-id="69815-114">Dreiecks Listen können auch zum Erstellen primitiver Elemente mit Spitzen Kanten eingesetzt werden, die mit der Gouraud-Schattierung schattiert werden.</span><span class="sxs-lookup"><span data-stu-id="69815-114">Triangle lists are also useful for creating primitives that have sharp edges and are shaded with Gouraud shading.</span></span> <span data-ttu-id="69815-115">Siehe [Gesicht-und Scheitelpunkt normale Vektoren (Direct3D 9)](face-and-vertex-normal-vectors.md).</span><span class="sxs-lookup"><span data-stu-id="69815-115">See [Face and Vertex Normal Vectors (Direct3D 9)](face-and-vertex-normal-vectors.md).</span></span>

<span data-ttu-id="69815-116">Die folgende Abbildung zeigt eine gerenderte Dreiecks Liste.</span><span class="sxs-lookup"><span data-stu-id="69815-116">The following illustration depicts a rendered triangle list.</span></span>

![Abbildung einer gerenderten Dreiecks Liste](images/trilist.png)

<span data-ttu-id="69815-118">Der folgende Code zeigt, wie Vertices für diese Dreiecks Liste erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="69815-118">The following code shows how to create vertices for this triangle list.</span></span>


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



<span data-ttu-id="69815-119">Das folgende Codebeispiel zeigt, wie Sie diese Dreiecks Liste in Direct3D 9 mit [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)Renderern.</span><span class="sxs-lookup"><span data-stu-id="69815-119">The code example below shows how to render this triangle list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 2 );
```



<span data-ttu-id="69815-120">Sie können auch Dreieck Striche verwenden, um Dreiecke zu Renten, die nicht miteinander verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="69815-120">You can also use triangle strips to render triangles that are not connected to one another.</span></span> <span data-ttu-id="69815-121">Geben Sie hierzu ein degeneriertes Dreieck (d. h. ein Dreieck mit einer Größe von 0) in der Liste an. Dadurch wird eine Linie zwischen den beiden Dreiecken erstellt, die während des Renderings nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="69815-121">To do this, specify a degenerate triangle (that is, a triangle with zero size) in the list; this will create a line between the two triangles which will not appear during rendering.</span></span> <span data-ttu-id="69815-122">Um z. b. nur das erste und letzte Dreieck aus dem vorherigen Beispiel zu rendern, initialisieren Sie den Vertex-Puffer mit den folgenden Vertices:</span><span class="sxs-lookup"><span data-stu-id="69815-122">For example, to render only the first and last triangle from the previous example, initialize the vertex buffer with the following vertices:</span></span>


```
CUSTOMVERTEX Vertices[] =
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    { 5.0, -5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



## <a name="related-topics"></a><span data-ttu-id="69815-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="69815-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69815-124">Primitive</span><span class="sxs-lookup"><span data-stu-id="69815-124">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
