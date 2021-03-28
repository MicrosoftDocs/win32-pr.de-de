---
title: Beispiel (DirectX HLSL-Strukturobjekt)
description: Stichproben eine Textur. | Sample (DirectX HLSL-Textur Objekt)
ms.assetid: 788ba4b4-8013-411f-9a19-fb9983386fa0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ec80d296025684c1bb67642661a31d8cdc119a53
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995295"
---
# <a name="sample-directx-hlsl-texture-object"></a><span data-ttu-id="c14eb-104">Beispiel (DirectX HLSL-Strukturobjekt)</span><span class="sxs-lookup"><span data-stu-id="c14eb-104">Sample (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="c14eb-105">Stichproben eine Textur.</span><span class="sxs-lookup"><span data-stu-id="c14eb-105">Samples a texture.</span></span>

|                                                                                  |
|----------------------------------------------------------------------------------|
| <span data-ttu-id="c14eb-106">&lt;Template Type &gt; Object. Sample (Sampler \_ State S, float Location \[ , int Offset \] );</span><span class="sxs-lookup"><span data-stu-id="c14eb-106">&lt;Template Type&gt; Object.Sample( sampler\_state S, float Location \[, int Offset\] );</span></span> |

## <a name="parameters"></a><span data-ttu-id="c14eb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c14eb-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c14eb-108">Element</span><span class="sxs-lookup"><span data-stu-id="c14eb-108">Item</span></span></th>
<th><span data-ttu-id="c14eb-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c14eb-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c14eb-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em></span><span class="sxs-lookup"><span data-stu-id="c14eb-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="c14eb-111">Ein beliebiger <a href="dx-graphics-hlsl-to-type.md">Textur Objekttyp</a> (mit Ausnahme von Texture2DMS und Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="c14eb-111">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c14eb-112"><span id="S"></span><span id="s"></span><em>Hymnen</em></span><span class="sxs-lookup"><span data-stu-id="c14eb-112"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="c14eb-113">in Ein <a href="dx-graphics-hlsl-sampler.md">samplerzustand</a>.</span><span class="sxs-lookup"><span data-stu-id="c14eb-113">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="c14eb-114">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="c14eb-114">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c14eb-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Hotels</em></span><span class="sxs-lookup"><span data-stu-id="c14eb-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="c14eb-116">in Die Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="c14eb-116">[in] The texture coordinates.</span></span> <span data-ttu-id="c14eb-117">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="c14eb-117">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c14eb-118">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="c14eb-118">Texture-Object Type</span></span></th>
<th><span data-ttu-id="c14eb-119">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="c14eb-119">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c14eb-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="c14eb-120">Texture1D</span></span></td>
<td><span data-ttu-id="c14eb-121">float</span><span class="sxs-lookup"><span data-stu-id="c14eb-121">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c14eb-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="c14eb-122">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="c14eb-123">float2</span><span class="sxs-lookup"><span data-stu-id="c14eb-123">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c14eb-124">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="c14eb-124">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="c14eb-125">float3</span><span class="sxs-lookup"><span data-stu-id="c14eb-125">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c14eb-126">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="c14eb-126">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="c14eb-127">float4</span><span class="sxs-lookup"><span data-stu-id="c14eb-127">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c14eb-128"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Kompensieren</em></span><span class="sxs-lookup"><span data-stu-id="c14eb-128"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="c14eb-129">in Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="c14eb-129">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="c14eb-130">Die Textur Offsets müssen statisch sein.</span><span class="sxs-lookup"><span data-stu-id="c14eb-130">The texture offsets need to be static.</span></span> <span data-ttu-id="c14eb-131">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="c14eb-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="c14eb-132">Weitere Informationen finden Sie unter <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Anwenden von Texturkoordinaten Offsets</a>.</span><span class="sxs-lookup"><span data-stu-id="c14eb-132">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c14eb-133">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="c14eb-133">Texture-Object Type</span></span></th>
<th><span data-ttu-id="c14eb-134">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="c14eb-134">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c14eb-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c14eb-135">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="c14eb-136">INT</span><span class="sxs-lookup"><span data-stu-id="c14eb-136">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c14eb-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c14eb-137">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="c14eb-138">int2</span><span class="sxs-lookup"><span data-stu-id="c14eb-138">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c14eb-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="c14eb-139">Texture3D</span></span></td>
<td><span data-ttu-id="c14eb-140">int3</span><span class="sxs-lookup"><span data-stu-id="c14eb-140">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c14eb-141">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="c14eb-141">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="c14eb-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c14eb-142">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>

## <a name="return-value"></a><span data-ttu-id="c14eb-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c14eb-143">Return value</span></span>

<span data-ttu-id="c14eb-144">Der Vorlagentyp der Textur, bei dem es sich um einen Vektor mit einer einzelnen oder mehreren Komponenten handeln kann.</span><span class="sxs-lookup"><span data-stu-id="c14eb-144">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="c14eb-145">Das Format basiert auf dem [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)der Textur.</span><span class="sxs-lookup"><span data-stu-id="c14eb-145">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="c14eb-146">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c14eb-146">Minimum Shader Model</span></span>

<span data-ttu-id="c14eb-147">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c14eb-147">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="c14eb-148">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c14eb-148">vs\_4\_0</span></span> | <span data-ttu-id="c14eb-149">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="c14eb-149">vs\_4\_1</span></span>  | <span data-ttu-id="c14eb-150">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c14eb-150">ps\_4\_0</span></span> | <span data-ttu-id="c14eb-151">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="c14eb-151">ps\_4\_1</span></span>  | <span data-ttu-id="c14eb-152">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c14eb-152">gs\_4\_0</span></span> | <span data-ttu-id="c14eb-153">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="c14eb-153">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="c14eb-154">x</span><span class="sxs-lookup"><span data-stu-id="c14eb-154">x</span></span>        | <span data-ttu-id="c14eb-155">x</span><span class="sxs-lookup"><span data-stu-id="c14eb-155">x</span></span>         |          |           |

1.  <span data-ttu-id="c14eb-156">Texturecubearray ist im Shader-Modell 4,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c14eb-156">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="c14eb-157">Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c14eb-157">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="c14eb-158">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c14eb-158">Example</span></span>

<span data-ttu-id="c14eb-159">Dieses partielle Codebeispiel basiert auf der Datei BasicHLSL11. fx im [BasicHLSL11](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11)-Beispiel.</span><span class="sxs-lookup"><span data-stu-id="c14eb-159">This partial code example is based on the BasicHLSL11.fx file in the [BasicHLSL11 Sample](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).</span></span>

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

## <a name="remarks"></a><span data-ttu-id="c14eb-160">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c14eb-160">Remarks</span></span>

<span data-ttu-id="c14eb-161">Bei der Textur Stichprobe wird die texusposition verwendet, um einen Texttyp zu suchen</span><span class="sxs-lookup"><span data-stu-id="c14eb-161">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="c14eb-162">Ein Offset kann vor der Suche auf die Position angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c14eb-162">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="c14eb-163">Der samplerstatus enthält die Optionen für Sampling und Filterung.</span><span class="sxs-lookup"><span data-stu-id="c14eb-163">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="c14eb-164">Diese Methode kann in einem Pixelshader aufgerufen werden, wird jedoch in einem Vertexshader oder einem Geometry-Shader nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c14eb-164">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="c14eb-165">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie abhängig von der Hardware Implementierung oder den Treibereinstellungen möglicherweise unterschiedliche Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="c14eb-165">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="c14eb-166">Berechnen von textabpositionen</span><span class="sxs-lookup"><span data-stu-id="c14eb-166">Calculating texel positions</span></span>

<span data-ttu-id="c14eb-167">Texturkoordinaten sind Gleit Komma Werte, die auf Textur Daten verweisen, die auch als normalisierter Textur Raum bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="c14eb-167">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="c14eb-168">Adress Umbruch Modi werden in dieser Reihenfolge (Texturkoordinaten + Offsets + Wrap-Modus) angewendet, um die Texturkoordinaten außerhalb des \[ Bereichs 0... 1 zu ändern \] .</span><span class="sxs-lookup"><span data-stu-id="c14eb-168">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="c14eb-169">Bei Textur Arrays gibt ein zusätzlicher Wert im Location-Parameter einen Index in ein Textur Array an.</span><span class="sxs-lookup"><span data-stu-id="c14eb-169">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="c14eb-170">Dieser Index wird als skalierter float-Wert (anstelle des normalisierten Raums für standardmäßige Texturkoordinaten) behandelt.</span><span class="sxs-lookup"><span data-stu-id="c14eb-170">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="c14eb-171">Die Konvertierung in einen ganzzahligen Index erfolgt in der folgenden Reihenfolge (float + Round-to-Next-even Integer + Klammer zum Array Bereich).</span><span class="sxs-lookup"><span data-stu-id="c14eb-171">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="c14eb-172">Anwenden von Texturkoordinaten Offsets</span><span class="sxs-lookup"><span data-stu-id="c14eb-172">Applying texture coordinate offsets</span></span>

<span data-ttu-id="c14eb-173">Der Offset-Parameter ändert die Texturkoordinaten in texesbereich.</span><span class="sxs-lookup"><span data-stu-id="c14eb-173">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="c14eb-174">Obwohl Texturkoordinaten normalisierte Gleit Komma Zahlen sind, wendet der Offset einen ganzzahligen Offset an.</span><span class="sxs-lookup"><span data-stu-id="c14eb-174">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="c14eb-175">Beachten Sie auch, dass die Textur Offsets statisch sein müssen.</span><span class="sxs-lookup"><span data-stu-id="c14eb-175">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="c14eb-176">Das zurückgegebene Datenformat wird durch das Textur Format bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c14eb-176">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="c14eb-177">Wenn die Textur Ressource z. b. mit dem DXGI- \_ Format \_ A8B8G8R8 \_ unorm \_ sRGB-Format definiert wurde, konvertiert der Samplingvorgang Sampling-texeln von Gamma 2,0 in 1,0, filtert und schreibt das Ergebnis als Gleit Komma Wert im Bereich \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="c14eb-177">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

## <a name="related-topics"></a><span data-ttu-id="c14eb-178">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c14eb-178">Related topics</span></span>

[<span data-ttu-id="c14eb-179">Texture-Objekt</span><span class="sxs-lookup"><span data-stu-id="c14eb-179">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
