---
description: Ein Dreiecks Streifen ist eine Reihe verbundener Dreiecke.
ms.assetid: 3923c570-47a4-4b53-a097-731981380ae0
title: Dreiecks Streifen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2766529a37b994e5fe30815ca6300476f06c7d4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104556171"
---
# <a name="triangle-strips"></a><span data-ttu-id="124b3-103">Dreiecks Streifen</span><span class="sxs-lookup"><span data-stu-id="124b3-103">Triangle Strips</span></span>

<span data-ttu-id="124b3-104">Ein Dreiecks Streifen ist eine Reihe verbundener Dreiecke.</span><span class="sxs-lookup"><span data-stu-id="124b3-104">A triangle strip is a series of connected triangles.</span></span> <span data-ttu-id="124b3-105">Da die Dreiecke verbunden ist, muss die Anwendung nicht wiederholt alle drei Scheitel Punkte für jedes Dreieck angeben.</span><span class="sxs-lookup"><span data-stu-id="124b3-105">Because the triangles are connected, the application does not need to repeatedly specify all three vertices for each triangle.</span></span> <span data-ttu-id="124b3-106">Beispielsweise benötigen Sie nur sieben Scheitel Punkte, um den folgenden Dreieck Streifen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="124b3-106">For example, you need only seven vertices to define the following triangle strip.</span></span>

![Abbildung eines Dreiecks Streifens mit sieben Vertices](images/tristrip.png)

<span data-ttu-id="124b3-108">Das System verwendet Vertices v1, v2 und V3 zum Zeichnen des ersten Dreiecks. v2, v4 und V3 zum Zeichnen des zweiten Dreiecks. v3, v4 und V5 zum Zeichnen des dritten. V4, V6 und V5 zum Zeichnen des vierten; Und so weiter.</span><span class="sxs-lookup"><span data-stu-id="124b3-108">The system uses vertices v1, v2, and v3 to draw the first triangle; v2, v4, and v3 to draw the second triangle; v3, v4, and v5 to draw the third; v4, v6, and v5 to draw the fourth; and so on.</span></span> <span data-ttu-id="124b3-109">Beachten Sie, dass die Scheitel Punkte des zweiten und vierten Dreiecke nicht in der richtigen Reihenfolge sind. Dies ist erforderlich, um sicherzustellen, dass alle Dreiecke in einer Ausrichtung im Uhrzeigersinn gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="124b3-109">Notice that the vertices of the second and fourth triangles are out of order; this is required to make sure that all the triangles are drawn in a clockwise orientation.</span></span>

<span data-ttu-id="124b3-110">Die meisten Objekte in 3D-Szenen bestehen aus Dreiecks Streifen.</span><span class="sxs-lookup"><span data-stu-id="124b3-110">Most objects in 3D scenes are composed of triangle strips.</span></span> <span data-ttu-id="124b3-111">Dies liegt daran, dass mithilfe von Dreiecks Streifen komplexe Objekte auf eine Weise festgelegt werden können, die die Speicher-und Verarbeitungszeit effizient verwendet.</span><span class="sxs-lookup"><span data-stu-id="124b3-111">This is because triangle strips can be used to specify complex objects in a way that makes efficient use of memory and processing time.</span></span>

<span data-ttu-id="124b3-112">In der folgenden Abbildung ist ein gerenderter Dreiecks Streifen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="124b3-112">The following illustration depicts a rendered triangle strip.</span></span>

![Abbildung eines gerenderten Dreiecks Streifens](images/tstrip2.png)

<span data-ttu-id="124b3-114">Der folgende Code zeigt, wie Scheitel Punkte für diesen Dreiecks Streifen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="124b3-114">The following code shows how to create vertices for this triangle strip.</span></span>


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



<span data-ttu-id="124b3-115">Das folgende Codebeispiel zeigt, wie Sie diesen Dreiecks Streifen in Direct3D 9 mit [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)Renderern.</span><span class="sxs-lookup"><span data-stu-id="124b3-115">The code example below shows how to render this triangle strip in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 4);
```



<span data-ttu-id="124b3-116">Verwenden Sie einen Dreiecks Streifen, um Dreiecke zu Renten, die nicht miteinander verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="124b3-116">Use a triangle strip to render triangles that are not connected to one another.</span></span> <span data-ttu-id="124b3-117">Geben Sie zu diesem Zweck ein degeneriertes Dreieck (d. h. ein Dreieck, dessen Bereich NULL ist) in der Dreiecks Liste an.</span><span class="sxs-lookup"><span data-stu-id="124b3-117">To do this, specify a degenerate triangle (that is, a triangle whose area is zero) in the triangle list.</span></span> <span data-ttu-id="124b3-118">Dadurch wird eine Linie zwischen den beiden Dreiecken erstellt, die nicht dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="124b3-118">This creates a line between the two triangles which will not render.</span></span> <span data-ttu-id="124b3-119">Um nur den ersten und den letzten Dreiecke aus dem vorherigen Beispiel zu erstellen, ändern Sie den Vertex-Puffer, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="124b3-119">To render only the first and last triangles from the previous example, modify the vertex buffer as shown here:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="124b3-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="124b3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="124b3-121">Primitive</span><span class="sxs-lookup"><span data-stu-id="124b3-121">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
