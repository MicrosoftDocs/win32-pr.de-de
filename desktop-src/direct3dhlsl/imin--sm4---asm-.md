---
title: Imin (SM4-ASM)
description: Die minimale Komponenten Weise Ganzzahl.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942384e7a988e4919a483e09c75e476d5a6917ba
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389569"
---
# <a name="imin-sm4---asm"></a><span data-ttu-id="5b79d-103">Imin (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="5b79d-103">imin (sm4 - asm)</span></span>

<span data-ttu-id="5b79d-104">Die minimale Komponenten Weise Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="5b79d-104">Component-wise integer minimum.</span></span>



| <span data-ttu-id="5b79d-105">Imin dest \[ . mask \] , \[  - \] src0 \[ . Swizzle \] , \[ - \] Quelle1 \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="5b79d-105">imin dest\[.mask\], \[ -\]src0\[.swizzle\], \[-\]src1\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="5b79d-106">Element</span><span class="sxs-lookup"><span data-stu-id="5b79d-106">Item</span></span>                                                            | <span data-ttu-id="5b79d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b79d-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b79d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5b79d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5b79d-109">\[im \] Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="5b79d-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="5b79d-110">*dest*  =  *src0*  <  *Quelle1* ?</span><span class="sxs-lookup"><span data-stu-id="5b79d-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="5b79d-111">*src0* : *Quelle1*</span><span class="sxs-lookup"><span data-stu-id="5b79d-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="5b79d-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5b79d-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5b79d-113">\[im \] Wert, der mit *Quelle1* verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b79d-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                       |
| <span data-ttu-id="5b79d-114"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="5b79d-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="5b79d-115">\[im \] Wert, der mit *src0* verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b79d-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="5b79d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b79d-116">Remarks</span></span>

<span data-ttu-id="5b79d-117">Der optionale Negation-Modifizierer für Quell Operanden nimmt die Ergänzung von 2 vor dem Ausführen des Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="5b79d-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="5b79d-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="5b79d-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5b79d-119">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="5b79d-119">Vertex Shader</span></span> | <span data-ttu-id="5b79d-120">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="5b79d-120">Geometry Shader</span></span> | <span data-ttu-id="5b79d-121">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="5b79d-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="5b79d-122">x</span><span class="sxs-lookup"><span data-stu-id="5b79d-122">x</span></span>             | <span data-ttu-id="5b79d-123">x</span><span class="sxs-lookup"><span data-stu-id="5b79d-123">x</span></span>               | <span data-ttu-id="5b79d-124">x</span><span class="sxs-lookup"><span data-stu-id="5b79d-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5b79d-125">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="5b79d-125">Minimum Shader Model</span></span>

<span data-ttu-id="5b79d-126">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5b79d-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5b79d-127">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="5b79d-127">Shader Model</span></span>                                              | <span data-ttu-id="5b79d-128">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5b79d-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5b79d-129">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="5b79d-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5b79d-130">ja</span><span class="sxs-lookup"><span data-stu-id="5b79d-130">yes</span></span>       |
| [<span data-ttu-id="5b79d-131">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="5b79d-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5b79d-132">ja</span><span class="sxs-lookup"><span data-stu-id="5b79d-132">yes</span></span>       |
| [<span data-ttu-id="5b79d-133">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="5b79d-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5b79d-134">ja</span><span class="sxs-lookup"><span data-stu-id="5b79d-134">yes</span></span>       |
| [<span data-ttu-id="5b79d-135">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5b79d-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5b79d-136">nein</span><span class="sxs-lookup"><span data-stu-id="5b79d-136">no</span></span>        |
| [<span data-ttu-id="5b79d-137">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5b79d-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5b79d-138">nein</span><span class="sxs-lookup"><span data-stu-id="5b79d-138">no</span></span>        |
| [<span data-ttu-id="5b79d-139">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5b79d-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5b79d-140">nein</span><span class="sxs-lookup"><span data-stu-id="5b79d-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5b79d-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5b79d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b79d-142">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5b79d-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





