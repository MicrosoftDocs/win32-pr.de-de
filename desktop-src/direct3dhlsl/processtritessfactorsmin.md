---
title: Processtritesfactorsmin-Funktion
description: Generiert die korrigierten Mosaik Faktoren für einen Tri-Patch. | Processtritesfactorsmin-Funktion
ms.assetid: fa1e19c2-fadf-42d4-9574-834eaf871393
keywords:
- Processtritesfactorsmin-Funktion HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f82c7935d47813d833ccc21a7ec0134adee1cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530650"
---
# <a name="processtritessfactorsmin-function"></a><span data-ttu-id="e1186-105">Processtritesfactorsmin-Funktion</span><span class="sxs-lookup"><span data-stu-id="e1186-105">ProcessTriTessFactorsMin function</span></span>

<span data-ttu-id="e1186-106">Generiert die korrigierten Mosaik Faktoren für einen Tri-Patch.</span><span class="sxs-lookup"><span data-stu-id="e1186-106">Generates the corrected tessellation factors for a tri patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1186-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1186-107">Syntax</span></span>

``` syntax
void ProcessTriTessFactorsMin(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactors,
  out float UnroundedInsideTessFactors
);
```

## <a name="parameters"></a><span data-ttu-id="e1186-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1186-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1186-109">*Rawedgefactors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1186-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1186-110">Typ: **float3**</span><span class="sxs-lookup"><span data-stu-id="e1186-110">Type: **float3**</span></span>

<span data-ttu-id="e1186-111">Die Edge-Mosaik Faktoren, die an die Mosaik Phase übergebenen werden.</span><span class="sxs-lookup"><span data-stu-id="e1186-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="e1186-112">*Insidescale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1186-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1186-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="e1186-113">Type: **float**</span></span>

<span data-ttu-id="e1186-114">Der Skalierungsfaktor, der auf die von der Mosaik Phase berechneten UV-Mosaik Faktoren angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e1186-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="e1186-115">Der zulässige Bereich für insidescale liegt zwischen 0,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="e1186-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="e1186-116">*Roundebug Factors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e1186-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1186-117">Typ: **float3**</span><span class="sxs-lookup"><span data-stu-id="e1186-117">Type: **float3**</span></span>

<span data-ttu-id="e1186-118">Die gerundeten Edge-Mosaik Faktoren, die von der Mosaik Phase berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="e1186-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="e1186-119">*Rounabdinsidetess Factors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e1186-119">*RoundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1186-120">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="e1186-120">Type: **float**</span></span>

<span data-ttu-id="e1186-121">Die gerundeten Mosaik Faktoren, die von der Mosaik Phase für innere Ränder berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="e1186-121">The rounded tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> <dt>

<span data-ttu-id="e1186-122">*Unroundecodinsidetess Factors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e1186-122">*UnroundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1186-123">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="e1186-123">Type: **float**</span></span>

<span data-ttu-id="e1186-124">Die Mosaik Faktoren, die von der Mosaik Phase für innere Ränder berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="e1186-124">The tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1186-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e1186-125">Return value</span></span>

<span data-ttu-id="e1186-126">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e1186-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1186-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1186-127">Remarks</span></span>

<span data-ttu-id="e1186-128">Generiert die korrigierten Mosaik Faktoren für einen Tri-Patch und berechnet den internen Mosaik Faktor als Minimalwert der Edge-Mosaik Faktoren, der dann von insidescale skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="e1186-128">Generates the corrected tessellation factors for a tri patch, computing the inside tessellation factor as the minimum of the edge tessellation factors, which is then scaled by InsideScale.</span></span> <span data-ttu-id="e1186-129">Das Ergebnis wird dann basierend auf dem Partitionierungs Modus abgerundet, aber die nicht gerundeten Ergebnisse sind mit dem unroundedinsidetess Factor-Parameter verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1186-129">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactor parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="e1186-130">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="e1186-130">Minimum Shader Model</span></span>

<span data-ttu-id="e1186-131">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e1186-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e1186-132">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="e1186-132">Shader Model</span></span>                                                                | <span data-ttu-id="e1186-133">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="e1186-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e1186-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="e1186-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="e1186-135">ja</span><span class="sxs-lookup"><span data-stu-id="e1186-135">yes</span></span>       |



 

<span data-ttu-id="e1186-136">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e1186-136">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="e1186-137">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="e1186-137">Vertex</span></span> | <span data-ttu-id="e1186-138">Hülle</span><span class="sxs-lookup"><span data-stu-id="e1186-138">Hull</span></span> | <span data-ttu-id="e1186-139">Domain</span><span class="sxs-lookup"><span data-stu-id="e1186-139">Domain</span></span> | <span data-ttu-id="e1186-140">Geometrie</span><span class="sxs-lookup"><span data-stu-id="e1186-140">Geometry</span></span> | <span data-ttu-id="e1186-141">Pixel</span><span class="sxs-lookup"><span data-stu-id="e1186-141">Pixel</span></span> | <span data-ttu-id="e1186-142">Compute</span><span class="sxs-lookup"><span data-stu-id="e1186-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="e1186-143">x</span><span class="sxs-lookup"><span data-stu-id="e1186-143">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="e1186-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e1186-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1186-145">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="e1186-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="e1186-146">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="e1186-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




