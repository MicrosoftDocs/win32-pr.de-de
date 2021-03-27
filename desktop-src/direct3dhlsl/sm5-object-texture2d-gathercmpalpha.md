---
title: 'Texture2D:: gathercmpalpha (S, float, float, int)-Funktion'
description: 'Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der Alpha Komponente mit einem Vergleichswert zurückgegeben. | Texture2D:: gathercmpalpha (S, float, float, int)-Funktion'
ms.assetid: 6fa60604-1eac-405d-bffa-3055569b7a09
keywords:
- Gathercmpalpha-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a7f7fcdc6e24cac5c04068fda7f781d0bdd376a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104393910"
---
# <a name="texture2dgathercmpalphasfloatfloatint-function"></a><span data-ttu-id="8842a-105">Texture2D:: gathercmpalpha (S, float, float, int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="8842a-105">Texture2D::GatherCmpAlpha(S,float,float,int) function</span></span>

<span data-ttu-id="8842a-106">Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der Alpha Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8842a-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8842a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8842a-107">Syntax</span></span>

``` syntax
float4 GatherCmpAlpha(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="8842a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8842a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8842a-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8842a-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8842a-110">Typ: **samplercomparisonstate**</span><span class="sxs-lookup"><span data-stu-id="8842a-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="8842a-111">Der null basierte samplerindex.</span><span class="sxs-lookup"><span data-stu-id="8842a-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="8842a-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8842a-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8842a-113">Typ: **float2**</span><span class="sxs-lookup"><span data-stu-id="8842a-113">Type: **float2**</span></span>

<span data-ttu-id="8842a-114">Die Beispiel Koordinaten (u, v).</span><span class="sxs-lookup"><span data-stu-id="8842a-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="8842a-115">*\_ Wert vergleichen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8842a-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8842a-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="8842a-116">Type: **float**</span></span>

<span data-ttu-id="8842a-117">Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8842a-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="8842a-118">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8842a-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8842a-119">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="8842a-119">Type: **int2**</span></span>

<span data-ttu-id="8842a-120">Ein Offset, der vor der Stichprobenentnahme auf die Textur Koordinate angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8842a-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8842a-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8842a-121">Return value</span></span>

<span data-ttu-id="8842a-122">Typ: **float4**</span><span class="sxs-lookup"><span data-stu-id="8842a-122">Type: **float4**</span></span>

<span data-ttu-id="8842a-123">Ein vier komponentenwert, wobei jede Komponente das Ergebnis eines Vergleichs pro Komponente ist.</span><span class="sxs-lookup"><span data-stu-id="8842a-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="8842a-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8842a-124">Remarks</span></span>

<span data-ttu-id="8842a-125">Die Textur Beispiele können für bilineare Interpolationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8842a-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="8842a-126">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="8842a-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8842a-127">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="8842a-127">Vertex</span></span> | <span data-ttu-id="8842a-128">Hülle</span><span class="sxs-lookup"><span data-stu-id="8842a-128">Hull</span></span> | <span data-ttu-id="8842a-129">Domain</span><span class="sxs-lookup"><span data-stu-id="8842a-129">Domain</span></span> | <span data-ttu-id="8842a-130">Geometrie</span><span class="sxs-lookup"><span data-stu-id="8842a-130">Geometry</span></span> | <span data-ttu-id="8842a-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="8842a-131">Pixel</span></span> | <span data-ttu-id="8842a-132">Compute</span><span class="sxs-lookup"><span data-stu-id="8842a-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8842a-133">x</span><span class="sxs-lookup"><span data-stu-id="8842a-133">x</span></span>      | <span data-ttu-id="8842a-134">x</span><span class="sxs-lookup"><span data-stu-id="8842a-134">x</span></span>    | <span data-ttu-id="8842a-135">x</span><span class="sxs-lookup"><span data-stu-id="8842a-135">x</span></span>      | <span data-ttu-id="8842a-136">x</span><span class="sxs-lookup"><span data-stu-id="8842a-136">x</span></span>        | <span data-ttu-id="8842a-137">x</span><span class="sxs-lookup"><span data-stu-id="8842a-137">x</span></span>     | <span data-ttu-id="8842a-138">x</span><span class="sxs-lookup"><span data-stu-id="8842a-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8842a-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8842a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8842a-140">Gathercmpalpha-Methoden</span><span class="sxs-lookup"><span data-stu-id="8842a-140">GatherCmpAlpha methods</span></span>](texture2d-gathercmpalpha.md)
</dt> <dt>

[<span data-ttu-id="8842a-141">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="8842a-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




