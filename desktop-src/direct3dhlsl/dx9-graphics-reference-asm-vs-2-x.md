---
title: vs_2_x
description: Erfahren Sie vs_2_x, einen programmierbaren Vertex-Shader, der aus einer Reihe von Anweisungen besteht, die mit Scheitelpunktdaten arbeiten.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3449ae4c1e1eb3b977916f6fb1d19303e9d21a4e
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010714"
---
# <a name="vs_2_x"></a><span data-ttu-id="d3fe8-103">Vs. \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d3fe8-103">vs\_2\_x</span></span>

<span data-ttu-id="d3fe8-104">Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die mit Scheitelpunktdaten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d3fe8-104">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="d3fe8-105">Registriert Übertragungsdaten in und aus der ALU.</span><span class="sxs-lookup"><span data-stu-id="d3fe8-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="d3fe8-106">Zusätzliche Steuerung kann angewendet werden, um die Anweisung, die Ergebnisse oder die ausgeschriebenen Daten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d3fe8-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="d3fe8-107">Vertex-Shaderversion im Vergleich zu 2 x erweitert den von unterstützten Funktionssatz im Vergleich \_ \_ zu \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="d3fe8-107">Vertex shader version vs\_2\_x extends the feature set supported by vs\_2\_0.</span></span> <span data-ttu-id="d3fe8-108">Jedes zusätzliche Feature wird durch eine entsprechende Obergrenze in der [**D3DCAPS9-Struktur**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) in [D3DVS20CAPS dargestellt.](/windows/desktop/direct3d9/d3dvs20caps)</span><span class="sxs-lookup"><span data-stu-id="d3fe8-108">Each additional feature is represented by a corresponding cap in the [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) structure within [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps).</span></span> <span data-ttu-id="d3fe8-109">Um eines der erweiterten Features zu verwenden, die durch diese Obergrenzen dargestellt werden, muss die Vertex-Shaderversion im Vergleich zu \_ 2 x angegeben \_ werden.</span><span class="sxs-lookup"><span data-stu-id="d3fe8-109">To use any of the enhanced features represented by these caps, the vertex shader version must be specified as vs\_2\_x.</span></span>

-   <span data-ttu-id="d3fe8-110">[Anweisungen im Vergleich \_ zu 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) enthält eine Liste der verfügbaren Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="d3fe8-110">[Instructions - vs\_2\_x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="d3fe8-111">[Register: Im Vergleich \_ zu 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) werden die verschiedenen Registertypen aufgeführt, die von der Vertex-Shader-ALU verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3fe8-111">[Registers - vs\_2\_x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="d3fe8-112">[Vertex-Shader-Registermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers.md) werden verwendet, um die Art und Weise zu ändern, wie eine Anweisung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d3fe8-112">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="d3fe8-113">[Vertex-Shader-Quellregistermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) ändern die Quellregisterdaten, bevor die Anweisung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3fe8-113">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="d3fe8-114">[Source Register Swizzling bietet](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) zusätzliche Kontrolle darüber, welche Registerkomponenten gelesen, kopiert oder geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d3fe8-114">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="d3fe8-115">[Zielregistermaskierung](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) bestimmt, welche Komponenten des Zielregisters geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d3fe8-115">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="d3fe8-116">Neue Funktionen</span><span class="sxs-lookup"><span data-stu-id="d3fe8-116">New Features</span></span>

<span data-ttu-id="d3fe8-117">Die neuen Features lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d3fe8-117">New features are as follows:</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="d3fe8-118">Dynamische Flusssteuerung</span><span class="sxs-lookup"><span data-stu-id="d3fe8-118">Dynamic Flow Control</span></span>

<span data-ttu-id="d3fe8-119">Wenn [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0 ist, werden die folgenden Anweisungen zur dynamischen Flusssteuerung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d3fe8-119">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, then the following dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="d3fe8-120">if \_ comp – vs</span><span class="sxs-lookup"><span data-stu-id="d3fe8-120">if\_comp - vs</span></span>](if-comp---vs.md)
-   [<span data-ttu-id="d3fe8-121">break – vs</span><span class="sxs-lookup"><span data-stu-id="d3fe8-121">break - vs</span></span>](break---vs.md)
-   [<span data-ttu-id="d3fe8-122">break \_ comp – vs</span><span class="sxs-lookup"><span data-stu-id="d3fe8-122">break\_comp - vs</span></span>](break-comp---vs.md)

<span data-ttu-id="d3fe8-123">Wenn [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) ebenfalls festgelegt ist, werden die folgenden zusätzlichen Anweisungen zur Flusssteuerung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d3fe8-123">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is also set, the following additional flow control instructions are supported:</span></span>

-   [<span data-ttu-id="d3fe8-124">setp \_ comp – vs</span><span class="sxs-lookup"><span data-stu-id="d3fe8-124">setp\_comp - vs</span></span>](setp-comp---vs.md)
-   [<span data-ttu-id="d3fe8-125">if pred – vs</span><span class="sxs-lookup"><span data-stu-id="d3fe8-125">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="d3fe8-126">callnz pred – vs</span><span class="sxs-lookup"><span data-stu-id="d3fe8-126">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="d3fe8-127">Breakp im Vergleich zu</span><span class="sxs-lookup"><span data-stu-id="d3fe8-127">breakp - vs</span></span>](breakp---vs.md)

<span data-ttu-id="d3fe8-128">Der Wertebereich für die dynamische Flusssteuerungstiefe beträgt 0 bis 24 und entspricht der Schachtelungstiefe der Anweisungen für die dynamische Flusssteuerung (weitere Informationen finden Sie unter [Grenzwerte](dx9-graphics-reference-asm-vs-instructions-flow-control.md) für die Flusssteuerungsschachtelung).</span><span class="sxs-lookup"><span data-stu-id="d3fe8-128">The range of values for dynamic flow control depth is 0 to 24 and is equal to the nesting depth of the dynamic flow control instructions (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span> <span data-ttu-id="d3fe8-129">Wenn diese Obergrenze 0 ist, unterstützt das Gerät keine Anweisungen zur dynamischen Flusssteuerung.</span><span class="sxs-lookup"><span data-stu-id="d3fe8-129">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

### <a name="number-of-temporary-registers"></a><span data-ttu-id="d3fe8-130">Anzahl temporärer Register</span><span class="sxs-lookup"><span data-stu-id="d3fe8-130">Number of Temporary Registers</span></span>

<span data-ttu-id="d3fe8-131">[D3DVS20CAPS stellt](/windows/desktop/direct3d9/d3dvs20caps) die Anzahl der temporären [Register](dx9-graphics-reference-asm-vs-registers-temporary.md)dar, die vom Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d3fe8-131">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s supported by the device.</span></span> <span data-ttu-id="d3fe8-132">Der Wertebereich für diese Obergrenze beträgt 12 bis 32.</span><span class="sxs-lookup"><span data-stu-id="d3fe8-132">The range of values for this cap is 12 to 32.</span></span>

### <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="d3fe8-133">Schachtelungstiefe der statischen Flusssteuerung</span><span class="sxs-lookup"><span data-stu-id="d3fe8-133">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="d3fe8-134">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) stellt die Schachtelungstiefe von zwei Typen statischer Flusssteuerungsanweisungen dar: loop [– vs](loop---vs.md)rep – vs und call – vs callnz bool – vs if bool – vs . loop – vs/rep – vs instructions can be nested up to D3DVS20CAPS deep (Vs. bool – vs. loop – vs/rep – vs. Anweisungen können bis / [](rep---vs.md) zu [](call---vs.md) / [](callnz-bool---vs.md) / [](if-bool---vs.md)D3DVS20CAPS tief geschachtelt werden).</span><span class="sxs-lookup"><span data-stu-id="d3fe8-134">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the nesting depth of two types of static flow control instructions: [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) and [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[if bool - vs](if-bool---vs.md). loop - vs/rep - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="d3fe8-135">Unabhängig können aufrufe – vs/callnz bool – vs instructions bis zu D3DVS20CAPS deep geschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="d3fe8-135">Independently, call - vs/callnz bool - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="d3fe8-136">Wenn D3DVS20CAPS ebenfalls festgelegt ist, wird [callnz pred - vs](callnz-pred---vs.md) zur Schachtelungstiefe des Aufrufs gezählt – vs/callnz bool – vs/if bool – vs (details finden Sie unter [Grenzwerte](dx9-graphics-reference-asm-vs-instructions-flow-control.md) für die Flusssteuerungsschachtelung).</span><span class="sxs-lookup"><span data-stu-id="d3fe8-136">If D3DVS20CAPS is also set, then [callnz pred - vs](callnz-pred---vs.md) is counted toward the nesting depth of call - vs/callnz bool - vs/if bool - vs (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span>

### <a name="predication"></a><span data-ttu-id="d3fe8-137">Prädikation</span><span class="sxs-lookup"><span data-stu-id="d3fe8-137">Predication</span></span>

<span data-ttu-id="d3fe8-138">Wenn [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) festgelegt ist, unterstützt das Gerät [setp \_ comp - vs](setp-comp---vs.md) and instruction predication.</span><span class="sxs-lookup"><span data-stu-id="d3fe8-138">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is set, the device supports [setp\_comp - vs](setp-comp---vs.md) and instruction predication.</span></span> <span data-ttu-id="d3fe8-139">Wenn D3DVS20CAPS ebenfalls größer als 0 ist, werden die folgenden zusätzlichen Anweisungen zur dynamischen Flusssteuerung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d3fe8-139">If D3DVS20CAPS is also greater than 0, then the following additional dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="d3fe8-140">if pred – vs</span><span class="sxs-lookup"><span data-stu-id="d3fe8-140">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="d3fe8-141">callnz pred – vs</span><span class="sxs-lookup"><span data-stu-id="d3fe8-141">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="d3fe8-142">Breakp im Vergleich zu</span><span class="sxs-lookup"><span data-stu-id="d3fe8-142">breakp - vs</span></span>](breakp---vs.md)

### <a name="instruction-count"></a><span data-ttu-id="d3fe8-143">Anweisungsanzahl</span><span class="sxs-lookup"><span data-stu-id="d3fe8-143">Instruction Count</span></span>

<span data-ttu-id="d3fe8-144">Für jeden Vertex-Shader können bis zu 256 Anweisungen gespeichert sein.</span><span class="sxs-lookup"><span data-stu-id="d3fe8-144">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="d3fe8-145">Die Anzahl der ausgeführten Anweisungen kann viel höher sein (aufgrund der Unterstützung von Schleifen/Wiederholungen) und ist durch [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)begrenzt, was mindestens 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="d3fe8-145">The number of instructions run can be much higher (because of the loop/rep support), and is capped by [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3fe8-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d3fe8-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3fe8-147">Vertex-Shader</span><span class="sxs-lookup"><span data-stu-id="d3fe8-147">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 