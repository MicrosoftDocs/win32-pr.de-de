---
title: 'Samplegrad:: samplegrad (S, float, float, float, int, float, uint)-Funktion für Texture3D'
description: Erfahren Sie, wie diese Funktion eine Textur Abtast, wobei ein Farbverlauf verwendet wird, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird Für Texture3D.
ms.assetid: 4B02A3B8-8179-497D-BF87-489BF0B9ECC2
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
ms.openlocfilehash: b80b6ddcc2eebecf02416b09256d714bd2b8772f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982661"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture3d"></a><span data-ttu-id="d9aef-105">Samplegrad:: samplegrad (S, float, float, float, int, float, uint)-Funktion für Texture3D</span><span class="sxs-lookup"><span data-stu-id="d9aef-105">SampleGrad::SampleGrad(S,float,float,float,int,float,uint) function for Texture3D</span></span>

<span data-ttu-id="d9aef-106">Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, wie der Beispiel Speicherort berechnet wird, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) fixiert werden.</span><span class="sxs-lookup"><span data-stu-id="d9aef-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="d9aef-107">Gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="d9aef-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9aef-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9aef-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in  SamplerState S,
  in  float        Location,
  in  float        DDX,
  in  float        DDY,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="d9aef-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9aef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9aef-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9aef-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9aef-111">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="d9aef-111">Type: **SamplerState**</span></span>

<span data-ttu-id="d9aef-112">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="d9aef-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="d9aef-113">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="d9aef-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="d9aef-114">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9aef-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9aef-115">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d9aef-115">Type: **float**</span></span>

<span data-ttu-id="d9aef-116">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="d9aef-116">The texture coordinates.</span></span> <span data-ttu-id="d9aef-117">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="d9aef-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="d9aef-118">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="d9aef-118">Texture-Object Type</span></span>                    | <span data-ttu-id="d9aef-119">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="d9aef-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="d9aef-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d9aef-120">Texture1D</span></span>                              | <span data-ttu-id="d9aef-121">float</span><span class="sxs-lookup"><span data-stu-id="d9aef-121">float</span></span>          |
| <span data-ttu-id="d9aef-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="d9aef-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="d9aef-123">float2</span><span class="sxs-lookup"><span data-stu-id="d9aef-123">float2</span></span>         |
| <span data-ttu-id="d9aef-124">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="d9aef-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="d9aef-125">float3</span><span class="sxs-lookup"><span data-stu-id="d9aef-125">float3</span></span>         |
| <span data-ttu-id="d9aef-126">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="d9aef-126">TextureCubeArray</span></span>                       | <span data-ttu-id="d9aef-127">float4</span><span class="sxs-lookup"><span data-stu-id="d9aef-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="d9aef-128">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9aef-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9aef-129">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d9aef-129">Type: **float**</span></span>

<span data-ttu-id="d9aef-130">Die Änderungs Rate der Oberflächengeometrie in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="d9aef-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="d9aef-131">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="d9aef-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="d9aef-132">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="d9aef-132">Texture-Object Type</span></span>                      | <span data-ttu-id="d9aef-133">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="d9aef-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="d9aef-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d9aef-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="d9aef-135">float</span><span class="sxs-lookup"><span data-stu-id="d9aef-135">float</span></span>          |
| <span data-ttu-id="d9aef-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d9aef-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="d9aef-137">float2</span><span class="sxs-lookup"><span data-stu-id="d9aef-137">float2</span></span>         |
| <span data-ttu-id="d9aef-138">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="d9aef-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="d9aef-139">float3</span><span class="sxs-lookup"><span data-stu-id="d9aef-139">float3</span></span>         |
| <span data-ttu-id="d9aef-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="d9aef-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="d9aef-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d9aef-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="d9aef-142">Nicht mehr  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9aef-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9aef-143">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d9aef-143">Type: **float**</span></span>

<span data-ttu-id="d9aef-144">Die Änderungs Rate der Oberflächengeometrie in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="d9aef-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="d9aef-145">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="d9aef-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="d9aef-146">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="d9aef-146">Texture-Object Type</span></span>                      | <span data-ttu-id="d9aef-147">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="d9aef-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="d9aef-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d9aef-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="d9aef-149">float</span><span class="sxs-lookup"><span data-stu-id="d9aef-149">float</span></span>          |
| <span data-ttu-id="d9aef-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d9aef-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="d9aef-151">float2</span><span class="sxs-lookup"><span data-stu-id="d9aef-151">float2</span></span>         |
| <span data-ttu-id="d9aef-152">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="d9aef-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="d9aef-153">float3</span><span class="sxs-lookup"><span data-stu-id="d9aef-153">float3</span></span>         |
| <span data-ttu-id="d9aef-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="d9aef-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="d9aef-155">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d9aef-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="d9aef-156">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9aef-156">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9aef-157">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="d9aef-157">Type: **int**</span></span>

<span data-ttu-id="d9aef-158">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="d9aef-158">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="d9aef-159">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="d9aef-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="d9aef-160">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="d9aef-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="d9aef-161">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="d9aef-161">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="d9aef-162">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="d9aef-162">Texture-Object Type</span></span>           | <span data-ttu-id="d9aef-163">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="d9aef-163">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="d9aef-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d9aef-164">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="d9aef-165">INT</span><span class="sxs-lookup"><span data-stu-id="d9aef-165">int</span></span>            |
| <span data-ttu-id="d9aef-166">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d9aef-166">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="d9aef-167">int2</span><span class="sxs-lookup"><span data-stu-id="d9aef-167">int2</span></span>           |
| <span data-ttu-id="d9aef-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d9aef-168">Texture3D</span></span>                     | <span data-ttu-id="d9aef-169">int3</span><span class="sxs-lookup"><span data-stu-id="d9aef-169">int3</span></span>           |
| <span data-ttu-id="d9aef-170">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="d9aef-170">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="d9aef-171">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d9aef-171">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="d9aef-172">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9aef-172">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9aef-173">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d9aef-173">Type: **float**</span></span>

<span data-ttu-id="d9aef-174">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="d9aef-174">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="d9aef-175">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="d9aef-175">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="d9aef-176">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d9aef-176">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9aef-177">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="d9aef-177">Type: **uint**</span></span>

<span data-ttu-id="d9aef-178">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="d9aef-178">The status of the operation.</span></span> <span data-ttu-id="d9aef-179">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d9aef-179">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="d9aef-180">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="d9aef-180">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="d9aef-181">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="d9aef-181">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9aef-182">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9aef-182">Return value</span></span>

<span data-ttu-id="d9aef-183">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="d9aef-183">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="d9aef-184">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="d9aef-184">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="d9aef-185">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d9aef-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9aef-186">Samplegrad-Methoden</span><span class="sxs-lookup"><span data-stu-id="d9aef-186">SampleGrad methods</span></span>](texture3d-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="d9aef-187">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="d9aef-187">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
