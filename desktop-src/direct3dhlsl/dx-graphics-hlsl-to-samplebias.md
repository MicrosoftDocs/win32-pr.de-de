---
title: SampleBias (DirectX HLSL-Texturobjekt)
description: Samples a texture, after applying the input bias to the mipmap level.
ms.assetid: 1bc03ad8-7b69-4001-81c7-64d8c631d68d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 01087ab36bdbe90ff73643899229c7ec6ccfbdbe
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826795"
---
# <a name="samplebias-directx-hlsl-texture-object"></a><span data-ttu-id="d394a-103">SampleBias (DirectX HLSL-Texturobjekt)</span><span class="sxs-lookup"><span data-stu-id="d394a-103">SampleBias (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="d394a-104">Samples a texture, after applying the input bias to the mipmap level.</span><span class="sxs-lookup"><span data-stu-id="d394a-104">Samples a texture, after applying the input bias to the mipmap level.</span></span>

<span data-ttu-id="d394a-105">&lt;Vorlagentyp &gt; Object.SampleBias( \_ Samplerzustand S, float Location, float Bias \[ , int Offset \] );</span><span class="sxs-lookup"><span data-stu-id="d394a-105">&lt;Template Type&gt; Object.SampleBias( sampler\_state S, float Location, float Bias \[, int Offset\] );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="d394a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d394a-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d394a-107">Element</span><span class="sxs-lookup"><span data-stu-id="d394a-107">Item</span></span></th>
<th><span data-ttu-id="d394a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d394a-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d394a-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em></span><span class="sxs-lookup"><span data-stu-id="d394a-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="d394a-110">Beliebiger <a href="dx-graphics-hlsl-to-type.md">Texturobjekttyp</a> (außer Texture2DMS und Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="d394a-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d394a-111"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="d394a-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="d394a-112">[in] Ein <a href="dx-graphics-hlsl-sampler.md">Samplerzustand.</a></span><span class="sxs-lookup"><span data-stu-id="d394a-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="d394a-113">Dies ist ein Objekt, das in einer Effektdatei deklariert ist, die Zustandszuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="d394a-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d394a-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Lage</em></span><span class="sxs-lookup"><span data-stu-id="d394a-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="d394a-115">[in] Die Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="d394a-115">[in] The texture coordinates.</span></span> <span data-ttu-id="d394a-116">Der Argumenttyp ist vom Texturobjekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="d394a-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d394a-117">Texture-Object Typ</span><span class="sxs-lookup"><span data-stu-id="d394a-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="d394a-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="d394a-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d394a-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d394a-119">Texture1D</span></span></td>
<td><span data-ttu-id="d394a-120">float</span><span class="sxs-lookup"><span data-stu-id="d394a-120">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d394a-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="d394a-121">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="d394a-122">float2</span><span class="sxs-lookup"><span data-stu-id="d394a-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d394a-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="d394a-123">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="d394a-124">float3</span><span class="sxs-lookup"><span data-stu-id="d394a-124">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d394a-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d394a-125">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="d394a-126">float4</span><span class="sxs-lookup"><span data-stu-id="d394a-126">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d394a-127"><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Vorurteil</em></span><span class="sxs-lookup"><span data-stu-id="d394a-127"><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Bias</em></span></span></p></td>
<td><p><span data-ttu-id="d394a-128">[in] Der Biaswert, bei dem es sich um eine Gleitkommazahl zwischen -16,0 und 15,99 handelt, wird vor der Stichprobenentnahme auf eine MIP-Ebene angewendet.</span><span class="sxs-lookup"><span data-stu-id="d394a-128">[in] The bias value, which is a floating-point number between -16.0 and 15.99, is applied to a mip level before sampling.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d394a-129"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span><span class="sxs-lookup"><span data-stu-id="d394a-129"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="d394a-130">[in] Ein optionaler Texturkoordinatenoffset, der für jeden Texturobjekttyp verwendet werden kann. Der Offset wird vor der Stichprobenentnahme auf die Position angewendet.</span><span class="sxs-lookup"><span data-stu-id="d394a-130">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="d394a-131">Die Texturoffsets müssen statisch sein.</span><span class="sxs-lookup"><span data-stu-id="d394a-131">The texture offsets need to be static.</span></span> <span data-ttu-id="d394a-132">Der Argumenttyp ist vom Texturobjekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="d394a-132">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="d394a-133">Weitere Informationen finden Sie unter <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Anwenden von Texturkoordinatenoffsets.</a></span><span class="sxs-lookup"><span data-stu-id="d394a-133">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d394a-134">Texture-Object Typ</span><span class="sxs-lookup"><span data-stu-id="d394a-134">Texture-Object Type</span></span></th>
<th><span data-ttu-id="d394a-135">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="d394a-135">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d394a-136">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d394a-136">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="d394a-137">INT</span><span class="sxs-lookup"><span data-stu-id="d394a-137">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d394a-138">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d394a-138">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="d394a-139">int2</span><span class="sxs-lookup"><span data-stu-id="d394a-139">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d394a-140">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d394a-140">Texture3D</span></span></td>
<td><span data-ttu-id="d394a-141">int3</span><span class="sxs-lookup"><span data-stu-id="d394a-141">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d394a-142">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d394a-142">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="d394a-143">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d394a-143">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="d394a-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d394a-144">Return Value</span></span>

<span data-ttu-id="d394a-145">Der Vorlagentyp der Textur, der ein Vektor mit einer oder mehreren Komponenten sein kann.</span><span class="sxs-lookup"><span data-stu-id="d394a-145">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="d394a-146">Das Format basiert auf dem DXGI FORMAT der [**\_ Textur.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="d394a-146">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="d394a-147">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d394a-147">Minimum Shader Model</span></span>

<span data-ttu-id="d394a-148">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d394a-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d394a-149">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d394a-149">vs\_4\_0</span></span> | <span data-ttu-id="d394a-150">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d394a-150">vs\_4\_1</span></span>  | <span data-ttu-id="d394a-151">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d394a-151">ps\_4\_0</span></span> | <span data-ttu-id="d394a-152">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d394a-152">ps\_4\_1</span></span>  | <span data-ttu-id="d394a-153">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d394a-153">gs\_4\_0</span></span> | <span data-ttu-id="d394a-154">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d394a-154">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="d394a-155">x</span><span class="sxs-lookup"><span data-stu-id="d394a-155">x</span></span>        | <span data-ttu-id="d394a-156">x</span><span class="sxs-lookup"><span data-stu-id="d394a-156">x</span></span>         |          |           |



 

1.  <span data-ttu-id="d394a-157">TextureCubeArray ist in Shader Model 4.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d394a-157">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="d394a-158">ShaderModell 4.1 ist in Direct3D 10.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d394a-158">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d394a-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d394a-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d394a-160">Texture-Object</span><span class="sxs-lookup"><span data-stu-id="d394a-160">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

