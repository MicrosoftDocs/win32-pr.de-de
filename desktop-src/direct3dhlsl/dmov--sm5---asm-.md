---
title: dmov (SM5-ASM)
description: Komponenten weises verschieben. | dmov (SM5-ASM)
ms.assetid: 05DBB9E2-10EC-4324-BB8F-1A9E315DE90C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b7d9c5ca0da1671ddf30fb9746333617f7688a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961526"
---
# <a name="dmov-sm5---asm"></a><span data-ttu-id="02607-104">dmov (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="02607-104">dmov (sm5 - asm)</span></span>

<span data-ttu-id="02607-105">Komponenten weises verschieben.</span><span class="sxs-lookup"><span data-stu-id="02607-105">Component-wise move.</span></span>



| <span data-ttu-id="02607-106">dmov \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="02607-106">dmov\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="02607-107">Element</span><span class="sxs-lookup"><span data-stu-id="02607-107">Item</span></span>                                                            | <span data-ttu-id="02607-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02607-108">Description</span></span>                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="02607-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="02607-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="02607-110">\[im Verschiebungs \] Ziel.</span><span class="sxs-lookup"><span data-stu-id="02607-110">\[in\] The move destination.</span></span> <span data-ttu-id="02607-111">*dest*  =  *src0*.</span><span class="sxs-lookup"><span data-stu-id="02607-111">*dest* = *src0*.</span></span><br/> |
| <span data-ttu-id="02607-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="02607-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="02607-113">\[in \] den Komponenten, die verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="02607-113">\[in\] The components to be moved.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="02607-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02607-114">Remarks</span></span>

<span data-ttu-id="02607-115">Bei den Modifizierern, mit Ausnahme von Swizzle, wird davon ausgegangen, dass die Daten Gleit Komma sind.</span><span class="sxs-lookup"><span data-stu-id="02607-115">The modifiers, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="02607-116">Das Fehlen von Modifizierern verschiebt Daten, ohne Bits zu ändern.</span><span class="sxs-lookup"><span data-stu-id="02607-116">The absence of modifiers moves data without altering bits.</span></span>

<span data-ttu-id="02607-117">Die gültigen Werte für die Quellparameter lauten ". xyzw", ". xyxy", ". zwxy", ". zwzw".</span><span class="sxs-lookup"><span data-stu-id="02607-117">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="02607-118">Die folgenden *src* -Zuordnungen sind Post-Swizzle:</span><span class="sxs-lookup"><span data-stu-id="02607-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="02607-119">*src0* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="02607-119">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="02607-120">*Quelle1* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="02607-120">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="02607-121">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="02607-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="02607-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="02607-122">Vertex</span></span> | <span data-ttu-id="02607-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="02607-123">Hull</span></span> | <span data-ttu-id="02607-124">Domain</span><span class="sxs-lookup"><span data-stu-id="02607-124">Domain</span></span> | <span data-ttu-id="02607-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="02607-125">Geometry</span></span> | <span data-ttu-id="02607-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="02607-126">Pixel</span></span> | <span data-ttu-id="02607-127">Compute</span><span class="sxs-lookup"><span data-stu-id="02607-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="02607-128">X</span><span class="sxs-lookup"><span data-stu-id="02607-128">X</span></span>      | <span data-ttu-id="02607-129">X</span><span class="sxs-lookup"><span data-stu-id="02607-129">X</span></span>    | <span data-ttu-id="02607-130">X</span><span class="sxs-lookup"><span data-stu-id="02607-130">X</span></span>      | <span data-ttu-id="02607-131">X</span><span class="sxs-lookup"><span data-stu-id="02607-131">X</span></span>        | <span data-ttu-id="02607-132">X</span><span class="sxs-lookup"><span data-stu-id="02607-132">X</span></span>     | <span data-ttu-id="02607-133">X</span><span class="sxs-lookup"><span data-stu-id="02607-133">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="02607-134">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="02607-134">Minimum Shader Model</span></span>

<span data-ttu-id="02607-135">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="02607-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="02607-136">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="02607-136">Shader Model</span></span>                                              | <span data-ttu-id="02607-137">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="02607-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="02607-138">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="02607-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="02607-139">ja</span><span class="sxs-lookup"><span data-stu-id="02607-139">yes</span></span>       |
| [<span data-ttu-id="02607-140">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="02607-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="02607-141">nein</span><span class="sxs-lookup"><span data-stu-id="02607-141">no</span></span>        |
| [<span data-ttu-id="02607-142">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="02607-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="02607-143">nein</span><span class="sxs-lookup"><span data-stu-id="02607-143">no</span></span>        |
| [<span data-ttu-id="02607-144">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="02607-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="02607-145">nein</span><span class="sxs-lookup"><span data-stu-id="02607-145">no</span></span>        |
| [<span data-ttu-id="02607-146">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="02607-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="02607-147">nein</span><span class="sxs-lookup"><span data-stu-id="02607-147">no</span></span>        |
| [<span data-ttu-id="02607-148">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="02607-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="02607-149">nein</span><span class="sxs-lookup"><span data-stu-id="02607-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="02607-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="02607-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02607-151">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="02607-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





