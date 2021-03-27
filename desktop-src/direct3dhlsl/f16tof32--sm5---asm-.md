---
title: f16tof32 (SM5-ASM)
description: Konvertierung von Komponenten weiser float16 zu float32. | f16tof32 (SM5-ASM)
ms.assetid: CFAA1350-DA7F-4105-A90A-72052C5E2FB3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d53af1f2eab1f50dfded820bf27b2cda8f23e6b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981536"
---
# <a name="f16tof32-sm5---asm"></a><span data-ttu-id="e01e3-104">f16tof32 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e01e3-104">f16tof32 (sm5 - asm)</span></span>

<span data-ttu-id="e01e3-105">Konvertierung von Komponenten weiser float16 zu float32.</span><span class="sxs-lookup"><span data-stu-id="e01e3-105">Component-wise float16 to float32 conversion.</span></span>



| <span data-ttu-id="e01e3-106">f16tof32 dest \[ . mask \] , \[ - \] src \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="e01e3-106">f16tof32 dest\[.mask\], \[-\]src\[.swizzle\]</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="e01e3-107">Element</span><span class="sxs-lookup"><span data-stu-id="e01e3-107">Item</span></span>                                                            | <span data-ttu-id="e01e3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e01e3-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e01e3-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="e01e3-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="e01e3-110">\[in \] der Adresse des float32-Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="e01e3-110">\[in\] The address of the float32 result.</span></span><br/> |
| <span data-ttu-id="e01e3-111"><span id="src"></span><span id="SRC"></span>*src*</span><span class="sxs-lookup"><span data-stu-id="e01e3-111"><span id="src"></span><span id="SRC"></span>*src*</span></span><br/>    | <span data-ttu-id="e01e3-112">\[im \] float16-Wert, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e01e3-112">\[in\] The float16 value to convert.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="e01e3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e01e3-113">Remarks</span></span>

<span data-ttu-id="e01e3-114">Mit diesem Vorgang wird eine Komponenten Weise Konvertierung eines float16-Werts von lsb-Bits in ein float32-Ergebnis durchführt.</span><span class="sxs-lookup"><span data-stu-id="e01e3-114">This operation performs a component-wise conversion of a float16 value from LSB bits to a float32 result.</span></span>

<span data-ttu-id="e01e3-115">Dieser Vorgang folgt den D3D-Regeln für die Gleit Komma Konvertierung.</span><span class="sxs-lookup"><span data-stu-id="e01e3-115">This operation follows D3D rules for floating point conversion.</span></span>

<span data-ttu-id="e01e3-116">Verwenden Sie diese Anweisung für die Shader-gesteuerte datenentkomprimierung.</span><span class="sxs-lookup"><span data-stu-id="e01e3-116">Use this instruction for shader-driven data decompression.</span></span>

<span data-ttu-id="e01e3-117">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="e01e3-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e01e3-118">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="e01e3-118">Vertex</span></span> | <span data-ttu-id="e01e3-119">Hülle</span><span class="sxs-lookup"><span data-stu-id="e01e3-119">Hull</span></span> | <span data-ttu-id="e01e3-120">Domain</span><span class="sxs-lookup"><span data-stu-id="e01e3-120">Domain</span></span> | <span data-ttu-id="e01e3-121">Geometrie</span><span class="sxs-lookup"><span data-stu-id="e01e3-121">Geometry</span></span> | <span data-ttu-id="e01e3-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="e01e3-122">Pixel</span></span> | <span data-ttu-id="e01e3-123">Compute</span><span class="sxs-lookup"><span data-stu-id="e01e3-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e01e3-124">X</span><span class="sxs-lookup"><span data-stu-id="e01e3-124">X</span></span>      | <span data-ttu-id="e01e3-125">X</span><span class="sxs-lookup"><span data-stu-id="e01e3-125">X</span></span>    | <span data-ttu-id="e01e3-126">X</span><span class="sxs-lookup"><span data-stu-id="e01e3-126">X</span></span>      | <span data-ttu-id="e01e3-127">X</span><span class="sxs-lookup"><span data-stu-id="e01e3-127">X</span></span>        | <span data-ttu-id="e01e3-128">X</span><span class="sxs-lookup"><span data-stu-id="e01e3-128">X</span></span>     | <span data-ttu-id="e01e3-129">X</span><span class="sxs-lookup"><span data-stu-id="e01e3-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e01e3-130">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="e01e3-130">Minimum Shader Model</span></span>

<span data-ttu-id="e01e3-131">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e01e3-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e01e3-132">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="e01e3-132">Shader Model</span></span>                                              | <span data-ttu-id="e01e3-133">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="e01e3-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e01e3-134">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="e01e3-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e01e3-135">ja</span><span class="sxs-lookup"><span data-stu-id="e01e3-135">yes</span></span>       |
| [<span data-ttu-id="e01e3-136">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="e01e3-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e01e3-137">nein</span><span class="sxs-lookup"><span data-stu-id="e01e3-137">no</span></span>        |
| [<span data-ttu-id="e01e3-138">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="e01e3-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e01e3-139">nein</span><span class="sxs-lookup"><span data-stu-id="e01e3-139">no</span></span>        |
| [<span data-ttu-id="e01e3-140">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e01e3-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e01e3-141">nein</span><span class="sxs-lookup"><span data-stu-id="e01e3-141">no</span></span>        |
| [<span data-ttu-id="e01e3-142">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e01e3-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e01e3-143">nein</span><span class="sxs-lookup"><span data-stu-id="e01e3-143">no</span></span>        |
| [<span data-ttu-id="e01e3-144">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e01e3-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e01e3-145">nein</span><span class="sxs-lookup"><span data-stu-id="e01e3-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e01e3-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e01e3-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e01e3-147">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e01e3-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





