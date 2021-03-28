---
title: Samplelevel (DirectX HLSL-Textur Objekt)
description: Gibt eine Textur mit einem Offset auf MipMap-Ebene aus.
ms.assetid: d61426c8-e09f-4e88-99f6-fa96c4a2b58d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73cf7bc0c13987099540cecd49519de35b4b7de1
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "104102590"
---
# <a name="samplelevel-directx-hlsl-texture-object"></a><span data-ttu-id="2fd2a-103">Samplelevel (DirectX HLSL-Textur Objekt)</span><span class="sxs-lookup"><span data-stu-id="2fd2a-103">SampleLevel (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="2fd2a-104">Gibt eine Textur mit einem Offset auf MipMap-Ebene aus.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-104">Samples a texture using a mipmap-level offset.</span></span>



|                                                                                                  |
|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd2a-105">&lt;Template Type &gt; Object. samplelevel (Sampler \_ State S, float Location, float Lod \[ , int Offset \] );</span><span class="sxs-lookup"><span data-stu-id="2fd2a-105">&lt;Template Type&gt; Object.SampleLevel( sampler\_state S, float Location, float LOD \[, int Offset\] );</span></span> |



 

<span data-ttu-id="2fd2a-106">Diese Funktion ähnelt [Sample](dx-graphics-hlsl-to-sample.md) , mit der Ausnahme, dass Sie die Lod-Ebene (in der letzten Komponente des Location-Parameters) verwendet, um die MipMap-Ebene auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-106">This function is similar to [Sample](dx-graphics-hlsl-to-sample.md) except that it uses the LOD level (in the last component of the location parameter) to choose the mipmap level.</span></span> <span data-ttu-id="2fd2a-107">Beispielsweise werden in einer 2D-Textur die ersten beiden Komponenten für UV-Koordinaten und die dritte Komponente für die MipMap-Ebene verwendet.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-107">For example, a 2D texture uses the first two components for uv coordinates and the third component for the mipmap level.</span></span>

## <a name="parameters"></a><span data-ttu-id="2fd2a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fd2a-108">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2fd2a-109">Element</span><span class="sxs-lookup"><span data-stu-id="2fd2a-109">Item</span></span></th>
<th><span data-ttu-id="2fd2a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fd2a-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2fd2a-111"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em></span><span class="sxs-lookup"><span data-stu-id="2fd2a-111"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="2fd2a-112">Ein beliebiger <a href="dx-graphics-hlsl-to-type.md">Textur Objekttyp</a> (mit Ausnahme von Texture2DMS und Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="2fd2a-112">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2fd2a-113"><span id="S"></span><span id="s"></span><em>Hymnen</em></span><span class="sxs-lookup"><span data-stu-id="2fd2a-113"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="2fd2a-114">in Ein <a href="dx-graphics-hlsl-sampler.md">samplerzustand</a>.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-114">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="2fd2a-115">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-115">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2fd2a-116"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Hotels</em></span><span class="sxs-lookup"><span data-stu-id="2fd2a-116"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="2fd2a-117">in Die Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-117">[in] The texture coordinates.</span></span> <span data-ttu-id="2fd2a-118">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-118">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2fd2a-119">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="2fd2a-119">Texture-Object Type</span></span></th>
<th><span data-ttu-id="2fd2a-120">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="2fd2a-120">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2fd2a-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2fd2a-121">Texture1D</span></span></td>
<td><span data-ttu-id="2fd2a-122">float</span><span class="sxs-lookup"><span data-stu-id="2fd2a-122">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2fd2a-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="2fd2a-123">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="2fd2a-124">float2</span><span class="sxs-lookup"><span data-stu-id="2fd2a-124">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2fd2a-125">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="2fd2a-125">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="2fd2a-126">float3</span><span class="sxs-lookup"><span data-stu-id="2fd2a-126">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2fd2a-127">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="2fd2a-127">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="2fd2a-128">float4</span><span class="sxs-lookup"><span data-stu-id="2fd2a-128">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="2fd2a-129">Wenn das Textur Objekt ein Array ist, ist die letzte Komponente der Array Index.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-129">If the texture object is an array, the last component is the array index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fd2a-130"><span id="LOD"></span><span id="lod"></span><em>LOD</em></span><span class="sxs-lookup"><span data-stu-id="2fd2a-130"><span id="LOD"></span><span id="lod"></span><em>LOD</em></span></span></p></td>
<td><p><span data-ttu-id="2fd2a-131">in Eine Zahl, die die MipMap-Ebene angibt.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-131">[in] A number that specifies the mipmap level.</span></span> <span data-ttu-id="2fd2a-132">Wenn der Wert = 0 ist, wird die NULL-Werte (größte Karte) verwendet.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-132">If the value is = 0, the zero'th (biggest map) is used.</span></span> <span data-ttu-id="2fd2a-133">Der Bruch Wert (falls angegeben) wird verwendet, um zwischen zwei MipMap-Ebenen zu interpolieren.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-133">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fd2a-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Kompensieren</em></span><span class="sxs-lookup"><span data-stu-id="2fd2a-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="2fd2a-135">in Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-135">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="2fd2a-136">Die Textur Offsets müssen statisch sein.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-136">The texture offsets need to be static.</span></span> <span data-ttu-id="2fd2a-137">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="2fd2a-138">Weitere Informationen finden Sie unter <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Anwenden von Texturkoordinaten Offsets</a>.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-138">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2fd2a-139">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="2fd2a-139">Texture-Object Type</span></span></th>
<th><span data-ttu-id="2fd2a-140">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="2fd2a-140">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2fd2a-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="2fd2a-141">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="2fd2a-142">INT</span><span class="sxs-lookup"><span data-stu-id="2fd2a-142">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2fd2a-143">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="2fd2a-143">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="2fd2a-144">int2</span><span class="sxs-lookup"><span data-stu-id="2fd2a-144">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2fd2a-145">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2fd2a-145">Texture3D</span></span></td>
<td><span data-ttu-id="2fd2a-146">int3</span><span class="sxs-lookup"><span data-stu-id="2fd2a-146">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2fd2a-147">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="2fd2a-147">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="2fd2a-148">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2fd2a-148">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="2fd2a-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2fd2a-149">Return Value</span></span>

<span data-ttu-id="2fd2a-150">Der Vorlagentyp der Textur, bei dem es sich um einen Vektor mit einer einzelnen oder mehreren Komponenten handeln kann.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-150">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="2fd2a-151">Das Format basiert auf dem [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)der Textur.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-151">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="2fd2a-152">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="2fd2a-152">Minimum Shader Model</span></span>

<span data-ttu-id="2fd2a-153">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2fd2a-154">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2fd2a-154">vs\_4\_0</span></span> | <span data-ttu-id="2fd2a-155">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="2fd2a-155">vs\_4\_1</span></span>  | <span data-ttu-id="2fd2a-156">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2fd2a-156">ps\_4\_0</span></span> | <span data-ttu-id="2fd2a-157">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="2fd2a-157">ps\_4\_1</span></span>  | <span data-ttu-id="2fd2a-158">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2fd2a-158">gs\_4\_0</span></span> | <span data-ttu-id="2fd2a-159">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="2fd2a-159">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="2fd2a-160">x</span><span class="sxs-lookup"><span data-stu-id="2fd2a-160">x</span></span>        | <span data-ttu-id="2fd2a-161">x</span><span class="sxs-lookup"><span data-stu-id="2fd2a-161">x</span></span>         | <span data-ttu-id="2fd2a-162">x</span><span class="sxs-lookup"><span data-stu-id="2fd2a-162">x</span></span>        | <span data-ttu-id="2fd2a-163">x</span><span class="sxs-lookup"><span data-stu-id="2fd2a-163">x</span></span>         | <span data-ttu-id="2fd2a-164">x</span><span class="sxs-lookup"><span data-stu-id="2fd2a-164">x</span></span>        | <span data-ttu-id="2fd2a-165">x</span><span class="sxs-lookup"><span data-stu-id="2fd2a-165">x</span></span>         |



 

1.  <span data-ttu-id="2fd2a-166">Texturecubearray ist im Shader-Modell 4,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-166">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="2fd2a-167">Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-167">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="2fd2a-168">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2fd2a-168">Example</span></span>

<span data-ttu-id="2fd2a-169">Dieses partielle Codebeispiel wird aus der Datei "Instancing. FX" im [Instancing10](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx)-Beispiel entnommen.</span><span class="sxs-lookup"><span data-stu-id="2fd2a-169">This partial code example is from the Instancing.fx file in the [Instancing10 Sample](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2fd2a-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2fd2a-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fd2a-171">Texture-Objekt</span><span class="sxs-lookup"><span data-stu-id="2fd2a-171">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

