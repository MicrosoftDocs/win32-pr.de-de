---
title: Add (SM4-ASM)
description: Komponenten weises Hinzufügen von zwei Vektoren.
ms.assetid: 405A513C-B2DD-43B9-A86D-1D173B084C51
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5630b983c88da3ba512b5fece6202e0217b2ed39
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516508"
---
# <a name="add-sm4---asm"></a><span data-ttu-id="2fcf4-103">Add (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2fcf4-103">add (sm4 - asm)</span></span>

<span data-ttu-id="2fcf4-104">Komponenten weises Hinzufügen von zwei Vektoren.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-104">Component-wise add of 2 vectors.</span></span>



| <span data-ttu-id="2fcf4-105">Add \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="2fcf4-105">add\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2fcf4-106">Element</span><span class="sxs-lookup"><span data-stu-id="2fcf4-106">Item</span></span>                                                            | <span data-ttu-id="2fcf4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fcf4-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="2fcf4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2fcf4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2fcf4-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="2fcf4-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2fcf4-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2fcf4-111">\[im \] Vektor, der *Quelle1* hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-111">\[in\] The vector to add to *src1*.</span></span><br/>                |
| <span data-ttu-id="2fcf4-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="2fcf4-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="2fcf4-113">\[im \] Vektor, der *src0* hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-113">\[in\] The vector to add to *src0*.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="2fcf4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fcf4-114">Remarks</span></span>

<span data-ttu-id="2fcf4-115">In der folgenden Tabelle werden die Ergebnisse angezeigt, die bei der Ausführung der Anweisung mit verschiedenen Klassen von Zahlen erzielt wurden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt</span><span class="sxs-lookup"><span data-stu-id="2fcf4-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="2fcf4-116">F bedeutet eine begrenzte reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-116">F means finite real number.</span></span>



|                    |          |            |             |        |        |            |            |          |         |
|--------------------|----------|------------|-------------|--------|--------|------------|------------|----------|---------|
| <span data-ttu-id="2fcf4-117">**src0 Quelle1->**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-117">**src0 src1->**</span></span> | <span data-ttu-id="2fcf4-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-118">**-inf**</span></span> | <span data-ttu-id="2fcf4-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-119">**-F**</span></span>     | <span data-ttu-id="2fcf4-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-120">**-denorm**</span></span> | <span data-ttu-id="2fcf4-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-121">**-0**</span></span> | <span data-ttu-id="2fcf4-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-122">**+0**</span></span> | <span data-ttu-id="2fcf4-123">**denorm**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-123">**denorm**</span></span> | <span data-ttu-id="2fcf4-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-124">**+F**</span></span>     | <span data-ttu-id="2fcf4-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-125">**+inf**</span></span> | <span data-ttu-id="2fcf4-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-126">**NaN**</span></span> |
| <span data-ttu-id="2fcf4-127">**-INF**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-127">**-inf**</span></span>           | <span data-ttu-id="2fcf4-128">-inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-128">-inf</span></span>     | <span data-ttu-id="2fcf4-129">-inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-129">-inf</span></span>       | <span data-ttu-id="2fcf4-130">-inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-130">-inf</span></span>        | <span data-ttu-id="2fcf4-131">-inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-131">-inf</span></span>   | <span data-ttu-id="2fcf4-132">-inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-132">-inf</span></span>   | <span data-ttu-id="2fcf4-133">-inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-133">-inf</span></span>       | <span data-ttu-id="2fcf4-134">-inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-134">-inf</span></span>       | <span data-ttu-id="2fcf4-135">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-135">NaN</span></span>      | <span data-ttu-id="2fcf4-136">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-136">NaN</span></span>     |
| <span data-ttu-id="2fcf4-137">**-F**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-137">**-F**</span></span>             | <span data-ttu-id="2fcf4-138">-inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-138">-inf</span></span>     | <span data-ttu-id="2fcf4-139">-F</span><span class="sxs-lookup"><span data-stu-id="2fcf4-139">-F</span></span>         | <span data-ttu-id="2fcf4-140">src0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-140">src0</span></span>        | <span data-ttu-id="2fcf4-141">src0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-141">src0</span></span>   | <span data-ttu-id="2fcf4-142">src0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-142">src0</span></span>   | <span data-ttu-id="2fcf4-143">src0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-143">src0</span></span>       | <span data-ttu-id="2fcf4-144">+-F oder +-0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-144">+-F or +-0</span></span> | <span data-ttu-id="2fcf4-145">+inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-145">+inf</span></span>     | <span data-ttu-id="2fcf4-146">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-146">NaN</span></span>     |
| <span data-ttu-id="2fcf4-147">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-147">**-denorm**</span></span>        | <span data-ttu-id="2fcf4-148">-inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-148">-inf</span></span>     | <span data-ttu-id="2fcf4-149">src1</span><span class="sxs-lookup"><span data-stu-id="2fcf4-149">src1</span></span>       | <span data-ttu-id="2fcf4-150">-0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-150">-0</span></span>          | <span data-ttu-id="2fcf4-151">-0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-151">-0</span></span>     | <span data-ttu-id="2fcf4-152">+0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-152">+0</span></span>     | <span data-ttu-id="2fcf4-153">+0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-153">+0</span></span>         | <span data-ttu-id="2fcf4-154">src1</span><span class="sxs-lookup"><span data-stu-id="2fcf4-154">src1</span></span>       | <span data-ttu-id="2fcf4-155">+inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-155">+inf</span></span>     | <span data-ttu-id="2fcf4-156">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-156">NaN</span></span>     |
| <span data-ttu-id="2fcf4-157">**-0**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-157">**-0**</span></span>             | <span data-ttu-id="2fcf4-158">-inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-158">-inf</span></span>     | <span data-ttu-id="2fcf4-159">src1</span><span class="sxs-lookup"><span data-stu-id="2fcf4-159">src1</span></span>       | <span data-ttu-id="2fcf4-160">-0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-160">-0</span></span>          | <span data-ttu-id="2fcf4-161">-0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-161">-0</span></span>     | <span data-ttu-id="2fcf4-162">+0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-162">+0</span></span>     | <span data-ttu-id="2fcf4-163">+0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-163">+0</span></span>         | <span data-ttu-id="2fcf4-164">src1</span><span class="sxs-lookup"><span data-stu-id="2fcf4-164">src1</span></span>       | <span data-ttu-id="2fcf4-165">+inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-165">+inf</span></span>     | <span data-ttu-id="2fcf4-166">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-166">NaN</span></span>     |
| <span data-ttu-id="2fcf4-167">**+0**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-167">**+0**</span></span>             | <span data-ttu-id="2fcf4-168">i-INF</span><span class="sxs-lookup"><span data-stu-id="2fcf4-168">i-inf</span></span>    | <span data-ttu-id="2fcf4-169">src1</span><span class="sxs-lookup"><span data-stu-id="2fcf4-169">src1</span></span>       | <span data-ttu-id="2fcf4-170">+0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-170">+0</span></span>          | <span data-ttu-id="2fcf4-171">+0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-171">+0</span></span>     | <span data-ttu-id="2fcf4-172">+0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-172">+0</span></span>     | <span data-ttu-id="2fcf4-173">+0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-173">+0</span></span>         | <span data-ttu-id="2fcf4-174">src1</span><span class="sxs-lookup"><span data-stu-id="2fcf4-174">src1</span></span>       | <span data-ttu-id="2fcf4-175">+inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-175">+inf</span></span>     | <span data-ttu-id="2fcf4-176">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-176">NaN</span></span>     |
| <span data-ttu-id="2fcf4-177">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-177">**+denorm**</span></span>        | <span data-ttu-id="2fcf4-178">-inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-178">-inf</span></span>     | <span data-ttu-id="2fcf4-179">src1</span><span class="sxs-lookup"><span data-stu-id="2fcf4-179">src1</span></span>       | <span data-ttu-id="2fcf4-180">+0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-180">+0</span></span>          | <span data-ttu-id="2fcf4-181">+0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-181">+0</span></span>     | <span data-ttu-id="2fcf4-182">+0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-182">+0</span></span>     | <span data-ttu-id="2fcf4-183">+0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-183">+0</span></span>         | <span data-ttu-id="2fcf4-184">src1</span><span class="sxs-lookup"><span data-stu-id="2fcf4-184">src1</span></span>       | <span data-ttu-id="2fcf4-185">+inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-185">+inf</span></span>     | <span data-ttu-id="2fcf4-186">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-186">NaN</span></span>     |
| <span data-ttu-id="2fcf4-187">**+ F**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-187">**+F**</span></span>             | <span data-ttu-id="2fcf4-188">-inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-188">-inf</span></span>     | <span data-ttu-id="2fcf4-189">+-F oder +-0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-189">+-F or +-0</span></span> | <span data-ttu-id="2fcf4-190">src0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-190">src0</span></span>        | <span data-ttu-id="2fcf4-191">src0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-191">src0</span></span>   | <span data-ttu-id="2fcf4-192">src0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-192">src0</span></span>   | <span data-ttu-id="2fcf4-193">src0</span><span class="sxs-lookup"><span data-stu-id="2fcf4-193">src0</span></span>       | <span data-ttu-id="2fcf4-194">+ F</span><span class="sxs-lookup"><span data-stu-id="2fcf4-194">+F</span></span>         | <span data-ttu-id="2fcf4-195">+inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-195">+inf</span></span>     | <span data-ttu-id="2fcf4-196">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-196">NaN</span></span>     |
| <span data-ttu-id="2fcf4-197">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-197">**+inf**</span></span>           | <span data-ttu-id="2fcf4-198">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-198">NaN</span></span>      | <span data-ttu-id="2fcf4-199">+inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-199">+inf</span></span>       | <span data-ttu-id="2fcf4-200">+inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-200">+inf</span></span>        | <span data-ttu-id="2fcf4-201">+inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-201">+inf</span></span>   | <span data-ttu-id="2fcf4-202">+inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-202">+inf</span></span>   | <span data-ttu-id="2fcf4-203">+inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-203">+inf</span></span>       | <span data-ttu-id="2fcf4-204">+inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-204">+inf</span></span>       | <span data-ttu-id="2fcf4-205">+inf</span><span class="sxs-lookup"><span data-stu-id="2fcf4-205">+inf</span></span>     | <span data-ttu-id="2fcf4-206">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-206">NaN</span></span>     |
| <span data-ttu-id="2fcf4-207">**NaN**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-207">**NaN**</span></span>            | <span data-ttu-id="2fcf4-208">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-208">NaN</span></span>      | <span data-ttu-id="2fcf4-209">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-209">NaN</span></span>        | <span data-ttu-id="2fcf4-210">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-210">NaN</span></span>         | <span data-ttu-id="2fcf4-211">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-211">NaN</span></span>    | <span data-ttu-id="2fcf4-212">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-212">NaN</span></span>    | <span data-ttu-id="2fcf4-213">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-213">NaN</span></span>        | <span data-ttu-id="2fcf4-214">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-214">NaN</span></span>        | <span data-ttu-id="2fcf4-215">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-215">NaN</span></span>      | <span data-ttu-id="2fcf4-216">NaN</span><span class="sxs-lookup"><span data-stu-id="2fcf4-216">NaN</span></span>     |



 

<span data-ttu-id="2fcf4-217">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="2fcf4-217">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2fcf4-218">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="2fcf4-218">Vertex Shader</span></span> | <span data-ttu-id="2fcf4-219">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="2fcf4-219">Geometry Shader</span></span> | <span data-ttu-id="2fcf4-220">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="2fcf4-220">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2fcf4-221">x</span><span class="sxs-lookup"><span data-stu-id="2fcf4-221">x</span></span>             | <span data-ttu-id="2fcf4-222">x</span><span class="sxs-lookup"><span data-stu-id="2fcf4-222">x</span></span>               | <span data-ttu-id="2fcf4-223">x</span><span class="sxs-lookup"><span data-stu-id="2fcf4-223">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2fcf4-224">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="2fcf4-224">Minimum Shader Model</span></span>

<span data-ttu-id="2fcf4-225">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-225">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2fcf4-226">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="2fcf4-226">Shader Model</span></span>                                              | <span data-ttu-id="2fcf4-227">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="2fcf4-227">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2fcf4-228">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="2fcf4-228">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2fcf4-229">ja</span><span class="sxs-lookup"><span data-stu-id="2fcf4-229">yes</span></span>       |
| [<span data-ttu-id="2fcf4-230">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="2fcf4-230">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2fcf4-231">ja</span><span class="sxs-lookup"><span data-stu-id="2fcf4-231">yes</span></span>       |
| [<span data-ttu-id="2fcf4-232">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="2fcf4-232">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2fcf4-233">ja</span><span class="sxs-lookup"><span data-stu-id="2fcf4-233">yes</span></span>       |
| [<span data-ttu-id="2fcf4-234">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fcf4-234">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2fcf4-235">nein</span><span class="sxs-lookup"><span data-stu-id="2fcf4-235">no</span></span>        |
| [<span data-ttu-id="2fcf4-236">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fcf4-236">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2fcf4-237">nein</span><span class="sxs-lookup"><span data-stu-id="2fcf4-237">no</span></span>        |
| [<span data-ttu-id="2fcf4-238">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fcf4-238">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2fcf4-239">nein</span><span class="sxs-lookup"><span data-stu-id="2fcf4-239">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2fcf4-240">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2fcf4-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fcf4-241">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fcf4-241">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





