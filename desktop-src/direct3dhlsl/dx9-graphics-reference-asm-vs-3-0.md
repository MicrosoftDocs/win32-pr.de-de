---
title: vs_3_0
description: Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die für Scheitelpunkt Daten verwendet werden. Registriert Übertragungsdaten in und aus dem Alu. Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 22a0e6e84aff34dcec44713dc4382e391ad05c2b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103858528"
---
# <a name="vs_3_0"></a><span data-ttu-id="63161-105">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="63161-105">vs\_3\_0</span></span>

<span data-ttu-id="63161-106">Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die für Scheitelpunkt Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63161-106">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="63161-107">Registriert Übertragungsdaten in und aus dem Alu.</span><span class="sxs-lookup"><span data-stu-id="63161-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="63161-108">Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="63161-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="63161-109">Die Vertex-Shader-Version vs \_ 3 \_ 0 erweitert den von vs \_ 2 x unterstützten Funktions Satz \_ .</span><span class="sxs-lookup"><span data-stu-id="63161-109">Vertex shader version vs\_3\_0 extends the feature set supported by vs\_2\_x.</span></span> <span data-ttu-id="63161-110">Alle Features in vs \_ 2 X, \_ für die eine Obergrenze festgelegt werden muss, sind in vs \_ 3 \_ 0 verfügbar, ohne dass die Obergrenze erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="63161-110">Each of the features in vs\_2\_X that requires a cap to be set, is available in vs\_3\_0 without requiring the cap.</span></span>

-   <span data-ttu-id="63161-111">[Anweisungen: vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) enthält eine Liste der verfügbaren Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="63161-111">[Instructions - vs\_3\_0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="63161-112">[Register-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) listet die verschiedenen Register Typen auf, die von Vertex Shader Alu verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63161-112">[Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="63161-113">[Vertex-Shader-registermodifiziererer](dx9-graphics-reference-asm-vs-registers-modifiers.md) werden verwendet, um die Funktionsweise einer Anweisung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="63161-113">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="63161-114">[Vertex-Shader-Quell Registrierungs Modifizierers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) ändern die Quell Registrierungsdaten, bevor die Anweisung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63161-114">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="63161-115">Das [Quellen Register "Schwenken](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) " bietet zusätzliche Kontrolle darüber, welche Register Komponenten gelesen, kopiert oder geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="63161-115">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="63161-116">Die [Ziel Register Maskierung](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) bestimmt, welche Komponenten des Ziel Registers geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="63161-116">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="63161-117">Neue Funktionen</span><span class="sxs-lookup"><span data-stu-id="63161-117">New Features</span></span>

<span data-ttu-id="63161-118">\_In den folgenden Abschnitten werden die neuen Features der Vertex-Shader-Version vs 3 \_ 0 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="63161-118">New features of vertex shader version vs\_3\_0 are listed in the following sections.</span></span>

### <a name="indexing-registers"></a><span data-ttu-id="63161-119">Indizieren von Registern</span><span class="sxs-lookup"><span data-stu-id="63161-119">Indexing Registers</span></span>

<span data-ttu-id="63161-120">In den früheren shadermodellen konnte nur die Konstante Register Bank indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="63161-120">In the earlier shader models, only the constant register bank could be indexed.</span></span> <span data-ttu-id="63161-121">In diesem Modell können die folgenden Register Banken indiziert werden, indem das Schleifen-Counter-Register (Al) verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="63161-121">In this model, the following register banks can be indexed, using the loop counter register (aL):</span></span>

-   <span data-ttu-id="63161-122">Eingabe Register (v \# )</span><span class="sxs-lookup"><span data-stu-id="63161-122">Input register (v\#)</span></span>
-   <span data-ttu-id="63161-123">Ausgabe Register (o \# )</span><span class="sxs-lookup"><span data-stu-id="63161-123">Output register (o\#)</span></span>

### <a name="vertex-textures"></a><span data-ttu-id="63161-124">Scheitelpunkt Texturen</span><span class="sxs-lookup"><span data-stu-id="63161-124">Vertex Textures</span></span>

<span data-ttu-id="63161-125">Dieses Shader-Modell unterstützt die Textur Suche im Vertex-Shader mithilfe von texldl.</span><span class="sxs-lookup"><span data-stu-id="63161-125">This shader model supports texture lookup in the vertex shader using texldl.</span></span> <span data-ttu-id="63161-126">Die Vertex-Engine verfügt über vier Textur Sampler-Phasen (die sich vom Verschiebungs Übersichts Sampler und den Textur Beispielen in der Pixel-Engine unterscheiden), die zum Beispiel für Texturen verwendet werden können, die in diesen Phasen festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="63161-126">The vertex engine has four texture sampler stages (distinct from the displacement map sampler and the texture samplers in the pixel engine) that can be used to sample textures set at those stages.</span></span> <span data-ttu-id="63161-127">Weitere Informationen finden Sie [unter Scheitelpunkt Texturen in vs \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).</span><span class="sxs-lookup"><span data-stu-id="63161-127">See [Vertex Textures in vs\_3\_0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).</span></span>

### <a name="vertex-stream-frequency"></a><span data-ttu-id="63161-128">Vertexstreamhäufigkeit</span><span class="sxs-lookup"><span data-stu-id="63161-128">Vertex Stream Frequency</span></span>

<span data-ttu-id="63161-129">Diese Funktion ermöglicht es, dass eine Teilmenge der Eingabe Register mit einer anderen Rate als einmal pro Scheitelpunkt initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="63161-129">This feature allows a subset of the input registers to be initialized at a rate different from once per vertex.</span></span> <span data-ttu-id="63161-130">Siehe [Zeichnen nicht indizierter Geometrie](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).</span><span class="sxs-lookup"><span data-stu-id="63161-130">See [Drawing Non-Indexed Geometry](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).</span></span>

### <a name="shader-output"></a><span data-ttu-id="63161-131">Shader-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="63161-131">Shader Output</span></span>

<span data-ttu-id="63161-132">Ähnlich wie bei vs \_ 2 \_ 0 kann die Ausgabe des Shaders von der statischen Fluss Steuerung abweichen.</span><span class="sxs-lookup"><span data-stu-id="63161-132">Similar to vs\_2\_0, the output of the shader can vary with static flow control.</span></span> <span data-ttu-id="63161-133">Gehen Sie bei dynamischer Verzweigungen vorsichtig vor, da dies dazu führen kann, dass Shader-Ausgaben pro Scheitelpunkt variieren.</span><span class="sxs-lookup"><span data-stu-id="63161-133">Be careful with dynamic branching as this can cause shader outputs to vary per vertex.</span></span> <span data-ttu-id="63161-134">Dies führt zu unvorhersehbaren Ergebnissen auf einer anderen Hardware.</span><span class="sxs-lookup"><span data-stu-id="63161-134">This will produce unpredictable results on different hardware.</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="63161-135">Dynamische Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="63161-135">Dynamic flow control</span></span>

<span data-ttu-id="63161-136">Alle Anweisungen zur dynamischen Fluss Steuerung werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63161-136">All dynamic flow control instructions are supported.</span></span> <span data-ttu-id="63161-137">Der maximal zulässige Wert für die Schachtelungs Tiefe ist 24.</span><span class="sxs-lookup"><span data-stu-id="63161-137">The maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="63161-138">(Ausführliche Informationen finden Sie unter [Fluss Steuerungs](dx9-graphics-reference-asm-vs-instructions-flow-control.md) Schachtelungs Limits.)</span><span class="sxs-lookup"><span data-stu-id="63161-138">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="temporary-registers"></a><span data-ttu-id="63161-139">Temporäre Register</span><span class="sxs-lookup"><span data-stu-id="63161-139">Temporary Registers</span></span>

<span data-ttu-id="63161-140">Insgesamt werden 32 temporäre Register (r \# ) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63161-140">A total of 32 temporary registers (r\#) is supported.</span></span>

### <a name="static-flow-control"></a><span data-ttu-id="63161-141">Statische Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="63161-141">Static Flow Control</span></span>

<span data-ttu-id="63161-142">Die maximale Schachtelungs Tiefe für [Loop-vs](loop---vs.md) / [Rep-vs](rep---vs.md) ist 4.</span><span class="sxs-lookup"><span data-stu-id="63161-142">The maximum nesting depth for [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) is 4.</span></span> <span data-ttu-id="63161-143">Die maximale Schachtelungs Tiefe für [Aufruf-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [callnz pred-vs](callnz-pred---vs.md) ist 4.</span><span class="sxs-lookup"><span data-stu-id="63161-143">The maximum nesting depth for [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[callnz pred - vs](callnz-pred---vs.md) is 4.</span></span> <span data-ttu-id="63161-144">Bei [booleschen](if-bool---vs.md)Werten beträgt der Wert für die maximale Schachtelungs Tiefe 24.</span><span class="sxs-lookup"><span data-stu-id="63161-144">For [if bool - vs](if-bool---vs.md), the maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="63161-145">(Ausführliche Informationen finden Sie unter [Fluss Steuerungs](dx9-graphics-reference-asm-vs-instructions-flow-control.md) Schachtelungs Limits.)</span><span class="sxs-lookup"><span data-stu-id="63161-145">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="predication"></a><span data-ttu-id="63161-146">Prädikation</span><span class="sxs-lookup"><span data-stu-id="63161-146">Predication</span></span>

<span data-ttu-id="63161-147">Das Anweisungs Prädikat wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63161-147">Instruction predication is supported.</span></span> <span data-ttu-id="63161-148">Verwenden Sie [SETP \_ Comp-vs](setp-comp---vs.md) , um das Prädikat Register festzulegen.</span><span class="sxs-lookup"><span data-stu-id="63161-148">Use [setp\_comp - vs](setp-comp---vs.md) to set the predicate register.</span></span>

### <a name="instruction-count"></a><span data-ttu-id="63161-149">Anweisungs Anzahl</span><span class="sxs-lookup"><span data-stu-id="63161-149">Instruction Count</span></span>

<span data-ttu-id="63161-150">Jeder Vertex-Shader ist von 512 bis zur Anzahl der Slots in MaxVertexShader30InstructionSlots in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)zulässig.</span><span class="sxs-lookup"><span data-stu-id="63161-150">Each vertex shader is allowed anywhere from 512 up to the number of slots in MaxVertexShader30InstructionSlots in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span></span> <span data-ttu-id="63161-151">Die Anzahl der auszuwerenden Anweisungen kann aufgrund der Unterstützung für Schleifen/Rep sehr viel höher sein. Dies wird jedoch durch maxvshaderinstructionsexecuted in D3DCAPS9 begrenzt, das mindestens 0xFFFF betragen sollte.</span><span class="sxs-lookup"><span data-stu-id="63161-151">The number of instructions run can be much higher because of the loop/rep support; however, this is capped by MaxVShaderInstructionsExecuted in D3DCAPS9 which should be at least 0xFFFF.</span></span>

### <a name="device-caps"></a><span data-ttu-id="63161-152">Geräte Obergrenzen</span><span class="sxs-lookup"><span data-stu-id="63161-152">Device Caps</span></span>

<span data-ttu-id="63161-153">Wenn Vertex Shader 3 \_ 0 unterstützt wird, werden die folgenden Obergrenzen auf Hardware (minimal) unterstützt:</span><span class="sxs-lookup"><span data-stu-id="63161-153">If Vertex Shader 3\_0 is supported, the following caps are supported in hardware (at a minimum):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="63161-154">Decke</span><span class="sxs-lookup"><span data-stu-id="63161-154">Cap</span></span></th>
<th><span data-ttu-id="63161-155">Funktion</span><span class="sxs-lookup"><span data-stu-id="63161-155">Capability</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63161-156">Shader-Caps</span><span class="sxs-lookup"><span data-stu-id="63161-156">Shader caps</span></span></td>
<td><ul>
<li><span data-ttu-id="63161-157">Dynamicflowcontroltiefe ist 24</span><span class="sxs-lookup"><span data-stu-id="63161-157">DynamicFlowControlDepth is 24</span></span></li>
<li><span data-ttu-id="63161-158">NumTemps ist 32</span><span class="sxs-lookup"><span data-stu-id="63161-158">NumTemps is 32</span></span></li>
<li><span data-ttu-id="63161-159">Staticflowcontroltiefe ist 4</span><span class="sxs-lookup"><span data-stu-id="63161-159">StaticFlowControlDepth is 4</span></span></li>
<li><span data-ttu-id="63161-160">Ein Prädikat wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63161-160">Predication is supported.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63161-161">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span><span class="sxs-lookup"><span data-stu-id="63161-161">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span></span></td>
<td><span data-ttu-id="63161-162">8 KB</span><span class="sxs-lookup"><span data-stu-id="63161-162">8K</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63161-163">VertexShaderVersion</span><span class="sxs-lookup"><span data-stu-id="63161-163">VertexShaderVersion</span></span></td>
<td><span data-ttu-id="63161-164">3_0</span><span class="sxs-lookup"><span data-stu-id="63161-164">3_0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63161-165">Maxvertexshaderkonstanten</span><span class="sxs-lookup"><span data-stu-id="63161-165">MaxVertexShaderConst</span></span></td>
<td><span data-ttu-id="63161-166">256</span><span class="sxs-lookup"><span data-stu-id="63161-166">256</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63161-167">MaxVertexShader30InstructionSlots</span><span class="sxs-lookup"><span data-stu-id="63161-167">MaxVertexShader30InstructionSlots</span></span></td>
<td><span data-ttu-id="63161-168">512</span><span class="sxs-lookup"><span data-stu-id="63161-168">512</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63161-169">Unterstützung für Nebel</span><span class="sxs-lookup"><span data-stu-id="63161-169">Fog support</span></span></td>
<td><span data-ttu-id="63161-170">D3DPRASTERCAPS_FOGVERTEX</span><span class="sxs-lookup"><span data-stu-id="63161-170">D3DPRASTERCAPS_FOGVERTEX</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63161-171">Vertextexturefiltercaps</span><span class="sxs-lookup"><span data-stu-id="63161-171">VertexTextureFilterCaps</span></span></td>
<td><ul>
<li><span data-ttu-id="63161-172"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="63161-172"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span></span></li>
<li><span data-ttu-id="63161-173"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="63161-173"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63161-174"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span><span class="sxs-lookup"><span data-stu-id="63161-174"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span></span></td>
<td><span data-ttu-id="63161-175">Vertex-Elemente in einer Scheitelpunkt Deklaration können denselben Streamoffset gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="63161-175">Vertex elements in a vertex declaration can share the same stream offset.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63161-176">Scheitelpunkt Formate</span><span class="sxs-lookup"><span data-stu-id="63161-176">Vertex formats</span></span></td>
<td><ul>
<li><span data-ttu-id="63161-177">D3DDECLTYPE_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="63161-177">D3DDECLTYPE_UBYTE4</span></span></li>
<li><span data-ttu-id="63161-178">D3DDECLTYPE_UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="63161-178">D3DDECLTYPE_UBYTE4N</span></span></li>
<li><span data-ttu-id="63161-179">D3DDECLTYPE_SHORT2N</span><span class="sxs-lookup"><span data-stu-id="63161-179">D3DDECLTYPE_SHORT2N</span></span></li>
<li><span data-ttu-id="63161-180">D3DDECLTYPE_SHORT4N</span><span class="sxs-lookup"><span data-stu-id="63161-180">D3DDECLTYPE_SHORT4N</span></span></li>
<li><span data-ttu-id="63161-181">D3DDECLTYPE_FLOAT16_2</span><span class="sxs-lookup"><span data-stu-id="63161-181">D3DDECLTYPE_FLOAT16_2</span></span></li>
<li><span data-ttu-id="63161-182">D3DDECLTYPE_FLOAT16_4</span><span class="sxs-lookup"><span data-stu-id="63161-182">D3DDECLTYPE_FLOAT16_4</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="63161-183">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="63161-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63161-184">Vertex-Shader</span><span class="sxs-lookup"><span data-stu-id="63161-184">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 