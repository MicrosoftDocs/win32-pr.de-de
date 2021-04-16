---
description: Ein Dreiecks Lüfter ähnelt einem Dreiecks Streifen, mit dem Unterschied, dass alle Dreiecke einen Scheitelpunkt gemeinsam verwenden, wie in der folgenden Abbildung dargestellt.
ms.assetid: a1fbfd78-121f-4f79-9ba8-44f23356a432
title: Dreiecks Lüfter (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2357af0d999cc759453e34cd278f61064a637cfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104555777"
---
# <a name="triangle-fans-direct3d-9"></a><span data-ttu-id="b4a2c-103">Dreiecks Lüfter (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b4a2c-103">Triangle Fans (Direct3D 9)</span></span>

<span data-ttu-id="b4a2c-104">Ein Dreiecks Lüfter ähnelt einem Dreiecks Streifen, mit dem Unterschied, dass alle Dreiecke einen Scheitelpunkt gemeinsam verwenden, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-104">A triangle fan is similar to a triangle strip, except that all the triangles share one vertex, as shown in the following illustration.</span></span>

![Abbildung eines Dreiecks Lüfters](images/trifan.gif)

<span data-ttu-id="b4a2c-106">Das System verwendet Vertices v2, v3 und v1, um das erste Dreieck zu zeichnen. v3, v4 und v1 zum Zeichnen des zweiten Dreiecks V4, V5 und v1 zum Zeichnen des dritten Dreiecks Und so weiter.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-106">The system uses vertices v2, v3, and v1 to draw the first triangle; v3, v4, and v1 to draw the second triangle; v4, v5, and v1 to draw the third triangle; and so on.</span></span> <span data-ttu-id="b4a2c-107">Wenn die flache Schattierung aktiviert ist, schattiert das System das Dreieck mit der Farbe seines ersten Scheitel Punkts.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-107">When flat shading is enabled, the system shades the triangle with the color from its first vertex.</span></span>

<span data-ttu-id="b4a2c-108">Die folgende Abbildung stellt einen gerenderten Dreiecks Lüfter dar.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-108">The following illustration depicts a rendered triangle fan.</span></span>

![Abbildung eines gerenderten Dreiecks Lüfters](images/tfan2.gif)

<span data-ttu-id="b4a2c-110">Der folgende Code zeigt, wie Vertices für diesen Dreiecks Lüfter erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-110">The following code shows how to create vertices for this triangle fan.</span></span>


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    { 0.0, 0.0, 0.0},
    {-5.0, 5.0, 0.0},
    {-3.0,  7.0, 0.0},
    { 0.0, 10.0, 0.0},
    { 3.0,  7.0, 0.0},
    { 5.0,  5.0, 0.0},
};
```



<span data-ttu-id="b4a2c-111">Das folgende Codebeispiel zeigt, wie Sie diesen Dreiecks Lüfter in Direct3D 9 mit [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)rendernen.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-111">The code example below shows how to render this triangle fan in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLEFAN, 0, 4 );
```



<span data-ttu-id="b4a2c-112">Dreiecks Lüfter werden in Direct3D 10 oder höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b4a2c-112">Triangle fans are not supported in Direct3D 10 or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4a2c-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b4a2c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4a2c-114">Primitive</span><span class="sxs-lookup"><span data-stu-id="b4a2c-114">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
