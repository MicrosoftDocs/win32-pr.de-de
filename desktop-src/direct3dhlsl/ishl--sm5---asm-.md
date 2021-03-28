---
title: ishl (sm5 - asm)
description: Nach links verschieben. | ishl (SM5-ASM)
ms.assetid: 3EE669BA-252D-4617-85B0-AEBB7F7E4C5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230034e66ca9adfbd6c94cc99351b485c6577fdf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353128"
---
# <a name="ishl-sm5---asm"></a><span data-ttu-id="c239e-104">ishl (sm5 - asm)</span><span class="sxs-lookup"><span data-stu-id="c239e-104">ishl (sm5 - asm)</span></span>

<span data-ttu-id="c239e-105">Nach links verschieben.</span><span class="sxs-lookup"><span data-stu-id="c239e-105">Shift left.</span></span>



| <span data-ttu-id="c239e-106">ishl dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c239e-106">ishl dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="c239e-107">Element</span><span class="sxs-lookup"><span data-stu-id="c239e-107">Item</span></span>                                                            | <span data-ttu-id="c239e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c239e-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c239e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c239e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c239e-110">\[in \] enthält die Ergebnisse der Verschiebung.</span><span class="sxs-lookup"><span data-stu-id="c239e-110">\[in\] Contains the results of the shift.</span></span><br/> |
| <span data-ttu-id="c239e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c239e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c239e-112">\[in \] den 32-Bit-Werten, die verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c239e-112">\[in\] The 32-bit values to shift.</span></span><br/>       |
| <span data-ttu-id="c239e-113"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="c239e-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="c239e-114">\[in \] der Anzahl von Bits, die verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c239e-114">\[in\] The number of bits to shift.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="c239e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c239e-115">Remarks</span></span>

<span data-ttu-id="c239e-116">Diese Anweisung führt eine Komponenten Weise Verschiebung jedes 32-Bit-Werts in *src0* nach links durch eine ganzzahlige Bitzahl ohne Vorzeichen aus, die von der LSB 5 Bits (0-31 Range) in *Quelle1* bereitgestellt wird, wobei 0 eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c239e-116">This instruction performs a component-wise shift of each 32-bit value in *src0* left by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, inserting 0.</span></span> <span data-ttu-id="c239e-117">Die 32-Bit-pro-Komponenten Ergebnisse werden in *dest* platziert.</span><span class="sxs-lookup"><span data-stu-id="c239e-117">The 32-bit per component results are placed in *dest*.</span></span>

<span data-ttu-id="c239e-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="c239e-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c239e-119">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c239e-119">Vertex</span></span> | <span data-ttu-id="c239e-120">Hülle</span><span class="sxs-lookup"><span data-stu-id="c239e-120">Hull</span></span> | <span data-ttu-id="c239e-121">Domain</span><span class="sxs-lookup"><span data-stu-id="c239e-121">Domain</span></span> | <span data-ttu-id="c239e-122">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c239e-122">Geometry</span></span> | <span data-ttu-id="c239e-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="c239e-123">Pixel</span></span> | <span data-ttu-id="c239e-124">Compute</span><span class="sxs-lookup"><span data-stu-id="c239e-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c239e-125">X</span><span class="sxs-lookup"><span data-stu-id="c239e-125">X</span></span>      | <span data-ttu-id="c239e-126">X</span><span class="sxs-lookup"><span data-stu-id="c239e-126">X</span></span>    | <span data-ttu-id="c239e-127">X</span><span class="sxs-lookup"><span data-stu-id="c239e-127">X</span></span>      | <span data-ttu-id="c239e-128">X</span><span class="sxs-lookup"><span data-stu-id="c239e-128">X</span></span>        | <span data-ttu-id="c239e-129">X</span><span class="sxs-lookup"><span data-stu-id="c239e-129">X</span></span>     | <span data-ttu-id="c239e-130">X</span><span class="sxs-lookup"><span data-stu-id="c239e-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c239e-131">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c239e-131">Minimum Shader Model</span></span>

<span data-ttu-id="c239e-132">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c239e-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c239e-133">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c239e-133">Shader Model</span></span>                                              | <span data-ttu-id="c239e-134">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c239e-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c239e-135">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="c239e-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c239e-136">ja</span><span class="sxs-lookup"><span data-stu-id="c239e-136">yes</span></span>       |
| [<span data-ttu-id="c239e-137">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="c239e-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c239e-138">nein</span><span class="sxs-lookup"><span data-stu-id="c239e-138">no</span></span>        |
| [<span data-ttu-id="c239e-139">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="c239e-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c239e-140">nein</span><span class="sxs-lookup"><span data-stu-id="c239e-140">no</span></span>        |
| [<span data-ttu-id="c239e-141">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c239e-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c239e-142">nein</span><span class="sxs-lookup"><span data-stu-id="c239e-142">no</span></span>        |
| [<span data-ttu-id="c239e-143">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c239e-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c239e-144">nein</span><span class="sxs-lookup"><span data-stu-id="c239e-144">no</span></span>        |
| [<span data-ttu-id="c239e-145">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c239e-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c239e-146">nein</span><span class="sxs-lookup"><span data-stu-id="c239e-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c239e-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c239e-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c239e-148">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c239e-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





