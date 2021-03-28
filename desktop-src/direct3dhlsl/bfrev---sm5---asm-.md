---
title: bfrev (SM5-ASM)
description: Umkehren einer 32-Bit-Zahl.
ms.assetid: 24F8209A-093E-4737-BF50-12F228024E9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11bf0f07b6c66babf8e7f91108f86ba753420fc2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993119"
---
# <a name="bfrev-sm5---asm"></a><span data-ttu-id="1242a-103">bfrev (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1242a-103">bfrev (sm5 - asm)</span></span>

<span data-ttu-id="1242a-104">Umkehren einer 32-Bit-Zahl.</span><span class="sxs-lookup"><span data-stu-id="1242a-104">Reverse a 32-bit number.</span></span>



| <span data-ttu-id="1242a-105">bfrev dest \[ . mask \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="1242a-105">bfrev dest\[.mask\], src0\[.swizzle\]</span></span> |
|---------------------------------------|



 



| <span data-ttu-id="1242a-106">Element</span><span class="sxs-lookup"><span data-stu-id="1242a-106">Item</span></span>                                                            | <span data-ttu-id="1242a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1242a-107">Description</span></span>                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="1242a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1242a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1242a-109">\[in \] der Adresse für *src0* mit umgekehrter Bits.</span><span class="sxs-lookup"><span data-stu-id="1242a-109">\[in\] The address for *src0* with bits reversed.</span></span><br/> |
| <span data-ttu-id="1242a-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1242a-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1242a-111">\[in \] der 32-Bit-Zahl, die umgekehrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1242a-111">\[in\] The 32-bit number to reverse.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="1242a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1242a-112">Remarks</span></span>

<span data-ttu-id="1242a-113">Bei Angabe von 0x12345678 wäre das Ergebnis z. b. 0x1e6a2c48.</span><span class="sxs-lookup"><span data-stu-id="1242a-113">For example, given 0x12345678 the result would be 0x1e6a2c48.</span></span>

<span data-ttu-id="1242a-114">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="1242a-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1242a-115">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="1242a-115">Vertex</span></span> | <span data-ttu-id="1242a-116">Hülle</span><span class="sxs-lookup"><span data-stu-id="1242a-116">Hull</span></span> | <span data-ttu-id="1242a-117">Domain</span><span class="sxs-lookup"><span data-stu-id="1242a-117">Domain</span></span> | <span data-ttu-id="1242a-118">Geometrie</span><span class="sxs-lookup"><span data-stu-id="1242a-118">Geometry</span></span> | <span data-ttu-id="1242a-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="1242a-119">Pixel</span></span> | <span data-ttu-id="1242a-120">Compute</span><span class="sxs-lookup"><span data-stu-id="1242a-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1242a-121">X</span><span class="sxs-lookup"><span data-stu-id="1242a-121">X</span></span>      | <span data-ttu-id="1242a-122">X</span><span class="sxs-lookup"><span data-stu-id="1242a-122">X</span></span>    | <span data-ttu-id="1242a-123">X</span><span class="sxs-lookup"><span data-stu-id="1242a-123">X</span></span>      | <span data-ttu-id="1242a-124">X</span><span class="sxs-lookup"><span data-stu-id="1242a-124">X</span></span>        | <span data-ttu-id="1242a-125">X</span><span class="sxs-lookup"><span data-stu-id="1242a-125">X</span></span>     | <span data-ttu-id="1242a-126">X</span><span class="sxs-lookup"><span data-stu-id="1242a-126">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1242a-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="1242a-127">Minimum Shader Model</span></span>

<span data-ttu-id="1242a-128">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1242a-128">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1242a-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="1242a-129">Shader Model</span></span>                                              | <span data-ttu-id="1242a-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="1242a-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1242a-131">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="1242a-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1242a-132">ja</span><span class="sxs-lookup"><span data-stu-id="1242a-132">yes</span></span>       |
| [<span data-ttu-id="1242a-133">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="1242a-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1242a-134">nein</span><span class="sxs-lookup"><span data-stu-id="1242a-134">no</span></span>        |
| [<span data-ttu-id="1242a-135">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="1242a-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1242a-136">nein</span><span class="sxs-lookup"><span data-stu-id="1242a-136">no</span></span>        |
| [<span data-ttu-id="1242a-137">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1242a-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1242a-138">nein</span><span class="sxs-lookup"><span data-stu-id="1242a-138">no</span></span>        |
| [<span data-ttu-id="1242a-139">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1242a-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1242a-140">nein</span><span class="sxs-lookup"><span data-stu-id="1242a-140">no</span></span>        |
| [<span data-ttu-id="1242a-141">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1242a-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1242a-142">nein</span><span class="sxs-lookup"><span data-stu-id="1242a-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1242a-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1242a-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1242a-144">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1242a-144">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





