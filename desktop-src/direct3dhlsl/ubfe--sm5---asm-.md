---
title: ubfe (SM5-ASM)
description: Wenn ein Bereich von Bits in einer Zahl angegeben ist, verschieben Sie diese Bits in den LSB, und legen Sie verbleibende Bits auf 0 fest.
ms.assetid: CC6BE378-2726-47A2-8E23-B8151521F72D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ebbe853ec1b53b452f32d79c9c2ec120e826b8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857771"
---
# <a name="ubfe-sm5---asm"></a><span data-ttu-id="b0be0-103">ubfe (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="b0be0-103">ubfe (sm5 - asm)</span></span>

<span data-ttu-id="b0be0-104">Wenn ein Bereich von Bits in einer Zahl angegeben ist, verschieben Sie diese Bits in den LSB, und legen Sie verbleibende Bits auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="b0be0-104">Given a range of bits in a number, shift those bits to the LSB and set remaining bits to 0.</span></span>



| <span data-ttu-id="b0be0-105">ubfe dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle \] , Quelle2 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="b0be0-105">ubfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="b0be0-106">Element</span><span class="sxs-lookup"><span data-stu-id="b0be0-106">Item</span></span>                                                            | <span data-ttu-id="b0be0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b0be0-107">Description</span></span>                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="b0be0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b0be0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b0be0-109">\[in \] enthält die Ergebnisse der-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="b0be0-109">\[in\] Contains the results of the instruction.</span></span><br/>                     |
| <span data-ttu-id="b0be0-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b0be0-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b0be0-111">\[Geben Sie in \] den lsb 5 Bits die Bitfeld-Breite (0-31) an.</span><span class="sxs-lookup"><span data-stu-id="b0be0-111">\[in\] The LSB 5 bits provide the bitfield width (0-31).</span></span><br/>            |
| <span data-ttu-id="b0be0-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="b0be0-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="b0be0-113">\[Geben Sie in \] den lsb 5-Bits von *Quelle1* den Bitfeld-Offset (0-31) an.</span><span class="sxs-lookup"><span data-stu-id="b0be0-113">\[in\] The LSB 5 bits of *src1* provide the bitfield offset (0-31).</span></span><br/> |
| <span data-ttu-id="b0be0-114"><span id="src2"></span><span id="SRC2"></span>*Quelle2*</span><span class="sxs-lookup"><span data-stu-id="b0be0-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="b0be0-115">\[in \] der zu Verschiebe Zahl.</span><span class="sxs-lookup"><span data-stu-id="b0be0-115">\[in\] The number to shift.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="b0be0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0be0-116">Remarks</span></span>

``` syntax
 
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ushr dest, dest, 32-width
                }
                else
                {
                    ushr dest, src2, offset
                }
```

<span data-ttu-id="b0be0-117">Verwenden Sie diese Anweisung, um Ganzzahlen ohne Vorzeichen oder Flags zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="b0be0-117">Use this instruction to unpack unsigned integers or flags.</span></span>

<span data-ttu-id="b0be0-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="b0be0-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b0be0-119">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="b0be0-119">Vertex</span></span> | <span data-ttu-id="b0be0-120">Hülle</span><span class="sxs-lookup"><span data-stu-id="b0be0-120">Hull</span></span> | <span data-ttu-id="b0be0-121">Domain</span><span class="sxs-lookup"><span data-stu-id="b0be0-121">Domain</span></span> | <span data-ttu-id="b0be0-122">Geometrie</span><span class="sxs-lookup"><span data-stu-id="b0be0-122">Geometry</span></span> | <span data-ttu-id="b0be0-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="b0be0-123">Pixel</span></span> | <span data-ttu-id="b0be0-124">Compute</span><span class="sxs-lookup"><span data-stu-id="b0be0-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b0be0-125">X</span><span class="sxs-lookup"><span data-stu-id="b0be0-125">X</span></span>      | <span data-ttu-id="b0be0-126">X</span><span class="sxs-lookup"><span data-stu-id="b0be0-126">X</span></span>    | <span data-ttu-id="b0be0-127">X</span><span class="sxs-lookup"><span data-stu-id="b0be0-127">X</span></span>      | <span data-ttu-id="b0be0-128">X</span><span class="sxs-lookup"><span data-stu-id="b0be0-128">X</span></span>        | <span data-ttu-id="b0be0-129">X</span><span class="sxs-lookup"><span data-stu-id="b0be0-129">X</span></span>     | <span data-ttu-id="b0be0-130">X</span><span class="sxs-lookup"><span data-stu-id="b0be0-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b0be0-131">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="b0be0-131">Minimum Shader Model</span></span>

<span data-ttu-id="b0be0-132">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="b0be0-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b0be0-133">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="b0be0-133">Shader Model</span></span>                                              | <span data-ttu-id="b0be0-134">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="b0be0-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b0be0-135">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="b0be0-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b0be0-136">ja</span><span class="sxs-lookup"><span data-stu-id="b0be0-136">yes</span></span>       |
| [<span data-ttu-id="b0be0-137">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="b0be0-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b0be0-138">nein</span><span class="sxs-lookup"><span data-stu-id="b0be0-138">no</span></span>        |
| [<span data-ttu-id="b0be0-139">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="b0be0-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b0be0-140">nein</span><span class="sxs-lookup"><span data-stu-id="b0be0-140">no</span></span>        |
| [<span data-ttu-id="b0be0-141">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b0be0-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b0be0-142">nein</span><span class="sxs-lookup"><span data-stu-id="b0be0-142">no</span></span>        |
| [<span data-ttu-id="b0be0-143">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b0be0-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b0be0-144">nein</span><span class="sxs-lookup"><span data-stu-id="b0be0-144">no</span></span>        |
| [<span data-ttu-id="b0be0-145">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b0be0-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b0be0-146">nein</span><span class="sxs-lookup"><span data-stu-id="b0be0-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b0be0-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b0be0-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0be0-148">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b0be0-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





