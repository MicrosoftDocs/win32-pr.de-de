---
title: ddiv (sm5 - asm)
description: Berechnet eine komponentenweise Division mit doppelter Genauigkeit.
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fc039b222b28a5fb1217d23c78470aff1739f7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999157"
---
# <a name="ddiv-sm5---asm"></a><span data-ttu-id="c5c1a-103">ddiv (sm5 - asm)</span><span class="sxs-lookup"><span data-stu-id="c5c1a-103">ddiv (sm5 - asm)</span></span>

<span data-ttu-id="c5c1a-104">Berechnet eine komponentenweise Division mit doppelter Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="c5c1a-104">Computes a component-wise double-precision division.</span></span>



| <span data-ttu-id="c5c1a-105">ddiv \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c5c1a-105">ddiv\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="c5c1a-106">Element</span><span class="sxs-lookup"><span data-stu-id="c5c1a-106">Item</span></span>                                                            | <span data-ttu-id="c5c1a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5c1a-107">Description</span></span>                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c1a-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="c5c1a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c5c1a-109">\[in \] Das Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c5c1a-109">\[in\] The result of the operation.</span></span> <span data-ttu-id="c5c1a-110">Der Ergebniswert muss auf 0,5 ULP genau sein.</span><span class="sxs-lookup"><span data-stu-id="c5c1a-110">The result value must be accurate to 0.5 ULP.</span></span> <br/> |
| <span data-ttu-id="c5c1a-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c5c1a-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c5c1a-112">\[im \] Dividend.</span><span class="sxs-lookup"><span data-stu-id="c5c1a-112">\[in\] The dividend.</span></span><br/>                                                               |
| <span data-ttu-id="c5c1a-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="c5c1a-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="c5c1a-114">\[in \] Der Divisor.</span><span class="sxs-lookup"><span data-stu-id="c5c1a-114">\[in\] The divisor.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="c5c1a-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c5c1a-115">Remarks</span></span>

<span data-ttu-id="c5c1a-116">Die DDIV-Anweisung wird immer dann vom HLSL-Compiler ausgegeben, wenn der Divisionsoperator mit doubles verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c5c1a-116">The DDIV instruction will be emitted by the HLSL compiler whenever the division operator is used with doubles.</span></span> <span data-ttu-id="c5c1a-117">Die Genauigkeit dieser Anweisung muss 0,5 ULP sein.</span><span class="sxs-lookup"><span data-stu-id="c5c1a-117">The accuracy of this instruction will be required to be 0.5 ULP.</span></span>

<span data-ttu-id="c5c1a-118">Shader, die diese Anweisung verwenden, werden mit einem Shaderflag gekennzeichnet, das dazu führen wird, dass sie nicht gebunden werden können, es sei denn, alle folgenden Bedingungen sind erfüllt.</span><span class="sxs-lookup"><span data-stu-id="c5c1a-118">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="c5c1a-119">Das System unterstützt DirectX 11.1.</span><span class="sxs-lookup"><span data-stu-id="c5c1a-119">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="c5c1a-120">Das System enthält einen WDDM 1.2-Treiber.</span><span class="sxs-lookup"><span data-stu-id="c5c1a-120">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="c5c1a-121">Der Treiber meldet Unterstützung für diese Anweisung über **D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS. ExtendedDoublesShaderInstructions auf** **TRUE festgelegt.**</span><span class="sxs-lookup"><span data-stu-id="c5c1a-121">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="c5c1a-122">Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen enthalten sind, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt.</span><span class="sxs-lookup"><span data-stu-id="c5c1a-122">The following table shows the results btained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="c5c1a-123">In dieser Tabelle steht F für finite-real number.</span><span class="sxs-lookup"><span data-stu-id="c5c1a-123">In this table F means finite-real number.</span></span>



| <span data-ttu-id="c5c1a-124">**src0 src1 ->**</span><span class="sxs-lookup"><span data-stu-id="c5c1a-124">**src0 src1 ->**</span></span> | <span data-ttu-id="c5c1a-125">**-inf**</span><span class="sxs-lookup"><span data-stu-id="c5c1a-125">**-inf**</span></span> | <span data-ttu-id="c5c1a-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="c5c1a-126">**-F**</span></span> | <span data-ttu-id="c5c1a-127">**-1.0**</span><span class="sxs-lookup"><span data-stu-id="c5c1a-127">**-1.0**</span></span> | <span data-ttu-id="c5c1a-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="c5c1a-128">**-0**</span></span> | <span data-ttu-id="c5c1a-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="c5c1a-129">**+0**</span></span> | <span data-ttu-id="c5c1a-130">**+1.0**</span><span class="sxs-lookup"><span data-stu-id="c5c1a-130">**+1.0**</span></span> | <span data-ttu-id="c5c1a-131">**+F**</span><span class="sxs-lookup"><span data-stu-id="c5c1a-131">**+F**</span></span> | <span data-ttu-id="c5c1a-132">**+inf**</span><span class="sxs-lookup"><span data-stu-id="c5c1a-132">**+inf**</span></span> | <span data-ttu-id="c5c1a-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="c5c1a-133">**NaN**</span></span> |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="c5c1a-134">**-inf**</span><span class="sxs-lookup"><span data-stu-id="c5c1a-134">**-inf**</span></span>            | <span data-ttu-id="c5c1a-135">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-135">NaN</span></span>      | <span data-ttu-id="c5c1a-136">+inf</span><span class="sxs-lookup"><span data-stu-id="c5c1a-136">+inf</span></span>   | <span data-ttu-id="c5c1a-137">+inf</span><span class="sxs-lookup"><span data-stu-id="c5c1a-137">+inf</span></span>     | <span data-ttu-id="c5c1a-138">+inf</span><span class="sxs-lookup"><span data-stu-id="c5c1a-138">+inf</span></span>   | <span data-ttu-id="c5c1a-139">-inf</span><span class="sxs-lookup"><span data-stu-id="c5c1a-139">-inf</span></span>   | <span data-ttu-id="c5c1a-140">-inf</span><span class="sxs-lookup"><span data-stu-id="c5c1a-140">-inf</span></span>     | <span data-ttu-id="c5c1a-141">-inf</span><span class="sxs-lookup"><span data-stu-id="c5c1a-141">-inf</span></span>   | <span data-ttu-id="c5c1a-142">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-142">NaN</span></span>      | <span data-ttu-id="c5c1a-143">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-143">NaN</span></span>     |
| <span data-ttu-id="c5c1a-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="c5c1a-144">**-F**</span></span>              | <span data-ttu-id="c5c1a-145">+0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-145">+0</span></span>       | <span data-ttu-id="c5c1a-146">+F</span><span class="sxs-lookup"><span data-stu-id="c5c1a-146">+F</span></span>     | <span data-ttu-id="c5c1a-147">-src0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-147">-src0</span></span>    | <span data-ttu-id="c5c1a-148">+inf</span><span class="sxs-lookup"><span data-stu-id="c5c1a-148">+inf</span></span>   | <span data-ttu-id="c5c1a-149">-inf</span><span class="sxs-lookup"><span data-stu-id="c5c1a-149">-inf</span></span>   | <span data-ttu-id="c5c1a-150">src0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-150">src0</span></span>     | <span data-ttu-id="c5c1a-151">-F</span><span class="sxs-lookup"><span data-stu-id="c5c1a-151">-F</span></span>     | <span data-ttu-id="c5c1a-152">-0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-152">-0</span></span>       | <span data-ttu-id="c5c1a-153">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-153">NaN</span></span>     |
| <span data-ttu-id="c5c1a-154">**-0**</span><span class="sxs-lookup"><span data-stu-id="c5c1a-154">**-0**</span></span>              | <span data-ttu-id="c5c1a-155">+0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-155">+0</span></span>       | <span data-ttu-id="c5c1a-156">+0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-156">+0</span></span>     | <span data-ttu-id="c5c1a-157">+0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-157">+0</span></span>       | <span data-ttu-id="c5c1a-158">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-158">NaN</span></span>    | <span data-ttu-id="c5c1a-159">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-159">NaN</span></span>    | <span data-ttu-id="c5c1a-160">-0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-160">-0</span></span>       | <span data-ttu-id="c5c1a-161">-0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-161">-0</span></span>     | <span data-ttu-id="c5c1a-162">-0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-162">-0</span></span>       | <span data-ttu-id="c5c1a-163">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-163">NaN</span></span>     |
| <span data-ttu-id="c5c1a-164">**+0**</span><span class="sxs-lookup"><span data-stu-id="c5c1a-164">**+0**</span></span>              | <span data-ttu-id="c5c1a-165">-0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-165">-0</span></span>       | <span data-ttu-id="c5c1a-166">-0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-166">-0</span></span>     | <span data-ttu-id="c5c1a-167">-0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-167">-0</span></span>       | <span data-ttu-id="c5c1a-168">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-168">NaN</span></span>    | <span data-ttu-id="c5c1a-169">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-169">NaN</span></span>    | <span data-ttu-id="c5c1a-170">+0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-170">+0</span></span>       | <span data-ttu-id="c5c1a-171">+0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-171">+0</span></span>     | <span data-ttu-id="c5c1a-172">+0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-172">+0</span></span>       | <span data-ttu-id="c5c1a-173">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-173">NaN</span></span>     |
| <span data-ttu-id="c5c1a-174">**+F**</span><span class="sxs-lookup"><span data-stu-id="c5c1a-174">**+F**</span></span>              | <span data-ttu-id="c5c1a-175">-0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-175">-0</span></span>       | <span data-ttu-id="c5c1a-176">-F</span><span class="sxs-lookup"><span data-stu-id="c5c1a-176">-F</span></span>     | <span data-ttu-id="c5c1a-177">-src0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-177">-src0</span></span>    | <span data-ttu-id="c5c1a-178">-inf</span><span class="sxs-lookup"><span data-stu-id="c5c1a-178">-inf</span></span>   | <span data-ttu-id="c5c1a-179">+inf</span><span class="sxs-lookup"><span data-stu-id="c5c1a-179">+inf</span></span>   | <span data-ttu-id="c5c1a-180">src0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-180">src0</span></span>     | <span data-ttu-id="c5c1a-181">+F</span><span class="sxs-lookup"><span data-stu-id="c5c1a-181">+F</span></span>     | <span data-ttu-id="c5c1a-182">+0</span><span class="sxs-lookup"><span data-stu-id="c5c1a-182">+0</span></span>       | <span data-ttu-id="c5c1a-183">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-183">NaN</span></span>     |
| <span data-ttu-id="c5c1a-184">**+inf**</span><span class="sxs-lookup"><span data-stu-id="c5c1a-184">**+inf**</span></span>            | <span data-ttu-id="c5c1a-185">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-185">NaN</span></span>      | <span data-ttu-id="c5c1a-186">-inf</span><span class="sxs-lookup"><span data-stu-id="c5c1a-186">-inf</span></span>   | <span data-ttu-id="c5c1a-187">-inf</span><span class="sxs-lookup"><span data-stu-id="c5c1a-187">-inf</span></span>     | <span data-ttu-id="c5c1a-188">-inf</span><span class="sxs-lookup"><span data-stu-id="c5c1a-188">-inf</span></span>   | <span data-ttu-id="c5c1a-189">+inf</span><span class="sxs-lookup"><span data-stu-id="c5c1a-189">+inf</span></span>   | <span data-ttu-id="c5c1a-190">+inf</span><span class="sxs-lookup"><span data-stu-id="c5c1a-190">+inf</span></span>     | <span data-ttu-id="c5c1a-191">+inf</span><span class="sxs-lookup"><span data-stu-id="c5c1a-191">+inf</span></span>   | <span data-ttu-id="c5c1a-192">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-192">NaN</span></span>      | <span data-ttu-id="c5c1a-193">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-193">NaN</span></span>     |
| <span data-ttu-id="c5c1a-194">**NaN**</span><span class="sxs-lookup"><span data-stu-id="c5c1a-194">**NaN**</span></span>             | <span data-ttu-id="c5c1a-195">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-195">NaN</span></span>      | <span data-ttu-id="c5c1a-196">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-196">NaN</span></span>    | <span data-ttu-id="c5c1a-197">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-197">NaN</span></span>      | <span data-ttu-id="c5c1a-198">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-198">NaN</span></span>    | <span data-ttu-id="c5c1a-199">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-199">NaN</span></span>    | <span data-ttu-id="c5c1a-200">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-200">NaN</span></span>      | <span data-ttu-id="c5c1a-201">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-201">NaN</span></span>    | <span data-ttu-id="c5c1a-202">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-202">NaN</span></span>      | <span data-ttu-id="c5c1a-203">NaN</span><span class="sxs-lookup"><span data-stu-id="c5c1a-203">NaN</span></span>     |



 

<span data-ttu-id="c5c1a-204">Diese Anweisung gilt für die folgenden Shaderstufen:</span><span class="sxs-lookup"><span data-stu-id="c5c1a-204">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c5c1a-205">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c5c1a-205">Vertex</span></span> | <span data-ttu-id="c5c1a-206">Rumpf</span><span class="sxs-lookup"><span data-stu-id="c5c1a-206">Hull</span></span> | <span data-ttu-id="c5c1a-207">Domain</span><span class="sxs-lookup"><span data-stu-id="c5c1a-207">Domain</span></span> | <span data-ttu-id="c5c1a-208">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c5c1a-208">Geometry</span></span> | <span data-ttu-id="c5c1a-209">Pixel</span><span class="sxs-lookup"><span data-stu-id="c5c1a-209">Pixel</span></span> | <span data-ttu-id="c5c1a-210">Compute</span><span class="sxs-lookup"><span data-stu-id="c5c1a-210">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c5c1a-211">X</span><span class="sxs-lookup"><span data-stu-id="c5c1a-211">X</span></span>      | <span data-ttu-id="c5c1a-212">X</span><span class="sxs-lookup"><span data-stu-id="c5c1a-212">X</span></span>    | <span data-ttu-id="c5c1a-213">X</span><span class="sxs-lookup"><span data-stu-id="c5c1a-213">X</span></span>      | <span data-ttu-id="c5c1a-214">X</span><span class="sxs-lookup"><span data-stu-id="c5c1a-214">X</span></span>        | <span data-ttu-id="c5c1a-215">X</span><span class="sxs-lookup"><span data-stu-id="c5c1a-215">X</span></span>     | <span data-ttu-id="c5c1a-216">X</span><span class="sxs-lookup"><span data-stu-id="c5c1a-216">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c5c1a-217">Shader-Mindestmodell</span><span class="sxs-lookup"><span data-stu-id="c5c1a-217">Minimum Shader Model</span></span>

<span data-ttu-id="c5c1a-218">Diese Anweisung wird in den folgenden Shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c5c1a-218">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c5c1a-219">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c5c1a-219">Shader Model</span></span>                                              | <span data-ttu-id="c5c1a-220">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c5c1a-220">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c5c1a-221">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="c5c1a-221">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c5c1a-222">ja</span><span class="sxs-lookup"><span data-stu-id="c5c1a-222">yes</span></span>       |
| [<span data-ttu-id="c5c1a-223">Shadermodell 4.1</span><span class="sxs-lookup"><span data-stu-id="c5c1a-223">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c5c1a-224">nein</span><span class="sxs-lookup"><span data-stu-id="c5c1a-224">no</span></span>        |
| [<span data-ttu-id="c5c1a-225">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="c5c1a-225">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c5c1a-226">nein</span><span class="sxs-lookup"><span data-stu-id="c5c1a-226">no</span></span>        |
| [<span data-ttu-id="c5c1a-227">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c5c1a-227">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c5c1a-228">nein</span><span class="sxs-lookup"><span data-stu-id="c5c1a-228">no</span></span>        |
| [<span data-ttu-id="c5c1a-229">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c5c1a-229">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c5c1a-230">nein</span><span class="sxs-lookup"><span data-stu-id="c5c1a-230">no</span></span>        |
| [<span data-ttu-id="c5c1a-231">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c5c1a-231">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c5c1a-232">nein</span><span class="sxs-lookup"><span data-stu-id="c5c1a-232">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c5c1a-233">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c5c1a-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5c1a-234">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c5c1a-234">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





