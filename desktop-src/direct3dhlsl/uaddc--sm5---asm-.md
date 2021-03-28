---
title: uaddc (SM5-ASM)
description: Ganzzahl ohne Vorzeichen mit "Carry" hinzufügen.
ms.assetid: 1007253C-F920-4003-B266-D124A255F731
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f57f75be617e32c15212207110851520a7a281e2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516484"
---
# <a name="uaddc-sm5---asm"></a><span data-ttu-id="89579-103">uaddc (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="89579-103">uaddc (sm5 - asm)</span></span>

<span data-ttu-id="89579-104">Ganzzahl ohne Vorzeichen mit "Carry" hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="89579-104">Unsigned integer add with carry.</span></span>



| <span data-ttu-id="89579-105">uaddc dest0 \[ . mask \] , dest1 \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="89579-105">uaddc dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="89579-106">Element</span><span class="sxs-lookup"><span data-stu-id="89579-106">Item</span></span>                                                               | <span data-ttu-id="89579-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89579-107">Description</span></span>                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="89579-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="89579-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="89579-109">\[\]die Adresse des Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="89579-109">\[in\] Address of the result.</span></span><br/>               |
| <span data-ttu-id="89579-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="89579-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="89579-111">\[in \] 1, wenn "Carry" erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="89579-111">\[in\] 1 if carry is produced.</span></span> <span data-ttu-id="89579-112">andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="89579-112">Otherwise 0.</span></span><br/> |
| <span data-ttu-id="89579-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="89579-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="89579-114">\[in \] 32-Bit-Operanden hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="89579-114">\[in\] 32-bit operand to be added.</span></span><br/>          |
| <span data-ttu-id="89579-115"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="89579-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="89579-116">\[in \] 32-Bit-Operanden hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="89579-116">\[in\] 32-bit operand to be added.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="89579-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89579-117">Remarks</span></span>

<span data-ttu-id="89579-118">*dest1* kann NULL sein, wenn der Carry nicht benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="89579-118">*dest1* can be NULL if the carry is not needed.</span></span>

<span data-ttu-id="89579-119">Verwenden Sie diese Anweisung für Berechnungen mit hoher Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="89579-119">Use this instruction for high precision arithmetic.</span></span>

<span data-ttu-id="89579-120">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="89579-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="89579-121">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="89579-121">Vertex</span></span> | <span data-ttu-id="89579-122">Hülle</span><span class="sxs-lookup"><span data-stu-id="89579-122">Hull</span></span> | <span data-ttu-id="89579-123">Domain</span><span class="sxs-lookup"><span data-stu-id="89579-123">Domain</span></span> | <span data-ttu-id="89579-124">Geometrie</span><span class="sxs-lookup"><span data-stu-id="89579-124">Geometry</span></span> | <span data-ttu-id="89579-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="89579-125">Pixel</span></span> | <span data-ttu-id="89579-126">Compute</span><span class="sxs-lookup"><span data-stu-id="89579-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="89579-127">X</span><span class="sxs-lookup"><span data-stu-id="89579-127">X</span></span>      | <span data-ttu-id="89579-128">X</span><span class="sxs-lookup"><span data-stu-id="89579-128">X</span></span>    | <span data-ttu-id="89579-129">X</span><span class="sxs-lookup"><span data-stu-id="89579-129">X</span></span>      | <span data-ttu-id="89579-130">X</span><span class="sxs-lookup"><span data-stu-id="89579-130">X</span></span>        | <span data-ttu-id="89579-131">X</span><span class="sxs-lookup"><span data-stu-id="89579-131">X</span></span>     | <span data-ttu-id="89579-132">X</span><span class="sxs-lookup"><span data-stu-id="89579-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="89579-133">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="89579-133">Minimum Shader Model</span></span>

<span data-ttu-id="89579-134">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="89579-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="89579-135">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="89579-135">Shader Model</span></span>                                              | <span data-ttu-id="89579-136">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="89579-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="89579-137">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="89579-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="89579-138">ja</span><span class="sxs-lookup"><span data-stu-id="89579-138">yes</span></span>       |
| [<span data-ttu-id="89579-139">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="89579-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="89579-140">nein</span><span class="sxs-lookup"><span data-stu-id="89579-140">no</span></span>        |
| [<span data-ttu-id="89579-141">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="89579-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="89579-142">nein</span><span class="sxs-lookup"><span data-stu-id="89579-142">no</span></span>        |
| [<span data-ttu-id="89579-143">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="89579-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="89579-144">nein</span><span class="sxs-lookup"><span data-stu-id="89579-144">no</span></span>        |
| [<span data-ttu-id="89579-145">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="89579-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="89579-146">nein</span><span class="sxs-lookup"><span data-stu-id="89579-146">no</span></span>        |
| [<span data-ttu-id="89579-147">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="89579-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="89579-148">nein</span><span class="sxs-lookup"><span data-stu-id="89579-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="89579-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="89579-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89579-150">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="89579-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





