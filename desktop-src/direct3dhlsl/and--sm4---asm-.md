---
title: und (SM4-ASM)
description: Bitweises AND.
ms.assetid: 403DA289-E2CF-4736-8882-4131F884F777
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ec9474322aafda2706502898902d01d0e13143
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719445"
---
# <a name="and-sm4---asm"></a><span data-ttu-id="82c9b-103">und (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="82c9b-103">and (sm4 - asm)</span></span>

<span data-ttu-id="82c9b-104">Bitweises **and**.</span><span class="sxs-lookup"><span data-stu-id="82c9b-104">Bitwise **AND**.</span></span>



| <span data-ttu-id="82c9b-105">und dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="82c9b-105">and dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="82c9b-106">Element</span><span class="sxs-lookup"><span data-stu-id="82c9b-106">Item</span></span>                                                            | <span data-ttu-id="82c9b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82c9b-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="82c9b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="82c9b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="82c9b-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="82c9b-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="82c9b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="82c9b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="82c9b-111">\[im \] 32-Bit-Wert zu **und** mit *Quelle1*.</span><span class="sxs-lookup"><span data-stu-id="82c9b-111">\[in\] The 32-bit value to **AND** with *src1*.</span></span><br/>    |
| <span data-ttu-id="82c9b-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="82c9b-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="82c9b-113">\[im \] 32-Bit-Wert zu **und** mit *src0*.</span><span class="sxs-lookup"><span data-stu-id="82c9b-113">\[in\] The 32-bit value to **AND** with *src0*.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="82c9b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82c9b-114">Remarks</span></span>

<span data-ttu-id="82c9b-115">Komponenten weises logisches **and** für jedes Paar von 32-Bit-Werten aus *src0* und *Quelle1*.</span><span class="sxs-lookup"><span data-stu-id="82c9b-115">Component-wise logical **AND** of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="82c9b-116">Die 32-Bit-Ergebnisse werden in *dest* platziert.</span><span class="sxs-lookup"><span data-stu-id="82c9b-116">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="82c9b-117">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="82c9b-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="82c9b-118">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="82c9b-118">Vertex Shader</span></span> | <span data-ttu-id="82c9b-119">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="82c9b-119">Geometry Shader</span></span> | <span data-ttu-id="82c9b-120">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="82c9b-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="82c9b-121">x</span><span class="sxs-lookup"><span data-stu-id="82c9b-121">x</span></span>             | <span data-ttu-id="82c9b-122">x</span><span class="sxs-lookup"><span data-stu-id="82c9b-122">x</span></span>               | <span data-ttu-id="82c9b-123">x</span><span class="sxs-lookup"><span data-stu-id="82c9b-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="82c9b-124">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="82c9b-124">Minimum Shader Model</span></span>

<span data-ttu-id="82c9b-125">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="82c9b-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="82c9b-126">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="82c9b-126">Shader Model</span></span>                                              | <span data-ttu-id="82c9b-127">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="82c9b-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="82c9b-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="82c9b-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="82c9b-129">ja</span><span class="sxs-lookup"><span data-stu-id="82c9b-129">yes</span></span>       |
| [<span data-ttu-id="82c9b-130">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="82c9b-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="82c9b-131">ja</span><span class="sxs-lookup"><span data-stu-id="82c9b-131">yes</span></span>       |
| [<span data-ttu-id="82c9b-132">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="82c9b-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="82c9b-133">ja</span><span class="sxs-lookup"><span data-stu-id="82c9b-133">yes</span></span>       |
| [<span data-ttu-id="82c9b-134">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82c9b-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="82c9b-135">nein</span><span class="sxs-lookup"><span data-stu-id="82c9b-135">no</span></span>        |
| [<span data-ttu-id="82c9b-136">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82c9b-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="82c9b-137">nein</span><span class="sxs-lookup"><span data-stu-id="82c9b-137">no</span></span>        |
| [<span data-ttu-id="82c9b-138">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82c9b-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="82c9b-139">nein</span><span class="sxs-lookup"><span data-stu-id="82c9b-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="82c9b-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="82c9b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82c9b-141">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82c9b-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





