---
description: 'D3DX10_ATTRIBUTE_RANGE Struktur: Speichert einen Attributtabelleneintrag.'
ms.assetid: 81c77dc9-e078-46a1-a435-4b241e36ec13
title: D3DX10_ATTRIBUTE_RANGE-Struktur (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_RANGE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 3e2954483da53c77ebef57f9cf2de104734caba2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094368"
---
# <a name="d3dx10_attribute_range-structure"></a><span data-ttu-id="7232b-103">D3DX10 \_ ATTRIBUTE \_ RANGE-Struktur</span><span class="sxs-lookup"><span data-stu-id="7232b-103">D3DX10\_ATTRIBUTE\_RANGE structure</span></span>

<span data-ttu-id="7232b-104">Speichert einen Attributtabelleneintrag.</span><span class="sxs-lookup"><span data-stu-id="7232b-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="7232b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7232b-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_RANGE {
  UINT AttribId;
  UINT FaceStart;
  UINT FaceCount;
  UINT VertexStart;
  UINT VertexCount;
} D3DX10_ATTRIBUTE_RANGE, *LPD3DX10_ATTRIBUTE_RANGE;
```



## <a name="members"></a><span data-ttu-id="7232b-106">Member</span><span class="sxs-lookup"><span data-stu-id="7232b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7232b-107">**AttribId**</span><span class="sxs-lookup"><span data-stu-id="7232b-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="7232b-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7232b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7232b-109">Attributtabellenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="7232b-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7232b-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="7232b-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="7232b-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7232b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7232b-112">Beginnendes Gesicht.</span><span class="sxs-lookup"><span data-stu-id="7232b-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="7232b-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="7232b-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="7232b-114">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7232b-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7232b-115">Gesichtsanzahl.</span><span class="sxs-lookup"><span data-stu-id="7232b-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="7232b-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="7232b-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="7232b-117">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7232b-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7232b-118">Starten des Scheitelpunkts.</span><span class="sxs-lookup"><span data-stu-id="7232b-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="7232b-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="7232b-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="7232b-120">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7232b-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7232b-121">Scheitelpunktanzahl.</span><span class="sxs-lookup"><span data-stu-id="7232b-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7232b-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7232b-122">Remarks</span></span>

<span data-ttu-id="7232b-123">Eine Attributtabelle wird verwendet, um Bereiche des Gitternetzes zu identifizieren, die mit unterschiedlichen Texturen, Renderzuständen, Materialien usw. gezeichnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7232b-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="7232b-124">Darüber hinaus kann die Anwendung die Attributtabelle verwenden, um Teile eines Gitters auszublenden, indem beim Zeichnen des Rahmens kein angegebener Attributbezeichner (AttribId) gezeichnunget wird.</span><span class="sxs-lookup"><span data-stu-id="7232b-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="7232b-125">Der TYP LPD3DX ATTRIBUTE RANGE wird als Zeiger auf die \_ \_ D3DX \_ ATTRIBUTE \_ RANGE-Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="7232b-125">The LPD3DX\_ATTRIBUTE\_RANGE type is defined as a pointer to the D3DX\_ATTRIBUTE\_RANGE structure.</span></span>


```
typedef D3DX_ATTRIBUTE_RANGE* LPD3DX_ATTRIBUTE_RANGE;
```



## <a name="requirements"></a><span data-ttu-id="7232b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7232b-126">Requirements</span></span>



| <span data-ttu-id="7232b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7232b-127">Requirement</span></span> | <span data-ttu-id="7232b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="7232b-128">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7232b-129">Header</span><span class="sxs-lookup"><span data-stu-id="7232b-129">Header</span></span><br/> | <dl> <span data-ttu-id="7232b-130"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="7232b-130"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7232b-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7232b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7232b-132">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="7232b-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
