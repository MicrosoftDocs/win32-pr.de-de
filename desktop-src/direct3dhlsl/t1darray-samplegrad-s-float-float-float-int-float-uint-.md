---
title: 'Samplegrad:: samplegrad (S, float, float, float, int, float, uint)-Funktion für Texture1DArray'
description: Erfahren Sie, wie diese Funktion eine Textur Abtast, wobei ein Farbverlauf verwendet wird, um die Art und Weise zu beeinflussen, wie der
ms.assetid: 8F0D2A4E-37A9-4141-9EE7-2AACBB29E3C2
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
ms.openlocfilehash: 7a0feca232f09da4dc99ff97f68eaab881f1e9ee
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762417"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture1darray"></a><span data-ttu-id="49ea5-104">Samplegrad:: samplegrad (S, float, float, float, int, float, uint)-Funktion für Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="49ea5-104">SampleGrad::SampleGrad(S,float,float,float,int,float,uint) function for Texture1DArray</span></span>

<span data-ttu-id="49ea5-105">Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, wie der Beispiel Speicherort berechnet wird, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) fixiert werden.</span><span class="sxs-lookup"><span data-stu-id="49ea5-105">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="49ea5-106">Gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="49ea5-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="49ea5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="49ea5-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="49ea5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="49ea5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49ea5-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49ea5-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ea5-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="49ea5-110">Type: **SamplerState**</span></span>

<span data-ttu-id="49ea5-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="49ea5-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="49ea5-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="49ea5-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="49ea5-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49ea5-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ea5-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="49ea5-114">Type: **float**</span></span>

<span data-ttu-id="49ea5-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="49ea5-115">The texture coordinates.</span></span> <span data-ttu-id="49ea5-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="49ea5-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="49ea5-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="49ea5-117">Texture-Object Type</span></span>                    | <span data-ttu-id="49ea5-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="49ea5-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="49ea5-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="49ea5-119">Texture1D</span></span>                              | <span data-ttu-id="49ea5-120">float</span><span class="sxs-lookup"><span data-stu-id="49ea5-120">float</span></span>          |
| <span data-ttu-id="49ea5-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="49ea5-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="49ea5-122">float2</span><span class="sxs-lookup"><span data-stu-id="49ea5-122">float2</span></span>         |
| <span data-ttu-id="49ea5-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="49ea5-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="49ea5-124">float3</span><span class="sxs-lookup"><span data-stu-id="49ea5-124">float3</span></span>         |
| <span data-ttu-id="49ea5-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="49ea5-125">TextureCubeArray</span></span>                       | <span data-ttu-id="49ea5-126">float4</span><span class="sxs-lookup"><span data-stu-id="49ea5-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="49ea5-127">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49ea5-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ea5-128">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="49ea5-128">Type: **float**</span></span>

<span data-ttu-id="49ea5-129">Die Änderungs Rate der Oberflächengeometrie in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="49ea5-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="49ea5-130">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="49ea5-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="49ea5-131">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="49ea5-131">Texture-Object Type</span></span>                      | <span data-ttu-id="49ea5-132">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="49ea5-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="49ea5-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="49ea5-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="49ea5-134">float</span><span class="sxs-lookup"><span data-stu-id="49ea5-134">float</span></span>          |
| <span data-ttu-id="49ea5-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="49ea5-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="49ea5-136">float2</span><span class="sxs-lookup"><span data-stu-id="49ea5-136">float2</span></span>         |
| <span data-ttu-id="49ea5-137">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="49ea5-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="49ea5-138">float3</span><span class="sxs-lookup"><span data-stu-id="49ea5-138">float3</span></span>         |
| <span data-ttu-id="49ea5-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="49ea5-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="49ea5-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="49ea5-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="49ea5-141">Nicht mehr  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49ea5-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ea5-142">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="49ea5-142">Type: **float**</span></span>

<span data-ttu-id="49ea5-143">Die Änderungs Rate der Oberflächengeometrie in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="49ea5-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="49ea5-144">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="49ea5-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="49ea5-145">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="49ea5-145">Texture-Object Type</span></span>                      | <span data-ttu-id="49ea5-146">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="49ea5-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="49ea5-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="49ea5-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="49ea5-148">float</span><span class="sxs-lookup"><span data-stu-id="49ea5-148">float</span></span>          |
| <span data-ttu-id="49ea5-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="49ea5-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="49ea5-150">float2</span><span class="sxs-lookup"><span data-stu-id="49ea5-150">float2</span></span>         |
| <span data-ttu-id="49ea5-151">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="49ea5-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="49ea5-152">float3</span><span class="sxs-lookup"><span data-stu-id="49ea5-152">float3</span></span>         |
| <span data-ttu-id="49ea5-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="49ea5-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="49ea5-154">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="49ea5-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="49ea5-155">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49ea5-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ea5-156">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="49ea5-156">Type: **int**</span></span>

<span data-ttu-id="49ea5-157">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="49ea5-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="49ea5-158">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="49ea5-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="49ea5-159">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="49ea5-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="49ea5-160">Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="49ea5-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="49ea5-161">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="49ea5-161">Texture-Object Type</span></span>           | <span data-ttu-id="49ea5-162">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="49ea5-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="49ea5-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="49ea5-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="49ea5-164">INT</span><span class="sxs-lookup"><span data-stu-id="49ea5-164">int</span></span>            |
| <span data-ttu-id="49ea5-165">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="49ea5-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="49ea5-166">int2</span><span class="sxs-lookup"><span data-stu-id="49ea5-166">int2</span></span>           |
| <span data-ttu-id="49ea5-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="49ea5-167">Texture3D</span></span>                     | <span data-ttu-id="49ea5-168">int3</span><span class="sxs-lookup"><span data-stu-id="49ea5-168">int3</span></span>           |
| <span data-ttu-id="49ea5-169">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="49ea5-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="49ea5-170">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="49ea5-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="49ea5-171">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49ea5-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ea5-172">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="49ea5-172">Type: **float**</span></span>

<span data-ttu-id="49ea5-173">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="49ea5-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="49ea5-174">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="49ea5-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="49ea5-175">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="49ea5-175">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49ea5-176">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="49ea5-176">Type: **uint**</span></span>

<span data-ttu-id="49ea5-177">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="49ea5-177">The status of the operation.</span></span> <span data-ttu-id="49ea5-178">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="49ea5-178">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="49ea5-179">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="49ea5-179">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="49ea5-180">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="49ea5-180">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49ea5-181">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49ea5-181">Return value</span></span>

<span data-ttu-id="49ea5-182">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="49ea5-182">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="49ea5-183">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="49ea5-183">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="49ea5-184">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="49ea5-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49ea5-185">Samplegrad-Methoden</span><span class="sxs-lookup"><span data-stu-id="49ea5-185">SampleGrad methods</span></span>](texture1darray-samplegrad.md)
</dt> </dl>

 

 
