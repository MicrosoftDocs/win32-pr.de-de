---
title: SampleGrad (DirectX HLSL-Texturobjekt)
description: Probieren Sie eine Textur mithilfe eines Farbverlaufs aus, um die Art und Weise zu beeinflussen, wie die Stichprobenposition berechnet wird. | SampleGrad (DirectX HLSL-Texturobjekt)
ms.assetid: f3d73296-23c4-4178-b89e-6f84cfcb48a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 959304d36da2b95bdf6289fba1b8c75d6ecfa314
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825737"
---
# <a name="samplegrad-directx-hlsl-texture-object"></a><span data-ttu-id="0c403-104">SampleGrad (DirectX HLSL-Texturobjekt)</span><span class="sxs-lookup"><span data-stu-id="0c403-104">SampleGrad (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="0c403-105">Probieren Sie eine Textur mithilfe eines Farbverlaufs aus, um die Art und Weise zu beeinflussen, wie die Stichprobenposition berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="0c403-105">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>

<span data-ttu-id="0c403-106">&lt;Vorlagentyp &gt; Object.SampleGrad( sampler \_ state S, float Location, float DDX, float DDY \[ , int Offset \] );</span><span class="sxs-lookup"><span data-stu-id="0c403-106">&lt;Template Type&gt; Object.SampleGrad( sampler\_state S, float Location, float DDX, float DDY \[, int Offset\] );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="0c403-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c403-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0c403-108">Element</span><span class="sxs-lookup"><span data-stu-id="0c403-108">Item</span></span></th>
<th><span data-ttu-id="0c403-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c403-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0c403-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em></span><span class="sxs-lookup"><span data-stu-id="0c403-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="0c403-111">Jeder <a href="dx-graphics-hlsl-to-type.md">Texturobjekttyp</a> (mit Ausnahme von Texture2DMS und Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="0c403-111">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c403-112"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="0c403-112"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="0c403-113">[in] Ein <a href="dx-graphics-hlsl-sampler.md">Samplerzustand.</a></span><span class="sxs-lookup"><span data-stu-id="0c403-113">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="0c403-114">Dies ist ein Objekt, das in einer Effektdatei deklariert ist, die Zustandszuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="0c403-114">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c403-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Lage</em></span><span class="sxs-lookup"><span data-stu-id="0c403-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="0c403-116">[in] Die Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="0c403-116">[in] The Texture coordinates.</span></span> <span data-ttu-id="0c403-117">Der Argumenttyp ist vom Texturobjekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="0c403-117">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0c403-118">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="0c403-118">Texture-Object Type</span></span></th>
<th><span data-ttu-id="0c403-119">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="0c403-119">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0c403-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0c403-120">Texture1D</span></span></td>
<td><span data-ttu-id="0c403-121">float</span><span class="sxs-lookup"><span data-stu-id="0c403-121">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c403-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="0c403-122">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="0c403-123">float2</span><span class="sxs-lookup"><span data-stu-id="0c403-123">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c403-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="0c403-124">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="0c403-125">float3</span><span class="sxs-lookup"><span data-stu-id="0c403-125">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c403-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0c403-126">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="0c403-127">float4</span><span class="sxs-lookup"><span data-stu-id="0c403-127">float4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c403-128">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="0c403-128">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="0c403-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0c403-129">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c403-130"><span id="DDX"></span><span id="ddx"></span><em>Ddx</em></span><span class="sxs-lookup"><span data-stu-id="0c403-130"><span id="DDX"></span><span id="ddx"></span><em>DDX</em></span></span></p></td>
<td><p><span data-ttu-id="0c403-131">[in] Die Änderungsrate der Oberflächengeometrie in x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="0c403-131">[in] The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="0c403-132">Der Argumenttyp ist vom Texturobjekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="0c403-132">The argument type is dependent on the texture-object type.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0c403-133">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="0c403-133">Texture-Object Type</span></span></th>
<th><span data-ttu-id="0c403-134">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="0c403-134">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0c403-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="0c403-135">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="0c403-136">float</span><span class="sxs-lookup"><span data-stu-id="0c403-136">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c403-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="0c403-137">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="0c403-138">float2</span><span class="sxs-lookup"><span data-stu-id="0c403-138">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c403-139">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0c403-139">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="0c403-140">float3</span><span class="sxs-lookup"><span data-stu-id="0c403-140">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c403-141">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="0c403-141">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="0c403-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0c403-142">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c403-143"><span id="DDY"></span><span id="ddy"></span><em>DDY</em></span><span class="sxs-lookup"><span data-stu-id="0c403-143"><span id="DDY"></span><span id="ddy"></span><em>DDY</em></span></span></p></td>
<td><p><span data-ttu-id="0c403-144">[in] Die Änderungsrate der Oberflächengeometrie in y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="0c403-144">[in] The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="0c403-145">Der Argumenttyp ist vom Texturobjekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="0c403-145">The argument type is dependent on the texture-object type.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0c403-146">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="0c403-146">Texture-Object Type</span></span></th>
<th><span data-ttu-id="0c403-147">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="0c403-147">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0c403-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="0c403-148">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="0c403-149">float</span><span class="sxs-lookup"><span data-stu-id="0c403-149">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c403-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="0c403-150">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="0c403-151">float2</span><span class="sxs-lookup"><span data-stu-id="0c403-151">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c403-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0c403-152">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="0c403-153">float3</span><span class="sxs-lookup"><span data-stu-id="0c403-153">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c403-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="0c403-154">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="0c403-155">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0c403-155">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c403-156"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span><span class="sxs-lookup"><span data-stu-id="0c403-156"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="0c403-157">[in] Ein optionaler Texturkoordinatenoffset, der für jeden Texturobjekttyp verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0c403-157">[in] An optional texture coordinate offset, which can be used for any texture-object types.</span></span> <span data-ttu-id="0c403-158">Der Offset wird vor der Stichprobenentnahme auf die Position angewendet.</span><span class="sxs-lookup"><span data-stu-id="0c403-158">The offset is applied to the location before sampling.</span></span> <span data-ttu-id="0c403-159">Verwenden Sie einen Offset nur auf einem ganzzahligen Miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die sich nicht gut in die Hardware übersetzen lassen.</span><span class="sxs-lookup"><span data-stu-id="0c403-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="0c403-160">Der Argumenttyp ist vom Texturobjekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="0c403-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="0c403-161">Weitere Informationen finden Sie unter<a href="dx-graphics-hlsl-to-sample.md">Anwenden von ganzzahligen Offsets.</a></span><span class="sxs-lookup"><span data-stu-id="0c403-161">For more info, see<a href="dx-graphics-hlsl-to-sample.md">Applying Integer Offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0c403-162">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="0c403-162">Texture-Object Type</span></span></th>
<th><span data-ttu-id="0c403-163">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="0c403-163">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0c403-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="0c403-164">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="0c403-165">INT</span><span class="sxs-lookup"><span data-stu-id="0c403-165">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c403-166">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="0c403-166">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="0c403-167">int2</span><span class="sxs-lookup"><span data-stu-id="0c403-167">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c403-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0c403-168">Texture3D</span></span></td>
<td><span data-ttu-id="0c403-169">int3</span><span class="sxs-lookup"><span data-stu-id="0c403-169">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c403-170">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0c403-170">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="0c403-171">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0c403-171">not supported</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c403-172">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="0c403-172">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="0c403-173">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0c403-173">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="0c403-174">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c403-174">Return Value</span></span>

<span data-ttu-id="0c403-175">Der Vorlagentyp der Textur, bei dem es sich um einen Ein- oder Mehrkomponentenvektor aussetzen kann.</span><span class="sxs-lookup"><span data-stu-id="0c403-175">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="0c403-176">Das Format basiert auf dem [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)der Textur.</span><span class="sxs-lookup"><span data-stu-id="0c403-176">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="0c403-177">Shader-Mindestmodell</span><span class="sxs-lookup"><span data-stu-id="0c403-177">Minimum Shader Model</span></span>

<span data-ttu-id="0c403-178">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0c403-178">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0c403-179">Vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0c403-179">vs\_4\_0</span></span> | <span data-ttu-id="0c403-180">Vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0c403-180">vs\_4\_1</span></span>  | <span data-ttu-id="0c403-181">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0c403-181">ps\_4\_0</span></span> | <span data-ttu-id="0c403-182">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0c403-182">ps\_4\_1</span></span>  | <span data-ttu-id="0c403-183">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0c403-183">gs\_4\_0</span></span> | <span data-ttu-id="0c403-184">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0c403-184">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="0c403-185">x</span><span class="sxs-lookup"><span data-stu-id="0c403-185">x</span></span>        | <span data-ttu-id="0c403-186">x</span><span class="sxs-lookup"><span data-stu-id="0c403-186">x</span></span>         | <span data-ttu-id="0c403-187">x</span><span class="sxs-lookup"><span data-stu-id="0c403-187">x</span></span>        | <span data-ttu-id="0c403-188">x</span><span class="sxs-lookup"><span data-stu-id="0c403-188">x</span></span>         | <span data-ttu-id="0c403-189">x</span><span class="sxs-lookup"><span data-stu-id="0c403-189">x</span></span>        | <span data-ttu-id="0c403-190">x</span><span class="sxs-lookup"><span data-stu-id="0c403-190">x</span></span>         |



 

1.  <span data-ttu-id="0c403-191">TextureCubeArray ist im Shadermodell 4.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0c403-191">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="0c403-192">Shadermodell 4.1 ist in Direct3D 10.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0c403-192">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="0c403-193">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0c403-193">Example</span></span>

<span data-ttu-id="0c403-194">Dieses Teilcodebeispiel stammt aus der Datei MotionBlur.fx im [MotionBlur10-Beispiel.](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="0c403-194">This partial code example is from the MotionBlur.fx file in the [MotionBlur10 Sample](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0c403-195">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0c403-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c403-196">Texturobjekt</span><span class="sxs-lookup"><span data-stu-id="0c403-196">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

