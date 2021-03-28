---
title: firstbit (SM5-ASM)
description: Sucht das erste Bit, das in einer Zahl festgelegt ist, entweder von der LSB oder von MSB.
ms.assetid: E3066676-5218-470A-944A-7B221E1BF64D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b88fa9291ce64fcc8c94510bd09bed31e7b7f96
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313746"
---
# <a name="firstbit-sm5---asm"></a><span data-ttu-id="e8db6-103">firstbit (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e8db6-103">firstbit (sm5 - asm)</span></span>

<span data-ttu-id="e8db6-104">Sucht das erste Bit, das in einer Zahl festgelegt ist, entweder von der LSB oder von MSB.</span><span class="sxs-lookup"><span data-stu-id="e8db6-104">Finds the first bit set in a number, either from LSB or MSB.</span></span>



| <span data-ttu-id="e8db6-105">firstbit { \_ Hi </span><span class="sxs-lookup"><span data-stu-id="e8db6-105">firstbit{\_hi</span></span>\|<span data-ttu-id="e8db6-106">\_Siehe</span><span class="sxs-lookup"><span data-stu-id="e8db6-106">\_lo\</span></span>|<span data-ttu-id="e8db6-107">\_Shi} dest \[ . mask \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="e8db6-107">\_shi} dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="e8db6-108">Element</span><span class="sxs-lookup"><span data-stu-id="e8db6-108">Item</span></span>                                                            | <span data-ttu-id="e8db6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8db6-109">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8db6-110"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="e8db6-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="e8db6-111">\[an \] der ganzzahligen Position des ersten Bits, das in *src0* beginnt, beginnend mit dem LSB für firstbit \_ Lo oder MSB für firstbit \_ Hi.</span><span class="sxs-lookup"><span data-stu-id="e8db6-111">\[in\] The integer position of the first bit set in *src0* starting from the LSB for firstbit\_lo or MSB for firstbit\_hi.</span></span><br/> |
| <span data-ttu-id="e8db6-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e8db6-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="e8db6-113">\[in \] der Eingabe Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="e8db6-113">\[in\] The input integer.</span></span><br/>                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="e8db6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8db6-114">Remarks</span></span>

<span data-ttu-id="e8db6-115">Mit diesem Vorgang wird die ganzzahlige Position des ersten Bits in der 32-Bit-Eingabe ab dem LSB für firstbit \_ Lo oder MSB für firstbit Hi zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="e8db6-115">This operation returns the integer position of the first bit set in the 32-bit input starting from the LSB for firstbit\_lo or MSB for firstbit\_hi.</span></span> <span data-ttu-id="e8db6-116">Beispielsweise gibt firstbit \_ Lo on 0x00000001 den Wert 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="e8db6-116">For example firstbit\_lo on 0x00000001 returns 0.</span></span> <span data-ttu-id="e8db6-117">firstbit \_ HI auf 0x10000000 gibt 3 zurück.</span><span class="sxs-lookup"><span data-stu-id="e8db6-117">firstbit\_hi on 0x10000000 returns 3.</span></span>

<span data-ttu-id="e8db6-118">firstbit \_ Shi (s für signed) gibt das erste 0 aus dem MSB zurück, wenn die Zahl negativ ist. andernfalls wird die erste 1 vom MSB zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e8db6-118">firstbit\_shi (s for signed) returns the first 0 from the MSB if the number is negative; otherwise it returns the first 1 from the MSB.</span></span>

<span data-ttu-id="e8db6-119">Alle Varianten der Anweisung geben ~ 0 (0xFFFFFFFF in 32-Bit-Register) zurück, wenn keine Entsprechung gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e8db6-119">All variants of the instruction return ~0 (0xffffffff in 32-bit register) if no match is found.</span></span>

<span data-ttu-id="e8db6-120">Verwenden Sie diese Anweisung, um in einem Bitfeld schnell festgelegte Bits aufzulisten oder die größte Potenz von 2 in einer Zahl zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="e8db6-120">Use this instruction to quickly enumerate set bits in a bitfield, or find the largest power of 2 in a number.</span></span>

<span data-ttu-id="e8db6-121">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="e8db6-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e8db6-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="e8db6-122">Vertex</span></span> | <span data-ttu-id="e8db6-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="e8db6-123">Hull</span></span> | <span data-ttu-id="e8db6-124">Domain</span><span class="sxs-lookup"><span data-stu-id="e8db6-124">Domain</span></span> | <span data-ttu-id="e8db6-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="e8db6-125">Geometry</span></span> | <span data-ttu-id="e8db6-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="e8db6-126">Pixel</span></span> | <span data-ttu-id="e8db6-127">Compute</span><span class="sxs-lookup"><span data-stu-id="e8db6-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e8db6-128">X</span><span class="sxs-lookup"><span data-stu-id="e8db6-128">X</span></span>      | <span data-ttu-id="e8db6-129">X</span><span class="sxs-lookup"><span data-stu-id="e8db6-129">X</span></span>    | <span data-ttu-id="e8db6-130">X</span><span class="sxs-lookup"><span data-stu-id="e8db6-130">X</span></span>      | <span data-ttu-id="e8db6-131">X</span><span class="sxs-lookup"><span data-stu-id="e8db6-131">X</span></span>        | <span data-ttu-id="e8db6-132">X</span><span class="sxs-lookup"><span data-stu-id="e8db6-132">X</span></span>     | <span data-ttu-id="e8db6-133">X</span><span class="sxs-lookup"><span data-stu-id="e8db6-133">X</span></span>       |



 

## <a name="mimimum-shader-model"></a><span data-ttu-id="e8db6-134">Imies Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="e8db6-134">Mimimum Shader Model</span></span>

<span data-ttu-id="e8db6-135">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e8db6-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e8db6-136">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="e8db6-136">Shader Model</span></span>                                              | <span data-ttu-id="e8db6-137">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="e8db6-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e8db6-138">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="e8db6-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e8db6-139">ja</span><span class="sxs-lookup"><span data-stu-id="e8db6-139">yes</span></span>       |
| [<span data-ttu-id="e8db6-140">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="e8db6-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e8db6-141">nein</span><span class="sxs-lookup"><span data-stu-id="e8db6-141">no</span></span>        |
| [<span data-ttu-id="e8db6-142">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="e8db6-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e8db6-143">nein</span><span class="sxs-lookup"><span data-stu-id="e8db6-143">no</span></span>        |
| [<span data-ttu-id="e8db6-144">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8db6-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e8db6-145">nein</span><span class="sxs-lookup"><span data-stu-id="e8db6-145">no</span></span>        |
| [<span data-ttu-id="e8db6-146">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8db6-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e8db6-147">nein</span><span class="sxs-lookup"><span data-stu-id="e8db6-147">no</span></span>        |
| [<span data-ttu-id="e8db6-148">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8db6-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e8db6-149">nein</span><span class="sxs-lookup"><span data-stu-id="e8db6-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e8db6-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e8db6-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8db6-151">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8db6-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





