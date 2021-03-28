---
title: atomic_iadd (SM5-ASM)
description: Atomarische Ganzzahl zu Arbeitsspeicher hinzufügen.
ms.assetid: 093C7FA5-41BF-4BDD-A35D-1AACE8CB9B5C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6a8652d4e29aae9f32a84f7a4e4d477abd54b7c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313733"
---
# <a name="atomic_iadd-sm5---asm"></a><span data-ttu-id="6cb9f-103">Atomic \_ IAdd (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6cb9f-103">atomic\_iadd (sm5 - asm)</span></span>

<span data-ttu-id="6cb9f-104">Atomarische Ganzzahl zu Arbeitsspeicher hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-104">Atomic integer add to memory.</span></span>



| <span data-ttu-id="6cb9f-105">Atomic \_ IAdd DST, dstaddress \[ . Swizzle \] , src0 \[ . Select- \_ Komponente\]</span><span class="sxs-lookup"><span data-stu-id="6cb9f-105">atomic\_iadd dst, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|----------------------------------------------------------------------|



 



| <span data-ttu-id="6cb9f-106">Element</span><span class="sxs-lookup"><span data-stu-id="6cb9f-106">Item</span></span>                                                                                                           | <span data-ttu-id="6cb9f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6cb9f-107">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb9f-108"><span id="dst"></span><span id="DST"></span>*DST*</span><span class="sxs-lookup"><span data-stu-id="6cb9f-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="6cb9f-109">\[in \] den Komponenten, die mit *src0* hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-109">\[in\] The components to add with *src0*.</span></span> <span data-ttu-id="6cb9f-110">Dieser Wert muss eine ungeordnete Zugriffs Ansicht (UAV) sein \# .</span><span class="sxs-lookup"><span data-stu-id="6cb9f-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="6cb9f-111">Im COMPUTE-Shader kann es sich auch um einen Thread Gruppen-Shared Memory (g \# ) handeln.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="6cb9f-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstaddress*</span><span class="sxs-lookup"><span data-stu-id="6cb9f-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="6cb9f-113">\[in \] der Speicheradresse.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                 |
| <span data-ttu-id="6cb9f-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6cb9f-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="6cb9f-115">\[in \] den Komponenten, die zu *DST* hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-115">\[in\] The components to add to *dst*.</span></span><br/>                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="6cb9f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6cb9f-116">Remarks</span></span>

<span data-ttu-id="6cb9f-117">Diese Anweisung führt eine einzelne Komponente 32-Bit-Ganzzahl von Operanden *src0* in *DST* um 32 Bit pro Komponenten Adresse *dstaddress* aus, die atomisch ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-117">This instruction performs a single component 32-bit integer add of operand *src0* into *dst* at 32-bit per component address *dstAddress*, performed atomically.</span></span> <span data-ttu-id="6cb9f-118">Diese Anweisung kann nicht signiert werden.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-118">This instruction is insensitive to sign.</span></span>

<span data-ttu-id="6cb9f-119">Die Anzahl der Komponenten, die von der Adresse entnommen werden, hängt von der Dimensionalität der *DST* u \# oder g ab \# .</span><span class="sxs-lookup"><span data-stu-id="6cb9f-119">The number of components taken from the address is determined by the dimensionality of *dst* u\# or g\#.</span></span>

<span data-ttu-id="6cb9f-120">Wenn *DST* eine u ist \# , kann Sie als RAW, typisiert oder strukturiert deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-120">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="6cb9f-121">Wenn Sie eingegeben wird, muss Sie als uint/Sint mit dem gebundenen Ressourcen Format "R32 \_ uint/ \_ Sint" deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-121">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="6cb9f-122">Wenn *DST* g ist \# , muss es als RAW oder strukturiert deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-122">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="6cb9f-123">An den Shader wird nichts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-123">Nothing is returned to the shader.</span></span>

<span data-ttu-id="6cb9f-124">Wenn der Shader-Aufruf inaktiv ist, z. b. wenn das Pixel bereits in seiner Ausführung verworfen wurde, oder wenn ein Pixel-/Beispielaufruf nur vorhanden ist, um als Hilfsobjekt für ein reales Pixel/Beispiel für Ableitungen zu dienen, ändert diese Anweisung den *DST* -Arbeitsspeicher überhaupt nicht (im Hintergrund).</span><span class="sxs-lookup"><span data-stu-id="6cb9f-124">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or if a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="6cb9f-125">Die Out-of-Bounds-Adressierung in u \# bewirkt, dass nichts in den Arbeitsspeicher geschrieben wird, außer wenn die u \# strukturiert ist und der Byte Offset in die Struktur (zweite Komponente der Adresse) den Zugriff außerhalb der Grenzen verursacht, dann wird der gesamte Inhalt der UAV nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-125">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="6cb9f-126">Die Begrenzung auf g \# (die Begrenzungen dieses bestimmten g im \# Gegensatz zum gesamten Shared Memory) bewirkt, dass der gesamte Inhalt des gesamten freigegebenen Speichers undefiniert wird.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-126">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="6cb9f-127">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="6cb9f-127">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6cb9f-128">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="6cb9f-128">Vertex</span></span> | <span data-ttu-id="6cb9f-129">Hülle</span><span class="sxs-lookup"><span data-stu-id="6cb9f-129">Hull</span></span> | <span data-ttu-id="6cb9f-130">Domain</span><span class="sxs-lookup"><span data-stu-id="6cb9f-130">Domain</span></span> | <span data-ttu-id="6cb9f-131">Geometrie</span><span class="sxs-lookup"><span data-stu-id="6cb9f-131">Geometry</span></span> | <span data-ttu-id="6cb9f-132">Pixel</span><span class="sxs-lookup"><span data-stu-id="6cb9f-132">Pixel</span></span> | <span data-ttu-id="6cb9f-133">Compute</span><span class="sxs-lookup"><span data-stu-id="6cb9f-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6cb9f-134">X</span><span class="sxs-lookup"><span data-stu-id="6cb9f-134">X</span></span>     | <span data-ttu-id="6cb9f-135">X</span><span class="sxs-lookup"><span data-stu-id="6cb9f-135">X</span></span>       |



 

<span data-ttu-id="6cb9f-136">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-136">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="6cb9f-137">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="6cb9f-137">Vertex</span></span> | <span data-ttu-id="6cb9f-138">Hülle</span><span class="sxs-lookup"><span data-stu-id="6cb9f-138">Hull</span></span> | <span data-ttu-id="6cb9f-139">Domain</span><span class="sxs-lookup"><span data-stu-id="6cb9f-139">Domain</span></span> | <span data-ttu-id="6cb9f-140">Geometrie</span><span class="sxs-lookup"><span data-stu-id="6cb9f-140">Geometry</span></span> | <span data-ttu-id="6cb9f-141">Pixel</span><span class="sxs-lookup"><span data-stu-id="6cb9f-141">Pixel</span></span> | <span data-ttu-id="6cb9f-142">Compute</span><span class="sxs-lookup"><span data-stu-id="6cb9f-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6cb9f-143">X</span><span class="sxs-lookup"><span data-stu-id="6cb9f-143">X</span></span>      | <span data-ttu-id="6cb9f-144">X</span><span class="sxs-lookup"><span data-stu-id="6cb9f-144">X</span></span>    | <span data-ttu-id="6cb9f-145">X</span><span class="sxs-lookup"><span data-stu-id="6cb9f-145">X</span></span>      | <span data-ttu-id="6cb9f-146">X</span><span class="sxs-lookup"><span data-stu-id="6cb9f-146">X</span></span>        | <span data-ttu-id="6cb9f-147">X</span><span class="sxs-lookup"><span data-stu-id="6cb9f-147">X</span></span>     | <span data-ttu-id="6cb9f-148">X</span><span class="sxs-lookup"><span data-stu-id="6cb9f-148">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6cb9f-149">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="6cb9f-149">Minimum Shader Model</span></span>

<span data-ttu-id="6cb9f-150">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="6cb9f-150">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6cb9f-151">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="6cb9f-151">Shader Model</span></span>                                              | <span data-ttu-id="6cb9f-152">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="6cb9f-152">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6cb9f-153">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="6cb9f-153">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6cb9f-154">ja</span><span class="sxs-lookup"><span data-stu-id="6cb9f-154">yes</span></span>       |
| [<span data-ttu-id="6cb9f-155">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="6cb9f-155">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6cb9f-156">nein</span><span class="sxs-lookup"><span data-stu-id="6cb9f-156">no</span></span>        |
| [<span data-ttu-id="6cb9f-157">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="6cb9f-157">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6cb9f-158">nein</span><span class="sxs-lookup"><span data-stu-id="6cb9f-158">no</span></span>        |
| [<span data-ttu-id="6cb9f-159">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6cb9f-159">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6cb9f-160">nein</span><span class="sxs-lookup"><span data-stu-id="6cb9f-160">no</span></span>        |
| [<span data-ttu-id="6cb9f-161">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6cb9f-161">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6cb9f-162">nein</span><span class="sxs-lookup"><span data-stu-id="6cb9f-162">no</span></span>        |
| [<span data-ttu-id="6cb9f-163">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6cb9f-163">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6cb9f-164">nein</span><span class="sxs-lookup"><span data-stu-id="6cb9f-164">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6cb9f-165">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6cb9f-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cb9f-166">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6cb9f-166">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





