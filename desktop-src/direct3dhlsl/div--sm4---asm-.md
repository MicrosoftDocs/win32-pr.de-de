---
title: div (sm4 - asm)
description: Komponentenweise Division.
ms.assetid: B086F069-8F43-4746-A6A5-8F4462212648
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d406c5e61b4615990b445abe169619227d22124c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999097"
---
# <a name="div-sm4---asm"></a><span data-ttu-id="bc41f-103">div (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="bc41f-103">div (sm4 - asm)</span></span>

<span data-ttu-id="bc41f-104">Komponentenweise Division.</span><span class="sxs-lookup"><span data-stu-id="bc41f-104">Component-wise divide.</span></span>



| <span data-ttu-id="bc41f-105">div \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="bc41f-105">div\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="bc41f-106">Element</span><span class="sxs-lookup"><span data-stu-id="bc41f-106">Item</span></span>                                                            | <span data-ttu-id="bc41f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc41f-107">Description</span></span>                                    |
|-----------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="bc41f-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="bc41f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="bc41f-109">\[in \] Das Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="bc41f-109">\[in\] The result of the operation.</span></span><br/> |
| <span data-ttu-id="bc41f-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="bc41f-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="bc41f-111">\[im \] Dividend.</span><span class="sxs-lookup"><span data-stu-id="bc41f-111">\[in\] The dividend.</span></span><br/>                |
| <span data-ttu-id="bc41f-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="bc41f-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="bc41f-113">\[in \] Der Divisor.</span><span class="sxs-lookup"><span data-stu-id="bc41f-113">\[in\] The divisor.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="bc41f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bc41f-114">Remarks</span></span>

<span data-ttu-id="bc41f-115">Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen erzielt werden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt.</span><span class="sxs-lookup"><span data-stu-id="bc41f-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="bc41f-116">Beachten Sie die beiden zulässigen Implementierungen von divide: a/b und a \* (1/b).</span><span class="sxs-lookup"><span data-stu-id="bc41f-116">You should note the two allowed implementations of divide: a/b and a\*(1/b).</span></span>

<span data-ttu-id="bc41f-117">Ein Ergebnis davon ist, dass für große Nennerwerte (größer als 8,5070592e+37), bei denen 1/Nenner eine Denorm ist, Ausnahmen von der folgenden Tabelle gelten.</span><span class="sxs-lookup"><span data-stu-id="bc41f-117">One outcome of this is that there are exceptions to the table below for large denominator values (greater than 8.5070592e+37), where 1/denominator is a denorm.</span></span> <span data-ttu-id="bc41f-118">Da Implementierungen eine Division als \* (1/b) ausführen können, anstatt direkt a/b, und ein großer Wert ein Denormal ist, der geleert werden kann, führen einige Fälle in der Tabelle zu unterschiedlichen \[ \] Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="bc41f-118">Because implementations may perform divide as a\*(1/b), instead of a/b directly, and 1/\[large value\] is a denorm that could get flushed, some cases in the table would produce different results.</span></span> <span data-ttu-id="bc41f-119">Beispielsweise kann der (+/-)INF/(+/-)-Wert \[ > 8.5070592e+37 für einige Implementierungen \] NaN erzeugen, aber (+/-)INF für andere Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="bc41f-119">For example, (+/-)INF / (+/-)\[value > 8.5070592e+37\] may produce NaN on some implementations, but (+/-)INF on other implementations</span></span>

<span data-ttu-id="bc41f-120">In dieser Tabelle steht F für finite-real number.</span><span class="sxs-lookup"><span data-stu-id="bc41f-120">In this table F means finite-real number.</span></span>



| <span data-ttu-id="bc41f-121">**src0 src1 ->**</span><span class="sxs-lookup"><span data-stu-id="bc41f-121">**src0 src1 ->**</span></span> | <span data-ttu-id="bc41f-122">**-inf**</span><span class="sxs-lookup"><span data-stu-id="bc41f-122">**-inf**</span></span> | <span data-ttu-id="bc41f-123">**-F**</span><span class="sxs-lookup"><span data-stu-id="bc41f-123">**-F**</span></span>     | <span data-ttu-id="bc41f-124">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="bc41f-124">**-denorm**</span></span> | <span data-ttu-id="bc41f-125">**-0**</span><span class="sxs-lookup"><span data-stu-id="bc41f-125">**-0**</span></span> | <span data-ttu-id="bc41f-126">**+0**</span><span class="sxs-lookup"><span data-stu-id="bc41f-126">**+0**</span></span> | <span data-ttu-id="bc41f-127">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="bc41f-127">**+denorm**</span></span> | <span data-ttu-id="bc41f-128">**+F**</span><span class="sxs-lookup"><span data-stu-id="bc41f-128">**+F**</span></span>     | <span data-ttu-id="bc41f-129">**+inf**</span><span class="sxs-lookup"><span data-stu-id="bc41f-129">**+inf**</span></span> | <span data-ttu-id="bc41f-130">**Nan**</span><span class="sxs-lookup"><span data-stu-id="bc41f-130">**Nan**</span></span> |
|---------------------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="bc41f-131">**-inf**</span><span class="sxs-lookup"><span data-stu-id="bc41f-131">**-inf**</span></span>            | <span data-ttu-id="bc41f-132">-inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-132">-inf</span></span>     | <span data-ttu-id="bc41f-133">-inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-133">-inf</span></span>       | <span data-ttu-id="bc41f-134">-inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-134">-inf</span></span>        | <span data-ttu-id="bc41f-135">-inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-135">-inf</span></span>   | <span data-ttu-id="bc41f-136">-inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-136">-inf</span></span>   | <span data-ttu-id="bc41f-137">-inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-137">-inf</span></span>        | <span data-ttu-id="bc41f-138">-inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-138">-inf</span></span>       | <span data-ttu-id="bc41f-139">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-139">NaN</span></span>      | <span data-ttu-id="bc41f-140">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-140">NaN</span></span>     |
| <span data-ttu-id="bc41f-141">**-F**</span><span class="sxs-lookup"><span data-stu-id="bc41f-141">**-F**</span></span>              | <span data-ttu-id="bc41f-142">-inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-142">-inf</span></span>     | <span data-ttu-id="bc41f-143">-F</span><span class="sxs-lookup"><span data-stu-id="bc41f-143">-F</span></span>         | <span data-ttu-id="bc41f-144">src0</span><span class="sxs-lookup"><span data-stu-id="bc41f-144">src0</span></span>        | <span data-ttu-id="bc41f-145">src0</span><span class="sxs-lookup"><span data-stu-id="bc41f-145">src0</span></span>   | <span data-ttu-id="bc41f-146">src0</span><span class="sxs-lookup"><span data-stu-id="bc41f-146">src0</span></span>   | <span data-ttu-id="bc41f-147">src0</span><span class="sxs-lookup"><span data-stu-id="bc41f-147">src0</span></span>        | <span data-ttu-id="bc41f-148">+-F oder +-0</span><span class="sxs-lookup"><span data-stu-id="bc41f-148">+-F or +-0</span></span> | <span data-ttu-id="bc41f-149">+inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-149">+inf</span></span>     | <span data-ttu-id="bc41f-150">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-150">NaN</span></span>     |
| <span data-ttu-id="bc41f-151">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="bc41f-151">**-denorm**</span></span>         | <span data-ttu-id="bc41f-152">-inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-152">-inf</span></span>     | <span data-ttu-id="bc41f-153">src1</span><span class="sxs-lookup"><span data-stu-id="bc41f-153">src1</span></span>       | <span data-ttu-id="bc41f-154">-0</span><span class="sxs-lookup"><span data-stu-id="bc41f-154">-0</span></span>          | <span data-ttu-id="bc41f-155">-0</span><span class="sxs-lookup"><span data-stu-id="bc41f-155">-0</span></span>     | <span data-ttu-id="bc41f-156">+0</span><span class="sxs-lookup"><span data-stu-id="bc41f-156">+0</span></span>     | <span data-ttu-id="bc41f-157">+0</span><span class="sxs-lookup"><span data-stu-id="bc41f-157">+0</span></span>          | <span data-ttu-id="bc41f-158">src1</span><span class="sxs-lookup"><span data-stu-id="bc41f-158">src1</span></span>       | <span data-ttu-id="bc41f-159">+inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-159">+inf</span></span>     | <span data-ttu-id="bc41f-160">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-160">NaN</span></span>     |
| <span data-ttu-id="bc41f-161">**-0**</span><span class="sxs-lookup"><span data-stu-id="bc41f-161">**-0**</span></span>              | <span data-ttu-id="bc41f-162">-inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-162">-inf</span></span>     | <span data-ttu-id="bc41f-163">src1</span><span class="sxs-lookup"><span data-stu-id="bc41f-163">src1</span></span>       | <span data-ttu-id="bc41f-164">-0</span><span class="sxs-lookup"><span data-stu-id="bc41f-164">-0</span></span>          | <span data-ttu-id="bc41f-165">-0</span><span class="sxs-lookup"><span data-stu-id="bc41f-165">-0</span></span>     | <span data-ttu-id="bc41f-166">+0</span><span class="sxs-lookup"><span data-stu-id="bc41f-166">+0</span></span>     | <span data-ttu-id="bc41f-167">+0</span><span class="sxs-lookup"><span data-stu-id="bc41f-167">+0</span></span>          | <span data-ttu-id="bc41f-168">src1</span><span class="sxs-lookup"><span data-stu-id="bc41f-168">src1</span></span>       | <span data-ttu-id="bc41f-169">+inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-169">+inf</span></span>     | <span data-ttu-id="bc41f-170">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-170">NaN</span></span>     |
| <span data-ttu-id="bc41f-171">**+0**</span><span class="sxs-lookup"><span data-stu-id="bc41f-171">**+0**</span></span>              | <span data-ttu-id="bc41f-172">-inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-172">-inf</span></span>     | <span data-ttu-id="bc41f-173">src1</span><span class="sxs-lookup"><span data-stu-id="bc41f-173">src1</span></span>       | <span data-ttu-id="bc41f-174">+0</span><span class="sxs-lookup"><span data-stu-id="bc41f-174">+0</span></span>          | <span data-ttu-id="bc41f-175">+0</span><span class="sxs-lookup"><span data-stu-id="bc41f-175">+0</span></span>     | <span data-ttu-id="bc41f-176">+0</span><span class="sxs-lookup"><span data-stu-id="bc41f-176">+0</span></span>     | <span data-ttu-id="bc41f-177">+0</span><span class="sxs-lookup"><span data-stu-id="bc41f-177">+0</span></span>          | <span data-ttu-id="bc41f-178">src1</span><span class="sxs-lookup"><span data-stu-id="bc41f-178">src1</span></span>       | <span data-ttu-id="bc41f-179">+inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-179">+inf</span></span>     | <span data-ttu-id="bc41f-180">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-180">NaN</span></span>     |
| <span data-ttu-id="bc41f-181">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="bc41f-181">**+denorm**</span></span>         | <span data-ttu-id="bc41f-182">-inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-182">-inf</span></span>     | <span data-ttu-id="bc41f-183">src1</span><span class="sxs-lookup"><span data-stu-id="bc41f-183">src1</span></span>       | <span data-ttu-id="bc41f-184">+0</span><span class="sxs-lookup"><span data-stu-id="bc41f-184">+0</span></span>          | <span data-ttu-id="bc41f-185">+0</span><span class="sxs-lookup"><span data-stu-id="bc41f-185">+0</span></span>     | <span data-ttu-id="bc41f-186">+0</span><span class="sxs-lookup"><span data-stu-id="bc41f-186">+0</span></span>     | <span data-ttu-id="bc41f-187">+0</span><span class="sxs-lookup"><span data-stu-id="bc41f-187">+0</span></span>          | <span data-ttu-id="bc41f-188">src1</span><span class="sxs-lookup"><span data-stu-id="bc41f-188">src1</span></span>       | <span data-ttu-id="bc41f-189">+inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-189">+inf</span></span>     | <span data-ttu-id="bc41f-190">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-190">NaN</span></span>     |
| <span data-ttu-id="bc41f-191">**+F**</span><span class="sxs-lookup"><span data-stu-id="bc41f-191">**+F**</span></span>              | <span data-ttu-id="bc41f-192">-inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-192">-inf</span></span>     | <span data-ttu-id="bc41f-193">+-F oder +-0</span><span class="sxs-lookup"><span data-stu-id="bc41f-193">+-F or +-0</span></span> | <span data-ttu-id="bc41f-194">src0</span><span class="sxs-lookup"><span data-stu-id="bc41f-194">src0</span></span>        | <span data-ttu-id="bc41f-195">src0</span><span class="sxs-lookup"><span data-stu-id="bc41f-195">src0</span></span>   | <span data-ttu-id="bc41f-196">src0</span><span class="sxs-lookup"><span data-stu-id="bc41f-196">src0</span></span>   | <span data-ttu-id="bc41f-197">src0</span><span class="sxs-lookup"><span data-stu-id="bc41f-197">src0</span></span>        | <span data-ttu-id="bc41f-198">+F</span><span class="sxs-lookup"><span data-stu-id="bc41f-198">+F</span></span>         | <span data-ttu-id="bc41f-199">+inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-199">+inf</span></span>     | <span data-ttu-id="bc41f-200">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-200">NaN</span></span>     |
| <span data-ttu-id="bc41f-201">**+inf**</span><span class="sxs-lookup"><span data-stu-id="bc41f-201">**+inf**</span></span>            | <span data-ttu-id="bc41f-202">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-202">NaN</span></span>      | <span data-ttu-id="bc41f-203">+inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-203">+inf</span></span>       | <span data-ttu-id="bc41f-204">+inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-204">+inf</span></span>        | <span data-ttu-id="bc41f-205">+inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-205">+inf</span></span>   | <span data-ttu-id="bc41f-206">+inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-206">+inf</span></span>   | <span data-ttu-id="bc41f-207">+inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-207">+inf</span></span>        | <span data-ttu-id="bc41f-208">+inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-208">+inf</span></span>       | <span data-ttu-id="bc41f-209">+inf</span><span class="sxs-lookup"><span data-stu-id="bc41f-209">+inf</span></span>     | <span data-ttu-id="bc41f-210">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-210">NaN</span></span>     |
| <span data-ttu-id="bc41f-211">**NaN**</span><span class="sxs-lookup"><span data-stu-id="bc41f-211">**NaN**</span></span>             | <span data-ttu-id="bc41f-212">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-212">NaN</span></span>      | <span data-ttu-id="bc41f-213">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-213">NaN</span></span>        | <span data-ttu-id="bc41f-214">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-214">NaN</span></span>         | <span data-ttu-id="bc41f-215">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-215">NaN</span></span>    | <span data-ttu-id="bc41f-216">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-216">NaN</span></span>    | <span data-ttu-id="bc41f-217">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-217">NaN</span></span>         | <span data-ttu-id="bc41f-218">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-218">NaN</span></span>        | <span data-ttu-id="bc41f-219">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-219">NaN</span></span>      | <span data-ttu-id="bc41f-220">NaN</span><span class="sxs-lookup"><span data-stu-id="bc41f-220">NaN</span></span>     |



 

<span data-ttu-id="bc41f-221">Diese Anweisung gilt für die folgenden Shaderstufen:</span><span class="sxs-lookup"><span data-stu-id="bc41f-221">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bc41f-222">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="bc41f-222">Vertex Shader</span></span> | <span data-ttu-id="bc41f-223">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="bc41f-223">Geometry Shader</span></span> | <span data-ttu-id="bc41f-224">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="bc41f-224">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="bc41f-225">x</span><span class="sxs-lookup"><span data-stu-id="bc41f-225">x</span></span>             | <span data-ttu-id="bc41f-226">x</span><span class="sxs-lookup"><span data-stu-id="bc41f-226">x</span></span>               | <span data-ttu-id="bc41f-227">x</span><span class="sxs-lookup"><span data-stu-id="bc41f-227">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bc41f-228">Shader-Mindestmodell</span><span class="sxs-lookup"><span data-stu-id="bc41f-228">Minimum Shader Model</span></span>

<span data-ttu-id="bc41f-229">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bc41f-229">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bc41f-230">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="bc41f-230">Shader Model</span></span>                                              | <span data-ttu-id="bc41f-231">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="bc41f-231">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bc41f-232">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="bc41f-232">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bc41f-233">ja</span><span class="sxs-lookup"><span data-stu-id="bc41f-233">yes</span></span>       |
| [<span data-ttu-id="bc41f-234">Shadermodell 4.1</span><span class="sxs-lookup"><span data-stu-id="bc41f-234">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bc41f-235">ja</span><span class="sxs-lookup"><span data-stu-id="bc41f-235">yes</span></span>       |
| [<span data-ttu-id="bc41f-236">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="bc41f-236">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bc41f-237">ja</span><span class="sxs-lookup"><span data-stu-id="bc41f-237">yes</span></span>       |
| [<span data-ttu-id="bc41f-238">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bc41f-238">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bc41f-239">nein</span><span class="sxs-lookup"><span data-stu-id="bc41f-239">no</span></span>        |
| [<span data-ttu-id="bc41f-240">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bc41f-240">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bc41f-241">nein</span><span class="sxs-lookup"><span data-stu-id="bc41f-241">no</span></span>        |
| [<span data-ttu-id="bc41f-242">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bc41f-242">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bc41f-243">nein</span><span class="sxs-lookup"><span data-stu-id="bc41f-243">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bc41f-244">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bc41f-244">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc41f-245">Shadermodell 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bc41f-245">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





