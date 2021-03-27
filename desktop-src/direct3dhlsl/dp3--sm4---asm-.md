---
title: DP3 (SM4-ASM)
description: 3-dimensionaler Vektor Punkt-Produkt von Komponenten RGB, POS-Swizzle.
ms.assetid: 8E6EA6CD-B5BB-4D64-8846-F7B9F7135582
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2598053abed93675107f15af762e0844d4938fbf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857759"
---
# <a name="dp3-sm4---asm"></a><span data-ttu-id="1f9e0-103">DP3 (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1f9e0-103">dp3 (sm4 - asm)</span></span>

<span data-ttu-id="1f9e0-104">3-dimensionaler Vektor Punkt-Produkt von Komponenten RGB, POS-Swizzle.</span><span class="sxs-lookup"><span data-stu-id="1f9e0-104">3-dimensional vector dot-product of components rgb, POS-swizzle.</span></span>



| <span data-ttu-id="1f9e0-105">DP3 \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="1f9e0-105">dp3\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="1f9e0-106">Element</span><span class="sxs-lookup"><span data-stu-id="1f9e0-106">Item</span></span>                                                            | <span data-ttu-id="1f9e0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1f9e0-107">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f9e0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1f9e0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1f9e0-109">\[im \] Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="1f9e0-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="1f9e0-110">*dest*  =  *src0. r* \* *Quelle1. r*  +  *src0. g* \* *Quelle1. g*  +  *src0. b* \* *Quelle1. b*</span><span class="sxs-lookup"><span data-stu-id="1f9e0-110">*dest* = *src0.r* \* *src1.r* + *src0.g* \* *src1.g* + *src0.b* \* *src1.b*</span></span><br/> |
| <span data-ttu-id="1f9e0-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1f9e0-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1f9e0-112">\[in \] den Komponenten im-Operator.</span><span class="sxs-lookup"><span data-stu-id="1f9e0-112">\[in\] The components in the opertation.</span></span><br/>                                                                                   |
| <span data-ttu-id="1f9e0-113"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="1f9e0-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="1f9e0-114">\[in \] den Komponenten im-Operator.</span><span class="sxs-lookup"><span data-stu-id="1f9e0-114">\[in\] The components in the opertation.</span></span><br/>                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="1f9e0-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f9e0-115">Remarks</span></span>

<span data-ttu-id="1f9e0-116">Das skalare Ergebnis wurde in den Komponenten in der Schreib Maske repliziert.</span><span class="sxs-lookup"><span data-stu-id="1f9e0-116">Scalar result replicated to components in write mask.</span></span>

<span data-ttu-id="1f9e0-117">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="1f9e0-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1f9e0-118">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="1f9e0-118">Vertex Shader</span></span> | <span data-ttu-id="1f9e0-119">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="1f9e0-119">Geometry Shader</span></span> | <span data-ttu-id="1f9e0-120">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="1f9e0-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1f9e0-121">x</span><span class="sxs-lookup"><span data-stu-id="1f9e0-121">x</span></span>             | <span data-ttu-id="1f9e0-122">x</span><span class="sxs-lookup"><span data-stu-id="1f9e0-122">x</span></span>               | <span data-ttu-id="1f9e0-123">x</span><span class="sxs-lookup"><span data-stu-id="1f9e0-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1f9e0-124">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="1f9e0-124">Minimum Shader Model</span></span>

<span data-ttu-id="1f9e0-125">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1f9e0-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1f9e0-126">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="1f9e0-126">Shader Model</span></span>                                              | <span data-ttu-id="1f9e0-127">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="1f9e0-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1f9e0-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="1f9e0-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1f9e0-129">ja</span><span class="sxs-lookup"><span data-stu-id="1f9e0-129">yes</span></span>       |
| [<span data-ttu-id="1f9e0-130">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="1f9e0-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1f9e0-131">ja</span><span class="sxs-lookup"><span data-stu-id="1f9e0-131">yes</span></span>       |
| [<span data-ttu-id="1f9e0-132">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="1f9e0-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1f9e0-133">ja</span><span class="sxs-lookup"><span data-stu-id="1f9e0-133">yes</span></span>       |
| [<span data-ttu-id="1f9e0-134">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f9e0-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1f9e0-135">nein</span><span class="sxs-lookup"><span data-stu-id="1f9e0-135">no</span></span>        |
| [<span data-ttu-id="1f9e0-136">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f9e0-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1f9e0-137">nein</span><span class="sxs-lookup"><span data-stu-id="1f9e0-137">no</span></span>        |
| [<span data-ttu-id="1f9e0-138">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f9e0-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1f9e0-139">nein</span><span class="sxs-lookup"><span data-stu-id="1f9e0-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1f9e0-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1f9e0-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f9e0-141">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f9e0-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





