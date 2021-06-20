---
description: PatchMesh9 definiert ein durch Bézierpatches definiertes Gitternetz, einschließlich einer Liste von Scheitelpunkte und patches für das Gitternetz durch Indizierung im Scheitelpunktarray.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811e593117f2ec57a4718ea8078d96bcea87e71f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404703"
---
# <a name="patchmesh9"></a><span data-ttu-id="e6232-103">PatchMesh9</span><span class="sxs-lookup"><span data-stu-id="e6232-103">PatchMesh9</span></span>

<span data-ttu-id="e6232-104">Definiert ein durch Bézierpatches definiertes Gitternetz.</span><span class="sxs-lookup"><span data-stu-id="e6232-104">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="e6232-105">Das erste Array ist eine Liste von Scheitelpunkte, und das zweite Array definiert die Patches für das Gitternetz durch Indizierung in das Scheitelpunktarray.</span><span class="sxs-lookup"><span data-stu-id="e6232-105">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

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

<span data-ttu-id="e6232-106">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="e6232-106">Where:</span></span>

-   <span data-ttu-id="e6232-107">Typ: Patchgitternetztyp: Rechteck, Dreieck oder N-Patch.</span><span class="sxs-lookup"><span data-stu-id="e6232-107">Type - Patch mesh type: rectangle, triangle, or N-patch.</span></span>
-   <span data-ttu-id="e6232-108">Degree: Grad der Variablen in der Kurvengleichung.</span><span class="sxs-lookup"><span data-stu-id="e6232-108">Degree - Degree of the variables in the curve equation.</span></span>
-   <span data-ttu-id="e6232-109">Basis: Basistyp einer hochwertigen Patchoberfläche.</span><span class="sxs-lookup"><span data-stu-id="e6232-109">Basis - Basis type of a high-order patch surface.</span></span>
-   <span data-ttu-id="e6232-110">nVertices: Anzahl der Scheitelzeichen.</span><span class="sxs-lookup"><span data-stu-id="e6232-110">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="e6232-111">sctices \[ nVertices \] : Array von Scheiteltices.</span><span class="sxs-lookup"><span data-stu-id="e6232-111">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="e6232-112">Siehe [**Vektor**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="e6232-112">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="e6232-113">nPatches: Anzahl der Patches.</span><span class="sxs-lookup"><span data-stu-id="e6232-113">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="e6232-114">patches \[ nPatches: \] Array von Patches.</span><span class="sxs-lookup"><span data-stu-id="e6232-114">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="e6232-115">Weitere Informationen [**finden Sie unter Patchen von**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="e6232-115">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="e6232-116">\[ ... \] – Hier kann eine beliebige X-Dateivorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6232-116">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="e6232-117">Dadurch wird die Architektur erweiterbar.</span><span class="sxs-lookup"><span data-stu-id="e6232-117">This makes the architecture extensible.</span></span>

<span data-ttu-id="e6232-118">Die Patches verwenden die Scheitelpunkte im Array von Scheitelpunkten als Kontrollpunkte für jeden Patch.</span><span class="sxs-lookup"><span data-stu-id="e6232-118">The patches use the vertices in the array of vertices as the control points for each patch.</span></span>

## <a name="see-also"></a><span data-ttu-id="e6232-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6232-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6232-120">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="e6232-120">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



