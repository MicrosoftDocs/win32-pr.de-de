---
title: atomic_umax (SM5-ASM)
description: Atomarische Ganzzahl ohne Vorzeichen, maximal im Arbeitsspeicher.
ms.assetid: 7255B67A-37BE-443A-BDF2-A1D4A56C5E11
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 578a96379ad8904459cbfd47ef87ba4256e5fd8d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857808"
---
# <a name="atomic_umax-sm5---asm"></a><span data-ttu-id="877d7-103">atomarische \_ Umax (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="877d7-103">atomic\_umax (sm5 - asm)</span></span>

<span data-ttu-id="877d7-104">Atomarische Ganzzahl ohne Vorzeichen, maximal im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="877d7-104">Atomic unsigned integer maximum to memory.</span></span>



| <span data-ttu-id="877d7-105">Atomic \_ Umax DST, dstaddress \[ . Swizzle \] , src0 \[ . Select- \_ Komponente\]</span><span class="sxs-lookup"><span data-stu-id="877d7-105">atomic\_umax dst, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|----------------------------------------------------------------------|



 



| <span data-ttu-id="877d7-106">Element</span><span class="sxs-lookup"><span data-stu-id="877d7-106">Item</span></span>                                                                                                           | <span data-ttu-id="877d7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="877d7-107">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="877d7-108"><span id="dst"></span><span id="DST"></span>*DST*</span><span class="sxs-lookup"><span data-stu-id="877d7-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="877d7-109">\[in \] den Komponenten, die mit *src0* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="877d7-109">\[in\] The components to compare to *src0*.</span></span> <span data-ttu-id="877d7-110">Dieser Wert muss eine ungeordnete Zugriffs Ansicht (UAV) sein \# .</span><span class="sxs-lookup"><span data-stu-id="877d7-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="877d7-111">Im COMPUTE-Shader kann es sich auch um einen Thread Gruppen-Shared Memory (g \# ) handeln.</span><span class="sxs-lookup"><span data-stu-id="877d7-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="877d7-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstaddress*</span><span class="sxs-lookup"><span data-stu-id="877d7-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="877d7-113">\[in \] der Speicheradresse.</span><span class="sxs-lookup"><span data-stu-id="877d7-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                   |
| <span data-ttu-id="877d7-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="877d7-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="877d7-115">\[in \] den Komponenten, die mit *DST* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="877d7-115">\[in\] The components to compare to *dst*.</span></span><br/>                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="877d7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="877d7-116">Remarks</span></span>

<span data-ttu-id="877d7-117">Diese Anweisung führt eine einzelne Komponente mit einer Länge von 32 Bit ohne Vorzeichen des Operanden *src0* in *DST* um 32 Bit pro Komponenten Adresse *dstaddress* aus, die atomisch ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="877d7-117">This instruction performs a single component 32-bit unsigned maximum of operand *src0* into *dst* at 32-bit per component address *dstAddress*, performed atomically.</span></span>

<span data-ttu-id="877d7-118">Die Anzahl der Komponenten, die von der Adresse entnommen werden, hängt von der Dimensionalität der DST u \# oder g ab \# .</span><span class="sxs-lookup"><span data-stu-id="877d7-118">The number of components taken from the address is determined by the dimensionality of dst u\# or g\#.</span></span>

<span data-ttu-id="877d7-119">Wenn *DST* eine u ist \# , kann Sie als RAW, typisiert oder strukturiert deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="877d7-119">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="877d7-120">Wenn Sie eingegeben wird, muss Sie als uint/Sint mit dem gebundenen Ressourcen Format "R32 \_ uint/ \_ Sint" deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="877d7-120">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="877d7-121">Wenn *DST* g ist \# , muss es als RAW oder strukturiert deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="877d7-121">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="877d7-122">An den Shader wird nichts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="877d7-122">Nothing is returned to the shader.</span></span>

<span data-ttu-id="877d7-123">Wenn der Shader-Aufruf inaktiv ist, z. b. wenn das Pixel bereits in seiner Ausführung verworfen wurde, oder wenn ein Pixel-/Beispielaufruf nur vorhanden ist, um als Hilfsobjekt für ein reales Pixel/Beispiel für Ableitungen zu dienen, ändert diese Anweisung den *DST* -Arbeitsspeicher überhaupt nicht (im Hintergrund).</span><span class="sxs-lookup"><span data-stu-id="877d7-123">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or if a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="877d7-124">Die Out-of-Bounds-Adressierung in u \# bewirkt, dass nichts in den Arbeitsspeicher geschrieben wird, außer wenn die u \# strukturiert ist und der Byte Offset in die Struktur (zweite Komponente der Adresse) den Zugriff außerhalb der Grenzen verursacht, dann wird der gesamte Inhalt der UAV nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="877d7-124">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="877d7-125">Die Begrenzung auf g \# (die Begrenzungen dieses bestimmten g im \# Gegensatz zum gesamten Shared Memory) bewirkt, dass der gesamte Inhalt des gesamten freigegebenen Speichers undefiniert wird.</span><span class="sxs-lookup"><span data-stu-id="877d7-125">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="877d7-126">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="877d7-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="877d7-127">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="877d7-127">Vertex</span></span> | <span data-ttu-id="877d7-128">Hülle</span><span class="sxs-lookup"><span data-stu-id="877d7-128">Hull</span></span> | <span data-ttu-id="877d7-129">Domain</span><span class="sxs-lookup"><span data-stu-id="877d7-129">Domain</span></span> | <span data-ttu-id="877d7-130">Geometrie</span><span class="sxs-lookup"><span data-stu-id="877d7-130">Geometry</span></span> | <span data-ttu-id="877d7-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="877d7-131">Pixel</span></span> | <span data-ttu-id="877d7-132">Compute</span><span class="sxs-lookup"><span data-stu-id="877d7-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="877d7-133">X</span><span class="sxs-lookup"><span data-stu-id="877d7-133">X</span></span>     | <span data-ttu-id="877d7-134">X</span><span class="sxs-lookup"><span data-stu-id="877d7-134">X</span></span>       |



 

<span data-ttu-id="877d7-135">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="877d7-135">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="877d7-136">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="877d7-136">Vertex</span></span> | <span data-ttu-id="877d7-137">Hülle</span><span class="sxs-lookup"><span data-stu-id="877d7-137">Hull</span></span> | <span data-ttu-id="877d7-138">Domain</span><span class="sxs-lookup"><span data-stu-id="877d7-138">Domain</span></span> | <span data-ttu-id="877d7-139">Geometrie</span><span class="sxs-lookup"><span data-stu-id="877d7-139">Geometry</span></span> | <span data-ttu-id="877d7-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="877d7-140">Pixel</span></span> | <span data-ttu-id="877d7-141">Compute</span><span class="sxs-lookup"><span data-stu-id="877d7-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="877d7-142">X</span><span class="sxs-lookup"><span data-stu-id="877d7-142">X</span></span>      | <span data-ttu-id="877d7-143">X</span><span class="sxs-lookup"><span data-stu-id="877d7-143">X</span></span>    | <span data-ttu-id="877d7-144">X</span><span class="sxs-lookup"><span data-stu-id="877d7-144">X</span></span>      | <span data-ttu-id="877d7-145">X</span><span class="sxs-lookup"><span data-stu-id="877d7-145">X</span></span>        | <span data-ttu-id="877d7-146">X</span><span class="sxs-lookup"><span data-stu-id="877d7-146">X</span></span>     | <span data-ttu-id="877d7-147">X</span><span class="sxs-lookup"><span data-stu-id="877d7-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="877d7-148">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="877d7-148">Minimum Shader Model</span></span>

<span data-ttu-id="877d7-149">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="877d7-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="877d7-150">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="877d7-150">Shader Model</span></span>                                              | <span data-ttu-id="877d7-151">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="877d7-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="877d7-152">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="877d7-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="877d7-153">ja</span><span class="sxs-lookup"><span data-stu-id="877d7-153">yes</span></span>       |
| [<span data-ttu-id="877d7-154">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="877d7-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="877d7-155">nein</span><span class="sxs-lookup"><span data-stu-id="877d7-155">no</span></span>        |
| [<span data-ttu-id="877d7-156">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="877d7-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="877d7-157">nein</span><span class="sxs-lookup"><span data-stu-id="877d7-157">no</span></span>        |
| [<span data-ttu-id="877d7-158">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="877d7-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="877d7-159">nein</span><span class="sxs-lookup"><span data-stu-id="877d7-159">no</span></span>        |
| [<span data-ttu-id="877d7-160">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="877d7-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="877d7-161">nein</span><span class="sxs-lookup"><span data-stu-id="877d7-161">no</span></span>        |
| [<span data-ttu-id="877d7-162">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="877d7-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="877d7-163">nein</span><span class="sxs-lookup"><span data-stu-id="877d7-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="877d7-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="877d7-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="877d7-165">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="877d7-165">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





