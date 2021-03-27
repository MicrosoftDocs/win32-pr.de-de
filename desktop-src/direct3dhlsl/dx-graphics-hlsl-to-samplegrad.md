---
title: Sample Grad (DirectX HLSL-Textur Objekt)
description: Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird | Sample Grad (DirectX HLSL-Textur Objekt)
ms.assetid: f3d73296-23c4-4178-b89e-6f84cfcb48a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 236c453f3636452cbba8ed6000b2416e5187898d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219180"
---
# <a name="samplegrad-directx-hlsl-texture-object"></a><span data-ttu-id="dd7d7-104">Sample Grad (DirectX HLSL-Textur Objekt)</span><span class="sxs-lookup"><span data-stu-id="dd7d7-104">SampleGrad (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="dd7d7-105">Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird</span><span class="sxs-lookup"><span data-stu-id="dd7d7-105">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>



|                                                                                                            |
|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd7d7-106">&lt;Template Type &gt; Object. samplegrad (Sampler \_ State S, float Location, float DDX, float DDY \[ , int Offset \] );</span><span class="sxs-lookup"><span data-stu-id="dd7d7-106">&lt;Template Type&gt; Object.SampleGrad( sampler\_state S, float Location, float DDX, float DDY \[, int Offset\] );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="dd7d7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd7d7-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dd7d7-108">Element</span><span class="sxs-lookup"><span data-stu-id="dd7d7-108">Item</span></span></th>
<th><span data-ttu-id="dd7d7-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd7d7-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dd7d7-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em></span><span class="sxs-lookup"><span data-stu-id="dd7d7-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="dd7d7-111">Ein beliebiger <a href="dx-graphics-hlsl-to-type.md">Textur Objekttyp</a> (mit Ausnahme von Texture2DMS und Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="dd7d7-111">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd7d7-112"><span id="S"></span><span id="s"></span><em>Hymnen</em></span><span class="sxs-lookup"><span data-stu-id="dd7d7-112"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="dd7d7-113">in Ein <a href="dx-graphics-hlsl-sampler.md">samplerzustand</a>.</span><span class="sxs-lookup"><span data-stu-id="dd7d7-113">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="dd7d7-114">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="dd7d7-114">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd7d7-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Hotels</em></span><span class="sxs-lookup"><span data-stu-id="dd7d7-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="dd7d7-116">in Die Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="dd7d7-116">[in] The Texture coordinates.</span></span> <span data-ttu-id="dd7d7-117">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="dd7d7-117">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dd7d7-118">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="dd7d7-118">Texture-Object Type</span></span></th>
<th><span data-ttu-id="dd7d7-119">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="dd7d7-119">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dd7d7-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="dd7d7-120">Texture1D</span></span></td>
<td><span data-ttu-id="dd7d7-121">float</span><span class="sxs-lookup"><span data-stu-id="dd7d7-121">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd7d7-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="dd7d7-122">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="dd7d7-123">float2</span><span class="sxs-lookup"><span data-stu-id="dd7d7-123">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd7d7-124">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="dd7d7-124">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="dd7d7-125">float3</span><span class="sxs-lookup"><span data-stu-id="dd7d7-125">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd7d7-126">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="dd7d7-126">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="dd7d7-127">float4</span><span class="sxs-lookup"><span data-stu-id="dd7d7-127">float4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd7d7-128">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="dd7d7-128">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="dd7d7-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dd7d7-129">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd7d7-130"><span id="DDX"></span><span id="ddx"></span><em>DDX</em></span><span class="sxs-lookup"><span data-stu-id="dd7d7-130"><span id="DDX"></span><span id="ddx"></span><em>DDX</em></span></span></p></td>
<td><p><span data-ttu-id="dd7d7-131">in Die Änderungs Rate der Oberflächengeometrie in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="dd7d7-131">[in] The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="dd7d7-132">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="dd7d7-132">The argument type is dependent on the texture-object type.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dd7d7-133">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="dd7d7-133">Texture-Object Type</span></span></th>
<th><span data-ttu-id="dd7d7-134">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="dd7d7-134">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dd7d7-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="dd7d7-135">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="dd7d7-136">float</span><span class="sxs-lookup"><span data-stu-id="dd7d7-136">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd7d7-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="dd7d7-137">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="dd7d7-138">float2</span><span class="sxs-lookup"><span data-stu-id="dd7d7-138">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd7d7-139">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="dd7d7-139">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="dd7d7-140">float3</span><span class="sxs-lookup"><span data-stu-id="dd7d7-140">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd7d7-141">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="dd7d7-141">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="dd7d7-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dd7d7-142">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd7d7-143"><span id="DDY"></span><span id="ddy"></span><em>Tziger</em></span><span class="sxs-lookup"><span data-stu-id="dd7d7-143"><span id="DDY"></span><span id="ddy"></span><em>DDY</em></span></span></p></td>
<td><p><span data-ttu-id="dd7d7-144">in Die Änderungs Rate der Oberflächengeometrie in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="dd7d7-144">[in] The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="dd7d7-145">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="dd7d7-145">The argument type is dependent on the texture-object type.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dd7d7-146">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="dd7d7-146">Texture-Object Type</span></span></th>
<th><span data-ttu-id="dd7d7-147">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="dd7d7-147">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dd7d7-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="dd7d7-148">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="dd7d7-149">float</span><span class="sxs-lookup"><span data-stu-id="dd7d7-149">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd7d7-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="dd7d7-150">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="dd7d7-151">float2</span><span class="sxs-lookup"><span data-stu-id="dd7d7-151">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd7d7-152">Texture3D, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="dd7d7-152">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="dd7d7-153">float3</span><span class="sxs-lookup"><span data-stu-id="dd7d7-153">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd7d7-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="dd7d7-154">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="dd7d7-155">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dd7d7-155">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd7d7-156"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Kompensieren</em></span><span class="sxs-lookup"><span data-stu-id="dd7d7-156"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="dd7d7-157">in Ein optionaler Offset der Textur Koordinate, der für beliebige Textur Objekttypen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="dd7d7-157">[in] An optional texture coordinate offset, which can be used for any texture-object types.</span></span> <span data-ttu-id="dd7d7-158">Der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="dd7d7-158">The offset is applied to the location before sampling.</span></span> <span data-ttu-id="dd7d7-159">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="dd7d7-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="dd7d7-160">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="dd7d7-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="dd7d7-161">Weitere Informationen finden Sie unter<a href="dx-graphics-hlsl-to-sample.md">Anwenden von ganzzahligen Offsets</a>.</span><span class="sxs-lookup"><span data-stu-id="dd7d7-161">For more info, see<a href="dx-graphics-hlsl-to-sample.md">Applying Integer Offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dd7d7-162">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="dd7d7-162">Texture-Object Type</span></span></th>
<th><span data-ttu-id="dd7d7-163">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="dd7d7-163">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dd7d7-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="dd7d7-164">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="dd7d7-165">INT</span><span class="sxs-lookup"><span data-stu-id="dd7d7-165">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd7d7-166">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="dd7d7-166">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="dd7d7-167">int2</span><span class="sxs-lookup"><span data-stu-id="dd7d7-167">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd7d7-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="dd7d7-168">Texture3D</span></span></td>
<td><span data-ttu-id="dd7d7-169">int3</span><span class="sxs-lookup"><span data-stu-id="dd7d7-169">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd7d7-170">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="dd7d7-170">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="dd7d7-171">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dd7d7-171">not supported</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd7d7-172">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="dd7d7-172">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="dd7d7-173">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dd7d7-173">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="dd7d7-174">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd7d7-174">Return Value</span></span>

<span data-ttu-id="dd7d7-175">Der Vorlagentyp der Textur, bei dem es sich um einen Vektor mit einer einzelnen oder mehreren Komponenten handeln kann.</span><span class="sxs-lookup"><span data-stu-id="dd7d7-175">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="dd7d7-176">Das Format basiert auf dem [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)der Textur.</span><span class="sxs-lookup"><span data-stu-id="dd7d7-176">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="dd7d7-177">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="dd7d7-177">Minimum Shader Model</span></span>

<span data-ttu-id="dd7d7-178">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd7d7-178">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dd7d7-179">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dd7d7-179">vs\_4\_0</span></span> | <span data-ttu-id="dd7d7-180">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dd7d7-180">vs\_4\_1</span></span>  | <span data-ttu-id="dd7d7-181">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dd7d7-181">ps\_4\_0</span></span> | <span data-ttu-id="dd7d7-182">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dd7d7-182">ps\_4\_1</span></span>  | <span data-ttu-id="dd7d7-183">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dd7d7-183">gs\_4\_0</span></span> | <span data-ttu-id="dd7d7-184">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dd7d7-184">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="dd7d7-185">x</span><span class="sxs-lookup"><span data-stu-id="dd7d7-185">x</span></span>        | <span data-ttu-id="dd7d7-186">x</span><span class="sxs-lookup"><span data-stu-id="dd7d7-186">x</span></span>         | <span data-ttu-id="dd7d7-187">x</span><span class="sxs-lookup"><span data-stu-id="dd7d7-187">x</span></span>        | <span data-ttu-id="dd7d7-188">x</span><span class="sxs-lookup"><span data-stu-id="dd7d7-188">x</span></span>         | <span data-ttu-id="dd7d7-189">x</span><span class="sxs-lookup"><span data-stu-id="dd7d7-189">x</span></span>        | <span data-ttu-id="dd7d7-190">x</span><span class="sxs-lookup"><span data-stu-id="dd7d7-190">x</span></span>         |



 

1.  <span data-ttu-id="dd7d7-191">Texturecubearray ist im Shader-Modell 4,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dd7d7-191">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="dd7d7-192">Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dd7d7-192">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="dd7d7-193">Beispiel</span><span class="sxs-lookup"><span data-stu-id="dd7d7-193">Example</span></span>

<span data-ttu-id="dd7d7-194">Dieses partielle Codebeispiel wird aus der Datei "" in der Datei "" in der Datei " [MotionBlur10](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx)" aus dem Beispiel</span><span class="sxs-lookup"><span data-stu-id="dd7d7-194">This partial code example is from the MotionBlur.fx file in the [MotionBlur10 Sample](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).</span></span>


```
// Object Declarations
Texture2D g_txDiffuse;

SamplerState g_samLinear
{
    Filter = ANISOTROPIC;
    MaxAnisotropy = 8;
    AddressU = Wrap;
    AddressV = Wrap;
};

struct VSSceneOut
{
    float4 Pos : SV_POSITION;
    float4 Color : COLOR0;
    float2 Tex : TEXCOORD;
    float2 Aniso : ANISOTROPY;
};

float4 PSSceneMain( VSSceneOut Input ) : SV_TARGET
{
    float2 ddx = Input.Aniso;
    float2 ddy = Input.Aniso;
    
    // Shader body calling the intrinsic function
    float4 diff = g_txDiffuse.SampleGrad( g_samLinear, Input.Tex, ddx, ddy);
    
    ...
}
```



## <a name="related-topics"></a><span data-ttu-id="dd7d7-195">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd7d7-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd7d7-196">Texture-Objekt</span><span class="sxs-lookup"><span data-stu-id="dd7d7-196">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

