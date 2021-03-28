---
title: div (SM4-ASM)
description: Komponenten Weise Aufteilung.
ms.assetid: B086F069-8F43-4746-A6A5-8F4462212648
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 332d494adc2cc9bebe2e714b47ff2c5a6b299966
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038328"
---
# <a name="div-sm4---asm"></a><span data-ttu-id="b6736-103">div (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b6736-103">div (sm4 - asm)</span></span>

<span data-ttu-id="b6736-104">Komponenten Weise Aufteilung.</span><span class="sxs-lookup"><span data-stu-id="b6736-104">Component-wise divide.</span></span>



| <span data-ttu-id="b6736-105">div \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="b6736-105">div\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="b6736-106">Element</span><span class="sxs-lookup"><span data-stu-id="b6736-106">Item</span></span>                                                            | <span data-ttu-id="b6736-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b6736-107">Description</span></span>                                    |
|-----------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="b6736-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b6736-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b6736-109">\[im \] Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="b6736-109">\[in\] The result of the operation.</span></span><br/> |
| <span data-ttu-id="b6736-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b6736-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b6736-111">\[in \] der Dividende.</span><span class="sxs-lookup"><span data-stu-id="b6736-111">\[in\] The dividend.</span></span><br/>                |
| <span data-ttu-id="b6736-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="b6736-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="b6736-113">\[im \] Divisor.</span><span class="sxs-lookup"><span data-stu-id="b6736-113">\[in\] The divisor.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="b6736-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6736-114">Remarks</span></span>

<span data-ttu-id="b6736-115">In der folgenden Tabelle werden die Ergebnisse angezeigt, die bei der Ausführung der Anweisung mit verschiedenen Klassen von Zahlen erzielt wurden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt</span><span class="sxs-lookup"><span data-stu-id="b6736-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="b6736-116">Beachten Sie die beiden zulässigen Implementierungen von dividieren: a/b und a \* (1/b).</span><span class="sxs-lookup"><span data-stu-id="b6736-116">You should note the two allowed implementations of divide: a/b and a\*(1/b).</span></span>

<span data-ttu-id="b6736-117">Ein Ergebnis hierfür ist, dass für große nennenwerte (größer als 8.5070592 e + 37) Ausnahmen von der folgenden Tabelle vorliegen, wobei 1/Nenner ein denorm ist.</span><span class="sxs-lookup"><span data-stu-id="b6736-117">One outcome of this is that there are exceptions to the table below for large denominator values (greater than 8.5070592e+37), where 1/denominator is a denorm.</span></span> <span data-ttu-id="b6736-118">Da Implementierungen möglicherweise eine Teilung als \* (1/b) statt direkt a/b ausführen, und 1/ \[ großer Wert \] ein denorm ist, das geleert werden könnte, würden einige Fälle in der Tabelle zu unterschiedlichen Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="b6736-118">Because implementations may perform divide as a\*(1/b), instead of a/b directly, and 1/\[large value\] is a denorm that could get flushed, some cases in the table would produce different results.</span></span> <span data-ttu-id="b6736-119">Beispiel: (+/-) inf/(+/-)- \[ Wert > 8.5070592 e + 37 \] kann Nan für einige Implementierungen, aber (+/-) inf für andere Implementierungen verursachen.</span><span class="sxs-lookup"><span data-stu-id="b6736-119">For example, (+/-)INF / (+/-)\[value > 8.5070592e+37\] may produce NaN on some implementations, but (+/-)INF on other implementations</span></span>

<span data-ttu-id="b6736-120">In dieser Tabelle steht F für eine endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="b6736-120">In this table F means finite-real number.</span></span>



|                     |          |            |             |        |        |             |            |          |         |
|---------------------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="b6736-121">**src0 Quelle1->**</span><span class="sxs-lookup"><span data-stu-id="b6736-121">**src0 src1 ->**</span></span> | <span data-ttu-id="b6736-122">**-INF**</span><span class="sxs-lookup"><span data-stu-id="b6736-122">**-inf**</span></span> | <span data-ttu-id="b6736-123">**-F**</span><span class="sxs-lookup"><span data-stu-id="b6736-123">**-F**</span></span>     | <span data-ttu-id="b6736-124">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="b6736-124">**-denorm**</span></span> | <span data-ttu-id="b6736-125">**-0**</span><span class="sxs-lookup"><span data-stu-id="b6736-125">**-0**</span></span> | <span data-ttu-id="b6736-126">**+0**</span><span class="sxs-lookup"><span data-stu-id="b6736-126">**+0**</span></span> | <span data-ttu-id="b6736-127">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="b6736-127">**+denorm**</span></span> | <span data-ttu-id="b6736-128">**+ F**</span><span class="sxs-lookup"><span data-stu-id="b6736-128">**+F**</span></span>     | <span data-ttu-id="b6736-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="b6736-129">**+inf**</span></span> | <span data-ttu-id="b6736-130">**Ji**</span><span class="sxs-lookup"><span data-stu-id="b6736-130">**Nan**</span></span> |
| <span data-ttu-id="b6736-131">**-INF**</span><span class="sxs-lookup"><span data-stu-id="b6736-131">**-inf**</span></span>            | <span data-ttu-id="b6736-132">-inf</span><span class="sxs-lookup"><span data-stu-id="b6736-132">-inf</span></span>     | <span data-ttu-id="b6736-133">-inf</span><span class="sxs-lookup"><span data-stu-id="b6736-133">-inf</span></span>       | <span data-ttu-id="b6736-134">-inf</span><span class="sxs-lookup"><span data-stu-id="b6736-134">-inf</span></span>        | <span data-ttu-id="b6736-135">-inf</span><span class="sxs-lookup"><span data-stu-id="b6736-135">-inf</span></span>   | <span data-ttu-id="b6736-136">-inf</span><span class="sxs-lookup"><span data-stu-id="b6736-136">-inf</span></span>   | <span data-ttu-id="b6736-137">-inf</span><span class="sxs-lookup"><span data-stu-id="b6736-137">-inf</span></span>        | <span data-ttu-id="b6736-138">-inf</span><span class="sxs-lookup"><span data-stu-id="b6736-138">-inf</span></span>       | <span data-ttu-id="b6736-139">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-139">NaN</span></span>      | <span data-ttu-id="b6736-140">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-140">NaN</span></span>     |
| <span data-ttu-id="b6736-141">**-F**</span><span class="sxs-lookup"><span data-stu-id="b6736-141">**-F**</span></span>              | <span data-ttu-id="b6736-142">-inf</span><span class="sxs-lookup"><span data-stu-id="b6736-142">-inf</span></span>     | <span data-ttu-id="b6736-143">-F</span><span class="sxs-lookup"><span data-stu-id="b6736-143">-F</span></span>         | <span data-ttu-id="b6736-144">src0</span><span class="sxs-lookup"><span data-stu-id="b6736-144">src0</span></span>        | <span data-ttu-id="b6736-145">src0</span><span class="sxs-lookup"><span data-stu-id="b6736-145">src0</span></span>   | <span data-ttu-id="b6736-146">src0</span><span class="sxs-lookup"><span data-stu-id="b6736-146">src0</span></span>   | <span data-ttu-id="b6736-147">src0</span><span class="sxs-lookup"><span data-stu-id="b6736-147">src0</span></span>        | <span data-ttu-id="b6736-148">+-F oder +-0</span><span class="sxs-lookup"><span data-stu-id="b6736-148">+-F or +-0</span></span> | <span data-ttu-id="b6736-149">+inf</span><span class="sxs-lookup"><span data-stu-id="b6736-149">+inf</span></span>     | <span data-ttu-id="b6736-150">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-150">NaN</span></span>     |
| <span data-ttu-id="b6736-151">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="b6736-151">**-denorm**</span></span>         | <span data-ttu-id="b6736-152">-inf</span><span class="sxs-lookup"><span data-stu-id="b6736-152">-inf</span></span>     | <span data-ttu-id="b6736-153">src1</span><span class="sxs-lookup"><span data-stu-id="b6736-153">src1</span></span>       | <span data-ttu-id="b6736-154">-0</span><span class="sxs-lookup"><span data-stu-id="b6736-154">-0</span></span>          | <span data-ttu-id="b6736-155">-0</span><span class="sxs-lookup"><span data-stu-id="b6736-155">-0</span></span>     | <span data-ttu-id="b6736-156">+0</span><span class="sxs-lookup"><span data-stu-id="b6736-156">+0</span></span>     | <span data-ttu-id="b6736-157">+0</span><span class="sxs-lookup"><span data-stu-id="b6736-157">+0</span></span>          | <span data-ttu-id="b6736-158">src1</span><span class="sxs-lookup"><span data-stu-id="b6736-158">src1</span></span>       | <span data-ttu-id="b6736-159">+inf</span><span class="sxs-lookup"><span data-stu-id="b6736-159">+inf</span></span>     | <span data-ttu-id="b6736-160">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-160">NaN</span></span>     |
| <span data-ttu-id="b6736-161">**-0**</span><span class="sxs-lookup"><span data-stu-id="b6736-161">**-0**</span></span>              | <span data-ttu-id="b6736-162">-inf</span><span class="sxs-lookup"><span data-stu-id="b6736-162">-inf</span></span>     | <span data-ttu-id="b6736-163">src1</span><span class="sxs-lookup"><span data-stu-id="b6736-163">src1</span></span>       | <span data-ttu-id="b6736-164">-0</span><span class="sxs-lookup"><span data-stu-id="b6736-164">-0</span></span>          | <span data-ttu-id="b6736-165">-0</span><span class="sxs-lookup"><span data-stu-id="b6736-165">-0</span></span>     | <span data-ttu-id="b6736-166">+0</span><span class="sxs-lookup"><span data-stu-id="b6736-166">+0</span></span>     | <span data-ttu-id="b6736-167">+0</span><span class="sxs-lookup"><span data-stu-id="b6736-167">+0</span></span>          | <span data-ttu-id="b6736-168">src1</span><span class="sxs-lookup"><span data-stu-id="b6736-168">src1</span></span>       | <span data-ttu-id="b6736-169">+inf</span><span class="sxs-lookup"><span data-stu-id="b6736-169">+inf</span></span>     | <span data-ttu-id="b6736-170">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-170">NaN</span></span>     |
| <span data-ttu-id="b6736-171">**+0**</span><span class="sxs-lookup"><span data-stu-id="b6736-171">**+0**</span></span>              | <span data-ttu-id="b6736-172">-inf</span><span class="sxs-lookup"><span data-stu-id="b6736-172">-inf</span></span>     | <span data-ttu-id="b6736-173">src1</span><span class="sxs-lookup"><span data-stu-id="b6736-173">src1</span></span>       | <span data-ttu-id="b6736-174">+0</span><span class="sxs-lookup"><span data-stu-id="b6736-174">+0</span></span>          | <span data-ttu-id="b6736-175">+0</span><span class="sxs-lookup"><span data-stu-id="b6736-175">+0</span></span>     | <span data-ttu-id="b6736-176">+0</span><span class="sxs-lookup"><span data-stu-id="b6736-176">+0</span></span>     | <span data-ttu-id="b6736-177">+0</span><span class="sxs-lookup"><span data-stu-id="b6736-177">+0</span></span>          | <span data-ttu-id="b6736-178">src1</span><span class="sxs-lookup"><span data-stu-id="b6736-178">src1</span></span>       | <span data-ttu-id="b6736-179">+inf</span><span class="sxs-lookup"><span data-stu-id="b6736-179">+inf</span></span>     | <span data-ttu-id="b6736-180">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-180">NaN</span></span>     |
| <span data-ttu-id="b6736-181">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="b6736-181">**+denorm**</span></span>         | <span data-ttu-id="b6736-182">-inf</span><span class="sxs-lookup"><span data-stu-id="b6736-182">-inf</span></span>     | <span data-ttu-id="b6736-183">src1</span><span class="sxs-lookup"><span data-stu-id="b6736-183">src1</span></span>       | <span data-ttu-id="b6736-184">+0</span><span class="sxs-lookup"><span data-stu-id="b6736-184">+0</span></span>          | <span data-ttu-id="b6736-185">+0</span><span class="sxs-lookup"><span data-stu-id="b6736-185">+0</span></span>     | <span data-ttu-id="b6736-186">+0</span><span class="sxs-lookup"><span data-stu-id="b6736-186">+0</span></span>     | <span data-ttu-id="b6736-187">+0</span><span class="sxs-lookup"><span data-stu-id="b6736-187">+0</span></span>          | <span data-ttu-id="b6736-188">src1</span><span class="sxs-lookup"><span data-stu-id="b6736-188">src1</span></span>       | <span data-ttu-id="b6736-189">+inf</span><span class="sxs-lookup"><span data-stu-id="b6736-189">+inf</span></span>     | <span data-ttu-id="b6736-190">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-190">NaN</span></span>     |
| <span data-ttu-id="b6736-191">**+ F**</span><span class="sxs-lookup"><span data-stu-id="b6736-191">**+F**</span></span>              | <span data-ttu-id="b6736-192">-inf</span><span class="sxs-lookup"><span data-stu-id="b6736-192">-inf</span></span>     | <span data-ttu-id="b6736-193">+-F oder +-0</span><span class="sxs-lookup"><span data-stu-id="b6736-193">+-F or +-0</span></span> | <span data-ttu-id="b6736-194">src0</span><span class="sxs-lookup"><span data-stu-id="b6736-194">src0</span></span>        | <span data-ttu-id="b6736-195">src0</span><span class="sxs-lookup"><span data-stu-id="b6736-195">src0</span></span>   | <span data-ttu-id="b6736-196">src0</span><span class="sxs-lookup"><span data-stu-id="b6736-196">src0</span></span>   | <span data-ttu-id="b6736-197">src0</span><span class="sxs-lookup"><span data-stu-id="b6736-197">src0</span></span>        | <span data-ttu-id="b6736-198">+ F</span><span class="sxs-lookup"><span data-stu-id="b6736-198">+F</span></span>         | <span data-ttu-id="b6736-199">+inf</span><span class="sxs-lookup"><span data-stu-id="b6736-199">+inf</span></span>     | <span data-ttu-id="b6736-200">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-200">NaN</span></span>     |
| <span data-ttu-id="b6736-201">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="b6736-201">**+inf**</span></span>            | <span data-ttu-id="b6736-202">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-202">NaN</span></span>      | <span data-ttu-id="b6736-203">+inf</span><span class="sxs-lookup"><span data-stu-id="b6736-203">+inf</span></span>       | <span data-ttu-id="b6736-204">+inf</span><span class="sxs-lookup"><span data-stu-id="b6736-204">+inf</span></span>        | <span data-ttu-id="b6736-205">+inf</span><span class="sxs-lookup"><span data-stu-id="b6736-205">+inf</span></span>   | <span data-ttu-id="b6736-206">+inf</span><span class="sxs-lookup"><span data-stu-id="b6736-206">+inf</span></span>   | <span data-ttu-id="b6736-207">+inf</span><span class="sxs-lookup"><span data-stu-id="b6736-207">+inf</span></span>        | <span data-ttu-id="b6736-208">+inf</span><span class="sxs-lookup"><span data-stu-id="b6736-208">+inf</span></span>       | <span data-ttu-id="b6736-209">+inf</span><span class="sxs-lookup"><span data-stu-id="b6736-209">+inf</span></span>     | <span data-ttu-id="b6736-210">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-210">NaN</span></span>     |
| <span data-ttu-id="b6736-211">**NaN**</span><span class="sxs-lookup"><span data-stu-id="b6736-211">**NaN**</span></span>             | <span data-ttu-id="b6736-212">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-212">NaN</span></span>      | <span data-ttu-id="b6736-213">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-213">NaN</span></span>        | <span data-ttu-id="b6736-214">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-214">NaN</span></span>         | <span data-ttu-id="b6736-215">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-215">NaN</span></span>    | <span data-ttu-id="b6736-216">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-216">NaN</span></span>    | <span data-ttu-id="b6736-217">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-217">NaN</span></span>         | <span data-ttu-id="b6736-218">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-218">NaN</span></span>        | <span data-ttu-id="b6736-219">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-219">NaN</span></span>      | <span data-ttu-id="b6736-220">NaN</span><span class="sxs-lookup"><span data-stu-id="b6736-220">NaN</span></span>     |



 

<span data-ttu-id="b6736-221">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="b6736-221">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b6736-222">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="b6736-222">Vertex Shader</span></span> | <span data-ttu-id="b6736-223">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="b6736-223">Geometry Shader</span></span> | <span data-ttu-id="b6736-224">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="b6736-224">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b6736-225">x</span><span class="sxs-lookup"><span data-stu-id="b6736-225">x</span></span>             | <span data-ttu-id="b6736-226">x</span><span class="sxs-lookup"><span data-stu-id="b6736-226">x</span></span>               | <span data-ttu-id="b6736-227">x</span><span class="sxs-lookup"><span data-stu-id="b6736-227">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b6736-228">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="b6736-228">Minimum Shader Model</span></span>

<span data-ttu-id="b6736-229">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b6736-229">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b6736-230">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="b6736-230">Shader Model</span></span>                                              | <span data-ttu-id="b6736-231">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="b6736-231">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b6736-232">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="b6736-232">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b6736-233">ja</span><span class="sxs-lookup"><span data-stu-id="b6736-233">yes</span></span>       |
| [<span data-ttu-id="b6736-234">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="b6736-234">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b6736-235">ja</span><span class="sxs-lookup"><span data-stu-id="b6736-235">yes</span></span>       |
| [<span data-ttu-id="b6736-236">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="b6736-236">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b6736-237">ja</span><span class="sxs-lookup"><span data-stu-id="b6736-237">yes</span></span>       |
| [<span data-ttu-id="b6736-238">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6736-238">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b6736-239">nein</span><span class="sxs-lookup"><span data-stu-id="b6736-239">no</span></span>        |
| [<span data-ttu-id="b6736-240">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6736-240">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b6736-241">nein</span><span class="sxs-lookup"><span data-stu-id="b6736-241">no</span></span>        |
| [<span data-ttu-id="b6736-242">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6736-242">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b6736-243">nein</span><span class="sxs-lookup"><span data-stu-id="b6736-243">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b6736-244">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b6736-244">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6736-245">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6736-245">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





