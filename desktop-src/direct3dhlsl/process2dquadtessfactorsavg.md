---
title: Process2DQuadTessFactorsAvg-Funktion
description: Generiert die korrigierten Mosaik Faktoren für einen Quad-Patch. | Process2DQuadTessFactorsAvg-Funktion
ms.assetid: 7f96f634-0ad5-4037-a08e-b0b99b89cd91
keywords:
- Process2DQuadTessFactorsAvg-Funktion (HLSL)
topic_type:
- apiref
api_name:
- Process2DQuadTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4012d99a1f7714fae68f4679991aedcf810d1b4e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761655"
---
# <a name="process2dquadtessfactorsavg-function"></a><span data-ttu-id="484de-105">Process2DQuadTessFactorsAvg-Funktion</span><span class="sxs-lookup"><span data-stu-id="484de-105">Process2DQuadTessFactorsAvg function</span></span>

<span data-ttu-id="484de-106">Generiert die korrigierten Mosaik Faktoren für einen Quad-Patch.</span><span class="sxs-lookup"><span data-stu-id="484de-106">Generates the corrected tessellation factors for a quad patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="484de-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="484de-107">Syntax</span></span>

``` syntax
void Process2DQuadTessFactorsAvg(
  in  float4 RawEdgeFactors,
  in  float2 InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a><span data-ttu-id="484de-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="484de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="484de-109">*Rawedgefactors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="484de-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="484de-110">Typ: **float4**</span><span class="sxs-lookup"><span data-stu-id="484de-110">Type: **float4**</span></span>

<span data-ttu-id="484de-111">Die Edge-Mosaik Faktoren, die an die Mosaik Phase übergebenen werden.</span><span class="sxs-lookup"><span data-stu-id="484de-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="484de-112">*Insidescale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="484de-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="484de-113">Typ: **float2**</span><span class="sxs-lookup"><span data-stu-id="484de-113">Type: **float2**</span></span>

<span data-ttu-id="484de-114">Der Skalierungsfaktor, der auf die von der Mosaik Phase berechneten UV-Mosaik Faktoren angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="484de-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="484de-115">Der zulässige Bereich für insidescale liegt zwischen 0,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="484de-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="484de-116">*Roundebug Factors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="484de-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="484de-117">Typ: **float4**</span><span class="sxs-lookup"><span data-stu-id="484de-117">Type: **float4**</span></span>

<span data-ttu-id="484de-118">Die gerundeten Edge-Mosaik Faktoren, die von der Mosaik Phase berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="484de-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="484de-119">*Rounabdinsidetess Factors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="484de-119">*RoundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="484de-120">Typ: **float2**</span><span class="sxs-lookup"><span data-stu-id="484de-120">Type: **float2**</span></span>

<span data-ttu-id="484de-121">Die gerundeten Mosaik Faktoren, die von der Mosaik Phase für innere Ränder berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="484de-121">The rounded tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> <dt>

<span data-ttu-id="484de-122">*Unroundecodinsidetess Factors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="484de-122">*UnroundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="484de-123">Typ: **float2**</span><span class="sxs-lookup"><span data-stu-id="484de-123">Type: **float2**</span></span>

<span data-ttu-id="484de-124">Die Mosaik Faktoren, die von der Mosaik Phase für innere Ränder berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="484de-124">The tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="484de-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="484de-125">Return value</span></span>

<span data-ttu-id="484de-126">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="484de-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="484de-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="484de-127">Remarks</span></span>

<span data-ttu-id="484de-128">Generiert die korrigierten Mosaik Faktoren für einen Quad-Patch, wobei die in Mosaik Faktoren als Durchschnitt der Edge-Mosaik Faktoren berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="484de-128">Generates the corrected tessellation factors for a quad patch, computing the inside tessellation factors as the average of the edge tessellation factors.</span></span> <span data-ttu-id="484de-129">Die Erfassungs Faktoren "You" und "V" werden unabhängig von dem Mittelwert der gegenüberliegenden Seite der Domäne berechnet und dann nach insidescale skaliert.</span><span class="sxs-lookup"><span data-stu-id="484de-129">The U and V inside tessellation factors are computed independently using the average of opposing sides of the domain, then are scaled by InsideScale.</span></span> <span data-ttu-id="484de-130">Das Ergebnis wird dann basierend auf dem Partitionierungs Modus abgerundet, aber die nicht gerundeten Ergebnisse sind mithilfe des Parameters unroundedinsidetess Factors verfügbar.</span><span class="sxs-lookup"><span data-stu-id="484de-130">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactors parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="484de-131">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="484de-131">Minimum Shader Model</span></span>

<span data-ttu-id="484de-132">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="484de-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="484de-133">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="484de-133">Shader Model</span></span>                                                                | <span data-ttu-id="484de-134">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="484de-134">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="484de-135">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="484de-135">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="484de-136">ja</span><span class="sxs-lookup"><span data-stu-id="484de-136">yes</span></span>       |



 

<span data-ttu-id="484de-137">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="484de-137">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="484de-138">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="484de-138">Vertex</span></span> | <span data-ttu-id="484de-139">Hülle</span><span class="sxs-lookup"><span data-stu-id="484de-139">Hull</span></span> | <span data-ttu-id="484de-140">Domain</span><span class="sxs-lookup"><span data-stu-id="484de-140">Domain</span></span> | <span data-ttu-id="484de-141">Geometrie</span><span class="sxs-lookup"><span data-stu-id="484de-141">Geometry</span></span> | <span data-ttu-id="484de-142">Pixel</span><span class="sxs-lookup"><span data-stu-id="484de-142">Pixel</span></span> | <span data-ttu-id="484de-143">Compute</span><span class="sxs-lookup"><span data-stu-id="484de-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="484de-144">x</span><span class="sxs-lookup"><span data-stu-id="484de-144">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="484de-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="484de-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="484de-146">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="484de-146">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="484de-147">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="484de-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




