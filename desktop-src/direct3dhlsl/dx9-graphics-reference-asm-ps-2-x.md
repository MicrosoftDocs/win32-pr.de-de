---
title: ps_2_x
description: Ein programmierbarer Pixelshader besteht aus einer Reihe von Anweisungen, die auf Pixeldaten angewendet werden. Registriert Übertragungsdaten in und aus dem Alu. Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13e5daf7c3a4b41e5b27b1c20f8b1f5f8355c325
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993503"
---
# <a name="ps_2_x"></a><span data-ttu-id="ef718-105">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ef718-105">ps\_2\_x</span></span>

<span data-ttu-id="ef718-106">Ein programmierbarer Pixelshader besteht aus einer Reihe von Anweisungen, die auf Pixeldaten angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef718-106">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="ef718-107">Registriert Übertragungsdaten in und aus dem Alu.</span><span class="sxs-lookup"><span data-stu-id="ef718-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="ef718-108">Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ef718-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="ef718-109">[die \_ Anweisungen für PS 2 \_ x](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) enthalten eine Liste der verfügbaren Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="ef718-109">[ps\_2\_x Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="ef718-110">[PS \_ 2 \_ x-Register](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) listet die verschiedenen Register Typen auf, die von Vertex Shader Alu verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef718-110">[ps\_2\_x Registers](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="ef718-111">[Modifiziererer](dx9-graphics-reference-asm-ps-registers-modifiers.md) Wird verwendet, um die Funktionsweise einer Anweisung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ef718-111">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="ef718-112">Die [Ziel Register-Schreib Maske](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) bestimmt, welche Komponenten des Ziel Registers geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ef718-112">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="ef718-113">[Pixel-Shader-Quell Registrierungs Modifizierern](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) ändern die Quell Registrierungsdaten, bevor die Anweisung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef718-113">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="ef718-114">Das [Quellen Register "Schwenken](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) " bietet zusätzliche Kontrolle darüber, welche Register Komponenten gelesen, kopiert oder geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ef718-114">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="dynamic-flow-control"></a><span data-ttu-id="ef718-115">Dynamische Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="ef718-115">Dynamic Flow Control</span></span>

<span data-ttu-id="ef718-116">[**Dynamicflowcontroltiefe**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) stellt die Schachtelungs Tiefe dynamischer Fluss Steuerungs Anweisungen dar: [if](if-bool---ps.md), [if \_ Comp](if-comp---ps.md), [if \_ pred](if-pred---ps.md), [break-PS](break---ps.md)und [break \_ -PS unterbrechen](break-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="ef718-116">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of dynamic flow control instructions: [if](if-bool---ps.md), [if\_comp](if-comp---ps.md), [if\_pred](if-pred---ps.md), [break - ps](break---ps.md), and [break\_comp - ps](break-comp---ps.md).</span></span> <span data-ttu-id="ef718-117">Der Wert ist gleich der Schachtelungs Tiefe des If- \_ Comp-Blocks.</span><span class="sxs-lookup"><span data-stu-id="ef718-117">The value is equal to the nesting depth of the if\_comp block.</span></span> <span data-ttu-id="ef718-118">Wenn diese Obergrenze NULL ist, unterstützt das Gerät keine Anweisungen zur dynamischen Fluss Steuerung.</span><span class="sxs-lookup"><span data-stu-id="ef718-118">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

## <a name="number-of-temporary-registers"></a><span data-ttu-id="ef718-119">Anzahl temporärer Register</span><span class="sxs-lookup"><span data-stu-id="ef718-119">Number of Temporary Registers</span></span>

<span data-ttu-id="ef718-120">Die Anzahl der vom Gerät unterstützten temporären Register.</span><span class="sxs-lookup"><span data-stu-id="ef718-120">The number of temporary registers supported by the device.</span></span> <span data-ttu-id="ef718-121">Der Bereich liegt zwischen 12 und 32.</span><span class="sxs-lookup"><span data-stu-id="ef718-121">The range is from 12 to 32.</span></span>

## <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="ef718-122">Schachtelungs Tiefe der statischen Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="ef718-122">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="ef718-123">[**Staticflowcontroltiefe**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) stellt die Schachtelungs Tiefe von zwei Typen von statischen Fluss Steuerungs Anweisungen dar: [Loop](loop---ps.md)  / [Rep](rep---ps.md) und [](call---ps.md)  / [callnz](callnz-bool---ps.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ef718-123">[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of two types of static flow control instructions: [loop](loop---ps.md) /[rep](rep---ps.md) And [call](call---ps.md) /[callnz](callnz-bool---ps.md).</span></span> <span data-ttu-id="ef718-124">Schleife/Rep Anweisungen können in der Tiefe von **staticflowcontroldeep** verschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="ef718-124">loop /rep instructions can be nested up to **StaticFlowControlDepth** deep.</span></span> <span data-ttu-id="ef718-125">/Callnz-Anweisungen können unabhängig voneinander in " **staticflowcontroldeep** " verschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="ef718-125">Independently, call /callnz instructions can be nested up to **StaticFlowControlDepth** deep.</span></span>

## <a name="number-of-instruction-slots"></a><span data-ttu-id="ef718-126">Anzahl der Anweisungs Slots</span><span class="sxs-lookup"><span data-stu-id="ef718-126">Number of Instruction Slots</span></span>

<span data-ttu-id="ef718-127">Die Anzahl der Anweisungs Slots kann zwischen 96 und einem Maximum von 512 liegen und wird durch [**maxpixelshaderinstructionslots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)angegeben.</span><span class="sxs-lookup"><span data-stu-id="ef718-127">The number of instruction slots can range from 96 to a maximum of 512, and is specified by the [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span></span> <span data-ttu-id="ef718-128">Die Gesamtanzahl der Anweisungen, die ausgeführt werden können, wird durch **maxpixelshaderinstructionsexecuted** definiert.</span><span class="sxs-lookup"><span data-stu-id="ef718-128">The total number of instructions that can run is defined by **MaxPixelShaderInstructionsExecuted**.</span></span> <span data-ttu-id="ef718-129">Dieser Wert kann größer als die Anzahl der Anweisungs Slots aufgrund von Schleifen-und Unterroutine aufrufen sein.</span><span class="sxs-lookup"><span data-stu-id="ef718-129">This can be larger than the number of instruction slots due to looping and subroutine calls.</span></span>

## <a name="arbitrary-swizzle"></a><span data-ttu-id="ef718-130">Beliebiger Swizzle</span><span class="sxs-lookup"><span data-stu-id="ef718-130">Arbitrary Swizzle</span></span>

<span data-ttu-id="ef718-131">Wenn [**D3DD3DPSHADERCAPS2 0 für das willkürliche \_ \_ aryswizzle**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, wird ein beliebiges Swizzle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ef718-131">If [**D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, arbitrary swizzle is supported.</span></span> <span data-ttu-id="ef718-132">Weitere Informationen finden Sie unter [Quellen Register: schwenken](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="ef718-132">See [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span></span>

## <a name="gradient-instructions"></a><span data-ttu-id="ef718-133">Farbverlaufs Anweisungen</span><span class="sxs-lookup"><span data-stu-id="ef718-133">Gradient Instructions</span></span>

<span data-ttu-id="ef718-134">Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ gradientinstructions**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, werden Farbverlaufs Anweisungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ef718-134">If [**D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, gradient instructions are supported.</span></span> <span data-ttu-id="ef718-135">Siehe [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)und [texldd-PS](texldd---ps.md).</span><span class="sxs-lookup"><span data-stu-id="ef718-135">See [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md), and [texldd - ps](texldd---ps.md).</span></span>

## <a name="predication"></a><span data-ttu-id="ef718-136">Prädikation</span><span class="sxs-lookup"><span data-stu-id="ef718-136">Predication</span></span>

<span data-ttu-id="ef718-137">Wenn das [**D3DD3DPSHADERCAPS2 \_ 0- \_ Prädikat**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, wird das Anweisungs Prädikat unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ef718-137">If [**D3DD3DPSHADERCAPS2\_0\_PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, instruction predication is supported.</span></span> <span data-ttu-id="ef718-138">Siehe [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="ef718-138">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>

## <a name="dependent-read-limit"></a><span data-ttu-id="ef718-139">Abhängiges Lese Limit</span><span class="sxs-lookup"><span data-stu-id="ef718-139">Dependent Read Limit</span></span>

<span data-ttu-id="ef718-140">Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ nodependentleselimit**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, gibt es keine abhängigen Lese Limits.</span><span class="sxs-lookup"><span data-stu-id="ef718-140">If [**D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there are no dependent read limits.</span></span>

## <a name="texture-instruction-limit"></a><span data-ttu-id="ef718-141">Grenzwert für Textur Anweisung</span><span class="sxs-lookup"><span data-stu-id="ef718-141">Texture Instruction Limit</span></span>

<span data-ttu-id="ef718-142">Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ notexinstructionlimit**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, gibt es keine Begrenzung der Textur Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="ef718-142">If [**D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there is no limit on texture instructions.</span></span>

## <a name="sampler-count"></a><span data-ttu-id="ef718-143">Sampleranzahl</span><span class="sxs-lookup"><span data-stu-id="ef718-143">Sampler Count</span></span>

<span data-ttu-id="ef718-144">Die Anzahl der verfügbaren Textur-Samplern ist 16.</span><span class="sxs-lookup"><span data-stu-id="ef718-144">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef718-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef718-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef718-146">Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="ef718-146">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 