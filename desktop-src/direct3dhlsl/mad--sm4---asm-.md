---
title: Mad (SM4-ASM)
description: Fügen Sie die Komponenten Weise Multiplikation hinzu.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d34823cdb3545f29426117b35903c97c08c5807
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038321"
---
# <a name="mad-sm4---asm"></a><span data-ttu-id="4df3d-103">Mad (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4df3d-103">mad (sm4 - asm)</span></span>

<span data-ttu-id="4df3d-104">Die Komponenten Weise Multiplikation & hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4df3d-104">Component-wise multiply & add.</span></span>



| <span data-ttu-id="4df3d-105">: Mad \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle2 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="4df3d-105">:mad\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="4df3d-106">Element</span><span class="sxs-lookup"><span data-stu-id="4df3d-106">Item</span></span>                                                            | <span data-ttu-id="4df3d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4df3d-107">Description</span></span>                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4df3d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="4df3d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="4df3d-109">\[im \] Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="4df3d-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="4df3d-110">*dest*  =  *src0* \* *Quelle1*  +  *Quelle2*</span><span class="sxs-lookup"><span data-stu-id="4df3d-110">*dest* = *src0* \* *src1* + *src2*</span></span><br/> |
| <span data-ttu-id="4df3d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4df3d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="4df3d-112">\[in \] multiplicand.</span><span class="sxs-lookup"><span data-stu-id="4df3d-112">\[in\] The multiplicand.</span></span><br/>                                                          |
| <span data-ttu-id="4df3d-113"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="4df3d-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="4df3d-114">\[im \] Multiplikator.</span><span class="sxs-lookup"><span data-stu-id="4df3d-114">\[in\] The multiplier.</span></span><br/>                                                            |
| <span data-ttu-id="4df3d-115"><span id="src2"></span><span id="SRC2"></span>*Quelle2*</span><span class="sxs-lookup"><span data-stu-id="4df3d-115"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="4df3d-116">\[im \] Addend.</span><span class="sxs-lookup"><span data-stu-id="4df3d-116">\[in\] The addend.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="4df3d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4df3d-117">Remarks</span></span>

<span data-ttu-id="4df3d-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="4df3d-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4df3d-119">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="4df3d-119">Vertex Shader</span></span> | <span data-ttu-id="4df3d-120">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="4df3d-120">Geometry Shader</span></span> | <span data-ttu-id="4df3d-121">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="4df3d-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4df3d-122">x</span><span class="sxs-lookup"><span data-stu-id="4df3d-122">x</span></span>             | <span data-ttu-id="4df3d-123">x</span><span class="sxs-lookup"><span data-stu-id="4df3d-123">x</span></span>               | <span data-ttu-id="4df3d-124">x</span><span class="sxs-lookup"><span data-stu-id="4df3d-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4df3d-125">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="4df3d-125">Minimum Shader Model</span></span>

<span data-ttu-id="4df3d-126">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4df3d-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4df3d-127">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="4df3d-127">Shader Model</span></span>                                              | <span data-ttu-id="4df3d-128">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="4df3d-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4df3d-129">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="4df3d-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4df3d-130">ja</span><span class="sxs-lookup"><span data-stu-id="4df3d-130">yes</span></span>       |
| [<span data-ttu-id="4df3d-131">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="4df3d-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4df3d-132">ja</span><span class="sxs-lookup"><span data-stu-id="4df3d-132">yes</span></span>       |
| [<span data-ttu-id="4df3d-133">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="4df3d-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4df3d-134">ja</span><span class="sxs-lookup"><span data-stu-id="4df3d-134">yes</span></span>       |
| [<span data-ttu-id="4df3d-135">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4df3d-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4df3d-136">nein</span><span class="sxs-lookup"><span data-stu-id="4df3d-136">no</span></span>        |
| [<span data-ttu-id="4df3d-137">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4df3d-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4df3d-138">nein</span><span class="sxs-lookup"><span data-stu-id="4df3d-138">no</span></span>        |
| [<span data-ttu-id="4df3d-139">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4df3d-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4df3d-140">nein</span><span class="sxs-lookup"><span data-stu-id="4df3d-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4df3d-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4df3d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4df3d-142">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4df3d-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





