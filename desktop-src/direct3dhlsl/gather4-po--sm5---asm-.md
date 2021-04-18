---
title: gather4_po (SM5-ASM)
description: Eine Variante von gather4, aber anstelle eines unmittelbaren Offsets \-8.. 7 \, wird der Offset als Parameter für die Anweisung und auch als größerer Bereich von \-32.. 31 \ angezeigt.
ms.assetid: A77A32B4-BD4F-46E7-9999-13EAA8A26974
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9197fee97645333d37d589db36c3774852b12229
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976425"
---
# <a name="gather4_po-sm5---asm"></a><span data-ttu-id="17e21-103">gather4 \_ Po (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="17e21-103">gather4\_po (sm5 - asm)</span></span>

<span data-ttu-id="17e21-104">Eine Variante von [gather4](gather4--sm5---asm-.md), aber anstelle eines unmittelbaren Offsets \[ -8.. 7, wird \] der Offset als Parameter für die Anweisung und auch als größerer Bereich von \[ -32.. 31 angezeigt \] .</span><span class="sxs-lookup"><span data-stu-id="17e21-104">A variant of [gather4](gather4--sm5---asm-.md), but instead of supporting an immediate offset \[-8..7\], the offset comes as a parameter to the instruction, and also has larger range of \[-32..31\].</span></span>



| <span data-ttu-id="17e21-105">gather4 \_ po dest \[ . mask \] , srcaddress \[ . Swizzle \] , srcOffset \[ . Swizzle \] , srkresource \[ . Swizzle \] , srcsampler \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="17e21-105">gather4\_po dest\[.mask\], srcAddress\[.swizzle\], srcOffset\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.select\_component\]</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="17e21-106">Element</span><span class="sxs-lookup"><span data-stu-id="17e21-106">Item</span></span>                                                                                                               | <span data-ttu-id="17e21-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17e21-107">Description</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="17e21-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="17e21-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="17e21-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="17e21-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="17e21-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*</span><span class="sxs-lookup"><span data-stu-id="17e21-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="17e21-111">\[in \] einem Satz von Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="17e21-111">\[in\] A set of texture coordinates.</span></span><br/>               |
| <span data-ttu-id="17e21-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span><span class="sxs-lookup"><span data-stu-id="17e21-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span></span><br/>         | <span data-ttu-id="17e21-113">\[im \] Offset.</span><span class="sxs-lookup"><span data-stu-id="17e21-113">\[in\] The offset.</span></span><br/>                                 |
| <span data-ttu-id="17e21-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*</span><span class="sxs-lookup"><span data-stu-id="17e21-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="17e21-115">\[in \] einem Textur Register.</span><span class="sxs-lookup"><span data-stu-id="17e21-115">\[in\] A texture register.</span></span><br/>                         |
| <span data-ttu-id="17e21-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*</span><span class="sxs-lookup"><span data-stu-id="17e21-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="17e21-117">\[in \] einem Samplerregister.</span><span class="sxs-lookup"><span data-stu-id="17e21-117">\[in\] A sampler register.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="17e21-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17e21-118">Remarks</span></span>

<span data-ttu-id="17e21-119">Die ersten beiden Komponenten des offset-Parameters "4-Vector" stellen ganzzahlige Offsets von 32 Bit bereit.</span><span class="sxs-lookup"><span data-stu-id="17e21-119">The first two components of the 4-vector offset parameter supply 32-bit integer offsets.</span></span> <span data-ttu-id="17e21-120">Die anderen Komponenten dieses Parameters werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="17e21-120">The other components of this parameter are ignored.</span></span>

<span data-ttu-id="17e21-121">Die 6 geringsten Bits jedes Offset Werts werden als signierter Wert berücksichtigt, der den \[ Bereich-32.. 31 ergibt \] .</span><span class="sxs-lookup"><span data-stu-id="17e21-121">The 6 least significant bits of each offset value is honored as a signed value, yielding \[-32..31\] range.</span></span>

<span data-ttu-id="17e21-122">Diese Anweisung funktioniert nur mit 2D-Texturen, im Gegensatz zu **gather4**, die auch mit texturecubes funktioniert.</span><span class="sxs-lookup"><span data-stu-id="17e21-122">This instruction only works with 2D textures, unlike **gather4**, which also works with TextureCubes.</span></span>

<span data-ttu-id="17e21-123">Die einzigen Modi, die im Sampler berücksichtigt werden, sind die Adressierungs Modi.</span><span class="sxs-lookup"><span data-stu-id="17e21-123">The only modes honored in the sampler are the addressing modes.</span></span> <span data-ttu-id="17e21-124">Nur das ausführlichste MIP in der Ressourcen Ansicht wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="17e21-124">Only the most detailed mip in the resource view is used.</span></span>

<span data-ttu-id="17e21-125">Wenn die Adresse in ein Textem-Center fällt, bedeutet dies nicht, dass die anderen texeln mit Nullen entfernt werden können.</span><span class="sxs-lookup"><span data-stu-id="17e21-125">If the address falls on a texel center, this does not mean the other texels can be zeroed out.</span></span>

<span data-ttu-id="17e21-126">Der *srcsampler* -Parameter enthält \[ . Select- \_ Komponente \] , sodass jede einzelne Komponente einer Textur abgerufen werden kann, einschließlich der Rückgabe von Standardwerten für fehlende Komponenten.</span><span class="sxs-lookup"><span data-stu-id="17e21-126">The *srcSampler* parameter includes \[.select\_component\], allowing any single component of a texture to be retrieved, including returning defaults for missing components.</span></span>

<span data-ttu-id="17e21-127">Bei Formaten mit float32-Komponenten wird der Wert, der abgerufen wird, normalisiert, denormalisiert, +-0 oder +-INF, an den Shader unverändert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="17e21-127">For formats with float32 components, if the value being fetched is normalized, denormalized, +-0 or +-INF, it is returned to the shader unaltered.</span></span> <span data-ttu-id="17e21-128">NaN wird als NaN zurückgegeben, aber die genaue Bitdarstellung des Nan kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="17e21-128">NaN is returned as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="17e21-129">Bei texturecubes müssen einige Synthese der fehlenden 4. Textteile in Ecken vorkommen, sodass das Konzept der Rückgabe von Bits, die für die synthetische Texttyp unverändert liegen, nicht zutrifft und denorms geleert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="17e21-129">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply, and denorms could be flushed.</span></span>

<span data-ttu-id="17e21-130">Verwenden Sie diese Anweisung, um den Offset Bereich von **gather4** auf einen größeren und programmierbaren Bereich zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="17e21-130">Use this instruction to extend offset range of **gather4** to be larger and programmable.</span></span> <span data-ttu-id="17e21-131">Das Suffix "Po" im Namen bedeutet "Programmierbarer Offset".</span><span class="sxs-lookup"><span data-stu-id="17e21-131">The "po" suffix on the name means "programmable offset".</span></span>

<span data-ttu-id="17e21-132">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="17e21-132">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="17e21-133">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="17e21-133">Vertex</span></span> | <span data-ttu-id="17e21-134">Hülle</span><span class="sxs-lookup"><span data-stu-id="17e21-134">Hull</span></span> | <span data-ttu-id="17e21-135">Domain</span><span class="sxs-lookup"><span data-stu-id="17e21-135">Domain</span></span> | <span data-ttu-id="17e21-136">Geometrie</span><span class="sxs-lookup"><span data-stu-id="17e21-136">Geometry</span></span> | <span data-ttu-id="17e21-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="17e21-137">Pixel</span></span> | <span data-ttu-id="17e21-138">Compute</span><span class="sxs-lookup"><span data-stu-id="17e21-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="17e21-139">X</span><span class="sxs-lookup"><span data-stu-id="17e21-139">X</span></span>      | <span data-ttu-id="17e21-140">X</span><span class="sxs-lookup"><span data-stu-id="17e21-140">X</span></span>    | <span data-ttu-id="17e21-141">X</span><span class="sxs-lookup"><span data-stu-id="17e21-141">X</span></span>      | <span data-ttu-id="17e21-142">X</span><span class="sxs-lookup"><span data-stu-id="17e21-142">X</span></span>        | <span data-ttu-id="17e21-143">X</span><span class="sxs-lookup"><span data-stu-id="17e21-143">X</span></span>     | <span data-ttu-id="17e21-144">X</span><span class="sxs-lookup"><span data-stu-id="17e21-144">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="17e21-145">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="17e21-145">Minimum Shader Model</span></span>

<span data-ttu-id="17e21-146">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="17e21-146">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="17e21-147">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="17e21-147">Shader Model</span></span>                                              | <span data-ttu-id="17e21-148">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="17e21-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="17e21-149">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="17e21-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="17e21-150">ja</span><span class="sxs-lookup"><span data-stu-id="17e21-150">yes</span></span>       |
| [<span data-ttu-id="17e21-151">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="17e21-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="17e21-152">nein</span><span class="sxs-lookup"><span data-stu-id="17e21-152">no</span></span>        |
| [<span data-ttu-id="17e21-153">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="17e21-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="17e21-154">nein</span><span class="sxs-lookup"><span data-stu-id="17e21-154">no</span></span>        |
| [<span data-ttu-id="17e21-155">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="17e21-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="17e21-156">nein</span><span class="sxs-lookup"><span data-stu-id="17e21-156">no</span></span>        |
| [<span data-ttu-id="17e21-157">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="17e21-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="17e21-158">nein</span><span class="sxs-lookup"><span data-stu-id="17e21-158">no</span></span>        |
| [<span data-ttu-id="17e21-159">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="17e21-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="17e21-160">nein</span><span class="sxs-lookup"><span data-stu-id="17e21-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="17e21-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="17e21-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17e21-162">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="17e21-162">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





