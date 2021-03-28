---
title: 'Samplegrad:: samplegrad (S, float, float, float, int, float)-Funktion für Texture1D'
description: Die-Funktion gibt eine Stichprobe für eine Textur aus und verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, wie der Beispiel Speicherort berechnet wird
ms.assetid: 34A79CB6-0C45-40ED-845C-77C08F1DEC57
keywords:
- Samplegrad-Funktion HLSL
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c6222d8fa9548e3154abf7605fc5032dd67235a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982748"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture1d"></a><span data-ttu-id="b1902-104">Samplegrad:: samplegrad (S, float, float, float, int, float)-Funktion für Texture1D</span><span class="sxs-lookup"><span data-stu-id="b1902-104">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture1D</span></span>

<span data-ttu-id="b1902-105">Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, wie der Beispiel Speicherort berechnet wird, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) fixiert werden.</span><span class="sxs-lookup"><span data-stu-id="b1902-105">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1902-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1902-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="b1902-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1902-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1902-108">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1902-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1902-109">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="b1902-109">Type: **SamplerState**</span></span>

<span data-ttu-id="b1902-110">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="b1902-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="b1902-111">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="b1902-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="b1902-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1902-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1902-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="b1902-113">Type: **float**</span></span>

<span data-ttu-id="b1902-114">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="b1902-114">The texture coordinates.</span></span> <span data-ttu-id="b1902-115">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="b1902-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="b1902-116">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="b1902-116">Texture-Object Type</span></span>                    | <span data-ttu-id="b1902-117">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="b1902-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="b1902-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b1902-118">Texture1D</span></span>                              | <span data-ttu-id="b1902-119">float</span><span class="sxs-lookup"><span data-stu-id="b1902-119">float</span></span>          |
| <span data-ttu-id="b1902-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="b1902-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="b1902-121">float2</span><span class="sxs-lookup"><span data-stu-id="b1902-121">float2</span></span>         |
| <span data-ttu-id="b1902-122">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="b1902-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="b1902-123">float3</span><span class="sxs-lookup"><span data-stu-id="b1902-123">float3</span></span>         |
| <span data-ttu-id="b1902-124">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="b1902-124">TextureCubeArray</span></span>                       | <span data-ttu-id="b1902-125">float4</span><span class="sxs-lookup"><span data-stu-id="b1902-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="b1902-126">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1902-126">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1902-127">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="b1902-127">Type: **float**</span></span>

<span data-ttu-id="b1902-128">Die Änderungs Rate der Oberflächengeometrie in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="b1902-128">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="b1902-129">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="b1902-129">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="b1902-130">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="b1902-130">Texture-Object Type</span></span>                      | <span data-ttu-id="b1902-131">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="b1902-131">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="b1902-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="b1902-132">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="b1902-133">float</span><span class="sxs-lookup"><span data-stu-id="b1902-133">float</span></span>          |
| <span data-ttu-id="b1902-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="b1902-134">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="b1902-135">float2</span><span class="sxs-lookup"><span data-stu-id="b1902-135">float2</span></span>         |
| <span data-ttu-id="b1902-136">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="b1902-136">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="b1902-137">float3</span><span class="sxs-lookup"><span data-stu-id="b1902-137">float3</span></span>         |
| <span data-ttu-id="b1902-138">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="b1902-138">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="b1902-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b1902-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="b1902-140">Nicht mehr  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1902-140">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1902-141">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="b1902-141">Type: **float**</span></span>

<span data-ttu-id="b1902-142">Die Änderungs Rate der Oberflächengeometrie in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="b1902-142">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="b1902-143">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="b1902-143">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="b1902-144">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="b1902-144">Texture-Object Type</span></span>                      | <span data-ttu-id="b1902-145">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="b1902-145">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="b1902-146">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="b1902-146">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="b1902-147">float</span><span class="sxs-lookup"><span data-stu-id="b1902-147">float</span></span>          |
| <span data-ttu-id="b1902-148">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="b1902-148">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="b1902-149">float2</span><span class="sxs-lookup"><span data-stu-id="b1902-149">float2</span></span>         |
| <span data-ttu-id="b1902-150">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="b1902-150">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="b1902-151">float3</span><span class="sxs-lookup"><span data-stu-id="b1902-151">float3</span></span>         |
| <span data-ttu-id="b1902-152">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="b1902-152">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="b1902-153">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b1902-153">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="b1902-154">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1902-154">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1902-155">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="b1902-155">Type: **int**</span></span>

<span data-ttu-id="b1902-156">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="b1902-156">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="b1902-157">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="b1902-157">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="b1902-158">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="b1902-158">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="b1902-159">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="b1902-159">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="b1902-160">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="b1902-160">Texture-Object Type</span></span>           | <span data-ttu-id="b1902-161">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="b1902-161">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="b1902-162">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="b1902-162">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="b1902-163">INT</span><span class="sxs-lookup"><span data-stu-id="b1902-163">int</span></span>            |
| <span data-ttu-id="b1902-164">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="b1902-164">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="b1902-165">int2</span><span class="sxs-lookup"><span data-stu-id="b1902-165">int2</span></span>           |
| <span data-ttu-id="b1902-166">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b1902-166">Texture3D</span></span>                     | <span data-ttu-id="b1902-167">int3</span><span class="sxs-lookup"><span data-stu-id="b1902-167">int3</span></span>           |
| <span data-ttu-id="b1902-168">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="b1902-168">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="b1902-169">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b1902-169">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="b1902-170">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1902-170">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1902-171">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="b1902-171">Type: **float**</span></span>

<span data-ttu-id="b1902-172">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="b1902-172">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="b1902-173">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="b1902-173">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1902-174">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1902-174">Return value</span></span>

<span data-ttu-id="b1902-175">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="b1902-175">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="b1902-176">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="b1902-176">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="b1902-177">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b1902-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1902-178">Samplegrad-Methoden</span><span class="sxs-lookup"><span data-stu-id="b1902-178">SampleGrad methods</span></span>](texture1d-samplegrad.md)
</dt> </dl>

 

 
