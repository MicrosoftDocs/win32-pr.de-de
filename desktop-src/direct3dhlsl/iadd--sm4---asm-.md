---
title: IAdd (SM4-ASM)
description: Ganzzahlige Addition.
ms.assetid: EF78EA65-DC16-469A-9E45-52844FF4BD93
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b593484aa7c1ef376bb5febf141b144ddef338e0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389574"
---
# <a name="iadd-sm4---asm"></a><span data-ttu-id="58f2d-103">IAdd (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="58f2d-103">iadd (sm4 - asm)</span></span>

<span data-ttu-id="58f2d-104">Ganzzahlige Addition.</span><span class="sxs-lookup"><span data-stu-id="58f2d-104">Integer addition.</span></span>



| <span data-ttu-id="58f2d-105">IAdd dest \[ . mask \] , \[ - \] src0 \[ . Swizzle \] , \[ - \] Quelle1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="58f2d-105">iadd dest\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="58f2d-106">Element</span><span class="sxs-lookup"><span data-stu-id="58f2d-106">Item</span></span>                                                            | <span data-ttu-id="58f2d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58f2d-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="58f2d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="58f2d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="58f2d-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="58f2d-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="58f2d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="58f2d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="58f2d-111">\[in \] der Zahl, die zu *Quelle1* hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="58f2d-111">\[in\] The number to be added to *src1*.</span></span><br/>           |
| <span data-ttu-id="58f2d-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="58f2d-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="58f2d-113">\[in \] der Zahl, die zu *src0* hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="58f2d-113">\[in\] The number to be added to *src0*.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="58f2d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58f2d-114">Remarks</span></span>

<span data-ttu-id="58f2d-115">Komponenten weises Hinzufügen von 32-Bit-Operanden *src0* und *Quelle1*, wobei das korrekte 32-Bit-Ergebnis in *dest* platziert wird.</span><span class="sxs-lookup"><span data-stu-id="58f2d-115">Component-wise add of 32-bit operands *src0* and *src1*, placing the correct 32-bit result in *dest*.</span></span> <span data-ttu-id="58f2d-116">Über die 32-Bit-Werte der einzelnen Komponenten hinaus werden keine übertragen oder Ausleihe durchgeführt, sodass diese Anweisung nicht für die Signierung ihrer Operanden sensibel ist.</span><span class="sxs-lookup"><span data-stu-id="58f2d-116">No carry or borrow beyond the 32-bit values of each component is performed, so this instruction is not sensitive to the signed-ness of its operands.</span></span>

<span data-ttu-id="58f2d-117">Der optionale Negation-Modifizierer für Quell Operanden nimmt die Ergänzung von 2 vor dem Ausführen des Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="58f2d-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="58f2d-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="58f2d-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="58f2d-119">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="58f2d-119">Vertex Shader</span></span> | <span data-ttu-id="58f2d-120">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="58f2d-120">Geometry Shader</span></span> | <span data-ttu-id="58f2d-121">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="58f2d-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="58f2d-122">x</span><span class="sxs-lookup"><span data-stu-id="58f2d-122">x</span></span>             | <span data-ttu-id="58f2d-123">x</span><span class="sxs-lookup"><span data-stu-id="58f2d-123">x</span></span>               | <span data-ttu-id="58f2d-124">x</span><span class="sxs-lookup"><span data-stu-id="58f2d-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="58f2d-125">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="58f2d-125">Minimum Shader Model</span></span>

<span data-ttu-id="58f2d-126">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="58f2d-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="58f2d-127">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="58f2d-127">Shader Model</span></span>                                              | <span data-ttu-id="58f2d-128">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="58f2d-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="58f2d-129">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="58f2d-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="58f2d-130">ja</span><span class="sxs-lookup"><span data-stu-id="58f2d-130">yes</span></span>       |
| [<span data-ttu-id="58f2d-131">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="58f2d-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="58f2d-132">ja</span><span class="sxs-lookup"><span data-stu-id="58f2d-132">yes</span></span>       |
| [<span data-ttu-id="58f2d-133">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="58f2d-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="58f2d-134">ja</span><span class="sxs-lookup"><span data-stu-id="58f2d-134">yes</span></span>       |
| [<span data-ttu-id="58f2d-135">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="58f2d-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="58f2d-136">nein</span><span class="sxs-lookup"><span data-stu-id="58f2d-136">no</span></span>        |
| [<span data-ttu-id="58f2d-137">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="58f2d-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="58f2d-138">nein</span><span class="sxs-lookup"><span data-stu-id="58f2d-138">no</span></span>        |
| [<span data-ttu-id="58f2d-139">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="58f2d-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="58f2d-140">nein</span><span class="sxs-lookup"><span data-stu-id="58f2d-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="58f2d-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="58f2d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58f2d-142">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="58f2d-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





