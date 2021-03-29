---
title: ushr (SM5-ASM)
description: Nach rechts verschieben. | ushr (SM5-ASM)
ms.assetid: C695CB6C-A6C9-4DC8-8EBE-70A0CFFC4981
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33c627ec4aa985b5ac8a27cf0babd6219c9247c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981688"
---
# <a name="ushr-sm5---asm"></a><span data-ttu-id="f6200-104">ushr (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f6200-104">ushr (sm5 - asm)</span></span>

<span data-ttu-id="f6200-105">Nach rechts verschieben.</span><span class="sxs-lookup"><span data-stu-id="f6200-105">Shift right.</span></span>



| <span data-ttu-id="f6200-106">ubfe dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="f6200-106">ubfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="f6200-107">Element</span><span class="sxs-lookup"><span data-stu-id="f6200-107">Item</span></span>                                                            | <span data-ttu-id="f6200-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6200-108">Description</span></span>                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f6200-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f6200-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f6200-110">\[in \] enthält die Ergebnisse der-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="f6200-110">\[in\] Contains the results of the instruction.</span></span><br/>                   |
| <span data-ttu-id="f6200-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f6200-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f6200-112">\[in \] den 32-Bit-Werten, die verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f6200-112">\[in\] The 32-bit values to shift.</span></span><br/>                                |
| <span data-ttu-id="f6200-113"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="f6200-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="f6200-114">\[\]Geben Sie in den lsb 5 Bits die Anzahl der zu Verschiebungs enden Bits (0-31) an.</span><span class="sxs-lookup"><span data-stu-id="f6200-114">\[in\] The LSB 5 bits provide the number of bits to shift (0-31).</span></span><br/> |



 

<span data-ttu-id="f6200-115">Diese Anweisung führt eine Komponenten Weise Verschiebung jedes 32-Bit-Werts in *src0* rechts durch eine ganzzahlige Bitzahl ohne Vorzeichen aus, die von der LSB 5 Bits (0-31 Range) in *Quelle1* bereitgestellt wird, wobei 0 eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f6200-115">This instruction performs a component-wise shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, inserting 0.</span></span> <span data-ttu-id="f6200-116">Das 32-Bit pro Komponenten Ergebnis wird in *dest* platziert.</span><span class="sxs-lookup"><span data-stu-id="f6200-116">The 32-bit per component results is placed in *dest*.</span></span>

<span data-ttu-id="f6200-117">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="f6200-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f6200-118">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="f6200-118">Vertex</span></span> | <span data-ttu-id="f6200-119">Hülle</span><span class="sxs-lookup"><span data-stu-id="f6200-119">Hull</span></span> | <span data-ttu-id="f6200-120">Domain</span><span class="sxs-lookup"><span data-stu-id="f6200-120">Domain</span></span> | <span data-ttu-id="f6200-121">Geometrie</span><span class="sxs-lookup"><span data-stu-id="f6200-121">Geometry</span></span> | <span data-ttu-id="f6200-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="f6200-122">Pixel</span></span> | <span data-ttu-id="f6200-123">Compute</span><span class="sxs-lookup"><span data-stu-id="f6200-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f6200-124">X</span><span class="sxs-lookup"><span data-stu-id="f6200-124">X</span></span>      | <span data-ttu-id="f6200-125">X</span><span class="sxs-lookup"><span data-stu-id="f6200-125">X</span></span>    | <span data-ttu-id="f6200-126">X</span><span class="sxs-lookup"><span data-stu-id="f6200-126">X</span></span>      | <span data-ttu-id="f6200-127">X</span><span class="sxs-lookup"><span data-stu-id="f6200-127">X</span></span>        | <span data-ttu-id="f6200-128">X</span><span class="sxs-lookup"><span data-stu-id="f6200-128">X</span></span>     | <span data-ttu-id="f6200-129">X</span><span class="sxs-lookup"><span data-stu-id="f6200-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f6200-130">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="f6200-130">Minimum Shader Model</span></span>

<span data-ttu-id="f6200-131">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f6200-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f6200-132">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="f6200-132">Shader Model</span></span>                                              | <span data-ttu-id="f6200-133">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="f6200-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f6200-134">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="f6200-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f6200-135">ja</span><span class="sxs-lookup"><span data-stu-id="f6200-135">yes</span></span>       |
| [<span data-ttu-id="f6200-136">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="f6200-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f6200-137">nein</span><span class="sxs-lookup"><span data-stu-id="f6200-137">no</span></span>        |
| [<span data-ttu-id="f6200-138">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="f6200-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f6200-139">nein</span><span class="sxs-lookup"><span data-stu-id="f6200-139">no</span></span>        |
| [<span data-ttu-id="f6200-140">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6200-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f6200-141">nein</span><span class="sxs-lookup"><span data-stu-id="f6200-141">no</span></span>        |
| [<span data-ttu-id="f6200-142">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6200-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f6200-143">nein</span><span class="sxs-lookup"><span data-stu-id="f6200-143">no</span></span>        |
| [<span data-ttu-id="f6200-144">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6200-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f6200-145">nein</span><span class="sxs-lookup"><span data-stu-id="f6200-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f6200-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f6200-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6200-147">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6200-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





