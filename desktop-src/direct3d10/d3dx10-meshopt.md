---
description: Gibt den Typ der auszuführenden Mesh-Optimierung an.
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: D3DX10_MESHOPT-Enumeration (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESHOPT
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: c8ccb13da1549b7e2eeeb67ebf7899c2187be363
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355557"
---
# <a name="d3dx10_meshopt-enumeration"></a><span data-ttu-id="4c9d5-103">D3dx10 \_ meshopt-Enumeration</span><span class="sxs-lookup"><span data-stu-id="4c9d5-103">D3DX10\_MESHOPT enumeration</span></span>

<span data-ttu-id="4c9d5-104">Gibt den Typ der auszuführenden Mesh-Optimierung an.</span><span class="sxs-lookup"><span data-stu-id="4c9d5-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c9d5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c9d5-105">Syntax</span></span>


```C++
typedef enum D3DX10_MESHOPT { 
  D3DX10_MESHOPT_COMPACT             = 0x01000000,
  D3DX10_MESHOPT_ATTR_SORT           = 0x02000000,
  D3DX10_MESHOPT_VERTEX_CACHE        = 0x04000000,
  D3DX10_MESHOPT_STRIP_REORDER       = 0x08000000,
  D3DX10_MESHOPT_IGNORE_VERTS        = 0x10000000,
  D3DX10_MESHOPT_DO_NOT_SPLIT        = 0x20000000,
  D3DX10_MESHOPT_DEVICE_INDEPENDENT  = 0x00400000
} D3DX10_MESHOPT, *LPD3DX10_MESHOPT;
```



## <a name="constants"></a><span data-ttu-id="4c9d5-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="4c9d5-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4c9d5-107"><span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3dx10 \_ meshopt \_ Compact**</span><span class="sxs-lookup"><span data-stu-id="4c9d5-107"><span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10\_MESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="4c9d5-108">Ordnet Gesichter neu an, um nicht verwendete Vertices und Gesichter zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="4c9d5-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="4c9d5-109"><span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3dx10 \_ meshopt \_ attr \_ Sortieren**</span><span class="sxs-lookup"><span data-stu-id="4c9d5-109"><span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10\_MESHOPT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="4c9d5-110">Ordnet Gesichter neu an, um die Leistung zu verbessern und die Leistung des Attribut Bündel Zustands zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="4c9d5-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced DrawSubset performance.</span></span>

</dd> <dt>

<span data-ttu-id="4c9d5-111"><span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3dx10 \_ meshopt- \_ Scheitelpunkt \_ Cache**</span><span class="sxs-lookup"><span data-stu-id="4c9d5-111"><span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10\_MESHOPT\_VERTEX\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="4c9d5-112">Ordnet Gesichter neu an, um die Cache Treffer Rate von Vertex-Caches zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="4c9d5-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="4c9d5-113"><span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**D3dx10 \_ meshopt \_ Strip \_ neu anordnen**</span><span class="sxs-lookup"><span data-stu-id="4c9d5-113"><span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**D3DX10\_MESHOPT\_STRIP\_REORDER**</span></span>
</dt> <dd>

<span data-ttu-id="4c9d5-114">Ordnet Flächen neu an, um die Länge der angrenzenden Dreiecke zu maximieren</span><span class="sxs-lookup"><span data-stu-id="4c9d5-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="4c9d5-115"><span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3dx10 \_ meshopt \_ ignoriert \_**</span><span class="sxs-lookup"><span data-stu-id="4c9d5-115"><span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10\_MESHOPT\_IGNORE\_VERTS**</span></span>
</dt> <dd>

<span data-ttu-id="4c9d5-116">Nur Gesichter optimieren; Optimieren Sie die Vertices nicht.</span><span class="sxs-lookup"><span data-stu-id="4c9d5-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="4c9d5-117"><span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3dx10 \_ meshopt \_ \_ nicht \_ teilen**</span><span class="sxs-lookup"><span data-stu-id="4c9d5-117"><span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10\_MESHOPT\_DO\_NOT\_SPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="4c9d5-118">Bei der Attribut Sortierung werden Vertices, die von Attribut Gruppen gemeinsam verwendet werden, nicht aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="4c9d5-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="4c9d5-119"><span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3dx10 \_ meshopt- \_ Geräte \_ unabhängig**</span><span class="sxs-lookup"><span data-stu-id="4c9d5-119"><span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10\_MESHOPT\_DEVICE\_INDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="4c9d5-120">Wirkt sich auf die Scheitelpunkt Cache Größe aus.</span><span class="sxs-lookup"><span data-stu-id="4c9d5-120">Affects the vertex cache size.</span></span> <span data-ttu-id="4c9d5-121">Die Verwendung dieses Flags gibt eine Standard Cache Größe an, die auf Legacy Hardware gut funktioniert.</span><span class="sxs-lookup"><span data-stu-id="4c9d5-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c9d5-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c9d5-122">Remarks</span></span>

<span data-ttu-id="4c9d5-123">Die \_ Optimierungs Flags "D3DXMESHOPT stripreorder" und "D3DXMESHOPT \_ vertexcache" schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="4c9d5-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="4c9d5-124">Das \_ Flag D3DXMESHOPT sharevb wurde aus dieser Enumeration entfernt.</span><span class="sxs-lookup"><span data-stu-id="4c9d5-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="4c9d5-125">Verwenden Sie \_ stattdessen die D3DXMESH vb- \_ Freigabe in D3DXMESH.</span><span class="sxs-lookup"><span data-stu-id="4c9d5-125">Use D3DXMESH\_VB\_SHARE instead, in D3DXMESH.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c9d5-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c9d5-126">Requirements</span></span>



| <span data-ttu-id="4c9d5-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c9d5-127">Requirement</span></span> | <span data-ttu-id="4c9d5-128">Wert</span><span class="sxs-lookup"><span data-stu-id="4c9d5-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c9d5-129">Header</span><span class="sxs-lookup"><span data-stu-id="4c9d5-129">Header</span></span><br/> | <dl> <span data-ttu-id="4c9d5-130"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c9d5-130"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c9d5-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c9d5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c9d5-132">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="4c9d5-132">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




