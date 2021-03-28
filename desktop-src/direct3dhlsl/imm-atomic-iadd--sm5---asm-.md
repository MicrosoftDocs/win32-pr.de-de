---
title: imm_atomic_iadd (SM5-ASM)
description: Unmittelbare atomarische Ganzzahl wird dem Arbeitsspeicher hinzugefügt. Gibt den Wert im Arbeitsspeicher vor dem Hinzufügen zurück.
ms.assetid: 24136B4C-D37C-4449-A318-57145BB8D8E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2695e23707fb61cd576748e2e83829cd7dc65259
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389568"
---
# <a name="imm_atomic_iadd-sm5---asm"></a><span data-ttu-id="1b0f5-104">imm \_ Atomic \_ IAdd (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1b0f5-104">imm\_atomic\_iadd (sm5 - asm)</span></span>

<span data-ttu-id="1b0f5-105">Unmittelbare atomarische Ganzzahl wird dem Arbeitsspeicher hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-105">Immediate atomic integer add to memory.</span></span> <span data-ttu-id="1b0f5-106">Gibt den Wert im Arbeitsspeicher vor dem Hinzufügen zurück.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-106">Returns the value in memory before the add.</span></span>



| <span data-ttu-id="1b0f5-107">imm \_ Atomic \_ IAdd dst0 \[ . Single \_ Component \_ mask \] , dST1, dstaddress \[ . Swizzle \] , src0 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="1b0f5-107">imm\_atomic\_iadd dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="1b0f5-108">Element</span><span class="sxs-lookup"><span data-stu-id="1b0f5-108">Item</span></span>                                                                                                           | <span data-ttu-id="1b0f5-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b0f5-109">Description</span></span>                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b0f5-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="1b0f5-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="1b0f5-111">\[in \] enthält den Wert in *dST1* vor dem Schreibvorgang.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-111">\[in\] Contains the value in *dst1* before the write.</span></span> <br/>                                                                           |
| <span data-ttu-id="1b0f5-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="1b0f5-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="1b0f5-113">Dieser Wert muss eine ungeordnete Zugriffs Ansicht (UAV) sein \# .</span><span class="sxs-lookup"><span data-stu-id="1b0f5-113">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="1b0f5-114">Im COMPUTE-Shader kann es sich auch um einen Thread Gruppen-Shared Memory (g \# ) handeln.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-114">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="1b0f5-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstaddress*</span><span class="sxs-lookup"><span data-stu-id="1b0f5-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="1b0f5-116">\[in \] der Speicher-nAddress.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-116">\[in\] The memory naddress.</span></span><br/>                                                                                                      |
| <span data-ttu-id="1b0f5-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1b0f5-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="1b0f5-118">\[in \] dem Wert, der *dST1* hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-118">\[in\] The value to add to *dst1*.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="1b0f5-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b0f5-119">Remarks</span></span>

<span data-ttu-id="1b0f5-120">Diese Anweisung führt eine einzelne Komponente 32-Bit-Ganzzahl-Add of Operand *src0* with *dST1* at 32 Bit pro Component Address *dstaddress* aus.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-120">This instruction performs a single component 32-bit integer add of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span> <span data-ttu-id="1b0f5-121">Das Signieren ist nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-121">It is insensitive to sign.</span></span>

<span data-ttu-id="1b0f5-122">Wenn *dST1* eine u ist \# , wurde Sie möglicherweise als RAW, typisiert oder strukturiert deklariert.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-122">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="1b0f5-123">Wenn Sie eingegeben wird, muss Sie als uint/Sint mit dem gebundenen Ressourcen Format "R32 \_ uint/ \_ Sint" deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-123">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="1b0f5-124">Wenn *dST1* den Wert g \# hat, muss er als RAW oder strukturiert deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-124">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="1b0f5-125">Der Wert im *dST1* -Arbeitsspeicher, bevor die Addition an *dst0* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-125">The value in *dst1* memory before addition is returned to *dst0*.</span></span>

<span data-ttu-id="1b0f5-126">Die Anzahl der Komponenten, die von der Adresse entnommen werden, wird durch die Dimensionalität von *dST1* bestimmt.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-126">The number of components taken from the address is determined by the dimensionality of *dst1*.</span></span>

<span data-ttu-id="1b0f5-127">Der gesamte Vorgang wird atomisch ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-127">The entire operation is performed atomically.</span></span>

<span data-ttu-id="1b0f5-128">Wenn der Shader-Aufruf inaktiv ist, z. b. wenn das Pixel zuvor in seiner Ausführung verworfen wurde oder ein Pixel-/Beispielaufruf nur vorhanden ist, um als Hilfsobjekt/Stichprobe für Ableitungen zu dienen, ändert diese Anweisung den *dST1* -Arbeitsspeicher nicht, und der zurückgegebene Wert ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-128">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="1b0f5-129">Die Out-of-Bounds-Adressierung in u \# bewirkt, dass nichts in den Arbeitsspeicher geschrieben wird, außer wenn die u \# strukturiert ist und der Byte Offset in die Struktur (zweite Komponente der Adresse) den Zugriff außerhalb der Grenzen verursacht, dann wird der gesamte Inhalt der UAV nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-129">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="1b0f5-130">Die Adressierung für "u" \# oder "g" bewirkt, \# dass ein nicht definiertes Ergebnis an den Shader in *dst0* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-130">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="1b0f5-131">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="1b0f5-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1b0f5-132">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="1b0f5-132">Vertex</span></span> | <span data-ttu-id="1b0f5-133">Hülle</span><span class="sxs-lookup"><span data-stu-id="1b0f5-133">Hull</span></span> | <span data-ttu-id="1b0f5-134">Domain</span><span class="sxs-lookup"><span data-stu-id="1b0f5-134">Domain</span></span> | <span data-ttu-id="1b0f5-135">Geometrie</span><span class="sxs-lookup"><span data-stu-id="1b0f5-135">Geometry</span></span> | <span data-ttu-id="1b0f5-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="1b0f5-136">Pixel</span></span> | <span data-ttu-id="1b0f5-137">Compute</span><span class="sxs-lookup"><span data-stu-id="1b0f5-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1b0f5-138">X</span><span class="sxs-lookup"><span data-stu-id="1b0f5-138">X</span></span>     | <span data-ttu-id="1b0f5-139">X</span><span class="sxs-lookup"><span data-stu-id="1b0f5-139">X</span></span>       |



 

<span data-ttu-id="1b0f5-140">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="1b0f5-141">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="1b0f5-141">Vertex</span></span> | <span data-ttu-id="1b0f5-142">Hülle</span><span class="sxs-lookup"><span data-stu-id="1b0f5-142">Hull</span></span> | <span data-ttu-id="1b0f5-143">Domain</span><span class="sxs-lookup"><span data-stu-id="1b0f5-143">Domain</span></span> | <span data-ttu-id="1b0f5-144">Geometrie</span><span class="sxs-lookup"><span data-stu-id="1b0f5-144">Geometry</span></span> | <span data-ttu-id="1b0f5-145">Pixel</span><span class="sxs-lookup"><span data-stu-id="1b0f5-145">Pixel</span></span> | <span data-ttu-id="1b0f5-146">Compute</span><span class="sxs-lookup"><span data-stu-id="1b0f5-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1b0f5-147">X</span><span class="sxs-lookup"><span data-stu-id="1b0f5-147">X</span></span>      | <span data-ttu-id="1b0f5-148">X</span><span class="sxs-lookup"><span data-stu-id="1b0f5-148">X</span></span>    | <span data-ttu-id="1b0f5-149">X</span><span class="sxs-lookup"><span data-stu-id="1b0f5-149">X</span></span>      | <span data-ttu-id="1b0f5-150">X</span><span class="sxs-lookup"><span data-stu-id="1b0f5-150">X</span></span>        | <span data-ttu-id="1b0f5-151">X</span><span class="sxs-lookup"><span data-stu-id="1b0f5-151">X</span></span>     | <span data-ttu-id="1b0f5-152">X</span><span class="sxs-lookup"><span data-stu-id="1b0f5-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1b0f5-153">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="1b0f5-153">Minimum Shader Model</span></span>

<span data-ttu-id="1b0f5-154">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1b0f5-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1b0f5-155">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="1b0f5-155">Shader Model</span></span>                                              | <span data-ttu-id="1b0f5-156">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="1b0f5-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1b0f5-157">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="1b0f5-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1b0f5-158">ja</span><span class="sxs-lookup"><span data-stu-id="1b0f5-158">yes</span></span>       |
| [<span data-ttu-id="1b0f5-159">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="1b0f5-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1b0f5-160">nein</span><span class="sxs-lookup"><span data-stu-id="1b0f5-160">no</span></span>        |
| [<span data-ttu-id="1b0f5-161">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="1b0f5-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1b0f5-162">nein</span><span class="sxs-lookup"><span data-stu-id="1b0f5-162">no</span></span>        |
| [<span data-ttu-id="1b0f5-163">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b0f5-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1b0f5-164">nein</span><span class="sxs-lookup"><span data-stu-id="1b0f5-164">no</span></span>        |
| [<span data-ttu-id="1b0f5-165">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b0f5-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1b0f5-166">nein</span><span class="sxs-lookup"><span data-stu-id="1b0f5-166">no</span></span>        |
| [<span data-ttu-id="1b0f5-167">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b0f5-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1b0f5-168">nein</span><span class="sxs-lookup"><span data-stu-id="1b0f5-168">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1b0f5-169">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1b0f5-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b0f5-170">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b0f5-170">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





