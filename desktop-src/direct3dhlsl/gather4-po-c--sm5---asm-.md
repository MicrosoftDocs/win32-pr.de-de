---
title: gather4_po_c (SM5-ASM)
description: Verhält sich wie gather4 \_ Po, außer führt einen Vergleich von Texels aus, ähnlich wie in Beispiel \_ c.
ms.assetid: B128EEF3-3440-4F00-9792-20FB1AE075E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b07dcad08b4d117a453a3c97e461e6b9b4cab6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389571"
---
# <a name="gather4_po_c-sm5---asm"></a><span data-ttu-id="b8479-103">gather4 \_ po \_ c (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="b8479-103">gather4\_po\_c (sm5 - asm)</span></span>

<span data-ttu-id="b8479-104">Verhält sich wie [**gather4 \_ po**](gather4-po--sm5---asm-.md), außer führt einen Vergleich von Texels aus, ähnlich wie in [**Beispiel \_ c**](sample-c--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="b8479-104">Behaves the same as [**gather4\_po**](gather4-po--sm5---asm-.md), except performs comparison on texels, similar to [**sample\_c**](sample-c--sm4---asm-.md).</span></span>



| <span data-ttu-id="b8479-105">gather4 \_ po \_ c dest \[ . mask \] , srcaddress \[ . Swizzle \] , srcOffset \[ . Swizzle \] , srkresource \[ . Swizzle \] , srcsampler \[ . R \] , srkreferencevalue</span><span class="sxs-lookup"><span data-stu-id="b8479-105">gather4\_po\_c dest\[.mask\], srcAddress\[.swizzle\], srcOffset\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.R\], srcReferenceValue</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="b8479-106">Element</span><span class="sxs-lookup"><span data-stu-id="b8479-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="b8479-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8479-107">Description</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b8479-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b8479-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="b8479-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="b8479-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="b8479-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*</span><span class="sxs-lookup"><span data-stu-id="b8479-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="b8479-111">\[in \] einem Satz von Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="b8479-111">\[in\] A set of texture coordinates.</span></span><br/>               |
| <span data-ttu-id="b8479-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span><span class="sxs-lookup"><span data-stu-id="b8479-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span></span><br/>                                 | <span data-ttu-id="b8479-113">\[im \] Offset.</span><span class="sxs-lookup"><span data-stu-id="b8479-113">\[in\] The offset.</span></span><br/>                                 |
| <span data-ttu-id="b8479-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*</span><span class="sxs-lookup"><span data-stu-id="b8479-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="b8479-115">\[in \] einem Textur Register.</span><span class="sxs-lookup"><span data-stu-id="b8479-115">\[in\] A texture register.</span></span><br/>                         |
| <span data-ttu-id="b8479-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*</span><span class="sxs-lookup"><span data-stu-id="b8479-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="b8479-117">\[in \] einem Samplerregister.</span><span class="sxs-lookup"><span data-stu-id="b8479-117">\[in\] A sampler register.</span></span><br/>                         |
| <span data-ttu-id="b8479-118"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srkreferencevalue*</span><span class="sxs-lookup"><span data-stu-id="b8479-118"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="b8479-119">\[in \] einer einzelnen Komponente ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="b8479-119">\[in\] Single component selected.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="b8479-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8479-120">Remarks</span></span>

<span data-ttu-id="b8479-121">In [**Beispiel \_ c**](sample-c--sm4---asm-.md) finden Sie Informationen dazu, wie *srkreferencevalue* mit den abgerufenen textsabgerufenen verglichen wird.</span><span class="sxs-lookup"><span data-stu-id="b8479-121">See [**sample\_c**](sample-c--sm4---asm-.md) for information about how *srcReferenceValue* is compared against each fetched texel.</span></span> <span data-ttu-id="b8479-122">Im Gegensatz zum **Beispiel \_ c** gibt *gather4 \_ po \_ c* die einzelnen Vergleichsergebnisse zurück, anstatt Sie zu filtern.</span><span class="sxs-lookup"><span data-stu-id="b8479-122">Unlike **sample\_c**, *gather4\_po\_c* returns each comparison result, rather than filtering them.</span></span>

<span data-ttu-id="b8479-123">Diese Anweisung, wie z. b. **gather4 \_ po**, funktioniert nur mit 2D-Texturen.</span><span class="sxs-lookup"><span data-stu-id="b8479-123">This instruction, like **gather4\_po**, only works with 2D textures.</span></span> <span data-ttu-id="b8479-124">Dies unterscheidet sich von [**gather4 \_ c**](gather4-c--sm5---asm-.md), das auch mit texturecubes funktioniert.</span><span class="sxs-lookup"><span data-stu-id="b8479-124">This is unlike [**gather4\_c**](gather4-c--sm5---asm-.md), which also works with TextureCubes.</span></span>

<span data-ttu-id="b8479-125">Bei Formaten mit float32-Komponenten wird der Wert, der abgerufen wird, normalisiert, oder +-INF, im Vergleichs Vorgang unverändert verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8479-125">For formats with float32 components, if the value being fetched is normalized, or +-INF, it is used in the comparison operation untouched.</span></span> <span data-ttu-id="b8479-126">NaN wird in der Vergleichsoperation als NaN verwendet, aber die genaue Bitdarstellung des Nan kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b8479-126">NaN is used in the comparison operation as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="b8479-127">Denorms werden in den Vergleich auf NULL geleert.</span><span class="sxs-lookup"><span data-stu-id="b8479-127">Denorms are flushed to zero going into the comparison.</span></span> <span data-ttu-id="b8479-128">Bei texturecubes muss eine Synthese der fehlenden 4. textextteile in Ecken vorkommen, sodass das Konzept der Rückgabe von Bits, die für die synthetische Texttyp unverändert sind, nicht zutrifft.</span><span class="sxs-lookup"><span data-stu-id="b8479-128">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply.</span></span>

<span data-ttu-id="b8479-129">Die für **gather4 \_ po \_ c** unterstützten Formate sind identisch mit denen, die für **Beispiel \_ c** unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b8479-129">Formats supported for **gather4\_po\_c** are same as those supported for **sample\_c**.</span></span> <span data-ttu-id="b8479-130">Dabei handelt es sich um Einzelkomponenten Formate und somit um. R auf srcsampler, anstelle eines beliebigen flüchtigen.</span><span class="sxs-lookup"><span data-stu-id="b8479-130">These are single-component formats, thus the .R on srcSampler, rather than an arbitrary swizzle.</span></span>

<span data-ttu-id="b8479-131">**gather4 \_ po \_ c** für eine ungebundene Ressource gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="b8479-131">**gather4\_po\_c** on an unbound resource returns 0.</span></span>

<span data-ttu-id="b8479-132">Verwenden Sie diese Methode zum Filtern von schattenkarten.</span><span class="sxs-lookup"><span data-stu-id="b8479-132">Use this method for shadow map filtering.</span></span>

<span data-ttu-id="b8479-133">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="b8479-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b8479-134">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="b8479-134">Vertex</span></span> | <span data-ttu-id="b8479-135">Hülle</span><span class="sxs-lookup"><span data-stu-id="b8479-135">Hull</span></span> | <span data-ttu-id="b8479-136">Domain</span><span class="sxs-lookup"><span data-stu-id="b8479-136">Domain</span></span> | <span data-ttu-id="b8479-137">Geometrie</span><span class="sxs-lookup"><span data-stu-id="b8479-137">Geometry</span></span> | <span data-ttu-id="b8479-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="b8479-138">Pixel</span></span> | <span data-ttu-id="b8479-139">Compute</span><span class="sxs-lookup"><span data-stu-id="b8479-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b8479-140">X</span><span class="sxs-lookup"><span data-stu-id="b8479-140">X</span></span>      | <span data-ttu-id="b8479-141">X</span><span class="sxs-lookup"><span data-stu-id="b8479-141">X</span></span>    | <span data-ttu-id="b8479-142">X</span><span class="sxs-lookup"><span data-stu-id="b8479-142">X</span></span>      | <span data-ttu-id="b8479-143">X</span><span class="sxs-lookup"><span data-stu-id="b8479-143">X</span></span>        | <span data-ttu-id="b8479-144">X</span><span class="sxs-lookup"><span data-stu-id="b8479-144">X</span></span>     | <span data-ttu-id="b8479-145">X</span><span class="sxs-lookup"><span data-stu-id="b8479-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b8479-146">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="b8479-146">Minimum Shader Model</span></span>

<span data-ttu-id="b8479-147">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="b8479-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b8479-148">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="b8479-148">Shader Model</span></span>                                              | <span data-ttu-id="b8479-149">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="b8479-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b8479-150">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="b8479-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b8479-151">ja</span><span class="sxs-lookup"><span data-stu-id="b8479-151">yes</span></span>       |
| [<span data-ttu-id="b8479-152">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="b8479-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b8479-153">nein</span><span class="sxs-lookup"><span data-stu-id="b8479-153">no</span></span>        |
| [<span data-ttu-id="b8479-154">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="b8479-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b8479-155">nein</span><span class="sxs-lookup"><span data-stu-id="b8479-155">no</span></span>        |
| [<span data-ttu-id="b8479-156">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8479-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b8479-157">nein</span><span class="sxs-lookup"><span data-stu-id="b8479-157">no</span></span>        |
| [<span data-ttu-id="b8479-158">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8479-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b8479-159">nein</span><span class="sxs-lookup"><span data-stu-id="b8479-159">no</span></span>        |
| [<span data-ttu-id="b8479-160">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8479-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b8479-161">nein</span><span class="sxs-lookup"><span data-stu-id="b8479-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b8479-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b8479-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8479-163">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8479-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





