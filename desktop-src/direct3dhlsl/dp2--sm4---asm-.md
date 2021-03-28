---
title: DP2 (SM4-ASM)
description: 2-dimensionaler Vektor Punkt-Produkt der Komponenten RG, POS-Swizzle.
ms.assetid: E35F6A8B-6D8E-4660-B0F3-95B76BC19229
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4073def6cb315dc0268d1ce8e3f28039b9b2a69
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389511"
---
# <a name="dp2-sm4---asm"></a><span data-ttu-id="327a4-103">DP2 (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="327a4-103">dp2 (sm4 - asm)</span></span>

<span data-ttu-id="327a4-104">2-dimensionaler Vektor Punkt-Produkt der Komponenten RG, POS-Swizzle.</span><span class="sxs-lookup"><span data-stu-id="327a4-104">2-dimensional vector dot-product of components rg, POS-swizzle.</span></span>



| <span data-ttu-id="327a4-105">DP2 \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="327a4-105">dp2\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="327a4-106">Element</span><span class="sxs-lookup"><span data-stu-id="327a4-106">Item</span></span>                                                            | <span data-ttu-id="327a4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="327a4-107">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="327a4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="327a4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="327a4-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="327a4-109">\[in\] The address of the result of the operation.</span></span> <br/> <span data-ttu-id="327a4-110">*dest*  =  *src0. r* \* *Quelle1. r*  +  *src0. g* \* *Quelle1. g*</span><span class="sxs-lookup"><span data-stu-id="327a4-110">*dest* = *src0.r* \* *src1.r* + *src0.g* \* *src1.g*</span></span><br/> |
| <span data-ttu-id="327a4-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="327a4-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="327a4-112">\[in \] den Komponenten des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="327a4-112">\[in\] The components in the operation.</span></span><br/>                                                                             |
| <span data-ttu-id="327a4-113"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="327a4-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="327a4-114">\[in \] den Komponenten des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="327a4-114">\[in\] The components in the operation.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="327a4-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="327a4-115">Remarks</span></span>

<span data-ttu-id="327a4-116">Das skalare Ergebnis wurde in den Komponenten in der Schreib Maske repliziert.</span><span class="sxs-lookup"><span data-stu-id="327a4-116">Scalar result replicated to components in write mask.</span></span>

<span data-ttu-id="327a4-117">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="327a4-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="327a4-118">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="327a4-118">Vertex Shader</span></span> | <span data-ttu-id="327a4-119">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="327a4-119">Geometry Shader</span></span> | <span data-ttu-id="327a4-120">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="327a4-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="327a4-121">x</span><span class="sxs-lookup"><span data-stu-id="327a4-121">x</span></span>             | <span data-ttu-id="327a4-122">x</span><span class="sxs-lookup"><span data-stu-id="327a4-122">x</span></span>               | <span data-ttu-id="327a4-123">x</span><span class="sxs-lookup"><span data-stu-id="327a4-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="327a4-124">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="327a4-124">Minimum Shader Model</span></span>

<span data-ttu-id="327a4-125">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="327a4-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="327a4-126">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="327a4-126">Shader Model</span></span>                                              | <span data-ttu-id="327a4-127">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="327a4-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="327a4-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="327a4-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="327a4-129">ja</span><span class="sxs-lookup"><span data-stu-id="327a4-129">yes</span></span>       |
| [<span data-ttu-id="327a4-130">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="327a4-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="327a4-131">ja</span><span class="sxs-lookup"><span data-stu-id="327a4-131">yes</span></span>       |
| [<span data-ttu-id="327a4-132">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="327a4-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="327a4-133">ja</span><span class="sxs-lookup"><span data-stu-id="327a4-133">yes</span></span>       |
| [<span data-ttu-id="327a4-134">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="327a4-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="327a4-135">nein</span><span class="sxs-lookup"><span data-stu-id="327a4-135">no</span></span>        |
| [<span data-ttu-id="327a4-136">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="327a4-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="327a4-137">nein</span><span class="sxs-lookup"><span data-stu-id="327a4-137">no</span></span>        |
| [<span data-ttu-id="327a4-138">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="327a4-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="327a4-139">nein</span><span class="sxs-lookup"><span data-stu-id="327a4-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="327a4-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="327a4-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="327a4-141">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="327a4-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





