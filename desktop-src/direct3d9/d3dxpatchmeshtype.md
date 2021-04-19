---
description: Mesh-Patchtypen.
ms.assetid: 229d01b2-781c-48a8-93f2-9dd9dbd67f3e
title: D3DXPATCHMESHTYPE-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHMESHTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: d6a663e983b339d79ec89bf1b4ddfe7b4eaa9f1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355157"
---
# <a name="d3dxpatchmeshtype-enumeration"></a><span data-ttu-id="87e38-103">D3DXPATCHMESHTYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="87e38-103">D3DXPATCHMESHTYPE enumeration</span></span>

<span data-ttu-id="87e38-104">Mesh-Patchtypen.</span><span class="sxs-lookup"><span data-stu-id="87e38-104">Mesh patch types.</span></span>

## <a name="syntax"></a><span data-ttu-id="87e38-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="87e38-105">Syntax</span></span>


```C++
typedef enum D3DXPATCHMESHTYPE { 
  D3DXPATCHMESH_RECT         = 0x001,
  D3DXPATCHMESH_TRI          = 0x002,
  D3DXPATCHMESH_NPATCH       = 0x003,
  D3DXPATCHMESH_FORCE_DWORD  = 0x7fffffff
} D3DXPATCHMESHTYPE, *LPD3DXPATCHMESHTYPE;
```



## <a name="constants"></a><span data-ttu-id="87e38-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="87e38-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="87e38-107"><span id="D3DXPATCHMESH_RECT"></span><span id="d3dxpatchmesh_rect"></span>**D3DXPATCHMESH \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="87e38-107"><span id="D3DXPATCHMESH_RECT"></span><span id="d3dxpatchmesh_rect"></span>**D3DXPATCHMESH\_RECT**</span></span>
</dt> <dd>

<span data-ttu-id="87e38-108">Messtyp des Rechteck Patches.</span><span class="sxs-lookup"><span data-stu-id="87e38-108">Rectangle patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="87e38-109"><span id="D3DXPATCHMESH_TRI"></span><span id="d3dxpatchmesh_tri"></span>**D3DXPATCHMESH \_ Tri**</span><span class="sxs-lookup"><span data-stu-id="87e38-109"><span id="D3DXPATCHMESH_TRI"></span><span id="d3dxpatchmesh_tri"></span>**D3DXPATCHMESH\_TRI**</span></span>
</dt> <dd>

<span data-ttu-id="87e38-110">Messtyp des Dreiecks Patches.</span><span class="sxs-lookup"><span data-stu-id="87e38-110">Triangle patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="87e38-111"><span id="D3DXPATCHMESH_NPATCH"></span><span id="d3dxpatchmesh_npatch"></span>**D3DXPATCHMESH \_ npatch**</span><span class="sxs-lookup"><span data-stu-id="87e38-111"><span id="D3DXPATCHMESH_NPATCH"></span><span id="d3dxpatchmesh_npatch"></span>**D3DXPATCHMESH\_NPATCH**</span></span>
</dt> <dd>

<span data-ttu-id="87e38-112">N-patchmesh-Typ.</span><span class="sxs-lookup"><span data-stu-id="87e38-112">N-patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="87e38-113"><span id="D3DXPATCHMESH_FORCE_DWORD"></span><span id="d3dxpatchmesh_force_dword"></span>**D3DXPATCHMESH \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="87e38-113"><span id="D3DXPATCHMESH_FORCE_DWORD"></span><span id="d3dxpatchmesh_force_dword"></span>**D3DXPATCHMESH\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="87e38-114">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="87e38-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="87e38-115">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="87e38-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="87e38-116">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="87e38-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87e38-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87e38-117">Remarks</span></span>

<span data-ttu-id="87e38-118">Dreiecks Patches haben drei Seiten und werden in [**D3DTRIPATCH \_ Info**](d3dtripatch-info.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="87e38-118">Triangle patches have three sides and are described in [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span> <span data-ttu-id="87e38-119">Rechteck-Patches sind vierseitig und werden in [**D3DRECTPATCH \_ Info**](d3drectpatch-info.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="87e38-119">Rectangle patches are four-sided and are described in [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87e38-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87e38-120">Requirements</span></span>



| <span data-ttu-id="87e38-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87e38-121">Requirement</span></span> | <span data-ttu-id="87e38-122">Wert</span><span class="sxs-lookup"><span data-stu-id="87e38-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87e38-123">Header</span><span class="sxs-lookup"><span data-stu-id="87e38-123">Header</span></span><br/> | <dl> <span data-ttu-id="87e38-124"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="87e38-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87e38-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87e38-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e38-126">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="87e38-126">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="87e38-127">Verwenden von Higher-Order primitiven (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="87e38-127">Using Higher-Order Primitives (Direct3D 9)</span></span>](using-higher-order-primitives.md)
</dt> </dl>

 

 




