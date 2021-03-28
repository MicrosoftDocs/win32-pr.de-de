---
title: Shader Model 4-Assembly
description: Shader Model 4-Assembly
ms.assetid: 2896e195-b48b-4ce9-9421-f5fa40674b5e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20c7ff5d2a171228223d52db28d3bae6007068c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036999"
---
# <a name="shader-model-4-assembly"></a><span data-ttu-id="f9318-103">Shader Model 4-Assembly</span><span class="sxs-lookup"><span data-stu-id="f9318-103">Shader Model 4 Assembly</span></span>

<span data-ttu-id="f9318-104">Shadermodell 4 erfordert, dass Sie Shader in HLSL programmieren.</span><span class="sxs-lookup"><span data-stu-id="f9318-104">Shader Model 4 requires you to program shaders in HLSL.</span></span> <span data-ttu-id="f9318-105">Der Shader-Compiler kompiliert den HLSL-Code jedoch in eine Assembly, die auf dem Gerät ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9318-105">However, the shader compiler compiles the HLSL code into assembly that runs on the device.</span></span> <span data-ttu-id="f9318-106">Wenn Sie pix für Windows verwenden, um die Shader zu debuggen, können Sie den Shader-Code entweder in HLSL oder in der Assembly anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f9318-106">If you are using PIX for Windows to debug your shaders, you can choose to display shader code in either HLSL or assembly.</span></span> <span data-ttu-id="f9318-107">In diesem Abschnitt werden die Assemblyanweisungen Shader Model 4 und Shader Model 4,1 aufgelistet, die beim Debuggen eines Shaders auftreten können.</span><span class="sxs-lookup"><span data-stu-id="f9318-107">This section lists the Shader Model 4 and Shader Model 4.1 assembly instructions that you may encounter when debugging a shader.</span></span>

<dl>

[<span data-ttu-id="f9318-108">Anweisungs Modifizierer</span><span class="sxs-lookup"><span data-stu-id="f9318-108">Instruction Modifiers</span></span>](instruction-modifiers.md)  
[<span data-ttu-id="f9318-109">add</span><span class="sxs-lookup"><span data-stu-id="f9318-109">add</span></span>](add--sm4---asm-.md)  
[<span data-ttu-id="f9318-110">and</span><span class="sxs-lookup"><span data-stu-id="f9318-110">and</span></span>](and--sm4---asm-.md)  
[<span data-ttu-id="f9318-111">break</span><span class="sxs-lookup"><span data-stu-id="f9318-111">break</span></span>](break--sm4---asm-.md)  
[<span data-ttu-id="f9318-112">breakc</span><span class="sxs-lookup"><span data-stu-id="f9318-112">breakc</span></span>](breakc--sm4---asm-.md)  
[<span data-ttu-id="f9318-113">call</span><span class="sxs-lookup"><span data-stu-id="f9318-113">call</span></span>](call--sm4---asm-.md)  
[<span data-ttu-id="f9318-114">callc</span><span class="sxs-lookup"><span data-stu-id="f9318-114">callc</span></span>](callc--sm4---asm-.md)  
[<span data-ttu-id="f9318-115">case</span><span class="sxs-lookup"><span data-stu-id="f9318-115">case</span></span>](case--sm4---asm-.md)  
[<span data-ttu-id="f9318-116">continue</span><span class="sxs-lookup"><span data-stu-id="f9318-116">continue</span></span>](continue--sm4---asm-.md)  
[<span data-ttu-id="f9318-117">continuec</span><span class="sxs-lookup"><span data-stu-id="f9318-117">continuec</span></span>](continuec--sm4---asm-.md)  
[<span data-ttu-id="f9318-118">Schnitts</span><span class="sxs-lookup"><span data-stu-id="f9318-118">cut</span></span>](cut--sm4---asm-.md)  
[<span data-ttu-id="f9318-119">DCL \_ constantbuffer</span><span class="sxs-lookup"><span data-stu-id="f9318-119">dcl\_constantBuffer</span></span>](dcl-constantbuffer.md)  
[<span data-ttu-id="f9318-120">DCL \_ globalflags</span><span class="sxs-lookup"><span data-stu-id="f9318-120">dcl\_globalFlags</span></span>](dcl-globalflags.md)  
[<span data-ttu-id="f9318-121">DCL \_ unmittelateconstantbuffer</span><span class="sxs-lookup"><span data-stu-id="f9318-121">dcl\_immediateConstantBuffer</span></span>](dcl-immediateconstantbuffer.md)  
[<span data-ttu-id="f9318-122">DCL- \_ indexabletemp</span><span class="sxs-lookup"><span data-stu-id="f9318-122">dcl\_indexableTemp</span></span>](dcl-indexabletemp.md)  
[<span data-ttu-id="f9318-123">DCL- \_ Indexbereich</span><span class="sxs-lookup"><span data-stu-id="f9318-123">dcl\_indexRange</span></span>](dcl-indexrange.md)  
[<span data-ttu-id="f9318-124">DCL- \_ Eingabe</span><span class="sxs-lookup"><span data-stu-id="f9318-124">dcl\_input</span></span>](dcl-input.md)  
[<span data-ttu-id="f9318-125">DCL- \_ Eingabe \_ SV</span><span class="sxs-lookup"><span data-stu-id="f9318-125">dcl\_input\_sv</span></span>](dcl-input-sv.md)  
[<span data-ttu-id="f9318-126">DCL- \_ Eingabe vprim</span><span class="sxs-lookup"><span data-stu-id="f9318-126">dcl\_input vPrim</span></span>](dcl-input-vprim.md)  
[<span data-ttu-id="f9318-127">DCL \_ maxoutputvertexcount</span><span class="sxs-lookup"><span data-stu-id="f9318-127">dcl\_maxOutputVertexCount</span></span>](dcl-maxoutputvertexcount.md)  
[<span data-ttu-id="f9318-128">DCL- \_ Ausgabe</span><span class="sxs-lookup"><span data-stu-id="f9318-128">dcl\_output</span></span>](dcl-output.md)  
[<span data-ttu-id="f9318-129">DCL- \_ Ausgabe- \_ otiefe</span><span class="sxs-lookup"><span data-stu-id="f9318-129">dcl\_output\_oDepth</span></span>](dcl-output-odepth.md)  
[<span data-ttu-id="f9318-130">DCL- \_ Ausgabe ( \_ Scalable)</span><span class="sxs-lookup"><span data-stu-id="f9318-130">dcl\_output\_sgv</span></span>](dcl-output-sgv.md)  
[<span data-ttu-id="f9318-131">DCL- \_ Ausgabe ( \_ SIV)</span><span class="sxs-lookup"><span data-stu-id="f9318-131">dcl\_output\_siv</span></span>](dcl-output-siv.md)  
[<span data-ttu-id="f9318-132">DCL- \_ outputtopology</span><span class="sxs-lookup"><span data-stu-id="f9318-132">dcl\_outputTopology</span></span>](dcl-outputtopology.md)  
[<span data-ttu-id="f9318-133">DCL- \_ Ressource</span><span class="sxs-lookup"><span data-stu-id="f9318-133">dcl\_resource</span></span>](dcl-resource.md)  
[<span data-ttu-id="f9318-134">DCL- \_ Sampler</span><span class="sxs-lookup"><span data-stu-id="f9318-134">dcl\_sampler</span></span>](dcl-sampler.md)  
[<span data-ttu-id="f9318-135">DCL- \_ Temps</span><span class="sxs-lookup"><span data-stu-id="f9318-135">dcl\_temps</span></span>](dcl-temps.md)  
[<span data-ttu-id="f9318-136">default</span><span class="sxs-lookup"><span data-stu-id="f9318-136">default</span></span>](default--sm4---asm-.md)  
[<span data-ttu-id="f9318-137">DERIV \_ RTX</span><span class="sxs-lookup"><span data-stu-id="f9318-137">deriv\_rtx</span></span>](deriv-rtx--sm4---asm-.md)  
[<span data-ttu-id="f9318-138">DERIV- \_ Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f9318-138">deriv\_rty</span></span>](deriv-rty--sm4---asm-.md)  
[<span data-ttu-id="f9318-139">Würfen</span><span class="sxs-lookup"><span data-stu-id="f9318-139">discard</span></span>](discard--sm4---asm-.md)  
[<span data-ttu-id="f9318-140">div</span><span class="sxs-lookup"><span data-stu-id="f9318-140">div</span></span>](div--sm4---asm-.md)  
[<span data-ttu-id="f9318-141">DP2</span><span class="sxs-lookup"><span data-stu-id="f9318-141">dp2</span></span>](dp2--sm4---asm-.md)  
[<span data-ttu-id="f9318-142">dp3</span><span class="sxs-lookup"><span data-stu-id="f9318-142">dp3</span></span>](dp3--sm4---asm-.md)  
[<span data-ttu-id="f9318-143">dp4</span><span class="sxs-lookup"><span data-stu-id="f9318-143">dp4</span></span>](dp4--sm4---asm-.md)  
[<span data-ttu-id="f9318-144">else</span><span class="sxs-lookup"><span data-stu-id="f9318-144">else</span></span>](else--sm4---asm-.md)  
[<span data-ttu-id="f9318-145">ausgeben</span><span class="sxs-lookup"><span data-stu-id="f9318-145">emit</span></span>](emit--sm4---asm-.md)  
[<span data-ttu-id="f9318-146">emitthencut</span><span class="sxs-lookup"><span data-stu-id="f9318-146">emitThenCut</span></span>](emitthencut--sm4---asm-.md)  
[<span data-ttu-id="f9318-147">endif</span><span class="sxs-lookup"><span data-stu-id="f9318-147">endif</span></span>](endif--sm4---asm-.md)  
[<span data-ttu-id="f9318-148">ENDLOOP</span><span class="sxs-lookup"><span data-stu-id="f9318-148">endloop</span></span>](endloop--sm4---asm-.md)  
[<span data-ttu-id="f9318-149">Endswitch</span><span class="sxs-lookup"><span data-stu-id="f9318-149">endswitch</span></span>](endswitch--sm4---asm-.md)  
[<span data-ttu-id="f9318-150">eq</span><span class="sxs-lookup"><span data-stu-id="f9318-150">eq</span></span>](eq--sm4---asm-.md)  
[<span data-ttu-id="f9318-151">exp</span><span class="sxs-lookup"><span data-stu-id="f9318-151">exp</span></span>](exp--sm4---asm-.md)  
[<span data-ttu-id="f9318-152">FRC</span><span class="sxs-lookup"><span data-stu-id="f9318-152">frc</span></span>](frc--sm4---asm-.md)  
[<span data-ttu-id="f9318-153">der Befehl</span><span class="sxs-lookup"><span data-stu-id="f9318-153">ftoi</span></span>](ftoi--sm4---asm-.md)  
[<span data-ttu-id="f9318-154">ftou</span><span class="sxs-lookup"><span data-stu-id="f9318-154">ftou</span></span>](ftou--sm4---asm-.md)  
[<span data-ttu-id="f9318-155">ge</span><span class="sxs-lookup"><span data-stu-id="f9318-155">ge</span></span>](ge--sm4---asm-.md)  
[<span data-ttu-id="f9318-156">IAdd</span><span class="sxs-lookup"><span data-stu-id="f9318-156">iadd</span></span>](iadd--sm4---asm-.md)  
[<span data-ttu-id="f9318-157">ibfe</span><span class="sxs-lookup"><span data-stu-id="f9318-157">ibfe</span></span>](dne--sm5---asm-.md)  
[<span data-ttu-id="f9318-158">IEQ</span><span class="sxs-lookup"><span data-stu-id="f9318-158">ieq</span></span>](ieq--sm4---asm-.md)  
[<span data-ttu-id="f9318-159">if</span><span class="sxs-lookup"><span data-stu-id="f9318-159">if</span></span>](if--sm4---asm-.md)  
[<span data-ttu-id="f9318-160">ige</span><span class="sxs-lookup"><span data-stu-id="f9318-160">ige</span></span>](ige--sm4---asm-.md)  
[<span data-ttu-id="f9318-161">ILT</span><span class="sxs-lookup"><span data-stu-id="f9318-161">ilt</span></span>](ilt--sm4---asm-.md)  
[<span data-ttu-id="f9318-162">Imad</span><span class="sxs-lookup"><span data-stu-id="f9318-162">imad</span></span>](imad--sm4---asm-.md)  
[<span data-ttu-id="f9318-163">Imin</span><span class="sxs-lookup"><span data-stu-id="f9318-163">imin</span></span>](imin--sm4---asm-.md)  
[<span data-ttu-id="f9318-164">imul</span><span class="sxs-lookup"><span data-stu-id="f9318-164">imul</span></span>](imul--sm4---asm-.md)  
[<span data-ttu-id="f9318-165">Bina</span><span class="sxs-lookup"><span data-stu-id="f9318-165">ine</span></span>](ine--sm4---asm-.md)  
[<span data-ttu-id="f9318-166">InEG</span><span class="sxs-lookup"><span data-stu-id="f9318-166">ineg</span></span>](ineg--sm4---asm-.md)  
[<span data-ttu-id="f9318-167">ishl</span><span class="sxs-lookup"><span data-stu-id="f9318-167">ishl</span></span>](ishl--sm4---asm-.md)  
[<span data-ttu-id="f9318-168">ISHR</span><span class="sxs-lookup"><span data-stu-id="f9318-168">ishr</span></span>](ishr--sm4---asm-.md)  
[<span data-ttu-id="f9318-169">itof</span><span class="sxs-lookup"><span data-stu-id="f9318-169">itof</span></span>](itof--sm4---asm-.md)  
[<span data-ttu-id="f9318-170">label</span><span class="sxs-lookup"><span data-stu-id="f9318-170">label</span></span>](label--sm4---asm-.md)  
[<span data-ttu-id="f9318-171">Teufels</span><span class="sxs-lookup"><span data-stu-id="f9318-171">ld</span></span>](ld--sm4---asm-.md)  
[<span data-ttu-id="f9318-172">angezeigt</span><span class="sxs-lookup"><span data-stu-id="f9318-172">log</span></span>](log--sm4---asm-.md)  
[<span data-ttu-id="f9318-173">loop</span><span class="sxs-lookup"><span data-stu-id="f9318-173">loop</span></span>](loop--sm4---asm-.md)  
[<span data-ttu-id="f9318-174">lt</span><span class="sxs-lookup"><span data-stu-id="f9318-174">lt</span></span>](lt--sm4---asm-.md)  
[<span data-ttu-id="f9318-175">geworden</span><span class="sxs-lookup"><span data-stu-id="f9318-175">mad</span></span>](mad--sm4---asm-.md)  
[<span data-ttu-id="f9318-176">max</span><span class="sxs-lookup"><span data-stu-id="f9318-176">max</span></span>](max--sm4---asm-.md)  
[<span data-ttu-id="f9318-177">min</span><span class="sxs-lookup"><span data-stu-id="f9318-177">min</span></span>](min--sm4---asm-.md)  
[<span data-ttu-id="f9318-178">MOV</span><span class="sxs-lookup"><span data-stu-id="f9318-178">mov</span></span>](mov--sm4---asm-.md)  
[<span data-ttu-id="f9318-179">"muvc"</span><span class="sxs-lookup"><span data-stu-id="f9318-179">movc</span></span>](movc--sm4---asm-.md)  
[<span data-ttu-id="f9318-180">mul</span><span class="sxs-lookup"><span data-stu-id="f9318-180">mul</span></span>](mul--sm4---asm-.md)  
[<span data-ttu-id="f9318-181">ne</span><span class="sxs-lookup"><span data-stu-id="f9318-181">ne</span></span>](ne--sm4---asm-.md)  
[<span data-ttu-id="f9318-182">NOP</span><span class="sxs-lookup"><span data-stu-id="f9318-182">nop</span></span>](nop--sm4---asm-.md)  
[<span data-ttu-id="f9318-183">not</span><span class="sxs-lookup"><span data-stu-id="f9318-183">not</span></span>](not--sm4---asm-.md)  
[<span data-ttu-id="f9318-184">or</span><span class="sxs-lookup"><span data-stu-id="f9318-184">or</span></span>](or--sm4---asm-.md)  
[<span data-ttu-id="f9318-185">ResInfo</span><span class="sxs-lookup"><span data-stu-id="f9318-185">resinfo</span></span>](resinfo--sm4---asm-.md)  
[<span data-ttu-id="f9318-186">TZI</span><span class="sxs-lookup"><span data-stu-id="f9318-186">ret</span></span>](ret--sm4---asm-.md)  
[<span data-ttu-id="f9318-187">RETC</span><span class="sxs-lookup"><span data-stu-id="f9318-187">retc</span></span>](retc--sm4---asm-.md)  
[<span data-ttu-id="f9318-188">\_roundne</span><span class="sxs-lookup"><span data-stu-id="f9318-188">round\_ne</span></span>](round-ne--sm4---asm-.md)  
[<span data-ttu-id="f9318-189">Round- \_ NI</span><span class="sxs-lookup"><span data-stu-id="f9318-189">round\_ni</span></span>](round-ni--sm4---asm-.md)  
[<span data-ttu-id="f9318-190">Round \_ Pi</span><span class="sxs-lookup"><span data-stu-id="f9318-190">round\_pi</span></span>](round-pi--sm4---asm-.md)  
[<span data-ttu-id="f9318-191">Round \_ z</span><span class="sxs-lookup"><span data-stu-id="f9318-191">round\_z</span></span>](round-z--sm4---asm-.md)  
[<span data-ttu-id="f9318-192">RSQ</span><span class="sxs-lookup"><span data-stu-id="f9318-192">rsq</span></span>](rsq--sm4---asm-.md)  
[<span data-ttu-id="f9318-193">Blutprobe</span><span class="sxs-lookup"><span data-stu-id="f9318-193">sample</span></span>](sample--sm4---asm-.md)  
[<span data-ttu-id="f9318-194">Beispiel \_ b</span><span class="sxs-lookup"><span data-stu-id="f9318-194">sample\_b</span></span>](sample-b--sm4---asm-.md)  
[<span data-ttu-id="f9318-195">Beispiel \_ c</span><span class="sxs-lookup"><span data-stu-id="f9318-195">sample\_c</span></span>](sample-c--sm4---asm-.md)  
[<span data-ttu-id="f9318-196">Beispiel- \_ c- \_ LZ</span><span class="sxs-lookup"><span data-stu-id="f9318-196">sample\_c\_lz</span></span>](sample-c-lz--sm4---asm-.md)  
[<span data-ttu-id="f9318-197">Beispiel \_ d</span><span class="sxs-lookup"><span data-stu-id="f9318-197">sample\_d</span></span>](sample-d--sm4---asm-.md)  
[<span data-ttu-id="f9318-198">Beispiel \_ l</span><span class="sxs-lookup"><span data-stu-id="f9318-198">sample\_l</span></span>](sample-l--sm4---asm-.md)  
[<span data-ttu-id="f9318-199">SinCos</span><span class="sxs-lookup"><span data-stu-id="f9318-199">sincos</span></span>](sincos--sm4---asm-.md)  
[<span data-ttu-id="f9318-200">SQRT</span><span class="sxs-lookup"><span data-stu-id="f9318-200">sqrt</span></span>](sqrt--sm4---asm-.md)  
[<span data-ttu-id="f9318-201">switch</span><span class="sxs-lookup"><span data-stu-id="f9318-201">switch</span></span>](switch--sm4---asm-.md)  
[<span data-ttu-id="f9318-202">udiv</span><span class="sxs-lookup"><span data-stu-id="f9318-202">udiv</span></span>](udiv--sm4---asm-.md)  
[<span data-ttu-id="f9318-203">UGE</span><span class="sxs-lookup"><span data-stu-id="f9318-203">uge</span></span>](uge--sm4---asm-.md)  
[<span data-ttu-id="f9318-204">ULT</span><span class="sxs-lookup"><span data-stu-id="f9318-204">ult</span></span>](ult--sm4---asm-.md)  
[<span data-ttu-id="f9318-205">Umad</span><span class="sxs-lookup"><span data-stu-id="f9318-205">umad</span></span>](umad--sm4---asm-.md)  
[<span data-ttu-id="f9318-206">Umax</span><span class="sxs-lookup"><span data-stu-id="f9318-206">umax</span></span>](umax--sm4---asm-.md)  
[<span data-ttu-id="f9318-207">-in</span><span class="sxs-lookup"><span data-stu-id="f9318-207">umin</span></span>](umin--sm4---asm-.md)  
[<span data-ttu-id="f9318-208">Umul</span><span class="sxs-lookup"><span data-stu-id="f9318-208">umul</span></span>](umul--sm4---asm-.md)  
[<span data-ttu-id="f9318-209">"ushr"</span><span class="sxs-lookup"><span data-stu-id="f9318-209">ushr</span></span>](ushr--sm4---asm-.md)  
[<span data-ttu-id="f9318-210">utof</span><span class="sxs-lookup"><span data-stu-id="f9318-210">utof</span></span>](utof--sm4---asm-.md)  
[<span data-ttu-id="f9318-211">xor</span><span class="sxs-lookup"><span data-stu-id="f9318-211">xor</span></span>](xor--sm4---asm-.md)  
</dl>

## <a name="shader-model-41-assembly"></a><span data-ttu-id="f9318-212">Shader-Modell 4,1-Assembly</span><span class="sxs-lookup"><span data-stu-id="f9318-212">Shader Model 4.1 Assembly</span></span>

<span data-ttu-id="f9318-213">Shader-Modell 4,1 unterstützt alle Shadermodell-4,0-Anweisungen und die folgenden zusätzlichen Anweisungen:</span><span class="sxs-lookup"><span data-stu-id="f9318-213">Shader Model 4.1 supports all of the Shader Model 4.0 instructions and the following additional instructions:</span></span>

<dl>

[<span data-ttu-id="f9318-214">gather4</span><span class="sxs-lookup"><span data-stu-id="f9318-214">gather4</span></span>](gather4--sm4-1---asm-.md)  
[<span data-ttu-id="f9318-215">ld2dms</span><span class="sxs-lookup"><span data-stu-id="f9318-215">ld2dms</span></span>](ld2dms--sm4-1---asm-.md)  
[<span data-ttu-id="f9318-216">LOD</span><span class="sxs-lookup"><span data-stu-id="f9318-216">lod</span></span>](lod--sm4-1---asm-.md)  
[<span data-ttu-id="f9318-217">sampleingefo</span><span class="sxs-lookup"><span data-stu-id="f9318-217">sampleinfo</span></span>](sampleinfo--sm4-1---asm-.md)  
[<span data-ttu-id="f9318-218">samplepos</span><span class="sxs-lookup"><span data-stu-id="f9318-218">samplepos</span></span>](samplepos--sm4-1---asm-.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="f9318-219">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9318-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9318-220">ASM-Shader-Referenz</span><span class="sxs-lookup"><span data-stu-id="f9318-220">Asm Shader Reference</span></span>](dx9-graphics-reference-asm.md)
</dt> <dt>

[<span data-ttu-id="f9318-221">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="f9318-221">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




