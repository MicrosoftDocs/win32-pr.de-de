---
title: Not (SM4-ASM)
description: Bitweiser Not-Operator.
ms.assetid: AC7EBBC2-4B52-4793-812C-B25897FB8D05
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0bf224e6e5af7f2db6bcbaf7ae287ba2d399727
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976449"
---
# <a name="not-sm4---asm"></a><span data-ttu-id="43199-103">Not (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="43199-103">not (sm4 - asm)</span></span>

<span data-ttu-id="43199-104">Bitweiser Not-Operator.</span><span class="sxs-lookup"><span data-stu-id="43199-104">Bitwise not.</span></span>



| <span data-ttu-id="43199-105">nicht dest \[ . mask \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="43199-105">not dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------|



 



| <span data-ttu-id="43199-106">Element</span><span class="sxs-lookup"><span data-stu-id="43199-106">Item</span></span>                                                            | <span data-ttu-id="43199-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43199-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="43199-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="43199-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="43199-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="43199-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="43199-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="43199-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="43199-111">\[in \] den ursprünglichen Komponenten.</span><span class="sxs-lookup"><span data-stu-id="43199-111">\[in\] The original components.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="43199-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43199-112">Remarks</span></span>

<span data-ttu-id="43199-113">Diese Anweisung führt ein Komponenten weises Komplement jedes 32-Bit-Werts in *src0* aus.</span><span class="sxs-lookup"><span data-stu-id="43199-113">This instruction performs a component-wise one's complement of each 32-bit value in *src0*.</span></span> <span data-ttu-id="43199-114">Die 32-Bit-Ergebnisse werden in *dest* gespeichert.</span><span class="sxs-lookup"><span data-stu-id="43199-114">The 32-bit results are stored in *dest*.</span></span>

<span data-ttu-id="43199-115">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="43199-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="43199-116">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="43199-116">Vertex Shader</span></span> | <span data-ttu-id="43199-117">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="43199-117">Geometry Shader</span></span> | <span data-ttu-id="43199-118">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="43199-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="43199-119">x</span><span class="sxs-lookup"><span data-stu-id="43199-119">x</span></span>             | <span data-ttu-id="43199-120">x</span><span class="sxs-lookup"><span data-stu-id="43199-120">x</span></span>               | <span data-ttu-id="43199-121">x</span><span class="sxs-lookup"><span data-stu-id="43199-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="43199-122">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="43199-122">Minimum Shader Model</span></span>

<span data-ttu-id="43199-123">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="43199-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="43199-124">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="43199-124">Shader Model</span></span>                                              | <span data-ttu-id="43199-125">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="43199-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="43199-126">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="43199-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="43199-127">ja</span><span class="sxs-lookup"><span data-stu-id="43199-127">yes</span></span>       |
| [<span data-ttu-id="43199-128">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="43199-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="43199-129">ja</span><span class="sxs-lookup"><span data-stu-id="43199-129">yes</span></span>       |
| [<span data-ttu-id="43199-130">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="43199-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="43199-131">ja</span><span class="sxs-lookup"><span data-stu-id="43199-131">yes</span></span>       |
| [<span data-ttu-id="43199-132">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="43199-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="43199-133">nein</span><span class="sxs-lookup"><span data-stu-id="43199-133">no</span></span>        |
| [<span data-ttu-id="43199-134">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="43199-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="43199-135">nein</span><span class="sxs-lookup"><span data-stu-id="43199-135">no</span></span>        |
| [<span data-ttu-id="43199-136">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="43199-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="43199-137">nein</span><span class="sxs-lookup"><span data-stu-id="43199-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="43199-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43199-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43199-139">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="43199-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





