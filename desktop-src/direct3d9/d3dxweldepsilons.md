---
description: 'D3DXWELDEPSILONS-Struktur: Gibt Beim Vergleich von Scheitelpunkten Toleranzwerte für jede Vertexkomponente an, um zu bestimmen, ob sie ähnlich genug sind, um zusammen zusammengestellt zu werden.'
ms.assetid: 534903da-ff65-4629-9be9-66c9daed6ef5
title: D3DXWELDEPSILONS-Struktur (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWELDEPSILONS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: bb11e6f5481b1adf7cc1bac58edf40d4ac770e92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115498"
---
# <a name="d3dxweldepsilons-structure"></a><span data-ttu-id="45d93-103">D3DXWELDEPSILONS-Struktur</span><span class="sxs-lookup"><span data-stu-id="45d93-103">D3DXWELDEPSILONS structure</span></span>

<span data-ttu-id="45d93-104">Gibt Beim Vergleich von Scheitelpunkten Toleranzwerte für jede Scheitelpunktkomponente an, um zu bestimmen, ob sie ähnlich genug sind, um zusammengeknauft zu werden.</span><span class="sxs-lookup"><span data-stu-id="45d93-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="45d93-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="45d93-105">Syntax</span></span>


```C++
typedef struct _D3DXWELDEPSILONS {
  FLOAT Position;
  FLOAT BlendWeights;
  FLOAT Normal;
  FLOAT PSize;
  FLOAT Specular;
  FLOAT Diffuse;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
  FLOAT TessFactor;
} D3DXWELDEPSILONS, *LPD3DXWELDEPSILONS;
```



## <a name="members"></a><span data-ttu-id="45d93-106">Member</span><span class="sxs-lookup"><span data-stu-id="45d93-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="45d93-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="45d93-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="45d93-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45d93-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="45d93-109">Position</span><span class="sxs-lookup"><span data-stu-id="45d93-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="45d93-110">**BlendWeights**</span><span class="sxs-lookup"><span data-stu-id="45d93-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="45d93-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45d93-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="45d93-112">Mischungsgewichtung</span><span class="sxs-lookup"><span data-stu-id="45d93-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="45d93-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="45d93-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="45d93-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45d93-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="45d93-115">Normal</span><span class="sxs-lookup"><span data-stu-id="45d93-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="45d93-116">**PSize**</span><span class="sxs-lookup"><span data-stu-id="45d93-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="45d93-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45d93-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="45d93-118">Wert der Punktgröße</span><span class="sxs-lookup"><span data-stu-id="45d93-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="45d93-119">**Glänzend**</span><span class="sxs-lookup"><span data-stu-id="45d93-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="45d93-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45d93-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="45d93-121">Glanzlichtwert</span><span class="sxs-lookup"><span data-stu-id="45d93-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="45d93-122">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="45d93-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="45d93-123">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45d93-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="45d93-124">Diffuser Beleuchtungswert</span><span class="sxs-lookup"><span data-stu-id="45d93-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="45d93-125">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="45d93-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="45d93-126">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45d93-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="45d93-127">Acht Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="45d93-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="45d93-128">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="45d93-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="45d93-129">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45d93-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="45d93-130">Tangens</span><span class="sxs-lookup"><span data-stu-id="45d93-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="45d93-131">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="45d93-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="45d93-132">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45d93-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="45d93-133">Binormal</span><span class="sxs-lookup"><span data-stu-id="45d93-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="45d93-134">**TessFactor**</span><span class="sxs-lookup"><span data-stu-id="45d93-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="45d93-135">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45d93-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="45d93-136">Mosaikfaktor</span><span class="sxs-lookup"><span data-stu-id="45d93-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45d93-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45d93-137">Remarks</span></span>

<span data-ttu-id="45d93-138">Der LPD3DXWELDEPSILONS-Typ ist als Zeiger auf die **D3DXWELDEPSILONS-Struktur** definiert.</span><span class="sxs-lookup"><span data-stu-id="45d93-138">The LPD3DXWELDEPSILONS type is defined as a pointer to the **D3DXWELDEPSILONS** structure.</span></span>


```
typedef D3DXWELDEPSILONS *LPD3DXWELDEPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="45d93-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45d93-139">Requirements</span></span>



| <span data-ttu-id="45d93-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45d93-140">Requirement</span></span> | <span data-ttu-id="45d93-141">Wert</span><span class="sxs-lookup"><span data-stu-id="45d93-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45d93-142">Header</span><span class="sxs-lookup"><span data-stu-id="45d93-142">Header</span></span><br/> | <dl> <span data-ttu-id="45d93-143"><dt>D3dx9mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="45d93-143"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45d93-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="45d93-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45d93-145">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="45d93-145">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="45d93-146">**D3DXWeldVertices**</span><span class="sxs-lookup"><span data-stu-id="45d93-146">**D3DXWeldVertices**</span></span>](d3dxweldvertices.md)
</dt> </dl>

 

 
