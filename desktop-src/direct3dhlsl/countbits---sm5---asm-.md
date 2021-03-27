---
title: count Bits (SM5-ASM)
description: Zählt die Anzahl der Bits, die in einer Zahl festgelegt sind.
ms.assetid: ED75487F-46FF-45F5-BEAA-7A32BEFB0571
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d46fe9c750790d65630a743dd9ddc347fea50e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857775"
---
# <a name="countbits-sm5---asm"></a><span data-ttu-id="18ebd-103">count Bits (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="18ebd-103">countbits (sm5 - asm)</span></span>

<span data-ttu-id="18ebd-104">Zählt die Anzahl der Bits, die in einer Zahl festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="18ebd-104">Counts the number of bits set in a number.</span></span>



| <span data-ttu-id="18ebd-105">count-Bits dest \[ . mask \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="18ebd-105">countbits dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="18ebd-106">Element</span><span class="sxs-lookup"><span data-stu-id="18ebd-106">Item</span></span>                                                            | <span data-ttu-id="18ebd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18ebd-107">Description</span></span>                                   |
|-----------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="18ebd-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="18ebd-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="18ebd-109">\[in \] der Adresse der Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="18ebd-109">\[in\] The address of the results.</span></span><br/> |
| <span data-ttu-id="18ebd-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="18ebd-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="18ebd-111">\[in \] der Eingabe-32-Bit-Nummer.</span><span class="sxs-lookup"><span data-stu-id="18ebd-111">\[in\] The input 32-bit number.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="18ebd-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18ebd-112">Remarks</span></span>

<span data-ttu-id="18ebd-113">Diese Anweisung kann verwendet werden, um den Prozentsatz der Shader-Eingabe Abdeckung zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="18ebd-113">This instruction can be used to compute shader input coverage percentage.</span></span>

<span data-ttu-id="18ebd-114">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="18ebd-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="18ebd-115">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="18ebd-115">Vertex</span></span> | <span data-ttu-id="18ebd-116">Hülle</span><span class="sxs-lookup"><span data-stu-id="18ebd-116">Hull</span></span> | <span data-ttu-id="18ebd-117">Domain</span><span class="sxs-lookup"><span data-stu-id="18ebd-117">Domain</span></span> | <span data-ttu-id="18ebd-118">Geometrie</span><span class="sxs-lookup"><span data-stu-id="18ebd-118">Geometry</span></span> | <span data-ttu-id="18ebd-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="18ebd-119">Pixel</span></span> | <span data-ttu-id="18ebd-120">Compute</span><span class="sxs-lookup"><span data-stu-id="18ebd-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="18ebd-121">X</span><span class="sxs-lookup"><span data-stu-id="18ebd-121">X</span></span>      | <span data-ttu-id="18ebd-122">X</span><span class="sxs-lookup"><span data-stu-id="18ebd-122">X</span></span>    | <span data-ttu-id="18ebd-123">X</span><span class="sxs-lookup"><span data-stu-id="18ebd-123">X</span></span>      | <span data-ttu-id="18ebd-124">X</span><span class="sxs-lookup"><span data-stu-id="18ebd-124">X</span></span>        | <span data-ttu-id="18ebd-125">X</span><span class="sxs-lookup"><span data-stu-id="18ebd-125">X</span></span>     | <span data-ttu-id="18ebd-126">X</span><span class="sxs-lookup"><span data-stu-id="18ebd-126">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="18ebd-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="18ebd-127">Minimum Shader Model</span></span>

<span data-ttu-id="18ebd-128">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="18ebd-128">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="18ebd-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="18ebd-129">Shader Model</span></span>                                              | <span data-ttu-id="18ebd-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="18ebd-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="18ebd-131">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="18ebd-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="18ebd-132">ja</span><span class="sxs-lookup"><span data-stu-id="18ebd-132">yes</span></span>       |
| [<span data-ttu-id="18ebd-133">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="18ebd-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="18ebd-134">nein</span><span class="sxs-lookup"><span data-stu-id="18ebd-134">no</span></span>        |
| [<span data-ttu-id="18ebd-135">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="18ebd-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="18ebd-136">nein</span><span class="sxs-lookup"><span data-stu-id="18ebd-136">no</span></span>        |
| [<span data-ttu-id="18ebd-137">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="18ebd-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="18ebd-138">nein</span><span class="sxs-lookup"><span data-stu-id="18ebd-138">no</span></span>        |
| [<span data-ttu-id="18ebd-139">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="18ebd-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="18ebd-140">nein</span><span class="sxs-lookup"><span data-stu-id="18ebd-140">no</span></span>        |
| [<span data-ttu-id="18ebd-141">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="18ebd-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="18ebd-142">nein</span><span class="sxs-lookup"><span data-stu-id="18ebd-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="18ebd-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="18ebd-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18ebd-144">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="18ebd-144">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





