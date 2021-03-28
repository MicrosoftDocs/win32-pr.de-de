---
title: DMin (SM5-ASM)
description: Die minimale Genauigkeit für die Komponente mit doppelter Genauigkeit.
ms.assetid: 77331B4D-C4B5-49B2-BB6A-77BD5050B575
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e199b01c68acca6609123425438f309af872fb4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038338"
---
# <a name="dmin-sm5---asm"></a><span data-ttu-id="5e029-103">DMin (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5e029-103">dmin (sm5 - asm)</span></span>

<span data-ttu-id="5e029-104">Die minimale Genauigkeit für die Komponente mit doppelter Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="5e029-104">Component-wise double-precision minimum.</span></span>



| <span data-ttu-id="5e029-105">DMin \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="5e029-105">dmin\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="5e029-106">Element</span><span class="sxs-lookup"><span data-stu-id="5e029-106">Item</span></span>                                                            | <span data-ttu-id="5e029-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e029-107">Description</span></span>                                                                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e029-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5e029-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5e029-109">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="5e029-109">\[in\] The address of the results of the operation.</span></span><br/> <span data-ttu-id="5e029-110">*dest*  =  *src0*  <  *Quelle1* ?</span><span class="sxs-lookup"><span data-stu-id="5e029-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="5e029-111">*src0* : *Quelle1*</span><span class="sxs-lookup"><span data-stu-id="5e029-111">*src0* : *src1*</span></span><br/> <span data-ttu-id="5e029-112">< wird anstelle von <= verwendet, sodass, wenn min (x, y) = x, dann Max (x, y) = y ist.</span><span class="sxs-lookup"><span data-stu-id="5e029-112">< is used instead of <= so that if min(x,y) = x then max(x,y) = y.</span></span> <br/> |
| <span data-ttu-id="5e029-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5e029-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5e029-114">\[in \] den Komponenten, die mit *Quelle1* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5e029-114">\[in\] The components to compare with *src1*.</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="5e029-115"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="5e029-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="5e029-116">\[in \] den Komponenten, die mit *src0* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5e029-116">\[in\] The components to compare with *src0*.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="5e029-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e029-117">Remarks</span></span>

<span data-ttu-id="5e029-118">Nan hat eine besondere Behandlung.</span><span class="sxs-lookup"><span data-stu-id="5e029-118">NaN has special handling.</span></span> <span data-ttu-id="5e029-119">Wenn ein Quell Operand NaN ist, wird der andere Quell Operand zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5e029-119">If one source operand is NaN, then the other source operand is returned.</span></span> <span data-ttu-id="5e029-120">Die Auswahl erfolgt pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="5e029-120">The choice is made per-component.</span></span> <span data-ttu-id="5e029-121">Wenn beide Nan sind, wird eine Nan-Darstellung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5e029-121">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="5e029-122">Die gültigen Werte für die Quellparameter lauten ". xyzw", ". xyxy", ". zwxy", ". zwzw".</span><span class="sxs-lookup"><span data-stu-id="5e029-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="5e029-123">Die gültigen *dest* -Masken sind. XY,. zw und. xyzw.</span><span class="sxs-lookup"><span data-stu-id="5e029-123">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="5e029-124">Die folgenden *src* -Zuordnungen sind Post-Swizzle:</span><span class="sxs-lookup"><span data-stu-id="5e029-124">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="5e029-125">*dest* ist eine doppelte vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="5e029-125">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="5e029-126">*src0* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="5e029-126">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="5e029-127">*Quelle1* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="5e029-127">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="5e029-128">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="5e029-128">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5e029-129">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="5e029-129">Vertex</span></span> | <span data-ttu-id="5e029-130">Hülle</span><span class="sxs-lookup"><span data-stu-id="5e029-130">Hull</span></span> | <span data-ttu-id="5e029-131">Domain</span><span class="sxs-lookup"><span data-stu-id="5e029-131">Domain</span></span> | <span data-ttu-id="5e029-132">Geometrie</span><span class="sxs-lookup"><span data-stu-id="5e029-132">Geometry</span></span> | <span data-ttu-id="5e029-133">Pixel</span><span class="sxs-lookup"><span data-stu-id="5e029-133">Pixel</span></span> | <span data-ttu-id="5e029-134">Compute</span><span class="sxs-lookup"><span data-stu-id="5e029-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5e029-135">X</span><span class="sxs-lookup"><span data-stu-id="5e029-135">X</span></span>      | <span data-ttu-id="5e029-136">X</span><span class="sxs-lookup"><span data-stu-id="5e029-136">X</span></span>    | <span data-ttu-id="5e029-137">X</span><span class="sxs-lookup"><span data-stu-id="5e029-137">X</span></span>      | <span data-ttu-id="5e029-138">X</span><span class="sxs-lookup"><span data-stu-id="5e029-138">X</span></span>        | <span data-ttu-id="5e029-139">X</span><span class="sxs-lookup"><span data-stu-id="5e029-139">X</span></span>     | <span data-ttu-id="5e029-140">X</span><span class="sxs-lookup"><span data-stu-id="5e029-140">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5e029-141">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="5e029-141">Minimum Shader Model</span></span>

<span data-ttu-id="5e029-142">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="5e029-142">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5e029-143">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="5e029-143">Shader Model</span></span>                                              | <span data-ttu-id="5e029-144">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5e029-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5e029-145">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="5e029-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5e029-146">ja</span><span class="sxs-lookup"><span data-stu-id="5e029-146">yes</span></span>       |
| [<span data-ttu-id="5e029-147">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="5e029-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5e029-148">nein</span><span class="sxs-lookup"><span data-stu-id="5e029-148">no</span></span>        |
| [<span data-ttu-id="5e029-149">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="5e029-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5e029-150">nein</span><span class="sxs-lookup"><span data-stu-id="5e029-150">no</span></span>        |
| [<span data-ttu-id="5e029-151">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e029-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5e029-152">nein</span><span class="sxs-lookup"><span data-stu-id="5e029-152">no</span></span>        |
| [<span data-ttu-id="5e029-153">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e029-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5e029-154">nein</span><span class="sxs-lookup"><span data-stu-id="5e029-154">no</span></span>        |
| [<span data-ttu-id="5e029-155">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e029-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5e029-156">nein</span><span class="sxs-lookup"><span data-stu-id="5e029-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5e029-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5e029-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e029-158">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e029-158">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





