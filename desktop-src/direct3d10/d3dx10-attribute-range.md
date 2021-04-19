---
description: Speichert einen Attribut Tabelleneintrag.
ms.assetid: 81c77dc9-e078-46a1-a435-4b241e36ec13
title: D3DX10_ATTRIBUTE_RANGE-Struktur (d3dx10. h)
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
ms.openlocfilehash: ddf7f10882e08232467130b3abbc6fb723a843ed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106369320"
---
# <a name="d3dx10_attribute_range-structure"></a><span data-ttu-id="aafb0-103">D3dx10- \_ Attribut \_ Bereichs Struktur</span><span class="sxs-lookup"><span data-stu-id="aafb0-103">D3DX10\_ATTRIBUTE\_RANGE structure</span></span>

<span data-ttu-id="aafb0-104">Speichert einen Attribut Tabelleneintrag.</span><span class="sxs-lookup"><span data-stu-id="aafb0-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="aafb0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aafb0-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_RANGE {
  UINT AttribId;
  UINT FaceStart;
  UINT FaceCount;
  UINT VertexStart;
  UINT VertexCount;
} D3DX10_ATTRIBUTE_RANGE, *LPD3DX10_ATTRIBUTE_RANGE;
```



## <a name="members"></a><span data-ttu-id="aafb0-106">Member</span><span class="sxs-lookup"><span data-stu-id="aafb0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="aafb0-107">**Atungbid**</span><span class="sxs-lookup"><span data-stu-id="aafb0-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="aafb0-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aafb0-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="aafb0-109">Attribut Tabellen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="aafb0-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="aafb0-110">**Fakestart**</span><span class="sxs-lookup"><span data-stu-id="aafb0-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="aafb0-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aafb0-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="aafb0-112">Startseite.</span><span class="sxs-lookup"><span data-stu-id="aafb0-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="aafb0-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="aafb0-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="aafb0-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aafb0-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="aafb0-115">Anzahl der Gesichter.</span><span class="sxs-lookup"><span data-stu-id="aafb0-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="aafb0-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="aafb0-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="aafb0-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aafb0-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="aafb0-118">Der Scheitelpunkt wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="aafb0-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="aafb0-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="aafb0-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="aafb0-120">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aafb0-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="aafb0-121">Vertex-Anzahl.</span><span class="sxs-lookup"><span data-stu-id="aafb0-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aafb0-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aafb0-122">Remarks</span></span>

<span data-ttu-id="aafb0-123">Eine Attribut Tabelle wird verwendet, um Bereiche des Netzes zu identifizieren, die mit unterschiedlichen Texturen, renderzuständen, Materialien usw. gezeichnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="aafb0-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="aafb0-124">Außerdem kann die Anwendung die Attribut Tabelle verwenden, um Teile eines Netzes auszublenden, indem beim Zeichnen des Frames kein angegebener Attribut Bezeichner (atungbid) gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="aafb0-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="aafb0-125">Der LPD3DX- \_ Attribut \_ Bereichstyp ist als Zeiger auf die D3DX- \_ Attribut \_ Bereichs Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="aafb0-125">The LPD3DX\_ATTRIBUTE\_RANGE type is defined as a pointer to the D3DX\_ATTRIBUTE\_RANGE structure.</span></span>


```
typedef D3DX_ATTRIBUTE_RANGE* LPD3DX_ATTRIBUTE_RANGE;
```



## <a name="requirements"></a><span data-ttu-id="aafb0-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aafb0-126">Requirements</span></span>



| <span data-ttu-id="aafb0-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aafb0-127">Requirement</span></span> | <span data-ttu-id="aafb0-128">Wert</span><span class="sxs-lookup"><span data-stu-id="aafb0-128">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aafb0-129">Header</span><span class="sxs-lookup"><span data-stu-id="aafb0-129">Header</span></span><br/> | <dl> <span data-ttu-id="aafb0-130"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="aafb0-130"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aafb0-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aafb0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aafb0-132">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="aafb0-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
