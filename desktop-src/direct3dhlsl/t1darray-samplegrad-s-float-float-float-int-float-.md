---
title: 'Samplegrad:: samplegrad (S, float, float, float, int, float)-Funktion für Texture1DArray'
description: Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, wie der Beispiel Speicherort berechnet wird, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) fixiert werden. Für Texture1DArray.
ms.assetid: 328EEC75-1E0A-4196-AD82-A48F3C66D65B
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
ms.openlocfilehash: e4af761ab82492fd49a4f6f048c74016a19aa872
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982740"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture1darray"></a><span data-ttu-id="8faef-105">Samplegrad:: samplegrad (S, float, float, float, int, float)-Funktion für Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="8faef-105">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture1DArray</span></span>

<span data-ttu-id="8faef-106">Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, wie der Beispiel Speicherort berechnet wird, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) fixiert werden.</span><span class="sxs-lookup"><span data-stu-id="8faef-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="8faef-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8faef-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="8faef-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8faef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8faef-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8faef-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8faef-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="8faef-110">Type: **SamplerState**</span></span>

<span data-ttu-id="8faef-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="8faef-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="8faef-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="8faef-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="8faef-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8faef-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8faef-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="8faef-114">Type: **float**</span></span>

<span data-ttu-id="8faef-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="8faef-115">The texture coordinates.</span></span> <span data-ttu-id="8faef-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="8faef-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="8faef-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="8faef-117">Texture-Object Type</span></span>                    | <span data-ttu-id="8faef-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="8faef-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="8faef-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="8faef-119">Texture1D</span></span>                              | <span data-ttu-id="8faef-120">float</span><span class="sxs-lookup"><span data-stu-id="8faef-120">float</span></span>          |
| <span data-ttu-id="8faef-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="8faef-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="8faef-122">float2</span><span class="sxs-lookup"><span data-stu-id="8faef-122">float2</span></span>         |
| <span data-ttu-id="8faef-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="8faef-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="8faef-124">float3</span><span class="sxs-lookup"><span data-stu-id="8faef-124">float3</span></span>         |
| <span data-ttu-id="8faef-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="8faef-125">TextureCubeArray</span></span>                       | <span data-ttu-id="8faef-126">float4</span><span class="sxs-lookup"><span data-stu-id="8faef-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="8faef-127">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8faef-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8faef-128">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="8faef-128">Type: **float**</span></span>

<span data-ttu-id="8faef-129">Die Änderungs Rate der Oberflächengeometrie in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="8faef-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="8faef-130">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="8faef-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="8faef-131">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="8faef-131">Texture-Object Type</span></span>                      | <span data-ttu-id="8faef-132">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="8faef-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="8faef-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="8faef-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="8faef-134">float</span><span class="sxs-lookup"><span data-stu-id="8faef-134">float</span></span>          |
| <span data-ttu-id="8faef-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="8faef-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="8faef-136">float2</span><span class="sxs-lookup"><span data-stu-id="8faef-136">float2</span></span>         |
| <span data-ttu-id="8faef-137">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="8faef-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="8faef-138">float3</span><span class="sxs-lookup"><span data-stu-id="8faef-138">float3</span></span>         |
| <span data-ttu-id="8faef-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="8faef-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="8faef-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8faef-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="8faef-141">Nicht mehr  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8faef-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8faef-142">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="8faef-142">Type: **float**</span></span>

<span data-ttu-id="8faef-143">Die Änderungs Rate der Oberflächengeometrie in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="8faef-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="8faef-144">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="8faef-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="8faef-145">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="8faef-145">Texture-Object Type</span></span>                      | <span data-ttu-id="8faef-146">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="8faef-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="8faef-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="8faef-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="8faef-148">float</span><span class="sxs-lookup"><span data-stu-id="8faef-148">float</span></span>          |
| <span data-ttu-id="8faef-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="8faef-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="8faef-150">float2</span><span class="sxs-lookup"><span data-stu-id="8faef-150">float2</span></span>         |
| <span data-ttu-id="8faef-151">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="8faef-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="8faef-152">float3</span><span class="sxs-lookup"><span data-stu-id="8faef-152">float3</span></span>         |
| <span data-ttu-id="8faef-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="8faef-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="8faef-154">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8faef-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="8faef-155">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8faef-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8faef-156">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="8faef-156">Type: **int**</span></span>

<span data-ttu-id="8faef-157">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="8faef-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="8faef-158">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="8faef-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="8faef-159">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="8faef-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="8faef-160">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="8faef-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="8faef-161">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="8faef-161">Texture-Object Type</span></span>           | <span data-ttu-id="8faef-162">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="8faef-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="8faef-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="8faef-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="8faef-164">INT</span><span class="sxs-lookup"><span data-stu-id="8faef-164">int</span></span>            |
| <span data-ttu-id="8faef-165">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="8faef-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="8faef-166">int2</span><span class="sxs-lookup"><span data-stu-id="8faef-166">int2</span></span>           |
| <span data-ttu-id="8faef-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="8faef-167">Texture3D</span></span>                     | <span data-ttu-id="8faef-168">int3</span><span class="sxs-lookup"><span data-stu-id="8faef-168">int3</span></span>           |
| <span data-ttu-id="8faef-169">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="8faef-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="8faef-170">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8faef-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="8faef-171">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8faef-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8faef-172">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="8faef-172">Type: **float**</span></span>

<span data-ttu-id="8faef-173">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="8faef-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="8faef-174">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="8faef-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8faef-175">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8faef-175">Return value</span></span>

<span data-ttu-id="8faef-176">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="8faef-176">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="8faef-177">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="8faef-177">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="8faef-178">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8faef-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8faef-179">Samplegrad-Methoden</span><span class="sxs-lookup"><span data-stu-id="8faef-179">SampleGrad methods</span></span>](texture1darray-samplegrad.md)
</dt> </dl>

 

 
