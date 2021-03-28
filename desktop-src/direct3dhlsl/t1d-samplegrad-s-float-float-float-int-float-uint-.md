---
title: 'Samplegrad:: samplegrad (S, float, float, float, int, float, uint)-Funktion für Texture1D'
description: Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, wie der Beispiel Speicherort berechnet wird, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) fixiert werden. Für Texture1D.
ms.assetid: E2B131AC-99E6-493A-91EE-EB0D3EE7FA8B
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
ms.openlocfilehash: 3a5f95a87f46e94c971dd19989ffa670e6993e8f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103961784"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture1d"></a><span data-ttu-id="a65ce-105">Samplegrad:: samplegrad (S, float, float, float, int, float, uint)-Funktion für Texture1D</span><span class="sxs-lookup"><span data-stu-id="a65ce-105">SampleGrad::SampleGrad(S,float,float,float,int,float,uint) function for Texture1D</span></span>

<span data-ttu-id="a65ce-106">Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, wie der Beispiel Speicherort berechnet wird, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) fixiert werden.</span><span class="sxs-lookup"><span data-stu-id="a65ce-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="a65ce-107">Gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="a65ce-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a65ce-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65ce-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="a65ce-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a65ce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a65ce-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a65ce-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a65ce-111">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="a65ce-111">Type: **SamplerState**</span></span>

<span data-ttu-id="a65ce-112">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="a65ce-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="a65ce-113">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="a65ce-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="a65ce-114">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a65ce-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a65ce-115">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="a65ce-115">Type: **float**</span></span>

<span data-ttu-id="a65ce-116">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="a65ce-116">The texture coordinates.</span></span> <span data-ttu-id="a65ce-117">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="a65ce-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a65ce-118">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="a65ce-118">Texture-Object Type</span></span>                    | <span data-ttu-id="a65ce-119">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="a65ce-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="a65ce-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a65ce-120">Texture1D</span></span>                              | <span data-ttu-id="a65ce-121">float</span><span class="sxs-lookup"><span data-stu-id="a65ce-121">float</span></span>          |
| <span data-ttu-id="a65ce-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="a65ce-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="a65ce-123">float2</span><span class="sxs-lookup"><span data-stu-id="a65ce-123">float2</span></span>         |
| <span data-ttu-id="a65ce-124">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="a65ce-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="a65ce-125">float3</span><span class="sxs-lookup"><span data-stu-id="a65ce-125">float3</span></span>         |
| <span data-ttu-id="a65ce-126">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="a65ce-126">TextureCubeArray</span></span>                       | <span data-ttu-id="a65ce-127">float4</span><span class="sxs-lookup"><span data-stu-id="a65ce-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="a65ce-128">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a65ce-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a65ce-129">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="a65ce-129">Type: **float**</span></span>

<span data-ttu-id="a65ce-130">Die Änderungs Rate der Oberflächengeometrie in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="a65ce-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="a65ce-131">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="a65ce-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a65ce-132">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="a65ce-132">Texture-Object Type</span></span>                      | <span data-ttu-id="a65ce-133">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="a65ce-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="a65ce-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a65ce-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="a65ce-135">float</span><span class="sxs-lookup"><span data-stu-id="a65ce-135">float</span></span>          |
| <span data-ttu-id="a65ce-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a65ce-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="a65ce-137">float2</span><span class="sxs-lookup"><span data-stu-id="a65ce-137">float2</span></span>         |
| <span data-ttu-id="a65ce-138">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="a65ce-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="a65ce-139">float3</span><span class="sxs-lookup"><span data-stu-id="a65ce-139">float3</span></span>         |
| <span data-ttu-id="a65ce-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="a65ce-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="a65ce-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a65ce-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="a65ce-142">Nicht mehr  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a65ce-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a65ce-143">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="a65ce-143">Type: **float**</span></span>

<span data-ttu-id="a65ce-144">Die Änderungs Rate der Oberflächengeometrie in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="a65ce-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="a65ce-145">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="a65ce-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a65ce-146">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="a65ce-146">Texture-Object Type</span></span>                      | <span data-ttu-id="a65ce-147">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="a65ce-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="a65ce-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a65ce-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="a65ce-149">float</span><span class="sxs-lookup"><span data-stu-id="a65ce-149">float</span></span>          |
| <span data-ttu-id="a65ce-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a65ce-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="a65ce-151">float2</span><span class="sxs-lookup"><span data-stu-id="a65ce-151">float2</span></span>         |
| <span data-ttu-id="a65ce-152">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="a65ce-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="a65ce-153">float3</span><span class="sxs-lookup"><span data-stu-id="a65ce-153">float3</span></span>         |
| <span data-ttu-id="a65ce-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="a65ce-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="a65ce-155">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a65ce-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="a65ce-156">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a65ce-156">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a65ce-157">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="a65ce-157">Type: **int**</span></span>

<span data-ttu-id="a65ce-158">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="a65ce-158">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="a65ce-159">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="a65ce-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="a65ce-160">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="a65ce-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="a65ce-161">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a65ce-161">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="a65ce-162">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="a65ce-162">Texture-Object Type</span></span>           | <span data-ttu-id="a65ce-163">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="a65ce-163">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="a65ce-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a65ce-164">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="a65ce-165">INT</span><span class="sxs-lookup"><span data-stu-id="a65ce-165">int</span></span>            |
| <span data-ttu-id="a65ce-166">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a65ce-166">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="a65ce-167">int2</span><span class="sxs-lookup"><span data-stu-id="a65ce-167">int2</span></span>           |
| <span data-ttu-id="a65ce-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a65ce-168">Texture3D</span></span>                     | <span data-ttu-id="a65ce-169">int3</span><span class="sxs-lookup"><span data-stu-id="a65ce-169">int3</span></span>           |
| <span data-ttu-id="a65ce-170">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="a65ce-170">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="a65ce-171">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a65ce-171">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="a65ce-172">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a65ce-172">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a65ce-173">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="a65ce-173">Type: **float**</span></span>

<span data-ttu-id="a65ce-174">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="a65ce-174">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="a65ce-175">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="a65ce-175">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="a65ce-176">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a65ce-176">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a65ce-177">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="a65ce-177">Type: **uint**</span></span>

<span data-ttu-id="a65ce-178">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="a65ce-178">The status of the operation.</span></span> <span data-ttu-id="a65ce-179">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="a65ce-179">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="a65ce-180">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="a65ce-180">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="a65ce-181">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="a65ce-181">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a65ce-182">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a65ce-182">Return value</span></span>

<span data-ttu-id="a65ce-183">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="a65ce-183">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="a65ce-184">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="a65ce-184">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="a65ce-185">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a65ce-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a65ce-186">Samplegrad-Methoden</span><span class="sxs-lookup"><span data-stu-id="a65ce-186">SampleGrad methods</span></span>](texture1d-samplegrad.md)
</dt> </dl>

 

 
