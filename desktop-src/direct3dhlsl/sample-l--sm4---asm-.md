---
title: sample_l (SM4-ASM)
description: Stichproben von Daten aus dem angegebenen Element/der Textur mithilfe der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filter Modus. | sample_l (SM4-ASM)
ms.assetid: D285F63E-1026-45F1-9959-6F5AB2A27C95
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5acd83d81e4648cc9eae5f8e0166013dcca512a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353359"
---
# <a name="sample_l-sm4---asm"></a><span data-ttu-id="380c6-104">Sample \_ l (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="380c6-104">sample\_l (sm4 - asm)</span></span>

<span data-ttu-id="380c6-105">Stichproben von Daten aus dem angegebenen Element/der Textur mithilfe der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filter Modus.</span><span class="sxs-lookup"><span data-stu-id="380c6-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="380c6-106">Sample \_ l \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle \] , srcsampler, srclod. Select \_ Component</span><span class="sxs-lookup"><span data-stu-id="380c6-106">sample\_l\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcLOD.select\_component</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="380c6-107">Element</span><span class="sxs-lookup"><span data-stu-id="380c6-107">Item</span></span>                                                                                                               | <span data-ttu-id="380c6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="380c6-108">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="380c6-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="380c6-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="380c6-110">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="380c6-110">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="380c6-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*</span><span class="sxs-lookup"><span data-stu-id="380c6-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="380c6-112">\[in \] einem Satz von Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="380c6-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="380c6-113">Weitere Informationen finden Sie in der [Beispiel](sample--sm4---asm-.md) Anweisung.</span><span class="sxs-lookup"><span data-stu-id="380c6-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="380c6-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*</span><span class="sxs-lookup"><span data-stu-id="380c6-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="380c6-115">\[in \] einem Textur Register.</span><span class="sxs-lookup"><span data-stu-id="380c6-115">\[in\] A texture register.</span></span> <span data-ttu-id="380c6-116">Weitere Informationen finden Sie in der **Beispiel** Anweisung.</span><span class="sxs-lookup"><span data-stu-id="380c6-116">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="380c6-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*</span><span class="sxs-lookup"><span data-stu-id="380c6-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="380c6-118">\[in \] einem Samplerregister.</span><span class="sxs-lookup"><span data-stu-id="380c6-118">\[in\] A sampler register.</span></span> <span data-ttu-id="380c6-119">Weitere Informationen finden Sie in der **Beispiel** Anweisung.</span><span class="sxs-lookup"><span data-stu-id="380c6-119">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="380c6-120"><span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srclod*</span><span class="sxs-lookup"><span data-stu-id="380c6-120"><span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*</span></span><br/>                     | <span data-ttu-id="380c6-121">\[in \] der Lod.</span><span class="sxs-lookup"><span data-stu-id="380c6-121">\[in\] The LOD.</span></span><br/>                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="380c6-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="380c6-122">Remarks</span></span>

<span data-ttu-id="380c6-123">Diese Anweisung ist mit [Sample](sample--sm4---asm-.md)identisch, mit dem Unterschied, dass Lod direkt von der Anwendung als Skalarwert bereitgestellt wird, der keine Anisotropie darstellt.</span><span class="sxs-lookup"><span data-stu-id="380c6-123">This instruction is identical to [sample](sample--sm4---asm-.md), except that LOD is provided directly by the application as a scalar value, representing no anisotropy.</span></span> <span data-ttu-id="380c6-124">Diese Anweisung ist in allen progambaren Shader-Stufen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="380c6-124">This instruction is available in all progammable Shader stages.</span></span>

<span data-ttu-id="380c6-125">**Sample \_ l** Stichproben der Textur mithilfe von *srclod* als Lod.</span><span class="sxs-lookup"><span data-stu-id="380c6-125">**sample\_l** samples the texture using *srcLOD* to be the LOD.</span></span> <span data-ttu-id="380c6-126">Wenn der Lod-Wert <= 0 ist, wird die NULL-Werte (größte Karte) ausgewählt, wobei der Vergrößerungsfilter angewendet wird (sofern zutreffend basierend auf dem Filter Modus).</span><span class="sxs-lookup"><span data-stu-id="380c6-126">If the LOD value is <= 0, the zero'th (biggest map) is chosen, with the magnify filter applied (if applicable based on the filter mode).</span></span> <span data-ttu-id="380c6-127">Da *srclod* ein Gleit Komma Wert ist, wird der Bruchteil-Wert verwendet, um zwischen zwei MIP-Ebenen zu interpolieren, wenn der minimieren-Filter linear ist, oder bei der anisotrope Filterung.</span><span class="sxs-lookup"><span data-stu-id="380c6-127">Because *srcLOD* is a floating point value, the fractional value is used to interpolate between two mip levels, if the minify filter is LINEAR or with anisotropic filtering.</span></span>

<span data-ttu-id="380c6-128">**Beispiel \_ l** ignoriert Adress Ableitungen, sodass das Filter Verhalten rein isotrotrog ist.</span><span class="sxs-lookup"><span data-stu-id="380c6-128">**sample\_l** ignores address derivatives, so filtering behavior is purely isotropic.</span></span> <span data-ttu-id="380c6-129">Da Ableitungen ignoriert werden, verhält sich die anisotrope Filterung als isotrope Filter.</span><span class="sxs-lookup"><span data-stu-id="380c6-129">Because derivatives are ignored, anisotropic filtering behaves as isotropic filtering.</span></span>

<span data-ttu-id="380c6-130">Die samplerzustände miplodbias und Max/minmiplevel werden berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="380c6-130">Sampler states MIPLODBIAS and MAX/MINMIPLEVEL are honored.</span></span>

<span data-ttu-id="380c6-131">Bei Verwendung im Pixel-Shader impliziert **Sample \_ l** , dass die Wahl der Lod pro Pixel und keine Auswirkung aus benachbarten Pixeln ist, z. b. im gleichen 2 x 2-Stempel.</span><span class="sxs-lookup"><span data-stu-id="380c6-131">When used in the Pixel Shader, **sample\_l** implies that the choice of LOD is per-pixel, with no effect from neighboring pixels, for example in the same 2x2 stamp.</span></span>

<span data-ttu-id="380c6-132">Wenn Sie aus einem Eingabe Slot abrufen, an das nichts gebunden ist, wird 0 für alle Komponenten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="380c6-132">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="380c6-133">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="380c6-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="380c6-134">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="380c6-134">Vertex Shader</span></span> | <span data-ttu-id="380c6-135">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="380c6-135">Geometry Shader</span></span> | <span data-ttu-id="380c6-136">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="380c6-136">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="380c6-137">X</span><span class="sxs-lookup"><span data-stu-id="380c6-137">X</span></span>             | <span data-ttu-id="380c6-138">X</span><span class="sxs-lookup"><span data-stu-id="380c6-138">X</span></span>               | <span data-ttu-id="380c6-139">w</span><span class="sxs-lookup"><span data-stu-id="380c6-139">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="380c6-140">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="380c6-140">Minimum Shader Model</span></span>

<span data-ttu-id="380c6-141">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="380c6-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="380c6-142">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="380c6-142">Shader Model</span></span>                                              | <span data-ttu-id="380c6-143">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="380c6-143">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="380c6-144">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="380c6-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="380c6-145">ja</span><span class="sxs-lookup"><span data-stu-id="380c6-145">yes</span></span>       |
| [<span data-ttu-id="380c6-146">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="380c6-146">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="380c6-147">ja</span><span class="sxs-lookup"><span data-stu-id="380c6-147">yes</span></span>       |
| [<span data-ttu-id="380c6-148">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="380c6-148">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="380c6-149">ja</span><span class="sxs-lookup"><span data-stu-id="380c6-149">yes</span></span>       |
| [<span data-ttu-id="380c6-150">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="380c6-150">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="380c6-151">nein</span><span class="sxs-lookup"><span data-stu-id="380c6-151">no</span></span>        |
| [<span data-ttu-id="380c6-152">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="380c6-152">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="380c6-153">nein</span><span class="sxs-lookup"><span data-stu-id="380c6-153">no</span></span>        |
| [<span data-ttu-id="380c6-154">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="380c6-154">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="380c6-155">nein</span><span class="sxs-lookup"><span data-stu-id="380c6-155">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="380c6-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="380c6-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="380c6-157">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="380c6-157">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





