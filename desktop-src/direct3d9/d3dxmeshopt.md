---
description: 'D3DXMESHOPT-Enumeration: Gibt den Typ der durchzuführenden Meshoptimierung an.'
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: D3DXMESHOPT-Enumeration (D3dx9mesh.h)
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
ms.openlocfilehash: db7c2a2411d1c846c7369fc1d925a8e5569df3b1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114348"
---
# <a name="d3dxmeshopt-enumeration"></a><span data-ttu-id="4400d-103">D3DXMESHOPT-Enumeration</span><span class="sxs-lookup"><span data-stu-id="4400d-103">D3DXMESHOPT enumeration</span></span>

<span data-ttu-id="4400d-104">Gibt den Typ der durchzuführenden Meshoptimierung an.</span><span class="sxs-lookup"><span data-stu-id="4400d-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="4400d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4400d-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="4400d-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="4400d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4400d-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ COMPACT**</span><span class="sxs-lookup"><span data-stu-id="4400d-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="4400d-108">Ordnet Gesichter neu an, um nicht verwendete Scheitelpunkte und Gesichter zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="4400d-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="4400d-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ ATTRSORT**</span><span class="sxs-lookup"><span data-stu-id="4400d-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT\_ATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="4400d-110">Ordnet Gesichter neu an, um die Leistung von [**ID3DXBaseMesh::D rawSubset**](id3dxbasemesh--drawsubset.md) zu optimieren, um weniger Änderungen am Attributbündelzustand zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="4400d-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced [**ID3DXBaseMesh::DrawSubset**](id3dxbasemesh--drawsubset.md) performance.</span></span>

</dd> <dt>

<span data-ttu-id="4400d-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ VERTEXCACHE**</span><span class="sxs-lookup"><span data-stu-id="4400d-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT\_VERTEXCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="4400d-112">Ordnet Gesichter neu an, um die Cachetrefferrate von Scheitelpunktcaches zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="4400d-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="4400d-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ STRIPREORDER**</span><span class="sxs-lookup"><span data-stu-id="4400d-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT\_STRIPREORDER**</span></span>
</dt> <dd>

<span data-ttu-id="4400d-114">Ordnet Gesichter neu an, um die Länge benachbarter Dreiecke zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="4400d-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="4400d-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ IGNOREVERTS**</span><span class="sxs-lookup"><span data-stu-id="4400d-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT\_IGNOREVERTS**</span></span>
</dt> <dd>

<span data-ttu-id="4400d-116">Nur die Gesichter optimieren; optimieren Sie die Scheitelpunkte nicht.</span><span class="sxs-lookup"><span data-stu-id="4400d-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="4400d-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ DONOTSPLIT**</span><span class="sxs-lookup"><span data-stu-id="4400d-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT\_DONOTSPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="4400d-118">Teilen Sie beim Sortieren von Attributen keine Scheitelpunkte, die von Attributgruppen gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="4400d-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="4400d-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT \_ DEVICEINDEPENDENT**</span><span class="sxs-lookup"><span data-stu-id="4400d-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT\_DEVICEINDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="4400d-120">Wirkt sich auf die Größe des Scheitelpunktcaches aus.</span><span class="sxs-lookup"><span data-stu-id="4400d-120">Affects the vertex cache size.</span></span> <span data-ttu-id="4400d-121">Die Verwendung dieses Flags gibt eine Standardgröße des Scheitelpunktcaches an, die auf Legacyhardware gut funktioniert.</span><span class="sxs-lookup"><span data-stu-id="4400d-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4400d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4400d-122">Remarks</span></span>

<span data-ttu-id="4400d-123">Die Optimierungsflags D3DXMESHOPT \_ STRIPREORDER und D3DXMESHOPT \_ VERTEXCACHE schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="4400d-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="4400d-124">Das SHAREVB-Flag D3DXMESHOPT \_ wurde aus dieser Enumeration entfernt.</span><span class="sxs-lookup"><span data-stu-id="4400d-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="4400d-125">Verwenden Sie stattdessen D3DXMESH \_ VB \_ SHARE in [**D3DXMESH**](./d3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="4400d-125">Use D3DXMESH\_VB\_SHARE instead, in [**D3DXMESH**](./d3dxmesh.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4400d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4400d-126">Requirements</span></span>



| <span data-ttu-id="4400d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4400d-127">Requirement</span></span> | <span data-ttu-id="4400d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="4400d-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4400d-129">Header</span><span class="sxs-lookup"><span data-stu-id="4400d-129">Header</span></span><br/> | <dl> <span data-ttu-id="4400d-130"><dt>D3dx9mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="4400d-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4400d-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4400d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4400d-132">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="4400d-132">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
