---
title: usubb (SM5-ASM)
description: Ganzzahl ohne Vorzeichen subtrahieren mit Auswahl.
ms.assetid: 6D42E3CA-5A37-4194-AB42-7A2337C5AB9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111ffd134a75b8cfe19f63597cd80655201359c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389498"
---
# <a name="usubb-sm5---asm"></a><span data-ttu-id="6e08f-103">usubb (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6e08f-103">usubb (sm5 - asm)</span></span>

<span data-ttu-id="6e08f-104">Ganzzahl ohne Vorzeichen subtrahieren mit Auswahl.</span><span class="sxs-lookup"><span data-stu-id="6e08f-104">Unsigned integer subtract with borrow.</span></span>



| <span data-ttu-id="6e08f-105">usubb dest0 \[ . mask \] , dest1 \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="6e08f-105">usubb dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="6e08f-106">Element</span><span class="sxs-lookup"><span data-stu-id="6e08f-106">Item</span></span>                                                               | <span data-ttu-id="6e08f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e08f-107">Description</span></span>                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e08f-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="6e08f-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="6e08f-109">\[in \] enthält die lsab-Ergebnisse der-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="6e08f-109">\[in\] Contains the LSAB results of the instruction.</span></span><br/>                                   |
| <span data-ttu-id="6e08f-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="6e08f-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="6e08f-111">\[in \] der entsprechenden Komponente von *dest0* , die angibt, ob eine einleihe erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6e08f-111">\[in\] The corresponding component of *dest0* that specifies if a borrow was produced.</span></span><br/> |
| <span data-ttu-id="6e08f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6e08f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="6e08f-113">\[in \] dem Wert, von dem subtrahiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e08f-113">\[in\] The value from which to subtract.</span></span><br/>                                               |
| <span data-ttu-id="6e08f-114"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="6e08f-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="6e08f-115">\[in \] der Menge, die von *src0* subtrahiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e08f-115">\[in\] The amount to subtract from *src0*.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="6e08f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e08f-116">Remarks</span></span>

<span data-ttu-id="6e08f-117">Diese Anweisung führt eine Komponenten Weise nicht signierte Subtraktion von 32-Bit-Operanden aus *Quelle1* von *src0*, wobei der LSB-Teil des 32-Bit-Ergebnisses in *dest0* platziert wird.</span><span class="sxs-lookup"><span data-stu-id="6e08f-117">This instruction performs a component-wise unsigned subtract of 32-bit operands *src1* from *src0*, placing the LSB part of the 32-bit result in *dest0*.</span></span>

<span data-ttu-id="6e08f-118">Die entsprechende Komponente in *dest1* wird mit 1 geschrieben, wenn eine Kredit Erstellung erstellt wird, andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="6e08f-118">The corresponding component in *dest1* is written with 1 if a borrow is produced, 0 otherwise.</span></span>

<span data-ttu-id="6e08f-119">*dest1* kann NULL sein, wenn die unter Leihe nicht benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="6e08f-119">*dest1* can be NULL if the borrow is not needed.</span></span>

<span data-ttu-id="6e08f-120">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="6e08f-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6e08f-121">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="6e08f-121">Vertex</span></span> | <span data-ttu-id="6e08f-122">Hülle</span><span class="sxs-lookup"><span data-stu-id="6e08f-122">Hull</span></span> | <span data-ttu-id="6e08f-123">Domain</span><span class="sxs-lookup"><span data-stu-id="6e08f-123">Domain</span></span> | <span data-ttu-id="6e08f-124">Geometrie</span><span class="sxs-lookup"><span data-stu-id="6e08f-124">Geometry</span></span> | <span data-ttu-id="6e08f-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="6e08f-125">Pixel</span></span> | <span data-ttu-id="6e08f-126">Compute</span><span class="sxs-lookup"><span data-stu-id="6e08f-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6e08f-127">X</span><span class="sxs-lookup"><span data-stu-id="6e08f-127">X</span></span>      | <span data-ttu-id="6e08f-128">X</span><span class="sxs-lookup"><span data-stu-id="6e08f-128">X</span></span>    | <span data-ttu-id="6e08f-129">X</span><span class="sxs-lookup"><span data-stu-id="6e08f-129">X</span></span>      | <span data-ttu-id="6e08f-130">X</span><span class="sxs-lookup"><span data-stu-id="6e08f-130">X</span></span>        | <span data-ttu-id="6e08f-131">X</span><span class="sxs-lookup"><span data-stu-id="6e08f-131">X</span></span>     | <span data-ttu-id="6e08f-132">X</span><span class="sxs-lookup"><span data-stu-id="6e08f-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6e08f-133">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="6e08f-133">Minimum Shader Model</span></span>

<span data-ttu-id="6e08f-134">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="6e08f-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6e08f-135">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="6e08f-135">Shader Model</span></span>                                              | <span data-ttu-id="6e08f-136">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="6e08f-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6e08f-137">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="6e08f-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6e08f-138">ja</span><span class="sxs-lookup"><span data-stu-id="6e08f-138">yes</span></span>       |
| [<span data-ttu-id="6e08f-139">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="6e08f-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6e08f-140">nein</span><span class="sxs-lookup"><span data-stu-id="6e08f-140">no</span></span>        |
| [<span data-ttu-id="6e08f-141">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="6e08f-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6e08f-142">nein</span><span class="sxs-lookup"><span data-stu-id="6e08f-142">no</span></span>        |
| [<span data-ttu-id="6e08f-143">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e08f-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6e08f-144">nein</span><span class="sxs-lookup"><span data-stu-id="6e08f-144">no</span></span>        |
| [<span data-ttu-id="6e08f-145">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e08f-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6e08f-146">nein</span><span class="sxs-lookup"><span data-stu-id="6e08f-146">no</span></span>        |
| [<span data-ttu-id="6e08f-147">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e08f-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6e08f-148">nein</span><span class="sxs-lookup"><span data-stu-id="6e08f-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6e08f-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6e08f-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e08f-150">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e08f-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





