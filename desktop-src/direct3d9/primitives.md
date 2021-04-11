---
description: Ein 3D-primitiv ist eine Sammlung von Vertices, die eine einzelne 3D-Entität bilden. Das einfachste primitive ist eine Auflistung von Punkten in einem 3D-Koordinatensystem, das als Punkt Liste bezeichnet wird.
ms.assetid: vs|directx_sdk|~\primitives.htm
title: Primitive (Direct3D 9-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38916e85add69574a2437b0e48c209b14a341e44
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123433"
---
# <a name="primitives-direct3d-9-graphics"></a><span data-ttu-id="5cedd-104">Primitive (Direct3D 9-Grafiken)</span><span class="sxs-lookup"><span data-stu-id="5cedd-104">Primitives (Direct3D 9 Graphics)</span></span>

<span data-ttu-id="5cedd-105">Ein 3D-primitiv ist eine Sammlung von Vertices, die eine einzelne 3D-Entität bilden.</span><span class="sxs-lookup"><span data-stu-id="5cedd-105">A 3D primitive is a collection of vertices that form a single 3D entity.</span></span> <span data-ttu-id="5cedd-106">Das einfachste primitive ist eine Auflistung von Punkten in einem 3D-Koordinatensystem, das als Punkt Liste bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="5cedd-106">The simplest primitive is a collection of points in a 3D coordinate system, which is called a point list.</span></span>

<span data-ttu-id="5cedd-107">Häufig sind 3D-primitive Polygone.</span><span class="sxs-lookup"><span data-stu-id="5cedd-107">Often, 3D primitives are polygons.</span></span> <span data-ttu-id="5cedd-108">Ein Polygon ist eine geschlossene 3D-Abbildung, die durch mindestens drei Vertices getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="5cedd-108">A polygon is a closed 3D figure delineated by at least three vertices.</span></span> <span data-ttu-id="5cedd-109">Das einfachste Polygon ist ein Dreieck.</span><span class="sxs-lookup"><span data-stu-id="5cedd-109">The simplest polygon is a triangle.</span></span> <span data-ttu-id="5cedd-110">Microsoft Direct3D verwendet Dreiecke, um die meisten Polygone zu verfassen, da alle drei Scheitel Punkte in einem Dreieck vollständig Coplanar sind.</span><span class="sxs-lookup"><span data-stu-id="5cedd-110">Microsoft Direct3D uses triangles to compose most of its polygons because all three vertices in a triangle are guaranteed to be coplanar.</span></span> <span data-ttu-id="5cedd-111">Das Rendern von nicht planaren Vertices ist ineffizient.</span><span class="sxs-lookup"><span data-stu-id="5cedd-111">Rendering nonplanar vertices is inefficient.</span></span> <span data-ttu-id="5cedd-112">Dreiecke können kombiniert werden, um große, komplexe Polygone und Netze zu bilden.</span><span class="sxs-lookup"><span data-stu-id="5cedd-112">You can combine triangles to form large, complex polygons and meshes.</span></span>

<span data-ttu-id="5cedd-113">In der folgenden Abbildung ist ein Cube dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5cedd-113">The following illustration shows a cube.</span></span> <span data-ttu-id="5cedd-114">Zwei Dreiecke bilden jedes Gesicht des Cubes.</span><span class="sxs-lookup"><span data-stu-id="5cedd-114">Two triangles form each face of the cube.</span></span> <span data-ttu-id="5cedd-115">Der gesamte Satz von Dreiecken bildet einen kubischen primitiven.</span><span class="sxs-lookup"><span data-stu-id="5cedd-115">The entire set of triangles forms one cubic primitive.</span></span> <span data-ttu-id="5cedd-116">Sie können Texturen und Materialien auf die Oberflächen von primitiven anwenden, damit Sie als ein einzelnes voll solides Formular angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5cedd-116">You can apply textures and materials to the surfaces of primitives to make them appear to be a single solid form.</span></span> <span data-ttu-id="5cedd-117">Weitere Informationen finden Sie unter [Material (Direct3D 9)](materials.md) and [Direct3D Texturen (Direct3D 9)](direct3d-textures.md).</span><span class="sxs-lookup"><span data-stu-id="5cedd-117">For details, see [Materials (Direct3D 9)](materials.md) and [Direct3D Textures (Direct3D 9)](direct3d-textures.md).</span></span>

![Abbildung eines Cubes mit zwei Dreiecken auf jeder Seite](images/cube3d.png)

<span data-ttu-id="5cedd-119">Sie können auch Dreiecke verwenden, um primitive zu erstellen, deren Oberflächen als glatte Kurven angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5cedd-119">You can also use triangles to create primitives whose surfaces appear to be smooth curves.</span></span> <span data-ttu-id="5cedd-120">In der folgenden Abbildung wird gezeigt, wie eine Kugel mit Dreiecken simuliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="5cedd-120">The following illustration shows how a sphere can be simulated with triangles.</span></span> <span data-ttu-id="5cedd-121">Nachdem ein Material angewendet wurde, wird die Kugel beim Rendern gerendert.</span><span class="sxs-lookup"><span data-stu-id="5cedd-121">After a material is applied, the sphere looks curved when it is rendered.</span></span> <span data-ttu-id="5cedd-122">Dies gilt insbesondere, wenn Sie die Verwendung von Gouraud-Schattierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="5cedd-122">This is especially true if you use Gouraud shading.</span></span> <span data-ttu-id="5cedd-123">Weitere Informationen finden Sie unter [Gouraud-Schattierung](shading-modes.md).</span><span class="sxs-lookup"><span data-stu-id="5cedd-123">For details, see [Gouraud Shading](shading-modes.md).</span></span>

![Abbildung einer Kugel, die mithilfe von Dreiecken simuliert wird](images/sphere3d.png)

<span data-ttu-id="5cedd-125">Direct3D-Geräte können die folgenden Typen von primitiven erstellen und bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="5cedd-125">Direct3D devices can create and manipulate the following types of primitives.</span></span>

-   [<span data-ttu-id="5cedd-126">Punkt Listen</span><span class="sxs-lookup"><span data-stu-id="5cedd-126">Point Lists</span></span>](point-lists.md)
-   [<span data-ttu-id="5cedd-127">Linien Listen</span><span class="sxs-lookup"><span data-stu-id="5cedd-127">Line Lists</span></span>](line-lists.md)
-   [<span data-ttu-id="5cedd-128">Zeilen Streifen</span><span class="sxs-lookup"><span data-stu-id="5cedd-128">Line Strips</span></span>](line-strips.md)
-   [<span data-ttu-id="5cedd-129">Dreiecks Listen</span><span class="sxs-lookup"><span data-stu-id="5cedd-129">Triangle Lists</span></span>](triangle-lists.md)
-   [<span data-ttu-id="5cedd-130">Dreiecks Streifen</span><span class="sxs-lookup"><span data-stu-id="5cedd-130">Triangle Strips</span></span>](triangle-strips.md)
-   [<span data-ttu-id="5cedd-131">Dreiecks Lüfter (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5cedd-131">Triangle Fans (Direct3D 9)</span></span>](triangle-fans.md)

<span data-ttu-id="5cedd-132">Sie können primitive Typen aus einer C++-Anwendung mit einer beliebigen Renderingmethode der [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle rendern.</span><span class="sxs-lookup"><span data-stu-id="5cedd-132">You can render primitive types from a C++ application with any of the rendering methods of the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cedd-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5cedd-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cedd-134">Direct3D-Geräte</span><span class="sxs-lookup"><span data-stu-id="5cedd-134">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
