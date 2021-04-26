---
title: dmul (sm5 - asm)
description: Komponentenweise Multiplikation mit doppelter Genauigkeit.
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5d311cb5c958e8b7403197027c9854d1a93a64
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999087"
---
# <a name="dmul-sm5---asm"></a><span data-ttu-id="00abd-103">dmul (sm5 - asm)</span><span class="sxs-lookup"><span data-stu-id="00abd-103">dmul (sm5 - asm)</span></span>

<span data-ttu-id="00abd-104">Komponentenweise Multiplikation mit doppelter Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="00abd-104">Component-wise double-precision multiply.</span></span>



| <span data-ttu-id="00abd-105">dmul \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , \[ - \] src1 abs \[ \_ \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="00abd-105">dmul\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="00abd-106">Element</span><span class="sxs-lookup"><span data-stu-id="00abd-106">Item</span></span>                                                            | <span data-ttu-id="00abd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00abd-107">Description</span></span>                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00abd-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="00abd-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="00abd-109">\[in \] Die Adresse des Ergebnisses des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="00abd-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="00abd-110">*dest*  =  *src0* \* *src1*</span><span class="sxs-lookup"><span data-stu-id="00abd-110">*dest* = *src0* \* *src1*</span></span><br/> |
| <span data-ttu-id="00abd-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="00abd-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="00abd-112">\[in \] Die Komponenten, die mit *src1 multipliziert werden.*</span><span class="sxs-lookup"><span data-stu-id="00abd-112">\[in\] The components to multiply with *src1*.</span></span><br/>                                          |
| <span data-ttu-id="00abd-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="00abd-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="00abd-114">\[in \] Die Komponenten, die mit *src0 multipliziert werden.*</span><span class="sxs-lookup"><span data-stu-id="00abd-114">\[in\] The components to multiply with *src0*.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="00abd-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00abd-115">Remarks</span></span>

<span data-ttu-id="00abd-116">Die gültigen Swizzles für die Quellparameter sind .xyzw, .xyxy, .zwxy, .zwzw.</span><span class="sxs-lookup"><span data-stu-id="00abd-116">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="00abd-117">Die *gültigen Destmasken* sind .xy, .zw und .xyzw.</span><span class="sxs-lookup"><span data-stu-id="00abd-117">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="00abd-118">Die folgenden *src-Zuordnungen* sind post swizzle:</span><span class="sxs-lookup"><span data-stu-id="00abd-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="00abd-119">*dest* ist ein double vec2 über (x 32LSB, y 32MSB) und (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="00abd-119">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="00abd-120">*src0* ist ein double vec2 über (x 32LSB, y 32MSB) und (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="00abd-120">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="00abd-121">*src1* ist ein double-vec2 zwischen (x 32LSB, y 32MSB) und (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="00abd-121">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="00abd-122">Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen erzielt werden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt.</span><span class="sxs-lookup"><span data-stu-id="00abd-122">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="00abd-123">F bedeutet endliche reale Zahl.</span><span class="sxs-lookup"><span data-stu-id="00abd-123">F means finite-real number.</span></span>



| <span data-ttu-id="00abd-124">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="00abd-124">**src0 src1->**</span></span> | <span data-ttu-id="00abd-125">**-inf**</span><span class="sxs-lookup"><span data-stu-id="00abd-125">**-inf**</span></span> | <span data-ttu-id="00abd-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="00abd-126">**-F**</span></span> | <span data-ttu-id="00abd-127">**-1.0**</span><span class="sxs-lookup"><span data-stu-id="00abd-127">**-1.0**</span></span> | <span data-ttu-id="00abd-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="00abd-128">**-0**</span></span> | <span data-ttu-id="00abd-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="00abd-129">**+0**</span></span> | <span data-ttu-id="00abd-130">**+1.0**</span><span class="sxs-lookup"><span data-stu-id="00abd-130">**+1.0**</span></span> | <span data-ttu-id="00abd-131">**+F**</span><span class="sxs-lookup"><span data-stu-id="00abd-131">**+F**</span></span> | <span data-ttu-id="00abd-132">**+inf**</span><span class="sxs-lookup"><span data-stu-id="00abd-132">**+inf**</span></span> | <span data-ttu-id="00abd-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="00abd-133">**NaN**</span></span> |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="00abd-134">**-inf**</span><span class="sxs-lookup"><span data-stu-id="00abd-134">**-inf**</span></span>           | <span data-ttu-id="00abd-135">+inf</span><span class="sxs-lookup"><span data-stu-id="00abd-135">+inf</span></span>     | <span data-ttu-id="00abd-136">+inf</span><span class="sxs-lookup"><span data-stu-id="00abd-136">+inf</span></span>   | <span data-ttu-id="00abd-137">+inf</span><span class="sxs-lookup"><span data-stu-id="00abd-137">+inf</span></span>     | <span data-ttu-id="00abd-138">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-138">NaN</span></span>    | <span data-ttu-id="00abd-139">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-139">NaN</span></span>    | <span data-ttu-id="00abd-140">-inf</span><span class="sxs-lookup"><span data-stu-id="00abd-140">-inf</span></span>     | <span data-ttu-id="00abd-141">-inf</span><span class="sxs-lookup"><span data-stu-id="00abd-141">-inf</span></span>   | <span data-ttu-id="00abd-142">-inf</span><span class="sxs-lookup"><span data-stu-id="00abd-142">-inf</span></span>     | <span data-ttu-id="00abd-143">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-143">NaN</span></span>     |
| <span data-ttu-id="00abd-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="00abd-144">**-F**</span></span>             | <span data-ttu-id="00abd-145">+inf</span><span class="sxs-lookup"><span data-stu-id="00abd-145">+inf</span></span>     | <span data-ttu-id="00abd-146">+F</span><span class="sxs-lookup"><span data-stu-id="00abd-146">+F</span></span>     | <span data-ttu-id="00abd-147">-src0</span><span class="sxs-lookup"><span data-stu-id="00abd-147">-src0</span></span>    | <span data-ttu-id="00abd-148">+0</span><span class="sxs-lookup"><span data-stu-id="00abd-148">+0</span></span>     | <span data-ttu-id="00abd-149">-0</span><span class="sxs-lookup"><span data-stu-id="00abd-149">-0</span></span>     | <span data-ttu-id="00abd-150">src0</span><span class="sxs-lookup"><span data-stu-id="00abd-150">src0</span></span>     | <span data-ttu-id="00abd-151">-F</span><span class="sxs-lookup"><span data-stu-id="00abd-151">-F</span></span>     | <span data-ttu-id="00abd-152">-inf</span><span class="sxs-lookup"><span data-stu-id="00abd-152">-inf</span></span>     | <span data-ttu-id="00abd-153">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-153">NaN</span></span>     |
| <span data-ttu-id="00abd-154">**-1.0F**</span><span class="sxs-lookup"><span data-stu-id="00abd-154">**-1.0F**</span></span>          | <span data-ttu-id="00abd-155">+inf</span><span class="sxs-lookup"><span data-stu-id="00abd-155">+inf</span></span>     | <span data-ttu-id="00abd-156">-src1</span><span class="sxs-lookup"><span data-stu-id="00abd-156">-src1</span></span>  | <span data-ttu-id="00abd-157">+1.0</span><span class="sxs-lookup"><span data-stu-id="00abd-157">+1.0</span></span>     | <span data-ttu-id="00abd-158">+0</span><span class="sxs-lookup"><span data-stu-id="00abd-158">+0</span></span>     | <span data-ttu-id="00abd-159">-0</span><span class="sxs-lookup"><span data-stu-id="00abd-159">-0</span></span>     | <span data-ttu-id="00abd-160">-1.0</span><span class="sxs-lookup"><span data-stu-id="00abd-160">-1.0</span></span>     | <span data-ttu-id="00abd-161">-src1</span><span class="sxs-lookup"><span data-stu-id="00abd-161">-src1</span></span>  | <span data-ttu-id="00abd-162">-inf</span><span class="sxs-lookup"><span data-stu-id="00abd-162">-inf</span></span>     | <span data-ttu-id="00abd-163">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-163">NaN</span></span>     |
| <span data-ttu-id="00abd-164">**-0**</span><span class="sxs-lookup"><span data-stu-id="00abd-164">**-0**</span></span>             | <span data-ttu-id="00abd-165">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-165">NaN</span></span>      | <span data-ttu-id="00abd-166">+0</span><span class="sxs-lookup"><span data-stu-id="00abd-166">+0</span></span>     | <span data-ttu-id="00abd-167">+0</span><span class="sxs-lookup"><span data-stu-id="00abd-167">+0</span></span>       | <span data-ttu-id="00abd-168">+0</span><span class="sxs-lookup"><span data-stu-id="00abd-168">+0</span></span>     | <span data-ttu-id="00abd-169">-0</span><span class="sxs-lookup"><span data-stu-id="00abd-169">-0</span></span>     | <span data-ttu-id="00abd-170">-0</span><span class="sxs-lookup"><span data-stu-id="00abd-170">-0</span></span>       | <span data-ttu-id="00abd-171">-0</span><span class="sxs-lookup"><span data-stu-id="00abd-171">-0</span></span>     | <span data-ttu-id="00abd-172">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-172">NaN</span></span>      | <span data-ttu-id="00abd-173">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-173">NaN</span></span>     |
| <span data-ttu-id="00abd-174">**+0**</span><span class="sxs-lookup"><span data-stu-id="00abd-174">**+0**</span></span>             | <span data-ttu-id="00abd-175">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-175">NaN</span></span>      | <span data-ttu-id="00abd-176">-0</span><span class="sxs-lookup"><span data-stu-id="00abd-176">-0</span></span>     | <span data-ttu-id="00abd-177">-0</span><span class="sxs-lookup"><span data-stu-id="00abd-177">-0</span></span>       | <span data-ttu-id="00abd-178">-0</span><span class="sxs-lookup"><span data-stu-id="00abd-178">-0</span></span>     | <span data-ttu-id="00abd-179">+0</span><span class="sxs-lookup"><span data-stu-id="00abd-179">+0</span></span>     | <span data-ttu-id="00abd-180">+0</span><span class="sxs-lookup"><span data-stu-id="00abd-180">+0</span></span>       | <span data-ttu-id="00abd-181">+0</span><span class="sxs-lookup"><span data-stu-id="00abd-181">+0</span></span>     | <span data-ttu-id="00abd-182">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-182">NaN</span></span>      | <span data-ttu-id="00abd-183">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-183">NaN</span></span>     |
| <span data-ttu-id="00abd-184">**+1.0**</span><span class="sxs-lookup"><span data-stu-id="00abd-184">**+1.0**</span></span>           | <span data-ttu-id="00abd-185">-inf</span><span class="sxs-lookup"><span data-stu-id="00abd-185">-inf</span></span>     | <span data-ttu-id="00abd-186">src1</span><span class="sxs-lookup"><span data-stu-id="00abd-186">src1</span></span>   | <span data-ttu-id="00abd-187">-1.0</span><span class="sxs-lookup"><span data-stu-id="00abd-187">-1.0</span></span>     | <span data-ttu-id="00abd-188">-0</span><span class="sxs-lookup"><span data-stu-id="00abd-188">-0</span></span>     | <span data-ttu-id="00abd-189">+0</span><span class="sxs-lookup"><span data-stu-id="00abd-189">+0</span></span>     | <span data-ttu-id="00abd-190">+1</span><span class="sxs-lookup"><span data-stu-id="00abd-190">+1</span></span>       | <span data-ttu-id="00abd-191">src1</span><span class="sxs-lookup"><span data-stu-id="00abd-191">src1</span></span>   | <span data-ttu-id="00abd-192">+inf</span><span class="sxs-lookup"><span data-stu-id="00abd-192">+inf</span></span>     | <span data-ttu-id="00abd-193">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-193">NaN</span></span>     |
| <span data-ttu-id="00abd-194">**+F**</span><span class="sxs-lookup"><span data-stu-id="00abd-194">**+F**</span></span>             | <span data-ttu-id="00abd-195">-inf</span><span class="sxs-lookup"><span data-stu-id="00abd-195">-inf</span></span>     | <span data-ttu-id="00abd-196">-F</span><span class="sxs-lookup"><span data-stu-id="00abd-196">-F</span></span>     | <span data-ttu-id="00abd-197">-src0</span><span class="sxs-lookup"><span data-stu-id="00abd-197">-src0</span></span>    | <span data-ttu-id="00abd-198">-0</span><span class="sxs-lookup"><span data-stu-id="00abd-198">-0</span></span>     | <span data-ttu-id="00abd-199">+0</span><span class="sxs-lookup"><span data-stu-id="00abd-199">+0</span></span>     | <span data-ttu-id="00abd-200">src0</span><span class="sxs-lookup"><span data-stu-id="00abd-200">src0</span></span>     | <span data-ttu-id="00abd-201">+F</span><span class="sxs-lookup"><span data-stu-id="00abd-201">+F</span></span>     | <span data-ttu-id="00abd-202">+inf</span><span class="sxs-lookup"><span data-stu-id="00abd-202">+inf</span></span>     | <span data-ttu-id="00abd-203">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-203">NaN</span></span>     |
| <span data-ttu-id="00abd-204">**+inf**</span><span class="sxs-lookup"><span data-stu-id="00abd-204">**+inf**</span></span>           | <span data-ttu-id="00abd-205">-inf</span><span class="sxs-lookup"><span data-stu-id="00abd-205">-inf</span></span>     | <span data-ttu-id="00abd-206">-inf</span><span class="sxs-lookup"><span data-stu-id="00abd-206">-inf</span></span>   | <span data-ttu-id="00abd-207">-inf</span><span class="sxs-lookup"><span data-stu-id="00abd-207">-inf</span></span>     | <span data-ttu-id="00abd-208">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-208">NaN</span></span>    | <span data-ttu-id="00abd-209">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-209">NaN</span></span>    | <span data-ttu-id="00abd-210">+inf</span><span class="sxs-lookup"><span data-stu-id="00abd-210">+inf</span></span>     | <span data-ttu-id="00abd-211">+inf</span><span class="sxs-lookup"><span data-stu-id="00abd-211">+inf</span></span>   | <span data-ttu-id="00abd-212">+inf</span><span class="sxs-lookup"><span data-stu-id="00abd-212">+inf</span></span>     | <span data-ttu-id="00abd-213">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-213">NaN</span></span>     |
| <span data-ttu-id="00abd-214">**NaN**</span><span class="sxs-lookup"><span data-stu-id="00abd-214">**NaN**</span></span>            | <span data-ttu-id="00abd-215">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-215">NaN</span></span>      | <span data-ttu-id="00abd-216">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-216">NaN</span></span>    | <span data-ttu-id="00abd-217">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-217">NaN</span></span>      | <span data-ttu-id="00abd-218">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-218">NaN</span></span>    | <span data-ttu-id="00abd-219">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-219">NaN</span></span>    | <span data-ttu-id="00abd-220">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-220">NaN</span></span>      | <span data-ttu-id="00abd-221">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-221">NaN</span></span>    | <span data-ttu-id="00abd-222">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-222">NaN</span></span>      | <span data-ttu-id="00abd-223">NaN</span><span class="sxs-lookup"><span data-stu-id="00abd-223">NaN</span></span>     |



 

<span data-ttu-id="00abd-224">Diese Anweisung gilt für die folgenden Shaderstufen:</span><span class="sxs-lookup"><span data-stu-id="00abd-224">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="00abd-225">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="00abd-225">Vertex</span></span> | <span data-ttu-id="00abd-226">Rumpf</span><span class="sxs-lookup"><span data-stu-id="00abd-226">Hull</span></span> | <span data-ttu-id="00abd-227">Domain</span><span class="sxs-lookup"><span data-stu-id="00abd-227">Domain</span></span> | <span data-ttu-id="00abd-228">Geometrie</span><span class="sxs-lookup"><span data-stu-id="00abd-228">Geometry</span></span> | <span data-ttu-id="00abd-229">Pixel</span><span class="sxs-lookup"><span data-stu-id="00abd-229">Pixel</span></span> | <span data-ttu-id="00abd-230">Compute</span><span class="sxs-lookup"><span data-stu-id="00abd-230">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="00abd-231">X</span><span class="sxs-lookup"><span data-stu-id="00abd-231">X</span></span>      | <span data-ttu-id="00abd-232">X</span><span class="sxs-lookup"><span data-stu-id="00abd-232">X</span></span>    | <span data-ttu-id="00abd-233">X</span><span class="sxs-lookup"><span data-stu-id="00abd-233">X</span></span>      | <span data-ttu-id="00abd-234">X</span><span class="sxs-lookup"><span data-stu-id="00abd-234">X</span></span>        | <span data-ttu-id="00abd-235">X</span><span class="sxs-lookup"><span data-stu-id="00abd-235">X</span></span>     | <span data-ttu-id="00abd-236">X</span><span class="sxs-lookup"><span data-stu-id="00abd-236">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="00abd-237">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="00abd-237">Minimum Shader Model</span></span>

<span data-ttu-id="00abd-238">Diese Anweisung wird in den folgenden Shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="00abd-238">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="00abd-239">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="00abd-239">Shader Model</span></span>                                              | <span data-ttu-id="00abd-240">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="00abd-240">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="00abd-241">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="00abd-241">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="00abd-242">ja</span><span class="sxs-lookup"><span data-stu-id="00abd-242">yes</span></span>       |
| [<span data-ttu-id="00abd-243">Shadermodell 4.1</span><span class="sxs-lookup"><span data-stu-id="00abd-243">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="00abd-244">nein</span><span class="sxs-lookup"><span data-stu-id="00abd-244">no</span></span>        |
| [<span data-ttu-id="00abd-245">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="00abd-245">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="00abd-246">nein</span><span class="sxs-lookup"><span data-stu-id="00abd-246">no</span></span>        |
| [<span data-ttu-id="00abd-247">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="00abd-247">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="00abd-248">nein</span><span class="sxs-lookup"><span data-stu-id="00abd-248">no</span></span>        |
| [<span data-ttu-id="00abd-249">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="00abd-249">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="00abd-250">nein</span><span class="sxs-lookup"><span data-stu-id="00abd-250">no</span></span>        |
| [<span data-ttu-id="00abd-251">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="00abd-251">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="00abd-252">nein</span><span class="sxs-lookup"><span data-stu-id="00abd-252">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="00abd-253">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00abd-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00abd-254">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="00abd-254">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





