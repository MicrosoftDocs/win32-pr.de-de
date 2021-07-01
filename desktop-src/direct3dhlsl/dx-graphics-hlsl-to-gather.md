---
title: Gather (DirectX HLSL-Texturobjekt)
description: Ruft die vier Stichproben (nur rote Komponente) ab, die für die bilineare Interpolation beim Sampling einer Textur verwendet werden.
ms.assetid: a394d8c2-99cc-4a38-9ac9-34afc666ebe0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4659ba19e9fa950a659969f2491533858f4658fb
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120545"
---
# <a name="gather-directx-hlsl-texture-object"></a><span data-ttu-id="712dc-103">Gather (DirectX HLSL-Texturobjekt)</span><span class="sxs-lookup"><span data-stu-id="712dc-103">Gather (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="712dc-104">Ruft die vier Stichproben (nur rote Komponente) ab, die für die bilineare Interpolation beim Sampling einer Textur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="712dc-104">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span>

<span data-ttu-id="712dc-105">&lt;Vorlagentyp &gt; 4 Object.Gather( \_ Samplerzustand S, float2 \| 3 \| 4 Location , \[ int2 Offset \] );</span><span class="sxs-lookup"><span data-stu-id="712dc-105">&lt;Template Type&gt;4 Object.Gather( sampler\_state S, float2\|3\|4 Location \[, int2 Offset\] );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="712dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="712dc-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="712dc-107">Element</span><span class="sxs-lookup"><span data-stu-id="712dc-107">Item</span></span></th>
<th><span data-ttu-id="712dc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="712dc-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="712dc-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em></span><span class="sxs-lookup"><span data-stu-id="712dc-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="712dc-110">Die folgenden <a href="dx-graphics-hlsl-to-type.md">Texturobjekttypen</a> werden unterstützt: Texture2D, Texture2DArray, TextureCube, TextureCubeArray.</span><span class="sxs-lookup"><span data-stu-id="712dc-110">The following <a href="dx-graphics-hlsl-to-type.md">texture-object</a> types are supported: Texture2D, Texture2DArray, TextureCube, TextureCubeArray.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="712dc-111"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="712dc-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="712dc-112">[in] Ein <a href="dx-graphics-hlsl-sampler.md">Samplerzustand.</a></span><span class="sxs-lookup"><span data-stu-id="712dc-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="712dc-113">Dies ist ein Objekt, das in einer Effektdatei deklariert ist, die Zustandszuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="712dc-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="712dc-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Lage</em></span><span class="sxs-lookup"><span data-stu-id="712dc-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="712dc-115">[in] Die Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="712dc-115">[in] The texture coordinates.</span></span> <span data-ttu-id="712dc-116">Der Argumenttyp ist vom Texturobjekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="712dc-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="712dc-117">Texture-Object Typ</span><span class="sxs-lookup"><span data-stu-id="712dc-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="712dc-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="712dc-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="712dc-119">Texture2D</span><span class="sxs-lookup"><span data-stu-id="712dc-119">Texture2D</span></span></td>
<td><span data-ttu-id="712dc-120">float2</span><span class="sxs-lookup"><span data-stu-id="712dc-120">float2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="712dc-121">Texture2DArray, TextureCube</span><span class="sxs-lookup"><span data-stu-id="712dc-121">Texture2DArray, TextureCube</span></span></td>
<td><span data-ttu-id="712dc-122">float3</span><span class="sxs-lookup"><span data-stu-id="712dc-122">float3</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="712dc-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="712dc-123">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="712dc-124">float4</span><span class="sxs-lookup"><span data-stu-id="712dc-124">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="712dc-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span><span class="sxs-lookup"><span data-stu-id="712dc-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="712dc-126">[in] Ein optionaler Texturkoordinatenoffset, der für jeden Texturobjekttyp verwendet werden kann. Der Offset wird vor der Stichprobenentnahme auf die Position angewendet.</span><span class="sxs-lookup"><span data-stu-id="712dc-126">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="712dc-127">Der Argumenttyp ist vom Texturobjekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="712dc-127">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="712dc-128">Bei Shadern, die auf ShaderModell 5.0 und höher abzielen, werden die 6 am wenigsten signifikanten Bits jedes Offsetwerts als Wert mit Vorsignierung verwendet, was einen Bereich von [-32...31] ergibt.</span><span class="sxs-lookup"><span data-stu-id="712dc-128">For shaders targeting Shader Model 5.0 and above, the 6 least significant bits of each offset value is honored as a signed value, yielding [-32..31] range.</span></span> <span data-ttu-id="712dc-129">Bei vorherigen Shadermodell-Shadern müssen Offsets direkte ganze Zahlen zwischen -8 und 7 sein.</span><span class="sxs-lookup"><span data-stu-id="712dc-129">For previous shader model shaders, offsets need to be immediate integers between -8 and 7.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="712dc-130">Texture-Object Typ</span><span class="sxs-lookup"><span data-stu-id="712dc-130">Texture-Object Type</span></span></th>
<th><span data-ttu-id="712dc-131">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="712dc-131">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="712dc-132">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="712dc-132">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="712dc-133">int2</span><span class="sxs-lookup"><span data-stu-id="712dc-133">int2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="712dc-134">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="712dc-134">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="712dc-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="712dc-135">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="712dc-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="712dc-136">Return Value</span></span>

<span data-ttu-id="712dc-137">Ein Vektor mit vier Komponenten mit vier Komponenten roter Daten, dessen Typ mit dem Vorlagentyp der Textur identisch ist.</span><span class="sxs-lookup"><span data-stu-id="712dc-137">A four-component vector, with four components of red data, whose type is the same as the texture's template type.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="712dc-138">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="712dc-138">Minimum Shader Model</span></span>

<span data-ttu-id="712dc-139">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="712dc-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="712dc-140">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="712dc-140">vs\_4\_0</span></span> | <span data-ttu-id="712dc-141">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="712dc-141">vs\_4\_1</span></span>  | <span data-ttu-id="712dc-142">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="712dc-142">ps\_4\_0</span></span> | <span data-ttu-id="712dc-143">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="712dc-143">ps\_4\_1</span></span>  | <span data-ttu-id="712dc-144">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="712dc-144">gs\_4\_0</span></span> | <span data-ttu-id="712dc-145">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="712dc-145">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="712dc-146">x</span><span class="sxs-lookup"><span data-stu-id="712dc-146">x</span></span>         |          | <span data-ttu-id="712dc-147">x</span><span class="sxs-lookup"><span data-stu-id="712dc-147">x</span></span>         |          | <span data-ttu-id="712dc-148">x</span><span class="sxs-lookup"><span data-stu-id="712dc-148">x</span></span>         |



 

1.  <span data-ttu-id="712dc-149">TextureCubeArray ist in Shader Model 4.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="712dc-149">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="712dc-150">ShaderModell 4.1 ist in Direct3D 10.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="712dc-150">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="712dc-151">Beispiel</span><span class="sxs-lookup"><span data-stu-id="712dc-151">Example</span></span>


```
Texture2D<int1> Tex2d;
Texture2DArray<int2> Tex2dArray;
TextureCube<int3> TexCube;
TextureCubeArray<float2> TexCubeArray;

SamplerState s;

int4 main (float4 f : SV_Position) : SV_Target
{
    int2 iOffset = int2(2,3);

    int4 i1 = Tex2d.Gather(s, f.xy);
    int4 i2 = Tex2d.Gather(s, f.xy, iOffset);

    int4 i3 = Tex2dArray.Gather(s, f.xyz);
    int4 i4 = Tex2dArray.Gather(s, f.xyz, iOffset);

    int4 i5 = TexCube.Gather(s, f.xyzw);

    float4 f6 = TexCubeArray.Gather(s, f.xyzw);

    return i1+i2+i3+i4+i5+int4(i6);
}
  
```



## <a name="related-topics"></a><span data-ttu-id="712dc-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="712dc-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="712dc-153">Texture-Object</span><span class="sxs-lookup"><span data-stu-id="712dc-153">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





