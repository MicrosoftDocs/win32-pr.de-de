---
description: Diese Konstante ist die maximale Anzahl von Vertex-Deklaratoren für ein Mesh.
ms.assetid: 234e99a2-1907-4065-b03b-fb9e8d6812ab
title: MAX_FVF_DECL_SIZE-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MAX_FVF_DECL_SIZE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7204308e6b9355b416218f31af301b5ea6d8fff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371905"
---
# <a name="max_fvf_decl_size-enumeration"></a><span data-ttu-id="3521c-103">Maximal zulässige Anzahl von \_ f- \_ decl- \_ Größen</span><span class="sxs-lookup"><span data-stu-id="3521c-103">MAX\_FVF\_DECL\_SIZE enumeration</span></span>

<span data-ttu-id="3521c-104">Diese Konstante ist die maximale Anzahl von Vertex-Deklaratoren für ein Mesh.</span><span class="sxs-lookup"><span data-stu-id="3521c-104">This constant is the maximum number of vertex declarators for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="3521c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3521c-105">Syntax</span></span>


```C++
typedef enum  { 
  MAX_FVF_DECL_SIZE  = MAXD3DDECLLENGTH + 1
} MAX_FVF_DECL_SIZE;
```



## <a name="constants"></a><span data-ttu-id="3521c-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="3521c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3521c-107"><span id="MAX_FVF_DECL_SIZE"></span><span id="max_fvf_decl_size"></span>**maximale \_ Größe der f- \_ decl \_**</span><span class="sxs-lookup"><span data-stu-id="3521c-107"><span id="MAX_FVF_DECL_SIZE"></span><span id="max_fvf_decl_size"></span>**MAX\_FVF\_DECL\_SIZE**</span></span>
</dt> <dd>

<span data-ttu-id="3521c-108">Die maximale Anzahl von Elementen in der Vertex-Deklaration.</span><span class="sxs-lookup"><span data-stu-id="3521c-108">The maximum number of elements in the vertex declaration.</span></span> <span data-ttu-id="3521c-109">Der zusätzliche (+ 1) ist für [**D3DDECL \_ End**](d3ddecl-end.md).</span><span class="sxs-lookup"><span data-stu-id="3521c-109">The additional (+1) is for [**D3DDECL\_END**](d3ddecl-end.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3521c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3521c-110">Remarks</span></span>

<span data-ttu-id="3521c-111">MAXD3DDECLLENGTH wird als Maximum von 64 definiert (siehe d3d9types. h).</span><span class="sxs-lookup"><span data-stu-id="3521c-111">MAXD3DDECLLENGTH is defined as a maximum of 64 (see d3d9types.h).</span></span> <span data-ttu-id="3521c-112">Dies schließt nicht das "End"-markervertex-Element ein.</span><span class="sxs-lookup"><span data-stu-id="3521c-112">This does not include the "end" marker vertex element.</span></span>

## <a name="requirements"></a><span data-ttu-id="3521c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3521c-113">Requirements</span></span>



| <span data-ttu-id="3521c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3521c-114">Requirement</span></span> | <span data-ttu-id="3521c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3521c-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3521c-116">Header</span><span class="sxs-lookup"><span data-stu-id="3521c-116">Header</span></span><br/> | <dl> <span data-ttu-id="3521c-117"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3521c-117"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3521c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3521c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3521c-119">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="3521c-119">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="3521c-120">**ID3DXBaseMesh**</span><span class="sxs-lookup"><span data-stu-id="3521c-120">**ID3DXBaseMesh**</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="3521c-121">**GetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="3521c-121">**GetDeclaration**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexdeclaration9-getdeclaration)
</dt> <dt>

[<span data-ttu-id="3521c-122">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="3521c-122">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> <dt>

[<span data-ttu-id="3521c-123">**ID3DXSkinInfo**</span><span class="sxs-lookup"><span data-stu-id="3521c-123">**ID3DXSkinInfo**</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
