---
title: 'Texture2DArray:: gathercmpgreen (S, float, float, int)-Funktion'
description: 'Für vier textexwerte, die in einem bilinearen Filterungs Vorgang verwendet werden, wird ein Vergleich der grünen Komponente mit einem Vergleichswert zurückgegeben. | Texture2DArray:: gathercmpgreen (S, float, float, int)-Funktion'
ms.assetid: baf14de9-5237-42a5-bffc-848e55cbc28f
keywords:
- Gathercmpgreen-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f29da331d71c1fa8a2ceff783e4daec4a886d06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995715"
---
# <a name="texture2darraygathercmpgreensfloatfloatint-function"></a><span data-ttu-id="1f616-105">Texture2DArray:: gathercmpgreen (S, float, float, int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="1f616-105">Texture2DArray::GatherCmpGreen(S,float,float,int) function</span></span>

<span data-ttu-id="1f616-106">Für vier textexwerte, die in einem bilinearen Filterungs Vorgang verwendet werden, wird ein Vergleich der grünen Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1f616-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f616-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f616-107">Syntax</span></span>

``` syntax
float4 GatherCmpGreen(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="1f616-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f616-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f616-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f616-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f616-110">Typ: **samplercomparisonstate**</span><span class="sxs-lookup"><span data-stu-id="1f616-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="1f616-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="1f616-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="1f616-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f616-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f616-113">Typ: **float3**</span><span class="sxs-lookup"><span data-stu-id="1f616-113">Type: **float3**</span></span>

<span data-ttu-id="1f616-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="1f616-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="1f616-115">*\_ Wert vergleichen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f616-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f616-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="1f616-116">Type: **float**</span></span>

<span data-ttu-id="1f616-117">Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f616-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="1f616-118">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f616-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f616-119">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="1f616-119">Type: **int2**</span></span>

<span data-ttu-id="1f616-120">Ein Offset, der vor der Stichprobenentnahme auf die Textur Koordinate angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f616-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f616-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f616-121">Return value</span></span>

<span data-ttu-id="1f616-122">Typ: **float4**</span><span class="sxs-lookup"><span data-stu-id="1f616-122">Type: **float4**</span></span>

<span data-ttu-id="1f616-123">Ein vier komponentenwert, wobei jede Komponente das Ergebnis eines Vergleichs pro Komponente ist.</span><span class="sxs-lookup"><span data-stu-id="1f616-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f616-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f616-124">Remarks</span></span>

<span data-ttu-id="1f616-125">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f616-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="1f616-126">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1f616-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1f616-127">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="1f616-127">Vertex</span></span> | <span data-ttu-id="1f616-128">Hülle</span><span class="sxs-lookup"><span data-stu-id="1f616-128">Hull</span></span> | <span data-ttu-id="1f616-129">Domain</span><span class="sxs-lookup"><span data-stu-id="1f616-129">Domain</span></span> | <span data-ttu-id="1f616-130">Geometrie</span><span class="sxs-lookup"><span data-stu-id="1f616-130">Geometry</span></span> | <span data-ttu-id="1f616-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="1f616-131">Pixel</span></span> | <span data-ttu-id="1f616-132">Compute</span><span class="sxs-lookup"><span data-stu-id="1f616-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1f616-133">x</span><span class="sxs-lookup"><span data-stu-id="1f616-133">x</span></span>      | <span data-ttu-id="1f616-134">x</span><span class="sxs-lookup"><span data-stu-id="1f616-134">x</span></span>    | <span data-ttu-id="1f616-135">x</span><span class="sxs-lookup"><span data-stu-id="1f616-135">x</span></span>      | <span data-ttu-id="1f616-136">x</span><span class="sxs-lookup"><span data-stu-id="1f616-136">x</span></span>        | <span data-ttu-id="1f616-137">x</span><span class="sxs-lookup"><span data-stu-id="1f616-137">x</span></span>     | <span data-ttu-id="1f616-138">x</span><span class="sxs-lookup"><span data-stu-id="1f616-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1f616-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1f616-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f616-140">Gathercmpgreen-Methoden</span><span class="sxs-lookup"><span data-stu-id="1f616-140">GatherCmpGreen methods</span></span>](texture2darray-gathercmpgreen.md)
</dt> <dt>

[<span data-ttu-id="1f616-141">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="1f616-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




