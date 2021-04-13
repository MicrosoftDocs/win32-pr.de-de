---
title: ld_structured (SM5-ASM)
description: Zufälliger Lesezugriff auf 1-4 32-Bit-Komponenten aus einem strukturierten Puffer.
ms.assetid: ED572B76-FF6C-405E-9110-4B12AD5E5AE6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a34bafdcfbe0658723dd83d62507e255ff4bfa
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389556"
---
# <a name="ld_structured-sm5---asm"></a><span data-ttu-id="b4fe3-103">LD \_ strukturiert (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="b4fe3-103">ld\_structured (sm5 - asm)</span></span>

<span data-ttu-id="b4fe3-104">Zufälliger Lesezugriff auf 1-4 32-Bit-Komponenten aus einem strukturierten Puffer.</span><span class="sxs-lookup"><span data-stu-id="b4fe3-104">Random-access read of 1-4 32bit components from a structured buffer.</span></span>



| <span data-ttu-id="b4fe3-105">: LD \_ strukturiert dst0 \[ . mask \] , srcaddress \[ . Select \_ Component \] , srcbyteoffset \[ . Select \_ Component \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="b4fe3-105">: ld\_structured dst0\[.mask\], srcAddress\[.select\_component\], srcByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="b4fe3-106">Element</span><span class="sxs-lookup"><span data-stu-id="b4fe3-106">Item</span></span>                                                                                                                       | <span data-ttu-id="b4fe3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4fe3-107">Description</span></span>                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4fe3-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="b4fe3-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="b4fe3-109">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="b4fe3-109">\[in\] The address of the results of the operation.</span></span><br/>                                                                                             |
| <span data-ttu-id="b4fe3-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*</span><span class="sxs-lookup"><span data-stu-id="b4fe3-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>             | <span data-ttu-id="b4fe3-111">\[in \] gibt den Index der zu lesenden-Struktur an.</span><span class="sxs-lookup"><span data-stu-id="b4fe3-111">\[in\] Specifies the index of the structure to read.</span></span><br/>                                                                                            |
| <span data-ttu-id="b4fe3-112"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcbyteoffset*</span><span class="sxs-lookup"><span data-stu-id="b4fe3-112"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span></span><br/> | <span data-ttu-id="b4fe3-113">\[in \] gibt den Byte Offset in der-Struktur an, ab dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4fe3-113">\[in\] Specifies the byte offset in the structure to start reading from.</span></span> <br/>                                                                       |
| <span data-ttu-id="b4fe3-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b4fe3-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="b4fe3-115">Der Puffer, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4fe3-115">The buffer to read from.</span></span> <span data-ttu-id="b4fe3-116">Dieser Parameter muss ein SRV (t \# ), UAV (u \# ) sein.</span><span class="sxs-lookup"><span data-stu-id="b4fe3-116">This parameter must be a SRV (t\#), UAV (u\#).</span></span> <span data-ttu-id="b4fe3-117">Im COMPUTE-Shader kann es sich auch um einen Thread Gruppen-Shared Memory (g \# ) handeln.</span><span class="sxs-lookup"><span data-stu-id="b4fe3-117">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="b4fe3-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4fe3-118">Remarks</span></span>

<span data-ttu-id="b4fe3-119">Die aus der-Struktur gelesenen Daten entsprechen dem folgenden Pseudocode: wobei der Offset, die Adresse, der Zeiger auf den Pufferinhalt, der Schritt der Quelle und die Daten linear gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="b4fe3-119">The data read from the structure is equivalent to the following pseudocode: where we have the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;         // from SRV or UAV
                    UINT BufferStride;            // from base resource
                    UINT srcAddress, srcByteOffset;   // from source registers
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + BufferStride * srcByteOffset
                                + srcOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

<span data-ttu-id="b4fe3-120">Dieser Pseudo Code zeigt, wie der Vorgang funktioniert, aber die tatsächlichen Daten müssen nicht linear gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b4fe3-120">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="b4fe3-121">Wenn die Daten nicht linear gespeichert werden, muss die tatsächliche Operation der Anweisung mit dem Verhalten des obigen Vorgangs identisch sein.</span><span class="sxs-lookup"><span data-stu-id="b4fe3-121">If the data is not stored linearly, the actual operation of the instruction needs to match the behavior of the above operation.</span></span>

<span data-ttu-id="b4fe3-122">Die Out-of-Bounds-Adressierung für die u- \# /t \# einer bestimmten 32-Bit-Komponente gibt 0 für diese Komponente zurück. mit Ausnahme von *srcbyteoffset* und Swizzle, was den Zugriff auf Sie \# /t verursacht \# , ist der zurückgegebene Wert für alle Komponenten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="b4fe3-122">Out of bounds addressing on u\#/t\# of any given 32-bit component returns 0 for that component, except if *srcByteOffset*, plus swizzle is what causes out of bounds access to u\#/t\#, the returned value for all component(s) is undefined.</span></span>

<span data-ttu-id="b4fe3-123">Die Adressierung auf g \# (die Begrenzungen dieses bestimmten g \# , im Gegensatz zum gesamten Shared Memory) für eine bestimmte 32-Bit-Komponente gibt ein nicht definiertes Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="b4fe3-123">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component returns an undefined result.</span></span>

<span data-ttu-id="b4fe3-124">*srcbyteoffset* ist ein separates Argument von *srcaddress* , da es sich häufig um einen Literalwert handelt.</span><span class="sxs-lookup"><span data-stu-id="b4fe3-124">*srcByteOffset* is a separate argument from *srcAddress* because it is commonly a literal.</span></span> <span data-ttu-id="b4fe3-125">Diese Parameter Trennung wurde nicht für Atomics in strukturiertem Arbeitsspeicher durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4fe3-125">This parameter separation has not been done for atomics on structured memory.</span></span>

<span data-ttu-id="b4fe3-126">CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung für UAV, SRV und TGSM.</span><span class="sxs-lookup"><span data-stu-id="b4fe3-126">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV, and TGSM.</span></span>

<span data-ttu-id="b4fe3-127">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="b4fe3-127">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b4fe3-128">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="b4fe3-128">Vertex</span></span> | <span data-ttu-id="b4fe3-129">Hülle</span><span class="sxs-lookup"><span data-stu-id="b4fe3-129">Hull</span></span> | <span data-ttu-id="b4fe3-130">Domain</span><span class="sxs-lookup"><span data-stu-id="b4fe3-130">Domain</span></span> | <span data-ttu-id="b4fe3-131">Geometrie</span><span class="sxs-lookup"><span data-stu-id="b4fe3-131">Geometry</span></span> | <span data-ttu-id="b4fe3-132">Pixel</span><span class="sxs-lookup"><span data-stu-id="b4fe3-132">Pixel</span></span> | <span data-ttu-id="b4fe3-133">Compute</span><span class="sxs-lookup"><span data-stu-id="b4fe3-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b4fe3-134">X</span><span class="sxs-lookup"><span data-stu-id="b4fe3-134">X</span></span>      | <span data-ttu-id="b4fe3-135">X</span><span class="sxs-lookup"><span data-stu-id="b4fe3-135">X</span></span>    | <span data-ttu-id="b4fe3-136">X</span><span class="sxs-lookup"><span data-stu-id="b4fe3-136">X</span></span>      | <span data-ttu-id="b4fe3-137">X</span><span class="sxs-lookup"><span data-stu-id="b4fe3-137">X</span></span>        | <span data-ttu-id="b4fe3-138">X</span><span class="sxs-lookup"><span data-stu-id="b4fe3-138">X</span></span>     | <span data-ttu-id="b4fe3-139">X</span><span class="sxs-lookup"><span data-stu-id="b4fe3-139">X</span></span>       |



 

<span data-ttu-id="b4fe3-140">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für UAVs für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b4fe3-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for UAVs for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="b4fe3-141">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="b4fe3-141">Vertex</span></span> | <span data-ttu-id="b4fe3-142">Hülle</span><span class="sxs-lookup"><span data-stu-id="b4fe3-142">Hull</span></span> | <span data-ttu-id="b4fe3-143">Domain</span><span class="sxs-lookup"><span data-stu-id="b4fe3-143">Domain</span></span> | <span data-ttu-id="b4fe3-144">Geometrie</span><span class="sxs-lookup"><span data-stu-id="b4fe3-144">Geometry</span></span> | <span data-ttu-id="b4fe3-145">Pixel</span><span class="sxs-lookup"><span data-stu-id="b4fe3-145">Pixel</span></span> | <span data-ttu-id="b4fe3-146">Compute</span><span class="sxs-lookup"><span data-stu-id="b4fe3-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b4fe3-147">X</span><span class="sxs-lookup"><span data-stu-id="b4fe3-147">X</span></span>      | <span data-ttu-id="b4fe3-148">X</span><span class="sxs-lookup"><span data-stu-id="b4fe3-148">X</span></span>    | <span data-ttu-id="b4fe3-149">X</span><span class="sxs-lookup"><span data-stu-id="b4fe3-149">X</span></span>      | <span data-ttu-id="b4fe3-150">X</span><span class="sxs-lookup"><span data-stu-id="b4fe3-150">X</span></span>        | <span data-ttu-id="b4fe3-151">X</span><span class="sxs-lookup"><span data-stu-id="b4fe3-151">X</span></span>     | <span data-ttu-id="b4fe3-152">X</span><span class="sxs-lookup"><span data-stu-id="b4fe3-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b4fe3-153">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="b4fe3-153">Minimum Shader Model</span></span>

<span data-ttu-id="b4fe3-154">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="b4fe3-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b4fe3-155">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="b4fe3-155">Shader Model</span></span>                                              | <span data-ttu-id="b4fe3-156">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="b4fe3-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b4fe3-157">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="b4fe3-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b4fe3-158">ja</span><span class="sxs-lookup"><span data-stu-id="b4fe3-158">yes</span></span>       |
| [<span data-ttu-id="b4fe3-159">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="b4fe3-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b4fe3-160">nein</span><span class="sxs-lookup"><span data-stu-id="b4fe3-160">no</span></span>        |
| [<span data-ttu-id="b4fe3-161">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="b4fe3-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b4fe3-162">nein</span><span class="sxs-lookup"><span data-stu-id="b4fe3-162">no</span></span>        |
| [<span data-ttu-id="b4fe3-163">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4fe3-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b4fe3-164">nein</span><span class="sxs-lookup"><span data-stu-id="b4fe3-164">no</span></span>        |
| [<span data-ttu-id="b4fe3-165">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4fe3-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b4fe3-166">nein</span><span class="sxs-lookup"><span data-stu-id="b4fe3-166">no</span></span>        |
| [<span data-ttu-id="b4fe3-167">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4fe3-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b4fe3-168">nein</span><span class="sxs-lookup"><span data-stu-id="b4fe3-168">no</span></span>        |



 

<span data-ttu-id="b4fe3-169">CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung für UAV, SRV und TGSM.</span><span class="sxs-lookup"><span data-stu-id="b4fe3-169">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV and TGSM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4fe3-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b4fe3-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4fe3-171">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4fe3-171">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





