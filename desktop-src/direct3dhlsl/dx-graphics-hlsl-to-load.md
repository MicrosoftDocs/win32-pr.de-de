---
title: Load (DirectX-HLSL-Textur Objekt)
description: Liest textandaten ohne Filterung oder Stichprobenentnahme.
ms.assetid: a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 08d3964788a238492ff7d5189544603b35808465
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "104123319"
---
# <a name="load-directx-hlsl-texture-object"></a><span data-ttu-id="2caa4-103">Load (DirectX-HLSL-Textur Objekt)</span><span class="sxs-lookup"><span data-stu-id="2caa4-103">Load (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="2caa4-104">Liest textandaten ohne Filterung oder Stichprobenentnahme.</span><span class="sxs-lookup"><span data-stu-id="2caa4-104">Reads texel data without any filtering or sampling.</span></span>



<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2caa4-105">Ret Object. Load (</span><span class="sxs-lookup"><span data-stu-id="2caa4-105">ret Object.Load(</span></span><dl> <span data-ttu-id="2caa4-106">TypeX-Speicherort,</span><span class="sxs-lookup"><span data-stu-id="2caa4-106">typeX Location,</span></span><br />
<span data-ttu-id="2caa4-107">[TypeX sampleingedex,]</span><span class="sxs-lookup"><span data-stu-id="2caa4-107">[typeX SampleIndex, ]</span></span><br />
<span data-ttu-id="2caa4-108">[TypeX-Offset]</span><span class="sxs-lookup"><span data-stu-id="2caa4-108">[typeX Offset ]</span></span><br />
</dl><span data-ttu-id="2caa4-109">);</span><span class="sxs-lookup"><span data-stu-id="2caa4-109">);</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2caa4-110">TypeX gibt an, dass vier mögliche Typen vorhanden sind: **int**, **int2**, **int3** oder **INT4**.</span><span class="sxs-lookup"><span data-stu-id="2caa4-110">typeX denotes that there are four possible types: **int**, **int2**, **int3** or **int4**.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="2caa4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2caa4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2caa4-112"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objekt*</span><span class="sxs-lookup"><span data-stu-id="2caa4-112"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span>
</dt> <dd>

<span data-ttu-id="2caa4-113">Ein [Textur Objekttyp](dx-graphics-hlsl-to-type.md) (außer texturecube oder texturecubearray).</span><span class="sxs-lookup"><span data-stu-id="2caa4-113">A [texture-object](dx-graphics-hlsl-to-type.md) type (except TextureCube or TextureCubeArray).</span></span>

</dd> <dt>

<span data-ttu-id="2caa4-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Hotels*</span><span class="sxs-lookup"><span data-stu-id="2caa4-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Location*</span></span>
</dt> <dd>

<span data-ttu-id="2caa4-115">\[in \] den Texturkoordinaten gibt die letzte Komponente die MipMap-Ebene an.</span><span class="sxs-lookup"><span data-stu-id="2caa4-115">\[in\] The texture coordinates; the last component specifies the mipmap level.</span></span> <span data-ttu-id="2caa4-116">Diese Methode verwendet ein 0-basiertes Koordinatensystem und kein 0,0-1.0-System.</span><span class="sxs-lookup"><span data-stu-id="2caa4-116">This method uses a 0-based coordinate system and not a 0.0-1.0 UV system.</span></span> <span data-ttu-id="2caa4-117">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="2caa4-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2caa4-118">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="2caa4-118">Object Type</span></span>                                  | <span data-ttu-id="2caa4-119">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="2caa4-119">Parameter Type</span></span> |
|----------------------------------------------|----------------|
| <span data-ttu-id="2caa4-120">Buffer</span><span class="sxs-lookup"><span data-stu-id="2caa4-120">Buffer</span></span>                                       | <span data-ttu-id="2caa4-121">INT</span><span class="sxs-lookup"><span data-stu-id="2caa4-121">int</span></span>            |
| <span data-ttu-id="2caa4-122">Texture1D, Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="2caa4-122">Texture1D, Texture2DMS</span></span>                       | <span data-ttu-id="2caa4-123">int2</span><span class="sxs-lookup"><span data-stu-id="2caa4-123">int2</span></span>           |
| <span data-ttu-id="2caa4-124">Texture1DArray, Textur 2D, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="2caa4-124">Texture1DArray, Texture 2D, Texture2DMSArray</span></span> | <span data-ttu-id="2caa4-125">int3</span><span class="sxs-lookup"><span data-stu-id="2caa4-125">int3</span></span>           |
| <span data-ttu-id="2caa4-126">Texture2DArray, Texture3D</span><span class="sxs-lookup"><span data-stu-id="2caa4-126">Texture2DArray, Texture3D</span></span>                    | <span data-ttu-id="2caa4-127">int4</span><span class="sxs-lookup"><span data-stu-id="2caa4-127">int4</span></span>           |



 

<span data-ttu-id="2caa4-128">Um z. b. auf eine 2D-Textur zuzugreifen, stellen Sie UV-Koordinaten für die ersten beiden Komponenten und eine MipMap-Ebene für die dritte Komponente bereit.</span><span class="sxs-lookup"><span data-stu-id="2caa4-128">For example, to access a 2D texture, supply UV coordinates for the first two components and a mipmap level for the third component.</span></span>

> [!Note]  
> <span data-ttu-id="2caa4-129">Wenn eine oder mehrere der Koordinaten an der *Position* die u-, v-oder w-MipMap-ebenendimensionen der Textur überschreiten, gibt **Load** in allen Komponenten 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="2caa4-129">When one or more of the coordinates in *Location* exceed the u, v, or w mipmap level dimensions of the texture, **Load** returns zero in all components.</span></span> <span data-ttu-id="2caa4-130">Direct3D garantiert, dass NULL für alle Ressourcen zurückgegeben wird, auf die außerhalb der Grenzen zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="2caa4-130">Direct3D guarantees to return zero for any resource that is accessed out of bounds.</span></span>

 

</dd> <dt>

<span data-ttu-id="2caa4-131"><span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*Sample Index*</span><span class="sxs-lookup"><span data-stu-id="2caa4-131"><span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*</span></span>
</dt> <dd>

<span data-ttu-id="2caa4-132">\[in \] einem optionalen Stichproben Index.</span><span class="sxs-lookup"><span data-stu-id="2caa4-132">\[in\] An optional sampling index.</span></span>



| <span data-ttu-id="2caa4-133">Textur-Typ</span><span class="sxs-lookup"><span data-stu-id="2caa4-133">Texture Type</span></span>                                                                                                   | <span data-ttu-id="2caa4-134">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="2caa4-134">Parameter Type</span></span> |
|----------------------------------------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="2caa4-135">Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, texturecube, texturecubearray</span><span class="sxs-lookup"><span data-stu-id="2caa4-135">Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="2caa4-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2caa4-136">not supported</span></span>  |
| <span data-ttu-id="2caa4-137">Texture2DMS, Texture2DMSArray ¹</span><span class="sxs-lookup"><span data-stu-id="2caa4-137">Texture2DMS, Texture2DMSArray¹</span></span>                                                                                 | <span data-ttu-id="2caa4-138">INT</span><span class="sxs-lookup"><span data-stu-id="2caa4-138">int</span></span>            |



 

> [!Note]  
> <span data-ttu-id="2caa4-139">*Sampleindex* ist nur für Texturen mit mehreren Beispielen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2caa4-139">*SampleIndex* is only available for multi-sample textures.</span></span>

 

</dd> <dt>

<span data-ttu-id="2caa4-140"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Kompensieren*</span><span class="sxs-lookup"><span data-stu-id="2caa4-140"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*</span></span>
</dt> <dd>

<span data-ttu-id="2caa4-141">\[\]ein optionaler Offset, der vor der Stichprobenentnahme auf die Texturkoordinaten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="2caa4-141">\[in\] An optional offset applied to the texture coordinates before sampling.</span></span> <span data-ttu-id="2caa4-142">Der offsettyp ist vom Textur Objekttyp abhängig und muss statisch sein.</span><span class="sxs-lookup"><span data-stu-id="2caa4-142">The offset type is dependent on the texture-object type, and needs to be static.</span></span>



| <span data-ttu-id="2caa4-143">Textur-Typ</span><span class="sxs-lookup"><span data-stu-id="2caa4-143">Texture Type</span></span>                                             | <span data-ttu-id="2caa4-144">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="2caa4-144">Parameter Type</span></span> |
|----------------------------------------------------------|----------------|
| <span data-ttu-id="2caa4-145">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="2caa4-145">Texture1D, Texture1DArray</span></span>                                | <span data-ttu-id="2caa4-146">INT</span><span class="sxs-lookup"><span data-stu-id="2caa4-146">int</span></span>            |
| <span data-ttu-id="2caa4-147">Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="2caa4-147">Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray</span></span> | <span data-ttu-id="2caa4-148">int2</span><span class="sxs-lookup"><span data-stu-id="2caa4-148">int2</span></span>           |
| <span data-ttu-id="2caa4-149">Texture3D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="2caa4-149">Texture3D, Texture2DArray</span></span>                                | <span data-ttu-id="2caa4-150">int3</span><span class="sxs-lookup"><span data-stu-id="2caa4-150">int3</span></span>           |



 

> [!Note]  
> <span data-ttu-id="2caa4-151">Wenn Sie *Offset* mit Multi-Sample-Texturen verwenden, müssen Sie auch *sampleindex* angeben.</span><span class="sxs-lookup"><span data-stu-id="2caa4-151">If you use *Offset* with multi-sample textures, you must also specify *SampleIndex*.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2caa4-152">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2caa4-152">Return Value</span></span>

<span data-ttu-id="2caa4-153">Der Rückgabetyp entspricht dem Typ in der *Objekt* Deklaration.</span><span class="sxs-lookup"><span data-stu-id="2caa4-153">The return type matches the type in the *Object* declaration.</span></span> <span data-ttu-id="2caa4-154">Ein Texture2D-Objekt, das als "Texture2D <uint4> MyTexture;" deklariert wurde, hat beispielsweise einen Rückgabewert vom Typ " **uint4**".</span><span class="sxs-lookup"><span data-stu-id="2caa4-154">For example, a Texture2D object that was declared as "Texture2d<uint4> myTexture;" has a return value of type **uint4**.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="2caa4-155">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="2caa4-155">Minimum Shader Model</span></span>

<span data-ttu-id="2caa4-156">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2caa4-156">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2caa4-157">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2caa4-157">vs\_4\_0</span></span> | <span data-ttu-id="2caa4-158">vs \_ 4 \_ ¹</span><span class="sxs-lookup"><span data-stu-id="2caa4-158">vs\_4\_1¹</span></span> | <span data-ttu-id="2caa4-159">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2caa4-159">ps\_4\_0</span></span> | <span data-ttu-id="2caa4-160">PS \_ 4 \_ ¹</span><span class="sxs-lookup"><span data-stu-id="2caa4-160">ps\_4\_1¹</span></span> | <span data-ttu-id="2caa4-161">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2caa4-161">gs\_4\_0</span></span> | <span data-ttu-id="2caa4-162">GS \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="2caa4-162">gs\_4\_1¹</span></span> |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="2caa4-163">x</span><span class="sxs-lookup"><span data-stu-id="2caa4-163">x</span></span>        | <span data-ttu-id="2caa4-164">x</span><span class="sxs-lookup"><span data-stu-id="2caa4-164">x</span></span>         | <span data-ttu-id="2caa4-165">x</span><span class="sxs-lookup"><span data-stu-id="2caa4-165">x</span></span>        | <span data-ttu-id="2caa4-166">x</span><span class="sxs-lookup"><span data-stu-id="2caa4-166">x</span></span>         | <span data-ttu-id="2caa4-167">x</span><span class="sxs-lookup"><span data-stu-id="2caa4-167">x</span></span>        | <span data-ttu-id="2caa4-168">x</span><span class="sxs-lookup"><span data-stu-id="2caa4-168">x</span></span>         |



 

-   <span data-ttu-id="2caa4-169">Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2caa4-169">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="2caa4-170">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2caa4-170">Example</span></span>

<span data-ttu-id="2caa4-171">Dieses partielle Codebeispiel wird aus der Paint. FX-Datei im [advancedpartikel](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)-Beispiel entnommen.</span><span class="sxs-lookup"><span data-stu-id="2caa4-171">This partial code example is from the Paint.fx file in the [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).</span></span>


```
// Object Declarations
Buffer<float4> g_ParticleBuffer;

// Shader body calling the intrinsic function
float4 PSPaint(PSQuadIn input) : SV_Target
{       
    ... 
    for( int i=g_ParticleStart; i<g_NumParticles; i+=g_ParticleStep )
    {
        ... 
        // load the particle
        float4 particlePos = g_ParticleBuffer.Load( i*4 );
        float4 particleColor = g_ParticleBuffer.Load( (i*4) + 2 );
        ...     
    }
    ...
}   
```



## <a name="related-topics"></a><span data-ttu-id="2caa4-172">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2caa4-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2caa4-173">Texture-Objekt</span><span class="sxs-lookup"><span data-stu-id="2caa4-173">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 




