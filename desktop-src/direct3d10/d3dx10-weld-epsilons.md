---
description: 'D3DX10_WELD_EPSILONS-Struktur: Gibt Toleranzwerte für jede Scheitelpunktkomponente an, wenn Scheitelpunkte verglichen werden, um zu bestimmen, ob sie ähnlich genug sind, um zusammen zusammengestellt zu werden.'
ms.assetid: b28a17bd-5d5b-41b3-86d9-327f5497fc94
title: D3DX10_WELD_EPSILONS-Struktur (D3DX10.h)
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
ms.openlocfilehash: 720a10dbe4b22b69910d88d3c03cea9ded768f1b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105428"
---
# <a name="d3dx10_weld_epsilons-structure"></a><span data-ttu-id="976cb-103">D3DX10 \_ VERZEIGEN \_ EPSILONS-Struktur</span><span class="sxs-lookup"><span data-stu-id="976cb-103">D3DX10\_WELD\_EPSILONS structure</span></span>

<span data-ttu-id="976cb-104">Gibt Beim Vergleich von Scheitelpunkten Toleranzwerte für jede Scheitelpunktkomponente an, um zu bestimmen, ob sie ähnlich genug sind, um zusammengeknauft zu werden.</span><span class="sxs-lookup"><span data-stu-id="976cb-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="976cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="976cb-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="976cb-106">Member</span><span class="sxs-lookup"><span data-stu-id="976cb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="976cb-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="976cb-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="976cb-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="976cb-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="976cb-109">Position</span><span class="sxs-lookup"><span data-stu-id="976cb-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="976cb-110">**BlendWeights**</span><span class="sxs-lookup"><span data-stu-id="976cb-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="976cb-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="976cb-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="976cb-112">Mischungsgewichtung</span><span class="sxs-lookup"><span data-stu-id="976cb-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="976cb-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="976cb-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="976cb-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="976cb-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="976cb-115">Normal</span><span class="sxs-lookup"><span data-stu-id="976cb-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="976cb-116">**PSize**</span><span class="sxs-lookup"><span data-stu-id="976cb-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="976cb-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="976cb-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="976cb-118">Wert der Punktgröße</span><span class="sxs-lookup"><span data-stu-id="976cb-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="976cb-119">**Glänzend**</span><span class="sxs-lookup"><span data-stu-id="976cb-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="976cb-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="976cb-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="976cb-121">Glanzlichtwert</span><span class="sxs-lookup"><span data-stu-id="976cb-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="976cb-122">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="976cb-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="976cb-123">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="976cb-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="976cb-124">Diffuser Beleuchtungswert</span><span class="sxs-lookup"><span data-stu-id="976cb-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="976cb-125">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="976cb-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="976cb-126">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="976cb-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="976cb-127">Acht Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="976cb-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="976cb-128">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="976cb-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="976cb-129">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="976cb-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="976cb-130">Tangens</span><span class="sxs-lookup"><span data-stu-id="976cb-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="976cb-131">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="976cb-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="976cb-132">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="976cb-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="976cb-133">Binormal</span><span class="sxs-lookup"><span data-stu-id="976cb-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="976cb-134">**TessFactor**</span><span class="sxs-lookup"><span data-stu-id="976cb-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="976cb-135">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="976cb-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="976cb-136">Mosaikfaktor</span><span class="sxs-lookup"><span data-stu-id="976cb-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="976cb-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="976cb-137">Remarks</span></span>

<span data-ttu-id="976cb-138">Der LPD3DXWeldEpsilons-Typ ist als Zeiger auf die D3DXWeldEpsilons-Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="976cb-138">The LPD3DXWeldEpsilons type is defined as a pointer to the D3DXWeldEpsilons structure.</span></span>


```
typedef D3DX_WELD_EPSILONS *LPD3DX_WELD_EPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="976cb-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="976cb-139">Requirements</span></span>



| <span data-ttu-id="976cb-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="976cb-140">Requirement</span></span> | <span data-ttu-id="976cb-141">Wert</span><span class="sxs-lookup"><span data-stu-id="976cb-141">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="976cb-142">Header</span><span class="sxs-lookup"><span data-stu-id="976cb-142">Header</span></span><br/> | <dl> <span data-ttu-id="976cb-143"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="976cb-143"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="976cb-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="976cb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="976cb-145">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="976cb-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
