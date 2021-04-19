---
description: Gibt den Typ der auszuführenden Mesh-Optimierung an.
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: D3DXMESHOPT-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: e7d4f9f4ae36cec74ea86fcb50a194ac66d0add7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361202"
---
# <a name="d3dxmeshopt-enumeration"></a><span data-ttu-id="c0931-103">D3DXMESHOPT-Enumeration</span><span class="sxs-lookup"><span data-stu-id="c0931-103">D3DXMESHOPT enumeration</span></span>

<span data-ttu-id="c0931-104">Gibt den Typ der auszuführenden Mesh-Optimierung an.</span><span class="sxs-lookup"><span data-stu-id="c0931-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0931-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0931-105">Syntax</span></span>


```C++
enum _D3DXMESHOPT {
  D3DXMESHOPT_COMPACT            = 0x01000000, 
  D3DXMESHOPT_ATTRSORT           = 0x02000000, 
  D3DXMESHOPT_VERTEXCACHE        = 0x04000000, 
  D3DXMESHOPT_STRIPREORDER       = 0x08000000, 
  D3DXMESHOPT_IGNOREVERTS        = 0x10000000, 
  D3DXMESHOPT_DONOTSPLIT         = 0x20000000, 
  D3DXMESHOPT_DEVICEINDEPENDENT  = 0x40000000 

};
```



## <a name="constants"></a><span data-ttu-id="c0931-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="c0931-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c0931-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ Compact**</span><span class="sxs-lookup"><span data-stu-id="c0931-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="c0931-108">Ordnet Gesichter neu an, um nicht verwendete Vertices und Gesichter zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="c0931-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="c0931-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ attrsort**</span><span class="sxs-lookup"><span data-stu-id="c0931-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT\_ATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="c0931-110">Ordnet Gesichter neu an, um weniger Attribut Bündel Statusänderungen und erweiterte [**ID3DXBaseMesh zu optimieren::D rawsubset**](id3dxbasemesh--drawsubset.md) Performance.</span><span class="sxs-lookup"><span data-stu-id="c0931-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced [**ID3DXBaseMesh::DrawSubset**](id3dxbasemesh--drawsubset.md) performance.</span></span>

</dd> <dt>

<span data-ttu-id="c0931-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ vertexcache**</span><span class="sxs-lookup"><span data-stu-id="c0931-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT\_VERTEXCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="c0931-112">Ordnet Gesichter neu an, um die Cache Treffer Rate von Vertex-Caches zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="c0931-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="c0931-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ stripreorder**</span><span class="sxs-lookup"><span data-stu-id="c0931-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT\_STRIPREORDER**</span></span>
</dt> <dd>

<span data-ttu-id="c0931-114">Ordnet Flächen neu an, um die Länge der angrenzenden Dreiecke zu maximieren</span><span class="sxs-lookup"><span data-stu-id="c0931-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="c0931-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ ignoreverts**</span><span class="sxs-lookup"><span data-stu-id="c0931-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT\_IGNOREVERTS**</span></span>
</dt> <dd>

<span data-ttu-id="c0931-116">Nur Gesichter optimieren; Optimieren Sie die Vertices nicht.</span><span class="sxs-lookup"><span data-stu-id="c0931-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="c0931-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ donotsplit**</span><span class="sxs-lookup"><span data-stu-id="c0931-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT\_DONOTSPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="c0931-118">Bei der Attribut Sortierung werden Vertices, die von Attribut Gruppen gemeinsam verwendet werden, nicht aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="c0931-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="c0931-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT-Geräte \_ abhängige Geräte**</span><span class="sxs-lookup"><span data-stu-id="c0931-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT\_DEVICEINDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="c0931-120">Wirkt sich auf die Scheitelpunkt Cache Größe aus.</span><span class="sxs-lookup"><span data-stu-id="c0931-120">Affects the vertex cache size.</span></span> <span data-ttu-id="c0931-121">Die Verwendung dieses Flags gibt eine Standard Cache Größe an, die auf Legacy Hardware gut funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c0931-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0931-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0931-122">Remarks</span></span>

<span data-ttu-id="c0931-123">Die \_ Optimierungs Flags "D3DXMESHOPT stripreorder" und "D3DXMESHOPT \_ vertexcache" schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="c0931-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="c0931-124">Das \_ Flag D3DXMESHOPT sharevb wurde aus dieser Enumeration entfernt.</span><span class="sxs-lookup"><span data-stu-id="c0931-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="c0931-125">Verwenden Sie \_ stattdessen die D3DXMESH vb- \_ Freigabe in [**D3DXMESH**](./d3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="c0931-125">Use D3DXMESH\_VB\_SHARE instead, in [**D3DXMESH**](./d3dxmesh.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0931-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0931-126">Requirements</span></span>



| <span data-ttu-id="c0931-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0931-127">Requirement</span></span> | <span data-ttu-id="c0931-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c0931-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0931-129">Header</span><span class="sxs-lookup"><span data-stu-id="c0931-129">Header</span></span><br/> | <dl> <span data-ttu-id="c0931-130"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0931-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0931-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0931-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0931-132">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="c0931-132">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
