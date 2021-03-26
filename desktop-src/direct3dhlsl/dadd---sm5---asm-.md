---
title: Dadd (SM5-ASM)
description: Komponenten weises addieren mit doppelter Genauigkeit.
ms.assetid: 416F1103-E27B-4AFC-9ED1-492FF8A93492
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e217a03a5ba9e4da0d365bbfd15e4283f1a69cb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389499"
---
# <a name="dadd-sm5---asm"></a><span data-ttu-id="4d1fb-103">Dadd (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="4d1fb-103">dadd (sm5 - asm)</span></span>

<span data-ttu-id="4d1fb-104">Komponenten weises addieren mit doppelter Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="4d1fb-104">Component-wise double-precision add.</span></span>



| <span data-ttu-id="4d1fb-105">Dadd \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="4d1fb-105">dadd\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="4d1fb-106">Element</span><span class="sxs-lookup"><span data-stu-id="4d1fb-106">Item</span></span>                                                            | <span data-ttu-id="4d1fb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d1fb-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="4d1fb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="4d1fb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="4d1fb-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="4d1fb-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="4d1fb-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4d1fb-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="4d1fb-111">\[in \] den Komponenten, die mit *Quelle1* hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4d1fb-111">\[in\] The components to add with *src1*.</span></span><br/>          |
| <span data-ttu-id="4d1fb-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="4d1fb-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="4d1fb-113">\[in \] den Komponenten, die mit *src0* hinzugefügt werden sollen</span><span class="sxs-lookup"><span data-stu-id="4d1fb-113">\[in\] The components to add with *src0*</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="4d1fb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d1fb-114">Remarks</span></span>

<span data-ttu-id="4d1fb-115">Die gültigen Werte für die Quellparameter lauten ". xyzw", ". xyxy", ". zwxy", ". zwzw".</span><span class="sxs-lookup"><span data-stu-id="4d1fb-115">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="4d1fb-116">Die gültigen *dest* -Masken sind. XY,. zw und. xyzw.</span><span class="sxs-lookup"><span data-stu-id="4d1fb-116">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="4d1fb-117">Die folgenden Zuordnungen sind Post-Swizzle:</span><span class="sxs-lookup"><span data-stu-id="4d1fb-117">The following mappings are post-swizzle:</span></span>

-   <span data-ttu-id="4d1fb-118">*dest* ist eine doppelte vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="4d1fb-118">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="4d1fb-119">*src0* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="4d1fb-119">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="4d1fb-120">*Quelle1* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="4d1fb-120">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="4d1fb-121">In der folgenden Tabelle werden die Ergebnisse angezeigt, die bei der Ausführung der Anweisung mit verschiedenen Klassen von Zahlen erzielt wurden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt</span><span class="sxs-lookup"><span data-stu-id="4d1fb-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="4d1fb-122">F bedeutet eine endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="4d1fb-122">F means finite-real number.</span></span>



<table>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="4d1fb-123"><strong>src0</strong></span><span class="sxs-lookup"><span data-stu-id="4d1fb-123"><strong>src0</strong></span></span><br /><span data-ttu-id="4d1fb-124">
<strong>Quelle1-></strong></span><span class="sxs-lookup"><span data-stu-id="4d1fb-124">
<strong>src1-></strong></span></span><br />
</dl></td>
<td><span data-ttu-id="4d1fb-125"><strong>-INF</strong></span><span class="sxs-lookup"><span data-stu-id="4d1fb-125"><strong>-inf</strong></span></span></td>
<td><span data-ttu-id="4d1fb-126"><strong>-F</strong></span><span class="sxs-lookup"><span data-stu-id="4d1fb-126"><strong>-F</strong></span></span></td>
<td><span data-ttu-id="4d1fb-127"><strong>-0</strong></span><span class="sxs-lookup"><span data-stu-id="4d1fb-127"><strong>-0</strong></span></span></td>
<td><span data-ttu-id="4d1fb-128"><strong>+0</strong></span><span class="sxs-lookup"><span data-stu-id="4d1fb-128"><strong>+0</strong></span></span></td>
<td><span data-ttu-id="4d1fb-129"><strong>+ F</strong></span><span class="sxs-lookup"><span data-stu-id="4d1fb-129"><strong>+F</strong></span></span></td>
<td><span data-ttu-id="4d1fb-130"><strong>+ INF</strong></span><span class="sxs-lookup"><span data-stu-id="4d1fb-130"><strong>+inf</strong></span></span></td>
<td><span data-ttu-id="4d1fb-131"><strong>NaN</strong></span><span class="sxs-lookup"><span data-stu-id="4d1fb-131"><strong>NaN</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d1fb-132"><strong>-INF</strong></span><span class="sxs-lookup"><span data-stu-id="4d1fb-132"><strong>-inf</strong></span></span></td>
<td><span data-ttu-id="4d1fb-133">-inf</span><span class="sxs-lookup"><span data-stu-id="4d1fb-133">-inf</span></span></td>
<td><span data-ttu-id="4d1fb-134">-inf</span><span class="sxs-lookup"><span data-stu-id="4d1fb-134">-inf</span></span></td>
<td><span data-ttu-id="4d1fb-135">-inf</span><span class="sxs-lookup"><span data-stu-id="4d1fb-135">-inf</span></span></td>
<td><span data-ttu-id="4d1fb-136">-inf</span><span class="sxs-lookup"><span data-stu-id="4d1fb-136">-inf</span></span></td>
<td><span data-ttu-id="4d1fb-137">-inf</span><span class="sxs-lookup"><span data-stu-id="4d1fb-137">-inf</span></span></td>
<td><span data-ttu-id="4d1fb-138">NaN</span><span class="sxs-lookup"><span data-stu-id="4d1fb-138">NaN</span></span></td>
<td><span data-ttu-id="4d1fb-139">NaN</span><span class="sxs-lookup"><span data-stu-id="4d1fb-139">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d1fb-140"><strong>-F</strong></span><span class="sxs-lookup"><span data-stu-id="4d1fb-140"><strong>-F</strong></span></span></td>
<td><span data-ttu-id="4d1fb-141">-inf</span><span class="sxs-lookup"><span data-stu-id="4d1fb-141">-inf</span></span></td>
<td><span data-ttu-id="4d1fb-142">-F</span><span class="sxs-lookup"><span data-stu-id="4d1fb-142">-F</span></span></td>
<td><span data-ttu-id="4d1fb-143">src0</span><span class="sxs-lookup"><span data-stu-id="4d1fb-143">src0</span></span></td>
<td><span data-ttu-id="4d1fb-144">src0</span><span class="sxs-lookup"><span data-stu-id="4d1fb-144">src0</span></span></td>
<td><span data-ttu-id="4d1fb-145">+-F oder +-0</span><span class="sxs-lookup"><span data-stu-id="4d1fb-145">+-F or +-0</span></span></td>
<td><span data-ttu-id="4d1fb-146">+inf</span><span class="sxs-lookup"><span data-stu-id="4d1fb-146">+inf</span></span></td>
<td><span data-ttu-id="4d1fb-147">NaN</span><span class="sxs-lookup"><span data-stu-id="4d1fb-147">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d1fb-148"><strong>-0</strong></span><span class="sxs-lookup"><span data-stu-id="4d1fb-148"><strong>-0</strong></span></span></td>
<td><span data-ttu-id="4d1fb-149">-inf</span><span class="sxs-lookup"><span data-stu-id="4d1fb-149">-inf</span></span></td>
<td><span data-ttu-id="4d1fb-150">src1</span><span class="sxs-lookup"><span data-stu-id="4d1fb-150">src1</span></span></td>
<td><span data-ttu-id="4d1fb-151">-0</span><span class="sxs-lookup"><span data-stu-id="4d1fb-151">-0</span></span></td>
<td><span data-ttu-id="4d1fb-152">+0</span><span class="sxs-lookup"><span data-stu-id="4d1fb-152">+0</span></span></td>
<td><span data-ttu-id="4d1fb-153">src1</span><span class="sxs-lookup"><span data-stu-id="4d1fb-153">src1</span></span></td>
<td><span data-ttu-id="4d1fb-154">+inf</span><span class="sxs-lookup"><span data-stu-id="4d1fb-154">+inf</span></span></td>
<td><span data-ttu-id="4d1fb-155">NaN</span><span class="sxs-lookup"><span data-stu-id="4d1fb-155">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d1fb-156"><strong>+0</strong></span><span class="sxs-lookup"><span data-stu-id="4d1fb-156"><strong>+0</strong></span></span></td>
<td><span data-ttu-id="4d1fb-157">-inf</span><span class="sxs-lookup"><span data-stu-id="4d1fb-157">-inf</span></span></td>
<td><span data-ttu-id="4d1fb-158">src1</span><span class="sxs-lookup"><span data-stu-id="4d1fb-158">src1</span></span></td>
<td><span data-ttu-id="4d1fb-159">+0</span><span class="sxs-lookup"><span data-stu-id="4d1fb-159">+0</span></span></td>
<td><span data-ttu-id="4d1fb-160">+0</span><span class="sxs-lookup"><span data-stu-id="4d1fb-160">+0</span></span></td>
<td><span data-ttu-id="4d1fb-161">src1</span><span class="sxs-lookup"><span data-stu-id="4d1fb-161">src1</span></span></td>
<td><span data-ttu-id="4d1fb-162">+inf</span><span class="sxs-lookup"><span data-stu-id="4d1fb-162">+inf</span></span></td>
<td><span data-ttu-id="4d1fb-163">NaN</span><span class="sxs-lookup"><span data-stu-id="4d1fb-163">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d1fb-164"><strong>+ F</strong></span><span class="sxs-lookup"><span data-stu-id="4d1fb-164"><strong>+F</strong></span></span></td>
<td><span data-ttu-id="4d1fb-165">-inf</span><span class="sxs-lookup"><span data-stu-id="4d1fb-165">-inf</span></span></td>
<td><span data-ttu-id="4d1fb-166">+-F oder +-0</span><span class="sxs-lookup"><span data-stu-id="4d1fb-166">+-F or +-0</span></span></td>
<td><span data-ttu-id="4d1fb-167">src0</span><span class="sxs-lookup"><span data-stu-id="4d1fb-167">src0</span></span></td>
<td><span data-ttu-id="4d1fb-168">src0</span><span class="sxs-lookup"><span data-stu-id="4d1fb-168">src0</span></span></td>
<td><span data-ttu-id="4d1fb-169">+ F</span><span class="sxs-lookup"><span data-stu-id="4d1fb-169">+F</span></span></td>
<td><span data-ttu-id="4d1fb-170">+inf</span><span class="sxs-lookup"><span data-stu-id="4d1fb-170">+inf</span></span></td>
<td><span data-ttu-id="4d1fb-171">NaN</span><span class="sxs-lookup"><span data-stu-id="4d1fb-171">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d1fb-172"><strong>+ INF</strong></span><span class="sxs-lookup"><span data-stu-id="4d1fb-172"><strong>+inf</strong></span></span></td>
<td><span data-ttu-id="4d1fb-173">NaN</span><span class="sxs-lookup"><span data-stu-id="4d1fb-173">NaN</span></span></td>
<td><span data-ttu-id="4d1fb-174">+inf</span><span class="sxs-lookup"><span data-stu-id="4d1fb-174">+inf</span></span></td>
<td><span data-ttu-id="4d1fb-175">+inf</span><span class="sxs-lookup"><span data-stu-id="4d1fb-175">+inf</span></span></td>
<td><span data-ttu-id="4d1fb-176">+inf</span><span class="sxs-lookup"><span data-stu-id="4d1fb-176">+inf</span></span></td>
<td><span data-ttu-id="4d1fb-177">+inf</span><span class="sxs-lookup"><span data-stu-id="4d1fb-177">+inf</span></span></td>
<td><span data-ttu-id="4d1fb-178">+inf</span><span class="sxs-lookup"><span data-stu-id="4d1fb-178">+inf</span></span></td>
<td><span data-ttu-id="4d1fb-179">NaN</span><span class="sxs-lookup"><span data-stu-id="4d1fb-179">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d1fb-180"><strong>NaN</strong></span><span class="sxs-lookup"><span data-stu-id="4d1fb-180"><strong>NaN</strong></span></span></td>
<td><span data-ttu-id="4d1fb-181">NaN</span><span class="sxs-lookup"><span data-stu-id="4d1fb-181">NaN</span></span></td>
<td><span data-ttu-id="4d1fb-182">NaN</span><span class="sxs-lookup"><span data-stu-id="4d1fb-182">NaN</span></span></td>
<td><span data-ttu-id="4d1fb-183">NaN</span><span class="sxs-lookup"><span data-stu-id="4d1fb-183">NaN</span></span></td>
<td><span data-ttu-id="4d1fb-184">NaN</span><span class="sxs-lookup"><span data-stu-id="4d1fb-184">NaN</span></span></td>
<td><span data-ttu-id="4d1fb-185">NaN</span><span class="sxs-lookup"><span data-stu-id="4d1fb-185">NaN</span></span></td>
<td><span data-ttu-id="4d1fb-186">NaN</span><span class="sxs-lookup"><span data-stu-id="4d1fb-186">NaN</span></span></td>
<td><span data-ttu-id="4d1fb-187">NaN</span><span class="sxs-lookup"><span data-stu-id="4d1fb-187">NaN</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4d1fb-188">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="4d1fb-188">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4d1fb-189">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="4d1fb-189">Vertex</span></span> | <span data-ttu-id="4d1fb-190">Hülle</span><span class="sxs-lookup"><span data-stu-id="4d1fb-190">Hull</span></span> | <span data-ttu-id="4d1fb-191">Domain</span><span class="sxs-lookup"><span data-stu-id="4d1fb-191">Domain</span></span> | <span data-ttu-id="4d1fb-192">Geometrie</span><span class="sxs-lookup"><span data-stu-id="4d1fb-192">Geometry</span></span> | <span data-ttu-id="4d1fb-193">Pixel</span><span class="sxs-lookup"><span data-stu-id="4d1fb-193">Pixel</span></span> | <span data-ttu-id="4d1fb-194">Compute</span><span class="sxs-lookup"><span data-stu-id="4d1fb-194">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4d1fb-195">X</span><span class="sxs-lookup"><span data-stu-id="4d1fb-195">X</span></span>      | <span data-ttu-id="4d1fb-196">X</span><span class="sxs-lookup"><span data-stu-id="4d1fb-196">X</span></span>    | <span data-ttu-id="4d1fb-197">X</span><span class="sxs-lookup"><span data-stu-id="4d1fb-197">X</span></span>      | <span data-ttu-id="4d1fb-198">X</span><span class="sxs-lookup"><span data-stu-id="4d1fb-198">X</span></span>        | <span data-ttu-id="4d1fb-199">X</span><span class="sxs-lookup"><span data-stu-id="4d1fb-199">X</span></span>     | <span data-ttu-id="4d1fb-200">X</span><span class="sxs-lookup"><span data-stu-id="4d1fb-200">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4d1fb-201">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="4d1fb-201">Minimum Shader Model</span></span>

<span data-ttu-id="4d1fb-202">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="4d1fb-202">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4d1fb-203">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="4d1fb-203">Shader Model</span></span>                                              | <span data-ttu-id="4d1fb-204">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="4d1fb-204">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4d1fb-205">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="4d1fb-205">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4d1fb-206">ja</span><span class="sxs-lookup"><span data-stu-id="4d1fb-206">yes</span></span>       |
| [<span data-ttu-id="4d1fb-207">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="4d1fb-207">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4d1fb-208">nein</span><span class="sxs-lookup"><span data-stu-id="4d1fb-208">no</span></span>        |
| [<span data-ttu-id="4d1fb-209">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="4d1fb-209">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4d1fb-210">nein</span><span class="sxs-lookup"><span data-stu-id="4d1fb-210">no</span></span>        |
| [<span data-ttu-id="4d1fb-211">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d1fb-211">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4d1fb-212">nein</span><span class="sxs-lookup"><span data-stu-id="4d1fb-212">no</span></span>        |
| [<span data-ttu-id="4d1fb-213">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d1fb-213">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4d1fb-214">nein</span><span class="sxs-lookup"><span data-stu-id="4d1fb-214">no</span></span>        |
| [<span data-ttu-id="4d1fb-215">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d1fb-215">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4d1fb-216">nein</span><span class="sxs-lookup"><span data-stu-id="4d1fb-216">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4d1fb-217">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d1fb-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d1fb-218">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d1fb-218">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





