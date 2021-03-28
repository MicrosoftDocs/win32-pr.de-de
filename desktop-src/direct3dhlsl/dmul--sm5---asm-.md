---
title: dmul (SM5-ASM)
description: Multiplizieren der Komponenten Weise mit doppelter Genauigkeit.
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18cce59ae237610b1038d90e02dff429812b4f00
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993054"
---
# <a name="dmul-sm5---asm"></a><span data-ttu-id="82a1d-103">dmul (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="82a1d-103">dmul (sm5 - asm)</span></span>

<span data-ttu-id="82a1d-104">Multiplizieren der Komponenten Weise mit doppelter Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="82a1d-104">Component-wise double-precision multiply.</span></span>



| <span data-ttu-id="82a1d-105">dmul \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="82a1d-105">dmul\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="82a1d-106">Element</span><span class="sxs-lookup"><span data-stu-id="82a1d-106">Item</span></span>                                                            | <span data-ttu-id="82a1d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82a1d-107">Description</span></span>                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82a1d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="82a1d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="82a1d-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="82a1d-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="82a1d-110">*dest*  =  *src0* \* *Quelle1*</span><span class="sxs-lookup"><span data-stu-id="82a1d-110">*dest* = *src0* \* *src1*</span></span><br/> |
| <span data-ttu-id="82a1d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="82a1d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="82a1d-112">\[in \] den Komponenten, die mit *Quelle1* multipliziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="82a1d-112">\[in\] The components to multiply with *src1*.</span></span><br/>                                          |
| <span data-ttu-id="82a1d-113"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="82a1d-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="82a1d-114">\[in \] den Komponenten, die mit *src0* multipliziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="82a1d-114">\[in\] The components to multiply with *src0*.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="82a1d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82a1d-115">Remarks</span></span>

<span data-ttu-id="82a1d-116">Die gültigen Werte für die Quellparameter lauten ". xyzw", ". xyxy", ". zwxy", ". zwzw".</span><span class="sxs-lookup"><span data-stu-id="82a1d-116">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="82a1d-117">Die gültigen *dest* -Masken sind. XY,. zw und. xyzw.</span><span class="sxs-lookup"><span data-stu-id="82a1d-117">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="82a1d-118">Die folgenden *src* -Zuordnungen sind Post-Swizzle:</span><span class="sxs-lookup"><span data-stu-id="82a1d-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="82a1d-119">*dest* ist eine doppelte vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="82a1d-119">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="82a1d-120">*src0* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="82a1d-120">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="82a1d-121">*Quelle1* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="82a1d-121">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="82a1d-122">In der folgenden Tabelle werden die Ergebnisse angezeigt, die bei der Ausführung der Anweisung mit verschiedenen Klassen von Zahlen erzielt wurden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt</span><span class="sxs-lookup"><span data-stu-id="82a1d-122">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="82a1d-123">F bedeutet eine endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="82a1d-123">F means finite-real number.</span></span>



|                    |          |        |          |        |        |          |        |          |         |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="82a1d-124">**src0 Quelle1->**</span><span class="sxs-lookup"><span data-stu-id="82a1d-124">**src0 src1->**</span></span> | <span data-ttu-id="82a1d-125">**-INF**</span><span class="sxs-lookup"><span data-stu-id="82a1d-125">**-inf**</span></span> | <span data-ttu-id="82a1d-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="82a1d-126">**-F**</span></span> | <span data-ttu-id="82a1d-127">**-1,0**</span><span class="sxs-lookup"><span data-stu-id="82a1d-127">**-1.0**</span></span> | <span data-ttu-id="82a1d-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="82a1d-128">**-0**</span></span> | <span data-ttu-id="82a1d-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="82a1d-129">**+0**</span></span> | <span data-ttu-id="82a1d-130">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="82a1d-130">**+1.0**</span></span> | <span data-ttu-id="82a1d-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="82a1d-131">**+F**</span></span> | <span data-ttu-id="82a1d-132">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="82a1d-132">**+inf**</span></span> | <span data-ttu-id="82a1d-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="82a1d-133">**NaN**</span></span> |
| <span data-ttu-id="82a1d-134">**-INF**</span><span class="sxs-lookup"><span data-stu-id="82a1d-134">**-inf**</span></span>           | <span data-ttu-id="82a1d-135">+inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-135">+inf</span></span>     | <span data-ttu-id="82a1d-136">+inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-136">+inf</span></span>   | <span data-ttu-id="82a1d-137">+inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-137">+inf</span></span>     | <span data-ttu-id="82a1d-138">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-138">NaN</span></span>    | <span data-ttu-id="82a1d-139">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-139">NaN</span></span>    | <span data-ttu-id="82a1d-140">-inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-140">-inf</span></span>     | <span data-ttu-id="82a1d-141">-inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-141">-inf</span></span>   | <span data-ttu-id="82a1d-142">-inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-142">-inf</span></span>     | <span data-ttu-id="82a1d-143">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-143">NaN</span></span>     |
| <span data-ttu-id="82a1d-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="82a1d-144">**-F**</span></span>             | <span data-ttu-id="82a1d-145">+inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-145">+inf</span></span>     | <span data-ttu-id="82a1d-146">+ F</span><span class="sxs-lookup"><span data-stu-id="82a1d-146">+F</span></span>     | <span data-ttu-id="82a1d-147">-src0</span><span class="sxs-lookup"><span data-stu-id="82a1d-147">-src0</span></span>    | <span data-ttu-id="82a1d-148">+0</span><span class="sxs-lookup"><span data-stu-id="82a1d-148">+0</span></span>     | <span data-ttu-id="82a1d-149">-0</span><span class="sxs-lookup"><span data-stu-id="82a1d-149">-0</span></span>     | <span data-ttu-id="82a1d-150">src0</span><span class="sxs-lookup"><span data-stu-id="82a1d-150">src0</span></span>     | <span data-ttu-id="82a1d-151">-F</span><span class="sxs-lookup"><span data-stu-id="82a1d-151">-F</span></span>     | <span data-ttu-id="82a1d-152">-inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-152">-inf</span></span>     | <span data-ttu-id="82a1d-153">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-153">NaN</span></span>     |
| <span data-ttu-id="82a1d-154">**-1.0 f**</span><span class="sxs-lookup"><span data-stu-id="82a1d-154">**-1.0F**</span></span>          | <span data-ttu-id="82a1d-155">+inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-155">+inf</span></span>     | <span data-ttu-id="82a1d-156">-Quelle1</span><span class="sxs-lookup"><span data-stu-id="82a1d-156">-src1</span></span>  | <span data-ttu-id="82a1d-157">+ 1,0</span><span class="sxs-lookup"><span data-stu-id="82a1d-157">+1.0</span></span>     | <span data-ttu-id="82a1d-158">+0</span><span class="sxs-lookup"><span data-stu-id="82a1d-158">+0</span></span>     | <span data-ttu-id="82a1d-159">-0</span><span class="sxs-lookup"><span data-stu-id="82a1d-159">-0</span></span>     | <span data-ttu-id="82a1d-160">-1.0</span><span class="sxs-lookup"><span data-stu-id="82a1d-160">-1.0</span></span>     | <span data-ttu-id="82a1d-161">-Quelle1</span><span class="sxs-lookup"><span data-stu-id="82a1d-161">-src1</span></span>  | <span data-ttu-id="82a1d-162">-inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-162">-inf</span></span>     | <span data-ttu-id="82a1d-163">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-163">NaN</span></span>     |
| <span data-ttu-id="82a1d-164">**-0**</span><span class="sxs-lookup"><span data-stu-id="82a1d-164">**-0**</span></span>             | <span data-ttu-id="82a1d-165">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-165">NaN</span></span>      | <span data-ttu-id="82a1d-166">+0</span><span class="sxs-lookup"><span data-stu-id="82a1d-166">+0</span></span>     | <span data-ttu-id="82a1d-167">+0</span><span class="sxs-lookup"><span data-stu-id="82a1d-167">+0</span></span>       | <span data-ttu-id="82a1d-168">+0</span><span class="sxs-lookup"><span data-stu-id="82a1d-168">+0</span></span>     | <span data-ttu-id="82a1d-169">-0</span><span class="sxs-lookup"><span data-stu-id="82a1d-169">-0</span></span>     | <span data-ttu-id="82a1d-170">-0</span><span class="sxs-lookup"><span data-stu-id="82a1d-170">-0</span></span>       | <span data-ttu-id="82a1d-171">-0</span><span class="sxs-lookup"><span data-stu-id="82a1d-171">-0</span></span>     | <span data-ttu-id="82a1d-172">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-172">NaN</span></span>      | <span data-ttu-id="82a1d-173">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-173">NaN</span></span>     |
| <span data-ttu-id="82a1d-174">**+0**</span><span class="sxs-lookup"><span data-stu-id="82a1d-174">**+0**</span></span>             | <span data-ttu-id="82a1d-175">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-175">NaN</span></span>      | <span data-ttu-id="82a1d-176">-0</span><span class="sxs-lookup"><span data-stu-id="82a1d-176">-0</span></span>     | <span data-ttu-id="82a1d-177">-0</span><span class="sxs-lookup"><span data-stu-id="82a1d-177">-0</span></span>       | <span data-ttu-id="82a1d-178">-0</span><span class="sxs-lookup"><span data-stu-id="82a1d-178">-0</span></span>     | <span data-ttu-id="82a1d-179">+0</span><span class="sxs-lookup"><span data-stu-id="82a1d-179">+0</span></span>     | <span data-ttu-id="82a1d-180">+0</span><span class="sxs-lookup"><span data-stu-id="82a1d-180">+0</span></span>       | <span data-ttu-id="82a1d-181">+0</span><span class="sxs-lookup"><span data-stu-id="82a1d-181">+0</span></span>     | <span data-ttu-id="82a1d-182">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-182">NaN</span></span>      | <span data-ttu-id="82a1d-183">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-183">NaN</span></span>     |
| <span data-ttu-id="82a1d-184">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="82a1d-184">**+1.0**</span></span>           | <span data-ttu-id="82a1d-185">-inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-185">-inf</span></span>     | <span data-ttu-id="82a1d-186">src1</span><span class="sxs-lookup"><span data-stu-id="82a1d-186">src1</span></span>   | <span data-ttu-id="82a1d-187">-1.0</span><span class="sxs-lookup"><span data-stu-id="82a1d-187">-1.0</span></span>     | <span data-ttu-id="82a1d-188">-0</span><span class="sxs-lookup"><span data-stu-id="82a1d-188">-0</span></span>     | <span data-ttu-id="82a1d-189">+0</span><span class="sxs-lookup"><span data-stu-id="82a1d-189">+0</span></span>     | <span data-ttu-id="82a1d-190">+1</span><span class="sxs-lookup"><span data-stu-id="82a1d-190">+1</span></span>       | <span data-ttu-id="82a1d-191">src1</span><span class="sxs-lookup"><span data-stu-id="82a1d-191">src1</span></span>   | <span data-ttu-id="82a1d-192">+inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-192">+inf</span></span>     | <span data-ttu-id="82a1d-193">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-193">NaN</span></span>     |
| <span data-ttu-id="82a1d-194">**+ F**</span><span class="sxs-lookup"><span data-stu-id="82a1d-194">**+F**</span></span>             | <span data-ttu-id="82a1d-195">-inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-195">-inf</span></span>     | <span data-ttu-id="82a1d-196">-F</span><span class="sxs-lookup"><span data-stu-id="82a1d-196">-F</span></span>     | <span data-ttu-id="82a1d-197">-src0</span><span class="sxs-lookup"><span data-stu-id="82a1d-197">-src0</span></span>    | <span data-ttu-id="82a1d-198">-0</span><span class="sxs-lookup"><span data-stu-id="82a1d-198">-0</span></span>     | <span data-ttu-id="82a1d-199">+0</span><span class="sxs-lookup"><span data-stu-id="82a1d-199">+0</span></span>     | <span data-ttu-id="82a1d-200">src0</span><span class="sxs-lookup"><span data-stu-id="82a1d-200">src0</span></span>     | <span data-ttu-id="82a1d-201">+ F</span><span class="sxs-lookup"><span data-stu-id="82a1d-201">+F</span></span>     | <span data-ttu-id="82a1d-202">+inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-202">+inf</span></span>     | <span data-ttu-id="82a1d-203">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-203">NaN</span></span>     |
| <span data-ttu-id="82a1d-204">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="82a1d-204">**+inf**</span></span>           | <span data-ttu-id="82a1d-205">-inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-205">-inf</span></span>     | <span data-ttu-id="82a1d-206">-inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-206">-inf</span></span>   | <span data-ttu-id="82a1d-207">-inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-207">-inf</span></span>     | <span data-ttu-id="82a1d-208">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-208">NaN</span></span>    | <span data-ttu-id="82a1d-209">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-209">NaN</span></span>    | <span data-ttu-id="82a1d-210">+inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-210">+inf</span></span>     | <span data-ttu-id="82a1d-211">+inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-211">+inf</span></span>   | <span data-ttu-id="82a1d-212">+inf</span><span class="sxs-lookup"><span data-stu-id="82a1d-212">+inf</span></span>     | <span data-ttu-id="82a1d-213">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-213">NaN</span></span>     |
| <span data-ttu-id="82a1d-214">**NaN**</span><span class="sxs-lookup"><span data-stu-id="82a1d-214">**NaN**</span></span>            | <span data-ttu-id="82a1d-215">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-215">NaN</span></span>      | <span data-ttu-id="82a1d-216">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-216">NaN</span></span>    | <span data-ttu-id="82a1d-217">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-217">NaN</span></span>      | <span data-ttu-id="82a1d-218">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-218">NaN</span></span>    | <span data-ttu-id="82a1d-219">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-219">NaN</span></span>    | <span data-ttu-id="82a1d-220">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-220">NaN</span></span>      | <span data-ttu-id="82a1d-221">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-221">NaN</span></span>    | <span data-ttu-id="82a1d-222">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-222">NaN</span></span>      | <span data-ttu-id="82a1d-223">NaN</span><span class="sxs-lookup"><span data-stu-id="82a1d-223">NaN</span></span>     |



 

<span data-ttu-id="82a1d-224">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="82a1d-224">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="82a1d-225">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="82a1d-225">Vertex</span></span> | <span data-ttu-id="82a1d-226">Hülle</span><span class="sxs-lookup"><span data-stu-id="82a1d-226">Hull</span></span> | <span data-ttu-id="82a1d-227">Domain</span><span class="sxs-lookup"><span data-stu-id="82a1d-227">Domain</span></span> | <span data-ttu-id="82a1d-228">Geometrie</span><span class="sxs-lookup"><span data-stu-id="82a1d-228">Geometry</span></span> | <span data-ttu-id="82a1d-229">Pixel</span><span class="sxs-lookup"><span data-stu-id="82a1d-229">Pixel</span></span> | <span data-ttu-id="82a1d-230">Compute</span><span class="sxs-lookup"><span data-stu-id="82a1d-230">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="82a1d-231">X</span><span class="sxs-lookup"><span data-stu-id="82a1d-231">X</span></span>      | <span data-ttu-id="82a1d-232">X</span><span class="sxs-lookup"><span data-stu-id="82a1d-232">X</span></span>    | <span data-ttu-id="82a1d-233">X</span><span class="sxs-lookup"><span data-stu-id="82a1d-233">X</span></span>      | <span data-ttu-id="82a1d-234">X</span><span class="sxs-lookup"><span data-stu-id="82a1d-234">X</span></span>        | <span data-ttu-id="82a1d-235">X</span><span class="sxs-lookup"><span data-stu-id="82a1d-235">X</span></span>     | <span data-ttu-id="82a1d-236">X</span><span class="sxs-lookup"><span data-stu-id="82a1d-236">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="82a1d-237">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="82a1d-237">Minimum Shader Model</span></span>

<span data-ttu-id="82a1d-238">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="82a1d-238">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="82a1d-239">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="82a1d-239">Shader Model</span></span>                                              | <span data-ttu-id="82a1d-240">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="82a1d-240">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="82a1d-241">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="82a1d-241">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="82a1d-242">ja</span><span class="sxs-lookup"><span data-stu-id="82a1d-242">yes</span></span>       |
| [<span data-ttu-id="82a1d-243">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="82a1d-243">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="82a1d-244">nein</span><span class="sxs-lookup"><span data-stu-id="82a1d-244">no</span></span>        |
| [<span data-ttu-id="82a1d-245">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="82a1d-245">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="82a1d-246">nein</span><span class="sxs-lookup"><span data-stu-id="82a1d-246">no</span></span>        |
| [<span data-ttu-id="82a1d-247">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82a1d-247">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="82a1d-248">nein</span><span class="sxs-lookup"><span data-stu-id="82a1d-248">no</span></span>        |
| [<span data-ttu-id="82a1d-249">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82a1d-249">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="82a1d-250">nein</span><span class="sxs-lookup"><span data-stu-id="82a1d-250">no</span></span>        |
| [<span data-ttu-id="82a1d-251">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82a1d-251">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="82a1d-252">nein</span><span class="sxs-lookup"><span data-stu-id="82a1d-252">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="82a1d-253">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="82a1d-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82a1d-254">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82a1d-254">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





