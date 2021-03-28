---
title: imm_atomic_or (SM5-ASM)
description: Direkter atomarischer bitweiser or-Operator. Gibt den Wert im Arbeitsspeicher vor oder zurück.
ms.assetid: 0ACE977D-5D0E-4E9C-A49F-B81D789B0D43
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2bc3b9afd2ba9f4dc63a8fb5c5818c1121c7ec6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038352"
---
# <a name="imm_atomic_or-sm5---asm"></a><span data-ttu-id="341c9-104">imm \_ Atomic \_ oder (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="341c9-104">imm\_atomic\_or (sm5 - asm)</span></span>

<span data-ttu-id="341c9-105">Direkter atomarischer bitweiser or-Operator.</span><span class="sxs-lookup"><span data-stu-id="341c9-105">Immediate atomic bitwise OR to memory.</span></span> <span data-ttu-id="341c9-106">Gibt den Wert im Arbeitsspeicher vor oder zurück.</span><span class="sxs-lookup"><span data-stu-id="341c9-106">Returns the value in memory before the OR.</span></span>



| <span data-ttu-id="341c9-107">imm \_ Atomic \_ oder dst0 \[ . Single \_ Component \_ mask \] , dST1, dstaddress \[ . Swizzle \] , src0 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="341c9-107">imm\_atomic\_or dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="341c9-108">Element</span><span class="sxs-lookup"><span data-stu-id="341c9-108">Item</span></span>                                                                                                           | <span data-ttu-id="341c9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="341c9-109">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="341c9-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="341c9-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="341c9-111">\[in \] enthält den Wert von *dST1* vor oder.</span><span class="sxs-lookup"><span data-stu-id="341c9-111">\[in\] Contains the value from *dst1* before the OR.</span></span><br/>                                                                   |
| <span data-ttu-id="341c9-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="341c9-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="341c9-113">\[in \] einer ungeordneten Zugriffs Ansicht (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="341c9-113">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="341c9-114">Im COMPUTE-Shader kann dies auch Thread Gruppe Shared Memory (g \# ) sein.</span><span class="sxs-lookup"><span data-stu-id="341c9-114">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="341c9-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstaddress*</span><span class="sxs-lookup"><span data-stu-id="341c9-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="341c9-116">\[in \] der Speicheradresse.</span><span class="sxs-lookup"><span data-stu-id="341c9-116">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="341c9-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="341c9-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="341c9-118">Der Wert für oder mit *dST1*.</span><span class="sxs-lookup"><span data-stu-id="341c9-118">The value to OR with *dst1*.</span></span><br/>                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="341c9-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="341c9-119">Remarks</span></span>

<span data-ttu-id="341c9-120">Diese Anweisung führt eine einzelne Komponente 32-Bit bitweises OR of Operand *src0* with *dST1* at 32-Bit pro Component Address *dstaddress* aus.</span><span class="sxs-lookup"><span data-stu-id="341c9-120">This instruction performs a single component 32-bit bitwise OR of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="341c9-121">Wenn *dST1* eine u ist \# , wurde Sie möglicherweise als RAW, typisiert oder strukturiert deklariert.</span><span class="sxs-lookup"><span data-stu-id="341c9-121">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="341c9-122">Wenn Sie eingegeben wird, muss Sie als uint/Sint mit dem gebundenen Ressourcen Format "R32 \_ uint/ \_ Sint" deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="341c9-122">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="341c9-123">Wenn *dST1* den Wert g \# hat, muss er als RAW oder strukturiert deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="341c9-123">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="341c9-124">Der Wert im *dST1* -Arbeitsspeicher, bevor oder an *dst0* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="341c9-124">The value in *dst1* memory before the OR is returned to *dst0*.</span></span>

<span data-ttu-id="341c9-125">Der gesamte Vorgang wird atomisch ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="341c9-125">The entire operation is performed atomically.</span></span>

<span data-ttu-id="341c9-126">Die Anzahl der Komponenten, die von der Adresse entnommen werden, hängt von der Dimensionalität der Ressource ab, die unter *dST1* deklariert ist.</span><span class="sxs-lookup"><span data-stu-id="341c9-126">The number of components taken from the address is determined by the dimensionality of the resource declared at *dst1*.</span></span>

<span data-ttu-id="341c9-127">Wenn der Shader-Aufruf inaktiv ist, z. b. wenn das Pixel zuvor in seiner Ausführung verworfen wurde oder ein Pixel-/Beispielaufruf nur vorhanden ist, um als Hilfsobjekt/Stichprobe für Ableitungen zu dienen, ändert diese Anweisung den *dST1* -Arbeitsspeicher nicht, und der zurückgegebene Wert ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="341c9-127">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="341c9-128">Die Out-of-Bounds-Adressierung in u \# bewirkt, dass nichts in den Arbeitsspeicher geschrieben wird, außer wenn die u \# strukturiert ist und der Byte Offset in die Struktur (zweite Komponente der Adresse) den Zugriff außerhalb der Grenzen verursacht, dann wird der gesamte Inhalt der UAV nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="341c9-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="341c9-129">Die Adressierung für "u" \# oder "g" bewirkt, \# dass ein nicht definiertes Ergebnis an den Shader in *dst0* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="341c9-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="341c9-130">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="341c9-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="341c9-131">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="341c9-131">Vertex</span></span> | <span data-ttu-id="341c9-132">Hülle</span><span class="sxs-lookup"><span data-stu-id="341c9-132">Hull</span></span> | <span data-ttu-id="341c9-133">Domain</span><span class="sxs-lookup"><span data-stu-id="341c9-133">Domain</span></span> | <span data-ttu-id="341c9-134">Geometrie</span><span class="sxs-lookup"><span data-stu-id="341c9-134">Geometry</span></span> | <span data-ttu-id="341c9-135">Pixel</span><span class="sxs-lookup"><span data-stu-id="341c9-135">Pixel</span></span> | <span data-ttu-id="341c9-136">Compute</span><span class="sxs-lookup"><span data-stu-id="341c9-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="341c9-137">X</span><span class="sxs-lookup"><span data-stu-id="341c9-137">X</span></span>     | <span data-ttu-id="341c9-138">X</span><span class="sxs-lookup"><span data-stu-id="341c9-138">X</span></span>       |



 

<span data-ttu-id="341c9-139">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="341c9-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="341c9-140">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="341c9-140">Vertex</span></span> | <span data-ttu-id="341c9-141">Hülle</span><span class="sxs-lookup"><span data-stu-id="341c9-141">Hull</span></span> | <span data-ttu-id="341c9-142">Domain</span><span class="sxs-lookup"><span data-stu-id="341c9-142">Domain</span></span> | <span data-ttu-id="341c9-143">Geometrie</span><span class="sxs-lookup"><span data-stu-id="341c9-143">Geometry</span></span> | <span data-ttu-id="341c9-144">Pixel</span><span class="sxs-lookup"><span data-stu-id="341c9-144">Pixel</span></span> | <span data-ttu-id="341c9-145">Compute</span><span class="sxs-lookup"><span data-stu-id="341c9-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="341c9-146">X</span><span class="sxs-lookup"><span data-stu-id="341c9-146">X</span></span>      | <span data-ttu-id="341c9-147">X</span><span class="sxs-lookup"><span data-stu-id="341c9-147">X</span></span>    | <span data-ttu-id="341c9-148">X</span><span class="sxs-lookup"><span data-stu-id="341c9-148">X</span></span>      | <span data-ttu-id="341c9-149">X</span><span class="sxs-lookup"><span data-stu-id="341c9-149">X</span></span>        | <span data-ttu-id="341c9-150">X</span><span class="sxs-lookup"><span data-stu-id="341c9-150">X</span></span>     | <span data-ttu-id="341c9-151">X</span><span class="sxs-lookup"><span data-stu-id="341c9-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="341c9-152">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="341c9-152">Minimum Shader Model</span></span>

<span data-ttu-id="341c9-153">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="341c9-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="341c9-154">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="341c9-154">Shader Model</span></span>                                              | <span data-ttu-id="341c9-155">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="341c9-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="341c9-156">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="341c9-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="341c9-157">ja</span><span class="sxs-lookup"><span data-stu-id="341c9-157">yes</span></span>       |
| [<span data-ttu-id="341c9-158">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="341c9-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="341c9-159">nein</span><span class="sxs-lookup"><span data-stu-id="341c9-159">no</span></span>        |
| [<span data-ttu-id="341c9-160">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="341c9-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="341c9-161">nein</span><span class="sxs-lookup"><span data-stu-id="341c9-161">no</span></span>        |
| [<span data-ttu-id="341c9-162">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="341c9-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="341c9-163">nein</span><span class="sxs-lookup"><span data-stu-id="341c9-163">no</span></span>        |
| [<span data-ttu-id="341c9-164">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="341c9-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="341c9-165">nein</span><span class="sxs-lookup"><span data-stu-id="341c9-165">no</span></span>        |
| [<span data-ttu-id="341c9-166">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="341c9-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="341c9-167">nein</span><span class="sxs-lookup"><span data-stu-id="341c9-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="341c9-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="341c9-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="341c9-169">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="341c9-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





