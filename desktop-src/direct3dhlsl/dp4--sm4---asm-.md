---
title: DP4 (SM4-ASM)
description: 4-dimensionaler Vektor Punkt-Produkt von Komponenten RGBA, POS-Swizzle.
ms.assetid: A41EC054-0060-49CA-90FB-A096E63DD27D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a91a253d4e8b53bc044e658c3fe75d8f7547da
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103948319"
---
# <a name="dp4-sm4---asm"></a><span data-ttu-id="43bff-103">DP4 (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="43bff-103">dp4 (sm4 - asm)</span></span>

<span data-ttu-id="43bff-104">4-dimensionaler Vektor Punkt-Produkt von Komponenten RGBA, POS-Swizzle.</span><span class="sxs-lookup"><span data-stu-id="43bff-104">4-dimensional vector dot-product of components rgba, POS-swizzle.</span></span>



| <span data-ttu-id="43bff-105">DP4 \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="43bff-105">dp4\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="43bff-106">Element</span><span class="sxs-lookup"><span data-stu-id="43bff-106">Item</span></span>                                                            | <span data-ttu-id="43bff-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43bff-107">Description</span></span>                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43bff-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="43bff-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="43bff-109">\[im \] Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="43bff-109">\[in\] The result of the operation.</span></span> <br/> <span data-ttu-id="43bff-110">*dest*  =  *src0. r* \* *Quelle1. r*  +  *src0. g* \* *Quelle1. g*  +  *src0. b* \* *Quelle1. b* +  *src0. a* \* *Quelle1. a*</span><span class="sxs-lookup"><span data-stu-id="43bff-110">*dest* = *src0.r* \* *src1.r* + *src0.g* \* *src1.g* + *src0.b* \* *src1.b*+ *src0.a* \* *src1.a*</span></span><br/> |
| <span data-ttu-id="43bff-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="43bff-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="43bff-112">\[in \] den Komponenten im-Operator.</span><span class="sxs-lookup"><span data-stu-id="43bff-112">\[in\] The components in the opertation.</span></span><br/>                                                                                                          |
| <span data-ttu-id="43bff-113"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="43bff-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="43bff-114">\[in \] den Komponenten im-Operator.</span><span class="sxs-lookup"><span data-stu-id="43bff-114">\[in\] The components in the opertation.</span></span><br/>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="43bff-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43bff-115">Remarks</span></span>

<span data-ttu-id="43bff-116">Das skalare Ergebnis wurde in den Komponenten in der Schreib Maske repliziert.</span><span class="sxs-lookup"><span data-stu-id="43bff-116">Scalar result replicated to components in write mask.</span></span>

<span data-ttu-id="43bff-117">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="43bff-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="43bff-118">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="43bff-118">Vertex Shader</span></span> | <span data-ttu-id="43bff-119">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="43bff-119">Geometry Shader</span></span> | <span data-ttu-id="43bff-120">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="43bff-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="43bff-121">x</span><span class="sxs-lookup"><span data-stu-id="43bff-121">x</span></span>             | <span data-ttu-id="43bff-122">x</span><span class="sxs-lookup"><span data-stu-id="43bff-122">x</span></span>               | <span data-ttu-id="43bff-123">x</span><span class="sxs-lookup"><span data-stu-id="43bff-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="43bff-124">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="43bff-124">Minimum Shader Model</span></span>

<span data-ttu-id="43bff-125">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="43bff-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="43bff-126">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="43bff-126">Shader Model</span></span>                                              | <span data-ttu-id="43bff-127">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="43bff-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="43bff-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="43bff-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="43bff-129">ja</span><span class="sxs-lookup"><span data-stu-id="43bff-129">yes</span></span>       |
| [<span data-ttu-id="43bff-130">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="43bff-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="43bff-131">ja</span><span class="sxs-lookup"><span data-stu-id="43bff-131">yes</span></span>       |
| [<span data-ttu-id="43bff-132">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="43bff-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="43bff-133">ja</span><span class="sxs-lookup"><span data-stu-id="43bff-133">yes</span></span>       |
| [<span data-ttu-id="43bff-134">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="43bff-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="43bff-135">nein</span><span class="sxs-lookup"><span data-stu-id="43bff-135">no</span></span>        |
| [<span data-ttu-id="43bff-136">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="43bff-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="43bff-137">nein</span><span class="sxs-lookup"><span data-stu-id="43bff-137">no</span></span>        |
| [<span data-ttu-id="43bff-138">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="43bff-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="43bff-139">nein</span><span class="sxs-lookup"><span data-stu-id="43bff-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="43bff-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43bff-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43bff-141">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="43bff-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





