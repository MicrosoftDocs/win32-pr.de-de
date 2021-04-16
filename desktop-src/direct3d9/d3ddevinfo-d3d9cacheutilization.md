---
description: Messen Sie die Leistung der Cache-Treffer Rate für Texturen und indizierte Vertices.
ms.assetid: 70bc4e93-0a34-485b-bdcc-028c24b52f62
title: D3DDEVINFO_D3D9CACHEUTILIZATION-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9CACHEUTILIZATION
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 94f77549d0ea2a9c59d7de8367a6133085cc2771
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530866"
---
# <a name="d3ddevinfo_d3d9cacheutilization-structure"></a><span data-ttu-id="1b77b-103">D3DDEVINFO \_ D3D9CACHEUTILIZATION-Struktur</span><span class="sxs-lookup"><span data-stu-id="1b77b-103">D3DDEVINFO\_D3D9CACHEUTILIZATION structure</span></span>

<span data-ttu-id="1b77b-104">Messen Sie die Leistung der Cache-Treffer Rate für Texturen und indizierte Vertices.</span><span class="sxs-lookup"><span data-stu-id="1b77b-104">Measure the cache hit rate performance for textures and indexed vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b77b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b77b-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9CACHEUTILIZATION {
  FLOAT TextureCacheHitRate;
  FLOAT PostTransformVertexCacheHitRate;
} D3DDEVINFO_D3D9CACHEUTILIZATION, *LPD3DDEVINFO_D3D9CACHEUTILIZATION;
```



## <a name="members"></a><span data-ttu-id="1b77b-106">Member</span><span class="sxs-lookup"><span data-stu-id="1b77b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1b77b-107">**Texturecachehitrate**</span><span class="sxs-lookup"><span data-stu-id="1b77b-107">**TextureCacheHitRate**</span></span>
</dt> <dd>

<span data-ttu-id="1b77b-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b77b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1b77b-109">Die Treffer Rate zum Ermitteln einer Textur im Textur Cache.</span><span class="sxs-lookup"><span data-stu-id="1b77b-109">The hit rate for finding a texture in the texture cache.</span></span> <span data-ttu-id="1b77b-110">Dabei wird davon ausgegangen, dass ein Textur Cache vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1b77b-110">This assumes there is a texture cache.</span></span> <span data-ttu-id="1b77b-111">Das Erhöhen der Detailebene für die Verwendung der detaillierteren Textur mit vielen großen Texturen oder das Erzeugen eines near Random Texture-Zugriffs Musters für große Texturen mit benutzerdefiniertem shadercode kann die Treffer Rate des Textur Caches erheblich beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="1b77b-111">Increasing the level-of-detail bias to use the most detailed texture, using many large textures, or producing a near random texture access pattern on large textures with custom shader code can dramatically affect the texture cache hit rate.</span></span>

</dd> <dt>

<span data-ttu-id="1b77b-112">**Posttransformvertexcachehitrate**</span><span class="sxs-lookup"><span data-stu-id="1b77b-112">**PostTransformVertexCacheHitRate**</span></span>
</dt> <dd>

<span data-ttu-id="1b77b-113">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b77b-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1b77b-114">Die Treffer Rate zum Suchen transformier ender Scheitel Punkte im Scheitelpunkt Cache.</span><span class="sxs-lookup"><span data-stu-id="1b77b-114">The hit rate for finding transformed vertices in the vertex cache.</span></span> <span data-ttu-id="1b77b-115">Die GPU ist so konzipiert, dass Sie indizierte Scheitel Punkte transformiert und Sie möglicherweise in einem Scheitelpunkt Cache speichert.</span><span class="sxs-lookup"><span data-stu-id="1b77b-115">The GPU is designed to transform indexed vertices and may store them in a vertex cache.</span></span> <span data-ttu-id="1b77b-116">Wenn Sie Meshes verwenden, kann [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) oder [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) zu einer besseren Vertex-Cache Auslastung führen.</span><span class="sxs-lookup"><span data-stu-id="1b77b-116">If you are using meshes, [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) or [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) may result in better vertex cache utilization.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b77b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b77b-117">Remarks</span></span>

<span data-ttu-id="1b77b-118">Ein effizienter Cache liegt in der Regel bei einer Treffer Rate von 90 Prozent, und ein ineffizienter Cache liegt in der Regel bei einer Trefferquote von 10 Prozent (obwohl ein niedriger Prozentsatz nicht unbedingt ein Problem darstellt).</span><span class="sxs-lookup"><span data-stu-id="1b77b-118">An efficient cache is typically closer to a 90 percent hit rate, and an inefficient cache is typically closer to a 10 percent hit rate (although a low percentage is not necessarily a problem).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b77b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b77b-119">Requirements</span></span>



| <span data-ttu-id="1b77b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b77b-120">Requirement</span></span> | <span data-ttu-id="1b77b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1b77b-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b77b-122">Header</span><span class="sxs-lookup"><span data-stu-id="1b77b-122">Header</span></span><br/> | <dl> <span data-ttu-id="1b77b-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b77b-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b77b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b77b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b77b-125">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="1b77b-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="1b77b-126">**GetData**</span><span class="sxs-lookup"><span data-stu-id="1b77b-126">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
