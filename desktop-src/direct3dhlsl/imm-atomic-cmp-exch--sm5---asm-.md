---
title: imm_atomic_cmp_exch (SM5-ASM)
description: Sofortiger Vergleich und Austausch in den Arbeitsspeicher.
ms.assetid: 317A69E1-0E0A-45C8-8E0A-B88659ADBECC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63e1be030d7cce0d6f0a581788db39a599272b2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857799"
---
# <a name="imm_atomic_cmp_exch-sm5---asm"></a><span data-ttu-id="2e392-103">imm \_ Atomic \_ CMP \_ -Exch (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2e392-103">imm\_atomic\_cmp\_exch (sm5 - asm)</span></span>

<span data-ttu-id="2e392-104">Sofortiger Vergleich und Austausch in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="2e392-104">Immediate compare and exchange to memory.</span></span>



| <span data-ttu-id="2e392-105">imm \_ Atomic \_ CMP \_ Exch dst0 \[ . Single \_ Component \_ mask \] , dST1, dstaddress \[ . Swizzle \] , src0 \[ . Select \_ Component \] , Quelle1 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="2e392-105">imm\_atomic\_cmp\_exch dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\], src1\[.select\_component\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2e392-106">Element</span><span class="sxs-lookup"><span data-stu-id="2e392-106">Item</span></span>                                                                                                           | <span data-ttu-id="2e392-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e392-107">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e392-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="2e392-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="2e392-109">\[Out \] enthält *dST1* vor dem Schreibvorgang.</span><span class="sxs-lookup"><span data-stu-id="2e392-109">\[out\] Contains *dst1* before the write.</span></span><br/>                                                                              |
| <span data-ttu-id="2e392-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="2e392-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="2e392-111">\[in \] einer ungeordneten Zugriffs Ansicht (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="2e392-111">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="2e392-112">Im COMPUTE-Shader kann dies auch Thread Gruppe Shared Memory (g \# ) sein.</span><span class="sxs-lookup"><span data-stu-id="2e392-112">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="2e392-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstaddress*</span><span class="sxs-lookup"><span data-stu-id="2e392-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="2e392-114">\[im \] Zielspeicher.</span><span class="sxs-lookup"><span data-stu-id="2e392-114">\[in\] The destination memory.</span></span><br/>                                                                                         |
| <span data-ttu-id="2e392-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2e392-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="2e392-116">\[im \] Wert, der mit *dST1* verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e392-116">\[in\] The value to compare to *dst1*.</span></span><br/>                                                                                 |
| <span data-ttu-id="2e392-117"><span id="scr1"></span><span id="SCR1"></span>*scr1*</span><span class="sxs-lookup"><span data-stu-id="2e392-117"><span id="scr1"></span><span id="SCR1"></span>*scr1*</span></span><br/>                                                | <span data-ttu-id="2e392-118">\[in \] dem Wert, der in den Zielspeicher geschrieben wird, wenn die verglichenen Werte identisch sind.</span><span class="sxs-lookup"><span data-stu-id="2e392-118">\[in\] The value written to the destination memory if the compared values are identical.</span></span><br/>                               |



 

<span data-ttu-id="2e392-119">Diese Anweisung führt einen einzelnen 32-Bit-Komponenten Vergleich von Operand *src0* mit *dST1* bei 32 Bit pro Komponenten Adresse *dstaddress* aus.</span><span class="sxs-lookup"><span data-stu-id="2e392-119">This instruction performs a single component 32-bit value compare of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="2e392-120">Wenn *dST1* eine u ist \# , wurde Sie möglicherweise als RAW, typisiert oder strukturiert deklariert.</span><span class="sxs-lookup"><span data-stu-id="2e392-120">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="2e392-121">Wenn Sie eingegeben wird, muss Sie als uint/Sint mit dem gebundenen Ressourcen Format "R32 \_ uint/ \_ Sint" deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="2e392-121">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="2e392-122">Wenn *dST1* den Wert g \# hat, muss er als RAW oder strukturiert deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="2e392-122">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="2e392-123">Wenn die verglichenen Werte identisch sind, wird der 32-Bit-Einzelkomponenten Wert in *Quelle1* in den Zielspeicher geschrieben.</span><span class="sxs-lookup"><span data-stu-id="2e392-123">If the compared values are identical, the single-component 32-bit value in *src1* is written to the destination memory.</span></span> <span data-ttu-id="2e392-124">Andernfalls wird der Ziel Arbeitsspeicher nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="2e392-124">Otherwise, the destination memory is not changed.</span></span>

<span data-ttu-id="2e392-125">Der ursprüngliche 32-Bit-Wert im Zielspeicher wird immer in *dst0* geschrieben.</span><span class="sxs-lookup"><span data-stu-id="2e392-125">The original 32-bit value in the destination memory is always written to *dst0*.</span></span>

<span data-ttu-id="2e392-126">Der gesamte Vorgang wird atomisch ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e392-126">The entire operation is performed atomically.</span></span>

<span data-ttu-id="2e392-127">Wenn der Shader-Aufruf inaktiv ist, z. b. wenn das Pixel zuvor in seiner Ausführung verworfen wurde oder ein Pixel-/Beispielaufruf nur vorhanden ist, um als Hilfsobjekt/Stichprobe für Ableitungen zu dienen, ändert diese Anweisung den *dST1* -Arbeitsspeicher nicht, und der zurückgegebene Wert ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="2e392-127">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="2e392-128">Die Out-of-Bounds-Adressierung in u \# bewirkt, dass nichts in den Arbeitsspeicher geschrieben wird, außer wenn die u \# strukturiert ist und der Byte Offset in die Struktur (zweite Komponente der Adresse) den Zugriff außerhalb der Grenzen verursacht, dann wird der gesamte Inhalt der UAV nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="2e392-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="2e392-129">Die Adressierung für "u" \# oder "g" bewirkt, \# dass ein nicht definiertes Ergebnis an den Shader in *dst0* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2e392-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="2e392-130">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="2e392-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2e392-131">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="2e392-131">Vertex</span></span> | <span data-ttu-id="2e392-132">Hülle</span><span class="sxs-lookup"><span data-stu-id="2e392-132">Hull</span></span> | <span data-ttu-id="2e392-133">Domain</span><span class="sxs-lookup"><span data-stu-id="2e392-133">Domain</span></span> | <span data-ttu-id="2e392-134">Geometrie</span><span class="sxs-lookup"><span data-stu-id="2e392-134">Geometry</span></span> | <span data-ttu-id="2e392-135">Pixel</span><span class="sxs-lookup"><span data-stu-id="2e392-135">Pixel</span></span> | <span data-ttu-id="2e392-136">Compute</span><span class="sxs-lookup"><span data-stu-id="2e392-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2e392-137">X</span><span class="sxs-lookup"><span data-stu-id="2e392-137">X</span></span>     | <span data-ttu-id="2e392-138">X</span><span class="sxs-lookup"><span data-stu-id="2e392-138">X</span></span>       |



 

<span data-ttu-id="2e392-139">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="2e392-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="2e392-140">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="2e392-140">Vertex</span></span> | <span data-ttu-id="2e392-141">Hülle</span><span class="sxs-lookup"><span data-stu-id="2e392-141">Hull</span></span> | <span data-ttu-id="2e392-142">Domain</span><span class="sxs-lookup"><span data-stu-id="2e392-142">Domain</span></span> | <span data-ttu-id="2e392-143">Geometrie</span><span class="sxs-lookup"><span data-stu-id="2e392-143">Geometry</span></span> | <span data-ttu-id="2e392-144">Pixel</span><span class="sxs-lookup"><span data-stu-id="2e392-144">Pixel</span></span> | <span data-ttu-id="2e392-145">Compute</span><span class="sxs-lookup"><span data-stu-id="2e392-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2e392-146">X</span><span class="sxs-lookup"><span data-stu-id="2e392-146">X</span></span>      | <span data-ttu-id="2e392-147">X</span><span class="sxs-lookup"><span data-stu-id="2e392-147">X</span></span>    | <span data-ttu-id="2e392-148">X</span><span class="sxs-lookup"><span data-stu-id="2e392-148">X</span></span>      | <span data-ttu-id="2e392-149">X</span><span class="sxs-lookup"><span data-stu-id="2e392-149">X</span></span>        | <span data-ttu-id="2e392-150">X</span><span class="sxs-lookup"><span data-stu-id="2e392-150">X</span></span>     | <span data-ttu-id="2e392-151">X</span><span class="sxs-lookup"><span data-stu-id="2e392-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2e392-152">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="2e392-152">Minimum Shader Model</span></span>

<span data-ttu-id="2e392-153">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="2e392-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2e392-154">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="2e392-154">Shader Model</span></span>                                              | <span data-ttu-id="2e392-155">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="2e392-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2e392-156">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="2e392-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2e392-157">ja</span><span class="sxs-lookup"><span data-stu-id="2e392-157">yes</span></span>       |
| [<span data-ttu-id="2e392-158">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="2e392-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2e392-159">nein</span><span class="sxs-lookup"><span data-stu-id="2e392-159">no</span></span>        |
| [<span data-ttu-id="2e392-160">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="2e392-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2e392-161">nein</span><span class="sxs-lookup"><span data-stu-id="2e392-161">no</span></span>        |
| [<span data-ttu-id="2e392-162">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2e392-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2e392-163">nein</span><span class="sxs-lookup"><span data-stu-id="2e392-163">no</span></span>        |
| [<span data-ttu-id="2e392-164">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2e392-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2e392-165">nein</span><span class="sxs-lookup"><span data-stu-id="2e392-165">no</span></span>        |
| [<span data-ttu-id="2e392-166">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2e392-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2e392-167">nein</span><span class="sxs-lookup"><span data-stu-id="2e392-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2e392-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2e392-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e392-169">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2e392-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





