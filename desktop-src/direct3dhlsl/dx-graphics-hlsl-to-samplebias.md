---
title: Sample Bias (DirectX HLSL-Textur Objekt)
description: Gibt eine Textur aus, nachdem die Eingabe Abweichung auf die MipMap-Ebene angewendet wurde.
ms.assetid: 1bc03ad8-7b69-4001-81c7-64d8c631d68d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e710b8a6c7dd2983c6d0c635d16356f95d0b4fe7
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "104391283"
---
# <a name="samplebias-directx-hlsl-texture-object"></a><span data-ttu-id="639a9-103">Sample Bias (DirectX HLSL-Textur Objekt)</span><span class="sxs-lookup"><span data-stu-id="639a9-103">SampleBias (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="639a9-104">Gibt eine Textur aus, nachdem die Eingabe Abweichung auf die MipMap-Ebene angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="639a9-104">Samples a texture, after applying the input bias to the mipmap level.</span></span>



|                                                                                                  |
|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="639a9-105">&lt;Template Type &gt; Object. Sample Bias (Sampler \_ State S, float Location, float Bias \[ , int Offset \] );</span><span class="sxs-lookup"><span data-stu-id="639a9-105">&lt;Template Type&gt; Object.SampleBias( sampler\_state S, float Location, float Bias \[, int Offset\] );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="639a9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="639a9-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="639a9-107">Element</span><span class="sxs-lookup"><span data-stu-id="639a9-107">Item</span></span></th>
<th><span data-ttu-id="639a9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="639a9-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="639a9-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em></span><span class="sxs-lookup"><span data-stu-id="639a9-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="639a9-110">Ein beliebiger <a href="dx-graphics-hlsl-to-type.md">Textur Objekttyp</a> (mit Ausnahme von Texture2DMS und Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="639a9-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="639a9-111"><span id="S"></span><span id="s"></span><em>Hymnen</em></span><span class="sxs-lookup"><span data-stu-id="639a9-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="639a9-112">in Ein <a href="dx-graphics-hlsl-sampler.md">samplerzustand</a>.</span><span class="sxs-lookup"><span data-stu-id="639a9-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="639a9-113">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="639a9-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="639a9-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Hotels</em></span><span class="sxs-lookup"><span data-stu-id="639a9-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="639a9-115">in Die Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="639a9-115">[in] The texture coordinates.</span></span> <span data-ttu-id="639a9-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="639a9-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="639a9-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="639a9-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="639a9-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="639a9-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="639a9-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="639a9-119">Texture1D</span></span></td>
<td><span data-ttu-id="639a9-120">float</span><span class="sxs-lookup"><span data-stu-id="639a9-120">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="639a9-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="639a9-121">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="639a9-122">float2</span><span class="sxs-lookup"><span data-stu-id="639a9-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="639a9-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="639a9-123">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="639a9-124">float3</span><span class="sxs-lookup"><span data-stu-id="639a9-124">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="639a9-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="639a9-125">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="639a9-126">float4</span><span class="sxs-lookup"><span data-stu-id="639a9-126">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="639a9-127"><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Eingenommen</em></span><span class="sxs-lookup"><span data-stu-id="639a9-127"><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Bias</em></span></span></p></td>
<td><p><span data-ttu-id="639a9-128">in Der Bias-Wert, bei dem es sich um eine Gleit Komma Zahl zwischen-16,0 und 15,99 handelt, wird vor der Stichprobenentnahme auf eine MIP-Ebene angewendet.</span><span class="sxs-lookup"><span data-stu-id="639a9-128">[in] The bias value, which is a floating-point number between -16.0 and 15.99, is applied to a mip level before sampling.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="639a9-129"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Kompensieren</em></span><span class="sxs-lookup"><span data-stu-id="639a9-129"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="639a9-130">in Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="639a9-130">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="639a9-131">Die Textur Offsets müssen statisch sein.</span><span class="sxs-lookup"><span data-stu-id="639a9-131">The texture offsets need to be static.</span></span> <span data-ttu-id="639a9-132">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="639a9-132">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="639a9-133">Weitere Informationen finden Sie unter <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Anwenden von Texturkoordinaten Offsets</a>.</span><span class="sxs-lookup"><span data-stu-id="639a9-133">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="639a9-134">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="639a9-134">Texture-Object Type</span></span></th>
<th><span data-ttu-id="639a9-135">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="639a9-135">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="639a9-136">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="639a9-136">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="639a9-137">INT</span><span class="sxs-lookup"><span data-stu-id="639a9-137">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="639a9-138">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="639a9-138">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="639a9-139">int2</span><span class="sxs-lookup"><span data-stu-id="639a9-139">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="639a9-140">Texture3D</span><span class="sxs-lookup"><span data-stu-id="639a9-140">Texture3D</span></span></td>
<td><span data-ttu-id="639a9-141">int3</span><span class="sxs-lookup"><span data-stu-id="639a9-141">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="639a9-142">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="639a9-142">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="639a9-143">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="639a9-143">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="639a9-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="639a9-144">Return Value</span></span>

<span data-ttu-id="639a9-145">Der Vorlagentyp der Textur, bei dem es sich um einen Vektor mit einer einzelnen oder mehreren Komponenten handeln kann.</span><span class="sxs-lookup"><span data-stu-id="639a9-145">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="639a9-146">Das Format basiert auf dem [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)der Textur.</span><span class="sxs-lookup"><span data-stu-id="639a9-146">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="639a9-147">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="639a9-147">Minimum Shader Model</span></span>

<span data-ttu-id="639a9-148">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="639a9-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="639a9-149">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="639a9-149">vs\_4\_0</span></span> | <span data-ttu-id="639a9-150">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="639a9-150">vs\_4\_1</span></span>  | <span data-ttu-id="639a9-151">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="639a9-151">ps\_4\_0</span></span> | <span data-ttu-id="639a9-152">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="639a9-152">ps\_4\_1</span></span>  | <span data-ttu-id="639a9-153">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="639a9-153">gs\_4\_0</span></span> | <span data-ttu-id="639a9-154">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="639a9-154">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="639a9-155">x</span><span class="sxs-lookup"><span data-stu-id="639a9-155">x</span></span>        | <span data-ttu-id="639a9-156">x</span><span class="sxs-lookup"><span data-stu-id="639a9-156">x</span></span>         |          |           |



 

1.  <span data-ttu-id="639a9-157">Texturecubearray ist im Shader-Modell 4,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="639a9-157">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="639a9-158">Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="639a9-158">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="639a9-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="639a9-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="639a9-160">Texture-Objekt</span><span class="sxs-lookup"><span data-stu-id="639a9-160">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

