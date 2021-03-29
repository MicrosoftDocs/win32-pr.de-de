---
title: 'Samplegrad:: samplegrad (S, float, float, float, float)-Funktion für texturecube'
description: Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, wie der Beispiel Speicherort berechnet wird, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) fixiert werden. Für texturecube
ms.assetid: C5BC71FA-63E3-4DE2-9202-B9C79789AE8E
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
ms.openlocfilehash: e4a51c49d9373dc210cbf216089e4c82835bf2c4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531121"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecube"></a><span data-ttu-id="38037-105">Samplegrad:: samplegrad (S, float, float, float, float)-Funktion für texturecube</span><span class="sxs-lookup"><span data-stu-id="38037-105">SampleGrad::SampleGrad(S,float,float,float,float) function for TextureCube</span></span>

<span data-ttu-id="38037-106">Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, wie der Beispiel Speicherort berechnet wird, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) fixiert werden.</span><span class="sxs-lookup"><span data-stu-id="38037-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="38037-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="38037-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="38037-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="38037-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38037-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38037-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38037-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="38037-110">Type: **SamplerState**</span></span>

<span data-ttu-id="38037-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="38037-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="38037-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="38037-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="38037-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38037-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38037-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="38037-114">Type: **float**</span></span>

<span data-ttu-id="38037-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="38037-115">The texture coordinates.</span></span> <span data-ttu-id="38037-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="38037-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="38037-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="38037-117">Texture-Object Type</span></span>                    | <span data-ttu-id="38037-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="38037-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="38037-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="38037-119">Texture1D</span></span>                              | <span data-ttu-id="38037-120">float</span><span class="sxs-lookup"><span data-stu-id="38037-120">float</span></span>          |
| <span data-ttu-id="38037-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="38037-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="38037-122">float2</span><span class="sxs-lookup"><span data-stu-id="38037-122">float2</span></span>         |
| <span data-ttu-id="38037-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="38037-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="38037-124">float3</span><span class="sxs-lookup"><span data-stu-id="38037-124">float3</span></span>         |
| <span data-ttu-id="38037-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="38037-125">TextureCubeArray</span></span>                       | <span data-ttu-id="38037-126">float4</span><span class="sxs-lookup"><span data-stu-id="38037-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="38037-127">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38037-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38037-128">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="38037-128">Type: **float**</span></span>

<span data-ttu-id="38037-129">Die Änderungs Rate der Oberflächengeometrie in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="38037-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="38037-130">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="38037-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="38037-131">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="38037-131">Texture-Object Type</span></span>                      | <span data-ttu-id="38037-132">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="38037-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="38037-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="38037-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="38037-134">float</span><span class="sxs-lookup"><span data-stu-id="38037-134">float</span></span>          |
| <span data-ttu-id="38037-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="38037-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="38037-136">float2</span><span class="sxs-lookup"><span data-stu-id="38037-136">float2</span></span>         |
| <span data-ttu-id="38037-137">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="38037-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="38037-138">float3</span><span class="sxs-lookup"><span data-stu-id="38037-138">float3</span></span>         |
| <span data-ttu-id="38037-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="38037-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="38037-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="38037-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="38037-141">Nicht mehr  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38037-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38037-142">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="38037-142">Type: **float**</span></span>

<span data-ttu-id="38037-143">Die Änderungs Rate der Oberflächengeometrie in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="38037-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="38037-144">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="38037-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="38037-145">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="38037-145">Texture-Object Type</span></span>                      | <span data-ttu-id="38037-146">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="38037-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="38037-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="38037-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="38037-148">float</span><span class="sxs-lookup"><span data-stu-id="38037-148">float</span></span>          |
| <span data-ttu-id="38037-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="38037-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="38037-150">float2</span><span class="sxs-lookup"><span data-stu-id="38037-150">float2</span></span>         |
| <span data-ttu-id="38037-151">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="38037-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="38037-152">float3</span><span class="sxs-lookup"><span data-stu-id="38037-152">float3</span></span>         |
| <span data-ttu-id="38037-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="38037-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="38037-154">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="38037-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="38037-155">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38037-155">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38037-156">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="38037-156">Type: **float**</span></span>

<span data-ttu-id="38037-157">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="38037-157">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="38037-158">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="38037-158">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38037-159">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38037-159">Return value</span></span>

<span data-ttu-id="38037-160">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="38037-160">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="38037-161">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="38037-161">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="38037-162">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="38037-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38037-163">Samplegrad-Methoden</span><span class="sxs-lookup"><span data-stu-id="38037-163">SampleGrad methods</span></span>](texturecube-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="38037-164">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="38037-164">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
