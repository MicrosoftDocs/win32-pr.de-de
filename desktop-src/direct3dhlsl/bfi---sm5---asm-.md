---
title: BFI (SM5-ASM)
description: Wenn ein Bitbereich vom lsb einer Zahl ist, platzieren Sie die Anzahl der Bits in einem beliebigen Offset in einer anderen Zahl.
ms.assetid: BA84C882-A141-4AD2-8FD9-C60F1483FC65
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14f8b9f6ef126ec3c6a31bf330dfd89cf0770c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038346"
---
# <a name="bfi-sm5---asm"></a><span data-ttu-id="eb480-103">BFI (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="eb480-103">bfi (sm5 - asm)</span></span>

<span data-ttu-id="eb480-104">Wenn ein Bitbereich vom lsb einer Zahl ist, platzieren Sie die Anzahl der Bits in einem beliebigen Offset in einer anderen Zahl.</span><span class="sxs-lookup"><span data-stu-id="eb480-104">Given a bit range from the LSB of a number, place that number of bits in another number at any offset.</span></span>



| <span data-ttu-id="eb480-105">BFI dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle \] , Quelle2 \[ . Swizzle \] , src3 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="eb480-105">bfi dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\], src3\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="eb480-106">Element</span><span class="sxs-lookup"><span data-stu-id="eb480-106">Item</span></span>                                                            | <span data-ttu-id="eb480-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb480-107">Description</span></span>                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="eb480-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="eb480-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="eb480-109">\[in \] der Adresse der Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="eb480-109">\[in\] The address of the results.</span></span><br/>                       |
| <span data-ttu-id="eb480-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="eb480-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="eb480-111">\[in \] der bitfeldbreite, die von *Quelle2* übernommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb480-111">\[in\] The bitfield width to take from *src2*.</span></span><br/>           |
| <span data-ttu-id="eb480-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="eb480-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="eb480-113">\[im \] Bitfeld-Offset zum Ersetzen von Bits in *src3*.</span><span class="sxs-lookup"><span data-stu-id="eb480-113">\[in\] The bitfield offset for replacing bits in *src3*.</span></span><br/> |
| <span data-ttu-id="eb480-114"><span id="src2"></span><span id="SRC2"></span>*Quelle2*</span><span class="sxs-lookup"><span data-stu-id="eb480-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="eb480-115">\[in \] der Zahl, von der die Bits entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="eb480-115">\[in\] The number the bits are taken from.</span></span> <br/>              |
| <span data-ttu-id="eb480-116"><span id="src3"></span><span id="SRC3"></span>*src3*</span><span class="sxs-lookup"><span data-stu-id="eb480-116"><span id="src3"></span><span id="SRC3"></span>*src3*</span></span><br/> | <span data-ttu-id="eb480-117">\[in \] der Zahl mit Bits, die ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eb480-117">\[in\] The number with bits to be replaced.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="eb480-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb480-118">Remarks</span></span>

<span data-ttu-id="eb480-119">Die lsb 5 Bits von *src0* geben die Bitfeld Breite (0-31) an, die von *Quelle2* genommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb480-119">The LSB 5 bits of *src0* provide the bitfield width (0-31) to take from *src2*.</span></span>

<span data-ttu-id="eb480-120">Die lsb 5-Bits von *Quelle1* stellen den Bitfeld-Offset (0-31) bereit, um die Bits in der von *src3* gelesenen Zahl zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="eb480-120">The LSB 5 bits of *src1* provide the bitfield offset (0-31) to start replacing bits in the number read from *src3*.</span></span>

``` syntax
Given width, offset:
                bitmask = (((1 << width)-1) << offset) & 0xffffffff
                dest = ((src2 << offset) & bitmask) | (src3 & ~bitmask)
```

<span data-ttu-id="eb480-121">Diese Anweisung wird zum Packen von Ganzzahlen oder Flags verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb480-121">This instruction is used for packing integers or flags.</span></span>

<span data-ttu-id="eb480-122">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="eb480-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="eb480-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="eb480-123">Vertex</span></span> | <span data-ttu-id="eb480-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="eb480-124">Hull</span></span> | <span data-ttu-id="eb480-125">Domain</span><span class="sxs-lookup"><span data-stu-id="eb480-125">Domain</span></span> | <span data-ttu-id="eb480-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="eb480-126">Geometry</span></span> | <span data-ttu-id="eb480-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="eb480-127">Pixel</span></span> | <span data-ttu-id="eb480-128">Compute</span><span class="sxs-lookup"><span data-stu-id="eb480-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="eb480-129">X</span><span class="sxs-lookup"><span data-stu-id="eb480-129">X</span></span>      | <span data-ttu-id="eb480-130">X</span><span class="sxs-lookup"><span data-stu-id="eb480-130">X</span></span>    | <span data-ttu-id="eb480-131">X</span><span class="sxs-lookup"><span data-stu-id="eb480-131">X</span></span>      | <span data-ttu-id="eb480-132">X</span><span class="sxs-lookup"><span data-stu-id="eb480-132">X</span></span>        | <span data-ttu-id="eb480-133">X</span><span class="sxs-lookup"><span data-stu-id="eb480-133">X</span></span>     | <span data-ttu-id="eb480-134">X</span><span class="sxs-lookup"><span data-stu-id="eb480-134">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="eb480-135">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="eb480-135">Minimum Shader Model</span></span>

<span data-ttu-id="eb480-136">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="eb480-136">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="eb480-137">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="eb480-137">Shader Model</span></span>                                              | <span data-ttu-id="eb480-138">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="eb480-138">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="eb480-139">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="eb480-139">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="eb480-140">ja</span><span class="sxs-lookup"><span data-stu-id="eb480-140">yes</span></span>       |
| [<span data-ttu-id="eb480-141">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="eb480-141">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="eb480-142">nein</span><span class="sxs-lookup"><span data-stu-id="eb480-142">no</span></span>        |
| [<span data-ttu-id="eb480-143">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="eb480-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="eb480-144">nein</span><span class="sxs-lookup"><span data-stu-id="eb480-144">no</span></span>        |
| [<span data-ttu-id="eb480-145">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb480-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="eb480-146">nein</span><span class="sxs-lookup"><span data-stu-id="eb480-146">no</span></span>        |
| [<span data-ttu-id="eb480-147">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb480-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="eb480-148">nein</span><span class="sxs-lookup"><span data-stu-id="eb480-148">no</span></span>        |
| [<span data-ttu-id="eb480-149">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb480-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="eb480-150">nein</span><span class="sxs-lookup"><span data-stu-id="eb480-150">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="eb480-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eb480-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb480-152">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb480-152">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





