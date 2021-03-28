---
title: sample_c_lz (SM4-ASM)
description: Führt einen Vergleichs Filter aus. Diese Anweisung verhält sich wie Beispiel \_ c, mit dem Unterschied, dass Lod 0 ist und Ableitungen ignoriert werden.
ms.assetid: 5F11F091-AF2F-4293-88C7-824F11FE01E4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ec2889dd3ea4c86af51c8e36bf2e302c6ad4dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389530"
---
# <a name="sample_c_lz-sm4---asm"></a><span data-ttu-id="1a098-104">Beispiel \_ c \_ LZ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1a098-104">sample\_c\_lz (sm4 - asm)</span></span>

<span data-ttu-id="1a098-105">Führt einen Vergleichs Filter aus.</span><span class="sxs-lookup"><span data-stu-id="1a098-105">Performs a comparison filter.</span></span> <span data-ttu-id="1a098-106">Diese Anweisung verhält sich wie [Beispiel \_ c](sample-c--sm4---asm-.md), mit dem Unterschied, dass Lod 0 ist und Ableitungen ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="1a098-106">This instruction behaves like [sample\_c](sample-c--sm4---asm-.md), except LOD is 0, and derivatives are ignored.</span></span>



| <span data-ttu-id="1a098-107">Beispiel \_ c \_ LZ \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource. r,//muss lauten. r Swizzle srcsampler, srkreferencevalue//Single Component Selected</span><span class="sxs-lookup"><span data-stu-id="1a098-107">sample\_c\_lz\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource.r, // must be .r swizzle srcSampler, srcReferenceValue // single component selected</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="1a098-108">Element</span><span class="sxs-lookup"><span data-stu-id="1a098-108">Item</span></span>                                                                                                                                       | <span data-ttu-id="1a098-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a098-109">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a098-110"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1a098-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="1a098-111">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="1a098-111">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="1a098-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*</span><span class="sxs-lookup"><span data-stu-id="1a098-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="1a098-113">\[in \] einem Satz von Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="1a098-113">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="1a098-114">Weitere Informationen finden Sie in der [Beispiel](sample--sm4---asm-.md) Anweisung.</span><span class="sxs-lookup"><span data-stu-id="1a098-114">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="1a098-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*</span><span class="sxs-lookup"><span data-stu-id="1a098-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="1a098-116">\[in \] einem Textur Register.</span><span class="sxs-lookup"><span data-stu-id="1a098-116">\[in\] A texture register.</span></span> <span data-ttu-id="1a098-117">Weitere Informationen finden Sie in der **Beispiel** Anweisung.</span><span class="sxs-lookup"><span data-stu-id="1a098-117">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="1a098-118"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*</span><span class="sxs-lookup"><span data-stu-id="1a098-118"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="1a098-119">\[in \] einem Samplerregister.</span><span class="sxs-lookup"><span data-stu-id="1a098-119">\[in\] A sampler register.</span></span> <span data-ttu-id="1a098-120">Weitere Informationen finden Sie in der **Beispiel** Anweisung.</span><span class="sxs-lookup"><span data-stu-id="1a098-120">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="1a098-121"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srkreferencevalue*</span><span class="sxs-lookup"><span data-stu-id="1a098-121"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="1a098-122">\[in \] einem Register, bei dem eine einzelne Komponente ausgewählt ist, die im Vergleich verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1a098-122">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="1a098-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a098-123">Remarks</span></span>

<span data-ttu-id="1a098-124">Die "LZ" steht für die Ebene 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1a098-124">The "lz" stands for level-zero.</span></span> <span data-ttu-id="1a098-125">Da Ableitungen ignoriert werden, ist diese Anweisung in anderen Shadern als dem Pixelshader verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1a098-125">Because derivatives are ignored, this instruction is available in shaders other than the Pixel Shader.</span></span>

<span data-ttu-id="1a098-126">Wenn diese Anweisung mit einer Mipmapping-Textur verwendet wird, wird Lod 0 als Stichprobe verwendet, es sei denn, der Sampler verfügt über eine Lod-Klammer, bei der die Lod an anderer Stelle platziert wird</span><span class="sxs-lookup"><span data-stu-id="1a098-126">If this instruction is used with a mipmapped texture, LOD 0 gets sampled, unless the sampler has an LOD clamp which places the LOD somewhere else, or if there is an LOD Bias, which would simply bias starting from 0.</span></span> <span data-ttu-id="1a098-127">Da Ableitungen ignoriert werden, verhält sich die anisotrope Filterung als isotrope Filter.</span><span class="sxs-lookup"><span data-stu-id="1a098-127">Because derivatives are ignored, anisotropic filtering behaves as isotropic filtering.</span></span>

<span data-ttu-id="1a098-128">In Pixel-Shadern kann diese Anweisung in einer unterschiedlichen Fluss Steuerung verwendet werden, wenn die Texturkoordinaten im Shader abgeleitet sind, im Gegensatz zum **Beispiel \_ c**.</span><span class="sxs-lookup"><span data-stu-id="1a098-128">In Pixel Shaders, this instruction can be used inside varying flow control when the texture coordinates are derived in the shader, unlike **sample\_c**.</span></span>

<span data-ttu-id="1a098-129">Wenn Sie aus einem Eingabe Slot abrufen, an das nichts gebunden ist, wird 0 für alle Komponenten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1a098-129">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="1a098-130">Diese Anweisung ist aus Gründen der Konsistenz in allen Shadern, nicht nur dem Pixelshader, verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1a098-130">This instruction is available in all shaders, not just the Pixel Shader, for consistency.</span></span>



| <span data-ttu-id="1a098-131">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="1a098-131">Vertex Shader</span></span> | <span data-ttu-id="1a098-132">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="1a098-132">Geometry Shader</span></span> | <span data-ttu-id="1a098-133">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="1a098-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1a098-134">X</span><span class="sxs-lookup"><span data-stu-id="1a098-134">X</span></span>             | <span data-ttu-id="1a098-135">X</span><span class="sxs-lookup"><span data-stu-id="1a098-135">X</span></span>               | <span data-ttu-id="1a098-136">w</span><span class="sxs-lookup"><span data-stu-id="1a098-136">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1a098-137">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="1a098-137">Minimum Shader Model</span></span>

<span data-ttu-id="1a098-138">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1a098-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1a098-139">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="1a098-139">Shader Model</span></span>                                              | <span data-ttu-id="1a098-140">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="1a098-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1a098-141">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="1a098-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1a098-142">ja</span><span class="sxs-lookup"><span data-stu-id="1a098-142">yes</span></span>       |
| [<span data-ttu-id="1a098-143">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="1a098-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1a098-144">ja</span><span class="sxs-lookup"><span data-stu-id="1a098-144">yes</span></span>       |
| [<span data-ttu-id="1a098-145">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="1a098-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1a098-146">ja</span><span class="sxs-lookup"><span data-stu-id="1a098-146">yes</span></span>       |
| [<span data-ttu-id="1a098-147">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a098-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1a098-148">nein</span><span class="sxs-lookup"><span data-stu-id="1a098-148">no</span></span>        |
| [<span data-ttu-id="1a098-149">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a098-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1a098-150">nein</span><span class="sxs-lookup"><span data-stu-id="1a098-150">no</span></span>        |
| [<span data-ttu-id="1a098-151">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a098-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1a098-152">nein</span><span class="sxs-lookup"><span data-stu-id="1a098-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1a098-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1a098-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a098-154">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a098-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





