---
title: Gather (DirectX-HLSL-Textur Objekt)
description: Ruft die vier Stichproben (nur rote Komponente) ab, die bei der Stichprobenentnahme einer Textur für die bilineare interpolung verwendet werden.
ms.assetid: a394d8c2-99cc-4a38-9ac9-34afc666ebe0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16c568afc3cfdc0d26472d50599abdf3dbd08301
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "104976928"
---
# <a name="gather-directx-hlsl-texture-object"></a><span data-ttu-id="555e5-103">Gather (DirectX-HLSL-Textur Objekt)</span><span class="sxs-lookup"><span data-stu-id="555e5-103">Gather (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="555e5-104">Ruft die vier Stichproben (nur rote Komponente) ab, die bei der Stichprobenentnahme einer Textur für die bilineare interpolung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="555e5-104">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span>



|                                                                                                    |
|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="555e5-105">&lt;Template Type &gt; 4 Object. Gather (Sampler \_ State S, float2 \| 3 \| 4 Location \[ , int2 Offset \] );</span><span class="sxs-lookup"><span data-stu-id="555e5-105">&lt;Template Type&gt;4 Object.Gather( sampler\_state S, float2\|3\|4 Location \[, int2 Offset\] );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="555e5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="555e5-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="555e5-107">Element</span><span class="sxs-lookup"><span data-stu-id="555e5-107">Item</span></span></th>
<th><span data-ttu-id="555e5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="555e5-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="555e5-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em></span><span class="sxs-lookup"><span data-stu-id="555e5-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="555e5-110">Die folgenden <a href="dx-graphics-hlsl-to-type.md">Textur Objekt</a> Typen werden unterstützt: Texture2D, Texture2DArray, texturecube, texturecubearray.</span><span class="sxs-lookup"><span data-stu-id="555e5-110">The following <a href="dx-graphics-hlsl-to-type.md">texture-object</a> types are supported: Texture2D, Texture2DArray, TextureCube, TextureCubeArray.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="555e5-111"><span id="S"></span><span id="s"></span><em>Hymnen</em></span><span class="sxs-lookup"><span data-stu-id="555e5-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="555e5-112">in Ein <a href="dx-graphics-hlsl-sampler.md">samplerzustand</a>.</span><span class="sxs-lookup"><span data-stu-id="555e5-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="555e5-113">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="555e5-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="555e5-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Hotels</em></span><span class="sxs-lookup"><span data-stu-id="555e5-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="555e5-115">in Die Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="555e5-115">[in] The texture coordinates.</span></span> <span data-ttu-id="555e5-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="555e5-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="555e5-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="555e5-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="555e5-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="555e5-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="555e5-119">Texture2D</span><span class="sxs-lookup"><span data-stu-id="555e5-119">Texture2D</span></span></td>
<td><span data-ttu-id="555e5-120">float2</span><span class="sxs-lookup"><span data-stu-id="555e5-120">float2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="555e5-121">Texture2DArray, texturecube</span><span class="sxs-lookup"><span data-stu-id="555e5-121">Texture2DArray, TextureCube</span></span></td>
<td><span data-ttu-id="555e5-122">float3</span><span class="sxs-lookup"><span data-stu-id="555e5-122">float3</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="555e5-123">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="555e5-123">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="555e5-124">float4</span><span class="sxs-lookup"><span data-stu-id="555e5-124">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="555e5-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Kompensieren</em></span><span class="sxs-lookup"><span data-stu-id="555e5-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="555e5-126">in Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="555e5-126">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="555e5-127">Die Textur Offsets müssen statisch sein.</span><span class="sxs-lookup"><span data-stu-id="555e5-127">The texture offsets need to be static.</span></span> <span data-ttu-id="555e5-128">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="555e5-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="555e5-129">Weitere Informationen finden Sie unter <a href="dx-graphics-hlsl-to-sample.md">Anwenden von Texturkoordinaten Offsets</a>.</span><span class="sxs-lookup"><span data-stu-id="555e5-129">For more info, see <a href="dx-graphics-hlsl-to-sample.md">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="555e5-130">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="555e5-130">Texture-Object Type</span></span></th>
<th><span data-ttu-id="555e5-131">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="555e5-131">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="555e5-132">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="555e5-132">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="555e5-133">int2</span><span class="sxs-lookup"><span data-stu-id="555e5-133">int2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="555e5-134">Texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="555e5-134">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="555e5-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="555e5-135">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="555e5-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="555e5-136">Return Value</span></span>

<span data-ttu-id="555e5-137">Ein Vektor mit vier Komponenten mit vier Komponenten von roten Daten, deren Typ mit dem Vorlagentyp der Textur identisch ist.</span><span class="sxs-lookup"><span data-stu-id="555e5-137">A four-component vector, with four components of red data, whose type is the same as the texture's template type.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="555e5-138">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="555e5-138">Minimum Shader Model</span></span>

<span data-ttu-id="555e5-139">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="555e5-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="555e5-140">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="555e5-140">vs\_4\_0</span></span> | <span data-ttu-id="555e5-141">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="555e5-141">vs\_4\_1</span></span>  | <span data-ttu-id="555e5-142">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="555e5-142">ps\_4\_0</span></span> | <span data-ttu-id="555e5-143">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="555e5-143">ps\_4\_1</span></span>  | <span data-ttu-id="555e5-144">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="555e5-144">gs\_4\_0</span></span> | <span data-ttu-id="555e5-145">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="555e5-145">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="555e5-146">x</span><span class="sxs-lookup"><span data-stu-id="555e5-146">x</span></span>         |          | <span data-ttu-id="555e5-147">x</span><span class="sxs-lookup"><span data-stu-id="555e5-147">x</span></span>         |          | <span data-ttu-id="555e5-148">x</span><span class="sxs-lookup"><span data-stu-id="555e5-148">x</span></span>         |



 

1.  <span data-ttu-id="555e5-149">Texturecubearray ist im Shader-Modell 4,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="555e5-149">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="555e5-150">Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="555e5-150">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="555e5-151">Beispiel</span><span class="sxs-lookup"><span data-stu-id="555e5-151">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="555e5-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="555e5-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="555e5-153">Texture-Objekt</span><span class="sxs-lookup"><span data-stu-id="555e5-153">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





