---
title: Swap (SM5-ASM)
description: Führt einen Komponenten bezogenen bedingten Austausch der Werte zwischen zwei Eingabe Registern aus.
ms.assetid: 3DFCEB82-076E-4AFA-915F-47390A355B7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d2ee674a1cb1067594b0e96c739ff8df73b152
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993087"
---
# <a name="swapc-sm5---asm"></a><span data-ttu-id="d565e-103">Swap (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="d565e-103">swapc (sm5 - asm)</span></span>

<span data-ttu-id="d565e-104">Führt einen Komponenten bezogenen bedingten Austausch der Werte zwischen zwei Eingabe Registern aus.</span><span class="sxs-lookup"><span data-stu-id="d565e-104">Performs a component-wise conditional swap of the values between two input registers.</span></span>



| <span data-ttu-id="d565e-105">"dest0. \[ Mask" \] , "dest1 \[ . Mask" \] , "src0 \[ . Swizzle" \] , "Quelle1 \[ . Swizzle" \] , "Quelle2 \[ . Swizzle"\]</span><span class="sxs-lookup"><span data-stu-id="d565e-105">swapc dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="d565e-106">Element</span><span class="sxs-lookup"><span data-stu-id="d565e-106">Item</span></span>                                                               | <span data-ttu-id="d565e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d565e-107">Description</span></span>                                                                                     |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d565e-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="d565e-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="d565e-109">\[in registrieren Sie sich für \] beliebige nicht leere Schreib Masken.</span><span class="sxs-lookup"><span data-stu-id="d565e-109">\[in\] Register with arbitrary nonempty write masks.</span></span> <span data-ttu-id="d565e-110">Muss sich von *dest1* unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="d565e-110">Must be different than *dest1*.</span></span><br/> |
| <span data-ttu-id="d565e-111"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="d565e-111"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="d565e-112">\[in registrieren Sie sich für \] beliebige nicht leere Schreib Masken.</span><span class="sxs-lookup"><span data-stu-id="d565e-112">\[in\] Register with arbitrary nonempty write masks.</span></span> <span data-ttu-id="d565e-113">Muss sich von *dest0* unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="d565e-113">Must be different than *dest0*.</span></span><br/> |
| <span data-ttu-id="d565e-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d565e-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="d565e-115">\[in werden \] vier Bedingungen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d565e-115">\[in\] Provides 4 conditions.</span></span> <span data-ttu-id="d565e-116">Ein ganzzahliger Wert ungleich 0 bedeutet **true**.</span><span class="sxs-lookup"><span data-stu-id="d565e-116">A nonzero integer value means **true**.</span></span> <br/>               |
| <span data-ttu-id="d565e-117"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="d565e-117"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="d565e-118">\[in \] einem der Werte, die ausgetauscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d565e-118">\[in\] One of the values to be swapped.</span></span><br/>                                              |
| <span data-ttu-id="d565e-119"><span id="src2"></span><span id="SRC2"></span>*Quelle2*</span><span class="sxs-lookup"><span data-stu-id="d565e-119"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/>    | <span data-ttu-id="d565e-120">\[in \] einem der Werte, die ausgetauscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d565e-120">\[in\] One of the values to be swapped.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="d565e-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d565e-121">Remarks</span></span>

<span data-ttu-id="d565e-122">Die Codierung dieser Anweisung versucht, mehrere parallele bedingte Austausch Vorgänge von skalaren in 2 4-Komponenten Registern zu Ausdrücken, wobei die Anordnung der Paare von Zahlen, die an dem Austausch beteiligt sind, geringfügig flexibel ist.</span><span class="sxs-lookup"><span data-stu-id="d565e-122">The encoding of this instruction attempts to compactly express multiple parallel conditional swaps of scalars across two 4-component registers, with minor flexibility in the arrangement of the pairs of numbers involved in swapping.</span></span>

<span data-ttu-id="d565e-123">Die Auswahl von Register und Wert für *src0*, *Quelle1* und *Quelle2* ist in keiner Weise eingeschränkt, wie z. b. in der Art von " [muvc](movc--sm4---asm-.md)".</span><span class="sxs-lookup"><span data-stu-id="d565e-123">The choice of register and value for *src0*, *src1*, and *src2* are unconstrained in any way, like [movc](movc--sm4---asm-.md).</span></span>

<span data-ttu-id="d565e-124">Die Semantik dieser Anweisung kann durch die entsprechenden Vorgänge mit der Anweisung " **muvc** " beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d565e-124">The semantics of this instruction can be described by the equivalent operations with the **movc** instruction.</span></span> <span data-ttu-id="d565e-125">Der schlimmste Fall wird im folgenden Beispiel gezeigt, um sicherzustellen, dass die Ziel Register bis zum Ende nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d565e-125">The worst case is shown in the following example, making sure destination registers are not updated until the end.</span></span>

``` syntax
                swapc dest0[.mask], 
                      dest1[.mask],
                      src0[.swizzle],
                      src1[.swizzle],
                      src2[.swizzle]

                expands to:

                movc temp[dest0 s mask], 
                     src0[.swizzle], 
                     src2[.swizzle], src1[.swizzle]

                movc dest1[.mask], 
                     src0[.swizzle], 
                     src1[.swizzle], src2[.swizzle]

                mov  dest0.mask, temp
```

<span data-ttu-id="d565e-126">Sie können auswählen, wie der Task angegangen werden soll, wenn nicht direkt.</span><span class="sxs-lookup"><span data-stu-id="d565e-126">You can choose how to tackle the task, if not directly.</span></span> <span data-ttu-id="d565e-127">Der gleiche Effekt kann z. b. durch eine Sequenz von bis zu 4 einfachen skalarbedingtem Austausch Vorgängen oder wie oben beschrieben werden, und zwar mit zwei Vektor- **muvc** -Anweisungen, zuzüglich des Aufwands, um sicherzustellen, dass die Quell Werte nicht durch frühere Vorgänge in der Mitte der Erweiterung geclot werden.</span><span class="sxs-lookup"><span data-stu-id="d565e-127">For example, the same effect can be achieved by a sequence of up to 4 simple scalar conditional swaps, or as above, two vector **movc** instructions, plus any overhead to make sure the source values are not clobbered by earlier operations in the midst of the expansion.</span></span>

<span data-ttu-id="d565e-128">Verwenden Sie diese Anweisung zum Sortieren.</span><span class="sxs-lookup"><span data-stu-id="d565e-128">Use this instruction for sorting.</span></span>

<span data-ttu-id="d565e-129">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="d565e-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d565e-130">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="d565e-130">Vertex</span></span> | <span data-ttu-id="d565e-131">Hülle</span><span class="sxs-lookup"><span data-stu-id="d565e-131">Hull</span></span> | <span data-ttu-id="d565e-132">Domain</span><span class="sxs-lookup"><span data-stu-id="d565e-132">Domain</span></span> | <span data-ttu-id="d565e-133">Geometrie</span><span class="sxs-lookup"><span data-stu-id="d565e-133">Geometry</span></span> | <span data-ttu-id="d565e-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="d565e-134">Pixel</span></span> | <span data-ttu-id="d565e-135">Compute</span><span class="sxs-lookup"><span data-stu-id="d565e-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d565e-136">X</span><span class="sxs-lookup"><span data-stu-id="d565e-136">X</span></span>      | <span data-ttu-id="d565e-137">X</span><span class="sxs-lookup"><span data-stu-id="d565e-137">X</span></span>    | <span data-ttu-id="d565e-138">X</span><span class="sxs-lookup"><span data-stu-id="d565e-138">X</span></span>      | <span data-ttu-id="d565e-139">X</span><span class="sxs-lookup"><span data-stu-id="d565e-139">X</span></span>        | <span data-ttu-id="d565e-140">X</span><span class="sxs-lookup"><span data-stu-id="d565e-140">X</span></span>     | <span data-ttu-id="d565e-141">X</span><span class="sxs-lookup"><span data-stu-id="d565e-141">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d565e-142">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="d565e-142">Minimum Shader Model</span></span>

<span data-ttu-id="d565e-143">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d565e-143">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d565e-144">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d565e-144">Shader Model</span></span>                                              | <span data-ttu-id="d565e-145">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d565e-145">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d565e-146">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="d565e-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d565e-147">ja</span><span class="sxs-lookup"><span data-stu-id="d565e-147">yes</span></span>       |
| [<span data-ttu-id="d565e-148">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="d565e-148">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d565e-149">nein</span><span class="sxs-lookup"><span data-stu-id="d565e-149">no</span></span>        |
| [<span data-ttu-id="d565e-150">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="d565e-150">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d565e-151">nein</span><span class="sxs-lookup"><span data-stu-id="d565e-151">no</span></span>        |
| [<span data-ttu-id="d565e-152">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d565e-152">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d565e-153">nein</span><span class="sxs-lookup"><span data-stu-id="d565e-153">no</span></span>        |
| [<span data-ttu-id="d565e-154">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d565e-154">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d565e-155">nein</span><span class="sxs-lookup"><span data-stu-id="d565e-155">no</span></span>        |
| [<span data-ttu-id="d565e-156">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d565e-156">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d565e-157">nein</span><span class="sxs-lookup"><span data-stu-id="d565e-157">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d565e-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d565e-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d565e-159">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d565e-159">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





