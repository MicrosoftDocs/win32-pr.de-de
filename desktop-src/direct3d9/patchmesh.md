---
description: Definiert ein Mesh, das von Bézier-Patches definiert wird. Das erste Array ist eine Liste von Vertices, und das zweite Array definiert die Patches für das Mesh, indem es in das vertexarray indiziert wird.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: Patchmesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcdefac9799736c796aef7cbb7222ab1942540d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520891"
---
# <a name="patchmesh"></a><span data-ttu-id="c0497-104">Patchmesh</span><span class="sxs-lookup"><span data-stu-id="c0497-104">PatchMesh</span></span>

<span data-ttu-id="c0497-105">Definiert ein Mesh, das von Bézier-Patches definiert wird.</span><span class="sxs-lookup"><span data-stu-id="c0497-105">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="c0497-106">Das erste Array ist eine Liste von Vertices, und das zweite Array definiert die Patches für das Mesh, indem es in das vertexarray indiziert wird.</span><span class="sxs-lookup"><span data-stu-id="c0497-106">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

``` syntax
template PatchMesh
{
    < D02C95CC-EDBA-4305-9B5D-1820D7704BBF >
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
}
```

<span data-ttu-id="c0497-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="c0497-107">Where:</span></span>

-   <span data-ttu-id="c0497-108">nvertices-Anzahl der Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="c0497-108">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="c0497-109">Vertices \[ nvertices \] -Array von Vertices.</span><span class="sxs-lookup"><span data-stu-id="c0497-109">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="c0497-110">Siehe [**Vektor**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="c0497-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="c0497-111">npatches-Anzahl der Patches.</span><span class="sxs-lookup"><span data-stu-id="c0497-111">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="c0497-112">Patches \[ npatches \] -Array von Patches.</span><span class="sxs-lookup"><span data-stu-id="c0497-112">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="c0497-113">Siehe [**Patch**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="c0497-113">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="c0497-114">\[ ... \] -Eine beliebige x-Datei Vorlage kann hier verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0497-114">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="c0497-115">Dadurch wird die Architektur erweiterbar.</span><span class="sxs-lookup"><span data-stu-id="c0497-115">This makes the architecture extensible.</span></span>

<span data-ttu-id="c0497-116">Die Patches verwenden die Scheitel Punkte im Array von Vertices als Steuerungs Punkte für die einzelnen Patches.</span><span class="sxs-lookup"><span data-stu-id="c0497-116">The patches use the vertices in the array of vertices as the control points for each patch.</span></span> <span data-ttu-id="c0497-117">Dies ist eine Legacy Vorlage.</span><span class="sxs-lookup"><span data-stu-id="c0497-117">This is a legacy template.</span></span> <span data-ttu-id="c0497-118">Die neueste patchmesh-Vorlage ist [**PatchMesh9**](patchmesh9.md).</span><span class="sxs-lookup"><span data-stu-id="c0497-118">The latest patch mesh template is [**PatchMesh9**](patchmesh9.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c0497-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0497-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0497-120">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="c0497-120">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



