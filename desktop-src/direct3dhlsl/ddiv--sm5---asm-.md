---
title: ddiv (SM5-ASM)
description: Berechnet eine Komponenten Weise Division mit doppelter Genauigkeit.
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56f5c3aae9d416d24f41de8d8308c5a69be9d016
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993015"
---
# <a name="ddiv-sm5---asm"></a><span data-ttu-id="68793-103">ddiv (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="68793-103">ddiv (sm5 - asm)</span></span>

<span data-ttu-id="68793-104">Berechnet eine Komponenten Weise Division mit doppelter Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="68793-104">Computes a component-wise double-precision division.</span></span>



| <span data-ttu-id="68793-105">ddiv \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="68793-105">ddiv\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="68793-106">Element</span><span class="sxs-lookup"><span data-stu-id="68793-106">Item</span></span>                                                            | <span data-ttu-id="68793-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="68793-107">Description</span></span>                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="68793-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="68793-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="68793-109">\[im \] Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="68793-109">\[in\] The result of the operation.</span></span> <span data-ttu-id="68793-110">Der Ergebniswert muss auf 0,5 ULP genau sein.</span><span class="sxs-lookup"><span data-stu-id="68793-110">The result value must be accurate to 0.5 ULP.</span></span> <br/> |
| <span data-ttu-id="68793-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="68793-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="68793-112">\[in \] der Dividende.</span><span class="sxs-lookup"><span data-stu-id="68793-112">\[in\] The dividend.</span></span><br/>                                                               |
| <span data-ttu-id="68793-113"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="68793-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="68793-114">\[im \] Divisor.</span><span class="sxs-lookup"><span data-stu-id="68793-114">\[in\] The divisor.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="68793-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68793-115">Remarks</span></span>

<span data-ttu-id="68793-116">Die ddiv-Anweisung wird vom HLSL-Compiler immer dann ausgegeben, wenn der Divisions Operator mit Double-Wert verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="68793-116">The DDIV instruction will be emitted by the HLSL compiler whenever the division operator is used with doubles.</span></span> <span data-ttu-id="68793-117">Die Genauigkeit dieser Anweisung muss 0,5 ULP sein.</span><span class="sxs-lookup"><span data-stu-id="68793-117">The accuracy of this instruction will be required to be 0.5 ULP.</span></span>

<span data-ttu-id="68793-118">Shader, die diese Anweisung verwenden, werden mit einem shaderflag gekennzeichnet, das dazu führt, dass Sie nicht gebunden werden, es sei denn, die folgenden Bedingungen sind erfüllt.</span><span class="sxs-lookup"><span data-stu-id="68793-118">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="68793-119">Das System unterstützt DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="68793-119">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="68793-120">Das System enthält einen WDDM 1,2-Treiber.</span><span class="sxs-lookup"><span data-stu-id="68793-120">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="68793-121">Der Treiber meldet die Unterstützung für diese Anweisung über **D3D11 \_ Feature \_ Data \_ D3D11 \_ options. "Extendeddoublesshaderinstructions** " ist auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="68793-121">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="68793-122">In der folgenden Tabelle werden die Ergebnisse angezeigt, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen aufgetreten sind. dabei wird davon ausgegangen, dass weder Überlauf noch Unterlauf auftreten.</span><span class="sxs-lookup"><span data-stu-id="68793-122">The following table shows the results btained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="68793-123">In dieser Tabelle steht F für eine endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="68793-123">In this table F means finite-real number.</span></span>



|                     |          |        |          |        |        |          |        |          |         |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="68793-124">**src0 Quelle1->**</span><span class="sxs-lookup"><span data-stu-id="68793-124">**src0 src1 ->**</span></span> | <span data-ttu-id="68793-125">**-INF**</span><span class="sxs-lookup"><span data-stu-id="68793-125">**-inf**</span></span> | <span data-ttu-id="68793-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="68793-126">**-F**</span></span> | <span data-ttu-id="68793-127">**-1,0**</span><span class="sxs-lookup"><span data-stu-id="68793-127">**-1.0**</span></span> | <span data-ttu-id="68793-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="68793-128">**-0**</span></span> | <span data-ttu-id="68793-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="68793-129">**+0**</span></span> | <span data-ttu-id="68793-130">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="68793-130">**+1.0**</span></span> | <span data-ttu-id="68793-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="68793-131">**+F**</span></span> | <span data-ttu-id="68793-132">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="68793-132">**+inf**</span></span> | <span data-ttu-id="68793-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="68793-133">**NaN**</span></span> |
| <span data-ttu-id="68793-134">**-INF**</span><span class="sxs-lookup"><span data-stu-id="68793-134">**-inf**</span></span>            | <span data-ttu-id="68793-135">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-135">NaN</span></span>      | <span data-ttu-id="68793-136">+inf</span><span class="sxs-lookup"><span data-stu-id="68793-136">+inf</span></span>   | <span data-ttu-id="68793-137">+inf</span><span class="sxs-lookup"><span data-stu-id="68793-137">+inf</span></span>     | <span data-ttu-id="68793-138">+inf</span><span class="sxs-lookup"><span data-stu-id="68793-138">+inf</span></span>   | <span data-ttu-id="68793-139">-inf</span><span class="sxs-lookup"><span data-stu-id="68793-139">-inf</span></span>   | <span data-ttu-id="68793-140">-inf</span><span class="sxs-lookup"><span data-stu-id="68793-140">-inf</span></span>     | <span data-ttu-id="68793-141">-inf</span><span class="sxs-lookup"><span data-stu-id="68793-141">-inf</span></span>   | <span data-ttu-id="68793-142">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-142">NaN</span></span>      | <span data-ttu-id="68793-143">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-143">NaN</span></span>     |
| <span data-ttu-id="68793-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="68793-144">**-F**</span></span>              | <span data-ttu-id="68793-145">+0</span><span class="sxs-lookup"><span data-stu-id="68793-145">+0</span></span>       | <span data-ttu-id="68793-146">+ F</span><span class="sxs-lookup"><span data-stu-id="68793-146">+F</span></span>     | <span data-ttu-id="68793-147">-src0</span><span class="sxs-lookup"><span data-stu-id="68793-147">-src0</span></span>    | <span data-ttu-id="68793-148">+inf</span><span class="sxs-lookup"><span data-stu-id="68793-148">+inf</span></span>   | <span data-ttu-id="68793-149">-inf</span><span class="sxs-lookup"><span data-stu-id="68793-149">-inf</span></span>   | <span data-ttu-id="68793-150">src0</span><span class="sxs-lookup"><span data-stu-id="68793-150">src0</span></span>     | <span data-ttu-id="68793-151">-F</span><span class="sxs-lookup"><span data-stu-id="68793-151">-F</span></span>     | <span data-ttu-id="68793-152">-0</span><span class="sxs-lookup"><span data-stu-id="68793-152">-0</span></span>       | <span data-ttu-id="68793-153">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-153">NaN</span></span>     |
| <span data-ttu-id="68793-154">**-0**</span><span class="sxs-lookup"><span data-stu-id="68793-154">**-0**</span></span>              | <span data-ttu-id="68793-155">+0</span><span class="sxs-lookup"><span data-stu-id="68793-155">+0</span></span>       | <span data-ttu-id="68793-156">+0</span><span class="sxs-lookup"><span data-stu-id="68793-156">+0</span></span>     | <span data-ttu-id="68793-157">+0</span><span class="sxs-lookup"><span data-stu-id="68793-157">+0</span></span>       | <span data-ttu-id="68793-158">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-158">NaN</span></span>    | <span data-ttu-id="68793-159">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-159">NaN</span></span>    | <span data-ttu-id="68793-160">-0</span><span class="sxs-lookup"><span data-stu-id="68793-160">-0</span></span>       | <span data-ttu-id="68793-161">-0</span><span class="sxs-lookup"><span data-stu-id="68793-161">-0</span></span>     | <span data-ttu-id="68793-162">-0</span><span class="sxs-lookup"><span data-stu-id="68793-162">-0</span></span>       | <span data-ttu-id="68793-163">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-163">NaN</span></span>     |
| <span data-ttu-id="68793-164">**+0**</span><span class="sxs-lookup"><span data-stu-id="68793-164">**+0**</span></span>              | <span data-ttu-id="68793-165">-0</span><span class="sxs-lookup"><span data-stu-id="68793-165">-0</span></span>       | <span data-ttu-id="68793-166">-0</span><span class="sxs-lookup"><span data-stu-id="68793-166">-0</span></span>     | <span data-ttu-id="68793-167">-0</span><span class="sxs-lookup"><span data-stu-id="68793-167">-0</span></span>       | <span data-ttu-id="68793-168">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-168">NaN</span></span>    | <span data-ttu-id="68793-169">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-169">NaN</span></span>    | <span data-ttu-id="68793-170">+0</span><span class="sxs-lookup"><span data-stu-id="68793-170">+0</span></span>       | <span data-ttu-id="68793-171">+0</span><span class="sxs-lookup"><span data-stu-id="68793-171">+0</span></span>     | <span data-ttu-id="68793-172">+0</span><span class="sxs-lookup"><span data-stu-id="68793-172">+0</span></span>       | <span data-ttu-id="68793-173">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-173">NaN</span></span>     |
| <span data-ttu-id="68793-174">**+ F**</span><span class="sxs-lookup"><span data-stu-id="68793-174">**+F**</span></span>              | <span data-ttu-id="68793-175">-0</span><span class="sxs-lookup"><span data-stu-id="68793-175">-0</span></span>       | <span data-ttu-id="68793-176">-F</span><span class="sxs-lookup"><span data-stu-id="68793-176">-F</span></span>     | <span data-ttu-id="68793-177">-src0</span><span class="sxs-lookup"><span data-stu-id="68793-177">-src0</span></span>    | <span data-ttu-id="68793-178">-inf</span><span class="sxs-lookup"><span data-stu-id="68793-178">-inf</span></span>   | <span data-ttu-id="68793-179">+inf</span><span class="sxs-lookup"><span data-stu-id="68793-179">+inf</span></span>   | <span data-ttu-id="68793-180">src0</span><span class="sxs-lookup"><span data-stu-id="68793-180">src0</span></span>     | <span data-ttu-id="68793-181">+ F</span><span class="sxs-lookup"><span data-stu-id="68793-181">+F</span></span>     | <span data-ttu-id="68793-182">+0</span><span class="sxs-lookup"><span data-stu-id="68793-182">+0</span></span>       | <span data-ttu-id="68793-183">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-183">NaN</span></span>     |
| <span data-ttu-id="68793-184">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="68793-184">**+inf**</span></span>            | <span data-ttu-id="68793-185">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-185">NaN</span></span>      | <span data-ttu-id="68793-186">-inf</span><span class="sxs-lookup"><span data-stu-id="68793-186">-inf</span></span>   | <span data-ttu-id="68793-187">-inf</span><span class="sxs-lookup"><span data-stu-id="68793-187">-inf</span></span>     | <span data-ttu-id="68793-188">-inf</span><span class="sxs-lookup"><span data-stu-id="68793-188">-inf</span></span>   | <span data-ttu-id="68793-189">+inf</span><span class="sxs-lookup"><span data-stu-id="68793-189">+inf</span></span>   | <span data-ttu-id="68793-190">+inf</span><span class="sxs-lookup"><span data-stu-id="68793-190">+inf</span></span>     | <span data-ttu-id="68793-191">+inf</span><span class="sxs-lookup"><span data-stu-id="68793-191">+inf</span></span>   | <span data-ttu-id="68793-192">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-192">NaN</span></span>      | <span data-ttu-id="68793-193">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-193">NaN</span></span>     |
| <span data-ttu-id="68793-194">**NaN**</span><span class="sxs-lookup"><span data-stu-id="68793-194">**NaN**</span></span>             | <span data-ttu-id="68793-195">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-195">NaN</span></span>      | <span data-ttu-id="68793-196">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-196">NaN</span></span>    | <span data-ttu-id="68793-197">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-197">NaN</span></span>      | <span data-ttu-id="68793-198">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-198">NaN</span></span>    | <span data-ttu-id="68793-199">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-199">NaN</span></span>    | <span data-ttu-id="68793-200">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-200">NaN</span></span>      | <span data-ttu-id="68793-201">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-201">NaN</span></span>    | <span data-ttu-id="68793-202">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-202">NaN</span></span>      | <span data-ttu-id="68793-203">NaN</span><span class="sxs-lookup"><span data-stu-id="68793-203">NaN</span></span>     |



 

<span data-ttu-id="68793-204">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="68793-204">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="68793-205">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="68793-205">Vertex</span></span> | <span data-ttu-id="68793-206">Hülle</span><span class="sxs-lookup"><span data-stu-id="68793-206">Hull</span></span> | <span data-ttu-id="68793-207">Domain</span><span class="sxs-lookup"><span data-stu-id="68793-207">Domain</span></span> | <span data-ttu-id="68793-208">Geometrie</span><span class="sxs-lookup"><span data-stu-id="68793-208">Geometry</span></span> | <span data-ttu-id="68793-209">Pixel</span><span class="sxs-lookup"><span data-stu-id="68793-209">Pixel</span></span> | <span data-ttu-id="68793-210">Compute</span><span class="sxs-lookup"><span data-stu-id="68793-210">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="68793-211">X</span><span class="sxs-lookup"><span data-stu-id="68793-211">X</span></span>      | <span data-ttu-id="68793-212">X</span><span class="sxs-lookup"><span data-stu-id="68793-212">X</span></span>    | <span data-ttu-id="68793-213">X</span><span class="sxs-lookup"><span data-stu-id="68793-213">X</span></span>      | <span data-ttu-id="68793-214">X</span><span class="sxs-lookup"><span data-stu-id="68793-214">X</span></span>        | <span data-ttu-id="68793-215">X</span><span class="sxs-lookup"><span data-stu-id="68793-215">X</span></span>     | <span data-ttu-id="68793-216">X</span><span class="sxs-lookup"><span data-stu-id="68793-216">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="68793-217">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="68793-217">Minimum Shader Model</span></span>

<span data-ttu-id="68793-218">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="68793-218">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="68793-219">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="68793-219">Shader Model</span></span>                                              | <span data-ttu-id="68793-220">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="68793-220">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="68793-221">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="68793-221">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="68793-222">ja</span><span class="sxs-lookup"><span data-stu-id="68793-222">yes</span></span>       |
| [<span data-ttu-id="68793-223">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="68793-223">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="68793-224">nein</span><span class="sxs-lookup"><span data-stu-id="68793-224">no</span></span>        |
| [<span data-ttu-id="68793-225">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="68793-225">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="68793-226">nein</span><span class="sxs-lookup"><span data-stu-id="68793-226">no</span></span>        |
| [<span data-ttu-id="68793-227">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="68793-227">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="68793-228">nein</span><span class="sxs-lookup"><span data-stu-id="68793-228">no</span></span>        |
| [<span data-ttu-id="68793-229">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="68793-229">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="68793-230">nein</span><span class="sxs-lookup"><span data-stu-id="68793-230">no</span></span>        |
| [<span data-ttu-id="68793-231">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="68793-231">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="68793-232">nein</span><span class="sxs-lookup"><span data-stu-id="68793-232">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="68793-233">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="68793-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68793-234">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="68793-234">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





