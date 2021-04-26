---
title: add (sm4 - asm)
description: Komponentenweises Hinzufügen von zwei Vektoren.
ms.assetid: 405A513C-B2DD-43B9-A86D-1D173B084C51
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e34f0a95ad9ee9ae4bdeed317eef133e3773311
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994977"
---
# <a name="add-sm4---asm"></a><span data-ttu-id="a4701-103">add (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="a4701-103">add (sm4 - asm)</span></span>

<span data-ttu-id="a4701-104">Komponentenweises Hinzufügen von 2 Vektoren.</span><span class="sxs-lookup"><span data-stu-id="a4701-104">Component-wise add of 2 vectors.</span></span>



| <span data-ttu-id="a4701-105">add \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , \[ - \] src1 abs \[ \_ \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="a4701-105">add\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a4701-106">Element</span><span class="sxs-lookup"><span data-stu-id="a4701-106">Item</span></span>                                                            | <span data-ttu-id="a4701-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4701-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a4701-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="a4701-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a4701-109">\[in \] Die Adresse des Ergebnisses des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="a4701-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="a4701-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a4701-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a4701-111">\[in \] Der Vektor, der *src1* hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4701-111">\[in\] The vector to add to *src1*.</span></span><br/>                |
| <span data-ttu-id="a4701-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="a4701-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="a4701-113">\[in \] Der Vektor, der *src0* hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4701-113">\[in\] The vector to add to *src0*.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="a4701-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a4701-114">Remarks</span></span>

<span data-ttu-id="a4701-115">Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen erzielt werden, vorausgesetzt, dass weder Überlauf noch Unterlauf auftreten.</span><span class="sxs-lookup"><span data-stu-id="a4701-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="a4701-116">F bedeutet endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="a4701-116">F means finite real number.</span></span>



| <span data-ttu-id="a4701-117">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="a4701-117">**src0 src1->**</span></span> | <span data-ttu-id="a4701-118">**-inf**</span><span class="sxs-lookup"><span data-stu-id="a4701-118">**-inf**</span></span> | <span data-ttu-id="a4701-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="a4701-119">**-F**</span></span>     | <span data-ttu-id="a4701-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="a4701-120">**-denorm**</span></span> | <span data-ttu-id="a4701-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="a4701-121">**-0**</span></span> | <span data-ttu-id="a4701-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="a4701-122">**+0**</span></span> | <span data-ttu-id="a4701-123">**denorm**</span><span class="sxs-lookup"><span data-stu-id="a4701-123">**denorm**</span></span> | <span data-ttu-id="a4701-124">**+F**</span><span class="sxs-lookup"><span data-stu-id="a4701-124">**+F**</span></span>     | <span data-ttu-id="a4701-125">**+inf**</span><span class="sxs-lookup"><span data-stu-id="a4701-125">**+inf**</span></span> | <span data-ttu-id="a4701-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a4701-126">**NaN**</span></span> |
|--------------------|----------|------------|-------------|--------|--------|------------|------------|----------|---------|
| <span data-ttu-id="a4701-127">**-inf**</span><span class="sxs-lookup"><span data-stu-id="a4701-127">**-inf**</span></span>           | <span data-ttu-id="a4701-128">-inf</span><span class="sxs-lookup"><span data-stu-id="a4701-128">-inf</span></span>     | <span data-ttu-id="a4701-129">-inf</span><span class="sxs-lookup"><span data-stu-id="a4701-129">-inf</span></span>       | <span data-ttu-id="a4701-130">-inf</span><span class="sxs-lookup"><span data-stu-id="a4701-130">-inf</span></span>        | <span data-ttu-id="a4701-131">-inf</span><span class="sxs-lookup"><span data-stu-id="a4701-131">-inf</span></span>   | <span data-ttu-id="a4701-132">-inf</span><span class="sxs-lookup"><span data-stu-id="a4701-132">-inf</span></span>   | <span data-ttu-id="a4701-133">-inf</span><span class="sxs-lookup"><span data-stu-id="a4701-133">-inf</span></span>       | <span data-ttu-id="a4701-134">-inf</span><span class="sxs-lookup"><span data-stu-id="a4701-134">-inf</span></span>       | <span data-ttu-id="a4701-135">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-135">NaN</span></span>      | <span data-ttu-id="a4701-136">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-136">NaN</span></span>     |
| <span data-ttu-id="a4701-137">**-F**</span><span class="sxs-lookup"><span data-stu-id="a4701-137">**-F**</span></span>             | <span data-ttu-id="a4701-138">-inf</span><span class="sxs-lookup"><span data-stu-id="a4701-138">-inf</span></span>     | <span data-ttu-id="a4701-139">-F</span><span class="sxs-lookup"><span data-stu-id="a4701-139">-F</span></span>         | <span data-ttu-id="a4701-140">src0</span><span class="sxs-lookup"><span data-stu-id="a4701-140">src0</span></span>        | <span data-ttu-id="a4701-141">src0</span><span class="sxs-lookup"><span data-stu-id="a4701-141">src0</span></span>   | <span data-ttu-id="a4701-142">src0</span><span class="sxs-lookup"><span data-stu-id="a4701-142">src0</span></span>   | <span data-ttu-id="a4701-143">src0</span><span class="sxs-lookup"><span data-stu-id="a4701-143">src0</span></span>       | <span data-ttu-id="a4701-144">+-F oder +-0</span><span class="sxs-lookup"><span data-stu-id="a4701-144">+-F or +-0</span></span> | <span data-ttu-id="a4701-145">+inf</span><span class="sxs-lookup"><span data-stu-id="a4701-145">+inf</span></span>     | <span data-ttu-id="a4701-146">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-146">NaN</span></span>     |
| <span data-ttu-id="a4701-147">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="a4701-147">**-denorm**</span></span>        | <span data-ttu-id="a4701-148">-inf</span><span class="sxs-lookup"><span data-stu-id="a4701-148">-inf</span></span>     | <span data-ttu-id="a4701-149">src1</span><span class="sxs-lookup"><span data-stu-id="a4701-149">src1</span></span>       | <span data-ttu-id="a4701-150">-0</span><span class="sxs-lookup"><span data-stu-id="a4701-150">-0</span></span>          | <span data-ttu-id="a4701-151">-0</span><span class="sxs-lookup"><span data-stu-id="a4701-151">-0</span></span>     | <span data-ttu-id="a4701-152">+0</span><span class="sxs-lookup"><span data-stu-id="a4701-152">+0</span></span>     | <span data-ttu-id="a4701-153">+0</span><span class="sxs-lookup"><span data-stu-id="a4701-153">+0</span></span>         | <span data-ttu-id="a4701-154">src1</span><span class="sxs-lookup"><span data-stu-id="a4701-154">src1</span></span>       | <span data-ttu-id="a4701-155">+inf</span><span class="sxs-lookup"><span data-stu-id="a4701-155">+inf</span></span>     | <span data-ttu-id="a4701-156">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-156">NaN</span></span>     |
| <span data-ttu-id="a4701-157">**-0**</span><span class="sxs-lookup"><span data-stu-id="a4701-157">**-0**</span></span>             | <span data-ttu-id="a4701-158">-inf</span><span class="sxs-lookup"><span data-stu-id="a4701-158">-inf</span></span>     | <span data-ttu-id="a4701-159">src1</span><span class="sxs-lookup"><span data-stu-id="a4701-159">src1</span></span>       | <span data-ttu-id="a4701-160">-0</span><span class="sxs-lookup"><span data-stu-id="a4701-160">-0</span></span>          | <span data-ttu-id="a4701-161">-0</span><span class="sxs-lookup"><span data-stu-id="a4701-161">-0</span></span>     | <span data-ttu-id="a4701-162">+0</span><span class="sxs-lookup"><span data-stu-id="a4701-162">+0</span></span>     | <span data-ttu-id="a4701-163">+0</span><span class="sxs-lookup"><span data-stu-id="a4701-163">+0</span></span>         | <span data-ttu-id="a4701-164">src1</span><span class="sxs-lookup"><span data-stu-id="a4701-164">src1</span></span>       | <span data-ttu-id="a4701-165">+inf</span><span class="sxs-lookup"><span data-stu-id="a4701-165">+inf</span></span>     | <span data-ttu-id="a4701-166">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-166">NaN</span></span>     |
| <span data-ttu-id="a4701-167">**+0**</span><span class="sxs-lookup"><span data-stu-id="a4701-167">**+0**</span></span>             | <span data-ttu-id="a4701-168">i-inf</span><span class="sxs-lookup"><span data-stu-id="a4701-168">i-inf</span></span>    | <span data-ttu-id="a4701-169">src1</span><span class="sxs-lookup"><span data-stu-id="a4701-169">src1</span></span>       | <span data-ttu-id="a4701-170">+0</span><span class="sxs-lookup"><span data-stu-id="a4701-170">+0</span></span>          | <span data-ttu-id="a4701-171">+0</span><span class="sxs-lookup"><span data-stu-id="a4701-171">+0</span></span>     | <span data-ttu-id="a4701-172">+0</span><span class="sxs-lookup"><span data-stu-id="a4701-172">+0</span></span>     | <span data-ttu-id="a4701-173">+0</span><span class="sxs-lookup"><span data-stu-id="a4701-173">+0</span></span>         | <span data-ttu-id="a4701-174">src1</span><span class="sxs-lookup"><span data-stu-id="a4701-174">src1</span></span>       | <span data-ttu-id="a4701-175">+inf</span><span class="sxs-lookup"><span data-stu-id="a4701-175">+inf</span></span>     | <span data-ttu-id="a4701-176">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-176">NaN</span></span>     |
| <span data-ttu-id="a4701-177">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="a4701-177">**+denorm**</span></span>        | <span data-ttu-id="a4701-178">-inf</span><span class="sxs-lookup"><span data-stu-id="a4701-178">-inf</span></span>     | <span data-ttu-id="a4701-179">src1</span><span class="sxs-lookup"><span data-stu-id="a4701-179">src1</span></span>       | <span data-ttu-id="a4701-180">+0</span><span class="sxs-lookup"><span data-stu-id="a4701-180">+0</span></span>          | <span data-ttu-id="a4701-181">+0</span><span class="sxs-lookup"><span data-stu-id="a4701-181">+0</span></span>     | <span data-ttu-id="a4701-182">+0</span><span class="sxs-lookup"><span data-stu-id="a4701-182">+0</span></span>     | <span data-ttu-id="a4701-183">+0</span><span class="sxs-lookup"><span data-stu-id="a4701-183">+0</span></span>         | <span data-ttu-id="a4701-184">src1</span><span class="sxs-lookup"><span data-stu-id="a4701-184">src1</span></span>       | <span data-ttu-id="a4701-185">+inf</span><span class="sxs-lookup"><span data-stu-id="a4701-185">+inf</span></span>     | <span data-ttu-id="a4701-186">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-186">NaN</span></span>     |
| <span data-ttu-id="a4701-187">**+F**</span><span class="sxs-lookup"><span data-stu-id="a4701-187">**+F**</span></span>             | <span data-ttu-id="a4701-188">-inf</span><span class="sxs-lookup"><span data-stu-id="a4701-188">-inf</span></span>     | <span data-ttu-id="a4701-189">+-F oder +-0</span><span class="sxs-lookup"><span data-stu-id="a4701-189">+-F or +-0</span></span> | <span data-ttu-id="a4701-190">src0</span><span class="sxs-lookup"><span data-stu-id="a4701-190">src0</span></span>        | <span data-ttu-id="a4701-191">src0</span><span class="sxs-lookup"><span data-stu-id="a4701-191">src0</span></span>   | <span data-ttu-id="a4701-192">src0</span><span class="sxs-lookup"><span data-stu-id="a4701-192">src0</span></span>   | <span data-ttu-id="a4701-193">src0</span><span class="sxs-lookup"><span data-stu-id="a4701-193">src0</span></span>       | <span data-ttu-id="a4701-194">+F</span><span class="sxs-lookup"><span data-stu-id="a4701-194">+F</span></span>         | <span data-ttu-id="a4701-195">+inf</span><span class="sxs-lookup"><span data-stu-id="a4701-195">+inf</span></span>     | <span data-ttu-id="a4701-196">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-196">NaN</span></span>     |
| <span data-ttu-id="a4701-197">**+inf**</span><span class="sxs-lookup"><span data-stu-id="a4701-197">**+inf**</span></span>           | <span data-ttu-id="a4701-198">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-198">NaN</span></span>      | <span data-ttu-id="a4701-199">+inf</span><span class="sxs-lookup"><span data-stu-id="a4701-199">+inf</span></span>       | <span data-ttu-id="a4701-200">+inf</span><span class="sxs-lookup"><span data-stu-id="a4701-200">+inf</span></span>        | <span data-ttu-id="a4701-201">+inf</span><span class="sxs-lookup"><span data-stu-id="a4701-201">+inf</span></span>   | <span data-ttu-id="a4701-202">+inf</span><span class="sxs-lookup"><span data-stu-id="a4701-202">+inf</span></span>   | <span data-ttu-id="a4701-203">+inf</span><span class="sxs-lookup"><span data-stu-id="a4701-203">+inf</span></span>       | <span data-ttu-id="a4701-204">+inf</span><span class="sxs-lookup"><span data-stu-id="a4701-204">+inf</span></span>       | <span data-ttu-id="a4701-205">+inf</span><span class="sxs-lookup"><span data-stu-id="a4701-205">+inf</span></span>     | <span data-ttu-id="a4701-206">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-206">NaN</span></span>     |
| <span data-ttu-id="a4701-207">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a4701-207">**NaN**</span></span>            | <span data-ttu-id="a4701-208">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-208">NaN</span></span>      | <span data-ttu-id="a4701-209">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-209">NaN</span></span>        | <span data-ttu-id="a4701-210">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-210">NaN</span></span>         | <span data-ttu-id="a4701-211">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-211">NaN</span></span>    | <span data-ttu-id="a4701-212">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-212">NaN</span></span>    | <span data-ttu-id="a4701-213">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-213">NaN</span></span>        | <span data-ttu-id="a4701-214">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-214">NaN</span></span>        | <span data-ttu-id="a4701-215">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-215">NaN</span></span>      | <span data-ttu-id="a4701-216">NaN</span><span class="sxs-lookup"><span data-stu-id="a4701-216">NaN</span></span>     |



 

<span data-ttu-id="a4701-217">Diese Anweisung gilt für die folgenden Shaderstufen:</span><span class="sxs-lookup"><span data-stu-id="a4701-217">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a4701-218">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="a4701-218">Vertex Shader</span></span> | <span data-ttu-id="a4701-219">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="a4701-219">Geometry Shader</span></span> | <span data-ttu-id="a4701-220">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="a4701-220">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a4701-221">x</span><span class="sxs-lookup"><span data-stu-id="a4701-221">x</span></span>             | <span data-ttu-id="a4701-222">x</span><span class="sxs-lookup"><span data-stu-id="a4701-222">x</span></span>               | <span data-ttu-id="a4701-223">x</span><span class="sxs-lookup"><span data-stu-id="a4701-223">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a4701-224">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="a4701-224">Minimum Shader Model</span></span>

<span data-ttu-id="a4701-225">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a4701-225">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a4701-226">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="a4701-226">Shader Model</span></span>                                              | <span data-ttu-id="a4701-227">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="a4701-227">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a4701-228">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="a4701-228">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a4701-229">ja</span><span class="sxs-lookup"><span data-stu-id="a4701-229">yes</span></span>       |
| [<span data-ttu-id="a4701-230">Shadermodell 4.1</span><span class="sxs-lookup"><span data-stu-id="a4701-230">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a4701-231">ja</span><span class="sxs-lookup"><span data-stu-id="a4701-231">yes</span></span>       |
| [<span data-ttu-id="a4701-232">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="a4701-232">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a4701-233">ja</span><span class="sxs-lookup"><span data-stu-id="a4701-233">yes</span></span>       |
| [<span data-ttu-id="a4701-234">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a4701-234">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a4701-235">nein</span><span class="sxs-lookup"><span data-stu-id="a4701-235">no</span></span>        |
| [<span data-ttu-id="a4701-236">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a4701-236">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a4701-237">nein</span><span class="sxs-lookup"><span data-stu-id="a4701-237">no</span></span>        |
| [<span data-ttu-id="a4701-238">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a4701-238">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a4701-239">nein</span><span class="sxs-lookup"><span data-stu-id="a4701-239">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a4701-240">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a4701-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4701-241">Shadermodell 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a4701-241">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





