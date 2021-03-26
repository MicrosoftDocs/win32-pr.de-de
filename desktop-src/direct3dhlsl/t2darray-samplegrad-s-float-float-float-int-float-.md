---
title: 'Samplegrad:: samplegrad (S, float, float, float, int, float)-Funktion für Texture2DArray'
description: Erfahren Sie, wie diese Funktion eine Textur Abtast, wobei ein Farbverlauf verwendet wird, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird Für Texture2DArray.
ms.assetid: CBC940D5-FC09-498D-9C7A-3CBAB2EC2D4D
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
ms.openlocfilehash: 032d2b228800ffca654704c85a72d5ada76e65ef
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982764"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture2darray"></a><span data-ttu-id="a4d95-105">Samplegrad:: samplegrad (S, float, float, float, int, float)-Funktion für Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a4d95-105">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture2DArray</span></span>

<span data-ttu-id="a4d95-106">Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, wie der Beispiel Speicherort berechnet wird, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) fixiert werden.</span><span class="sxs-lookup"><span data-stu-id="a4d95-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4d95-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4d95-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="a4d95-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4d95-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4d95-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4d95-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d95-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="a4d95-110">Type: **SamplerState**</span></span>

<span data-ttu-id="a4d95-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="a4d95-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="a4d95-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="a4d95-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="a4d95-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4d95-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d95-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="a4d95-114">Type: **float**</span></span>

<span data-ttu-id="a4d95-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="a4d95-115">The texture coordinates.</span></span> <span data-ttu-id="a4d95-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="a4d95-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a4d95-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="a4d95-117">Texture-Object Type</span></span>                    | <span data-ttu-id="a4d95-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="a4d95-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="a4d95-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a4d95-119">Texture1D</span></span>                              | <span data-ttu-id="a4d95-120">float</span><span class="sxs-lookup"><span data-stu-id="a4d95-120">float</span></span>          |
| <span data-ttu-id="a4d95-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="a4d95-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="a4d95-122">float2</span><span class="sxs-lookup"><span data-stu-id="a4d95-122">float2</span></span>         |
| <span data-ttu-id="a4d95-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="a4d95-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="a4d95-124">float3</span><span class="sxs-lookup"><span data-stu-id="a4d95-124">float3</span></span>         |
| <span data-ttu-id="a4d95-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="a4d95-125">TextureCubeArray</span></span>                       | <span data-ttu-id="a4d95-126">float4</span><span class="sxs-lookup"><span data-stu-id="a4d95-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="a4d95-127">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4d95-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d95-128">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="a4d95-128">Type: **float**</span></span>

<span data-ttu-id="a4d95-129">Die Änderungs Rate der Oberflächengeometrie in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="a4d95-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="a4d95-130">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="a4d95-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a4d95-131">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="a4d95-131">Texture-Object Type</span></span>                      | <span data-ttu-id="a4d95-132">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="a4d95-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="a4d95-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a4d95-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="a4d95-134">float</span><span class="sxs-lookup"><span data-stu-id="a4d95-134">float</span></span>          |
| <span data-ttu-id="a4d95-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a4d95-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="a4d95-136">float2</span><span class="sxs-lookup"><span data-stu-id="a4d95-136">float2</span></span>         |
| <span data-ttu-id="a4d95-137">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="a4d95-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="a4d95-138">float3</span><span class="sxs-lookup"><span data-stu-id="a4d95-138">float3</span></span>         |
| <span data-ttu-id="a4d95-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="a4d95-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="a4d95-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a4d95-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="a4d95-141">Nicht mehr  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4d95-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d95-142">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="a4d95-142">Type: **float**</span></span>

<span data-ttu-id="a4d95-143">Die Änderungs Rate der Oberflächengeometrie in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="a4d95-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="a4d95-144">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="a4d95-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a4d95-145">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="a4d95-145">Texture-Object Type</span></span>                      | <span data-ttu-id="a4d95-146">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="a4d95-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="a4d95-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a4d95-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="a4d95-148">float</span><span class="sxs-lookup"><span data-stu-id="a4d95-148">float</span></span>          |
| <span data-ttu-id="a4d95-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a4d95-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="a4d95-150">float2</span><span class="sxs-lookup"><span data-stu-id="a4d95-150">float2</span></span>         |
| <span data-ttu-id="a4d95-151">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="a4d95-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="a4d95-152">float3</span><span class="sxs-lookup"><span data-stu-id="a4d95-152">float3</span></span>         |
| <span data-ttu-id="a4d95-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="a4d95-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="a4d95-154">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a4d95-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="a4d95-155">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4d95-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d95-156">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="a4d95-156">Type: **int**</span></span>

<span data-ttu-id="a4d95-157">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="a4d95-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="a4d95-158">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="a4d95-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="a4d95-159">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="a4d95-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="a4d95-160">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a4d95-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="a4d95-161">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="a4d95-161">Texture-Object Type</span></span>           | <span data-ttu-id="a4d95-162">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="a4d95-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="a4d95-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a4d95-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="a4d95-164">INT</span><span class="sxs-lookup"><span data-stu-id="a4d95-164">int</span></span>            |
| <span data-ttu-id="a4d95-165">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a4d95-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="a4d95-166">int2</span><span class="sxs-lookup"><span data-stu-id="a4d95-166">int2</span></span>           |
| <span data-ttu-id="a4d95-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a4d95-167">Texture3D</span></span>                     | <span data-ttu-id="a4d95-168">int3</span><span class="sxs-lookup"><span data-stu-id="a4d95-168">int3</span></span>           |
| <span data-ttu-id="a4d95-169">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="a4d95-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="a4d95-170">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a4d95-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="a4d95-171">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4d95-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d95-172">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="a4d95-172">Type: **float**</span></span>

<span data-ttu-id="a4d95-173">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="a4d95-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="a4d95-174">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="a4d95-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4d95-175">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4d95-175">Return value</span></span>

<span data-ttu-id="a4d95-176">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="a4d95-176">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="a4d95-177">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="a4d95-177">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="a4d95-178">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a4d95-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4d95-179">Samplegrad-Methoden</span><span class="sxs-lookup"><span data-stu-id="a4d95-179">SampleGrad methods</span></span>](texture2darray-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="a4d95-180">**Texture2DArray**</span><span class="sxs-lookup"><span data-stu-id="a4d95-180">**Texture2DArray**</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

 
