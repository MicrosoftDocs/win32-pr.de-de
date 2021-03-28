---
title: XOR (SM4-ASM)
description: Bitweises XOR.
ms.assetid: 6B949653-6DDA-402B-8ABE-B93858B68470
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a998bd1e95793f463d7f234b464a542bed4fc0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389494"
---
# <a name="xor-sm4---asm"></a><span data-ttu-id="cd3c4-103">XOR (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="cd3c4-103">xor (sm4 - asm)</span></span>

<span data-ttu-id="cd3c4-104">Bitweises XOR.</span><span class="sxs-lookup"><span data-stu-id="cd3c4-104">Bitwise xor.</span></span>



| <span data-ttu-id="cd3c4-105">XOR dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="cd3c4-105">xor dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="cd3c4-106">Element</span><span class="sxs-lookup"><span data-stu-id="cd3c4-106">Item</span></span>                                                            | <span data-ttu-id="cd3c4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd3c4-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cd3c4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="cd3c4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="cd3c4-109">\[im \] Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="cd3c4-109">\[in\] The result of the operation.</span></span><br/>       |
| <span data-ttu-id="cd3c4-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="cd3c4-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="cd3c4-111">\[in \] den Komponenten zu XOR mit *Quelle1*.</span><span class="sxs-lookup"><span data-stu-id="cd3c4-111">\[in\] The components to XOR with *src1*.</span></span><br/> |
| <span data-ttu-id="cd3c4-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="cd3c4-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="cd3c4-113">\[in \] den Komponenten zu XOR mit *src0*.</span><span class="sxs-lookup"><span data-stu-id="cd3c4-113">\[in\] The components to XOR with *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cd3c4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd3c4-114">Remarks</span></span>

<span data-ttu-id="cd3c4-115">Diese Anweisung führt ein Komponenten weises logisches XOR für jedes Paar von 32-Bit-Werten aus *src0* und *Quelle1* aus.</span><span class="sxs-lookup"><span data-stu-id="cd3c4-115">This instruction performs a component-wise logical XOR of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="cd3c4-116">32-Bit-Ergebnisse werden in *dest* platziert.</span><span class="sxs-lookup"><span data-stu-id="cd3c4-116">32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="cd3c4-117">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="cd3c4-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cd3c4-118">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="cd3c4-118">Vertex Shader</span></span> | <span data-ttu-id="cd3c4-119">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="cd3c4-119">Geometry Shader</span></span> | <span data-ttu-id="cd3c4-120">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="cd3c4-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="cd3c4-121">x</span><span class="sxs-lookup"><span data-stu-id="cd3c4-121">x</span></span>             | <span data-ttu-id="cd3c4-122">x</span><span class="sxs-lookup"><span data-stu-id="cd3c4-122">x</span></span>               | <span data-ttu-id="cd3c4-123">x</span><span class="sxs-lookup"><span data-stu-id="cd3c4-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cd3c4-124">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="cd3c4-124">Minimum Shader Model</span></span>

<span data-ttu-id="cd3c4-125">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd3c4-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cd3c4-126">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="cd3c4-126">Shader Model</span></span>                                              | <span data-ttu-id="cd3c4-127">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="cd3c4-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cd3c4-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="cd3c4-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cd3c4-129">ja</span><span class="sxs-lookup"><span data-stu-id="cd3c4-129">yes</span></span>       |
| [<span data-ttu-id="cd3c4-130">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="cd3c4-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cd3c4-131">ja</span><span class="sxs-lookup"><span data-stu-id="cd3c4-131">yes</span></span>       |
| [<span data-ttu-id="cd3c4-132">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="cd3c4-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cd3c4-133">ja</span><span class="sxs-lookup"><span data-stu-id="cd3c4-133">yes</span></span>       |
| [<span data-ttu-id="cd3c4-134">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cd3c4-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cd3c4-135">nein</span><span class="sxs-lookup"><span data-stu-id="cd3c4-135">no</span></span>        |
| [<span data-ttu-id="cd3c4-136">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cd3c4-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cd3c4-137">nein</span><span class="sxs-lookup"><span data-stu-id="cd3c4-137">no</span></span>        |
| [<span data-ttu-id="cd3c4-138">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cd3c4-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cd3c4-139">nein</span><span class="sxs-lookup"><span data-stu-id="cd3c4-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cd3c4-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cd3c4-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd3c4-141">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cd3c4-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





