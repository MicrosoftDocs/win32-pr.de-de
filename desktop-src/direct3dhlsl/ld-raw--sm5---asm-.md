---
title: ld_raw (SM5-ASM)
description: Zufälliger Zugriffs Lesevorgang von 1-4 32-Bit-Komponenten aus einem RAW-Puffer.
ms.assetid: F7DBA80D-4DD5-4271-B571-24FB6188ABFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4a9480ef60098b394e0eff2b06043fd9a32e45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976400"
---
# <a name="ld_raw-sm5---asm"></a><span data-ttu-id="e746f-103">LD \_ RAW (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e746f-103">ld\_raw (sm5 - asm)</span></span>

<span data-ttu-id="e746f-104">Zufälliger Zugriffs Lesevorgang von 1-4 32-Bit-Komponenten aus einem RAW-Puffer.</span><span class="sxs-lookup"><span data-stu-id="e746f-104">Random-access read of 1-4 32bit components from a raw buffer.</span></span>



| <span data-ttu-id="e746f-105">LD \_ RAW dst0 \[ . mask \] , srcbyteoffset \[ . Select \_ Component \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="e746f-105">ld\_raw dst0\[.mask\], srcByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------|



 



| <span data-ttu-id="e746f-106">Element</span><span class="sxs-lookup"><span data-stu-id="e746f-106">Item</span></span>                                                                                                                       | <span data-ttu-id="e746f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e746f-107">Description</span></span>                                                   |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e746f-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="e746f-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="e746f-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="e746f-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="e746f-110"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcbyteoffset*</span><span class="sxs-lookup"><span data-stu-id="e746f-110"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span></span><br/> | <span data-ttu-id="e746f-111">\[in \] gibt den Offset an, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e746f-111">\[in\] Specifies the offset to read from.</span></span><br/>          |
| <span data-ttu-id="e746f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e746f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="e746f-113">\[in \] der zu lesenden Komponente.</span><span class="sxs-lookup"><span data-stu-id="e746f-113">\[in\] The component to read.</span></span> <br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="e746f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e746f-114">Remarks</span></span>

<span data-ttu-id="e746f-115">*src0* muss Folgendes sein:</span><span class="sxs-lookup"><span data-stu-id="e746f-115">*src0* must be:</span></span>

-   <span data-ttu-id="e746f-116">Beliebige Shader-Stufe: SRV (t \# ) LD St</span><span class="sxs-lookup"><span data-stu-id="e746f-116">Any shader stage: SRV (t\#)ld st</span></span>
-   <span data-ttu-id="e746f-117">Compute-Shader oder Pixel-Shader: UAV (u \# )</span><span class="sxs-lookup"><span data-stu-id="e746f-117">Compute shader or pixel shader: UAV (u\#)</span></span>
-   <span data-ttu-id="e746f-118">Compute-Shader: Thread Gruppe Shared Memory (g \# )</span><span class="sxs-lookup"><span data-stu-id="e746f-118">Compute shader: thread group shared memory (g\#)</span></span>

<span data-ttu-id="e746f-119">*srcbyteoffset* gibt den 32-Bit-Basis Wert im Arbeitsspeicher für ein Fenster von 4 sequenziellen 32-Bit-Werten an, in denen Daten möglicherweise gelesen werden, je nach dem flüchtigen und der Maske anderer Parameter.</span><span class="sxs-lookup"><span data-stu-id="e746f-119">*srcByteOffset* specifies the base 32-bit value in memory for a window of 4 sequential 32-bit values in which data may be read, depending on the swizzle and mask on other parameters.</span></span>

<span data-ttu-id="e746f-120">Die aus dem RAW-Puffer gelesenen Daten entsprechen dem folgenden Pseudo Code:, wobei der Offset, die Adresse, der Zeiger auf den Pufferinhalt, der Stride der Quelle und die Daten linear gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e746f-120">The data read from the raw buffer is equivalent to the following pseudocode: where we have the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;         // from src0
                    UINT srcByteOffset;           // from srcRegister
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + srcByteOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

<span data-ttu-id="e746f-121">Die Out-of-Bounds-Adressierung für u \# /t \# einer bestimmten 32-Bit-Komponente gibt 0 für diese Komponente zurück.</span><span class="sxs-lookup"><span data-stu-id="e746f-121">Out of bounds addressing on u\#/t\# of any given 32-bit component returns 0 for that component.</span></span>

<span data-ttu-id="e746f-122">Die Adressierung auf g \# (die Begrenzungen dieses bestimmten g \# , im Gegensatz zum gesamten Shared Memory) für eine bestimmte 32-Bit-Komponente gibt ein nicht definiertes Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="e746f-122">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component returns an undefined result.</span></span>

<span data-ttu-id="e746f-123">CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung für UAV und SRV.</span><span class="sxs-lookup"><span data-stu-id="e746f-123">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

<span data-ttu-id="e746f-124">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="e746f-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e746f-125">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="e746f-125">Vertex</span></span> | <span data-ttu-id="e746f-126">Hülle</span><span class="sxs-lookup"><span data-stu-id="e746f-126">Hull</span></span> | <span data-ttu-id="e746f-127">Domain</span><span class="sxs-lookup"><span data-stu-id="e746f-127">Domain</span></span> | <span data-ttu-id="e746f-128">Geometrie</span><span class="sxs-lookup"><span data-stu-id="e746f-128">Geometry</span></span> | <span data-ttu-id="e746f-129">Pixel</span><span class="sxs-lookup"><span data-stu-id="e746f-129">Pixel</span></span> | <span data-ttu-id="e746f-130">Compute</span><span class="sxs-lookup"><span data-stu-id="e746f-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e746f-131">X</span><span class="sxs-lookup"><span data-stu-id="e746f-131">X</span></span>      | <span data-ttu-id="e746f-132">X</span><span class="sxs-lookup"><span data-stu-id="e746f-132">X</span></span>    | <span data-ttu-id="e746f-133">X</span><span class="sxs-lookup"><span data-stu-id="e746f-133">X</span></span>      | <span data-ttu-id="e746f-134">X</span><span class="sxs-lookup"><span data-stu-id="e746f-134">X</span></span>        | <span data-ttu-id="e746f-135">X</span><span class="sxs-lookup"><span data-stu-id="e746f-135">X</span></span>     | <span data-ttu-id="e746f-136">X</span><span class="sxs-lookup"><span data-stu-id="e746f-136">X</span></span>       |



 

<span data-ttu-id="e746f-137">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für UAVs für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e746f-137">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for UAVs for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="e746f-138">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="e746f-138">Vertex</span></span> | <span data-ttu-id="e746f-139">Hülle</span><span class="sxs-lookup"><span data-stu-id="e746f-139">Hull</span></span> | <span data-ttu-id="e746f-140">Domain</span><span class="sxs-lookup"><span data-stu-id="e746f-140">Domain</span></span> | <span data-ttu-id="e746f-141">Geometrie</span><span class="sxs-lookup"><span data-stu-id="e746f-141">Geometry</span></span> | <span data-ttu-id="e746f-142">Pixel</span><span class="sxs-lookup"><span data-stu-id="e746f-142">Pixel</span></span> | <span data-ttu-id="e746f-143">Compute</span><span class="sxs-lookup"><span data-stu-id="e746f-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e746f-144">X</span><span class="sxs-lookup"><span data-stu-id="e746f-144">X</span></span>      | <span data-ttu-id="e746f-145">X</span><span class="sxs-lookup"><span data-stu-id="e746f-145">X</span></span>    | <span data-ttu-id="e746f-146">X</span><span class="sxs-lookup"><span data-stu-id="e746f-146">X</span></span>      | <span data-ttu-id="e746f-147">X</span><span class="sxs-lookup"><span data-stu-id="e746f-147">X</span></span>        | <span data-ttu-id="e746f-148">X</span><span class="sxs-lookup"><span data-stu-id="e746f-148">X</span></span>     | <span data-ttu-id="e746f-149">X</span><span class="sxs-lookup"><span data-stu-id="e746f-149">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e746f-150">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="e746f-150">Minimum Shader Model</span></span>

<span data-ttu-id="e746f-151">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e746f-151">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e746f-152">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="e746f-152">Shader Model</span></span>                                              | <span data-ttu-id="e746f-153">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="e746f-153">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e746f-154">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="e746f-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e746f-155">ja</span><span class="sxs-lookup"><span data-stu-id="e746f-155">yes</span></span>       |
| [<span data-ttu-id="e746f-156">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="e746f-156">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e746f-157">nein</span><span class="sxs-lookup"><span data-stu-id="e746f-157">no</span></span>        |
| [<span data-ttu-id="e746f-158">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="e746f-158">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e746f-159">nein</span><span class="sxs-lookup"><span data-stu-id="e746f-159">no</span></span>        |
| [<span data-ttu-id="e746f-160">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e746f-160">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e746f-161">nein</span><span class="sxs-lookup"><span data-stu-id="e746f-161">no</span></span>        |
| [<span data-ttu-id="e746f-162">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e746f-162">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e746f-163">nein</span><span class="sxs-lookup"><span data-stu-id="e746f-163">no</span></span>        |
| [<span data-ttu-id="e746f-164">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e746f-164">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e746f-165">nein</span><span class="sxs-lookup"><span data-stu-id="e746f-165">no</span></span>        |



 

<span data-ttu-id="e746f-166">CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung für UAV und SRV.</span><span class="sxs-lookup"><span data-stu-id="e746f-166">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e746f-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e746f-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e746f-168">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e746f-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





