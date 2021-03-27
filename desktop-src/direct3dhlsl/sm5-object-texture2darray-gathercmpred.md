---
title: 'Texture2DArray:: gathercmpred (S, float, float, int)-Funktion'
description: 'Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der roten Komponente mit einem Vergleichswert zurückgegeben. | Texture2DArray:: gathercmpred (S, float, float, int)-Funktion'
ms.assetid: aa7fadf8-fe96-406a-9c93-9ae0c59ef087
keywords:
- Gathercmpred-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3cf0f7094c7e535a84e6d8fd6ba7e87bb702dbfd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995511"
---
# <a name="texture2darraygathercmpredsfloatfloatint-function"></a><span data-ttu-id="502f1-105">Texture2DArray:: gathercmpred (S, float, float, int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="502f1-105">Texture2DArray::GatherCmpRed(S,float,float,int) function</span></span>

<span data-ttu-id="502f1-106">Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der roten Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="502f1-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="502f1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="502f1-107">Syntax</span></span>

``` syntax
float4 GatherCmpRed(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="502f1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="502f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="502f1-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="502f1-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="502f1-110">Typ: **samplercomparisonstate**</span><span class="sxs-lookup"><span data-stu-id="502f1-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="502f1-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="502f1-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="502f1-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="502f1-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="502f1-113">Typ: **float3**</span><span class="sxs-lookup"><span data-stu-id="502f1-113">Type: **float3**</span></span>

<span data-ttu-id="502f1-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="502f1-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="502f1-115">*\_ Wert vergleichen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="502f1-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="502f1-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="502f1-116">Type: **float**</span></span>

<span data-ttu-id="502f1-117">Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="502f1-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="502f1-118">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="502f1-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="502f1-119">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="502f1-119">Type: **int2**</span></span>

<span data-ttu-id="502f1-120">Ein Offset, der vor der Stichprobenentnahme auf die Textur Koordinate angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="502f1-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="502f1-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="502f1-121">Return value</span></span>

<span data-ttu-id="502f1-122">Typ: **float4**</span><span class="sxs-lookup"><span data-stu-id="502f1-122">Type: **float4**</span></span>

<span data-ttu-id="502f1-123">Ein vier komponentenwert, wobei jede Komponente das Ergebnis eines Vergleichs pro Komponente ist.</span><span class="sxs-lookup"><span data-stu-id="502f1-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="502f1-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="502f1-124">Remarks</span></span>

<span data-ttu-id="502f1-125">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="502f1-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="502f1-126">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="502f1-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="502f1-127">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="502f1-127">Vertex</span></span> | <span data-ttu-id="502f1-128">Hülle</span><span class="sxs-lookup"><span data-stu-id="502f1-128">Hull</span></span> | <span data-ttu-id="502f1-129">Domain</span><span class="sxs-lookup"><span data-stu-id="502f1-129">Domain</span></span> | <span data-ttu-id="502f1-130">Geometrie</span><span class="sxs-lookup"><span data-stu-id="502f1-130">Geometry</span></span> | <span data-ttu-id="502f1-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="502f1-131">Pixel</span></span> | <span data-ttu-id="502f1-132">Compute</span><span class="sxs-lookup"><span data-stu-id="502f1-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="502f1-133">x</span><span class="sxs-lookup"><span data-stu-id="502f1-133">x</span></span>      | <span data-ttu-id="502f1-134">x</span><span class="sxs-lookup"><span data-stu-id="502f1-134">x</span></span>    | <span data-ttu-id="502f1-135">x</span><span class="sxs-lookup"><span data-stu-id="502f1-135">x</span></span>      | <span data-ttu-id="502f1-136">x</span><span class="sxs-lookup"><span data-stu-id="502f1-136">x</span></span>        | <span data-ttu-id="502f1-137">x</span><span class="sxs-lookup"><span data-stu-id="502f1-137">x</span></span>     | <span data-ttu-id="502f1-138">x</span><span class="sxs-lookup"><span data-stu-id="502f1-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="502f1-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="502f1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="502f1-140">Gathercmpred-Methoden</span><span class="sxs-lookup"><span data-stu-id="502f1-140">GatherCmpRed methods</span></span>](texture2darray-gathercmpred.md)
</dt> <dt>

[<span data-ttu-id="502f1-141">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="502f1-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




