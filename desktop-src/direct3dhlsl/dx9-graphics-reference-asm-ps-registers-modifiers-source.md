---
title: Pixelshader-Quellregistermodifizierer
description: Verwenden Sie Quellregistermodifizierer, um den Aus einem Register gelesenen Wert zu ändern, bevor eine Anweisung ausgeführt wird.
ms.assetid: b45d0919-7878-4184-ad4a-5623aae9d1f1
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a9dd4476dd7a1a885edb2e62a29b5127f5ff0a14
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129677"
---
# <a name="pixel-shader-source-register-modifiers"></a><span data-ttu-id="9e7a0-103">Pixelshader-Quellregistermodifizierer</span><span class="sxs-lookup"><span data-stu-id="9e7a0-103">Pixel Shader Source Register Modifiers</span></span>

<span data-ttu-id="9e7a0-104">Verwenden Sie Quellregistermodifizierer, um den Aus einem Register gelesenen Wert zu ändern, bevor eine Anweisung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-104">Use source register modifiers to change the value read from a register before an instruction runs.</span></span> <span data-ttu-id="9e7a0-105">Der Inhalt eines Quellregisters bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-105">The contents of a source register are left unchanged.</span></span> <span data-ttu-id="9e7a0-106">Modifizierer sind nützlich, um den Bereich der Registerdaten als Vorbereitung für die Anweisung anzupassen.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-106">Modifiers are useful for adjusting the range of register data in preparation for the instruction.</span></span> <span data-ttu-id="9e7a0-107">Eine Reihe von Modifizierern, die als Selektoren bezeichnet werden, kopiert oder repliziert die Daten aus einem einzelnen Kanal (r,g,b,a) in die anderen Kanäle.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-107">A set of modifiers called selectors copies or replicates the data from a single channel (r,g,b,a) into the other channels.</span></span>

## <a name="ps_1_1---ps_1_4"></a><span data-ttu-id="9e7a0-108">ps \_ 1 \_ 1 - ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="9e7a0-108">ps\_1\_1 - ps\_1\_4</span></span>

<span data-ttu-id="9e7a0-109">In dieser Tabelle sind die Versionen aufgeführt, die die einzelnen Modifizierer unterstützen:</span><span class="sxs-lookup"><span data-stu-id="9e7a0-109">This table identifies the versions that support each modifier:</span></span>



| <span data-ttu-id="9e7a0-110">Quellregistermodifizierer</span><span class="sxs-lookup"><span data-stu-id="9e7a0-110">Source register modifiers</span></span>                                                                                    | <span data-ttu-id="9e7a0-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e7a0-111">Syntax</span></span>         | <span data-ttu-id="9e7a0-112">Version 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9e7a0-112">Version 1\_1</span></span> | <span data-ttu-id="9e7a0-113">Version 1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="9e7a0-113">Version 1\_2</span></span>     | <span data-ttu-id="9e7a0-114">Version 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9e7a0-114">Version 1\_3</span></span>     | <span data-ttu-id="9e7a0-115">Version 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="9e7a0-115">Version 1\_4</span></span>     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|
| [<span data-ttu-id="9e7a0-116">Vorurteil</span><span class="sxs-lookup"><span data-stu-id="9e7a0-116">bias</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | <span data-ttu-id="9e7a0-117">\_Registervoreingenommenheit</span><span class="sxs-lookup"><span data-stu-id="9e7a0-117">register\_bias</span></span> | <span data-ttu-id="9e7a0-118">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-118">X</span></span>       | <span data-ttu-id="9e7a0-119">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-119">X</span></span>    | <span data-ttu-id="9e7a0-120">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-120">X</span></span>    | <span data-ttu-id="9e7a0-121">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-121">X</span></span>    |
| [<span data-ttu-id="9e7a0-122">Invertieren</span><span class="sxs-lookup"><span data-stu-id="9e7a0-122">invert</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | <span data-ttu-id="9e7a0-123">1– Registrieren</span><span class="sxs-lookup"><span data-stu-id="9e7a0-123">1 - register</span></span>   | <span data-ttu-id="9e7a0-124">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-124">X</span></span>       | <span data-ttu-id="9e7a0-125">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-125">X</span></span>    | <span data-ttu-id="9e7a0-126">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-126">X</span></span>    | <span data-ttu-id="9e7a0-127">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-127">X</span></span>    |
| [<span data-ttu-id="9e7a0-128">Negieren</span><span class="sxs-lookup"><span data-stu-id="9e7a0-128">negate</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | <span data-ttu-id="9e7a0-129">\- Registrieren</span><span class="sxs-lookup"><span data-stu-id="9e7a0-129">\- register</span></span>    | <span data-ttu-id="9e7a0-130">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-130">X</span></span>       | <span data-ttu-id="9e7a0-131">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-131">X</span></span>    | <span data-ttu-id="9e7a0-132">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-132">X</span></span>    | <span data-ttu-id="9e7a0-133">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-133">X</span></span>    |
| [<span data-ttu-id="9e7a0-134">Skalierung um 2</span><span class="sxs-lookup"><span data-stu-id="9e7a0-134">scale by 2</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | <span data-ttu-id="9e7a0-135">Registrieren \_ von x2</span><span class="sxs-lookup"><span data-stu-id="9e7a0-135">register\_x2</span></span>   |         |      |      | <span data-ttu-id="9e7a0-136">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-136">X</span></span>    |
| [<span data-ttu-id="9e7a0-137">Signierte Skalierung</span><span class="sxs-lookup"><span data-stu-id="9e7a0-137">signed scaling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | <span data-ttu-id="9e7a0-138">register \_ bx2</span><span class="sxs-lookup"><span data-stu-id="9e7a0-138">register\_bx2</span></span>  | <span data-ttu-id="9e7a0-139">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-139">X</span></span>       | <span data-ttu-id="9e7a0-140">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-140">X</span></span>    | <span data-ttu-id="9e7a0-141">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-141">X</span></span>    | <span data-ttu-id="9e7a0-142">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-142">X</span></span>    |
| [<span data-ttu-id="9e7a0-143">Texld- und Texcrd-Modifizierer</span><span class="sxs-lookup"><span data-stu-id="9e7a0-143">texld and texcrd modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | <span data-ttu-id="9e7a0-144">register \_ d\*</span><span class="sxs-lookup"><span data-stu-id="9e7a0-144">register\_d\*</span></span>  | <span data-ttu-id="9e7a0-145">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-145">X</span></span>       | <span data-ttu-id="9e7a0-146">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-146">X</span></span>    | <span data-ttu-id="9e7a0-147">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-147">X</span></span>    | <span data-ttu-id="9e7a0-148">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-148">X</span></span>    |
| [<span data-ttu-id="9e7a0-149">Quellenregister-Swizzling</span><span class="sxs-lookup"><span data-stu-id="9e7a0-149">source register swizzling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | <span data-ttu-id="9e7a0-150">register.xyzw</span><span class="sxs-lookup"><span data-stu-id="9e7a0-150">register.xyzw</span></span>  | <span data-ttu-id="9e7a0-151">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-151">X</span></span>       | <span data-ttu-id="9e7a0-152">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-152">X</span></span>    | <span data-ttu-id="9e7a0-153">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-153">X</span></span>    | <span data-ttu-id="9e7a0-154">X</span><span class="sxs-lookup"><span data-stu-id="9e7a0-154">X</span></span>    |



 

<span data-ttu-id="9e7a0-155">Quellregistermodifizierer können nur für arithmetische Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-155">Source register modifiers can be used only on arithmetic instructions.</span></span> <span data-ttu-id="9e7a0-156">Sie können nicht für Texturadressanweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-156">They cannot be used on texture address instructions.</span></span> <span data-ttu-id="9e7a0-157">Eine Ausnahme bildet der Modifizierer [Scale by 2.](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)</span><span class="sxs-lookup"><span data-stu-id="9e7a0-157">The exception to this is the [scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) modifier.</span></span> <span data-ttu-id="9e7a0-158">Für Version 1 \_ 1 kann die signierte Skalierung für das Quellargument jeder texm-Anweisung verwendet \* werden.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-158">For version 1\_1, signed scale can be used on the source argument of any texm\* instruction.</span></span> <span data-ttu-id="9e7a0-159">Für Version \_ 1 2 oder 1 \_ 3 kann die signierte Skalierung für das Quellargument einer beliebigen Texturadressanweisung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-159">For version 1\_2 or 1\_3, signed scale can be used on the source argument of any texture address instruction.</span></span>

<span data-ttu-id="9e7a0-160">Einige modifiziererspezifische Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="9e7a0-160">Some modifier specific restrictions:</span></span>

-   <span data-ttu-id="9e7a0-161">Negate kann entweder mit dem Modifizierer bias, signed scaling oder scalex2 kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-161">Negate can be combined with either the bias, signed scaling, or scalex2 modifier.</span></span> <span data-ttu-id="9e7a0-162">In kombination wird "negate" zuletzt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-162">When combined, negate is run last.</span></span>
-   <span data-ttu-id="9e7a0-163">Invert kann nicht mit einem anderen Modifizierer kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-163">Invert cannot be combined with any other modifier.</span></span>
-   <span data-ttu-id="9e7a0-164">Invertieren, Negieren, Voreingenommenheit, signierte Skalierung und Scalex2 können mit jedem der Selektoren kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-164">Invert, negate, bias, signed scaling, and scalex2 can be combined with any of the selectors.</span></span>
-   <span data-ttu-id="9e7a0-165">Quellregistermodifizierer sollten nicht für Konstantenregister verwendet werden, da sie nicht definierte Ergebnisse verursachen.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-165">Source register modifiers should not be used on constant registers because they will cause undefined results.</span></span> <span data-ttu-id="9e7a0-166">Für Version 1 \_ 4 sind Modifizierer für Konstanten nicht zulässig und schlagen bei der Überprüfung fehl.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-166">For version 1\_4, modifiers on constants are not allowed and will fail validation.</span></span>

## <a name="ps_2_0-and-above"></a><span data-ttu-id="9e7a0-167">ps \_ 2 \_ 0 und höher</span><span class="sxs-lookup"><span data-stu-id="9e7a0-167">ps\_2\_0 and Above</span></span>

<span data-ttu-id="9e7a0-168">Für Version ps \_ 2 \_ 0 und höher wurde die Anzahl der Modifizierer vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-168">For version ps\_2\_0 and up, the number of modifiers has been simplified.</span></span>

### <a name="negate"></a><span data-ttu-id="9e7a0-169">Negate</span><span class="sxs-lookup"><span data-stu-id="9e7a0-169">Negate</span></span>

<span data-ttu-id="9e7a0-170">Negieren Sie den Inhalt des Quellregisters.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-170">Negate the contents of the source register.</span></span>



| <span data-ttu-id="9e7a0-171">Komponentenmodifizierer</span><span class="sxs-lookup"><span data-stu-id="9e7a0-171">Component modifier</span></span> | <span data-ttu-id="9e7a0-172">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e7a0-172">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="9e7a0-173">\- R</span><span class="sxs-lookup"><span data-stu-id="9e7a0-173">\- r</span></span>               | <span data-ttu-id="9e7a0-174">Quelln negation</span><span class="sxs-lookup"><span data-stu-id="9e7a0-174">Source negation</span></span> |



 

<span data-ttu-id="9e7a0-175">Der Modifizierer negate kann nicht im zweiten Quellregister dieser Anweisungen verwendet werden: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md)und [m4x4 - ps](m4x4---ps.md).</span><span class="sxs-lookup"><span data-stu-id="9e7a0-175">The negate modifier cannot be used on second source register of these instructions: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), and [m4x4 - ps](m4x4---ps.md).</span></span>



| <span data-ttu-id="9e7a0-176">Pixelshaderversionen</span><span class="sxs-lookup"><span data-stu-id="9e7a0-176">Pixel shader versions</span></span> | <span data-ttu-id="9e7a0-177">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9e7a0-177">2\_0</span></span> | <span data-ttu-id="9e7a0-178">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9e7a0-178">2\_x</span></span> | <span data-ttu-id="9e7a0-179">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="9e7a0-179">2\_sw</span></span> | <span data-ttu-id="9e7a0-180">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9e7a0-180">3\_0</span></span> | <span data-ttu-id="9e7a0-181">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="9e7a0-181">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| \-                    | <span data-ttu-id="9e7a0-182">x</span><span class="sxs-lookup"><span data-stu-id="9e7a0-182">x</span></span>    | <span data-ttu-id="9e7a0-183">x</span><span class="sxs-lookup"><span data-stu-id="9e7a0-183">x</span></span>    | <span data-ttu-id="9e7a0-184">x</span><span class="sxs-lookup"><span data-stu-id="9e7a0-184">x</span></span>     | <span data-ttu-id="9e7a0-185">x</span><span class="sxs-lookup"><span data-stu-id="9e7a0-185">x</span></span>    | <span data-ttu-id="9e7a0-186">x</span><span class="sxs-lookup"><span data-stu-id="9e7a0-186">x</span></span>     |



 

### <a name="absolute-value"></a><span data-ttu-id="9e7a0-187">Absoluter Wert</span><span class="sxs-lookup"><span data-stu-id="9e7a0-187">Absolute Value</span></span>

<span data-ttu-id="9e7a0-188">Nehmen Sie den absoluten Wert des Registers.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-188">Take the absolute value of the register.</span></span>



| <span data-ttu-id="9e7a0-189">Pixelshaderversionen</span><span class="sxs-lookup"><span data-stu-id="9e7a0-189">Pixel shader versions</span></span> | <span data-ttu-id="9e7a0-190">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9e7a0-190">2\_0</span></span> | <span data-ttu-id="9e7a0-191">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9e7a0-191">2\_x</span></span> | <span data-ttu-id="9e7a0-192">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="9e7a0-192">2\_sw</span></span> | <span data-ttu-id="9e7a0-193">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9e7a0-193">3\_0</span></span> | <span data-ttu-id="9e7a0-194">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="9e7a0-194">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| <span data-ttu-id="9e7a0-195">abs</span><span class="sxs-lookup"><span data-stu-id="9e7a0-195">abs</span></span>                   |      |      |       | <span data-ttu-id="9e7a0-196">x</span><span class="sxs-lookup"><span data-stu-id="9e7a0-196">x</span></span>    | <span data-ttu-id="9e7a0-197">x</span><span class="sxs-lookup"><span data-stu-id="9e7a0-197">x</span></span>     |



 

<span data-ttu-id="9e7a0-198">Wenn ein Shader der Version 3 aus einem oder mehreren konstanten float-Registern (c) liest, \# muss eines der folgenden Punkte zutreffen.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-198">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="9e7a0-199">Alle konstanten Gleitkommaregister müssen den Abs-Modifizierer verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-199">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="9e7a0-200">Keiner der konstanten Gleitkommaregister kann den Abs-Modifizierer verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e7a0-200">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e7a0-201">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9e7a0-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e7a0-202">Registermodifizierer für Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="9e7a0-202">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




