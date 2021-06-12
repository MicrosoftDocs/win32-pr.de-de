---
title: vs_3_0
description: Erfahren Sie mehr über vs_3_0, einen programmierbaren Vertex-Shader, der aus einer Reihe von Anweisungen besteht, die mit Scheitelpunktdaten arbeiten.
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 310d64170280053c34766f214969f78d66560ea3
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011073"
---
# <a name="vs_3_0"></a><span data-ttu-id="f917a-103">Vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f917a-103">vs\_3\_0</span></span>

<span data-ttu-id="f917a-104">Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die für Scheitelpunktdaten ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f917a-104">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="f917a-105">Registriert Datenübertragungen in und aus der ALU.</span><span class="sxs-lookup"><span data-stu-id="f917a-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="f917a-106">Es kann ein zusätzliches Steuerelement angewendet werden, um die Anweisung, die Ergebnisse oder die geschriebenen Daten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f917a-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="f917a-107">Die Vertex-Shaderversion im Vergleich \_ zu 3 \_ 0 erweitert den Featuresatz, der von und 2 x unterstützt \_ \_ wird.</span><span class="sxs-lookup"><span data-stu-id="f917a-107">Vertex shader version vs\_3\_0 extends the feature set supported by vs\_2\_x.</span></span> <span data-ttu-id="f917a-108">Jedes der Features in vs \_ 2 \_ X, für die eine Obergrenze festgelegt werden muss, ist in \_ Vs. 3 \_ 0 verfügbar, ohne dass die Obergrenze erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f917a-108">Each of the features in vs\_2\_X that requires a cap to be set, is available in vs\_3\_0 without requiring the cap.</span></span>

-   <span data-ttu-id="f917a-109">[Anweisungen im Vergleich zu \_ 3 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) enthält eine Liste der verfügbaren Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="f917a-109">[Instructions - vs\_3\_0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="f917a-110">[Register : Im Vergleich zu \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) werden die verschiedenen Registertypen aufgelistet, die von der Vertex-Shader-ALU verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f917a-110">[Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="f917a-111">[Vertex-Shaderregistermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers.md) werden verwendet, um die Funktionsweise einer Anweisung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f917a-111">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="f917a-112">[Vertex-Shader-Quellregistermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) ändern die Quellregisterdaten, bevor die Anweisung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f917a-112">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="f917a-113">[Das Quellenregister swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) bietet zusätzliche Kontrolle darüber, welche Registerkomponenten gelesen, kopiert oder geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f917a-113">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="f917a-114">[Die Zielregistermaskierung](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) bestimmt, welche Komponenten des Zielregisters geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f917a-114">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="f917a-115">Neue Funktionen</span><span class="sxs-lookup"><span data-stu-id="f917a-115">New Features</span></span>

<span data-ttu-id="f917a-116">Neue Features der Vertex-Shaderversion im Vergleich zu \_ Version \_ 3 0 sind in den folgenden Abschnitten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f917a-116">New features of vertex shader version vs\_3\_0 are listed in the following sections.</span></span>

### <a name="indexing-registers"></a><span data-ttu-id="f917a-117">Indizierungsregister</span><span class="sxs-lookup"><span data-stu-id="f917a-117">Indexing Registers</span></span>

<span data-ttu-id="f917a-118">In den früheren Shadermodellen konnte nur die konstante Registerbank indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f917a-118">In the earlier shader models, only the constant register bank could be indexed.</span></span> <span data-ttu-id="f917a-119">In diesem Modell können die folgenden Registerbanken mithilfe des Schleifenzählerregisters (Loop Counter Register, aL) indiziert werden:</span><span class="sxs-lookup"><span data-stu-id="f917a-119">In this model, the following register banks can be indexed, using the loop counter register (aL):</span></span>

-   <span data-ttu-id="f917a-120">Eingaberegister (v \# )</span><span class="sxs-lookup"><span data-stu-id="f917a-120">Input register (v\#)</span></span>
-   <span data-ttu-id="f917a-121">Ausgaberegister (o \# )</span><span class="sxs-lookup"><span data-stu-id="f917a-121">Output register (o\#)</span></span>

### <a name="vertex-textures"></a><span data-ttu-id="f917a-122">Scheitelpunkttexturen</span><span class="sxs-lookup"><span data-stu-id="f917a-122">Vertex Textures</span></span>

<span data-ttu-id="f917a-123">Dieses Shadermodell unterstützt die Textursuche im Vertex-Shader mithilfe von Texldl.</span><span class="sxs-lookup"><span data-stu-id="f917a-123">This shader model supports texture lookup in the vertex shader using texldl.</span></span> <span data-ttu-id="f917a-124">Die Vertex-Engine verfügt über vier Textur-Samplerstufen (die sich von der Verschiebungszuordnungs-Sampler und den Textur-Samplern in der Pixel-Engine unterscheiden), die zum Abtasten von Texturen verwendet werden können, die in diesen Phasen festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="f917a-124">The vertex engine has four texture sampler stages (distinct from the displacement map sampler and the texture samplers in the pixel engine) that can be used to sample textures set at those stages.</span></span> <span data-ttu-id="f917a-125">Siehe [Vertextexturen in vs \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).</span><span class="sxs-lookup"><span data-stu-id="f917a-125">See [Vertex Textures in vs\_3\_0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).</span></span>

### <a name="vertex-stream-frequency"></a><span data-ttu-id="f917a-126">Vertexstreamfrequenz</span><span class="sxs-lookup"><span data-stu-id="f917a-126">Vertex Stream Frequency</span></span>

<span data-ttu-id="f917a-127">Mit diesem Feature kann eine Teilmenge der Eingaberegister mit einer anderen Rate als einmal pro Scheitelpunkt initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f917a-127">This feature allows a subset of the input registers to be initialized at a rate different from once per vertex.</span></span> <span data-ttu-id="f917a-128">Weitere Informationen finden Sie unter [Zeichnen einer nicht indizierten Geometrie.](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry)</span><span class="sxs-lookup"><span data-stu-id="f917a-128">See [Drawing Non-Indexed Geometry](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).</span></span>

### <a name="shader-output"></a><span data-ttu-id="f917a-129">Shaderausgabe</span><span class="sxs-lookup"><span data-stu-id="f917a-129">Shader Output</span></span>

<span data-ttu-id="f917a-130">Ähnlich wie bei \_ 2 \_ 0 kann die Ausgabe des Shaders mit der statischen Flusssteuerung variieren.</span><span class="sxs-lookup"><span data-stu-id="f917a-130">Similar to vs\_2\_0, the output of the shader can vary with static flow control.</span></span> <span data-ttu-id="f917a-131">Seien Sie vorsichtig bei der dynamischen Verzweigung, da dies dazu führen kann, dass shader-Ausgaben pro Scheitelpunkt variieren.</span><span class="sxs-lookup"><span data-stu-id="f917a-131">Be careful with dynamic branching as this can cause shader outputs to vary per vertex.</span></span> <span data-ttu-id="f917a-132">Dies führt zu unvorhersehbaren Ergebnissen auf unterschiedlichen Hardwarekomponenten.</span><span class="sxs-lookup"><span data-stu-id="f917a-132">This will produce unpredictable results on different hardware.</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="f917a-133">Dynamische Flusssteuerung</span><span class="sxs-lookup"><span data-stu-id="f917a-133">Dynamic flow control</span></span>

<span data-ttu-id="f917a-134">Alle Anweisungen zur dynamischen Flusssteuerung werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f917a-134">All dynamic flow control instructions are supported.</span></span> <span data-ttu-id="f917a-135">Der maximal zulässige Schachtelungstiefewert ist 24.</span><span class="sxs-lookup"><span data-stu-id="f917a-135">The maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="f917a-136">(Weitere Informationen finden Sie unter [Schachtelungsgrenzwerte](dx9-graphics-reference-asm-vs-instructions-flow-control.md) für die Flusssteuerung.)</span><span class="sxs-lookup"><span data-stu-id="f917a-136">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="temporary-registers"></a><span data-ttu-id="f917a-137">Temporäre Register</span><span class="sxs-lookup"><span data-stu-id="f917a-137">Temporary Registers</span></span>

<span data-ttu-id="f917a-138">Insgesamt werden 32 temporäre Register \# (r) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f917a-138">A total of 32 temporary registers (r\#) is supported.</span></span>

### <a name="static-flow-control"></a><span data-ttu-id="f917a-139">Statische Flusssteuerung</span><span class="sxs-lookup"><span data-stu-id="f917a-139">Static Flow Control</span></span>

<span data-ttu-id="f917a-140">Die maximale Schachtelungstiefe für [die Schleife – im Vergleich zu](loop---vs.md)rep – im Vergleich / [zu](rep---vs.md) 4.</span><span class="sxs-lookup"><span data-stu-id="f917a-140">The maximum nesting depth for [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) is 4.</span></span> <span data-ttu-id="f917a-141">Die maximale Schachtelungstiefe für [call - vs](call---vs.md) / [callnz bool - vs](callnz-bool---vs.md) / [callnz pred - vs](callnz-pred---vs.md) ist 4.</span><span class="sxs-lookup"><span data-stu-id="f917a-141">The maximum nesting depth for [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[callnz pred - vs](callnz-pred---vs.md) is 4.</span></span> <span data-ttu-id="f917a-142">Bei [bool – im Vergleich](if-bool---vs.md)zu – ist der maximal zulässige Schachtelungstiefewert 24.</span><span class="sxs-lookup"><span data-stu-id="f917a-142">For [if bool - vs](if-bool---vs.md), the maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="f917a-143">(Weitere Informationen finden Sie unter [Schachtelungsgrenzwerte](dx9-graphics-reference-asm-vs-instructions-flow-control.md) für die Flusssteuerung.)</span><span class="sxs-lookup"><span data-stu-id="f917a-143">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="predication"></a><span data-ttu-id="f917a-144">Prädikation</span><span class="sxs-lookup"><span data-stu-id="f917a-144">Predication</span></span>

<span data-ttu-id="f917a-145">Anweisungsprädikation wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f917a-145">Instruction predication is supported.</span></span> <span data-ttu-id="f917a-146">Verwenden Sie [setp \_ comp - vs](setp-comp---vs.md) , um das Prädikatregister festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f917a-146">Use [setp\_comp - vs](setp-comp---vs.md) to set the predicate register.</span></span>

### <a name="instruction-count"></a><span data-ttu-id="f917a-147">Anweisungsanzahl</span><span class="sxs-lookup"><span data-stu-id="f917a-147">Instruction Count</span></span>

<span data-ttu-id="f917a-148">Jeder Vertexshader ist überall von 512 bis zur Anzahl der Slots in MaxVertexShader30InstructionSlots in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)zulässig.</span><span class="sxs-lookup"><span data-stu-id="f917a-148">Each vertex shader is allowed anywhere from 512 up to the number of slots in MaxVertexShader30InstructionSlots in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span></span> <span data-ttu-id="f917a-149">Die Anzahl der ausgeführten Anweisungen kann aufgrund der Schleifen-/Rep-Unterstützung deutlich höher sein. Dies ist jedoch durch MaxVShaderInstructionsExecuted in D3DCAPS9 begrenzt, das mindestens 0xFFFF sein sollte.</span><span class="sxs-lookup"><span data-stu-id="f917a-149">The number of instructions run can be much higher because of the loop/rep support; however, this is capped by MaxVShaderInstructionsExecuted in D3DCAPS9 which should be at least 0xFFFF.</span></span>

### <a name="device-caps"></a><span data-ttu-id="f917a-150">Geräteobergrenzen</span><span class="sxs-lookup"><span data-stu-id="f917a-150">Device Caps</span></span>

<span data-ttu-id="f917a-151">Wenn Vertex-Shader 3 \_ 0 unterstützt wird, werden die folgenden Obergrenzen (mindestens) in der Hardware unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f917a-151">If Vertex Shader 3\_0 is supported, the following caps are supported in hardware (at a minimum):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f917a-152">Cap</span><span class="sxs-lookup"><span data-stu-id="f917a-152">Cap</span></span></th>
<th><span data-ttu-id="f917a-153">Funktion</span><span class="sxs-lookup"><span data-stu-id="f917a-153">Capability</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f917a-154">Shader-Kapselungen</span><span class="sxs-lookup"><span data-stu-id="f917a-154">Shader caps</span></span></td>
<td><ul>
<li><span data-ttu-id="f917a-155">DynamicFlowControlDepth ist 24</span><span class="sxs-lookup"><span data-stu-id="f917a-155">DynamicFlowControlDepth is 24</span></span></li>
<li><span data-ttu-id="f917a-156">NumTemps ist 32</span><span class="sxs-lookup"><span data-stu-id="f917a-156">NumTemps is 32</span></span></li>
<li><span data-ttu-id="f917a-157">StaticFlowControlDepth ist 4</span><span class="sxs-lookup"><span data-stu-id="f917a-157">StaticFlowControlDepth is 4</span></span></li>
<li><span data-ttu-id="f917a-158">Prädikation wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f917a-158">Predication is supported.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f917a-159">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span><span class="sxs-lookup"><span data-stu-id="f917a-159">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span></span></td>
<td><span data-ttu-id="f917a-160">8 KB</span><span class="sxs-lookup"><span data-stu-id="f917a-160">8K</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f917a-161">VertexShaderVersion</span><span class="sxs-lookup"><span data-stu-id="f917a-161">VertexShaderVersion</span></span></td>
<td><span data-ttu-id="f917a-162">3_0</span><span class="sxs-lookup"><span data-stu-id="f917a-162">3_0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f917a-163">MaxVertexShaderConst</span><span class="sxs-lookup"><span data-stu-id="f917a-163">MaxVertexShaderConst</span></span></td>
<td><span data-ttu-id="f917a-164">256</span><span class="sxs-lookup"><span data-stu-id="f917a-164">256</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f917a-165">MaxVertexShader30InstructionSlots</span><span class="sxs-lookup"><span data-stu-id="f917a-165">MaxVertexShader30InstructionSlots</span></span></td>
<td><span data-ttu-id="f917a-166">512</span><span class="sxs-lookup"><span data-stu-id="f917a-166">512</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f917a-167">Unterstützung für Diess</span><span class="sxs-lookup"><span data-stu-id="f917a-167">Fog support</span></span></td>
<td><span data-ttu-id="f917a-168">D3DPRASTERCAPS_FOGVERTEX</span><span class="sxs-lookup"><span data-stu-id="f917a-168">D3DPRASTERCAPS_FOGVERTEX</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f917a-169">VertexTextureFilterCaps</span><span class="sxs-lookup"><span data-stu-id="f917a-169">VertexTextureFilterCaps</span></span></td>
<td><ul>
<li><span data-ttu-id="f917a-170"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="f917a-170"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span></span></li>
<li><span data-ttu-id="f917a-171"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="f917a-171"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f917a-172"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span><span class="sxs-lookup"><span data-stu-id="f917a-172"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span></span></td>
<td><span data-ttu-id="f917a-173">Vertexelemente in einer Scheitelpunktdeklaration können denselben Datenstromoffset gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="f917a-173">Vertex elements in a vertex declaration can share the same stream offset.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f917a-174">Vertexformate</span><span class="sxs-lookup"><span data-stu-id="f917a-174">Vertex formats</span></span></td>
<td><ul>
<li><span data-ttu-id="f917a-175">D3DDECLTYPE_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="f917a-175">D3DDECLTYPE_UBYTE4</span></span></li>
<li><span data-ttu-id="f917a-176">D3DDECLTYPE_UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="f917a-176">D3DDECLTYPE_UBYTE4N</span></span></li>
<li><span data-ttu-id="f917a-177">D3DDECLTYPE_SHORT2N</span><span class="sxs-lookup"><span data-stu-id="f917a-177">D3DDECLTYPE_SHORT2N</span></span></li>
<li><span data-ttu-id="f917a-178">D3DDECLTYPE_SHORT4N</span><span class="sxs-lookup"><span data-stu-id="f917a-178">D3DDECLTYPE_SHORT4N</span></span></li>
<li><span data-ttu-id="f917a-179">D3DDECLTYPE_FLOAT16_2</span><span class="sxs-lookup"><span data-stu-id="f917a-179">D3DDECLTYPE_FLOAT16_2</span></span></li>
<li><span data-ttu-id="f917a-180">D3DDECLTYPE_FLOAT16_4</span><span class="sxs-lookup"><span data-stu-id="f917a-180">D3DDECLTYPE_FLOAT16_4</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f917a-181">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f917a-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f917a-182">Vertex-Shader</span><span class="sxs-lookup"><span data-stu-id="f917a-182">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 