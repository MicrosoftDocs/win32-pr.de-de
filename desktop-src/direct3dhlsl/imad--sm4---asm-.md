---
title: Imad (SM4-ASM)
description: Ganze Zahl mit Vorzeichen multiplizieren und hinzufügen.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90db4cb0a36b0d3951e8b0490bb3ca08db8d5354
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992983"
---
# <a name="imad-sm4---asm"></a><span data-ttu-id="079fe-103">Imad (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="079fe-103">imad (sm4 - asm)</span></span>

<span data-ttu-id="079fe-104">Ganze Zahl mit Vorzeichen multiplizieren und hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="079fe-104">Signed integer multiply and add.</span></span>



| <span data-ttu-id="079fe-105">Imad dest \[ . mask \] , \[ - \] src0 \[ . Swizzle \] , \[ - \] Quelle1 \[ . Swizzle \] , \[ - \] Quelle2 \[ . Swizzle</span><span class="sxs-lookup"><span data-stu-id="079fe-105">imad dest\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\], \[-\]src2\[.swizzle</span></span> |
|---------------------------------------------------------------------------------------|



 



| <span data-ttu-id="079fe-106">Element</span><span class="sxs-lookup"><span data-stu-id="079fe-106">Item</span></span>                                                            | <span data-ttu-id="079fe-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="079fe-107">Description</span></span>                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="079fe-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="079fe-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="079fe-109">\[im \] Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="079fe-109">\[in\] The result of the operation.</span></span><br/>                      |
| <span data-ttu-id="079fe-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="079fe-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="079fe-111">\[unter \] Wert, der mit *Quelle1* multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="079fe-111">\[in\] Value to multiply with *src1*.</span></span><br/>                    |
| <span data-ttu-id="079fe-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="079fe-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="079fe-113">\[unter \] Wert, der mit *src0* multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="079fe-113">\[in\] Value to multiply with *src0*.</span></span><br/>                    |
| <span data-ttu-id="079fe-114"><span id="src2"></span><span id="SRC2"></span>*Quelle2*</span><span class="sxs-lookup"><span data-stu-id="079fe-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="079fe-115">\[unter \] Wert, der dem Produkt von *src0* und *Quelle1* hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="079fe-115">\[in\] Value to add to the product of *src0* and *src1*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="079fe-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="079fe-116">Remarks</span></span>

<span data-ttu-id="079fe-117">Komponenten Weise [imul](imul--sm4---asm-.md) der 32-Bit-Operanden *src0* und *Quelle1* (signiert), wobei die niedrigen 32 Bits (pro Komponente) des Ergebnisses, gefolgt von einem [IAdd](iadd--sm4---asm-.md) -Wert von *Quelle2*, generiert werden, wodurch das korrekte niedrige 32-Bit-Ergebnis (pro Komponente) erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="079fe-117">Component-wise [imul](imul--sm4---asm-.md) of 32-bit operands *src0* and *src1* (signed), keeping low 32-bits (per component) of the result, followed by an [iadd](iadd--sm4---asm-.md) of *src2*, producing the correct low 32-bit (per component) result.</span></span> <span data-ttu-id="079fe-118">Die 32-Bit-Ergebnisse werden in *dest* platziert.</span><span class="sxs-lookup"><span data-stu-id="079fe-118">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="079fe-119">Der optionale Negation-Modifizierer für Quell Operanden nimmt vor dem Ausführen arithmetischer Operationen eine Ergänzung von 2.</span><span class="sxs-lookup"><span data-stu-id="079fe-119">Optional negate modifier on source operands takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="079fe-120">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="079fe-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="079fe-121">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="079fe-121">Vertex Shader</span></span> | <span data-ttu-id="079fe-122">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="079fe-122">Geometry Shader</span></span> | <span data-ttu-id="079fe-123">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="079fe-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="079fe-124">x</span><span class="sxs-lookup"><span data-stu-id="079fe-124">x</span></span>             | <span data-ttu-id="079fe-125">x</span><span class="sxs-lookup"><span data-stu-id="079fe-125">x</span></span>               | <span data-ttu-id="079fe-126">x</span><span class="sxs-lookup"><span data-stu-id="079fe-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="079fe-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="079fe-127">Minimum Shader Model</span></span>

<span data-ttu-id="079fe-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="079fe-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="079fe-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="079fe-129">Shader Model</span></span>                                              | <span data-ttu-id="079fe-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="079fe-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="079fe-131">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="079fe-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="079fe-132">ja</span><span class="sxs-lookup"><span data-stu-id="079fe-132">yes</span></span>       |
| [<span data-ttu-id="079fe-133">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="079fe-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="079fe-134">ja</span><span class="sxs-lookup"><span data-stu-id="079fe-134">yes</span></span>       |
| [<span data-ttu-id="079fe-135">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="079fe-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="079fe-136">ja</span><span class="sxs-lookup"><span data-stu-id="079fe-136">yes</span></span>       |
| [<span data-ttu-id="079fe-137">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="079fe-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="079fe-138">nein</span><span class="sxs-lookup"><span data-stu-id="079fe-138">no</span></span>        |
| [<span data-ttu-id="079fe-139">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="079fe-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="079fe-140">nein</span><span class="sxs-lookup"><span data-stu-id="079fe-140">no</span></span>        |
| [<span data-ttu-id="079fe-141">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="079fe-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="079fe-142">nein</span><span class="sxs-lookup"><span data-stu-id="079fe-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="079fe-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="079fe-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="079fe-144">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="079fe-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





