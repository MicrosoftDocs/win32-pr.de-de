---
title: imm_atomic_umax (SM5-ASM)
description: Sofortiger atomarer unsignierter Max-Wert im Speicher. Gibt den Wert im Arbeitsspeicher vor dem maximalen Vorgang zurück.
ms.assetid: 6C9D2CA3-1502-41E1-8535-C94DF31201E1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072ef5a2a8e91a17501015bdc34738465880d91e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389580"
---
# <a name="imm_atomic_umax-sm5---asm"></a><span data-ttu-id="c9202-104">imm \_ Atomic \_ Umax (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c9202-104">imm\_atomic\_umax (sm5 - asm)</span></span>

<span data-ttu-id="c9202-105">Sofortiger atomarer unsignierter Max-Wert im Speicher.</span><span class="sxs-lookup"><span data-stu-id="c9202-105">Immediate atomic unsigned max to memory.</span></span> <span data-ttu-id="c9202-106">Gibt den Wert im Arbeitsspeicher vor dem maximalen Vorgang zurück.</span><span class="sxs-lookup"><span data-stu-id="c9202-106">Returns value in memory before the max operation.</span></span>



| <span data-ttu-id="c9202-107">imm \_ Atomic \_ Umax dst0 \[ . Single \_ Component \_ mask \] , dST1, dstaddress \[ . Swizzle \] , src0 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="c9202-107">imm\_atomic\_umax dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="c9202-108">Element</span><span class="sxs-lookup"><span data-stu-id="c9202-108">Item</span></span>                                                                                                           | <span data-ttu-id="c9202-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9202-109">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9202-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="c9202-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="c9202-111">\[in \] enthält den Wert von *dST1* vor dieser Anweisung.</span><span class="sxs-lookup"><span data-stu-id="c9202-111">\[in\] Contains the value from *dst1* before this instruction.</span></span><br/>                                                         |
| <span data-ttu-id="c9202-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="c9202-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="c9202-113">\[in \] einer ungeordneten Zugriffs Ansicht (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="c9202-113">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="c9202-114">Im COMPUTE-Shader kann dies auch Thread Gruppe Shared Memory (g \# ) sein.</span><span class="sxs-lookup"><span data-stu-id="c9202-114">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="c9202-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstaddress*</span><span class="sxs-lookup"><span data-stu-id="c9202-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="c9202-116">\[in \] der Speicheradresse.</span><span class="sxs-lookup"><span data-stu-id="c9202-116">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="c9202-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c9202-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="c9202-118">\[in \] dem Wert, der mit *dST1* bei *dstaddress* verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9202-118">\[in\] The value to compare to *dst1* at *dstAddress*.</span></span><br/>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="c9202-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9202-119">Remarks</span></span>

<span data-ttu-id="c9202-120">Diese Anweisung führt eine einzelne Komponente mit einer Länge von 32 Bit ohne Vorzeichen des Operanden *src0* mit *dST1* bei 32 Bit pro Komponenten Adresse *dstaddress* aus.</span><span class="sxs-lookup"><span data-stu-id="c9202-120">This instruction performs a single component 32-bit unsigned maximum of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="c9202-121">Wenn *dST1* eine u ist \# , wurde Sie möglicherweise als RAW, typisiert oder strukturiert deklariert.</span><span class="sxs-lookup"><span data-stu-id="c9202-121">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="c9202-122">Wenn Sie eingegeben wird, muss Sie als uint/Sint mit dem gebundenen Ressourcen Format "R32 \_ uint/ \_ Sint" deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="c9202-122">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="c9202-123">Wenn *dST1* den Wert g \# hat, muss er als RAW oder strukturiert deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="c9202-123">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="c9202-124">Der Wert im *dST1* -Arbeitsspeicher vor dem maximalen Wert wird an *dst0* zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c9202-124">The value in *dst1* memory before max is returned to *dst0*.</span></span>

<span data-ttu-id="c9202-125">Die Anzahl der Komponenten, die von der Adresse entnommen werden, wird durch die Dimensionalität von *dST1* bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c9202-125">The number of components taken from the address is determined by the dimensionality of *dst1*.</span></span>

<span data-ttu-id="c9202-126">Der gesamte Vorgang wird atomisch ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9202-126">The entire operation is performed atomically.</span></span>

<span data-ttu-id="c9202-127">Wenn der Shader-Aufruf inaktiv ist, z. b. wenn das Pixel zuvor in seiner Ausführung verworfen wurde oder ein Pixel-/Beispielaufruf nur vorhanden ist, um als Hilfsobjekt/Stichprobe für Ableitungen zu dienen, ändert diese Anweisung den *dST1* -Arbeitsspeicher nicht, und der zurückgegebene Wert ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="c9202-127">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="c9202-128">Die Out-of-Bounds-Adressierung in u \# bewirkt, dass nichts in den Arbeitsspeicher geschrieben wird, außer wenn die u \# strukturiert ist und der Byte Offset in die Struktur (zweite Komponente der Adresse) den Zugriff außerhalb der Grenzen verursacht, dann wird der gesamte Inhalt der UAV nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="c9202-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="c9202-129">Die Adressierung für "u" \# oder "g" bewirkt, \# dass ein nicht definiertes Ergebnis an den Shader in *dst0* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c9202-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="c9202-130">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="c9202-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c9202-131">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c9202-131">Vertex</span></span> | <span data-ttu-id="c9202-132">Hülle</span><span class="sxs-lookup"><span data-stu-id="c9202-132">Hull</span></span> | <span data-ttu-id="c9202-133">Domain</span><span class="sxs-lookup"><span data-stu-id="c9202-133">Domain</span></span> | <span data-ttu-id="c9202-134">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c9202-134">Geometry</span></span> | <span data-ttu-id="c9202-135">Pixel</span><span class="sxs-lookup"><span data-stu-id="c9202-135">Pixel</span></span> | <span data-ttu-id="c9202-136">Compute</span><span class="sxs-lookup"><span data-stu-id="c9202-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c9202-137">X</span><span class="sxs-lookup"><span data-stu-id="c9202-137">X</span></span>     | <span data-ttu-id="c9202-138">X</span><span class="sxs-lookup"><span data-stu-id="c9202-138">X</span></span>       |



 

<span data-ttu-id="c9202-139">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c9202-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="c9202-140">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c9202-140">Vertex</span></span> | <span data-ttu-id="c9202-141">Hülle</span><span class="sxs-lookup"><span data-stu-id="c9202-141">Hull</span></span> | <span data-ttu-id="c9202-142">Domain</span><span class="sxs-lookup"><span data-stu-id="c9202-142">Domain</span></span> | <span data-ttu-id="c9202-143">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c9202-143">Geometry</span></span> | <span data-ttu-id="c9202-144">Pixel</span><span class="sxs-lookup"><span data-stu-id="c9202-144">Pixel</span></span> | <span data-ttu-id="c9202-145">Compute</span><span class="sxs-lookup"><span data-stu-id="c9202-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c9202-146">X</span><span class="sxs-lookup"><span data-stu-id="c9202-146">X</span></span>      | <span data-ttu-id="c9202-147">X</span><span class="sxs-lookup"><span data-stu-id="c9202-147">X</span></span>    | <span data-ttu-id="c9202-148">X</span><span class="sxs-lookup"><span data-stu-id="c9202-148">X</span></span>      | <span data-ttu-id="c9202-149">X</span><span class="sxs-lookup"><span data-stu-id="c9202-149">X</span></span>        | <span data-ttu-id="c9202-150">X</span><span class="sxs-lookup"><span data-stu-id="c9202-150">X</span></span>     | <span data-ttu-id="c9202-151">X</span><span class="sxs-lookup"><span data-stu-id="c9202-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c9202-152">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c9202-152">Minimum Shader Model</span></span>

<span data-ttu-id="c9202-153">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c9202-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c9202-154">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c9202-154">Shader Model</span></span>                                              | <span data-ttu-id="c9202-155">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c9202-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c9202-156">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="c9202-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c9202-157">ja</span><span class="sxs-lookup"><span data-stu-id="c9202-157">yes</span></span>       |
| [<span data-ttu-id="c9202-158">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="c9202-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c9202-159">nein</span><span class="sxs-lookup"><span data-stu-id="c9202-159">no</span></span>        |
| [<span data-ttu-id="c9202-160">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="c9202-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c9202-161">nein</span><span class="sxs-lookup"><span data-stu-id="c9202-161">no</span></span>        |
| [<span data-ttu-id="c9202-162">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9202-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c9202-163">nein</span><span class="sxs-lookup"><span data-stu-id="c9202-163">no</span></span>        |
| [<span data-ttu-id="c9202-164">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9202-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c9202-165">nein</span><span class="sxs-lookup"><span data-stu-id="c9202-165">no</span></span>        |
| [<span data-ttu-id="c9202-166">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9202-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c9202-167">nein</span><span class="sxs-lookup"><span data-stu-id="c9202-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c9202-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c9202-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9202-169">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9202-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





