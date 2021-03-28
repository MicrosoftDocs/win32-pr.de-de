---
title: sample_c (SM4-ASM)
description: Führt einen Vergleichs Filter aus.
ms.assetid: 59786ED2-48FB-494E-A5A4-F732D63BF01B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23563fe52bbc943e8756d04085b66d156ab259d7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993023"
---
# <a name="sample_c-sm4---asm"></a><span data-ttu-id="9b519-103">Beispiel \_ c (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9b519-103">sample\_c (sm4 - asm)</span></span>

<span data-ttu-id="9b519-104">Führt einen Vergleichs Filter aus.</span><span class="sxs-lookup"><span data-stu-id="9b519-104">Performs a comparison filter.</span></span>



| <span data-ttu-id="9b519-105">Beispiel \_ c \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource. r,//muss lauten. r Swizzle srcsampler, srkreferencevalue//Single Component Selected</span><span class="sxs-lookup"><span data-stu-id="9b519-105">sample\_c\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource.r, // must be .r swizzle srcSampler, srcReferenceValue // single component selected</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="9b519-106">Element</span><span class="sxs-lookup"><span data-stu-id="9b519-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="9b519-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b519-107">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b519-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9b519-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="9b519-109">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="9b519-109">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="9b519-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*</span><span class="sxs-lookup"><span data-stu-id="9b519-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="9b519-111">\[in \] einem Satz von Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="9b519-111">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="9b519-112">Weitere Informationen finden Sie in der [Beispiel](sample--sm4---asm-.md) Anweisung.</span><span class="sxs-lookup"><span data-stu-id="9b519-112">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="9b519-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*</span><span class="sxs-lookup"><span data-stu-id="9b519-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="9b519-114">\[in \] einem Textur Register.</span><span class="sxs-lookup"><span data-stu-id="9b519-114">\[in\] A texture register.</span></span> <span data-ttu-id="9b519-115">Weitere Informationen finden Sie in der **Beispiel** Anweisung.</span><span class="sxs-lookup"><span data-stu-id="9b519-115">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="9b519-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*</span><span class="sxs-lookup"><span data-stu-id="9b519-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="9b519-117">\[in \] einem Samplerregister.</span><span class="sxs-lookup"><span data-stu-id="9b519-117">\[in\] A sampler register.</span></span> <span data-ttu-id="9b519-118">Weitere Informationen finden Sie in der **Beispiel** Anweisung.</span><span class="sxs-lookup"><span data-stu-id="9b519-118">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="9b519-119"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srkreferencevalue*</span><span class="sxs-lookup"><span data-stu-id="9b519-119"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="9b519-120">\[in \] einem Register, bei dem eine einzelne Komponente ausgewählt ist, die im Vergleich verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b519-120">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="9b519-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b519-121">Remarks</span></span>

<span data-ttu-id="9b519-122">Der Hauptzweck dieser Anweisung besteht darin, einen Baustein für die Percentage-Closer Tiefe Filterung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9b519-122">The primary purpose for this instruction is to provide a building-block for Percentage-Closer Depth filtering.</span></span> <span data-ttu-id="9b519-123">Das "c" in **Beispiel \_ c** steht für den Vergleich.</span><span class="sxs-lookup"><span data-stu-id="9b519-123">The "c" in **sample\_c** stands for Comparison.</span></span>

<span data-ttu-id="9b519-124">Die Operanden für **" \_ c** " sind identisch mit der [Beispiel](sample--sm4---asm-.md) Anweisung, mit dem Unterschied, dass es einen zusätzlichen float32-Quell Operanden (" *srkreferencevalue*") gibt, bei dem es sich um eine Registerkarte mit einer einzelnen Komponente oder einen skalaren Literalwert handeln muss.</span><span class="sxs-lookup"><span data-stu-id="9b519-124">The operands to **sample\_c** are identical to the [sample](sample--sm4---asm-.md) instruction, except that there is an additional float32 source operand, *srcReferenceValue*, which must be a register with single-component selected, or a scalar literal.</span></span>

<span data-ttu-id="9b519-125">Der *srkresource* -Parameter muss eine. r (rot)-Swizzle aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9b519-125">The *srcResource* parameter must have a .r (red) swizzle.</span></span> <span data-ttu-id="9b519-126">**Beispiel \_ c** arbeitet ausschließlich auf der roten Komponente und gibt einen einzelnen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9b519-126">**sample\_c** operates exclusively on the red component, and returns a single value.</span></span> <span data-ttu-id="9b519-127">Das. r-wischen in *srkresource* gibt an, dass das skalare Ergebnis an alle Komponenten repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="9b519-127">The .r swizzle on *srcResource* indicates that the scalar result is replicated to all components.</span></span>

<span data-ttu-id="9b519-128">Wenn ein tiefen Puffer als Eingabe Textur festgelegt wird, wird der tiefen Wert in der roten Komponente angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b519-128">When a Depth Buffer is set as an input texture, the depth value shows up in the red component.</span></span>

<span data-ttu-id="9b519-129">Wenn diese Anweisung mit einer Ressource verwendet wird, die kein Texture1D/2D/2darray/Cube/cubearray ist, werden nicht definierte Ergebnisse erzeugt.</span><span class="sxs-lookup"><span data-stu-id="9b519-129">If this instruction is used with a Resource that is not a Texture1D/2D/2DArray/Cube/CubeArray, it produces undefined results.</span></span>

<span data-ttu-id="9b519-130">Wenn diese Anweisung ausgeführt wird, verwendet die samplinghardware die comparisonfunction des aktuellen Samplers zum Vergleichen von *srkreferencevalue* mit dem Wert der roten Komponente für die Quell Ressource an jedem Filter-Tap-Speicherort (Texel), den der aktuell konfigurierte Textur Filter abdeckt, basierend auf den bereitgestellten Koordinaten in *srcaddress*.</span><span class="sxs-lookup"><span data-stu-id="9b519-130">When this instruction is executed, the sampling hardware uses the current Sampler's ComparisonFunction to compare *srcReferenceValue* against the Red component value for the source Resource at each filter "tap" location (texel) that the currently configured texture filter covers, based on the provided coordinates in *srcAddress*.</span></span>

<span data-ttu-id="9b519-131">Der Vergleich findet statt, nachdem *srkreferencevalue* mit der Genauigkeit des Textur Formats quantifisiert wurde, und zwar genau auf die gleiche Weise, wie z in der Tiefe der Puffer Genauigkeit quantifisiert wird, bevor der tiefen Vergleich beim Ergebnis der Ausgabe Zusammenführung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="9b519-131">The comparison occurs after *srcReferenceValue* has been quantized to the precision of the texture format, in exactly the same way that z is quantized to depth buffer precision before Depth Comparison at the Output Merger visibility test.</span></span> <span data-ttu-id="9b519-132">Dies schließt eine Klammer für den Formatbereich ein (z. b. \[ 0.. 1 \] für ein unorm-Format).</span><span class="sxs-lookup"><span data-stu-id="9b519-132">This includes a clamp to the format range (e.g. \[0..1\] for a UNORM format).</span></span>

<span data-ttu-id="9b519-133">Die rote Komponente des Quell texgs wird mit dem quantifizierten *srroferencevalue* verglichen.</span><span class="sxs-lookup"><span data-stu-id="9b519-133">The source texel's Red component is compared against the quantized *srcReferenceValue*.</span></span> <span data-ttu-id="9b519-134">Bei texeln, die auf die Ressource zurückgreifen, wird der Wert der roten Komponente durch Anwenden der Adress Modi (und bordercolorr, wenn im Rahmen Modus) vom Sampler festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9b519-134">For texels that fall off the Resource, the Red component value is determined by applying the Address Modes (and BorderColorR if in Border mode) from the Sampler.</span></span> <span data-ttu-id="9b519-135">Beim Vergleich werden alle D3D11-Gleit Komma Vergleichs Regeln berücksichtigt, wenn das Textur Format Gleit Komma Wert ist.</span><span class="sxs-lookup"><span data-stu-id="9b519-135">The comparison honors all D3D11 floating point comparison rules, in the case the texture format is floating point.</span></span>

<span data-ttu-id="9b519-136">Jeder übergebenen Vergleich gibt 1.0 f als den roten Komponenten Wert für den Texttyp zurück, und jeder fehlgeschlagene Vergleich gibt 0,0 f als den roten Wert für die Textur zurück.</span><span class="sxs-lookup"><span data-stu-id="9b519-136">Each comparison that passes returns 1.0f as the Red component value for the texel, and each comparison that fails returns 0.0f as the Red value for the texture.</span></span> <span data-ttu-id="9b519-137">Das Filtern erfolgt dann genau wie in den samplerzuständen angegeben, nur in der roten Komponente betrieben, und es wird ein einzelnes skalarfiltergebnis zurück an den Shader zurückgegeben, das auf *alle maskierten* Endkomponenten repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="9b519-137">Filtering then occurs exactly as specified by the Sampler states, operating only in the Red component, and returning a single scalar filter result back to the Shader, replicated to all masked *dest* components.</span></span>

<span data-ttu-id="9b519-138">Die Verwendung von **Beispiel \_ c** ist orthogonal zu allen anderen allgemeinen Filterungs Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="9b519-138">The use of **sample\_c** is orthogonal to all other general purpose filtering controls.</span></span> <span data-ttu-id="9b519-139">**Beispiel \_ c** funktioniert nahtlos mit den anderen allgemeinen Filtermodi.</span><span class="sxs-lookup"><span data-stu-id="9b519-139">**sample\_c** works seamlessly with the other general purpose filter modes.</span></span> <span data-ttu-id="9b519-140">in **Beispiel \_ c** wird das Verhalten der allgemeinen Filter so geändert, dass die Filter, die alle gefiltert werden, aufgrund von Vergleichs Ergebnissen 1.0 f oder 0,0 f werden.</span><span class="sxs-lookup"><span data-stu-id="9b519-140">**sample\_c** changes the behavior of the general purpose filters such that the values being filtered all become 1.0f or 0.0f due to comparison results.</span></span>

<span data-ttu-id="9b519-141">Wenn Sie aus einem Eingabe Slot abrufen, an das nichts gebunden ist, wird 0 für alle Komponenten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9b519-141">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="9b519-142">Weitere Informationen finden Sie in der [Beispiel](sample--sm4---asm-.md) Anweisung.</span><span class="sxs-lookup"><span data-stu-id="9b519-142">For more information, see the [sample](sample--sm4---asm-.md) instruction.</span></span>

<span data-ttu-id="9b519-143">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="9b519-143">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9b519-144">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="9b519-144">Vertex Shader</span></span> | <span data-ttu-id="9b519-145">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="9b519-145">Geometry Shader</span></span> | <span data-ttu-id="9b519-146">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="9b519-146">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="9b519-147">x</span><span class="sxs-lookup"><span data-stu-id="9b519-147">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9b519-148">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="9b519-148">Minimum Shader Model</span></span>

<span data-ttu-id="9b519-149">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b519-149">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9b519-150">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="9b519-150">Shader Model</span></span>                                              | <span data-ttu-id="9b519-151">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="9b519-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9b519-152">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="9b519-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9b519-153">ja</span><span class="sxs-lookup"><span data-stu-id="9b519-153">yes</span></span>       |
| [<span data-ttu-id="9b519-154">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="9b519-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9b519-155">ja</span><span class="sxs-lookup"><span data-stu-id="9b519-155">yes</span></span>       |
| [<span data-ttu-id="9b519-156">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="9b519-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9b519-157">ja</span><span class="sxs-lookup"><span data-stu-id="9b519-157">yes</span></span>       |
| [<span data-ttu-id="9b519-158">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b519-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9b519-159">nein</span><span class="sxs-lookup"><span data-stu-id="9b519-159">no</span></span>        |
| [<span data-ttu-id="9b519-160">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b519-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9b519-161">nein</span><span class="sxs-lookup"><span data-stu-id="9b519-161">no</span></span>        |
| [<span data-ttu-id="9b519-162">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b519-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9b519-163">nein</span><span class="sxs-lookup"><span data-stu-id="9b519-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9b519-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9b519-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b519-165">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b519-165">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





