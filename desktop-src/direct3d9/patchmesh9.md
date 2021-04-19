---
description: Definiert ein Mesh, das von Bézier-Patches definiert wird. Das erste Array ist eine Liste von Vertices, und das zweite Array definiert die Patches für das Mesh, indem es in das vertexarray indiziert wird.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b3d8232fe8c83358feb216acfb45a7877d7acb9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338886"
---
# <a name="patchmesh9"></a><span data-ttu-id="35af2-104">PatchMesh9</span><span class="sxs-lookup"><span data-stu-id="35af2-104">PatchMesh9</span></span>

<span data-ttu-id="35af2-105">Definiert ein Mesh, das von Bézier-Patches definiert wird.</span><span class="sxs-lookup"><span data-stu-id="35af2-105">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="35af2-106">Das erste Array ist eine Liste von Vertices, und das zweite Array definiert die Patches für das Mesh, indem es in das vertexarray indiziert wird.</span><span class="sxs-lookup"><span data-stu-id="35af2-106">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

``` syntax
template PatchMesh9
{
    < B9EC94E1-B9A6-4251-BA18-94893F02C0EA >
    DWORD Type;
    DWORD Degree;
    DWORD Basis;
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
} 
```

<span data-ttu-id="35af2-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="35af2-107">Where:</span></span>

-   <span data-ttu-id="35af2-108">Typ-patchmesh-Typ: Rechteck, Dreieck oder N-Patch.</span><span class="sxs-lookup"><span data-stu-id="35af2-108">Type - Patch mesh type: rectangle, triangle, or N-patch.</span></span>
-   <span data-ttu-id="35af2-109">Grad-Grad der Variablen in der Kurven Gleichung.</span><span class="sxs-lookup"><span data-stu-id="35af2-109">Degree - Degree of the variables in the curve equation.</span></span>
-   <span data-ttu-id="35af2-110">Der Grund für den Typ einer hochwertigen patchoberfläche.</span><span class="sxs-lookup"><span data-stu-id="35af2-110">Basis - Basis type of a high-order patch surface.</span></span>
-   <span data-ttu-id="35af2-111">nvertices-Anzahl der Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="35af2-111">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="35af2-112">Vertices \[ nvertices \] -Array von Vertices.</span><span class="sxs-lookup"><span data-stu-id="35af2-112">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="35af2-113">Siehe [**Vektor**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="35af2-113">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="35af2-114">npatches-Anzahl der Patches.</span><span class="sxs-lookup"><span data-stu-id="35af2-114">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="35af2-115">Patches \[ npatches \] -Array von Patches.</span><span class="sxs-lookup"><span data-stu-id="35af2-115">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="35af2-116">Siehe [**Patch**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="35af2-116">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="35af2-117">\[ ... \] -Eine beliebige x-Datei Vorlage kann hier verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="35af2-117">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="35af2-118">Dadurch wird die Architektur erweiterbar.</span><span class="sxs-lookup"><span data-stu-id="35af2-118">This makes the architecture extensible.</span></span>

<span data-ttu-id="35af2-119">Die Patches verwenden die Scheitel Punkte im Array von Vertices als Steuerungs Punkte für die einzelnen Patches.</span><span class="sxs-lookup"><span data-stu-id="35af2-119">The patches use the vertices in the array of vertices as the control points for each patch.</span></span>

## <a name="see-also"></a><span data-ttu-id="35af2-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35af2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35af2-121">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="35af2-121">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



