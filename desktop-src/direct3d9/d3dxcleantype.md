---
description: Definiert Vorgänge, die für Scheitel Punkte zur Vorbereitung der Mesh-Bereinigung durchgeführt werden.
ms.assetid: f222acaa-fa82-4591-b7c2-b520cb648ed5
title: D3DXCLEANTYPE-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCLEANTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: b38578d0f50521def552b8bd6608c2696b405d0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219557"
---
# <a name="d3dxcleantype-enumeration"></a><span data-ttu-id="fbe34-103">D3DXCLEANTYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="fbe34-103">D3DXCLEANTYPE enumeration</span></span>

<span data-ttu-id="fbe34-104">Definiert Vorgänge, die für Scheitel Punkte zur Vorbereitung der Mesh-Bereinigung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fbe34-104">Defines operations to perform on vertices in preparation for mesh cleaning.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbe34-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbe34-105">Syntax</span></span>


```C++
typedef enum D3DXCLEANTYPE { 
  D3DXCLEAN_BACKFACING      = 1,
  D3DXCLEAN_BOWTIES         = 2,
  D3DXCLEAN_SKINNING        = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_OPTIMIZATION    = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_SIMPLIFICATION  = D3DXCLEAN_BACKFACING | D3DXCLEAN_BOWTIES
} D3DXCLEANTYPE, *LPD3DXCLEANTYPE;
```



## <a name="constants"></a><span data-ttu-id="fbe34-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="fbe34-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fbe34-107"><span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN \_**</span><span class="sxs-lookup"><span data-stu-id="fbe34-107"><span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN\_BACKFACING**</span></span>
</dt> <dd>

<span data-ttu-id="fbe34-108">Das Zusammenführen von Dreiecken, die die gleichen Scheitelpunkt Indizes aufweisen, aber über Gesichts normale verfügen, die auf entgegengesetzte Richtungen zeigen</span><span class="sxs-lookup"><span data-stu-id="fbe34-108">Merge triangles that share the same vertex indices but have face normals pointing in opposite directions (back-facing triangles).</span></span> <span data-ttu-id="fbe34-109">Wenn die Dreiecke nicht durch Hinzufügen eines replizierten Scheitel Punkts geteilt werden, können die Gitter einfügdaten der beiden Dreiecke einen Konflikt verursachen.</span><span class="sxs-lookup"><span data-stu-id="fbe34-109">Unless the triangles are not split by adding a replicated vertex, mesh adjacency data from the two triangles may conflict.</span></span>

</dd> <dt>

<span data-ttu-id="fbe34-110"><span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN- \_ bowties**</span><span class="sxs-lookup"><span data-stu-id="fbe34-110"><span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN\_BOWTIES**</span></span>
</dt> <dd>

<span data-ttu-id="fbe34-111">Wenn ein Scheitelpunkt die Spitze zweier Dreiecks Lüfter (ein Bowtie) ist und Mesh-Vorgänge einen der Lüfter beeinflussen, teilen Sie den freigegebenen Scheitelpunkt in zwei neue Scheitel Punkte auf.</span><span class="sxs-lookup"><span data-stu-id="fbe34-111">If a vertex is the apex of two triangle fans (a bowtie) and mesh operations will affect one of the fans, then split the shared vertex into two new vertices.</span></span> <span data-ttu-id="fbe34-112">Bowties können Probleme bei Vorgängen verursachen, z. b. bei der Mesh-Vereinfachung, bei der Vertices entfernt werden, da das Entfernen eines Scheitel Punkts zwei unterschiedliche Dreiecke</span><span class="sxs-lookup"><span data-stu-id="fbe34-112">Bowties can cause problems for operations such as mesh simplification that remove vertices, because removing one vertex affects two distinct sets of triangles.</span></span>

</dd> <dt>

<span data-ttu-id="fbe34-113"><span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN- \_ Skinning**</span><span class="sxs-lookup"><span data-stu-id="fbe34-113"><span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN\_SKINNING**</span></span>
</dt> <dd>

<span data-ttu-id="fbe34-114">Verwenden Sie dieses Flag, um unendliche Schleifen während der Einrichtung von settervorgängen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="fbe34-114">Use this flag to prevent infinite loops during skinning setup mesh operations.</span></span>

</dd> <dt>

<span data-ttu-id="fbe34-115"><span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**D3DXCLEAN- \_ Optimierung**</span><span class="sxs-lookup"><span data-stu-id="fbe34-115"><span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**D3DXCLEAN\_OPTIMIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="fbe34-116">Verwenden Sie dieses Flag, um unendliche Schleifen während Gitter Optimierungs Vorgängen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="fbe34-116">Use this flag to prevent infinite loops during mesh optimization operations.</span></span>

</dd> <dt>

<span data-ttu-id="fbe34-117"><span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**D3DXCLEAN- \_ Vereinfachung**</span><span class="sxs-lookup"><span data-stu-id="fbe34-117"><span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**D3DXCLEAN\_SIMPLIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="fbe34-118">Verwenden Sie dieses Flag, um unendliche Schleifen während Mesh-Vereinfachungs Vorgängen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="fbe34-118">Use this flag to prevent infinite loops during mesh simplification operations.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fbe34-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbe34-119">Requirements</span></span>



| <span data-ttu-id="fbe34-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbe34-120">Requirement</span></span> | <span data-ttu-id="fbe34-121">Wert</span><span class="sxs-lookup"><span data-stu-id="fbe34-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbe34-122">Header</span><span class="sxs-lookup"><span data-stu-id="fbe34-122">Header</span></span><br/> | <dl> <span data-ttu-id="fbe34-123"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbe34-123"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbe34-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbe34-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbe34-125">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="fbe34-125">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




