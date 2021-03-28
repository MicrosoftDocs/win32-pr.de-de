---
title: imm_atomic_exch (SM5-ASM)
description: Direkter atomarer Austausch in den Arbeitsspeicher.
ms.assetid: D06AE57E-52A4-4579-84FF-7DE9E713A5E3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb38cd696af079c5ae7dc896db619b95dd1d1d6c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101098"
---
# <a name="imm_atomic_exch-sm5---asm"></a><span data-ttu-id="c2166-103">imm \_ Atomic \_ Exch (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c2166-103">imm\_atomic\_exch (sm5 - asm)</span></span>

<span data-ttu-id="c2166-104">Direkter atomarer Austausch in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c2166-104">Immediate atomic exchange to memory.</span></span>



| <span data-ttu-id="c2166-105">imm \_ Atomic \_ Exch dst0 \[ . Single \_ Component \_ mask \] , dST1, dstaddress \[ . Swizzle \] , src0 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="c2166-105">imm\_atomic\_exch dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="c2166-106">Element</span><span class="sxs-lookup"><span data-stu-id="c2166-106">Item</span></span>                                                                                                           | <span data-ttu-id="c2166-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2166-107">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2166-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="c2166-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="c2166-109">\[in \] enthält den Wert von *dST1* vor dem Schreibvorgang.</span><span class="sxs-lookup"><span data-stu-id="c2166-109">\[in\] Contains the value from *dst1* before the write.</span></span><br/>                                                                |
| <span data-ttu-id="c2166-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="c2166-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="c2166-111">\[in \] einer ungeordneten Zugriffs Ansicht (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="c2166-111">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="c2166-112">Im COMPUTE-Shader kann dies auch Thread Gruppe Shared Memory (g \# ) sein.</span><span class="sxs-lookup"><span data-stu-id="c2166-112">In the Compute Shader this can also be Thread Group Shared Memory (g\#).</span></span> <br/> |
| <span data-ttu-id="c2166-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstaddress*</span><span class="sxs-lookup"><span data-stu-id="c2166-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="c2166-114">\[in \] der Speicheradresse.</span><span class="sxs-lookup"><span data-stu-id="c2166-114">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="c2166-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c2166-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="c2166-116">\[in \] dem Wert, der in *dST1* in *dstaddress* geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2166-116">\[in\] The value to write to *dst1* at *dstAddress*.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="c2166-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2166-117">Remarks</span></span>

<span data-ttu-id="c2166-118">Diese Anweisung führt einen einzelnen Komponenten-32-Bit-Wert Schreiben von Operand *src0* zu *dST1* um 32 Bit pro Komponenten Adresse *dstaddress* aus.</span><span class="sxs-lookup"><span data-stu-id="c2166-118">This instruction performs a single component 32-bit value write of operand *src0* to *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="c2166-119">Wenn *dST1* eine u ist \# , wurde Sie möglicherweise als RAW, typisiert oder strukturiert deklariert.</span><span class="sxs-lookup"><span data-stu-id="c2166-119">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="c2166-120">Wenn Sie eingegeben wird, muss Sie als uint/Sint mit dem gebundenen Ressourcen Format "R32 \_ uint/ \_ Sint" deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="c2166-120">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="c2166-121">Wenn *dST1* den Wert g \# hat, muss er als RAW oder strukturiert deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="c2166-121">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="c2166-122">Die Anzahl der Komponenten, die von der Adresse entnommen werden, hängt von der Dimensionalität der Ressource ab, die unter *dST1* deklariert ist.</span><span class="sxs-lookup"><span data-stu-id="c2166-122">The number of components taken from the address is determined by the dimensionality of the resource declared at *dst1*.</span></span>

<span data-ttu-id="c2166-123">Der ursprüngliche 32-Bit-Wert im Zielspeicher wird in *dst0* geschrieben.</span><span class="sxs-lookup"><span data-stu-id="c2166-123">The original 32-bit value in the destination memory is written to *dst0*.</span></span>

<span data-ttu-id="c2166-124">Der gesamte Vorgang wird atomisch ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2166-124">The entire operation is performed atomically.</span></span>

<span data-ttu-id="c2166-125">Wenn der Shader-Aufruf inaktiv ist, z. b. wenn das Pixel zuvor in seiner Ausführung verworfen wurde oder ein Pixel-/Beispielaufruf nur vorhanden ist, um als Hilfsobjekt/Stichprobe für Ableitungen zu dienen, ändert diese Anweisung den *dST1* -Arbeitsspeicher nicht, und der zurückgegebene Wert ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="c2166-125">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="c2166-126">Die Out-of-Bounds-Adressierung in u \# bewirkt, dass nichts in den Arbeitsspeicher geschrieben wird, außer wenn die u \# strukturiert ist und der Byte Offset in die Struktur (zweite Komponente der Adresse) den Zugriff außerhalb der Grenzen verursacht, dann wird der gesamte Inhalt der UAV nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="c2166-126">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="c2166-127">Die Adressierung für "u" \# oder "g" bewirkt, \# dass ein nicht definiertes Ergebnis an den Shader in *dst0* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c2166-127">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="c2166-128">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="c2166-128">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c2166-129">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c2166-129">Vertex</span></span> | <span data-ttu-id="c2166-130">Hülle</span><span class="sxs-lookup"><span data-stu-id="c2166-130">Hull</span></span> | <span data-ttu-id="c2166-131">Domain</span><span class="sxs-lookup"><span data-stu-id="c2166-131">Domain</span></span> | <span data-ttu-id="c2166-132">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c2166-132">Geometry</span></span> | <span data-ttu-id="c2166-133">Pixel</span><span class="sxs-lookup"><span data-stu-id="c2166-133">Pixel</span></span> | <span data-ttu-id="c2166-134">Compute</span><span class="sxs-lookup"><span data-stu-id="c2166-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c2166-135">X</span><span class="sxs-lookup"><span data-stu-id="c2166-135">X</span></span>     | <span data-ttu-id="c2166-136">X</span><span class="sxs-lookup"><span data-stu-id="c2166-136">X</span></span>       |



 

<span data-ttu-id="c2166-137">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c2166-137">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="c2166-138">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c2166-138">Vertex</span></span> | <span data-ttu-id="c2166-139">Hülle</span><span class="sxs-lookup"><span data-stu-id="c2166-139">Hull</span></span> | <span data-ttu-id="c2166-140">Domain</span><span class="sxs-lookup"><span data-stu-id="c2166-140">Domain</span></span> | <span data-ttu-id="c2166-141">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c2166-141">Geometry</span></span> | <span data-ttu-id="c2166-142">Pixel</span><span class="sxs-lookup"><span data-stu-id="c2166-142">Pixel</span></span> | <span data-ttu-id="c2166-143">Compute</span><span class="sxs-lookup"><span data-stu-id="c2166-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c2166-144">X</span><span class="sxs-lookup"><span data-stu-id="c2166-144">X</span></span>      | <span data-ttu-id="c2166-145">X</span><span class="sxs-lookup"><span data-stu-id="c2166-145">X</span></span>    | <span data-ttu-id="c2166-146">X</span><span class="sxs-lookup"><span data-stu-id="c2166-146">X</span></span>      | <span data-ttu-id="c2166-147">X</span><span class="sxs-lookup"><span data-stu-id="c2166-147">X</span></span>        | <span data-ttu-id="c2166-148">X</span><span class="sxs-lookup"><span data-stu-id="c2166-148">X</span></span>     | <span data-ttu-id="c2166-149">X</span><span class="sxs-lookup"><span data-stu-id="c2166-149">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c2166-150">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c2166-150">Minimum Shader Model</span></span>

<span data-ttu-id="c2166-151">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c2166-151">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c2166-152">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c2166-152">Shader Model</span></span>                                              | <span data-ttu-id="c2166-153">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c2166-153">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c2166-154">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="c2166-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c2166-155">ja</span><span class="sxs-lookup"><span data-stu-id="c2166-155">yes</span></span>       |
| [<span data-ttu-id="c2166-156">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="c2166-156">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c2166-157">nein</span><span class="sxs-lookup"><span data-stu-id="c2166-157">no</span></span>        |
| [<span data-ttu-id="c2166-158">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="c2166-158">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c2166-159">nein</span><span class="sxs-lookup"><span data-stu-id="c2166-159">no</span></span>        |
| [<span data-ttu-id="c2166-160">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2166-160">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c2166-161">nein</span><span class="sxs-lookup"><span data-stu-id="c2166-161">no</span></span>        |
| [<span data-ttu-id="c2166-162">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2166-162">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c2166-163">nein</span><span class="sxs-lookup"><span data-stu-id="c2166-163">no</span></span>        |
| [<span data-ttu-id="c2166-164">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2166-164">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c2166-165">nein</span><span class="sxs-lookup"><span data-stu-id="c2166-165">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c2166-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c2166-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2166-167">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2166-167">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





