---
title: Pixel-Shader-Unterschiede
description: Pixel-Shader-Unterschiede
ms.assetid: 11aefb26-eb82-486c-81ff-7c0cfbab1b7a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a74b5cc7588220fdc5173c470f7852ee9ef763d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390504"
---
# <a name="pixel-shader-differences"></a><span data-ttu-id="8aba0-103">Pixel-Shader-Unterschiede</span><span class="sxs-lookup"><span data-stu-id="8aba0-103">Pixel Shader Differences</span></span>

## <a name="instruction-slots"></a><span data-ttu-id="8aba0-104">Anweisungs Slots</span><span class="sxs-lookup"><span data-stu-id="8aba0-104">Instruction Slots</span></span>

<span data-ttu-id="8aba0-105">Jede Version unterstützt eine andere Anzahl an maximalen Anweisungs Slots.</span><span class="sxs-lookup"><span data-stu-id="8aba0-105">Each version supports a different number of maximum instruction slots.</span></span>



| <span data-ttu-id="8aba0-106">Version</span><span class="sxs-lookup"><span data-stu-id="8aba0-106">Version</span></span>  | <span data-ttu-id="8aba0-107">Maximale Anzahl von Anweisungs Slots</span><span class="sxs-lookup"><span data-stu-id="8aba0-107">Maximum number of instruction slots</span></span>                                                                                   |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8aba0-108">PS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="8aba0-108">ps\_1\_1</span></span> | <span data-ttu-id="8aba0-109">4 Textur + 8 Arithmetik</span><span class="sxs-lookup"><span data-stu-id="8aba0-109">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="8aba0-110">PS \_ 1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="8aba0-110">ps\_1\_2</span></span> | <span data-ttu-id="8aba0-111">4 Textur + 8 Arithmetik</span><span class="sxs-lookup"><span data-stu-id="8aba0-111">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="8aba0-112">PS \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="8aba0-112">ps\_1\_3</span></span> | <span data-ttu-id="8aba0-113">4 Textur + 8 Arithmetik</span><span class="sxs-lookup"><span data-stu-id="8aba0-113">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="8aba0-114">PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="8aba0-114">ps\_1\_4</span></span> | <span data-ttu-id="8aba0-115">6 Textur + 8 Arithmetik pro Phase</span><span class="sxs-lookup"><span data-stu-id="8aba0-115">6 texture + 8 arithmetic per phase</span></span>                                                                                    |
| <span data-ttu-id="8aba0-116">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8aba0-116">ps\_2\_0</span></span> | <span data-ttu-id="8aba0-117">32 Textur + 64 Arithmetik</span><span class="sxs-lookup"><span data-stu-id="8aba0-117">32 texture + 64 arithmetic</span></span>                                                                                            |
| <span data-ttu-id="8aba0-118">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8aba0-118">ps\_2\_x</span></span> | <span data-ttu-id="8aba0-119">96 (minimal) und bis zur Anzahl der Slots in D3DCAPS9. D3DPSHADERCAPS2 \_ 0. numinstructionslots.</span><span class="sxs-lookup"><span data-stu-id="8aba0-119">96 minimum, and up to the number of slots in D3DCAPS9.D3DPSHADERCAPS2\_0.NumInstructionSlots.</span></span> <span data-ttu-id="8aba0-120">Siehe D3DPSHADERCAPS2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="8aba0-120">See D3DPSHADERCAPS2\_0.</span></span> |
| <span data-ttu-id="8aba0-121">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8aba0-121">ps\_3\_0</span></span> | <span data-ttu-id="8aba0-122">512 (minimal) und bis zur Anzahl der Slots in D3DCAPS9. MaxPixelShader30InstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="8aba0-122">512 minimum, and up to the number of slots in D3DCAPS9.MaxPixelShader30InstructionSlots.</span></span> <span data-ttu-id="8aba0-123">Siehe D3DPSHADERCAPS2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="8aba0-123">See D3DPSHADERCAPS2\_0.</span></span>      |



 

<span data-ttu-id="8aba0-124">Informationen zu den Einschränkungen von Software-Shadern finden Sie unter [Software-Shader](dx9-graphics-reference-asm-software-shaders.md).</span><span class="sxs-lookup"><span data-stu-id="8aba0-124">For information about the limitations of software shaders, see [Software Shaders](dx9-graphics-reference-asm-software-shaders.md).</span></span>

## <a name="flow-control-nesting-limits"></a><span data-ttu-id="8aba0-125">Schachtelungs Limits der Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="8aba0-125">Flow Control Nesting Limits</span></span>

-   <span data-ttu-id="8aba0-126">Siehe [Fluss Steuerungs Einschränkungen](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="8aba0-126">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>

## <a name="ps_1_x-features"></a><span data-ttu-id="8aba0-127">PS \_ 1 \_ x-Funktionen</span><span class="sxs-lookup"><span data-stu-id="8aba0-127">ps\_1\_x Features</span></span>

<span data-ttu-id="8aba0-128">Neue Anweisungen:</span><span class="sxs-lookup"><span data-stu-id="8aba0-128">New instructions:</span></span>

<span data-ttu-id="8aba0-129">Weitere Informationen finden Sie unter [PS 1 \_ \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="8aba0-129">See [ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md).</span></span>

<span data-ttu-id="8aba0-130">Neue Register:</span><span class="sxs-lookup"><span data-stu-id="8aba0-130">New registers:</span></span>

<span data-ttu-id="8aba0-131">Siehe [PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4-Register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="8aba0-131">See [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="ps_2_0-features"></a><span data-ttu-id="8aba0-132">PS \_ 2 \_ 0-Features</span><span class="sxs-lookup"><span data-stu-id="8aba0-132">ps\_2\_0 Features</span></span>

<span data-ttu-id="8aba0-133">Neue Funktionen:</span><span class="sxs-lookup"><span data-stu-id="8aba0-133">New features:</span></span>

-   <span data-ttu-id="8aba0-134">Drei neue "swi. yzxw", ". zxyw", ". wzyx"</span><span class="sxs-lookup"><span data-stu-id="8aba0-134">Three new swizzles - .yzxw, .zxyw, .wzyx</span></span>
-   <span data-ttu-id="8aba0-135">Die Anzahl der [temporären Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) wurde auf 12 angehoben.</span><span class="sxs-lookup"><span data-stu-id="8aba0-135">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) increased to 12</span></span>
-   <span data-ttu-id="8aba0-136">Anzahl [konstanter float-Register](dx9-graphics-reference-asm-ps-registers-constant-float.md) Register (c \# ) auf 32</span><span class="sxs-lookup"><span data-stu-id="8aba0-136">Number of [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md) registers (c\#) increased to 32</span></span>
-   <span data-ttu-id="8aba0-137">Anzahl der [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)s (t \# ) wurde auf 8 angehoben.</span><span class="sxs-lookup"><span data-stu-id="8aba0-137">Number of [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)s (t\#) increased to 8</span></span>

<span data-ttu-id="8aba0-138">Neue Anweisungen:</span><span class="sxs-lookup"><span data-stu-id="8aba0-138">New instructions:</span></span>

-   <span data-ttu-id="8aba0-139">Setup Anweisungen- [DCL-(SM2, SM3-PS ASM)](dcl---ps.md), [DCL \_ samplertype (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)</span><span class="sxs-lookup"><span data-stu-id="8aba0-139">Setup instructions - [dcl - (sm2, sm3 - ps asm)](dcl---ps.md), [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)</span></span>
-   <span data-ttu-id="8aba0-140">Arithmetische Anweisungen- [ABS-PS](abs---ps.md), [CRS-PS](crs---ps.md), [dp2add-PS](dp2add---ps.md), [Exp-PS](exp---ps.md), [FRC-PS](frc---ps.md), [Log-PS](log---ps.md), [m3x2-PS](m3x2---ps.md), [M3x3-PS](m3x3---ps.md), [M3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md), [M4x4-PS](m4x4---ps.md), [Max-PS](max---ps.md), [Min-PS](min---ps.md), [NRM-PS](nrm---ps.md), [Pow-PS](pow---ps.md), [RCP-PS](rcp---ps.md), [RSQ-PS](rsq---ps.md), [SinCos-PS](sincos---ps.md)</span><span class="sxs-lookup"><span data-stu-id="8aba0-140">Arithmetic instructions - [abs - ps](abs---ps.md), [crs - ps](crs---ps.md), [dp2add - ps](dp2add---ps.md), [exp - ps](exp---ps.md), [frc - ps](frc---ps.md), [log - ps](log---ps.md), [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), [m4x4 - ps](m4x4---ps.md), [max - ps](max---ps.md), [min - ps](min---ps.md), [nrm - ps](nrm---ps.md), [pow - ps](pow---ps.md), [rcp - ps](rcp---ps.md), [rsq - ps](rsq---ps.md), [sincos - ps](sincos---ps.md)</span></span>
-   <span data-ttu-id="8aba0-141">Textur Anweisungen- [texld-PS \_ 2 \_ 0 und aufwärts](texld---ps-2-0.md) (unterschiedliche Syntax), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)</span><span class="sxs-lookup"><span data-stu-id="8aba0-141">Texture instructions - [texld - ps\_2\_0 and up](texld---ps-2-0.md) (different syntax), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)</span></span>

<span data-ttu-id="8aba0-142">Neue Register:</span><span class="sxs-lookup"><span data-stu-id="8aba0-142">New registers:</span></span>

-   <span data-ttu-id="8aba0-143">[Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \#</span><span class="sxs-lookup"><span data-stu-id="8aba0-143">[Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#)</span></span>

## <a name="ps_2_x-features"></a><span data-ttu-id="8aba0-144">PS \_ 2 \_ x-Features</span><span class="sxs-lookup"><span data-stu-id="8aba0-144">ps\_2\_x Features</span></span>

<span data-ttu-id="8aba0-145">Neue Features (siehe [**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)):</span><span class="sxs-lookup"><span data-stu-id="8aba0-145">New features (See [**D3DPSHADERCAPS2\_0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).):</span></span>

-   <span data-ttu-id="8aba0-146">Dynamische Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="8aba0-146">Dynamic flow control</span></span>
-   <span data-ttu-id="8aba0-147">Statische Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="8aba0-147">Static flow control</span></span>
-   <span data-ttu-id="8aba0-148">Schachtelung für dynamische und statische Fluss Steuerungs Anweisungen</span><span class="sxs-lookup"><span data-stu-id="8aba0-148">Nesting for dynamic and static flow control instructions</span></span>
-   <span data-ttu-id="8aba0-149">Anzahl der [temporären Registrierungs](dx9-graphics-reference-asm-ps-registers-temporary.md)-e (r \# )</span><span class="sxs-lookup"><span data-stu-id="8aba0-149">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md)s (r\#) increased</span></span>
-   <span data-ttu-id="8aba0-150">Beliebiger Quellpfad</span><span class="sxs-lookup"><span data-stu-id="8aba0-150">Arbitrary source swizzle</span></span>
-   <span data-ttu-id="8aba0-151">Farbverlaufs Anweisungen</span><span class="sxs-lookup"><span data-stu-id="8aba0-151">Gradient instructions</span></span>
-   <span data-ttu-id="8aba0-152">Prädikation</span><span class="sxs-lookup"><span data-stu-id="8aba0-152">Predication</span></span>
-   <span data-ttu-id="8aba0-153">Keine abhängige Textur Lese Beschränkung</span><span class="sxs-lookup"><span data-stu-id="8aba0-153">No dependent texture read limit</span></span>
-   <span data-ttu-id="8aba0-154">Keine Textur Anweisungs Beschränkung</span><span class="sxs-lookup"><span data-stu-id="8aba0-154">No texture instruction limit</span></span>

<span data-ttu-id="8aba0-155">Neue Anweisungen:</span><span class="sxs-lookup"><span data-stu-id="8aba0-155">New instructions:</span></span>

-   <span data-ttu-id="8aba0-156">Anweisungen zur statischen Fluss Steuerung: [if bool-PS](if-bool---ps.md), [callps](call---ps.md), [callnz bool-PS](callnz-bool---ps.md), [else-PS](else---ps.md), [EndIf-PS](endif---ps.md), [Rep-PS](rep---ps.md), [ENDREP-PS](endrep---ps.md), [Label-PS](label---ps.md), [ret-PS](ret---ps.md)</span><span class="sxs-lookup"><span data-stu-id="8aba0-156">Static flow control instructions - [if bool - ps](if-bool---ps.md), [call - ps](call---ps.md), [callnz bool - ps](callnz-bool---ps.md), [else - ps](else---ps.md), [endif - ps](endif---ps.md), [rep - ps](rep---ps.md), [endrep - ps](endrep---ps.md), [label - ps](label---ps.md), [ret - ps](ret---ps.md)</span></span>
-   <span data-ttu-id="8aba0-157">Dynamische Fluss Steuerungs Anweisungen-unter [brechen](break---ps.md)von [ \_ Comp-PS](break-comp---ps.md), [breakp-PS](break-p---ps.md), [callnz pred-PS](callnz-pred---ps.md), [if \_ Comp-PS](if-comp---ps.md), [if pred-PS](if-pred---ps.md), [SETP \_ Comp-PS](setp-comp---ps.md)</span><span class="sxs-lookup"><span data-stu-id="8aba0-157">Dynamic flow control instructions - [break - ps](break---ps.md), [break\_comp - ps](break-comp---ps.md), [breakp - ps](break-p---ps.md), [callnz pred - ps](callnz-pred---ps.md), [if\_comp - ps](if-comp---ps.md), [if pred - ps](if-pred---ps.md), [setp\_comp - ps](setp-comp---ps.md)</span></span>
-   <span data-ttu-id="8aba0-158">Arithmetische Anweisungen- [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)</span><span class="sxs-lookup"><span data-stu-id="8aba0-158">Arithmetic instructions - [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)</span></span>
-   <span data-ttu-id="8aba0-159">Textur Anweisung- [texldd-PS](texldd---ps.md)</span><span class="sxs-lookup"><span data-stu-id="8aba0-159">Texture instruction - [texldd - ps](texldd---ps.md)</span></span>

<span data-ttu-id="8aba0-160">Neue Register:</span><span class="sxs-lookup"><span data-stu-id="8aba0-160">New registers:</span></span>

-   <span data-ttu-id="8aba0-161">[Prädikat Register](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0)</span><span class="sxs-lookup"><span data-stu-id="8aba0-161">[Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0)</span></span>

## <a name="ps_3_0-features"></a><span data-ttu-id="8aba0-162">Features von PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8aba0-162">ps\_3\_0 Features</span></span>

<span data-ttu-id="8aba0-163">Neue Funktionen:</span><span class="sxs-lookup"><span data-stu-id="8aba0-163">New features:</span></span>

-   <span data-ttu-id="8aba0-164">Konsolidierte 10 [Eingabe Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)s (v \# )</span><span class="sxs-lookup"><span data-stu-id="8aba0-164">Consolidated 10 [Input Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)s (v\#)</span></span>
-   <span data-ttu-id="8aba0-165">Indizierbares [Eingabe Farb Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) mit dem [Schleifen-Counter-Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al)</span><span class="sxs-lookup"><span data-stu-id="8aba0-165">Indexable [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) with the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL)</span></span>
-   <span data-ttu-id="8aba0-166">Anzahl der [temporären Registrierungs](dx9-graphics-reference-asm-ps-registers-temporary.md)-e (r \# ) wurde auf 32 erweitert.</span><span class="sxs-lookup"><span data-stu-id="8aba0-166">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md)s (r\#) increased to 32</span></span>
-   <span data-ttu-id="8aba0-167">Anzahl [konstanter float-Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c \# ) auf 224</span><span class="sxs-lookup"><span data-stu-id="8aba0-167">Number of [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c\#) increased to 224</span></span>

<span data-ttu-id="8aba0-168">Neue Anweisungen:</span><span class="sxs-lookup"><span data-stu-id="8aba0-168">New instructions:</span></span>

-   <span data-ttu-id="8aba0-169">Setup Anweisung- [DCL- \_ Semantik (SM3-PS ASM)](dcl-usage---ps.md)</span><span class="sxs-lookup"><span data-stu-id="8aba0-169">Setup instruction - [dcl\_semantics (sm3 - ps asm)](dcl-usage---ps.md)</span></span>
-   <span data-ttu-id="8aba0-170">Statische Fluss Anweisungen- [Loop-PS](loop---ps.md), [ENDLOOP-PS](endloop---ps.md)</span><span class="sxs-lookup"><span data-stu-id="8aba0-170">Static flow instructions - [loop - ps](loop---ps.md), [endloop - ps](endloop---ps.md)</span></span>
-   <span data-ttu-id="8aba0-171">Arithmetische Anweisung- [SinCos-PS](sincos---ps.md) (neue Syntax)</span><span class="sxs-lookup"><span data-stu-id="8aba0-171">Arithmetic instruction - [sincos - ps](sincos---ps.md) (new syntax)</span></span>
-   <span data-ttu-id="8aba0-172">Textur Anweisung- [texldl-PS](texldl---ps.md)</span><span class="sxs-lookup"><span data-stu-id="8aba0-172">Texture instruction - [texldl - ps](texldl---ps.md)</span></span>

<span data-ttu-id="8aba0-173">Neue Register:</span><span class="sxs-lookup"><span data-stu-id="8aba0-173">New registers:</span></span>

-   <span data-ttu-id="8aba0-174">[Eingabe Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# )</span><span class="sxs-lookup"><span data-stu-id="8aba0-174">[Input Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v\#)</span></span>
-   <span data-ttu-id="8aba0-175">[Positions Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vpos)</span><span class="sxs-lookup"><span data-stu-id="8aba0-175">[Position Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vPos)</span></span>
-   <span data-ttu-id="8aba0-176">[Gesichts Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vface)</span><span class="sxs-lookup"><span data-stu-id="8aba0-176">[Face Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vFace)</span></span>

## <a name="related-topics"></a><span data-ttu-id="8aba0-177">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8aba0-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8aba0-178">Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="8aba0-178">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 