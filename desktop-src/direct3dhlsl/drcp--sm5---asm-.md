---
title: drcp (sm5 – asm)
description: Berechnet einen komponentenweisen Kehrwert mit doppelter Genauigkeit.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 770159f5007b08f5482ba8b58634b44e7f3e6ef0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998337"
---
# <a name="drcp-sm5---asm"></a><span data-ttu-id="ecd7d-103">drcp (sm5 – asm)</span><span class="sxs-lookup"><span data-stu-id="ecd7d-103">drcp (sm5 - asm)</span></span>

<span data-ttu-id="ecd7d-104">Berechnet einen komponentenweisen Kehrwert mit doppelter Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="ecd7d-104">Computes a component-wise double-precision reciprocal.</span></span>



| <span data-ttu-id="ecd7d-105">rcp \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="ecd7d-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="ecd7d-106">Element</span><span class="sxs-lookup"><span data-stu-id="ecd7d-106">Item</span></span>                                                            | <span data-ttu-id="ecd7d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ecd7d-107">Description</span></span>                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecd7d-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="ecd7d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ecd7d-109">\[in \] Die Adresse der Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="ecd7d-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="ecd7d-110">*dest*  =  **1.0**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="ecd7d-110">*dest* = **1.0** / *src0*.</span></span> <span data-ttu-id="ecd7d-111">Der Ergebniswert muss auf 1,0 ULP genau sein.</span><span class="sxs-lookup"><span data-stu-id="ecd7d-111">The result value must be accurate to 1.0 ULP</span></span><br/> |
| <span data-ttu-id="ecd7d-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ecd7d-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ecd7d-113">\[in \] Die Zahl, von der der Kehrwert annimmt wird.</span><span class="sxs-lookup"><span data-stu-id="ecd7d-113">\[in\] The number to take the reciprocal of.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="ecd7d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ecd7d-114">Remarks</span></span>

<span data-ttu-id="ecd7d-115">Die DRCP-Anweisung wird vom HLSL-Compiler nur ausgegeben, wenn sie explizit über die systeminterne rcp()-Anweisung aufgerufen wird, wenn ein Double als Argument verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ecd7d-115">The DRCP instruction is emitted by the HLSL compiler only when explicitly called via the rcp() intrinsic, when a double is used as the argument.</span></span> <span data-ttu-id="ecd7d-116">Die Genauigkeit dieser Anweisung muss 1,0 ULP sein.</span><span class="sxs-lookup"><span data-stu-id="ecd7d-116">The accuracy of this instruction is required to be 1.0 ULP.</span></span>

<span data-ttu-id="ecd7d-117">Shader, die diese Anweisung verwenden, werden mit einem Shaderflag gekennzeichnet, das dazu führt, dass sie nicht gebunden werden, es sei denn, alle folgenden Bedingungen sind erfüllt.</span><span class="sxs-lookup"><span data-stu-id="ecd7d-117">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="ecd7d-118">Das System unterstützt DirectX 11.1.</span><span class="sxs-lookup"><span data-stu-id="ecd7d-118">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="ecd7d-119">Das System enthält einen WDDM 1.2-Treiber.</span><span class="sxs-lookup"><span data-stu-id="ecd7d-119">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="ecd7d-120">Der Treiber meldet Unterstützung für diese Anweisung über **D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS. ExtendedDoublesShaderInstructions** ist auf **TRUE** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ecd7d-120">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="ecd7d-121">Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen erzielt werden, vorausgesetzt, dass weder Überlauf noch Unterlauf auftreten.</span><span class="sxs-lookup"><span data-stu-id="ecd7d-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="ecd7d-122">In dieser Tabelle bedeutet F endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="ecd7d-122">In this table F means finite-real number.</span></span>



| <span data-ttu-id="ecd7d-123">**Src**-></span><span class="sxs-lookup"><span data-stu-id="ecd7d-123">**src**-></span></span>  | <span data-ttu-id="ecd7d-124">**-inf**</span><span class="sxs-lookup"><span data-stu-id="ecd7d-124">**-inf**</span></span> | <span data-ttu-id="ecd7d-125">**-F**</span><span class="sxs-lookup"><span data-stu-id="ecd7d-125">**-F**</span></span> | <span data-ttu-id="ecd7d-126">**-0**</span><span class="sxs-lookup"><span data-stu-id="ecd7d-126">**-0**</span></span> | <span data-ttu-id="ecd7d-127">**+0**</span><span class="sxs-lookup"><span data-stu-id="ecd7d-127">**+0**</span></span> | <span data-ttu-id="ecd7d-128">**+F**</span><span class="sxs-lookup"><span data-stu-id="ecd7d-128">**+F**</span></span> | <span data-ttu-id="ecd7d-129">**+inf**</span><span class="sxs-lookup"><span data-stu-id="ecd7d-129">**+inf**</span></span> | <span data-ttu-id="ecd7d-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="ecd7d-130">**NaN**</span></span> |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| <span data-ttu-id="ecd7d-131">**Dest**-></span><span class="sxs-lookup"><span data-stu-id="ecd7d-131">**dest**-></span></span> | <span data-ttu-id="ecd7d-132">-0</span><span class="sxs-lookup"><span data-stu-id="ecd7d-132">-0</span></span>       | <span data-ttu-id="ecd7d-133">-F</span><span class="sxs-lookup"><span data-stu-id="ecd7d-133">-F</span></span>     | <span data-ttu-id="ecd7d-134">-inf</span><span class="sxs-lookup"><span data-stu-id="ecd7d-134">-inf</span></span>   | <span data-ttu-id="ecd7d-135">+inf</span><span class="sxs-lookup"><span data-stu-id="ecd7d-135">+inf</span></span>   | <span data-ttu-id="ecd7d-136">+F</span><span class="sxs-lookup"><span data-stu-id="ecd7d-136">+F</span></span>     | <span data-ttu-id="ecd7d-137">+0</span><span class="sxs-lookup"><span data-stu-id="ecd7d-137">+0</span></span>       | <span data-ttu-id="ecd7d-138">NaN</span><span class="sxs-lookup"><span data-stu-id="ecd7d-138">NaN</span></span>     |



 

<span data-ttu-id="ecd7d-139">Diese Anweisung gilt für die folgenden Shaderstufen:</span><span class="sxs-lookup"><span data-stu-id="ecd7d-139">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ecd7d-140">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="ecd7d-140">Vertex</span></span> | <span data-ttu-id="ecd7d-141">Rumpf</span><span class="sxs-lookup"><span data-stu-id="ecd7d-141">Hull</span></span> | <span data-ttu-id="ecd7d-142">Domain</span><span class="sxs-lookup"><span data-stu-id="ecd7d-142">Domain</span></span> | <span data-ttu-id="ecd7d-143">Geometrie</span><span class="sxs-lookup"><span data-stu-id="ecd7d-143">Geometry</span></span> | <span data-ttu-id="ecd7d-144">Pixel</span><span class="sxs-lookup"><span data-stu-id="ecd7d-144">Pixel</span></span> | <span data-ttu-id="ecd7d-145">Compute</span><span class="sxs-lookup"><span data-stu-id="ecd7d-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ecd7d-146">X</span><span class="sxs-lookup"><span data-stu-id="ecd7d-146">X</span></span>      | <span data-ttu-id="ecd7d-147">X</span><span class="sxs-lookup"><span data-stu-id="ecd7d-147">X</span></span>    | <span data-ttu-id="ecd7d-148">X</span><span class="sxs-lookup"><span data-stu-id="ecd7d-148">X</span></span>      | <span data-ttu-id="ecd7d-149">X</span><span class="sxs-lookup"><span data-stu-id="ecd7d-149">X</span></span>        | <span data-ttu-id="ecd7d-150">X</span><span class="sxs-lookup"><span data-stu-id="ecd7d-150">X</span></span>     | <span data-ttu-id="ecd7d-151">X</span><span class="sxs-lookup"><span data-stu-id="ecd7d-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ecd7d-152">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="ecd7d-152">Minimum Shader Model</span></span>

<span data-ttu-id="ecd7d-153">Diese Anweisung wird in den folgenden Shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ecd7d-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ecd7d-154">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="ecd7d-154">Shader Model</span></span>                                              | <span data-ttu-id="ecd7d-155">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ecd7d-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ecd7d-156">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="ecd7d-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ecd7d-157">ja</span><span class="sxs-lookup"><span data-stu-id="ecd7d-157">yes</span></span>       |
| [<span data-ttu-id="ecd7d-158">Shadermodell 4.1</span><span class="sxs-lookup"><span data-stu-id="ecd7d-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ecd7d-159">nein</span><span class="sxs-lookup"><span data-stu-id="ecd7d-159">no</span></span>        |
| [<span data-ttu-id="ecd7d-160">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="ecd7d-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ecd7d-161">nein</span><span class="sxs-lookup"><span data-stu-id="ecd7d-161">no</span></span>        |
| [<span data-ttu-id="ecd7d-162">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecd7d-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ecd7d-163">nein</span><span class="sxs-lookup"><span data-stu-id="ecd7d-163">no</span></span>        |
| [<span data-ttu-id="ecd7d-164">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecd7d-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ecd7d-165">nein</span><span class="sxs-lookup"><span data-stu-id="ecd7d-165">no</span></span>        |
| [<span data-ttu-id="ecd7d-166">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecd7d-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ecd7d-167">nein</span><span class="sxs-lookup"><span data-stu-id="ecd7d-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ecd7d-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ecd7d-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecd7d-169">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecd7d-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





