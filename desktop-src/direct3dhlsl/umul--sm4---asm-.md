---
title: Umul (SM4-ASM)
description: Ganzzahl ohne Vorzeichen multiplizieren.
ms.assetid: C84AF349-32E6-40C4-9973-BCFA73EFBF0B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581696ef5aa7d027c30b4ae866d06401275ef4bc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389534"
---
# <a name="umul-sm4---asm"></a><span data-ttu-id="827e3-103">Umul (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="827e3-103">umul (sm4 - asm)</span></span>

<span data-ttu-id="827e3-104">Ganzzahl ohne Vorzeichen multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="827e3-104">Unsigned integer multiply.</span></span>



| <span data-ttu-id="827e3-105">Umul desthi \[ . mask \] , destlo \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="827e3-105">umul destHI\[.mask\], destLO\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------|



 



| <span data-ttu-id="827e3-106">Element</span><span class="sxs-lookup"><span data-stu-id="827e3-106">Item</span></span>                                                                                           | <span data-ttu-id="827e3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="827e3-107">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="827e3-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*desthi*</span><span class="sxs-lookup"><span data-stu-id="827e3-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span></span><br/> | <span data-ttu-id="827e3-109">\[in \] den hohen 32 Bits des Ergebnisses pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="827e3-109">\[in\] The high 32 bits of the result, per component.</span></span><br/> |
| <span data-ttu-id="827e3-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destlo*</span><span class="sxs-lookup"><span data-stu-id="827e3-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span></span><br/> | <span data-ttu-id="827e3-111">\[in \] den unteren 32 Bits des Ergebnisses pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="827e3-111">\[in\] The low 32 bits of the result, per component.</span></span><br/>  |
| <span data-ttu-id="827e3-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="827e3-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                | <span data-ttu-id="827e3-113">\[in \] den Komponenten, nach denen *Quelle1* multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="827e3-113">\[in\] The components by which to multiply *src1*.</span></span><br/>    |
| <span data-ttu-id="827e3-114"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="827e3-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                | <span data-ttu-id="827e3-115">\[in \] den Komponenten, nach denen *src0* multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="827e3-115">\[in\] The components by which to multiply *src0*.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="827e3-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="827e3-116">Remarks</span></span>

<span data-ttu-id="827e3-117">Diese Anweisung führt eine Komponenten Weise Multiplikation von nicht signierten 32-Bit-Operanden *src0* und *Quelle1* aus und erzeugt das korrekte vollständige 64-Bit-Ergebnis pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="827e3-117">This instruction performs a component-wise multiply of unsigned 32-bit operands *src0* and *src1*, producing the correct full 64-bit result per component.</span></span> <span data-ttu-id="827e3-118">Die unteren 32 Bits pro Komponente werden in " *destlo*" platziert.</span><span class="sxs-lookup"><span data-stu-id="827e3-118">The low 32 bits per component are placed in *destLO*.</span></span> <span data-ttu-id="827e3-119">Die hohen 32 Bits pro Komponente werden in *desthi* platziert.</span><span class="sxs-lookup"><span data-stu-id="827e3-119">The high 32 bits per component are placed in *destHI*.</span></span>

<span data-ttu-id="827e3-120">Sie können entweder *desthi* oder *destlo* als NULL angeben, anstatt ein Register anzugeben, wenn die hohen oder unteren 32 Bits des 64-Bit-Ergebnisses nicht benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="827e3-120">You can specify either *destHI* or *destLO* as NULL instead of specifying a register if the high or low 32 bits of the 64-bit result are not needed.</span></span>

<span data-ttu-id="827e3-121">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="827e3-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="827e3-122">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="827e3-122">Vertex Shader</span></span> | <span data-ttu-id="827e3-123">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="827e3-123">Geometry Shader</span></span> | <span data-ttu-id="827e3-124">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="827e3-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="827e3-125">x</span><span class="sxs-lookup"><span data-stu-id="827e3-125">x</span></span>             | <span data-ttu-id="827e3-126">x</span><span class="sxs-lookup"><span data-stu-id="827e3-126">x</span></span>               | <span data-ttu-id="827e3-127">x</span><span class="sxs-lookup"><span data-stu-id="827e3-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="827e3-128">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="827e3-128">Minimum Shader Model</span></span>

<span data-ttu-id="827e3-129">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="827e3-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="827e3-130">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="827e3-130">Shader Model</span></span>                                              | <span data-ttu-id="827e3-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="827e3-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="827e3-132">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="827e3-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="827e3-133">ja</span><span class="sxs-lookup"><span data-stu-id="827e3-133">yes</span></span>       |
| [<span data-ttu-id="827e3-134">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="827e3-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="827e3-135">ja</span><span class="sxs-lookup"><span data-stu-id="827e3-135">yes</span></span>       |
| [<span data-ttu-id="827e3-136">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="827e3-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="827e3-137">ja</span><span class="sxs-lookup"><span data-stu-id="827e3-137">yes</span></span>       |
| [<span data-ttu-id="827e3-138">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="827e3-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="827e3-139">nein</span><span class="sxs-lookup"><span data-stu-id="827e3-139">no</span></span>        |
| [<span data-ttu-id="827e3-140">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="827e3-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="827e3-141">nein</span><span class="sxs-lookup"><span data-stu-id="827e3-141">no</span></span>        |
| [<span data-ttu-id="827e3-142">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="827e3-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="827e3-143">nein</span><span class="sxs-lookup"><span data-stu-id="827e3-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="827e3-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="827e3-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="827e3-145">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="827e3-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





