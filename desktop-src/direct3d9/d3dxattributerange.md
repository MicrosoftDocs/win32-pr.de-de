---
description: 'D3DXATTRIBUTERANGE-Struktur: Speichert einen Attributtabelleneintrag.'
ms.assetid: b9f13b12-35ba-4e4c-93ac-3dd44d611b47
title: D3DXATTRIBUTERANGE-Struktur (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTERANGE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7dfdf15f653fda77b1ca8c9a14cd32decee9658e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116008"
---
# <a name="d3dxattributerange-structure"></a><span data-ttu-id="8675d-103">D3DXATTRIBUTERANGE-Struktur</span><span class="sxs-lookup"><span data-stu-id="8675d-103">D3DXATTRIBUTERANGE structure</span></span>

<span data-ttu-id="8675d-104">Speichert einen Attributtabelleneintrag.</span><span class="sxs-lookup"><span data-stu-id="8675d-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="8675d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8675d-105">Syntax</span></span>


```C++
typedef struct D3DXATTRIBUTERANGE {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
} D3DXATTRIBUTERANGE, *LPD3DXATTRIBUTERANGE;
```



## <a name="members"></a><span data-ttu-id="8675d-106">Member</span><span class="sxs-lookup"><span data-stu-id="8675d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8675d-107">**AttribId**</span><span class="sxs-lookup"><span data-stu-id="8675d-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="8675d-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8675d-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8675d-109">Attributtabellenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="8675d-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="8675d-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="8675d-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="8675d-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8675d-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8675d-112">Beginnendes Gesicht.</span><span class="sxs-lookup"><span data-stu-id="8675d-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="8675d-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="8675d-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="8675d-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8675d-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8675d-115">Gesichtsanzahl.</span><span class="sxs-lookup"><span data-stu-id="8675d-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="8675d-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="8675d-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="8675d-117">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8675d-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8675d-118">Starten des Scheitelpunkts.</span><span class="sxs-lookup"><span data-stu-id="8675d-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="8675d-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="8675d-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="8675d-120">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8675d-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8675d-121">Scheitelpunktanzahl.</span><span class="sxs-lookup"><span data-stu-id="8675d-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8675d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8675d-122">Remarks</span></span>

<span data-ttu-id="8675d-123">Eine Attributtabelle wird verwendet, um Bereiche des Gitternetzes zu identifizieren, die mit unterschiedlichen Texturen, Renderzuständen, Materialien usw. gezeichnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8675d-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="8675d-124">Darüber hinaus kann die Anwendung die Attributtabelle verwenden, um Teile eines Gitters auszublenden, indem beim Zeichnen des Rahmens kein angegebener Attributbezeichner (AttribId) gezeichnunget wird.</span><span class="sxs-lookup"><span data-stu-id="8675d-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="8675d-125">Der LPD3DXATTRIBUTERANGE-Typ wird als Zeiger auf die **D3DXATTRIBUTERANGE-Struktur** definiert.</span><span class="sxs-lookup"><span data-stu-id="8675d-125">The LPD3DXATTRIBUTERANGE type is defined as a pointer to the **D3DXATTRIBUTERANGE** structure.</span></span>


```
typedef D3DXATTRIBUTERANGE* LPD3DXATTRIBUTERANGE;
```



## <a name="requirements"></a><span data-ttu-id="8675d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8675d-126">Requirements</span></span>



| <span data-ttu-id="8675d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8675d-127">Requirement</span></span> | <span data-ttu-id="8675d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="8675d-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8675d-129">Header</span><span class="sxs-lookup"><span data-stu-id="8675d-129">Header</span></span><br/> | <dl> <span data-ttu-id="8675d-130"><dt>D3dx9mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="8675d-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8675d-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8675d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8675d-132">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="8675d-132">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
