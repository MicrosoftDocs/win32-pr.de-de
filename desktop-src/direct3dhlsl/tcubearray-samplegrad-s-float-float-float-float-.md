---
title: 'Samplegrad:: samplegrad (S, float, float, float, float)-Funktion für texturecubearray'
description: Erfahren Sie, wie diese Funktion eine Textur Abtast, wobei ein Farbverlauf verwendet wird, um die Art und Weise zu beeinflussen, wie der Für texturecubearray.
ms.assetid: 0C7DC9AA-3F0A-47E4-852F-7AE25CF67EA3
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
ms.openlocfilehash: 5320f47a5ae4db5bd96232dfa0a1d55b54f29c25
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762402"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecubearray"></a><span data-ttu-id="3f0a5-105">Samplegrad:: samplegrad (S, float, float, float, float)-Funktion für texturecubearray</span><span class="sxs-lookup"><span data-stu-id="3f0a5-105">SampleGrad::SampleGrad(S,float,float,float,float) function for TextureCubeArray</span></span>

<span data-ttu-id="3f0a5-106">Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, wie der Beispiel Speicherort berechnet wird, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) fixiert werden.</span><span class="sxs-lookup"><span data-stu-id="3f0a5-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f0a5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f0a5-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="3f0a5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f0a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f0a5-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f0a5-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0a5-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="3f0a5-110">Type: **SamplerState**</span></span>

<span data-ttu-id="3f0a5-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="3f0a5-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="3f0a5-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="3f0a5-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="3f0a5-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f0a5-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0a5-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="3f0a5-114">Type: **float**</span></span>

<span data-ttu-id="3f0a5-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="3f0a5-115">The texture coordinates.</span></span> <span data-ttu-id="3f0a5-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="3f0a5-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3f0a5-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="3f0a5-117">Texture-Object Type</span></span>                    | <span data-ttu-id="3f0a5-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="3f0a5-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="3f0a5-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3f0a5-119">Texture1D</span></span>                              | <span data-ttu-id="3f0a5-120">float</span><span class="sxs-lookup"><span data-stu-id="3f0a5-120">float</span></span>          |
| <span data-ttu-id="3f0a5-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="3f0a5-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="3f0a5-122">float2</span><span class="sxs-lookup"><span data-stu-id="3f0a5-122">float2</span></span>         |
| <span data-ttu-id="3f0a5-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="3f0a5-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="3f0a5-124">float3</span><span class="sxs-lookup"><span data-stu-id="3f0a5-124">float3</span></span>         |
| <span data-ttu-id="3f0a5-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="3f0a5-125">TextureCubeArray</span></span>                       | <span data-ttu-id="3f0a5-126">float4</span><span class="sxs-lookup"><span data-stu-id="3f0a5-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="3f0a5-127">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f0a5-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0a5-128">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="3f0a5-128">Type: **float**</span></span>

<span data-ttu-id="3f0a5-129">Die Änderungs Rate der Oberflächengeometrie in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="3f0a5-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="3f0a5-130">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="3f0a5-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3f0a5-131">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="3f0a5-131">Texture-Object Type</span></span>                      | <span data-ttu-id="3f0a5-132">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="3f0a5-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="3f0a5-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3f0a5-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="3f0a5-134">float</span><span class="sxs-lookup"><span data-stu-id="3f0a5-134">float</span></span>          |
| <span data-ttu-id="3f0a5-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3f0a5-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="3f0a5-136">float2</span><span class="sxs-lookup"><span data-stu-id="3f0a5-136">float2</span></span>         |
| <span data-ttu-id="3f0a5-137">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="3f0a5-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="3f0a5-138">float3</span><span class="sxs-lookup"><span data-stu-id="3f0a5-138">float3</span></span>         |
| <span data-ttu-id="3f0a5-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="3f0a5-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="3f0a5-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3f0a5-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="3f0a5-141">Nicht mehr  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f0a5-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0a5-142">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="3f0a5-142">Type: **float**</span></span>

<span data-ttu-id="3f0a5-143">Die Änderungs Rate der Oberflächengeometrie in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="3f0a5-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="3f0a5-144">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="3f0a5-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3f0a5-145">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="3f0a5-145">Texture-Object Type</span></span>                      | <span data-ttu-id="3f0a5-146">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="3f0a5-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="3f0a5-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3f0a5-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="3f0a5-148">float</span><span class="sxs-lookup"><span data-stu-id="3f0a5-148">float</span></span>          |
| <span data-ttu-id="3f0a5-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3f0a5-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="3f0a5-150">float2</span><span class="sxs-lookup"><span data-stu-id="3f0a5-150">float2</span></span>         |
| <span data-ttu-id="3f0a5-151">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="3f0a5-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="3f0a5-152">float3</span><span class="sxs-lookup"><span data-stu-id="3f0a5-152">float3</span></span>         |
| <span data-ttu-id="3f0a5-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="3f0a5-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="3f0a5-154">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3f0a5-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="3f0a5-155">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f0a5-155">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0a5-156">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="3f0a5-156">Type: **float**</span></span>

<span data-ttu-id="3f0a5-157">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="3f0a5-157">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="3f0a5-158">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="3f0a5-158">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f0a5-159">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f0a5-159">Return value</span></span>

<span data-ttu-id="3f0a5-160">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="3f0a5-160">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="3f0a5-161">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="3f0a5-161">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="3f0a5-162">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3f0a5-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f0a5-163">Samplegrad-Methoden</span><span class="sxs-lookup"><span data-stu-id="3f0a5-163">SampleGrad methods</span></span>](texturecubearray-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="3f0a5-164">**Texturecubearray**</span><span class="sxs-lookup"><span data-stu-id="3f0a5-164">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
