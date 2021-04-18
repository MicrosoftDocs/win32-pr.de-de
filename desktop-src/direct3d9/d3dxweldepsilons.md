---
description: Gibt Toleranzwerte für jede Scheitelpunkt Komponente an, wenn Vertices verglichen werden, um zu bestimmen, ob Sie so ähnlich sind, dass Sie miteinander verbunden werden.
ms.assetid: 534903da-ff65-4629-9be9-66c9daed6ef5
title: D3DXWELDEPSILONS-Struktur (D3dx9mesh. h)
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
ms.openlocfilehash: 6b6673e16b153f53baf17967b7f33c4bcb40d518
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365105"
---
# <a name="d3dxweldepsilons-structure"></a><span data-ttu-id="9612d-103">D3DXWELDEPSILONS-Struktur</span><span class="sxs-lookup"><span data-stu-id="9612d-103">D3DXWELDEPSILONS structure</span></span>

<span data-ttu-id="9612d-104">Gibt Toleranzwerte für jede Scheitelpunkt Komponente an, wenn Vertices verglichen werden, um zu bestimmen, ob Sie so ähnlich sind, dass Sie miteinander verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="9612d-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="9612d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9612d-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="9612d-106">Member</span><span class="sxs-lookup"><span data-stu-id="9612d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9612d-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="9612d-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="9612d-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9612d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9612d-109">Position</span><span class="sxs-lookup"><span data-stu-id="9612d-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="9612d-110">**Blendweights**</span><span class="sxs-lookup"><span data-stu-id="9612d-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="9612d-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9612d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9612d-112">Blend-Gewichtung</span><span class="sxs-lookup"><span data-stu-id="9612d-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="9612d-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="9612d-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="9612d-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9612d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9612d-115">Normal</span><span class="sxs-lookup"><span data-stu-id="9612d-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="9612d-116">**Psize**</span><span class="sxs-lookup"><span data-stu-id="9612d-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="9612d-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9612d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9612d-118">Wert der Punktgröße</span><span class="sxs-lookup"><span data-stu-id="9612d-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="9612d-119">**Glänzend**</span><span class="sxs-lookup"><span data-stu-id="9612d-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="9612d-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9612d-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9612d-121">Glanzlicht Wert</span><span class="sxs-lookup"><span data-stu-id="9612d-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="9612d-122">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="9612d-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="9612d-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9612d-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9612d-124">Diffuses Beleuchtungs Wert</span><span class="sxs-lookup"><span data-stu-id="9612d-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="9612d-125">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="9612d-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="9612d-126">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9612d-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9612d-127">Acht Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="9612d-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="9612d-128">**Tangens**</span><span class="sxs-lookup"><span data-stu-id="9612d-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="9612d-129">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9612d-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9612d-130">Tangens</span><span class="sxs-lookup"><span data-stu-id="9612d-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="9612d-131">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="9612d-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="9612d-132">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9612d-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9612d-133">Binormal</span><span class="sxs-lookup"><span data-stu-id="9612d-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="9612d-134">**Mosaik Faktor**</span><span class="sxs-lookup"><span data-stu-id="9612d-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="9612d-135">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9612d-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9612d-136">Mosaik Faktor</span><span class="sxs-lookup"><span data-stu-id="9612d-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9612d-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9612d-137">Remarks</span></span>

<span data-ttu-id="9612d-138">Der LPD3DXWELDEPSILONS-Typ wird als Zeiger auf die **D3DXWELDEPSILONS** -Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="9612d-138">The LPD3DXWELDEPSILONS type is defined as a pointer to the **D3DXWELDEPSILONS** structure.</span></span>


```
typedef D3DXWELDEPSILONS *LPD3DXWELDEPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="9612d-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9612d-139">Requirements</span></span>



| <span data-ttu-id="9612d-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9612d-140">Requirement</span></span> | <span data-ttu-id="9612d-141">Wert</span><span class="sxs-lookup"><span data-stu-id="9612d-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9612d-142">Header</span><span class="sxs-lookup"><span data-stu-id="9612d-142">Header</span></span><br/> | <dl> <span data-ttu-id="9612d-143"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9612d-143"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9612d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9612d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9612d-145">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="9612d-145">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="9612d-146">**D3DXWeldVertices**</span><span class="sxs-lookup"><span data-stu-id="9612d-146">**D3DXWeldVertices**</span></span>](d3dxweldvertices.md)
</dt> </dl>

 

 
