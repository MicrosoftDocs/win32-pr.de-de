---
title: Processtritess factorsavg-Funktion
description: Generiert die korrigierten Mosaik Faktoren für einen Tri-Patch. | Processtritess factorsavg-Funktion
ms.assetid: 005a63b6-f35d-42d6-bb29-f4ebb374080e
keywords:
- Processtritesfactorsavg-Funktion HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90cfa86a09e0e76c90f0013cfa6121917ca25378
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995430"
---
# <a name="processtritessfactorsavg-function"></a><span data-ttu-id="19686-105">Processtritess factorsavg-Funktion</span><span class="sxs-lookup"><span data-stu-id="19686-105">ProcessTriTessFactorsAvg function</span></span>

<span data-ttu-id="19686-106">Generiert die korrigierten Mosaik Faktoren für einen Tri-Patch.</span><span class="sxs-lookup"><span data-stu-id="19686-106">Generates the corrected tessellation factors for a tri patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="19686-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="19686-107">Syntax</span></span>

``` syntax
void ProcessTriTessFactorsAvg(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactor,
  out float UnroundedInsideTessFactor
);
```

## <a name="parameters"></a><span data-ttu-id="19686-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="19686-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19686-109">*Rawedgefactors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19686-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19686-110">Typ: **float3**</span><span class="sxs-lookup"><span data-stu-id="19686-110">Type: **float3**</span></span>

<span data-ttu-id="19686-111">Die Edge-Mosaik Faktoren, die an die Mosaik Phase übergebenen werden.</span><span class="sxs-lookup"><span data-stu-id="19686-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="19686-112">*Insidescale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19686-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19686-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="19686-113">Type: **float**</span></span>

<span data-ttu-id="19686-114">Der Skalierungsfaktor, der auf die von der Mosaik Phase berechneten UV-Mosaik Faktoren angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="19686-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="19686-115">Der zulässige Bereich für insidescale liegt zwischen 0,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="19686-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="19686-116">*Roundebug Factors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="19686-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19686-117">Typ: **float3**</span><span class="sxs-lookup"><span data-stu-id="19686-117">Type: **float3**</span></span>

<span data-ttu-id="19686-118">Die gerundeten Edge-Mosaik Faktoren, die von der Mosaik Phase berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="19686-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="19686-119">*Rounabdinsidetess Factor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="19686-119">*RoundedInsideTessFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19686-120">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="19686-120">Type: **float**</span></span>

<span data-ttu-id="19686-121">Die Mosaik Faktoren, die von der Mosaik Stufe berechnet werden, und gerundet.</span><span class="sxs-lookup"><span data-stu-id="19686-121">The tessellation factors calculated by the tessellator stage, and rounded.</span></span>

</dd> <dt>

<span data-ttu-id="19686-122">*Unroundecodinsidetess Factor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="19686-122">*UnroundedInsideTessFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19686-123">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="19686-123">Type: **float**</span></span>

<span data-ttu-id="19686-124">Die ursprünglichen, nicht abgerundeten, von der Mosaik Phase berechneten UV-Mosaik Faktoren.</span><span class="sxs-lookup"><span data-stu-id="19686-124">The original, unrounded, UV tessellation factors computed by the tessellation stage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19686-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19686-125">Return value</span></span>

<span data-ttu-id="19686-126">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="19686-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="19686-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19686-127">Remarks</span></span>

<span data-ttu-id="19686-128">Generiert die korrigierten Mosaik Faktoren für einen Tri-Patch, der den inneren Mosaik Faktor als Mittelwert der Edge-Mosaik Faktoren berechnet, der dann von insidescale skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="19686-128">Generates the corrected tessellation factors for a tri patch, computing the inside tessellation factor as the average of the edge tessellation factors, which is then scaled by InsideScale.</span></span> <span data-ttu-id="19686-129">Das Ergebnis wird dann basierend auf dem Partitionierungs Modus abgerundet, aber die nicht gerundeten Ergebnisse sind mit dem unroundedinsidetess Factor-Parameter verfügbar.</span><span class="sxs-lookup"><span data-stu-id="19686-129">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactor parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="19686-130">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="19686-130">Minimum Shader Model</span></span>

<span data-ttu-id="19686-131">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19686-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="19686-132">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="19686-132">Shader Model</span></span>                                                                | <span data-ttu-id="19686-133">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="19686-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="19686-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="19686-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="19686-135">ja</span><span class="sxs-lookup"><span data-stu-id="19686-135">yes</span></span>       |



 

<span data-ttu-id="19686-136">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="19686-136">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="19686-137">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="19686-137">Vertex</span></span> | <span data-ttu-id="19686-138">Hülle</span><span class="sxs-lookup"><span data-stu-id="19686-138">Hull</span></span> | <span data-ttu-id="19686-139">Domain</span><span class="sxs-lookup"><span data-stu-id="19686-139">Domain</span></span> | <span data-ttu-id="19686-140">Geometrie</span><span class="sxs-lookup"><span data-stu-id="19686-140">Geometry</span></span> | <span data-ttu-id="19686-141">Pixel</span><span class="sxs-lookup"><span data-stu-id="19686-141">Pixel</span></span> | <span data-ttu-id="19686-142">Compute</span><span class="sxs-lookup"><span data-stu-id="19686-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="19686-143">x</span><span class="sxs-lookup"><span data-stu-id="19686-143">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="19686-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="19686-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19686-145">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="19686-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="19686-146">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="19686-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




