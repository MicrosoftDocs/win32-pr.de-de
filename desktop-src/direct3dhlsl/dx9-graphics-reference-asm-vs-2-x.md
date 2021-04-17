---
title: vs_2_x
description: Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die für Scheitelpunkt Daten verwendet werden. Registriert Übertragungsdaten in und aus dem Alu. Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d09af016ca4fd399de0f2aeec1267343b9d11574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473756"
---
# <a name="vs_2_x"></a><span data-ttu-id="93bc8-105">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="93bc8-105">vs\_2\_x</span></span>

<span data-ttu-id="93bc8-106">Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die für Scheitelpunkt Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93bc8-106">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="93bc8-107">Registriert Übertragungsdaten in und aus dem Alu.</span><span class="sxs-lookup"><span data-stu-id="93bc8-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="93bc8-108">Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="93bc8-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="93bc8-109">Die Vertex-Shader-Version vs \_ 2 \_ x erweitert den von vs \_ 2 0 unterstützten Funktions Satz \_ .</span><span class="sxs-lookup"><span data-stu-id="93bc8-109">Vertex shader version vs\_2\_x extends the feature set supported by vs\_2\_0.</span></span> <span data-ttu-id="93bc8-110">Jede zusätzliche Funktion wird durch eine entsprechende Obergrenze in der [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) -Struktur innerhalb von [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="93bc8-110">Each additional feature is represented by a corresponding cap in the [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) structure within [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps).</span></span> <span data-ttu-id="93bc8-111">Um eine der erweiterten Features zu verwenden, die durch diese Caps repräsentiert werden, muss die Vertex-Shader-Version als vs \_ 2 x angegeben werden \_ .</span><span class="sxs-lookup"><span data-stu-id="93bc8-111">To use any of the enhanced features represented by these caps, the vertex shader version must be specified as vs\_2\_x.</span></span>

-   <span data-ttu-id="93bc8-112">[Anweisungen-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) enthält eine Liste der verfügbaren Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="93bc8-112">[Instructions - vs\_2\_x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="93bc8-113">[Register-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) listet die verschiedenen Register Typen auf, die von Vertex-Shader-Alu verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93bc8-113">[Registers - vs\_2\_x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="93bc8-114">[Vertex-Shader-registermodifiziererer](dx9-graphics-reference-asm-vs-registers-modifiers.md) werden verwendet, um die Funktionsweise einer Anweisung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="93bc8-114">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="93bc8-115">[Vertex-Shader-Quell Registrierungs Modifizierers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) ändern die Quell Registrierungsdaten, bevor die Anweisung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="93bc8-115">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="93bc8-116">Das [Quellen Register "Schwenken](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) " bietet zusätzliche Kontrolle darüber, welche Register Komponenten gelesen, kopiert oder geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="93bc8-116">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="93bc8-117">Die [Ziel Register Maskierung](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) bestimmt, welche Komponenten des Ziel Registers geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="93bc8-117">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="93bc8-118">Neue Funktionen</span><span class="sxs-lookup"><span data-stu-id="93bc8-118">New Features</span></span>

<span data-ttu-id="93bc8-119">Die neuen Features lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="93bc8-119">New features are as follows:</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="93bc8-120">Dynamische Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="93bc8-120">Dynamic Flow Control</span></span>

<span data-ttu-id="93bc8-121">Wenn [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0 ist, werden die folgenden dynamischen Fluss Steuerungs Anweisungen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="93bc8-121">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, then the following dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="93bc8-122">Wenn \_ Comp-vs</span><span class="sxs-lookup"><span data-stu-id="93bc8-122">if\_comp - vs</span></span>](if-comp---vs.md)
-   [<span data-ttu-id="93bc8-123">Break-vs</span><span class="sxs-lookup"><span data-stu-id="93bc8-123">break - vs</span></span>](break---vs.md)
-   [<span data-ttu-id="93bc8-124">" \_ Comp-vs" Abbrechen</span><span class="sxs-lookup"><span data-stu-id="93bc8-124">break\_comp - vs</span></span>](break-comp---vs.md)

<span data-ttu-id="93bc8-125">Wenn [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) ebenfalls festgelegt ist, werden die folgenden zusätzlichen Anweisungen für die Fluss Steuerung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="93bc8-125">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is also set, the following additional flow control instructions are supported:</span></span>

-   [<span data-ttu-id="93bc8-126">SETP \_ -Comp-vs</span><span class="sxs-lookup"><span data-stu-id="93bc8-126">setp\_comp - vs</span></span>](setp-comp---vs.md)
-   [<span data-ttu-id="93bc8-127">Wenn pred-vs</span><span class="sxs-lookup"><span data-stu-id="93bc8-127">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="93bc8-128">callnz pred-vs</span><span class="sxs-lookup"><span data-stu-id="93bc8-128">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="93bc8-129">Break p-vs</span><span class="sxs-lookup"><span data-stu-id="93bc8-129">breakp - vs</span></span>](breakp---vs.md)

<span data-ttu-id="93bc8-130">Der Wertebereich für die Tiefe der dynamischen Fluss Steuerung liegt zwischen 0 und 24 und entspricht der Schachtelungs Tiefe der dynamischen Fluss Steuerungs Anweisungen (Weitere Informationen finden Sie unter [Fluss Steuerungs](dx9-graphics-reference-asm-vs-instructions-flow-control.md) Schachtelungs Limits).</span><span class="sxs-lookup"><span data-stu-id="93bc8-130">The range of values for dynamic flow control depth is 0 to 24 and is equal to the nesting depth of the dynamic flow control instructions (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span> <span data-ttu-id="93bc8-131">Wenn diese Obergrenze NULL ist, unterstützt das Gerät keine Anweisungen zur dynamischen Fluss Steuerung.</span><span class="sxs-lookup"><span data-stu-id="93bc8-131">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

### <a name="number-of-temporary-registers"></a><span data-ttu-id="93bc8-132">Anzahl temporärer Register</span><span class="sxs-lookup"><span data-stu-id="93bc8-132">Number of Temporary Registers</span></span>

<span data-ttu-id="93bc8-133">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) stellt die Anzahl der vom Gerät unterstützten [temporären Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s dar.</span><span class="sxs-lookup"><span data-stu-id="93bc8-133">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s supported by the device.</span></span> <span data-ttu-id="93bc8-134">Der Wertebereich für diese Obergrenze liegt zwischen 12 und 32.</span><span class="sxs-lookup"><span data-stu-id="93bc8-134">The range of values for this cap is 12 to 32.</span></span>

### <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="93bc8-135">Schachtelungs Tiefe der statischen Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="93bc8-135">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="93bc8-136">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) stellt die Schachtelungs Tiefe von zwei Typen von statischen Fluss Steuerungs Anweisungen dar: [Loop-vs](loop---vs.md) / [Rep-vs](rep---vs.md) und [](call---vs.md) / [Call-vs callnz bool-vs](callnz-bool---vs.md) / ,[Wenn bool-vs](if-bool---vs.md). Loop-vs/Rep-vs-Anweisungen bis zu D3DVS20CAPS tief geschachtelt werden können.</span><span class="sxs-lookup"><span data-stu-id="93bc8-136">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the nesting depth of two types of static flow control instructions: [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) and [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[if bool - vs](if-bool---vs.md). loop - vs/rep - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="93bc8-137">Unabhängig davon können die Anweisungen "Aufruf-vs/callnz bool-vs" bis zu D3DVS20CAPS tief verschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="93bc8-137">Independently, call - vs/callnz bool - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="93bc8-138">Wenn D3DVS20CAPS ebenfalls festgelegt ist, wird [callnz pred-vs](callnz-pred---vs.md) in Richtung der Schachtelungs Tiefe von Call-vs/callnz bool-vs/if bool-vs gezählt (Weitere Informationen finden Sie unter [Fluss Steuerungs](dx9-graphics-reference-asm-vs-instructions-flow-control.md) Schachtelungs Limits).</span><span class="sxs-lookup"><span data-stu-id="93bc8-138">If D3DVS20CAPS is also set, then [callnz pred - vs](callnz-pred---vs.md) is counted toward the nesting depth of call - vs/callnz bool - vs/if bool - vs (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span>

### <a name="predication"></a><span data-ttu-id="93bc8-139">Prädikation</span><span class="sxs-lookup"><span data-stu-id="93bc8-139">Predication</span></span>

<span data-ttu-id="93bc8-140">Wenn [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) festgelegt ist, unterstützt das Gerät [SETP \_ Comp-vs](setp-comp---vs.md) und Anweisungs Prädikat.</span><span class="sxs-lookup"><span data-stu-id="93bc8-140">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is set, the device supports [setp\_comp - vs](setp-comp---vs.md) and instruction predication.</span></span> <span data-ttu-id="93bc8-141">Wenn D3DVS20CAPS auch größer als 0 ist, werden die folgenden zusätzlichen dynamischen Fluss Steuerungs Anweisungen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="93bc8-141">If D3DVS20CAPS is also greater than 0, then the following additional dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="93bc8-142">Wenn pred-vs</span><span class="sxs-lookup"><span data-stu-id="93bc8-142">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="93bc8-143">callnz pred-vs</span><span class="sxs-lookup"><span data-stu-id="93bc8-143">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="93bc8-144">Break p-vs</span><span class="sxs-lookup"><span data-stu-id="93bc8-144">breakp - vs</span></span>](breakp---vs.md)

### <a name="instruction-count"></a><span data-ttu-id="93bc8-145">Anweisungs Anzahl</span><span class="sxs-lookup"><span data-stu-id="93bc8-145">Instruction Count</span></span>

<span data-ttu-id="93bc8-146">Jeder Vertex-Shader kann bis zu 256 Anweisungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="93bc8-146">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="93bc8-147">Die Anzahl der auszustellenden Anweisungen kann aufgrund der Unterstützung für Schleifen/Rep erheblich höher sein und wird von [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)begrenzt. Dies sollte mindestens 0xFFFF betragen.</span><span class="sxs-lookup"><span data-stu-id="93bc8-147">The number of instructions run can be much higher (because of the loop/rep support), and is capped by [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93bc8-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="93bc8-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93bc8-149">Vertex-Shader</span><span class="sxs-lookup"><span data-stu-id="93bc8-149">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 