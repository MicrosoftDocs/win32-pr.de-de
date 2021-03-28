---
title: Sample (S, float, int, float)-Funktion (HLSL-Referenz)
description: Abtast eine Texture2D mit einem optionalen Wert, um Werte von Sample-Werten (LOD) an zu binden.
ms.assetid: 899FACB6-40BB-471B-82A7-BDBBC63B206E
keywords:
- Beispiel Funktion HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5c151c3d93f5e2fe374f0f60fd06798cf1ce52a
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "104102586"
---
# <a name="samplesfloatintfloat-function-hlsl-reference"></a><span data-ttu-id="ab720-104">Sample (S, float, int, float)-Funktion (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="ab720-104">Sample(S,float,int,float) function (HLSL reference)</span></span>

<span data-ttu-id="ab720-105">Abtast eine [**Texture2D**](sm5-object-texture2d.md) mit einem optionalen Wert, um Werte von Sample-Werten (LOD) an zu binden.</span><span class="sxs-lookup"><span data-stu-id="ab720-105">Samples a [**Texture2D**](sm5-object-texture2d.md) with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

> [!Note]  
> <span data-ttu-id="ab720-106">Erfordert [Shader-Modell 5](d3d11-graphics-reference-sm5.md) oder höher.</span><span class="sxs-lookup"><span data-stu-id="ab720-106">Requires [shader model 5](d3d11-graphics-reference-sm5.md) or higher.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ab720-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab720-107">Syntax</span></span>

``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float Location,
  in int Offset,
  in float Clamp
);
```

## <a name="parameters"></a><span data-ttu-id="ab720-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab720-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab720-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab720-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab720-110">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="ab720-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="ab720-111">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="ab720-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="ab720-112">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab720-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab720-113">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="ab720-113">The texture coordinates.</span></span> <span data-ttu-id="ab720-114">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="ab720-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="ab720-115">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="ab720-115">Texture-Object Type</span></span>                    | <span data-ttu-id="ab720-116">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="ab720-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="ab720-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ab720-117">Texture1D</span></span>                              | <span data-ttu-id="ab720-118">float</span><span class="sxs-lookup"><span data-stu-id="ab720-118">float</span></span>          |
| <span data-ttu-id="ab720-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="ab720-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="ab720-120">float2</span><span class="sxs-lookup"><span data-stu-id="ab720-120">float2</span></span>         |
| <span data-ttu-id="ab720-121">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="ab720-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="ab720-122">float3</span><span class="sxs-lookup"><span data-stu-id="ab720-122">float3</span></span>         |
| <span data-ttu-id="ab720-123">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="ab720-123">TextureCubeArray</span></span>                       | <span data-ttu-id="ab720-124">float4</span><span class="sxs-lookup"><span data-stu-id="ab720-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="ab720-125">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab720-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab720-126">Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="ab720-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="ab720-127">Die Textur Offsets müssen statisch sein.</span><span class="sxs-lookup"><span data-stu-id="ab720-127">The texture offsets need to be static.</span></span> <span data-ttu-id="ab720-128">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="ab720-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="ab720-129">Weitere Informationen finden Sie unter [Anwenden von Texturkoordinaten Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="ab720-129">For more info, see [Applying texture coordinate offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="ab720-130">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="ab720-130">Texture-Object Type</span></span>           | <span data-ttu-id="ab720-131">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="ab720-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="ab720-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ab720-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="ab720-133">INT</span><span class="sxs-lookup"><span data-stu-id="ab720-133">int</span></span>            |
| <span data-ttu-id="ab720-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ab720-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="ab720-135">int2</span><span class="sxs-lookup"><span data-stu-id="ab720-135">int2</span></span>           |
| <span data-ttu-id="ab720-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ab720-136">Texture3D</span></span>                     | <span data-ttu-id="ab720-137">int3</span><span class="sxs-lookup"><span data-stu-id="ab720-137">int3</span></span>           |
| <span data-ttu-id="ab720-138">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="ab720-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="ab720-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ab720-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="ab720-140">*Klammer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab720-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab720-141">Ein optionaler Wert zum Einspannen von Sample-Lod-Werten.</span><span class="sxs-lookup"><span data-stu-id="ab720-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="ab720-142">Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.</span><span class="sxs-lookup"><span data-stu-id="ab720-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab720-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab720-143">Return value</span></span>

<span data-ttu-id="ab720-144">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="ab720-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="remarks"></a><span data-ttu-id="ab720-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab720-145">Remarks</span></span>

<span data-ttu-id="ab720-146">Bei der Textur Stichprobe wird die texusposition verwendet, um einen Texttyp zu suchen</span><span class="sxs-lookup"><span data-stu-id="ab720-146">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="ab720-147">Ein Offset kann vor der Suche auf die Position angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab720-147">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="ab720-148">Der samplerstatus enthält die Optionen für Sampling und Filterung.</span><span class="sxs-lookup"><span data-stu-id="ab720-148">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="ab720-149">Diese Methode kann in einem Pixelshader aufgerufen werden, wird jedoch in einem Vertexshader oder einem Geometry-Shader nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab720-149">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="ab720-150">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie abhängig von der Hardware Implementierung oder den Treibereinstellungen möglicherweise unterschiedliche Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="ab720-150">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="ab720-151">Berechnen von textabpositionen</span><span class="sxs-lookup"><span data-stu-id="ab720-151">Calculating Texel Positions</span></span>

<span data-ttu-id="ab720-152">Texturkoordinaten sind Gleit Komma Werte, die auf Textur Daten verweisen, die auch als normalisierter Textur Raum bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="ab720-152">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="ab720-153">Adress Umbruch Modi werden in dieser Reihenfolge (Texturkoordinaten + Offsets + Wrap-Modus) angewendet, um die Texturkoordinaten außerhalb des \[ Bereichs 0... 1 zu ändern \] .</span><span class="sxs-lookup"><span data-stu-id="ab720-153">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="ab720-154">Bei Textur Arrays gibt ein zusätzlicher Wert im Location-Parameter einen Index in ein Textur Array an.</span><span class="sxs-lookup"><span data-stu-id="ab720-154">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="ab720-155">Dieser Index wird als skalierter float-Wert (anstelle des normalisierten Raums für standardmäßige Texturkoordinaten) behandelt.</span><span class="sxs-lookup"><span data-stu-id="ab720-155">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="ab720-156">Die Konvertierung in einen ganzzahligen Index erfolgt in der folgenden Reihenfolge (float + Round-to-Next-even Integer + Klammer zum Array Bereich).</span><span class="sxs-lookup"><span data-stu-id="ab720-156">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="ab720-157">Anwenden von Texturkoordinaten Offsets</span><span class="sxs-lookup"><span data-stu-id="ab720-157">Applying Texture Coordinate Offsets</span></span>

<span data-ttu-id="ab720-158">Der Offset-Parameter ändert die Texturkoordinaten in texesbereich.</span><span class="sxs-lookup"><span data-stu-id="ab720-158">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="ab720-159">Obwohl Texturkoordinaten normalisierte Gleit Komma Zahlen sind, wendet der Offset einen ganzzahligen Offset an.</span><span class="sxs-lookup"><span data-stu-id="ab720-159">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="ab720-160">Beachten Sie auch, dass die Textur Offsets statisch sein müssen.</span><span class="sxs-lookup"><span data-stu-id="ab720-160">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="ab720-161">Das zurückgegebene Datenformat wird durch das Textur Format bestimmt.</span><span class="sxs-lookup"><span data-stu-id="ab720-161">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="ab720-162">Wenn die Textur Ressource z. b. mit dem DXGI- \_ Format \_ A8B8G8R8 \_ unorm \_ sRGB-Format definiert wurde, konvertiert der Samplingvorgang Sampling-texeln von Gamma 2,0 in 1,0, filtert und schreibt das Ergebnis als Gleit Komma Wert im Bereich \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="ab720-162">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

<span data-ttu-id="ab720-163">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="ab720-163">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab720-164">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ab720-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab720-165">Beispiel Methoden</span><span class="sxs-lookup"><span data-stu-id="ab720-165">Sample methods</span></span>](texture-sample-overload.md)
</dt> <dt>

[<span data-ttu-id="ab720-166">Texture-Objekt</span><span class="sxs-lookup"><span data-stu-id="ab720-166">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
