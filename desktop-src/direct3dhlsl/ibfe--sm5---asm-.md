---
title: ibfe (SM5-ASM)
description: Wenn ein Bereich von Bits in einer Zahl angegeben ist, verschieben Sie diese Bits in den LSB und Signieren den MSB des Bereichs.
ms.assetid: 1ED39812-A89F-4325-82A0-DA2CCC55A99A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 805d5c1137e25d8b8fa560588b9e876ccc5c8748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719368"
---
# <a name="ibfe-sm5---asm"></a><span data-ttu-id="c250d-103">ibfe (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c250d-103">ibfe (sm5 - asm)</span></span>

<span data-ttu-id="c250d-104">Wenn ein Bereich von Bits in einer Zahl angegeben ist, verschieben Sie diese Bits in den LSB und Signieren den MSB des Bereichs.</span><span class="sxs-lookup"><span data-stu-id="c250d-104">Given a range of bits in a number, shift those bits to the LSB and sign extend the MSB of the range.</span></span>



| <span data-ttu-id="c250d-105">ibfe dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle \] , Quelle2 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c250d-105">ibfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="c250d-106">Element</span><span class="sxs-lookup"><span data-stu-id="c250d-106">Item</span></span>                                                            | <span data-ttu-id="c250d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c250d-107">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="c250d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c250d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c250d-109">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c250d-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="c250d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c250d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c250d-111">\[in \] der Bitfeld Breite.</span><span class="sxs-lookup"><span data-stu-id="c250d-111">\[in\] The bitfield width.</span></span><br/>                          |
| <span data-ttu-id="c250d-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="c250d-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="c250d-113">\[im \] Bitfeld-Offset.</span><span class="sxs-lookup"><span data-stu-id="c250d-113">\[in\] The bitfield offset.</span></span><br/>                         |
| <span data-ttu-id="c250d-114"><span id="src2"></span><span id="SRC2"></span>*Quelle2*</span><span class="sxs-lookup"><span data-stu-id="c250d-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="c250d-115">\[im \] zu Verschiebe Wert.</span><span class="sxs-lookup"><span data-stu-id="c250d-115">\[in\] The value to shift.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="c250d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c250d-116">Remarks</span></span>

<span data-ttu-id="c250d-117">In den lsb 5 Bits von src0 wird die Bitfeld Breite (0-31) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c250d-117">The LSB 5 bits of src0 provide the bitfield width (0-31).</span></span>

<span data-ttu-id="c250d-118">Mit den lsb 5 Bits von Quelle1 wird der Bitfeld-Offset (0-31) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c250d-118">The LSB 5 bits of src1 provide the bitfield offset (0-31).</span></span>

<span data-ttu-id="c250d-119">Das folgende Beispiel zeigt die Verwendung dieser Anweisung.</span><span class="sxs-lookup"><span data-stu-id="c250d-119">The following example shows how to use this instruction.</span></span>

``` syntax
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ishr dest, dest, 32-width
                }
                else
                {
                    ishr dest, src2, offset
                }
```

<span data-ttu-id="c250d-120">Verwenden Sie diese Anweisung, um ganze Zahlen oder Flags mit Vorzeichen zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="c250d-120">Use this instruction to unpack signed integers or flags.</span></span>

<span data-ttu-id="c250d-121">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="c250d-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c250d-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c250d-122">Vertex</span></span> | <span data-ttu-id="c250d-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="c250d-123">Hull</span></span> | <span data-ttu-id="c250d-124">Domain</span><span class="sxs-lookup"><span data-stu-id="c250d-124">Domain</span></span> | <span data-ttu-id="c250d-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c250d-125">Geometry</span></span> | <span data-ttu-id="c250d-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="c250d-126">Pixel</span></span> | <span data-ttu-id="c250d-127">Compute</span><span class="sxs-lookup"><span data-stu-id="c250d-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c250d-128">X</span><span class="sxs-lookup"><span data-stu-id="c250d-128">X</span></span>      | <span data-ttu-id="c250d-129">X</span><span class="sxs-lookup"><span data-stu-id="c250d-129">X</span></span>    | <span data-ttu-id="c250d-130">X</span><span class="sxs-lookup"><span data-stu-id="c250d-130">X</span></span>      | <span data-ttu-id="c250d-131">X</span><span class="sxs-lookup"><span data-stu-id="c250d-131">X</span></span>        | <span data-ttu-id="c250d-132">X</span><span class="sxs-lookup"><span data-stu-id="c250d-132">X</span></span>     | <span data-ttu-id="c250d-133">X</span><span class="sxs-lookup"><span data-stu-id="c250d-133">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c250d-134">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c250d-134">Minimum Shader Model</span></span>

<span data-ttu-id="c250d-135">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c250d-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c250d-136">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c250d-136">Shader Model</span></span>                                              | <span data-ttu-id="c250d-137">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c250d-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c250d-138">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="c250d-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c250d-139">ja</span><span class="sxs-lookup"><span data-stu-id="c250d-139">yes</span></span>       |
| [<span data-ttu-id="c250d-140">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="c250d-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c250d-141">nein</span><span class="sxs-lookup"><span data-stu-id="c250d-141">no</span></span>        |
| [<span data-ttu-id="c250d-142">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="c250d-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c250d-143">nein</span><span class="sxs-lookup"><span data-stu-id="c250d-143">no</span></span>        |
| [<span data-ttu-id="c250d-144">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c250d-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c250d-145">nein</span><span class="sxs-lookup"><span data-stu-id="c250d-145">no</span></span>        |
| [<span data-ttu-id="c250d-146">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c250d-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c250d-147">nein</span><span class="sxs-lookup"><span data-stu-id="c250d-147">no</span></span>        |
| [<span data-ttu-id="c250d-148">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c250d-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c250d-149">nein</span><span class="sxs-lookup"><span data-stu-id="c250d-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c250d-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c250d-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c250d-151">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c250d-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





