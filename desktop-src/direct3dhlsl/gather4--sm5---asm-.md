---
title: gather4 (SM5-ASM)
description: Sammelt die vier texeln, die in einem bilinearen Filter Vorgang verwendet werden, und verpackt Sie in ein einzelnes Register. | gather4 (SM5-ASM)
ms.assetid: 5F93BB70-7696-48E4-BCD3-91D5D42FF63E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5657265738f12331afc7596286f02170de2a635
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219206"
---
# <a name="gather4-sm5---asm"></a><span data-ttu-id="46530-104">gather4 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="46530-104">gather4 (sm5 - asm)</span></span>

<span data-ttu-id="46530-105">Sammelt die vier texeln, die in einem bilinearen Filter Vorgang verwendet werden, und verpackt Sie in ein einzelnes Register.</span><span class="sxs-lookup"><span data-stu-id="46530-105">Gathers the four texels that would be used in a bi-linear filtering operation and packs them into a single register.</span></span> <span data-ttu-id="46530-106">Diese Anweisung funktioniert nur mit 2D-oder cubemap-Texturen, einschließlich Arrays.</span><span class="sxs-lookup"><span data-stu-id="46530-106">This instruction only works with 2D or CubeMap textures, including arrays.</span></span> <span data-ttu-id="46530-107">Es werden nur die Adressierungs Modi des Samplers verwendet, und die oberste Ebene jeder MIP-Pyramide wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="46530-107">Only the addressing modes of the sampler are used and the top level of any mip pyramid is used.</span></span>



| <span data-ttu-id="46530-108">gather4 \[ \_ aoffimmi (u, v) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle \] , srcsampler \[ . Select- \_ Komponente\]</span><span class="sxs-lookup"><span data-stu-id="46530-108">gather4\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.select\_component\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="46530-109">Element</span><span class="sxs-lookup"><span data-stu-id="46530-109">Item</span></span>                                                                                                               | <span data-ttu-id="46530-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46530-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="46530-111"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="46530-111"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="46530-112">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="46530-112">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="46530-113"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*</span><span class="sxs-lookup"><span data-stu-id="46530-113"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="46530-114">\[in \] einem Satz von Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="46530-114">\[in\] A set of texture coordinates.</span></span><br/>                |
| <span data-ttu-id="46530-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*</span><span class="sxs-lookup"><span data-stu-id="46530-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="46530-116">\[in \] einem Textur Register.</span><span class="sxs-lookup"><span data-stu-id="46530-116">\[in\] A texture register.</span></span><br/>                          |
| <span data-ttu-id="46530-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*</span><span class="sxs-lookup"><span data-stu-id="46530-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="46530-118">\[in \] einem Samplerregister.</span><span class="sxs-lookup"><span data-stu-id="46530-118">\[in\] A sampler register.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="46530-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46530-119">Remarks</span></span>

<span data-ttu-id="46530-120">Diese Anweisung verhält sich wie die [**Beispiel**](sample--sm4---asm-.md) Anweisung, aber ein gefiltertes Beispiel wird nicht generiert.</span><span class="sxs-lookup"><span data-stu-id="46530-120">This instruction behaves like the [**sample**](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="46530-121">Die vier Beispiele, die zum Filtern beitragen würden, werden in xyzw im Uhrzeigersinn im Uhrzeigersinn eingefügt, beginnend mit dem Beispiel in der unteren linken Ecke des abgefragten Speicher Orts.</span><span class="sxs-lookup"><span data-stu-id="46530-121">The four samples that would contribute to filtering are placed into xyzw in counter clockwise order starting with the sample to the lower left of the queried location.</span></span> <span data-ttu-id="46530-122">Dies ist identisch mit der Punkt Stichprobe mit (u, v) Texturkoordinaten Deltas an den folgenden Positionen: (-, +), (+, +), (+,-), (-,-), wobei die Größe der Deltas immer eine halbe Texturgröße ist.</span><span class="sxs-lookup"><span data-stu-id="46530-122">This is the same as point sampling with (u,v) texture coordinate deltas at the following locations: (-,+),(+,+),(+,-),(-,-), where the magnitude of the deltas are always half a texel.</span></span>

<span data-ttu-id="46530-123">Bei cubemap-Texturen werden texeln aus dem benachbarten Gesicht verwendet, wenn ein bidirektionale Speicherbedarf einen Rand umfasst.</span><span class="sxs-lookup"><span data-stu-id="46530-123">For CubeMap textures, when a bi-linear footprint spans an edge, texels from the neighboring face are used.</span></span> <span data-ttu-id="46530-124">Für Ecken werden dieselben Regeln wie für die [**Beispiel**](sample--sm4---asm-.md) Anweisung verwendet. Das heißt, die unbekannte Ecke wird als Durchschnitt der drei sich Zieh enden Gesichts Ecken betrachtet.</span><span class="sxs-lookup"><span data-stu-id="46530-124">Corners use the same rules as the [**sample**](sample--sm4---asm-.md) instruction; that is, the unknown corner is considered the average of the three impinging face corners.</span></span>

<span data-ttu-id="46530-125">Es gibt Textur Format Einschränkungen, die für **gather4** gelten, die in der Format Liste ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="46530-125">There are texture format restrictions that apply to **gather4** which are expressed in the format list.</span></span>

<span data-ttu-id="46530-126">Das Swizzle in *srkresource* ermöglicht es, dass die zurückgegebenen Werte willkürlich durchlaufen werden, bevor Sie in das Ziel geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="46530-126">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="46530-127">Die. Select- \_ Komponente in *srcsampler* wählt die Komponente der Quell Textur (r/g/b/a) aus, von der 4 texeln gelesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="46530-127">The .select\_component on *srcSampler* chooses which component of the source texture (r/g/b/a) to read 4 texels from.</span></span>

<span data-ttu-id="46530-128">Bei Formaten mit float32-Komponenten wird der Wert, der abgerufen wird, normalisiert, denormalisiert, +-0 oder +-INF, an den Shader unverändert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="46530-128">For formats with float32 components, if the value being fetched is normalized, denormalized, +-0 or +-INF, it is returned to the shader unaltered.</span></span> <span data-ttu-id="46530-129">NaN wird als NaN zurückgegeben, aber die genaue Bitdarstellung des Nan kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="46530-129">NaN is returned as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="46530-130">Bei texturecubes müssen einige Synthese der fehlenden 4. Textteile in Ecken vorkommen, sodass das Zurückgeben von Bits, die für die synthetische Texttyp unverändert bleiben, nicht zutrifft und denorms geleert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="46530-130">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so returning bits unchanged for the synthesized texel does not apply, and denorms could be flushed.</span></span>

<span data-ttu-id="46530-131">Bei Hardware Implementierungen können Optimierungen in herkömmlichen bilinearen filtern, die Beispiele direkt in texeln erkennen und das Lesen von texeln überspringen, die eine Gewichtung von 0 haben, nicht mit dieser Anweisung genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="46530-131">For hardware implementations, optimizations in traditional bilinear filtering that detect samples directly on texels and skip reading of texels that would have weight 0 cannot be leveraged with this instruction.</span></span> <span data-ttu-id="46530-132">*gather4* gibt immer alle angeforderten Texels zurück.</span><span class="sxs-lookup"><span data-stu-id="46530-132">*gather4* always returns all requested texels.</span></span>

<span data-ttu-id="46530-133">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="46530-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="46530-134">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="46530-134">Vertex</span></span> | <span data-ttu-id="46530-135">Hülle</span><span class="sxs-lookup"><span data-stu-id="46530-135">Hull</span></span> | <span data-ttu-id="46530-136">Domain</span><span class="sxs-lookup"><span data-stu-id="46530-136">Domain</span></span> | <span data-ttu-id="46530-137">Geometrie</span><span class="sxs-lookup"><span data-stu-id="46530-137">Geometry</span></span> | <span data-ttu-id="46530-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="46530-138">Pixel</span></span> | <span data-ttu-id="46530-139">Compute</span><span class="sxs-lookup"><span data-stu-id="46530-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="46530-140">X</span><span class="sxs-lookup"><span data-stu-id="46530-140">X</span></span>      | <span data-ttu-id="46530-141">X</span><span class="sxs-lookup"><span data-stu-id="46530-141">X</span></span>    | <span data-ttu-id="46530-142">X</span><span class="sxs-lookup"><span data-stu-id="46530-142">X</span></span>      | <span data-ttu-id="46530-143">X</span><span class="sxs-lookup"><span data-stu-id="46530-143">X</span></span>        | <span data-ttu-id="46530-144">X</span><span class="sxs-lookup"><span data-stu-id="46530-144">X</span></span>     | <span data-ttu-id="46530-145">X</span><span class="sxs-lookup"><span data-stu-id="46530-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="46530-146">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="46530-146">Minimum Shader Model</span></span>

<span data-ttu-id="46530-147">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="46530-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="46530-148">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="46530-148">Shader Model</span></span>                                              | <span data-ttu-id="46530-149">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="46530-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="46530-150">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="46530-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="46530-151">ja</span><span class="sxs-lookup"><span data-stu-id="46530-151">yes</span></span>       |
| [<span data-ttu-id="46530-152">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="46530-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="46530-153">nein</span><span class="sxs-lookup"><span data-stu-id="46530-153">no</span></span>        |
| [<span data-ttu-id="46530-154">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="46530-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="46530-155">nein</span><span class="sxs-lookup"><span data-stu-id="46530-155">no</span></span>        |
| [<span data-ttu-id="46530-156">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="46530-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="46530-157">nein</span><span class="sxs-lookup"><span data-stu-id="46530-157">no</span></span>        |
| [<span data-ttu-id="46530-158">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="46530-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="46530-159">nein</span><span class="sxs-lookup"><span data-stu-id="46530-159">no</span></span>        |
| [<span data-ttu-id="46530-160">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="46530-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="46530-161">nein</span><span class="sxs-lookup"><span data-stu-id="46530-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="46530-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="46530-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46530-163">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="46530-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





