---
title: store_raw (SM5-ASM)
description: Zufälliger Zugriff auf Schreibvorgänge von 1-4 32-Bit-Komponenten in typlosen Arbeitsspeicher.
ms.assetid: D166116A-CF4E-4020-9F6A-F9CEEFCDAB21
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44b4d22a576853fb8b7d2c43fcb6a2d7fc9a448
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389582"
---
# <a name="store_raw-sm5---asm"></a><span data-ttu-id="7faba-103">\_rohspeicher (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="7faba-103">store\_raw (sm5 - asm)</span></span>

<span data-ttu-id="7faba-104">Zufälliger Zugriff auf Schreibvorgänge von 1-4 32-Bit-Komponenten in typlosen Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="7faba-104">Random-access write of 1-4 32bit components into typeless memory.</span></span>



| <span data-ttu-id="7faba-105">\_Rohdaten speichern dst0 \[ . Write \_ mask \] , dstbyteoffset \[ . Select \_ Component \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="7faba-105">store\_raw dst0\[.write\_mask\], dstByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------|



 



| <span data-ttu-id="7faba-106">Element</span><span class="sxs-lookup"><span data-stu-id="7faba-106">Item</span></span>                                                                                                                       | <span data-ttu-id="7faba-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7faba-107">Description</span></span>                                |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="7faba-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="7faba-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="7faba-109">\[in \] der Speicheradresse.</span><span class="sxs-lookup"><span data-stu-id="7faba-109">\[in\] The memory address.</span></span><br/>      |
| <span data-ttu-id="7faba-110"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstbyteoffset*</span><span class="sxs-lookup"><span data-stu-id="7faba-110"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span></span><br/> | <span data-ttu-id="7faba-111">\[im \] Offset.</span><span class="sxs-lookup"><span data-stu-id="7faba-111">\[in\] The offset.</span></span><br/>              |
| <span data-ttu-id="7faba-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="7faba-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="7faba-113">\[in \] den zu schreibende Komponenten.</span><span class="sxs-lookup"><span data-stu-id="7faba-113">\[in\] The components to write.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7faba-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7faba-114">Remarks</span></span>

<span data-ttu-id="7faba-115">Diese Anweisung führt 1-4 \* -Komponente 32-Bit-Komponenten aus, die am Offset in *dstbyteoffset* von *src0* in *dst0* geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="7faba-115">This instruction performs 1-4 component \*32-bit components written from *src0* to *dst0* at the offset in *dstByteOffset*.</span></span> <span data-ttu-id="7faba-116">Es gibt keine Formatkonvertierung.</span><span class="sxs-lookup"><span data-stu-id="7faba-116">There is no format conversion.</span></span>

<span data-ttu-id="7faba-117">*dst0* muss ein UAV (u \# ) sein, oder im COMPUTE-Shader kann es sich auch um einen Thread Gruppen-Shared Memory (g \# ) handeln.</span><span class="sxs-lookup"><span data-stu-id="7faba-117">*dst0* must be a UAV (u\#), or in the compute shader it can also be thread group shared memory (g\#).</span></span>

<span data-ttu-id="7faba-118">*dstbyteoffset* gibt den 32-Bit-Basis Wert im Arbeitsspeicher für ein Fenster von 4 sequenziellen 32-Bit-Werten an, in dem Daten geschrieben werden können, abhängig von der Striche-und Maske für andere Parameter.</span><span class="sxs-lookup"><span data-stu-id="7faba-118">*dstByteOffset* specifies the base 32-bit value in memory for a window of 4 sequential 32-bit values in which data may be written, depending on the swizzle and mask on other parameters.</span></span>

<span data-ttu-id="7faba-119">Der Speicherort der geschriebenen Daten entspricht dem folgenden Pseudo Code, der die Adresse, den Zeiger auf den Pufferinhalt und die Daten, die linear gespeichert werden, anzeigt.</span><span class="sxs-lookup"><span data-stu-id="7faba-119">The location of the data written is equivalent to the following pseudocode which show the address, pointer to the buffer contents, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;          // from src0
                    UINT dstByteOffset;            // source register
                    BYTE *WriteLocation;           // value to calculate

                    // calculate writing location
                    WriteLocation = BufferContents 
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
                             WriteComponents * sizeof(UINT32));
```

<span data-ttu-id="7faba-120">Dieser Pseudo Code zeigt, wie der Vorgang funktioniert, aber die tatsächlichen Daten müssen nicht linear gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7faba-120">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="7faba-121">*dst0* kann nur eine Schreib Maske aufweisen, die eine der folgenden ist:. x,. XY,. XYZ,. xyzw.</span><span class="sxs-lookup"><span data-stu-id="7faba-121">*dst0* can only have a write mask that is one of the following: .x, .xy, .xyz, .xyzw.</span></span> <span data-ttu-id="7faba-122">Die Schreib Maske bestimmt, wie viele 32-Bit-Komponenten ohne Lücken geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7faba-122">The write mask determines the number of 32bit components to write without gaps.</span></span>

<span data-ttu-id="7faba-123">Die Adressierung von u \# bedeutet, dass nichts in den Speicher außerhalb des gültigen Bereichs geschrieben wird. alle Teile, die sich in den Grenzen befinden, werden ordnungsgemäß geschrieben.</span><span class="sxs-lookup"><span data-stu-id="7faba-123">Out of bounds addressing on u\# means nothing is written to the out of bounds memory; any part that is in bounds is written correctly.</span></span>

<span data-ttu-id="7faba-124">Die Adressierung auf g \# (die Begrenzungen dieses bestimmten g \# , im Gegensatz zum gesamten freigegebenen Speicher) für eine bestimmte 32-Bit-Komponente bewirkt, dass der gesamte Inhalt des gesamten freigegebenen Speichers undefiniert wird.</span><span class="sxs-lookup"><span data-stu-id="7faba-124">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="7faba-125">CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung für UAV.</span><span class="sxs-lookup"><span data-stu-id="7faba-125">cs\_4\_0 and cs\_4\_1 support this instruction for UAV.</span></span>

<span data-ttu-id="7faba-126">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="7faba-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7faba-127">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="7faba-127">Vertex</span></span> | <span data-ttu-id="7faba-128">Hülle</span><span class="sxs-lookup"><span data-stu-id="7faba-128">Hull</span></span> | <span data-ttu-id="7faba-129">Domain</span><span class="sxs-lookup"><span data-stu-id="7faba-129">Domain</span></span> | <span data-ttu-id="7faba-130">Geometrie</span><span class="sxs-lookup"><span data-stu-id="7faba-130">Geometry</span></span> | <span data-ttu-id="7faba-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="7faba-131">Pixel</span></span> | <span data-ttu-id="7faba-132">Compute</span><span class="sxs-lookup"><span data-stu-id="7faba-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="7faba-133">X</span><span class="sxs-lookup"><span data-stu-id="7faba-133">X</span></span>     | <span data-ttu-id="7faba-134">X</span><span class="sxs-lookup"><span data-stu-id="7faba-134">X</span></span>       |



 

<span data-ttu-id="7faba-135">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7faba-135">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="7faba-136">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="7faba-136">Vertex</span></span> | <span data-ttu-id="7faba-137">Hülle</span><span class="sxs-lookup"><span data-stu-id="7faba-137">Hull</span></span> | <span data-ttu-id="7faba-138">Domain</span><span class="sxs-lookup"><span data-stu-id="7faba-138">Domain</span></span> | <span data-ttu-id="7faba-139">Geometrie</span><span class="sxs-lookup"><span data-stu-id="7faba-139">Geometry</span></span> | <span data-ttu-id="7faba-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="7faba-140">Pixel</span></span> | <span data-ttu-id="7faba-141">Compute</span><span class="sxs-lookup"><span data-stu-id="7faba-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7faba-142">X</span><span class="sxs-lookup"><span data-stu-id="7faba-142">X</span></span>      | <span data-ttu-id="7faba-143">X</span><span class="sxs-lookup"><span data-stu-id="7faba-143">X</span></span>    | <span data-ttu-id="7faba-144">X</span><span class="sxs-lookup"><span data-stu-id="7faba-144">X</span></span>      | <span data-ttu-id="7faba-145">X</span><span class="sxs-lookup"><span data-stu-id="7faba-145">X</span></span>        | <span data-ttu-id="7faba-146">X</span><span class="sxs-lookup"><span data-stu-id="7faba-146">X</span></span>     | <span data-ttu-id="7faba-147">X</span><span class="sxs-lookup"><span data-stu-id="7faba-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7faba-148">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="7faba-148">Minimum Shader Model</span></span>

<span data-ttu-id="7faba-149">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="7faba-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="7faba-150">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="7faba-150">Shader Model</span></span>                                              | <span data-ttu-id="7faba-151">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="7faba-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7faba-152">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="7faba-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7faba-153">ja</span><span class="sxs-lookup"><span data-stu-id="7faba-153">yes</span></span>       |
| [<span data-ttu-id="7faba-154">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="7faba-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7faba-155">nein</span><span class="sxs-lookup"><span data-stu-id="7faba-155">no</span></span>        |
| [<span data-ttu-id="7faba-156">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="7faba-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7faba-157">nein</span><span class="sxs-lookup"><span data-stu-id="7faba-157">no</span></span>        |
| [<span data-ttu-id="7faba-158">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7faba-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7faba-159">nein</span><span class="sxs-lookup"><span data-stu-id="7faba-159">no</span></span>        |
| [<span data-ttu-id="7faba-160">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7faba-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7faba-161">nein</span><span class="sxs-lookup"><span data-stu-id="7faba-161">no</span></span>        |
| [<span data-ttu-id="7faba-162">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7faba-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7faba-163">nein</span><span class="sxs-lookup"><span data-stu-id="7faba-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7faba-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7faba-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7faba-165">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7faba-165">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





