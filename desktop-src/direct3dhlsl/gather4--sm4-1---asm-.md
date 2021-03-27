---
title: gather4 (SM 4.1-ASM)
description: Sammelt die vier texeln, die in einem bilinearen Filter Vorgang verwendet werden, und verpackt Sie in ein einzelnes Register. | gather4 (SM 4.1-ASM)
ms.assetid: 219B25AE-CBF9-4B68-B2DB-6D8C3C5B4CEA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84387bfe027e30b338b4701ec941a9d4e1b5e242
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981560"
---
# <a name="gather4-sm41---asm"></a><span data-ttu-id="2b3e5-104">gather4 (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="2b3e5-104">gather4 (sm4.1 - asm)</span></span>

<span data-ttu-id="2b3e5-105">Sammelt die vier texeln, die in einem bilinearen Filter Vorgang verwendet werden, und verpackt Sie in ein einzelnes Register.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-105">Gathers the four texels that would be used in a bi-linear filtering operation and packs them into a single register.</span></span>



| <span data-ttu-id="2b3e5-106">gather4 \[ \_ aoffimmi (u, v) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle \] srcsampler. r</span><span class="sxs-lookup"><span data-stu-id="2b3e5-106">gather4\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\] srcSampler.r</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2b3e5-107">Element</span><span class="sxs-lookup"><span data-stu-id="2b3e5-107">Item</span></span>                                                                                                               | <span data-ttu-id="2b3e5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b3e5-108">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b3e5-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2b3e5-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="2b3e5-110">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-110">\[in\] The address of the result of the operation.</span></span><br/>                                                                                                       |
| <span data-ttu-id="2b3e5-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*</span><span class="sxs-lookup"><span data-stu-id="2b3e5-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="2b3e5-112">\[in \] enthält die Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-112">\[in\] Contains the texture coordinates.</span></span> <br/>                                                                                                                |
| <span data-ttu-id="2b3e5-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*</span><span class="sxs-lookup"><span data-stu-id="2b3e5-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="2b3e5-114">\[in \] einem Ressourcen Register.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-114">\[in\] A resource register.</span></span> <br/> <span data-ttu-id="2b3e5-115">Das Swizzle ermöglicht, dass die zurückgegebenen Werte willkürlich durchlaufen werden, bevor Sie in den *dest*-Wert geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-115">The swizzle allows the returned values to be swizzled arbitrarily before they are written to *dest*.</span></span> <br/>            |
| <span data-ttu-id="2b3e5-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*</span><span class="sxs-lookup"><span data-stu-id="2b3e5-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="2b3e5-117">\[in \] einem Samplerregister.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-117">\[in\] A sampler register.</span></span><br/> <span data-ttu-id="2b3e5-118">Dieser Parameter muss über eine. r (rot)-Swizzle verfügen, was darauf hinweist, dass der Wert des r-Kanals in das *dest*-Objekt kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-118">This parameter must have a .r (red) swizzle, which indicates that the value of the R channel is copied to *dest*.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="2b3e5-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b3e5-119">Remarks</span></span>

<span data-ttu-id="2b3e5-120">Dieser Vorgang funktioniert nur mit einzelnen Kanälen 2D-oder cubemap-Texturen.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-120">This operation only works with single channel 2D or CubeMap textures.</span></span> <span data-ttu-id="2b3e5-121">Bei 2D-Texturen werden nur die Adressierungs Modi des Samplers verwendet und die oberste Ebene jeder MIP-Pyramide verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-121">For 2D textures only the addressing modes of the sampler are used and the top level of any mip pyramid is used.</span></span>

<span data-ttu-id="2b3e5-122">Diese Anweisung verhält sich wie die [Beispiel](sample--sm4---asm-.md) Anweisung, aber ein gefiltertes Beispiel wird nicht generiert.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-122">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="2b3e5-123">Die vier Beispiele, die zum Filtern beitragen würden, werden in xyzw im Uhrzeigersinn im Uhrzeigersinn eingefügt, beginnend mit dem Beispiel in der unteren linken Ecke des abgefragten Speicher Orts.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-123">The four samples that would contribute to filtering are placed into xyzw in counter clockwise order starting with the sample to the lower left of the queried location.</span></span> <span data-ttu-id="2b3e5-124">Dies ist identisch mit der Punkt Stichprobe mit (u, v) Texturkoordinaten Deltas an den folgenden Positionen: (-, +), (+, +), (+,-), (-,-), wobei die Größe der Deltas immer eine halbe Texturgröße ist.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-124">This is the same as point sampling with (u,v) texture coordinate deltas at the following locations: (-,+),(+,+),(+,-),(-,-), where the magnitude of the deltas are always half a texel.</span></span>

<span data-ttu-id="2b3e5-125">Bei cubemap-Texturen, bei denen ein bidirektionale Speicherbedarf einen edgetext aus dem benachbarten Gesicht umfasst, werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-125">For CubeMap textures when a bi-linear footprint spans an edge texels from the neighboring face are used.</span></span> <span data-ttu-id="2b3e5-126">Für Ecken werden dieselben Regeln wie für die **Beispiel** Anweisung verwendet. Dies ist die unbekannter-Ecke, die als Durchschnitt der drei sich erziehenden Gesichts Ecken betrachtet wird.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-126">Corners use the same rules as the **sample** instruction; that is the unkown corner is considered the average of the three impinging face corners.</span></span>

<span data-ttu-id="2b3e5-127">Die auf die **Beispiel** Anweisungen geltenden Textur Format Einschränkungen gelten auch für die **gather4** -Anweisung.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-127">The texture format restrictions that apply to the **sample** instructions also apply to the **gather4** instruction.</span></span>

<span data-ttu-id="2b3e5-128">Bei Hardware Implementierungen können Optimierungen in herkömmlichen bilinearen filtern, die Beispiele direkt in texeln erkennen und das Lesen von texeln überspringen, die eine Gewichtung von 0 haben, nicht mit **gather4** genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-128">For hardware implementations, optimizations in traditional bilinear filtering that detect samples directly on texels and skip reading of texels that would have weight 0 cannot be leveraged with **gather4**.</span></span> <span data-ttu-id="2b3e5-129">**gather4** gibt immer alle angeforderten Texels zurück.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-129">**gather4** always returns all requested texels.</span></span>

<span data-ttu-id="2b3e5-130">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="2b3e5-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2b3e5-131">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="2b3e5-131">Vertex Shader</span></span> | <span data-ttu-id="2b3e5-132">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="2b3e5-132">Geometry Shader</span></span> | <span data-ttu-id="2b3e5-133">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="2b3e5-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2b3e5-134">x</span><span class="sxs-lookup"><span data-stu-id="2b3e5-134">x</span></span>             | <span data-ttu-id="2b3e5-135">x</span><span class="sxs-lookup"><span data-stu-id="2b3e5-135">x</span></span>               | <span data-ttu-id="2b3e5-136">x</span><span class="sxs-lookup"><span data-stu-id="2b3e5-136">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2b3e5-137">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="2b3e5-137">Minimum Shader Model</span></span>

<span data-ttu-id="2b3e5-138">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2b3e5-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2b3e5-139">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="2b3e5-139">Shader Model</span></span>                                              | <span data-ttu-id="2b3e5-140">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="2b3e5-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2b3e5-141">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="2b3e5-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2b3e5-142">ja</span><span class="sxs-lookup"><span data-stu-id="2b3e5-142">yes</span></span>       |
| [<span data-ttu-id="2b3e5-143">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="2b3e5-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2b3e5-144">ja</span><span class="sxs-lookup"><span data-stu-id="2b3e5-144">yes</span></span>       |
| [<span data-ttu-id="2b3e5-145">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="2b3e5-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2b3e5-146">nein</span><span class="sxs-lookup"><span data-stu-id="2b3e5-146">no</span></span>        |
| [<span data-ttu-id="2b3e5-147">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b3e5-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2b3e5-148">nein</span><span class="sxs-lookup"><span data-stu-id="2b3e5-148">no</span></span>        |
| [<span data-ttu-id="2b3e5-149">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b3e5-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2b3e5-150">nein</span><span class="sxs-lookup"><span data-stu-id="2b3e5-150">no</span></span>        |
| [<span data-ttu-id="2b3e5-151">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b3e5-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2b3e5-152">nein</span><span class="sxs-lookup"><span data-stu-id="2b3e5-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2b3e5-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2b3e5-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b3e5-154">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2b3e5-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





