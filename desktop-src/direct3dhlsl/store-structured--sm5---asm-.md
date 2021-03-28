---
title: store_structured (SM5-ASM)
description: Zufälliger Zugriff auf Schreibvorgänge von 1-4 32-Bit-Komponenten in eine strukturierte Puffer-UAV (unsortierter Zugriffs Ansicht).
ms.assetid: 8080B2CA-5BDA-4F01-8B2B-B85BDD58C5AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5890d30fac57923365f0bdea89fcce55f7922c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038326"
---
# <a name="store_structured-sm5---asm"></a><span data-ttu-id="40c68-103">\_strukturierte Geschäfte (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="40c68-103">store\_structured (sm5 - asm)</span></span>

<span data-ttu-id="40c68-104">Zufälliger Zugriff auf Schreibvorgänge von 1-4 32-Bit-Komponenten in eine strukturierte Puffer-UAV (unsortierter Zugriffs Ansicht).</span><span class="sxs-lookup"><span data-stu-id="40c68-104">Random-access write of 1-4 32-bit components into a structured buffer unordered access view (UAV).</span></span>



| <span data-ttu-id="40c68-105">Store \_ strukturiert dst0 \[ . Write \_ mask \] , dstaddress \[ . Select \_ Component \] , dstbyteoffset \[ . Select \_ Component \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="40c68-105">store\_structured dst0\[.write\_mask\], dstAddress\[.select\_component\], dstByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="40c68-106">Element</span><span class="sxs-lookup"><span data-stu-id="40c68-106">Item</span></span>                                                                                                                       | <span data-ttu-id="40c68-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40c68-107">Description</span></span>                                                    |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="40c68-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="40c68-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="40c68-109">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="40c68-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="40c68-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstaddress*</span><span class="sxs-lookup"><span data-stu-id="40c68-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/>             | <span data-ttu-id="40c68-111">\[in \] der Adresse, an der geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="40c68-111">\[in\] The address at which to write.</span></span><br/>               |
| <span data-ttu-id="40c68-112"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstbyteoffset*</span><span class="sxs-lookup"><span data-stu-id="40c68-112"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span></span><br/> | <span data-ttu-id="40c68-113">\[im \] Index der zu schreibenden-Struktur.</span><span class="sxs-lookup"><span data-stu-id="40c68-113">\[in\] The index of the structure to write.</span></span><br/>         |
| <span data-ttu-id="40c68-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="40c68-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="40c68-115">\[in \] den zu schreibende Komponenten.</span><span class="sxs-lookup"><span data-stu-id="40c68-115">\[in\] The components to write.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="40c68-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40c68-116">Remarks</span></span>

<span data-ttu-id="40c68-117">Diese Anweisung führt 1-4 \* -Komponente-32-Bit-Komponenten aus, die von *src0* auf *dst0* an der Adresse in *dstaddress* und *dstbyteoffset* geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="40c68-117">This instruction performs 1-4 component \*32bit components written from *src0* to *dst0* at the address in *dstAddress* and *dstByteOffset*.</span></span> <span data-ttu-id="40c68-118">Keine Formatkonvertierung.</span><span class="sxs-lookup"><span data-stu-id="40c68-118">No format conversion.</span></span>

<span data-ttu-id="40c68-119">*dst0* muss eine UAV (u \# ) sein.</span><span class="sxs-lookup"><span data-stu-id="40c68-119">*dst0* must be a UAV (u\#).</span></span> <span data-ttu-id="40c68-120">Im COMPUTE-Shader kann es sich auch um einen Thread Gruppen-Shared Memory (g \# ) handeln.</span><span class="sxs-lookup"><span data-stu-id="40c68-120">In the compute shader it can also be thread group shared memory (g\#).</span></span>

<span data-ttu-id="40c68-121">*dstaddress* gibt den Index der zu schreibenden Struktur an.</span><span class="sxs-lookup"><span data-stu-id="40c68-121">*dstAddress* specifies the index of the structure to write.</span></span>

<span data-ttu-id="40c68-122">Der Speicherort der geschriebenen Daten entspricht dem folgenden Pseudo Code, der den Offset, die Adresse, den Zeiger auf den Pufferinhalt, den Schritt der Quelle und die Daten, die linear gespeichert werden, anzeigt.</span><span class="sxs-lookup"><span data-stu-id="40c68-122">The location of the data written is equivalent to the following pseudocode which shows the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;             // from dst0
                    UINT BufferStride;                // from dst0
                    UINT dstAddress, dstByteOffset;   // source registers
                    BYTE *WriteLocation;              // value to calculate

                    // calculate writing location
                     WriteLocation = BufferContents 
                                + BufferStride * dstAddress 
                                + dstByteOffset;

                    // calculate the number of components to write
                    switch (dstWriteMask)
                    {
                        x:    WriteComponents = 1; break;
                        xy:   WriteComponents = 2; break;
                        xyz:  WriteComponents = 3; break;
                        xyzw: WriteComponents = 4; break;
                        default:  // only these masks are valid                              
                    }

                    // copy the data from the source register with
                    //    the swizzle applied
                    memcpy(WriteLocation, swizzle(src0, src0.swizzle), 
                             WriteComponents * sizeof(INT32));
```

<span data-ttu-id="40c68-123">Dieser Pseudo Code zeigt, wie der Vorgang funktioniert, aber die tatsächlichen Daten müssen nicht linear gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="40c68-123">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="40c68-124">Wenn die Daten nicht linear gespeichert werden, muss die tatsächliche Operation der Anweisung mit dem Verhalten des obigen Vorgangs identisch sein.</span><span class="sxs-lookup"><span data-stu-id="40c68-124">If the data is not stored linearly, the actual operation of the instruction needs to match the behavior of the above operation.</span></span>

<span data-ttu-id="40c68-125">*dst0* kann nur eine Schreib Maske aufweisen, die eine der folgenden ist:. x,. XY,. XYZ,. xyzw.</span><span class="sxs-lookup"><span data-stu-id="40c68-125">*dst0* can only have a write mask that is one of the following: .x, .xy, .xyz, .xyzw.</span></span> <span data-ttu-id="40c68-126">Die Schreib Maske bestimmt die Anzahl der 32-Bit-Komponenten, die ohne Lücken geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="40c68-126">The write mask determines the number of 32-bit components to write without gaps.</span></span>

<span data-ttu-id="40c68-127">Wenn die Adressierung von " \# *dstaddress* " nicht mehr begrenzt ist, bedeutet dies, dass nichts in den Speicher außerhalb des gültigen Bereichs geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="40c68-127">Out of bounds addressing on u\# casued by *dstAddress* means nothing is written to the out of bounds memory.</span></span>

<span data-ttu-id="40c68-128">Wenn *dstbyteoffset*, einschließlich *dstschreitemask*, den Zugriff für den Zugriff auf Sie verursacht, wird \# der gesamte Inhalt der UAV nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="40c68-128">If the *dstByteOffset*, including *dstWriteMask*, is what causes out of bounds access to u\#, the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="40c68-129">Die Adressierung auf g \# (die Begrenzungen dieses bestimmten g \# , im Gegensatz zum gesamten freigegebenen Speicher) für eine bestimmte 32-Bit-Komponente bewirkt, dass der gesamte Inhalt des gesamten freigegebenen Speichers undefiniert wird.</span><span class="sxs-lookup"><span data-stu-id="40c68-129">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="40c68-130">*dstbyteoffset* ist ein separates Argument von *dstaddress* , da es sich in der Regel um ein Literalelement handelt.</span><span class="sxs-lookup"><span data-stu-id="40c68-130">*dstByteOffset* is a separate argument from *dstAddress* because it is commonly a literal.</span></span> <span data-ttu-id="40c68-131">Diese Parameter Trennung wurde nicht für Atomics in strukturiertem Arbeitsspeicher durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="40c68-131">This parameter separation has not been done for atomics on structured memory.</span></span>

<span data-ttu-id="40c68-132">CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung für UAV und TGSM.</span><span class="sxs-lookup"><span data-stu-id="40c68-132">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and TGSM.</span></span>

<span data-ttu-id="40c68-133">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="40c68-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="40c68-134">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="40c68-134">Vertex</span></span> | <span data-ttu-id="40c68-135">Hülle</span><span class="sxs-lookup"><span data-stu-id="40c68-135">Hull</span></span> | <span data-ttu-id="40c68-136">Domain</span><span class="sxs-lookup"><span data-stu-id="40c68-136">Domain</span></span> | <span data-ttu-id="40c68-137">Geometrie</span><span class="sxs-lookup"><span data-stu-id="40c68-137">Geometry</span></span> | <span data-ttu-id="40c68-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="40c68-138">Pixel</span></span> | <span data-ttu-id="40c68-139">Compute</span><span class="sxs-lookup"><span data-stu-id="40c68-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="40c68-140">X</span><span class="sxs-lookup"><span data-stu-id="40c68-140">X</span></span>     | <span data-ttu-id="40c68-141">X</span><span class="sxs-lookup"><span data-stu-id="40c68-141">X</span></span>       |



 

<span data-ttu-id="40c68-142">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="40c68-142">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="40c68-143">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="40c68-143">Vertex</span></span> | <span data-ttu-id="40c68-144">Hülle</span><span class="sxs-lookup"><span data-stu-id="40c68-144">Hull</span></span> | <span data-ttu-id="40c68-145">Domain</span><span class="sxs-lookup"><span data-stu-id="40c68-145">Domain</span></span> | <span data-ttu-id="40c68-146">Geometrie</span><span class="sxs-lookup"><span data-stu-id="40c68-146">Geometry</span></span> | <span data-ttu-id="40c68-147">Pixel</span><span class="sxs-lookup"><span data-stu-id="40c68-147">Pixel</span></span> | <span data-ttu-id="40c68-148">Compute</span><span class="sxs-lookup"><span data-stu-id="40c68-148">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="40c68-149">X</span><span class="sxs-lookup"><span data-stu-id="40c68-149">X</span></span>      | <span data-ttu-id="40c68-150">X</span><span class="sxs-lookup"><span data-stu-id="40c68-150">X</span></span>    | <span data-ttu-id="40c68-151">X</span><span class="sxs-lookup"><span data-stu-id="40c68-151">X</span></span>      | <span data-ttu-id="40c68-152">X</span><span class="sxs-lookup"><span data-stu-id="40c68-152">X</span></span>        | <span data-ttu-id="40c68-153">X</span><span class="sxs-lookup"><span data-stu-id="40c68-153">X</span></span>     | <span data-ttu-id="40c68-154">X</span><span class="sxs-lookup"><span data-stu-id="40c68-154">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="40c68-155">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="40c68-155">Minimum Shader Model</span></span>

<span data-ttu-id="40c68-156">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="40c68-156">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="40c68-157">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="40c68-157">Shader Model</span></span>                                              | <span data-ttu-id="40c68-158">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="40c68-158">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="40c68-159">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="40c68-159">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="40c68-160">ja</span><span class="sxs-lookup"><span data-stu-id="40c68-160">yes</span></span>       |
| [<span data-ttu-id="40c68-161">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="40c68-161">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="40c68-162">nein</span><span class="sxs-lookup"><span data-stu-id="40c68-162">no</span></span>        |
| [<span data-ttu-id="40c68-163">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="40c68-163">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="40c68-164">nein</span><span class="sxs-lookup"><span data-stu-id="40c68-164">no</span></span>        |
| [<span data-ttu-id="40c68-165">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="40c68-165">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="40c68-166">nein</span><span class="sxs-lookup"><span data-stu-id="40c68-166">no</span></span>        |
| [<span data-ttu-id="40c68-167">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="40c68-167">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="40c68-168">nein</span><span class="sxs-lookup"><span data-stu-id="40c68-168">no</span></span>        |
| [<span data-ttu-id="40c68-169">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="40c68-169">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="40c68-170">nein</span><span class="sxs-lookup"><span data-stu-id="40c68-170">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="40c68-171">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="40c68-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40c68-172">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="40c68-172">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





