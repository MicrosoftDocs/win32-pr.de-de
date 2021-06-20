---
description: PatchMesh definiert ein Gitternetz, das von Bézierpatches definiert wird, einschließlich einer Liste von Scheitelpunkte und patches für das Gitternetz durch Indizierung in das Scheitelpunktarray.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabb3846246c7fb76a7146baf0b30bd9730fe24b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404713"
---
# <a name="patchmesh"></a><span data-ttu-id="ff6eb-103">PatchMesh</span><span class="sxs-lookup"><span data-stu-id="ff6eb-103">PatchMesh</span></span>

<span data-ttu-id="ff6eb-104">Definiert ein durch Bézierpatches definiertes Gitternetz.</span><span class="sxs-lookup"><span data-stu-id="ff6eb-104">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="ff6eb-105">Das erste Array ist eine Liste von Scheitelpunkte, und das zweite Array definiert die Patches für das Gitternetz durch Indizierung in das Scheitelpunktarray.</span><span class="sxs-lookup"><span data-stu-id="ff6eb-105">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

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

<span data-ttu-id="ff6eb-106">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="ff6eb-106">Where:</span></span>

-   <span data-ttu-id="ff6eb-107">nVertices: Anzahl der Scheitelzeichen.</span><span class="sxs-lookup"><span data-stu-id="ff6eb-107">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="ff6eb-108">sctices \[ nVertices \] : Array von Scheiteltices.</span><span class="sxs-lookup"><span data-stu-id="ff6eb-108">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="ff6eb-109">Siehe [**Vektor**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="ff6eb-109">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="ff6eb-110">nPatches: Anzahl der Patches.</span><span class="sxs-lookup"><span data-stu-id="ff6eb-110">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="ff6eb-111">patches \[ nPatches: \] Array von Patches.</span><span class="sxs-lookup"><span data-stu-id="ff6eb-111">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="ff6eb-112">Weitere Informationen [**finden Sie unter Patchen von**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="ff6eb-112">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="ff6eb-113">\[ ... \] – Hier kann eine beliebige X-Dateivorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff6eb-113">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="ff6eb-114">Dadurch wird die Architektur erweiterbar.</span><span class="sxs-lookup"><span data-stu-id="ff6eb-114">This makes the architecture extensible.</span></span>

<span data-ttu-id="ff6eb-115">Die Patches verwenden die Scheitelpunkte im Array von Scheitelpunkten als Kontrollpunkte für jeden Patch.</span><span class="sxs-lookup"><span data-stu-id="ff6eb-115">The patches use the vertices in the array of vertices as the control points for each patch.</span></span> <span data-ttu-id="ff6eb-116">Dies ist eine Legacyvorlage.</span><span class="sxs-lookup"><span data-stu-id="ff6eb-116">This is a legacy template.</span></span> <span data-ttu-id="ff6eb-117">Die neueste Patch mesh-Vorlage ist [**PatchMesh9.**](patchmesh9.md)</span><span class="sxs-lookup"><span data-stu-id="ff6eb-117">The latest patch mesh template is [**PatchMesh9**](patchmesh9.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ff6eb-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff6eb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff6eb-119">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="ff6eb-119">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



