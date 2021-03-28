---
title: ISHR (SM5-ASM)
description: Arithmetische UMSCHALT Rechte (Zeichen Erweiterung). | ISHR (SM5-ASM)
ms.assetid: 8124B6C3-4576-4616-85A9-A2DD19EB6BB9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06df958b2e5c6e9cdd2a4dfb3d35c8112453ce9f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995728"
---
# <a name="ishr-sm5---asm"></a><span data-ttu-id="911f0-104">ISHR (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="911f0-104">ishr (sm5 - asm)</span></span>

<span data-ttu-id="911f0-105">Arithmetische UMSCHALT Rechte (Zeichen Erweiterung).</span><span class="sxs-lookup"><span data-stu-id="911f0-105">Arithmetic shift right (sign extending).</span></span>



| <span data-ttu-id="911f0-106">ishl dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="911f0-106">ishl dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="911f0-107">Element</span><span class="sxs-lookup"><span data-stu-id="911f0-107">Item</span></span>                                                            | <span data-ttu-id="911f0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="911f0-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="911f0-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="911f0-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="911f0-110">\[in \] enthält die Ergebnisse der Verschiebung.</span><span class="sxs-lookup"><span data-stu-id="911f0-110">\[in\] Contains the results of the shift.</span></span><br/> |
| <span data-ttu-id="911f0-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="911f0-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="911f0-112">\[in \] der Anzahl von Bits, die verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="911f0-112">\[in\] The number of bits to shift.</span></span><br/>       |
| <span data-ttu-id="911f0-113"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="911f0-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="911f0-114">\[in \] den 32-Bit-Werten, die verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="911f0-114">\[in\] The 32-bit values to shift.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="911f0-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="911f0-115">Remarks</span></span>

<span data-ttu-id="911f0-116">Diese Anweisung führt eine Komponenten Weise arithmetische Verschiebung jedes 32-Bit-Werts in *src0* rechts durch eine ganzzahlige Bitzahl ohne Vorzeichen aus, die von der LSB 5 Bits (0-31 Range) in *Quelle1* bereitgestellt wird, wobei der Wert von Bit 31 replizieren wird.</span><span class="sxs-lookup"><span data-stu-id="911f0-116">This instruction performs a component-wise arithmetic shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, replicating the value of bit 31.</span></span> <span data-ttu-id="911f0-117">Das 32-Bit pro Komponenten Ergebnis wird in *dest* platziert.</span><span class="sxs-lookup"><span data-stu-id="911f0-117">The 32-bit per component result is placed in *dest*.</span></span>

<span data-ttu-id="911f0-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="911f0-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="911f0-119">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="911f0-119">Vertex</span></span> | <span data-ttu-id="911f0-120">Hülle</span><span class="sxs-lookup"><span data-stu-id="911f0-120">Hull</span></span> | <span data-ttu-id="911f0-121">Domain</span><span class="sxs-lookup"><span data-stu-id="911f0-121">Domain</span></span> | <span data-ttu-id="911f0-122">Geometrie</span><span class="sxs-lookup"><span data-stu-id="911f0-122">Geometry</span></span> | <span data-ttu-id="911f0-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="911f0-123">Pixel</span></span> | <span data-ttu-id="911f0-124">Compute</span><span class="sxs-lookup"><span data-stu-id="911f0-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="911f0-125">X</span><span class="sxs-lookup"><span data-stu-id="911f0-125">X</span></span>      | <span data-ttu-id="911f0-126">X</span><span class="sxs-lookup"><span data-stu-id="911f0-126">X</span></span>    | <span data-ttu-id="911f0-127">X</span><span class="sxs-lookup"><span data-stu-id="911f0-127">X</span></span>      | <span data-ttu-id="911f0-128">X</span><span class="sxs-lookup"><span data-stu-id="911f0-128">X</span></span>        | <span data-ttu-id="911f0-129">X</span><span class="sxs-lookup"><span data-stu-id="911f0-129">X</span></span>     | <span data-ttu-id="911f0-130">X</span><span class="sxs-lookup"><span data-stu-id="911f0-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="911f0-131">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="911f0-131">Minimum Shader Model</span></span>

<span data-ttu-id="911f0-132">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="911f0-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="911f0-133">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="911f0-133">Shader Model</span></span>                                              | <span data-ttu-id="911f0-134">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="911f0-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="911f0-135">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="911f0-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="911f0-136">ja</span><span class="sxs-lookup"><span data-stu-id="911f0-136">yes</span></span>       |
| [<span data-ttu-id="911f0-137">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="911f0-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="911f0-138">nein</span><span class="sxs-lookup"><span data-stu-id="911f0-138">no</span></span>        |
| [<span data-ttu-id="911f0-139">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="911f0-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="911f0-140">nein</span><span class="sxs-lookup"><span data-stu-id="911f0-140">no</span></span>        |
| [<span data-ttu-id="911f0-141">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="911f0-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="911f0-142">nein</span><span class="sxs-lookup"><span data-stu-id="911f0-142">no</span></span>        |
| [<span data-ttu-id="911f0-143">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="911f0-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="911f0-144">nein</span><span class="sxs-lookup"><span data-stu-id="911f0-144">no</span></span>        |
| [<span data-ttu-id="911f0-145">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="911f0-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="911f0-146">nein</span><span class="sxs-lookup"><span data-stu-id="911f0-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="911f0-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="911f0-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="911f0-148">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="911f0-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





