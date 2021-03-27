---
title: imul (SM4-ASM)
description: Ganze Zahl mit Vorzeichen multipliziert.
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f62fc389ad1e0fb6b23dd6c419ff8b3933b41
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719422"
---
# <a name="imul-sm4---asm"></a><span data-ttu-id="dde4e-103">imul (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="dde4e-103">imul (sm4 - asm)</span></span>

<span data-ttu-id="dde4e-104">Ganze Zahl mit Vorzeichen multipliziert.</span><span class="sxs-lookup"><span data-stu-id="dde4e-104">Signed integer multiply.</span></span>



| <span data-ttu-id="dde4e-105">imul desthi \[ . mask \] , destlo \[ . mask \] , \[ - \] src0 \[ . Swizzle \] , \[ - \] Quelle1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="dde4e-105">imul destHI\[.mask\], destLO\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------|



 



| <span data-ttu-id="dde4e-106">Element</span><span class="sxs-lookup"><span data-stu-id="dde4e-106">Item</span></span>                                                                                           | <span data-ttu-id="dde4e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dde4e-107">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="dde4e-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*desthi*</span><span class="sxs-lookup"><span data-stu-id="dde4e-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span></span><br/> | <span data-ttu-id="dde4e-109">\[in \] der Adresse der hohen 32 Bits des Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="dde4e-109">\[in\] The address of the high 32 bits of the result.</span></span><br/> |
| <span data-ttu-id="dde4e-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destlo*</span><span class="sxs-lookup"><span data-stu-id="dde4e-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span></span><br/> | <span data-ttu-id="dde4e-111">\[in \] der Adresse der unteren 32 Bits des Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="dde4e-111">\[in\] The address of the low 32 bits of the result.</span></span><br/>  |
| <span data-ttu-id="dde4e-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="dde4e-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                | <span data-ttu-id="dde4e-113">\[im \] Wert, der mit *Quelle1* multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="dde4e-113">\[in\] The value to multiply with *src1*.</span></span><br/>             |
| <span data-ttu-id="dde4e-114"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="dde4e-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                | <span data-ttu-id="dde4e-115">\[im \] Wert, der mit *src0* multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="dde4e-115">\[in\] The value to multiply with *src0*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="dde4e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dde4e-116">Remarks</span></span>

<span data-ttu-id="dde4e-117">Die Komponenten Weise Multiplikation von 32-Bit-Operanden *src0* und *Quelle1* (beide sind signiert), wodurch das korrekte vollständige 64-Bit-Ergebnis (pro Komponente) erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="dde4e-117">Component-wise multiply of 32-bit operands *src0* and *src1* (both are signed), producing the correct full 64-bit (per component) result.</span></span> <span data-ttu-id="dde4e-118">Die unteren 32 Bits (pro Komponente) werden in *destlo* abgelegt.</span><span class="sxs-lookup"><span data-stu-id="dde4e-118">The low 32 bits (per component) are placed in *destLO*.</span></span> <span data-ttu-id="dde4e-119">Die hohen 32 Bits (pro Komponente) werden in *desthi* platziert.</span><span class="sxs-lookup"><span data-stu-id="dde4e-119">The high 32 bits (per component) are placed in *destHI*.</span></span>

<span data-ttu-id="dde4e-120">Entweder *desthi* oder *destlo* kann als NULL angegeben werden, anstatt ein Register anzugeben, wenn die hohen oder unteren 32 Bits des 64-Bit-Ergebnisses nicht benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="dde4e-120">Either *destHI* or *destLO* may be specified as NULL instead of specifying a register, if the high or low 32 bits of the 64-bit result are not needed.</span></span>

<span data-ttu-id="dde4e-121">Der optionale Negation-Modifizierer für Quell Operanden nimmt vor dem Ausführen arithmetischer Operationen eine Ergänzung von 2.</span><span class="sxs-lookup"><span data-stu-id="dde4e-121">Optional negate modifier on source operands takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="dde4e-122">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="dde4e-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="dde4e-123">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="dde4e-123">Vertex Shader</span></span> | <span data-ttu-id="dde4e-124">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="dde4e-124">Geometry Shader</span></span> | <span data-ttu-id="dde4e-125">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="dde4e-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="dde4e-126">x</span><span class="sxs-lookup"><span data-stu-id="dde4e-126">x</span></span>             | <span data-ttu-id="dde4e-127">x</span><span class="sxs-lookup"><span data-stu-id="dde4e-127">x</span></span>               | <span data-ttu-id="dde4e-128">x</span><span class="sxs-lookup"><span data-stu-id="dde4e-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dde4e-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="dde4e-129">Minimum Shader Model</span></span>

<span data-ttu-id="dde4e-130">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dde4e-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dde4e-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="dde4e-131">Shader Model</span></span>                                              | <span data-ttu-id="dde4e-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="dde4e-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="dde4e-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="dde4e-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="dde4e-134">ja</span><span class="sxs-lookup"><span data-stu-id="dde4e-134">yes</span></span>       |
| [<span data-ttu-id="dde4e-135">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="dde4e-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="dde4e-136">ja</span><span class="sxs-lookup"><span data-stu-id="dde4e-136">yes</span></span>       |
| [<span data-ttu-id="dde4e-137">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="dde4e-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="dde4e-138">ja</span><span class="sxs-lookup"><span data-stu-id="dde4e-138">yes</span></span>       |
| [<span data-ttu-id="dde4e-139">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dde4e-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="dde4e-140">nein</span><span class="sxs-lookup"><span data-stu-id="dde4e-140">no</span></span>        |
| [<span data-ttu-id="dde4e-141">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dde4e-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="dde4e-142">nein</span><span class="sxs-lookup"><span data-stu-id="dde4e-142">no</span></span>        |
| [<span data-ttu-id="dde4e-143">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dde4e-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="dde4e-144">nein</span><span class="sxs-lookup"><span data-stu-id="dde4e-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="dde4e-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dde4e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dde4e-146">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dde4e-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





