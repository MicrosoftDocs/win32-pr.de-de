---
title: Process2DQuadTessFactorsMax-Funktion
description: Generiert die korrigierten Mosaik Faktoren für einen Quad-Patch. | Process2DQuadTessFactorsMax-Funktion
ms.assetid: 1de95946-d82d-42ba-93d7-ab8383fd5018
keywords:
- Process2DQuadTessFactorsMax-Funktion (HLSL)
topic_type:
- apiref
api_name:
- Process2DQuadTessFactorsMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d090c102671ec89fa347db95da2b21b5f11adcfe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995367"
---
# <a name="process2dquadtessfactorsmax-function"></a><span data-ttu-id="4787c-105">Process2DQuadTessFactorsMax-Funktion</span><span class="sxs-lookup"><span data-stu-id="4787c-105">Process2DQuadTessFactorsMax function</span></span>

<span data-ttu-id="4787c-106">Generiert die korrigierten Mosaik Faktoren für einen Quad-Patch.</span><span class="sxs-lookup"><span data-stu-id="4787c-106">Generates the corrected tessellation factors for a quad patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="4787c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4787c-107">Syntax</span></span>

``` syntax
void Process2DQuadTessFactorsMax(
  in  float4 RawEdgeFactors,
  in  float2 InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a><span data-ttu-id="4787c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4787c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4787c-109">*Rawedgefactors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4787c-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4787c-110">Typ: **float4**</span><span class="sxs-lookup"><span data-stu-id="4787c-110">Type: **float4**</span></span>

<span data-ttu-id="4787c-111">Die Edge-Mosaik Faktoren, die an die Mosaik Phase übergebenen werden.</span><span class="sxs-lookup"><span data-stu-id="4787c-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="4787c-112">*Insidescale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4787c-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4787c-113">Typ: **float2**</span><span class="sxs-lookup"><span data-stu-id="4787c-113">Type: **float2**</span></span>

<span data-ttu-id="4787c-114">Der Skalierungsfaktor, der auf die von der Mosaik Phase berechneten UV-Mosaik Faktoren angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4787c-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="4787c-115">Der zulässige Bereich für insidescale liegt zwischen 0,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="4787c-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="4787c-116">*Roundebug Factors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4787c-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4787c-117">Typ: **float4**</span><span class="sxs-lookup"><span data-stu-id="4787c-117">Type: **float4**</span></span>

<span data-ttu-id="4787c-118">Die gerundeten Edge-Mosaik Faktoren, die von der Mosaik Phase berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="4787c-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="4787c-119">*Rounabdinsidetess Factors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4787c-119">*RoundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4787c-120">Typ: **float2**</span><span class="sxs-lookup"><span data-stu-id="4787c-120">Type: **float2**</span></span>

<span data-ttu-id="4787c-121">Die gerundeten Mosaik Faktoren, die von der Mosaik Phase für innere Ränder berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="4787c-121">The rounded tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> <dt>

<span data-ttu-id="4787c-122">*Unroundecodinsidetess Factors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4787c-122">*UnroundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4787c-123">Typ: **float2**</span><span class="sxs-lookup"><span data-stu-id="4787c-123">Type: **float2**</span></span>

<span data-ttu-id="4787c-124">Die Mosaik Faktoren, die von der Mosaik Phase für innere Ränder berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="4787c-124">The tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4787c-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4787c-125">Return value</span></span>

<span data-ttu-id="4787c-126">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4787c-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4787c-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4787c-127">Remarks</span></span>

<span data-ttu-id="4787c-128">Generiert die korrigierten Mosaik Faktoren für einen Quad-Patch und berechnet die innerhalb der Mosaik Faktoren als Maximum der Edge-Mosaik Faktoren.</span><span class="sxs-lookup"><span data-stu-id="4787c-128">Generates the corrected tessellation factors for a quad patch, computing the inside tessellation factors as the maximum of the edge tessellation factors.</span></span> <span data-ttu-id="4787c-129">Die-und-V-innerhalb der Mosaik Faktoren werden unabhängig von den Höchstwerte der Gegenseite der Domäne berechnet und dann nach insidescale skaliert.</span><span class="sxs-lookup"><span data-stu-id="4787c-129">The U and V inside tessellation factors are computed independently using the maximums of opposing sides of the domain, then are scaled by InsideScale.</span></span> <span data-ttu-id="4787c-130">Das Ergebnis wird dann basierend auf dem Partitionierungs Modus abgerundet, aber die nicht gerundeten Ergebnisse sind mithilfe des Parameters unroundedinsidetess Factors verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4787c-130">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactors parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="4787c-131">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="4787c-131">Minimum Shader Model</span></span>

<span data-ttu-id="4787c-132">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4787c-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4787c-133">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="4787c-133">Shader Model</span></span>                                                                | <span data-ttu-id="4787c-134">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="4787c-134">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4787c-135">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="4787c-135">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="4787c-136">ja</span><span class="sxs-lookup"><span data-stu-id="4787c-136">yes</span></span>       |



 

<span data-ttu-id="4787c-137">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="4787c-137">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="4787c-138">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="4787c-138">Vertex</span></span> | <span data-ttu-id="4787c-139">Hülle</span><span class="sxs-lookup"><span data-stu-id="4787c-139">Hull</span></span> | <span data-ttu-id="4787c-140">Domain</span><span class="sxs-lookup"><span data-stu-id="4787c-140">Domain</span></span> | <span data-ttu-id="4787c-141">Geometrie</span><span class="sxs-lookup"><span data-stu-id="4787c-141">Geometry</span></span> | <span data-ttu-id="4787c-142">Pixel</span><span class="sxs-lookup"><span data-stu-id="4787c-142">Pixel</span></span> | <span data-ttu-id="4787c-143">Compute</span><span class="sxs-lookup"><span data-stu-id="4787c-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="4787c-144">x</span><span class="sxs-lookup"><span data-stu-id="4787c-144">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="4787c-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4787c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4787c-146">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="4787c-146">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="4787c-147">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="4787c-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




