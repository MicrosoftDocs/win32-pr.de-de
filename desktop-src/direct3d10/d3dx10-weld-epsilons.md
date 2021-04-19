---
description: Gibt Toleranzwerte für jede Scheitelpunkt Komponente an, wenn Vertices verglichen werden, um zu bestimmen, ob Sie so ähnlich sind, dass Sie miteinander verbunden werden.
ms.assetid: b28a17bd-5d5b-41b3-86d9-327f5497fc94
title: D3DX10_WELD_EPSILONS-Struktur (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_WELD_EPSILONS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: c72f63e3ecef1fdb193fcaec9220f9768204d099
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367458"
---
# <a name="d3dx10_weld_epsilons-structure"></a><span data-ttu-id="5d154-103">D3dx10 \_ Weld \_ epsilons-Struktur</span><span class="sxs-lookup"><span data-stu-id="5d154-103">D3DX10\_WELD\_EPSILONS structure</span></span>

<span data-ttu-id="5d154-104">Gibt Toleranzwerte für jede Scheitelpunkt Komponente an, wenn Vertices verglichen werden, um zu bestimmen, ob Sie so ähnlich sind, dass Sie miteinander verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="5d154-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d154-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d154-105">Syntax</span></span>


```C++
typedef struct D3DX10_WELD_EPSILONS {
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
} D3DX10_WELD_EPSILONS, *LPD3DX10_WELD_EPSILONS;
```



## <a name="members"></a><span data-ttu-id="5d154-106">Member</span><span class="sxs-lookup"><span data-stu-id="5d154-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5d154-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="5d154-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="5d154-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d154-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5d154-109">Position</span><span class="sxs-lookup"><span data-stu-id="5d154-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="5d154-110">**Blendweights**</span><span class="sxs-lookup"><span data-stu-id="5d154-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="5d154-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d154-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5d154-112">Blend-Gewichtung</span><span class="sxs-lookup"><span data-stu-id="5d154-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="5d154-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="5d154-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="5d154-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d154-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5d154-115">Normal</span><span class="sxs-lookup"><span data-stu-id="5d154-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="5d154-116">**Psize**</span><span class="sxs-lookup"><span data-stu-id="5d154-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="5d154-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d154-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5d154-118">Wert der Punktgröße</span><span class="sxs-lookup"><span data-stu-id="5d154-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="5d154-119">**Glänzend**</span><span class="sxs-lookup"><span data-stu-id="5d154-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="5d154-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d154-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5d154-121">Glanzlicht Wert</span><span class="sxs-lookup"><span data-stu-id="5d154-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="5d154-122">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="5d154-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="5d154-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d154-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5d154-124">Diffuses Beleuchtungs Wert</span><span class="sxs-lookup"><span data-stu-id="5d154-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="5d154-125">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="5d154-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="5d154-126">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d154-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5d154-127">Acht Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="5d154-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="5d154-128">**Tangens**</span><span class="sxs-lookup"><span data-stu-id="5d154-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="5d154-129">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d154-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5d154-130">Tangens</span><span class="sxs-lookup"><span data-stu-id="5d154-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="5d154-131">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="5d154-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="5d154-132">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d154-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5d154-133">Binormal</span><span class="sxs-lookup"><span data-stu-id="5d154-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="5d154-134">**Mosaik Faktor**</span><span class="sxs-lookup"><span data-stu-id="5d154-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="5d154-135">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d154-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5d154-136">Mosaik Faktor</span><span class="sxs-lookup"><span data-stu-id="5d154-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d154-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d154-137">Remarks</span></span>

<span data-ttu-id="5d154-138">Der LPD3DXWeldEpsilons-Typ wird als Zeiger auf die D3DXWeldEpsilons-Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="5d154-138">The LPD3DXWeldEpsilons type is defined as a pointer to the D3DXWeldEpsilons structure.</span></span>


```
typedef D3DX_WELD_EPSILONS *LPD3DX_WELD_EPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="5d154-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d154-139">Requirements</span></span>



| <span data-ttu-id="5d154-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d154-140">Requirement</span></span> | <span data-ttu-id="5d154-141">Wert</span><span class="sxs-lookup"><span data-stu-id="5d154-141">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5d154-142">Header</span><span class="sxs-lookup"><span data-stu-id="5d154-142">Header</span></span><br/> | <dl> <span data-ttu-id="5d154-143"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d154-143"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d154-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d154-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d154-145">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="5d154-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
