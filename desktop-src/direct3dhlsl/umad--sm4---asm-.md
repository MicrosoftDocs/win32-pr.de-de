---
title: Umad (SM4-ASM)
description: Ganzzahl ohne Vorzeichen multiplizieren und hinzufügen.
ms.assetid: C0BE31CA-E01D-42C0-A660-E63727CE344F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce52925622cb2f6f7cf53dec0e3f6f65d3fdcb58
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719392"
---
# <a name="umad-sm4---asm"></a><span data-ttu-id="f86e3-103">Umad (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f86e3-103">umad (sm4 - asm)</span></span>

<span data-ttu-id="f86e3-104">Ganzzahl ohne Vorzeichen multiplizieren und hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f86e3-104">Unsigned integer multiply and add.</span></span>



| <span data-ttu-id="f86e3-105">Umad dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle \] , Quelle2 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="f86e3-105">umad dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="f86e3-106">Element</span><span class="sxs-lookup"><span data-stu-id="f86e3-106">Item</span></span>                                                            | <span data-ttu-id="f86e3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f86e3-107">Description</span></span>                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="f86e3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f86e3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f86e3-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="f86e3-109">\[in\] The address of the result of the operation.</span></span><br/>           |
| <span data-ttu-id="f86e3-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f86e3-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f86e3-111">\[im \] Wert, der mit *Quelle1* multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f86e3-111">\[in\] The value to multiply with *src1*.</span></span><br/>                    |
| <span data-ttu-id="f86e3-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="f86e3-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="f86e3-113">\[im \] Wert, der mit *Quelle1* multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f86e3-113">\[in\] The value to multiply with *src1*.</span></span><br/>                     |
| <span data-ttu-id="f86e3-114"><span id="src2"></span><span id="SRC2"></span>*Quelle2*</span><span class="sxs-lookup"><span data-stu-id="f86e3-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="f86e3-115">\[in \] dem Wert, der dem Produkt von *src0* und *Quelle1* hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f86e3-115">\[in\] The value to add to the product of *src0* and *src1*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f86e3-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f86e3-116">Remarks</span></span>

<span data-ttu-id="f86e3-117">Komponenten Weise [Umul](umul--sm4---asm-.md) der 32-Bit-Operanden *src0* und *Quelle1* ohne Vorzeichen, wobei die unteren 32 Bits pro Komponente des Ergebnisses beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="f86e3-117">Component-wise [umul](umul--sm4---asm-.md) of 32-bit operands *src0* and *src1* unsigned, keeping the low 32-bits, per component, of the result.</span></span> <span data-ttu-id="f86e3-118">Diese Anweisung führt dann ein [IAdd](iadd--sm4---asm-.md) -Element von *Quelle2* aus und erzeugt das korrekte niedrige 32-Bit-Ergebnis (pro Komponente).</span><span class="sxs-lookup"><span data-stu-id="f86e3-118">This instruction then performs an [iadd](iadd--sm4---asm-.md) of *src2*, producing the correct low 32-bit (per component) result.</span></span> <span data-ttu-id="f86e3-119">Die 32-Bit-Ergebnisse werden in *dest* platziert.</span><span class="sxs-lookup"><span data-stu-id="f86e3-119">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="f86e3-120">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="f86e3-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f86e3-121">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="f86e3-121">Vertex Shader</span></span> | <span data-ttu-id="f86e3-122">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="f86e3-122">Geometry Shader</span></span> | <span data-ttu-id="f86e3-123">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="f86e3-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f86e3-124">x</span><span class="sxs-lookup"><span data-stu-id="f86e3-124">x</span></span>             | <span data-ttu-id="f86e3-125">x</span><span class="sxs-lookup"><span data-stu-id="f86e3-125">x</span></span>               | <span data-ttu-id="f86e3-126">x</span><span class="sxs-lookup"><span data-stu-id="f86e3-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f86e3-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="f86e3-127">Minimum Shader Model</span></span>

<span data-ttu-id="f86e3-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f86e3-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f86e3-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="f86e3-129">Shader Model</span></span>                                              | <span data-ttu-id="f86e3-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="f86e3-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f86e3-131">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="f86e3-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f86e3-132">ja</span><span class="sxs-lookup"><span data-stu-id="f86e3-132">yes</span></span>       |
| [<span data-ttu-id="f86e3-133">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="f86e3-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f86e3-134">ja</span><span class="sxs-lookup"><span data-stu-id="f86e3-134">yes</span></span>       |
| [<span data-ttu-id="f86e3-135">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="f86e3-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f86e3-136">ja</span><span class="sxs-lookup"><span data-stu-id="f86e3-136">yes</span></span>       |
| [<span data-ttu-id="f86e3-137">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f86e3-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f86e3-138">nein</span><span class="sxs-lookup"><span data-stu-id="f86e3-138">no</span></span>        |
| [<span data-ttu-id="f86e3-139">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f86e3-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f86e3-140">nein</span><span class="sxs-lookup"><span data-stu-id="f86e3-140">no</span></span>        |
| [<span data-ttu-id="f86e3-141">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f86e3-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f86e3-142">nein</span><span class="sxs-lookup"><span data-stu-id="f86e3-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f86e3-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f86e3-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f86e3-144">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f86e3-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





