---
title: f32tof16 (SM5-ASM)
description: Konvertierung von Komponenten weiser float16 zu float32. | f32tof16 (SM5-ASM)
ms.assetid: 36BCCFC5-722A-45EB-8A66-7544833BBBA5
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54a101f370f9c53d1d3f43f9e1cf6c4da82933d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982030"
---
# <a name="f32tof16-sm5---asm"></a><span data-ttu-id="7cfd3-104">f32tof16 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="7cfd3-104">f32tof16 (sm5 - asm)</span></span>

<span data-ttu-id="7cfd3-105">Konvertierung von Komponenten weiser float16 zu float32.</span><span class="sxs-lookup"><span data-stu-id="7cfd3-105">Component-wise float16 to float32 conversion.</span></span>



| <span data-ttu-id="7cfd3-106">f32tof16 dest \[ . mask \] , \[ - \] src \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="7cfd3-106">f32tof16 dest\[.mask\], \[-\]src\[.swizzle\]</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="7cfd3-107">Element</span><span class="sxs-lookup"><span data-stu-id="7cfd3-107">Item</span></span>                                                            | <span data-ttu-id="7cfd3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7cfd3-108">Description</span></span>                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="7cfd3-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="7cfd3-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="7cfd3-110">\[in \] der Adresse des float16-Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="7cfd3-110">\[in\] The address of float16 result.</span></span><br/> |
| <span data-ttu-id="7cfd3-111"><span id="src"></span><span id="SRC"></span>*src*</span><span class="sxs-lookup"><span data-stu-id="7cfd3-111"><span id="src"></span><span id="SRC"></span>*src*</span></span><br/>    | <span data-ttu-id="7cfd3-112">\[im \] float32-Wert, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7cfd3-112">\[in\] The float32 value to convert.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="7cfd3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7cfd3-113">Remarks</span></span>

<span data-ttu-id="7cfd3-114">Diese Anweisung führt eine Komponenten Weise Konvertierung eines float32-Werts in ein float16-Wert Ergebnis in den lsb-16-Bit-Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7cfd3-114">This instruction performs a component-wise conversion of a float32 value to a float16 value result placed in LSB 16 bits.</span></span>

<span data-ttu-id="7cfd3-115">Diese Anweisung folgt den D3D-Regeln für die Gleit Komma Konvertierung.</span><span class="sxs-lookup"><span data-stu-id="7cfd3-115">This instruction follows D3D rules for floating point conversion.</span></span>

<span data-ttu-id="7cfd3-116">Verwenden Sie diese Anweisung für die Shader-gesteuerte Datenkomprimierung.</span><span class="sxs-lookup"><span data-stu-id="7cfd3-116">Use this instruction for shader-driven data compression.</span></span>

<span data-ttu-id="7cfd3-117">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="7cfd3-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7cfd3-118">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="7cfd3-118">Vertex</span></span> | <span data-ttu-id="7cfd3-119">Hülle</span><span class="sxs-lookup"><span data-stu-id="7cfd3-119">Hull</span></span> | <span data-ttu-id="7cfd3-120">Domain</span><span class="sxs-lookup"><span data-stu-id="7cfd3-120">Domain</span></span> | <span data-ttu-id="7cfd3-121">Geometrie</span><span class="sxs-lookup"><span data-stu-id="7cfd3-121">Geometry</span></span> | <span data-ttu-id="7cfd3-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="7cfd3-122">Pixel</span></span> | <span data-ttu-id="7cfd3-123">Compute</span><span class="sxs-lookup"><span data-stu-id="7cfd3-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7cfd3-124">X</span><span class="sxs-lookup"><span data-stu-id="7cfd3-124">X</span></span>      | <span data-ttu-id="7cfd3-125">X</span><span class="sxs-lookup"><span data-stu-id="7cfd3-125">X</span></span>    | <span data-ttu-id="7cfd3-126">X</span><span class="sxs-lookup"><span data-stu-id="7cfd3-126">X</span></span>      | <span data-ttu-id="7cfd3-127">X</span><span class="sxs-lookup"><span data-stu-id="7cfd3-127">X</span></span>        | <span data-ttu-id="7cfd3-128">X</span><span class="sxs-lookup"><span data-stu-id="7cfd3-128">X</span></span>     | <span data-ttu-id="7cfd3-129">X</span><span class="sxs-lookup"><span data-stu-id="7cfd3-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7cfd3-130">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="7cfd3-130">Minimum Shader Model</span></span>

<span data-ttu-id="7cfd3-131">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="7cfd3-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="7cfd3-132">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="7cfd3-132">Shader Model</span></span>                                              | <span data-ttu-id="7cfd3-133">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="7cfd3-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7cfd3-134">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="7cfd3-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7cfd3-135">ja</span><span class="sxs-lookup"><span data-stu-id="7cfd3-135">yes</span></span>       |
| [<span data-ttu-id="7cfd3-136">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="7cfd3-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7cfd3-137">nein</span><span class="sxs-lookup"><span data-stu-id="7cfd3-137">no</span></span>        |
| [<span data-ttu-id="7cfd3-138">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="7cfd3-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7cfd3-139">nein</span><span class="sxs-lookup"><span data-stu-id="7cfd3-139">no</span></span>        |
| [<span data-ttu-id="7cfd3-140">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7cfd3-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7cfd3-141">nein</span><span class="sxs-lookup"><span data-stu-id="7cfd3-141">no</span></span>        |
| [<span data-ttu-id="7cfd3-142">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7cfd3-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7cfd3-143">nein</span><span class="sxs-lookup"><span data-stu-id="7cfd3-143">no</span></span>        |
| [<span data-ttu-id="7cfd3-144">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7cfd3-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7cfd3-145">nein</span><span class="sxs-lookup"><span data-stu-id="7cfd3-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7cfd3-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7cfd3-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cfd3-147">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7cfd3-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





