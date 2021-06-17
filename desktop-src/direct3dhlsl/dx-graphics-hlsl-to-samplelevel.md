---
title: SampleLevel (DirectX HLSL-Texturobjekt)
description: Probieren Sie eine Textur mithilfe eines Offsets auf Mipmapebene aus.
ms.assetid: d61426c8-e09f-4e88-99f6-fa96c4a2b58d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bc3a074641ce5b15a3d837e8bd91dfdae09fe627
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826684"
---
# <a name="samplelevel-directx-hlsl-texture-object"></a><span data-ttu-id="cb6c2-103">SampleLevel (DirectX HLSL-Texturobjekt)</span><span class="sxs-lookup"><span data-stu-id="cb6c2-103">SampleLevel (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="cb6c2-104">Probieren Sie eine Textur mithilfe eines Offsets auf Mipmapebene aus.</span><span class="sxs-lookup"><span data-stu-id="cb6c2-104">Samples a texture using a mipmap-level offset.</span></span>

<span data-ttu-id="cb6c2-105">&lt;Vorlagentyp &gt; Object.SampleLevel( sampler \_ state S, float Location, float LOD \[ , int Offset \] );</span><span class="sxs-lookup"><span data-stu-id="cb6c2-105">&lt;Template Type&gt; Object.SampleLevel( sampler\_state S, float Location, float LOD \[, int Offset\] );</span></span>



 

<span data-ttu-id="cb6c2-106">Diese Funktion ähnelt [Sample,](dx-graphics-hlsl-to-sample.md) mit der Ausnahme, dass sie die LOD-Ebene (in der letzten Komponente des Location-Parameters) verwendet, um die Mipmapebene auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="cb6c2-106">This function is similar to [Sample](dx-graphics-hlsl-to-sample.md) except that it uses the LOD level (in the last component of the location parameter) to choose the mipmap level.</span></span> <span data-ttu-id="cb6c2-107">Beispielsweise verwendet eine 2D-Textur die ersten beiden Komponenten für UV-Koordinaten und die dritte Komponente für die Mipmapebene.</span><span class="sxs-lookup"><span data-stu-id="cb6c2-107">For example, a 2D texture uses the first two components for uv coordinates and the third component for the mipmap level.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb6c2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb6c2-108">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb6c2-109">Element</span><span class="sxs-lookup"><span data-stu-id="cb6c2-109">Item</span></span></th>
<th><span data-ttu-id="cb6c2-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb6c2-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cb6c2-111"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em></span><span class="sxs-lookup"><span data-stu-id="cb6c2-111"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="cb6c2-112">Jeder <a href="dx-graphics-hlsl-to-type.md">Texturobjekttyp</a> (mit Ausnahme von Texture2DMS und Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="cb6c2-112">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb6c2-113"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="cb6c2-113"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="cb6c2-114">[in] Ein <a href="dx-graphics-hlsl-sampler.md">Samplerzustand.</a></span><span class="sxs-lookup"><span data-stu-id="cb6c2-114">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="cb6c2-115">Dies ist ein Objekt, das in einer Effektdatei deklariert ist, die Zustandszuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="cb6c2-115">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb6c2-116"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Lage</em></span><span class="sxs-lookup"><span data-stu-id="cb6c2-116"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="cb6c2-117">[in] Die Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="cb6c2-117">[in] The texture coordinates.</span></span> <span data-ttu-id="cb6c2-118">Der Argumenttyp ist vom Texturobjekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="cb6c2-118">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cb6c2-119">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="cb6c2-119">Texture-Object Type</span></span></th>
<th><span data-ttu-id="cb6c2-120">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="cb6c2-120">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cb6c2-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="cb6c2-121">Texture1D</span></span></td>
<td><span data-ttu-id="cb6c2-122">float</span><span class="sxs-lookup"><span data-stu-id="cb6c2-122">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb6c2-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="cb6c2-123">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="cb6c2-124">float2</span><span class="sxs-lookup"><span data-stu-id="cb6c2-124">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb6c2-125">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="cb6c2-125">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="cb6c2-126">float3</span><span class="sxs-lookup"><span data-stu-id="cb6c2-126">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb6c2-127">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="cb6c2-127">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="cb6c2-128">float4</span><span class="sxs-lookup"><span data-stu-id="cb6c2-128">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="cb6c2-129">Wenn das Texturobjekt ein Array ist, ist die letzte Komponente der Arrayindex.</span><span class="sxs-lookup"><span data-stu-id="cb6c2-129">If the texture object is an array, the last component is the array index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb6c2-130"><span id="LOD"></span><span id="lod"></span><em>Lod</em></span><span class="sxs-lookup"><span data-stu-id="cb6c2-130"><span id="LOD"></span><span id="lod"></span><em>LOD</em></span></span></p></td>
<td><p><span data-ttu-id="cb6c2-131">[in] Eine Zahl, die die Mipmapebene angibt.</span><span class="sxs-lookup"><span data-stu-id="cb6c2-131">[in] A number that specifies the mipmap level.</span></span> <span data-ttu-id="cb6c2-132">Wenn der Wert = 0 ist, wird der Nullth (größte Karte) verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb6c2-132">If the value is = 0, the zero'th (biggest map) is used.</span></span> <span data-ttu-id="cb6c2-133">Der Bruchwert (sofern angegeben) wird verwendet, um zwischen zwei Mipmapebenen zu interpolieren.</span><span class="sxs-lookup"><span data-stu-id="cb6c2-133">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb6c2-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span><span class="sxs-lookup"><span data-stu-id="cb6c2-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="cb6c2-135">[in] Ein optionaler Texturkoordinatenoffset, der für jeden Texturobjekttyp verwendet werden kann. Der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="cb6c2-135">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="cb6c2-136">Die Texturoffsets müssen statisch sein.</span><span class="sxs-lookup"><span data-stu-id="cb6c2-136">The texture offsets need to be static.</span></span> <span data-ttu-id="cb6c2-137">Der Argumenttyp ist vom Texturobjekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="cb6c2-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="cb6c2-138">Weitere Informationen finden Sie unter <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Anwenden von Texturkoordinatenoffsets.</a></span><span class="sxs-lookup"><span data-stu-id="cb6c2-138">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cb6c2-139">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="cb6c2-139">Texture-Object Type</span></span></th>
<th><span data-ttu-id="cb6c2-140">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="cb6c2-140">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cb6c2-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="cb6c2-141">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="cb6c2-142">INT</span><span class="sxs-lookup"><span data-stu-id="cb6c2-142">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb6c2-143">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="cb6c2-143">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="cb6c2-144">int2</span><span class="sxs-lookup"><span data-stu-id="cb6c2-144">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb6c2-145">Texture3D</span><span class="sxs-lookup"><span data-stu-id="cb6c2-145">Texture3D</span></span></td>
<td><span data-ttu-id="cb6c2-146">int3</span><span class="sxs-lookup"><span data-stu-id="cb6c2-146">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb6c2-147">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="cb6c2-147">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="cb6c2-148">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cb6c2-148">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="cb6c2-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb6c2-149">Return Value</span></span>

<span data-ttu-id="cb6c2-150">Der Vorlagentyp der Textur, bei dem es sich um einen Ein- oder Mehrkomponentenvektor aussetzen kann.</span><span class="sxs-lookup"><span data-stu-id="cb6c2-150">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="cb6c2-151">Das Format basiert auf dem [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)der Textur.</span><span class="sxs-lookup"><span data-stu-id="cb6c2-151">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="cb6c2-152">Shader-Mindestmodell</span><span class="sxs-lookup"><span data-stu-id="cb6c2-152">Minimum Shader Model</span></span>

<span data-ttu-id="cb6c2-153">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cb6c2-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cb6c2-154">Vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cb6c2-154">vs\_4\_0</span></span> | <span data-ttu-id="cb6c2-155">Vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="cb6c2-155">vs\_4\_1</span></span>  | <span data-ttu-id="cb6c2-156">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cb6c2-156">ps\_4\_0</span></span> | <span data-ttu-id="cb6c2-157">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="cb6c2-157">ps\_4\_1</span></span>  | <span data-ttu-id="cb6c2-158">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cb6c2-158">gs\_4\_0</span></span> | <span data-ttu-id="cb6c2-159">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="cb6c2-159">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="cb6c2-160">x</span><span class="sxs-lookup"><span data-stu-id="cb6c2-160">x</span></span>        | <span data-ttu-id="cb6c2-161">x</span><span class="sxs-lookup"><span data-stu-id="cb6c2-161">x</span></span>         | <span data-ttu-id="cb6c2-162">x</span><span class="sxs-lookup"><span data-stu-id="cb6c2-162">x</span></span>        | <span data-ttu-id="cb6c2-163">x</span><span class="sxs-lookup"><span data-stu-id="cb6c2-163">x</span></span>         | <span data-ttu-id="cb6c2-164">x</span><span class="sxs-lookup"><span data-stu-id="cb6c2-164">x</span></span>        | <span data-ttu-id="cb6c2-165">x</span><span class="sxs-lookup"><span data-stu-id="cb6c2-165">x</span></span>         |



 

1.  <span data-ttu-id="cb6c2-166">TextureCubeArray ist im Shadermodell 4.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cb6c2-166">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="cb6c2-167">Shadermodell 4.1 ist in Direct3D 10.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cb6c2-167">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="cb6c2-168">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cb6c2-168">Example</span></span>

<span data-ttu-id="cb6c2-169">Dieses Teilcodebeispiel stammt aus der Datei Instancing.fx im [Beispiel Instancing10.](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="cb6c2-169">This partial code example is from the Instancing.fx file in the [Instancing10 Sample](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).</span></span>


```
// Object Declarations
Texture1D g_txRandom;

SamplerState g_samPoint
{
    Filter = MIN_MAG_MIP_POINT;
    AddressU = Wrap;
    AddressV = Wrap;
};

    
// Shader body calling the intrinsic function
float3 RandomDir(float fOffset)
{   
    float tCoord = (fOffset) / 300.0;
    return g_txRandom.SampleLevel( g_samPoint, tCoord, 0 );
   ...

```



## <a name="related-topics"></a><span data-ttu-id="cb6c2-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cb6c2-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb6c2-171">Texturobjekt</span><span class="sxs-lookup"><span data-stu-id="cb6c2-171">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

