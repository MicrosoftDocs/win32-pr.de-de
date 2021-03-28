---
title: 'Samplegrad:: samplegrad (S, float, float, float, float, uint)-Funktion für texturecubearray'
description: Erfahren Sie, wie diese Funktion eine Textur Abtast, wobei ein Farbverlauf verwendet wird, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird Für texturecubearray.
ms.assetid: 849FAF04-A133-4E5B-967E-0679AE335CCC
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
ms.openlocfilehash: 00adfb5c7a1a95e5462b1bc524a6c7d86f71c2e8
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982645"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="c6448-105">Samplegrad:: samplegrad (S, float, float, float, float, uint)-Funktion für texturecubearray</span><span class="sxs-lookup"><span data-stu-id="c6448-105">SampleGrad::SampleGrad(S,float,float,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="c6448-106">Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, wie der Beispiel Speicherort berechnet wird, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) fixiert werden.</span><span class="sxs-lookup"><span data-stu-id="c6448-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="c6448-107">Gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="c6448-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6448-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6448-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in  SamplerState S,
  in  float        Location,
  in  float        DDX,
  in  float        DDY,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="c6448-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6448-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6448-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6448-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6448-111">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="c6448-111">Type: **SamplerState**</span></span>

<span data-ttu-id="c6448-112">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="c6448-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="c6448-113">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="c6448-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="c6448-114">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6448-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6448-115">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="c6448-115">Type: **float**</span></span>

<span data-ttu-id="c6448-116">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="c6448-116">The texture coordinates.</span></span> <span data-ttu-id="c6448-117">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="c6448-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c6448-118">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="c6448-118">Texture-Object Type</span></span>                    | <span data-ttu-id="c6448-119">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="c6448-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="c6448-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="c6448-120">Texture1D</span></span>                              | <span data-ttu-id="c6448-121">float</span><span class="sxs-lookup"><span data-stu-id="c6448-121">float</span></span>          |
| <span data-ttu-id="c6448-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="c6448-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="c6448-123">float2</span><span class="sxs-lookup"><span data-stu-id="c6448-123">float2</span></span>         |
| <span data-ttu-id="c6448-124">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="c6448-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="c6448-125">float3</span><span class="sxs-lookup"><span data-stu-id="c6448-125">float3</span></span>         |
| <span data-ttu-id="c6448-126">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="c6448-126">TextureCubeArray</span></span>                       | <span data-ttu-id="c6448-127">float4</span><span class="sxs-lookup"><span data-stu-id="c6448-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="c6448-128">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6448-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6448-129">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="c6448-129">Type: **float**</span></span>

<span data-ttu-id="c6448-130">Die Änderungs Rate der Oberflächengeometrie in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="c6448-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="c6448-131">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="c6448-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c6448-132">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="c6448-132">Texture-Object Type</span></span>                      | <span data-ttu-id="c6448-133">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="c6448-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="c6448-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c6448-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="c6448-135">float</span><span class="sxs-lookup"><span data-stu-id="c6448-135">float</span></span>          |
| <span data-ttu-id="c6448-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c6448-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="c6448-137">float2</span><span class="sxs-lookup"><span data-stu-id="c6448-137">float2</span></span>         |
| <span data-ttu-id="c6448-138">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="c6448-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="c6448-139">float3</span><span class="sxs-lookup"><span data-stu-id="c6448-139">float3</span></span>         |
| <span data-ttu-id="c6448-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="c6448-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="c6448-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c6448-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c6448-142">Nicht mehr  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6448-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6448-143">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="c6448-143">Type: **float**</span></span>

<span data-ttu-id="c6448-144">Die Änderungs Rate der Oberflächengeometrie in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="c6448-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="c6448-145">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="c6448-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c6448-146">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="c6448-146">Texture-Object Type</span></span>                      | <span data-ttu-id="c6448-147">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="c6448-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="c6448-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c6448-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="c6448-149">float</span><span class="sxs-lookup"><span data-stu-id="c6448-149">float</span></span>          |
| <span data-ttu-id="c6448-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c6448-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="c6448-151">float2</span><span class="sxs-lookup"><span data-stu-id="c6448-151">float2</span></span>         |
| <span data-ttu-id="c6448-152">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="c6448-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="c6448-153">float3</span><span class="sxs-lookup"><span data-stu-id="c6448-153">float3</span></span>         |
| <span data-ttu-id="c6448-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="c6448-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="c6448-155">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c6448-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c6448-156">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6448-156">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6448-157">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="c6448-157">Type: **float**</span></span>

<span data-ttu-id="c6448-158">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="c6448-158">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="c6448-159">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="c6448-159">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="c6448-160">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c6448-160">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6448-161">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="c6448-161">Type: **uint**</span></span>

<span data-ttu-id="c6448-162">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c6448-162">The status of the operation.</span></span> <span data-ttu-id="c6448-163">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c6448-163">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c6448-164">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="c6448-164">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c6448-165">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="c6448-165">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6448-166">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6448-166">Return value</span></span>

<span data-ttu-id="c6448-167">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="c6448-167">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="c6448-168">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="c6448-168">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="c6448-169">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c6448-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6448-170">Samplegrad-Methoden</span><span class="sxs-lookup"><span data-stu-id="c6448-170">SampleGrad methods</span></span>](texturecubearray-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="c6448-171">**Texturecubearray**</span><span class="sxs-lookup"><span data-stu-id="c6448-171">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
