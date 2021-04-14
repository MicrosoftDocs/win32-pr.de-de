---
title: gather4_c (SM5-ASM)
description: Identisch mit gather4, mit dem Unterschied, dass diese instrumention einen Vergleich mit texeln ausführt, ähnlich wie in Beispiel \_ c.
ms.assetid: 6265151A-36CE-4D31-B7B2-233CEEBDCF87
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35414aa2cd4d9f0686ab7a5cc17b94caa960cec1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993135"
---
# <a name="gather4_c-sm5---asm"></a><span data-ttu-id="e2d81-103">gather4 \_ c (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e2d81-103">gather4\_c (sm5 - asm)</span></span>

<span data-ttu-id="e2d81-104">Identisch mit [**gather4**](gather4--sm5---asm-.md), mit dem Unterschied, dass diese instrumention einen Vergleich mit texeln ausführt, ähnlich wie in [**Beispiel \_ c**](sample-c--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="e2d81-104">Same as [**gather4**](gather4--sm5---asm-.md), except this instrution performs comparison on texels, similar to [**sample\_c**](sample-c--sm4---asm-.md).</span></span>



| <span data-ttu-id="e2d81-105">gather4 \_ c \[ \_ aoffimmi (u, v) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle \] , srcsampler \[ . R \] , srkreferencevalue</span><span class="sxs-lookup"><span data-stu-id="e2d81-105">gather4\_c\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.R\], srcReferenceValue</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="e2d81-106">Element</span><span class="sxs-lookup"><span data-stu-id="e2d81-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="e2d81-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2d81-107">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d81-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="e2d81-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="e2d81-109">\[in \] der Adresse des Vorgangs Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="e2d81-109">\[in\] The address of the result of the operation</span></span><br/>                                    |
| <span data-ttu-id="e2d81-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*</span><span class="sxs-lookup"><span data-stu-id="e2d81-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="e2d81-111">\[in \] einem Satz von Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="e2d81-111">\[in\] A set of texture coordinates.</span></span><br/>                                                 |
| <span data-ttu-id="e2d81-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*</span><span class="sxs-lookup"><span data-stu-id="e2d81-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="e2d81-113">\[in \] einem Textur Register.</span><span class="sxs-lookup"><span data-stu-id="e2d81-113">\[in\] A texture register.</span></span><br/>                                                           |
| <span data-ttu-id="e2d81-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*</span><span class="sxs-lookup"><span data-stu-id="e2d81-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="e2d81-115">\[in \] einem Samplerregister.</span><span class="sxs-lookup"><span data-stu-id="e2d81-115">\[in\] A sampler register.</span></span><br/>                                                           |
| <span data-ttu-id="e2d81-116"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srkreferencevalue*</span><span class="sxs-lookup"><span data-stu-id="e2d81-116"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="e2d81-117">\[in \] einem Register, bei dem eine einzelne Komponente ausgewählt ist, die im Vergleich verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e2d81-117">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e2d81-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2d81-118">Remarks</span></span>

<span data-ttu-id="e2d81-119">In [**Beispiel \_ c**](sample-c--sm4---asm-.md) finden Sie eine Beschreibung der Art und Weise, wie *srkreferencevalue* mit jedem abgerufenen texaus verglichen wird.</span><span class="sxs-lookup"><span data-stu-id="e2d81-119">See [**sample\_c**](sample-c--sm4---asm-.md) for a description of how *srcReferenceValue* gets compared against each fetched texel.</span></span> <span data-ttu-id="e2d81-120">Im Gegensatz zum **Beispiel \_ c** gibt **gather4 \_ c** alle Vergleichsergebnisse zurück, anstatt Sie zu filtern.</span><span class="sxs-lookup"><span data-stu-id="e2d81-120">Unlike **sample\_c**, **gather4\_c** returns each comparison result, rather than filtering them.</span></span>

<span data-ttu-id="e2d81-121">Bei texturecube-Ecken, in denen es drei echte texeln gibt und ein viertes synthetisiert werden muss, muss die Synthese nach dem Vergleichs Schritt erfolgen.</span><span class="sxs-lookup"><span data-stu-id="e2d81-121">For TextureCube corners, where there are three real texels and a fourth must be synthesized, the synthesis must occur after the comparison step.</span></span> <span data-ttu-id="e2d81-122">Dies bedeutet, dass das zurückgegebene Vergleichs Ergebnis für den textegroßen Textwert 0, 0,33, 0,66 oder 1 sein kann.</span><span class="sxs-lookup"><span data-stu-id="e2d81-122">This means the returned comparison result for the syntesized texel can be 0, 0.33 , 0.66 , or 1.</span></span> <span data-ttu-id="e2d81-123">Einige Implementierungen geben möglicherweise nur 0 oder 1 für den Textem Textem aus.</span><span class="sxs-lookup"><span data-stu-id="e2d81-123">Some implementations may only return either 0 or 1 for the synthesized texel.</span></span> <span data-ttu-id="e2d81-124">Abgesehen von dieser Auflistung möglicher Ergebnisse ist die Methode zum synthealisieren des Texel nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="e2d81-124">Aside from this listing of possible results, the method for synthesizing the texel is unspecified.</span></span>

<span data-ttu-id="e2d81-125">Bei Formaten mit float32-Komponenten wird der Wert, der abgerufen wird, normalisiert, oder +-INF, im Vergleichs Vorgang unverändert verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2d81-125">For formats with float32 components, if the value being fetched is normalized, or +-INF, it is used in the comparison operation untouched.</span></span> <span data-ttu-id="e2d81-126">NaN wird in der Vergleichsoperation als NaN verwendet, aber die genaue Bitdarstellung des Nan kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e2d81-126">NaN is used in the comparison operation as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="e2d81-127">Denorms werden in den Vergleich auf NULL geleert.</span><span class="sxs-lookup"><span data-stu-id="e2d81-127">Denorms are flushed to zero going into the comparison.</span></span> <span data-ttu-id="e2d81-128">Bei texturecubes muss eine Synthese der fehlenden 4. textextteile in Ecken vorkommen, sodass das Konzept der Rückgabe von Bits, die für die synthetische Texttyp unverändert sind, nicht zutrifft.</span><span class="sxs-lookup"><span data-stu-id="e2d81-128">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply.</span></span>

<span data-ttu-id="e2d81-129">Die für *gather4 \_ c* unterstützten Formate sind identisch mit denen, die für *Beispiel \_ c* unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e2d81-129">Formats supported for *gather4\_c* are same as those supported for *sample\_c*.</span></span> <span data-ttu-id="e2d81-130">Dabei handelt es sich um Einzelkomponenten Formate und somit um. R auf *srcsampler*, anstelle eines beliebigen flüchtigen.</span><span class="sxs-lookup"><span data-stu-id="e2d81-130">These are single-component formats, thus the .R on *srcSampler*, rather than an arbitrary swizzle.</span></span> <span data-ttu-id="e2d81-131">**gather4 \_ c** für eine ungebundene Ressource gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="e2d81-131">**gather4\_c** on an unbound resource returns 0.</span></span>

<span data-ttu-id="e2d81-132">Verwenden Sie diese Anweisung zum Filtern von benutzerdefinierten schattenkarten.</span><span class="sxs-lookup"><span data-stu-id="e2d81-132">Use this instruction for custom shadow map filtering.</span></span>

<span data-ttu-id="e2d81-133">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="e2d81-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e2d81-134">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="e2d81-134">Vertex</span></span> | <span data-ttu-id="e2d81-135">Hülle</span><span class="sxs-lookup"><span data-stu-id="e2d81-135">Hull</span></span> | <span data-ttu-id="e2d81-136">Domain</span><span class="sxs-lookup"><span data-stu-id="e2d81-136">Domain</span></span> | <span data-ttu-id="e2d81-137">Geometrie</span><span class="sxs-lookup"><span data-stu-id="e2d81-137">Geometry</span></span> | <span data-ttu-id="e2d81-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="e2d81-138">Pixel</span></span> | <span data-ttu-id="e2d81-139">Compute</span><span class="sxs-lookup"><span data-stu-id="e2d81-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e2d81-140">X</span><span class="sxs-lookup"><span data-stu-id="e2d81-140">X</span></span>      | <span data-ttu-id="e2d81-141">X</span><span class="sxs-lookup"><span data-stu-id="e2d81-141">X</span></span>    | <span data-ttu-id="e2d81-142">X</span><span class="sxs-lookup"><span data-stu-id="e2d81-142">X</span></span>      | <span data-ttu-id="e2d81-143">X</span><span class="sxs-lookup"><span data-stu-id="e2d81-143">X</span></span>        | <span data-ttu-id="e2d81-144">X</span><span class="sxs-lookup"><span data-stu-id="e2d81-144">X</span></span>     | <span data-ttu-id="e2d81-145">X</span><span class="sxs-lookup"><span data-stu-id="e2d81-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e2d81-146">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="e2d81-146">Minimum Shader Model</span></span>

<span data-ttu-id="e2d81-147">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e2d81-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e2d81-148">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="e2d81-148">Shader Model</span></span>                                              | <span data-ttu-id="e2d81-149">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="e2d81-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e2d81-150">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="e2d81-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e2d81-151">ja</span><span class="sxs-lookup"><span data-stu-id="e2d81-151">yes</span></span>       |
| [<span data-ttu-id="e2d81-152">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="e2d81-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e2d81-153">nein</span><span class="sxs-lookup"><span data-stu-id="e2d81-153">no</span></span>        |
| [<span data-ttu-id="e2d81-154">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="e2d81-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e2d81-155">nein</span><span class="sxs-lookup"><span data-stu-id="e2d81-155">no</span></span>        |
| [<span data-ttu-id="e2d81-156">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e2d81-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e2d81-157">nein</span><span class="sxs-lookup"><span data-stu-id="e2d81-157">no</span></span>        |
| [<span data-ttu-id="e2d81-158">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e2d81-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e2d81-159">nein</span><span class="sxs-lookup"><span data-stu-id="e2d81-159">no</span></span>        |
| [<span data-ttu-id="e2d81-160">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e2d81-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e2d81-161">nein</span><span class="sxs-lookup"><span data-stu-id="e2d81-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e2d81-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e2d81-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2d81-163">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e2d81-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





