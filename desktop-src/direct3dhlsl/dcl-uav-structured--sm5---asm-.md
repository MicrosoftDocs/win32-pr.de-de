---
title: dcl_uav_structured (SM5-ASM)
description: Deklarieren Sie eine ungeordnete Zugriffs Ansicht (UAV) für die Verwendung durch einen Shader. | dcl_uav_structured (SM5-ASM)
ms.assetid: 40D6B8F7-8A41-4EFE-A8A3-44A646B4D43B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc02396f4837a095506e736d81ea8c00eb0669f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219210"
---
# <a name="dcl_uav_structured-sm5---asm"></a><span data-ttu-id="2c78a-104">strukturierte DCL \_ -UAV \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2c78a-104">dcl\_uav\_structured (sm5 - asm)</span></span>

<span data-ttu-id="2c78a-105">Deklarieren Sie eine ungeordnete Zugriffs Ansicht (UAV) für die Verwendung durch einen Shader.</span><span class="sxs-lookup"><span data-stu-id="2c78a-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="2c78a-106">DCL \_ UAV \_ strukturiert \[ \_ GLC \] dstuav, structbytestride</span><span class="sxs-lookup"><span data-stu-id="2c78a-106">dcl\_uav\_structured\[\_glc\] dstUAV, structByteStride</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="2c78a-107">Element</span><span class="sxs-lookup"><span data-stu-id="2c78a-107">Item</span></span>                                                                                                                                   | <span data-ttu-id="2c78a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c78a-108">Description</span></span>                                           |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="2c78a-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstuav*</span><span class="sxs-lookup"><span data-stu-id="2c78a-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/>                                         | <span data-ttu-id="2c78a-110">\[in \] der UAV.</span><span class="sxs-lookup"><span data-stu-id="2c78a-110">\[in\] The UAV.</span></span><br/>                            |
| <span data-ttu-id="2c78a-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structbytestride*</span><span class="sxs-lookup"><span data-stu-id="2c78a-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="2c78a-112">\[in \] der Größe der Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2c78a-112">\[in\] The size of the structure in bytes.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2c78a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c78a-113">Remarks</span></span>

<span data-ttu-id="2c78a-114">*dstuav* ist ein u- \# Register, das als Verweis auf eine unorderedaccessview eines strukturierten Puffers mit dem angegebenen Schritt deklariert wurde, der an die API an den UAV-Slot gebunden werden muss \# .</span><span class="sxs-lookup"><span data-stu-id="2c78a-114">*dstUAV* is a u\# register declared as a reference to an UnorderedAccessView of a structured buffer with the specified stride that must be bound to UAV slot \# at the API.</span></span>

<span data-ttu-id="2c78a-115">Der Inhalt der-Struktur hat keinen Typ. für den Arbeitsspeicher ausgeführte Vorgänge können die Daten implizit als Typ interpretieren.</span><span class="sxs-lookup"><span data-stu-id="2c78a-115">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="2c78a-116">*structbytestride* ist die Größe der Struktur in Bytes im Puffer, der deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="2c78a-116">*structByteStride* is the size of the structure in bytes in the buffer being declared.</span></span> <span data-ttu-id="2c78a-117">Dieser Wert muss größer als 0 sein.</span><span class="sxs-lookup"><span data-stu-id="2c78a-117">This value must be greater than zero.</span></span> <span data-ttu-id="2c78a-118">*structbytestride* ist vom Typ uint und muss ein Vielfaches von 4 sein.</span><span class="sxs-lookup"><span data-stu-id="2c78a-118">*structByteStride* is of type uint, and must be a multiple of 4.</span></span>

<span data-ttu-id="2c78a-119">Anweisungen, die auf eine strukturierte u verweisen \# , nehmen eine 2D-Adresse auf, bei der die erste Komponente struct auswählt \[ \] und die zweite Komponente \[ Offset innerhalb von Struktur in ausgerichteten Bytes auswählt \] .</span><span class="sxs-lookup"><span data-stu-id="2c78a-119">Instructions that reference a structured u\# take a 2D address, where the first component picks \[struct\], and the second component picks \[offset within struct, in aligned bytes\].</span></span>

<span data-ttu-id="2c78a-120">Das \_ GLC-Flag bedeutet "Global kohärent".</span><span class="sxs-lookup"><span data-stu-id="2c78a-120">The \_glc flag means for"globally coherent".</span></span> <span data-ttu-id="2c78a-121">Das Fehlen von \_ GLC bedeutet, dass die UAV im COMPUTE-Shader nur als "zusammenhängender Gruppe" oder "lokal kohärent" in einem einzelnen Pixelshader-Aufruf deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="2c78a-121">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="2c78a-122">Das \_ OPC-Flag ist der Wert für die Beibehaltung der Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="2c78a-122">The \_opc flag is the order preserving counter.</span></span> <span data-ttu-id="2c78a-123">Wenn eine UAV an Slot \# (u) gebunden ist \# , muss Sie mit dem Counter-Flag erstellt worden sein.</span><span class="sxs-lookup"><span data-stu-id="2c78a-123">It indicates that if a UAV is bound to slot \# (u\#), it must have been created with the COUNTER flag.</span></span> <span data-ttu-id="2c78a-124">Dies bedeutet, dass die Atomic- [ \_ \_ Zuordnungen von "imm Atomic](imm-atomic-alloc--sm5---asm-.md) " oder " [imm \_ Atomic \_ ](imm-atomic-consume--sm5---asm-.md) " im Shader einen Counter bearbeiten, dessen Werte im Shader als dauerhafter Verweis auf einen Speicherort in der UAV verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="2c78a-124">This means that [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) operations in the shader manipulate a counter whose values can be used in the shader as a permanent reference to a location in the UAV.</span></span> <span data-ttu-id="2c78a-125">Die Daten können nicht neu angeordnet werden, nachdem der Shader vorbei ist.</span><span class="sxs-lookup"><span data-stu-id="2c78a-125">Data cannot be reordered after the shader is over.</span></span>

<span data-ttu-id="2c78a-126">Wenn das OPC- \_ Flag nicht vorhanden ist, bedeutet dies Folgendes: Wenn der Shader "[imm \_ Atomic \_ Zuweisungs](imm-atomic-alloc--sm5---asm-.md) Anweisungen" oder " [imm \_ Atomic \_ ](imm-atomic-consume--sm5---asm-.md) using Instructions" verwendet und eine UAV an Slot \# (u) gebunden ist, muss Sie mit dem Append-Flag erstellt worden sein, das einen gegen Wert bereitstellt, der nicht garantiert, dass die Reihenfolge nach dem Aufruf des Shaders</span><span class="sxs-lookup"><span data-stu-id="2c78a-126">The absence of the \_opc flag means that if the shader uses[imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) instructions and a UAV is bound to slot \# (u), it must have been created with the APPEND flag, which provides a counter that does not guarantee order is preserved after the shader invocation.</span></span>

<span data-ttu-id="2c78a-127">Wenn das \_ OPC-Flag fehlt und der Shader keine " [imm \_ Atomic \_ Zuweisungs](imm-atomic-alloc--sm5---asm-.md) "-oder " [imm \_ Atomic \_ ](imm-atomic-consume--sm5---asm-.md) using"-Anweisungen enthält, ist es zulässig, dass ein an Slot (u) gebundenes UAV \# mit dem Counter-Flag erstellt wurde (der Counter wird von diesem Shader nicht verwendet), ohne Flag (kein Counter), aber nicht mit dem Append-Flag.</span><span class="sxs-lookup"><span data-stu-id="2c78a-127">If the \_opc flag is absent and the shader does not contain [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) instructions, a UAV bound to slot \# (u) is permitted to have been created with the COUNTER flag (the counter will go unused by this shader), no flag (no counter), but not with the APPEND flag.</span></span>

> [!Note]  
> <span data-ttu-id="2c78a-128">CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen die **strukturierte DCL- \_ TGSM \_**, aber nicht die [DCL- \_ TGSM- \_ Rohdaten](dcl-tgsm-raw--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="2c78a-128">cs\_4\_0 and cs\_4\_1 supports **dcl\_tgsm\_structured**, but not [dcl\_tgsm\_raw](dcl-tgsm-raw--sm5---asm-.md).</span></span>

 

<span data-ttu-id="2c78a-129">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="2c78a-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2c78a-130">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="2c78a-130">Vertex</span></span> | <span data-ttu-id="2c78a-131">Hülle</span><span class="sxs-lookup"><span data-stu-id="2c78a-131">Hull</span></span> | <span data-ttu-id="2c78a-132">Domain</span><span class="sxs-lookup"><span data-stu-id="2c78a-132">Domain</span></span> | <span data-ttu-id="2c78a-133">Geometrie</span><span class="sxs-lookup"><span data-stu-id="2c78a-133">Geometry</span></span> | <span data-ttu-id="2c78a-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="2c78a-134">Pixel</span></span> | <span data-ttu-id="2c78a-135">Compute</span><span class="sxs-lookup"><span data-stu-id="2c78a-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2c78a-136">X</span><span class="sxs-lookup"><span data-stu-id="2c78a-136">X</span></span>     | <span data-ttu-id="2c78a-137">X</span><span class="sxs-lookup"><span data-stu-id="2c78a-137">X</span></span>       |



 

<span data-ttu-id="2c78a-138">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="2c78a-138">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="2c78a-139">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="2c78a-139">Vertex</span></span> | <span data-ttu-id="2c78a-140">Hülle</span><span class="sxs-lookup"><span data-stu-id="2c78a-140">Hull</span></span> | <span data-ttu-id="2c78a-141">Domain</span><span class="sxs-lookup"><span data-stu-id="2c78a-141">Domain</span></span> | <span data-ttu-id="2c78a-142">Geometrie</span><span class="sxs-lookup"><span data-stu-id="2c78a-142">Geometry</span></span> | <span data-ttu-id="2c78a-143">Pixel</span><span class="sxs-lookup"><span data-stu-id="2c78a-143">Pixel</span></span> | <span data-ttu-id="2c78a-144">Compute</span><span class="sxs-lookup"><span data-stu-id="2c78a-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2c78a-145">X</span><span class="sxs-lookup"><span data-stu-id="2c78a-145">X</span></span>      | <span data-ttu-id="2c78a-146">X</span><span class="sxs-lookup"><span data-stu-id="2c78a-146">X</span></span>    | <span data-ttu-id="2c78a-147">X</span><span class="sxs-lookup"><span data-stu-id="2c78a-147">X</span></span>      | <span data-ttu-id="2c78a-148">X</span><span class="sxs-lookup"><span data-stu-id="2c78a-148">X</span></span>        | <span data-ttu-id="2c78a-149">X</span><span class="sxs-lookup"><span data-stu-id="2c78a-149">X</span></span>     | <span data-ttu-id="2c78a-150">X</span><span class="sxs-lookup"><span data-stu-id="2c78a-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2c78a-151">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="2c78a-151">Minimum Shader Model</span></span>

<span data-ttu-id="2c78a-152">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="2c78a-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2c78a-153">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="2c78a-153">Shader Model</span></span>                                              | <span data-ttu-id="2c78a-154">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="2c78a-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2c78a-155">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="2c78a-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2c78a-156">ja</span><span class="sxs-lookup"><span data-stu-id="2c78a-156">yes</span></span>       |
| [<span data-ttu-id="2c78a-157">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="2c78a-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2c78a-158">nein</span><span class="sxs-lookup"><span data-stu-id="2c78a-158">no</span></span>        |
| [<span data-ttu-id="2c78a-159">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="2c78a-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2c78a-160">nein</span><span class="sxs-lookup"><span data-stu-id="2c78a-160">no</span></span>        |
| [<span data-ttu-id="2c78a-161">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c78a-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2c78a-162">nein</span><span class="sxs-lookup"><span data-stu-id="2c78a-162">no</span></span>        |
| [<span data-ttu-id="2c78a-163">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c78a-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2c78a-164">nein</span><span class="sxs-lookup"><span data-stu-id="2c78a-164">no</span></span>        |
| [<span data-ttu-id="2c78a-165">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c78a-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2c78a-166">nein</span><span class="sxs-lookup"><span data-stu-id="2c78a-166">no</span></span>        |



 

> [!Note]  
> <span data-ttu-id="2c78a-167">Diese Anweisung wird in CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2c78a-167">This instruction is supported in cs\_4\_0 and cs\_4\_1.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2c78a-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2c78a-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c78a-169">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c78a-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





