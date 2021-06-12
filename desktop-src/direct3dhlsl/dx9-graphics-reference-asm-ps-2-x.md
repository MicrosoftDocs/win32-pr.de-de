---
title: ps_2_x
description: Erfahren Sie mehr über ps_2_x, einen programmierbaren Pixelshader, der aus einer Reihe von Anweisungen besteht, die mit Pixeldaten arbeiten.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9efedc6011cb63b6465fd2d3ced4a7807c09f4da
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010873"
---
# <a name="ps_2_x"></a><span data-ttu-id="e32f4-103">ps \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e32f4-103">ps\_2\_x</span></span>

<span data-ttu-id="e32f4-104">Ein programmierbarer Pixel-Shader besteht aus einer Reihe von Anweisungen, die mit Pixeldaten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e32f4-104">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="e32f4-105">Registriert Datenübertragungen in und aus der ALU.</span><span class="sxs-lookup"><span data-stu-id="e32f4-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="e32f4-106">Es kann ein zusätzliches Steuerelement angewendet werden, um die Anweisung, die Ergebnisse oder die geschriebenen Daten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e32f4-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="e32f4-107">[ps \_ 2 \_ x Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) enthält eine Liste der verfügbaren Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="e32f4-107">[ps\_2\_x Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="e32f4-108">[ps \_ 2 \_ x Registers listet](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) die verschiedenen Registertypen auf, die vom Vertex-Shader ALU verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e32f4-108">[ps\_2\_x Registers](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="e32f4-109">[Modifizierer](dx9-graphics-reference-asm-ps-registers-modifiers.md) Werden verwendet, um die Funktionsweise einer Anweisung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e32f4-109">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="e32f4-110">[Zielregister-Schreibmaske](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) bestimmt, welche Komponenten des Zielregisters geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e32f4-110">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="e32f4-111">[Die Quellregistermodifizierer des Pixelshader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) ändern die Quellregisterdaten, bevor die Anweisung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e32f4-111">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="e32f4-112">[Das Quellenregister swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) bietet zusätzliche Kontrolle darüber, welche Registerkomponenten gelesen, kopiert oder geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e32f4-112">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="dynamic-flow-control"></a><span data-ttu-id="e32f4-113">Dynamische Flusssteuerung</span><span class="sxs-lookup"><span data-stu-id="e32f4-113">Dynamic Flow Control</span></span>

<span data-ttu-id="e32f4-114">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) stellt die Schachtelungstiefe dynamischer Ablaufsteuerungsanweisungen dar: [, wenn](if-bool---ps.md) [, wenn \_ comp](if-comp---ps.md), [wenn vor \_ ,](if-pred---ps.md) [break - ps](break---ps.md), und break comp - [ \_ ps](break-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="e32f4-114">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of dynamic flow control instructions: [if](if-bool---ps.md), [if\_comp](if-comp---ps.md), [if\_pred](if-pred---ps.md), [break - ps](break---ps.md), and [break\_comp - ps](break-comp---ps.md).</span></span> <span data-ttu-id="e32f4-115">Der Wert entspricht der Schachtelungstiefe des if \_ comp-Blocks.</span><span class="sxs-lookup"><span data-stu-id="e32f4-115">The value is equal to the nesting depth of the if\_comp block.</span></span> <span data-ttu-id="e32f4-116">Wenn diese Obergrenze 0 (null) ist, unterstützt das Gerät keine Anweisungen zur dynamischen Flusssteuerung.</span><span class="sxs-lookup"><span data-stu-id="e32f4-116">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

## <a name="number-of-temporary-registers"></a><span data-ttu-id="e32f4-117">Anzahl temporärer Register</span><span class="sxs-lookup"><span data-stu-id="e32f4-117">Number of Temporary Registers</span></span>

<span data-ttu-id="e32f4-118">Die Anzahl der vom Gerät unterstützten temporären Register.</span><span class="sxs-lookup"><span data-stu-id="e32f4-118">The number of temporary registers supported by the device.</span></span> <span data-ttu-id="e32f4-119">Der Bereich liegt zwischen 12 und 32.</span><span class="sxs-lookup"><span data-stu-id="e32f4-119">The range is from 12 to 32.</span></span>

## <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="e32f4-120">Schachtelungstiefe der statischen Flusssteuerung</span><span class="sxs-lookup"><span data-stu-id="e32f4-120">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="e32f4-121">[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) stellt die Schachtelungstiefe von zwei Typen statischer Ablaufsteuerungsanweisungen dar: [](loop---ps.md)  / [Schleifenreplik und](rep---ps.md) [Aufruf](call---ps.md)  / [von callnz](callnz-bool---ps.md).</span><span class="sxs-lookup"><span data-stu-id="e32f4-121">[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of two types of static flow control instructions: [loop](loop---ps.md) /[rep](rep---ps.md) And [call](call---ps.md) /[callnz](callnz-bool---ps.md).</span></span> <span data-ttu-id="e32f4-122">Schleifenanweisungen /rep können bis zu **StaticFlowControlDepth** deep geschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="e32f4-122">loop /rep instructions can be nested up to **StaticFlowControlDepth** deep.</span></span> <span data-ttu-id="e32f4-123">Unabhängig davon können Aufrufanweisungen von /callnz bis zu **StaticFlowControlDepth** deep geschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="e32f4-123">Independently, call /callnz instructions can be nested up to **StaticFlowControlDepth** deep.</span></span>

## <a name="number-of-instruction-slots"></a><span data-ttu-id="e32f4-124">Anzahl der Anweisungsslots</span><span class="sxs-lookup"><span data-stu-id="e32f4-124">Number of Instruction Slots</span></span>

<span data-ttu-id="e32f4-125">Die Anzahl der Anweisungsslots kann zwischen 96 und maximal 512 liegen und wird von [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)angegeben.</span><span class="sxs-lookup"><span data-stu-id="e32f4-125">The number of instruction slots can range from 96 to a maximum of 512, and is specified by the [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span></span> <span data-ttu-id="e32f4-126">Die Gesamtzahl der Anweisungen, die ausgeführt werden können, wird von **MaxPixelShaderInstructionsExecuted** definiert.</span><span class="sxs-lookup"><span data-stu-id="e32f4-126">The total number of instructions that can run is defined by **MaxPixelShaderInstructionsExecuted**.</span></span> <span data-ttu-id="e32f4-127">Dies kann aufgrund von Schleifen- und Unterroutinenaufrufen größer als die Anzahl der Anweisungsslots sein.</span><span class="sxs-lookup"><span data-stu-id="e32f4-127">This can be larger than the number of instruction slots due to looping and subroutine calls.</span></span>

## <a name="arbitrary-swizzle"></a><span data-ttu-id="e32f4-128">Beliebiger Swizzle</span><span class="sxs-lookup"><span data-stu-id="e32f4-128">Arbitrary Swizzle</span></span>

<span data-ttu-id="e32f4-129">Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, wird beliebige Swizzle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e32f4-129">If [**D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, arbitrary swizzle is supported.</span></span> <span data-ttu-id="e32f4-130">Weitere Informationen finden Sie [unter Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="e32f4-130">See [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span></span>

## <a name="gradient-instructions"></a><span data-ttu-id="e32f4-131">Farbverlaufsanweisungen</span><span class="sxs-lookup"><span data-stu-id="e32f4-131">Gradient Instructions</span></span>

<span data-ttu-id="e32f4-132">Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, werden Farbverlaufsanweisungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e32f4-132">If [**D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, gradient instructions are supported.</span></span> <span data-ttu-id="e32f4-133">Siehe [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)und [texldd - ps](texldd---ps.md).</span><span class="sxs-lookup"><span data-stu-id="e32f4-133">See [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md), and [texldd - ps](texldd---ps.md).</span></span>

## <a name="predication"></a><span data-ttu-id="e32f4-134">Prädikation</span><span class="sxs-lookup"><span data-stu-id="e32f4-134">Predication</span></span>

<span data-ttu-id="e32f4-135">Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, wird die Anweisungsprädikation unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e32f4-135">If [**D3DD3DPSHADERCAPS2\_0\_PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, instruction predication is supported.</span></span> <span data-ttu-id="e32f4-136">Weitere Informationen finden Sie unter [Prädikatregister.](dx9-graphics-reference-asm-ps-registers-predicate.md)</span><span class="sxs-lookup"><span data-stu-id="e32f4-136">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>

## <a name="dependent-read-limit"></a><span data-ttu-id="e32f4-137">Abhängiger Lesegrenzwert</span><span class="sxs-lookup"><span data-stu-id="e32f4-137">Dependent Read Limit</span></span>

<span data-ttu-id="e32f4-138">Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, gibt es keine abhängigen Lesegrenzwerte.</span><span class="sxs-lookup"><span data-stu-id="e32f4-138">If [**D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there are no dependent read limits.</span></span>

## <a name="texture-instruction-limit"></a><span data-ttu-id="e32f4-139">Grenzwert für Texturanweisung</span><span class="sxs-lookup"><span data-stu-id="e32f4-139">Texture Instruction Limit</span></span>

<span data-ttu-id="e32f4-140">Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, gibt es keine Beschränkung für Texturanweisungen.</span><span class="sxs-lookup"><span data-stu-id="e32f4-140">If [**D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there is no limit on texture instructions.</span></span>

## <a name="sampler-count"></a><span data-ttu-id="e32f4-141">Sampleranzahl</span><span class="sxs-lookup"><span data-stu-id="e32f4-141">Sampler Count</span></span>

<span data-ttu-id="e32f4-142">Die Anzahl der verfügbaren Textur-Sampler beträgt 16.</span><span class="sxs-lookup"><span data-stu-id="e32f4-142">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e32f4-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e32f4-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e32f4-144">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="e32f4-144">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 