---
title: Samplecmp (DirectX HLSL-Textur Objekt)
description: Vergleicht eine Textur und vergleicht eine einzelne Komponente mit dem angegebenen Vergleichswert.
ms.assetid: e21894c4-e8c5-4c3d-92c1-727964f8fd94
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6991bead4bfc42451c26fe5476b4c114626eb7e8
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "104993654"
---
# <a name="samplecmp-directx-hlsl-texture-object"></a><span data-ttu-id="db302-103">Samplecmp (DirectX HLSL-Textur Objekt)</span><span class="sxs-lookup"><span data-stu-id="db302-103">SampleCmp (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="db302-104">Vergleicht eine Textur und vergleicht eine einzelne Komponente mit dem angegebenen Vergleichswert.</span><span class="sxs-lookup"><span data-stu-id="db302-104">Samples a texture and compares a single component against the specified comparison value.</span></span>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db302-105">float-Objekt. samplecmp (</span><span class="sxs-lookup"><span data-stu-id="db302-105">float Object.SampleCmp(</span></span> <dl> <span data-ttu-id="db302-106">Samplercomparisonstate S,</span><span class="sxs-lookup"><span data-stu-id="db302-106">SamplerComparisonState S,</span></span><br />
<span data-ttu-id="db302-107">float-Speicherort</span><span class="sxs-lookup"><span data-stu-id="db302-107">float Location,</span></span><br />
<span data-ttu-id="db302-108">float-CompareValue,</span><span class="sxs-lookup"><span data-stu-id="db302-108">float CompareValue,</span></span><br />
<span data-ttu-id="db302-109">[int Offset]</span><span class="sxs-lookup"><span data-stu-id="db302-109">[int Offset]</span></span><br />
</dl><span data-ttu-id="db302-110">);</span><span class="sxs-lookup"><span data-stu-id="db302-110">);</span></span></td>
</tr>
</tbody>
</table>
 

<span data-ttu-id="db302-111">Der Vergleich ist ein Einzelkomponenten Vergleich zwischen der ersten in der Textur gespeicherten Komponente und dem in der Methode übergebenen Vergleichswert.</span><span class="sxs-lookup"><span data-stu-id="db302-111">The comparison is a single-component comparison between the first component stored in the texture, and the comparison value passed into the method.</span></span>

<span data-ttu-id="db302-112">Diese Methode kann nur von einem Pixelshader aufgerufen werden. Sie wird in einem Scheitelpunkt oder Geometry-Shader nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db302-112">This method can be invoked only from a pixel shader; it isn't supported in a vertex or geometry shader.</span></span>

## <a name="parameters"></a><span data-ttu-id="db302-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="db302-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db302-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objekt*</span><span class="sxs-lookup"><span data-stu-id="db302-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span>
</dt> <dd>

<span data-ttu-id="db302-115">Ein beliebiger [Textur Objekttyp](dx-graphics-hlsl-to-type.md) (mit Ausnahme von Texture2DMS, Texture2DMSArray oder Texture3D).</span><span class="sxs-lookup"><span data-stu-id="db302-115">Any [texture-object](dx-graphics-hlsl-to-type.md) type (except Texture2DMS, Texture2DMSArray, or Texture3D).</span></span>

</dd> <dt>

<span data-ttu-id="db302-116"><span id="S"></span><span id="s"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="db302-116"><span id="S"></span><span id="s"></span>*S*</span></span>
</dt> <dd>

<span data-ttu-id="db302-117">\[in \] einem Sampler-Vergleichs Zustand, bei dem es sich um den samplerzustand plus einen Vergleichs Zustand handelt (eine Vergleichsfunktion und ein Vergleichs Filter).</span><span class="sxs-lookup"><span data-stu-id="db302-117">\[in\] A sampler-comparison state, which is the sampler state plus a comparison state (a comparison function and a comparison filter).</span></span> <span data-ttu-id="db302-118">Weitere Informationen und ein Beispiel finden Sie unter dem [Samplingtyp](dx-graphics-hlsl-sampler.md) .</span><span class="sxs-lookup"><span data-stu-id="db302-118">See the [sampler type](dx-graphics-hlsl-sampler.md) for details and an example.</span></span>

</dd> <dt>

<span data-ttu-id="db302-119"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Hotels*</span><span class="sxs-lookup"><span data-stu-id="db302-119"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Location*</span></span>
</dt> <dd>

<span data-ttu-id="db302-120">\[in \] den Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="db302-120">\[in\] The texture coordinates.</span></span> <span data-ttu-id="db302-121">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="db302-121">The argument type is dependent on the texture-object type.</span></span>

| <span data-ttu-id="db302-122">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="db302-122">Texture-Object Type</span></span>          | <span data-ttu-id="db302-123">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="db302-123">Parameter Type</span></span> |
|------------------------------|----------------|
| <span data-ttu-id="db302-124">Texture1D</span><span class="sxs-lookup"><span data-stu-id="db302-124">Texture1D</span></span>                    | <span data-ttu-id="db302-125">float</span><span class="sxs-lookup"><span data-stu-id="db302-125">float</span></span>          |
| <span data-ttu-id="db302-126">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="db302-126">Texture1DArray, Texture2D</span></span>    | <span data-ttu-id="db302-127">float2</span><span class="sxs-lookup"><span data-stu-id="db302-127">float2</span></span>         |
| <span data-ttu-id="db302-128">Texture2DArray ¹, texturecube</span><span class="sxs-lookup"><span data-stu-id="db302-128">Texture2DArray¹, TextureCube</span></span> | <span data-ttu-id="db302-129">float3</span><span class="sxs-lookup"><span data-stu-id="db302-129">float3</span></span>         |
| <span data-ttu-id="db302-130">Texturecubearray ¹</span><span class="sxs-lookup"><span data-stu-id="db302-130">TextureCubeArray¹</span></span>            | <span data-ttu-id="db302-131">float4</span><span class="sxs-lookup"><span data-stu-id="db302-131">float4</span></span>         |

</dd> <dt>

<span data-ttu-id="db302-132"><span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*</span><span class="sxs-lookup"><span data-stu-id="db302-132"><span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*</span></span>
</dt> <dd>

<span data-ttu-id="db302-133">Ein Gleit Komma Wert, der als Vergleichswert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="db302-133">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="db302-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Kompensieren*</span><span class="sxs-lookup"><span data-stu-id="db302-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*</span></span>
</dt> <dd>

<span data-ttu-id="db302-135">\[in \] einem optionalen Text der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet.</span><span class="sxs-lookup"><span data-stu-id="db302-135">\[in\] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="db302-136">Die Textur Offsets müssen statisch sein.</span><span class="sxs-lookup"><span data-stu-id="db302-136">The texture offsets need to be static.</span></span> <span data-ttu-id="db302-137">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="db302-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="db302-138">Weitere Informationen finden Sie unter [Anwenden von Texturkoordinaten Offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="db302-138">For more info, see [Applying texture coordinate offsets](dx-graphics-hlsl-to-sample.md).</span></span>

| <span data-ttu-id="db302-139">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="db302-139">Texture-Object Type</span></span>            | <span data-ttu-id="db302-140">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="db302-140">Parameter Type</span></span> |
|--------------------------------|----------------|
| <span data-ttu-id="db302-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="db302-141">Texture1D, Texture1DArray</span></span>      | <span data-ttu-id="db302-142">INT</span><span class="sxs-lookup"><span data-stu-id="db302-142">int</span></span>            |
| <span data-ttu-id="db302-143">Texture2D, Texture2DArray ¹</span><span class="sxs-lookup"><span data-stu-id="db302-143">Texture2D, Texture2DArray¹</span></span>     | <span data-ttu-id="db302-144">int2</span><span class="sxs-lookup"><span data-stu-id="db302-144">int2</span></span>           |
| <span data-ttu-id="db302-145">Texturecube, texturecubearray ¹</span><span class="sxs-lookup"><span data-stu-id="db302-145">TextureCube, TextureCubeArray¹</span></span> | <span data-ttu-id="db302-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="db302-146">Not supported</span></span>  |

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db302-147">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db302-147">Return Value</span></span>

<span data-ttu-id="db302-148">Gibt einen Gleit Komma Wert im Bereich von \[ 0.. 1 zurück \] .</span><span class="sxs-lookup"><span data-stu-id="db302-148">Returns a floating-point value in the range \[0..1\].</span></span>

<span data-ttu-id="db302-149">Bei jedem abgerufenen Texttyp (basierend auf der samplingkonfiguration des Filter Modus) führt **samplecmp** einen Vergleich des z-Werts (3rd-Komponente der Eingabe) vom Shader mit dem textexwert aus (1, wenn der Vergleich durchlaufen wird; andernfalls 0).</span><span class="sxs-lookup"><span data-stu-id="db302-149">For each texel fetched (based on the sampler configuration of the filter mode), **SampleCmp** performs a comparison of the z value (3rd component of input) from the shader against the texel value (1 if the comparison passes; otherwise 0).</span></span> <span data-ttu-id="db302-150">**Samplecmp** kombiniert dann diese 0-und 1-Ergebnisse für alle Texttypen wie bei normaler Textur Filterung (kein Durchschnitt) und gibt den resultierenden \[ Wert 0.. 1 \] an den Shader zurück.</span><span class="sxs-lookup"><span data-stu-id="db302-150">**SampleCmp** then blends these 0 and 1 results for each texel together as in normal texture filtering (not an average) and returns the resulting \[0..1\] value to the shader.</span></span>

## <a name="remarks"></a><span data-ttu-id="db302-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db302-151">Remarks</span></span>

<span data-ttu-id="db302-152">Durch die Vergleichs Filterung wird ein grundlegender Filter Vorgang bereitstellt, der für eine genauere (prozentuale) Filterung nützlich ist.</span><span class="sxs-lookup"><span data-stu-id="db302-152">Comparison filtering provides a basic filtering operation that is useful for percentage-closer-depth filtering.</span></span>

<span data-ttu-id="db302-153">Wenn diese Methode für eine Gleit Komma Ressource verwendet wird (anstelle eines signierten oder nicht signierten normalisierten Formats), wird der Vergleichswert nicht automatisch zwischen 0,0 und 1,0 gebunden.</span><span class="sxs-lookup"><span data-stu-id="db302-153">When using this method on a floating-point resource (Instead of a signed-normalized or unsigned-normalized format), the comparison value is not automatically clamped between 0.0 and 1.0.</span></span> <span data-ttu-id="db302-154">Daher kann eine manuelle Klammer des Vergleichs Werts für gängige shadoingtechniken erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="db302-154">Therefore, a manual clamp of the comparison value may be necessary for common shadowing techniques.</span></span>

<span data-ttu-id="db302-155">Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie abhängig von der Hardware Implementierung oder den Treibereinstellungen möglicherweise unterschiedliche Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="db302-155">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="db302-156">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="db302-156">Minimum Shader Model</span></span>

<span data-ttu-id="db302-157">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db302-157">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="db302-158">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="db302-158">vs\_4\_0</span></span> | <span data-ttu-id="db302-159">vs \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="db302-159">vs\_4\_1²</span></span> | <span data-ttu-id="db302-160">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="db302-160">ps\_4\_0</span></span> | <span data-ttu-id="db302-161">PS \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="db302-161">ps\_4\_1²</span></span> | <span data-ttu-id="db302-162">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="db302-162">gs\_4\_0</span></span> | <span data-ttu-id="db302-163">GS \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="db302-163">gs\_4\_1²</span></span> |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="db302-164">x ¹</span><span class="sxs-lookup"><span data-stu-id="db302-164">x¹</span></span>       | <span data-ttu-id="db302-165">x</span><span class="sxs-lookup"><span data-stu-id="db302-165">x</span></span>         |          |           |

1.  <span data-ttu-id="db302-166">Texture2DArray und texturecubearray sind im Shader-Modell 4,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="db302-166">Texture2DArray and TextureCubeArray are available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="db302-167">Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="db302-167">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

> [!NOTE]  
> <span data-ttu-id="db302-168">**Samplecmp** ist auch in der PS 4 \_ 0 \_ \_ -Ebene 9 \_ 1 und 4 \_ 0 \_ Stufe \_ 9 3 verfügbar \_ , wenn Sie die Verfahren verwenden, die unter [Implementieren von Schatten Puffern für Direct3D Feature Level 9](/previous-versions/windows/apps/jj262110(v=win.10))beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="db302-168">**SampleCmp** is also available in ps 4\_0\_level\_9\_1 and 4\_0\_level\_9\_3 when you use the techniques that are described in [Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="db302-169">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="db302-169">Related topics</span></span>

[<span data-ttu-id="db302-170">Texture-Objekt</span><span class="sxs-lookup"><span data-stu-id="db302-170">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
