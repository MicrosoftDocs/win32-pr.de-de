---
description: Speichert einen Attribut Tabelleneintrag.
ms.assetid: b9f13b12-35ba-4e4c-93ac-3dd44d611b47
title: D3DXATTRIBUTERANGE-Struktur (D3dx9mesh. h)
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
ms.openlocfilehash: a842bbf41847f4b4e65c975e11f3e160cea1422d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350694"
---
# <a name="d3dxattributerange-structure"></a><span data-ttu-id="6694e-103">D3DXATTRIBUTERANGE-Struktur</span><span class="sxs-lookup"><span data-stu-id="6694e-103">D3DXATTRIBUTERANGE structure</span></span>

<span data-ttu-id="6694e-104">Speichert einen Attribut Tabelleneintrag.</span><span class="sxs-lookup"><span data-stu-id="6694e-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="6694e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6694e-105">Syntax</span></span>


```C++
typedef struct D3DXATTRIBUTERANGE {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
} D3DXATTRIBUTERANGE, *LPD3DXATTRIBUTERANGE;
```



## <a name="members"></a><span data-ttu-id="6694e-106">Member</span><span class="sxs-lookup"><span data-stu-id="6694e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6694e-107">**Atungbid**</span><span class="sxs-lookup"><span data-stu-id="6694e-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="6694e-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6694e-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6694e-109">Attribut Tabellen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="6694e-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="6694e-110">**Fakestart**</span><span class="sxs-lookup"><span data-stu-id="6694e-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="6694e-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6694e-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6694e-112">Startseite.</span><span class="sxs-lookup"><span data-stu-id="6694e-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="6694e-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="6694e-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="6694e-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6694e-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6694e-115">Anzahl der Gesichter.</span><span class="sxs-lookup"><span data-stu-id="6694e-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="6694e-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="6694e-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="6694e-117">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6694e-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6694e-118">Der Scheitelpunkt wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="6694e-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="6694e-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="6694e-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="6694e-120">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6694e-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6694e-121">Vertex-Anzahl.</span><span class="sxs-lookup"><span data-stu-id="6694e-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6694e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6694e-122">Remarks</span></span>

<span data-ttu-id="6694e-123">Eine Attribut Tabelle wird verwendet, um Bereiche des Netzes zu identifizieren, die mit unterschiedlichen Texturen, renderzuständen, Materialien usw. gezeichnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="6694e-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="6694e-124">Außerdem kann die Anwendung die Attribut Tabelle verwenden, um Teile eines Netzes auszublenden, indem beim Zeichnen des Frames kein angegebener Attribut Bezeichner (atungbid) gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="6694e-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="6694e-125">Der LPD3DXATTRIBUTERANGE-Typ wird als Zeiger auf die **D3DXATTRIBUTERANGE** -Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="6694e-125">The LPD3DXATTRIBUTERANGE type is defined as a pointer to the **D3DXATTRIBUTERANGE** structure.</span></span>


```
typedef D3DXATTRIBUTERANGE* LPD3DXATTRIBUTERANGE;
```



## <a name="requirements"></a><span data-ttu-id="6694e-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6694e-126">Requirements</span></span>



| <span data-ttu-id="6694e-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6694e-127">Requirement</span></span> | <span data-ttu-id="6694e-128">Wert</span><span class="sxs-lookup"><span data-stu-id="6694e-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6694e-129">Header</span><span class="sxs-lookup"><span data-stu-id="6694e-129">Header</span></span><br/> | <dl> <span data-ttu-id="6694e-130"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6694e-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6694e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6694e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6694e-132">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="6694e-132">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
