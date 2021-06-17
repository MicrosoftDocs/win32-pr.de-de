---
title: Beispiel (DirectX HLSL-Strukturobjekt)
description: Stichproben einer Textur. | Beispiel (DirectX HLSL-Texturobjekt)
ms.assetid: 788ba4b4-8013-411f-9a19-fb9983386fa0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2374063d222d06576f720fed2aa7fb714bcccf04
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825747"
---
# <a name="sample-directx-hlsl-texture-object"></a><span data-ttu-id="6257b-104">Beispiel (DirectX HLSL-Strukturobjekt)</span><span class="sxs-lookup"><span data-stu-id="6257b-104">Sample (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="6257b-105">Stichproben einer Textur.</span><span class="sxs-lookup"><span data-stu-id="6257b-105">Samples a texture.</span></span>

<span data-ttu-id="6257b-106">&lt;Vorlagentyp &gt; Object.Sample( \_ Samplerzustand S, float Location \[ , int Offset \] );</span><span class="sxs-lookup"><span data-stu-id="6257b-106">&lt;Template Type&gt; Object.Sample( sampler\_state S, float Location \[, int Offset\] );</span></span>

## <a name="parameters"></a><span data-ttu-id="6257b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6257b-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6257b-108">Element</span><span class="sxs-lookup"><span data-stu-id="6257b-108">Item</span></span></th>
<th><span data-ttu-id="6257b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6257b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6257b-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em></span><span class="sxs-lookup"><span data-stu-id="6257b-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="6257b-111">Beliebiger <a href="dx-graphics-hlsl-to-type.md">Texturobjekttyp</a> (außer Texture2DMS und Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="6257b-111">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6257b-112"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="6257b-112"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="6257b-113">[in] Ein <a href="dx-graphics-hlsl-sampler.md">Samplerzustand.</a></span><span class="sxs-lookup"><span data-stu-id="6257b-113">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="6257b-114">Dies ist ein Objekt, das in einer Effektdatei deklariert ist, die Zustandszuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="6257b-114">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6257b-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Lage</em></span><span class="sxs-lookup"><span data-stu-id="6257b-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="6257b-116">[in] Die Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="6257b-116">[in] The texture coordinates.</span></span> <span data-ttu-id="6257b-117">Der Argumenttyp ist vom Texturobjekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="6257b-117">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6257b-118">Texture-Object Typ</span><span class="sxs-lookup"><span data-stu-id="6257b-118">Texture-Object Type</span></span></th>
<th><span data-ttu-id="6257b-119">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="6257b-119">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6257b-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6257b-120">Texture1D</span></span></td>
<td><span data-ttu-id="6257b-121">float</span><span class="sxs-lookup"><span data-stu-id="6257b-121">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6257b-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="6257b-122">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="6257b-123">float2</span><span class="sxs-lookup"><span data-stu-id="6257b-123">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6257b-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="6257b-124">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="6257b-125">float3</span><span class="sxs-lookup"><span data-stu-id="6257b-125">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6257b-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="6257b-126">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="6257b-127">float4</span><span class="sxs-lookup"><span data-stu-id="6257b-127">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6257b-128"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span><span class="sxs-lookup"><span data-stu-id="6257b-128"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="6257b-129">[in] Ein optionaler Texturkoordinatenoffset, der für jeden Texturobjekttyp verwendet werden kann. Der Offset wird vor der Stichprobenentnahme auf die Position angewendet.</span><span class="sxs-lookup"><span data-stu-id="6257b-129">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="6257b-130">Die Texturoffsets müssen statisch sein.</span><span class="sxs-lookup"><span data-stu-id="6257b-130">The texture offsets need to be static.</span></span> <span data-ttu-id="6257b-131">Der Argumenttyp ist vom Texturobjekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="6257b-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="6257b-132">Weitere Informationen finden Sie unter <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Anwenden von Texturkoordinatenoffsets.</a></span><span class="sxs-lookup"><span data-stu-id="6257b-132">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6257b-133">Texture-Object Typ</span><span class="sxs-lookup"><span data-stu-id="6257b-133">Texture-Object Type</span></span></th>
<th><span data-ttu-id="6257b-134">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="6257b-134">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6257b-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="6257b-135">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="6257b-136">INT</span><span class="sxs-lookup"><span data-stu-id="6257b-136">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6257b-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="6257b-137">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="6257b-138">int2</span><span class="sxs-lookup"><span data-stu-id="6257b-138">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6257b-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6257b-139">Texture3D</span></span></td>
<td><span data-ttu-id="6257b-140">int3</span><span class="sxs-lookup"><span data-stu-id="6257b-140">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6257b-141">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="6257b-141">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="6257b-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6257b-142">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>

## <a name="return-value"></a><span data-ttu-id="6257b-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6257b-143">Return value</span></span>

<span data-ttu-id="6257b-144">Der Vorlagentyp der Textur, der ein Vektor mit einer oder mehreren Komponenten sein kann.</span><span class="sxs-lookup"><span data-stu-id="6257b-144">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="6257b-145">Das Format basiert auf dem DXGI FORMAT der [**\_ Textur.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="6257b-145">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="6257b-146">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="6257b-146">Minimum Shader Model</span></span>

<span data-ttu-id="6257b-147">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6257b-147">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="6257b-148">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6257b-148">vs\_4\_0</span></span> | <span data-ttu-id="6257b-149">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="6257b-149">vs\_4\_1</span></span>  | <span data-ttu-id="6257b-150">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6257b-150">ps\_4\_0</span></span> | <span data-ttu-id="6257b-151">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="6257b-151">ps\_4\_1</span></span>  | <span data-ttu-id="6257b-152">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6257b-152">gs\_4\_0</span></span> | <span data-ttu-id="6257b-153">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="6257b-153">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="6257b-154">x</span><span class="sxs-lookup"><span data-stu-id="6257b-154">x</span></span>        | <span data-ttu-id="6257b-155">x</span><span class="sxs-lookup"><span data-stu-id="6257b-155">x</span></span>         |          |           |

1.  <span data-ttu-id="6257b-156">TextureCubeArray ist in Shader Model 4.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6257b-156">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="6257b-157">ShaderModell 4.1 ist in Direct3D 10.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6257b-157">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="6257b-158">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6257b-158">Example</span></span>

<span data-ttu-id="6257b-159">Dieses Teilcodebeispiel basiert auf der Datei BasicHLSL11.fx im [BasicHLSL11-Beispiel](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).</span><span class="sxs-lookup"><span data-stu-id="6257b-159">This partial code example is based on the BasicHLSL11.fx file in the [BasicHLSL11 Sample](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).</span></span>

```
// Object Declarations
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color (note that COLOR0 is clamped from 0..1)
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT In;

// Shader body calling the intrinsic function
   ...
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
```

## <a name="remarks"></a><span data-ttu-id="6257b-160">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6257b-160">Remarks</span></span>

<span data-ttu-id="6257b-161">Bei der Texturstichprobe wird die Texelposition verwendet, um einen Texelwert zu suchen.</span><span class="sxs-lookup"><span data-stu-id="6257b-161">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="6257b-162">Ein Offset kann vor der Suche auf die Position angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="6257b-162">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="6257b-163">Der Samplerzustand enthält die Sampling- und Filteroptionen.</span><span class="sxs-lookup"><span data-stu-id="6257b-163">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="6257b-164">Diese Methode kann innerhalb eines Pixel-Shaders aufgerufen werden, wird jedoch in einem Vertex-Shader oder geometrie-Shader nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6257b-164">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="6257b-165">Verwenden Sie einen Offset nur bei einer ganzzahligen MIP-Ebene. Andernfalls erhalten Sie je nach Hardwareimplementierung oder Treibereinstellungen möglicherweise unterschiedliche Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="6257b-165">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="6257b-166">Berechnen von Texelpositionen</span><span class="sxs-lookup"><span data-stu-id="6257b-166">Calculating texel positions</span></span>

<span data-ttu-id="6257b-167">Texturkoordinaten sind Gleitkommawerte, die auf Texturdaten verweisen, die auch als normalisierter Texturraum bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="6257b-167">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="6257b-168">Adressumbruchmodi werden in dieser Reihenfolge (Texturkoordinaten + Offsets + Umbruchmodus) angewendet, um Texturkoordinaten außerhalb des \[ Bereichs 0...1 zu \] ändern.</span><span class="sxs-lookup"><span data-stu-id="6257b-168">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="6257b-169">Bei Texturarrays gibt ein zusätzlicher Wert im location-Parameter einen Index in einem Texturarray an.</span><span class="sxs-lookup"><span data-stu-id="6257b-169">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="6257b-170">Dieser Index wird als skalierte Gleitkommawerte behandelt (anstelle des normalisierten Platzes für Standardtexturkoordinaten).</span><span class="sxs-lookup"><span data-stu-id="6257b-170">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="6257b-171">Die Konvertierung in einen ganzzahligen Index erfolgt in der folgenden Reihenfolge (float + round-to-nearest-even integer + clamp to the array range).</span><span class="sxs-lookup"><span data-stu-id="6257b-171">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="6257b-172">Anwenden von Texturkoordinatenoffsets</span><span class="sxs-lookup"><span data-stu-id="6257b-172">Applying texture coordinate offsets</span></span>

<span data-ttu-id="6257b-173">Der offset-Parameter ändert die Texturkoordinaten im Texelraum.</span><span class="sxs-lookup"><span data-stu-id="6257b-173">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="6257b-174">Obwohl Texturkoordinaten normalisierte Gleitkommazahlen sind, wendet der Offset einen ganzzahligen Offset an.</span><span class="sxs-lookup"><span data-stu-id="6257b-174">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="6257b-175">Beachten Sie auch, dass die Texturoffsets statisch sein müssen.</span><span class="sxs-lookup"><span data-stu-id="6257b-175">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="6257b-176">Das zurückgegebene Datenformat wird durch das Texturformat bestimmt.</span><span class="sxs-lookup"><span data-stu-id="6257b-176">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="6257b-177">Wenn die Texturressource z. B. mit dem DXGI \_ FORMAT \_ A8B8G8R8 UNORM SRGB-Format definiert wurde, konvertiert der Samplingvorgang \_ sampled texels von gamma 2.0 in 1.0, filtert das Ergebnis und schreibt das Ergebnis als Gleitkommawert im Bereich \_ \[ 0..1 \] .</span><span class="sxs-lookup"><span data-stu-id="6257b-177">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

## <a name="related-topics"></a><span data-ttu-id="6257b-178">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6257b-178">Related topics</span></span>

[<span data-ttu-id="6257b-179">Texture-Object</span><span class="sxs-lookup"><span data-stu-id="6257b-179">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
