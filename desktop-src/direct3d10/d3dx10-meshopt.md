---
description: 'D3DX10_MESHOPT Enumeration: Gibt den Typ der durchzuführenden Gitternetzoptimierung an.'
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: D3DX10_MESHOPT -Enumeration (D3DX10Mesh.h)
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
ms.openlocfilehash: 7b3085cf9970f2c1f6fe3748cc4db8f4fb2b2a78
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105448"
---
# <a name="d3dx10_meshopt-enumeration"></a><span data-ttu-id="bcc26-103">D3DX10 \_ MESHOPT-Enumeration</span><span class="sxs-lookup"><span data-stu-id="bcc26-103">D3DX10\_MESHOPT enumeration</span></span>

<span data-ttu-id="bcc26-104">Gibt den Typ der durchzuführenden Gitternetzoptimierung an.</span><span class="sxs-lookup"><span data-stu-id="bcc26-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcc26-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bcc26-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="bcc26-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="bcc26-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bcc26-107"><span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10 \_ MESHOPT \_ COMPACT**</span><span class="sxs-lookup"><span data-stu-id="bcc26-107"><span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10\_MESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="bcc26-108">Ordnet Gesichter neu an, um nicht verwendete Scheitelungen und Gesichter zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="bcc26-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="bcc26-109"><span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10 \_ MESHOPT \_ ATTR \_ SORT**</span><span class="sxs-lookup"><span data-stu-id="bcc26-109"><span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10\_MESHOPT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="bcc26-110">Ordnet Gesichter neu an, um für weniger Attributbündelzustandsänderungen und verbesserte DrawSubset-Leistung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="bcc26-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced DrawSubset performance.</span></span>

</dd> <dt>

<span data-ttu-id="bcc26-111"><span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10 \_ MESHOPT \_ VERTEX \_ CACHE**</span><span class="sxs-lookup"><span data-stu-id="bcc26-111"><span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10\_MESHOPT\_VERTEX\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="bcc26-112">Ordnet Gesichter neu an, um die Cachetrefferrate von Scheitelpunktcaches zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="bcc26-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="bcc26-113"><span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**D3DX10 \_ MESHOPT \_ STRIP \_ REORDER**</span><span class="sxs-lookup"><span data-stu-id="bcc26-113"><span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**D3DX10\_MESHOPT\_STRIP\_REORDER**</span></span>
</dt> <dd>

<span data-ttu-id="bcc26-114">Ordnet Gesichter neu an, um die Länge benachbarter Dreiecke zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="bcc26-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="bcc26-115"><span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10 \_ MESHOPT \_ \_ VERTS IGNORIEREN**</span><span class="sxs-lookup"><span data-stu-id="bcc26-115"><span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10\_MESHOPT\_IGNORE\_VERTS**</span></span>
</dt> <dd>

<span data-ttu-id="bcc26-116">Nur die Gesichter optimieren; optimieren Sie die Scheitelungen nicht.</span><span class="sxs-lookup"><span data-stu-id="bcc26-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="bcc26-117"><span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10 \_ MESHOPT \_ NICHT \_ \_ TEILEN**</span><span class="sxs-lookup"><span data-stu-id="bcc26-117"><span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10\_MESHOPT\_DO\_NOT\_SPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="bcc26-118">Teilen Sie bei der Attributsortierung keine Scheitelungen auf, die von Attributgruppen gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="bcc26-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="bcc26-119"><span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10 \_ MESHOPT \_ DEVICE \_ INDEPENDENT**</span><span class="sxs-lookup"><span data-stu-id="bcc26-119"><span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10\_MESHOPT\_DEVICE\_INDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="bcc26-120">Wirkt sich auf die Größe des Scheitelpunktcaches aus.</span><span class="sxs-lookup"><span data-stu-id="bcc26-120">Affects the vertex cache size.</span></span> <span data-ttu-id="bcc26-121">Mit diesem Flag wird eine Standardgröße für den Scheitelpunktcache angegeben, die auf Legacyhardware gut funktioniert.</span><span class="sxs-lookup"><span data-stu-id="bcc26-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bcc26-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bcc26-122">Remarks</span></span>

<span data-ttu-id="bcc26-123">Die D3DXMESHOPT \_ STRIPREORDER- und D3DXMESHOPT \_ VERTEXCACHE-Optimierungsflags schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="bcc26-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="bcc26-124">Das D3DXMESHOPT \_ SHAREVB-Flag wurde aus dieser Enumeration entfernt.</span><span class="sxs-lookup"><span data-stu-id="bcc26-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="bcc26-125">Verwenden Sie stattdessen D3DXMESH \_ VB \_ SHARE in D3DXMESH.</span><span class="sxs-lookup"><span data-stu-id="bcc26-125">Use D3DXMESH\_VB\_SHARE instead, in D3DXMESH.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcc26-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bcc26-126">Requirements</span></span>



| <span data-ttu-id="bcc26-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bcc26-127">Requirement</span></span> | <span data-ttu-id="bcc26-128">Wert</span><span class="sxs-lookup"><span data-stu-id="bcc26-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcc26-129">Header</span><span class="sxs-lookup"><span data-stu-id="bcc26-129">Header</span></span><br/> | <dl> <span data-ttu-id="bcc26-130"><dt>D3DX10Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="bcc26-130"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcc26-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bcc26-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcc26-132">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="bcc26-132">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




