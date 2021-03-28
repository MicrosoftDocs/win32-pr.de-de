---
title: Pixel-Shader-quellregistrierungs Modifizierern
description: Verwenden Sie die quellregistrierungs modifiziererer, um den Wert zu ändern, der aus einem Register gelesen wird, bevor eine Anweisung
ms.assetid: b45d0919-7878-4184-ad4a-5623aae9d1f1
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 12cfee533a71408a445d97a63bbd8b76b281236b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311490"
---
# <a name="pixel-shader-source-register-modifiers"></a><span data-ttu-id="94b67-103">Pixel-Shader-quellregistrierungs Modifizierern</span><span class="sxs-lookup"><span data-stu-id="94b67-103">Pixel Shader Source Register Modifiers</span></span>

<span data-ttu-id="94b67-104">Verwenden Sie die quellregistrierungs modifiziererer, um den Wert zu ändern, der aus einem Register gelesen wird, bevor eine Anweisung</span><span class="sxs-lookup"><span data-stu-id="94b67-104">Use source register modifiers to change the value read from a register before an instruction runs.</span></span> <span data-ttu-id="94b67-105">Der Inhalt eines Quell Registers bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="94b67-105">The contents of a source register are left unchanged.</span></span> <span data-ttu-id="94b67-106">Modifizierer sind nützlich, um den Bereich der Register Daten zur Vorbereitung der Anweisung anzupassen.</span><span class="sxs-lookup"><span data-stu-id="94b67-106">Modifiers are useful for adjusting the range of register data in preparation for the instruction.</span></span> <span data-ttu-id="94b67-107">Ein Satz von Modifizierern, die als Selektoren bezeichnet werden, kopiert oder repliziert die Daten von einem einzelnen Kanal (r, g, b, a) in die anderen Kanäle.</span><span class="sxs-lookup"><span data-stu-id="94b67-107">A set of modifiers called selectors copies or replicates the data from a single channel (r,g,b,a) into the other channels.</span></span>

## <a name="ps_1_1---ps_1_4"></a><span data-ttu-id="94b67-108">PS \_ 1 \_ 1-PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="94b67-108">ps\_1\_1 - ps\_1\_4</span></span>

<span data-ttu-id="94b67-109">Diese Tabelle identifiziert die Versionen, die die einzelnen Modifizierer unterstützen:</span><span class="sxs-lookup"><span data-stu-id="94b67-109">This table identifies the versions that support each modifier:</span></span>



| <span data-ttu-id="94b67-110">Quellregistrierungs modifiziererer</span><span class="sxs-lookup"><span data-stu-id="94b67-110">Source register modifiers</span></span>                                                                                    | <span data-ttu-id="94b67-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="94b67-111">Syntax</span></span>         | <span data-ttu-id="94b67-112">Version</span><span class="sxs-lookup"><span data-stu-id="94b67-112">Version</span></span> |      |      |      |     |     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|-----|-----|
|                                                                                                              |                | <span data-ttu-id="94b67-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="94b67-113">1\_1</span></span>    | <span data-ttu-id="94b67-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="94b67-114">1\_2</span></span> | <span data-ttu-id="94b67-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="94b67-115">1\_3</span></span> | <span data-ttu-id="94b67-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="94b67-116">1\_4</span></span> |     |     |
| [<span data-ttu-id="94b67-117">eingenommen</span><span class="sxs-lookup"><span data-stu-id="94b67-117">bias</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | <span data-ttu-id="94b67-118">\_Befangenheit registrieren</span><span class="sxs-lookup"><span data-stu-id="94b67-118">register\_bias</span></span> | <span data-ttu-id="94b67-119">X</span><span class="sxs-lookup"><span data-stu-id="94b67-119">X</span></span>       | <span data-ttu-id="94b67-120">X</span><span class="sxs-lookup"><span data-stu-id="94b67-120">X</span></span>    | <span data-ttu-id="94b67-121">X</span><span class="sxs-lookup"><span data-stu-id="94b67-121">X</span></span>    | <span data-ttu-id="94b67-122">X</span><span class="sxs-lookup"><span data-stu-id="94b67-122">X</span></span>    |     |     |
| [<span data-ttu-id="94b67-123">umkehren</span><span class="sxs-lookup"><span data-stu-id="94b67-123">invert</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | <span data-ttu-id="94b67-124">1: registrieren</span><span class="sxs-lookup"><span data-stu-id="94b67-124">1 - register</span></span>   | <span data-ttu-id="94b67-125">X</span><span class="sxs-lookup"><span data-stu-id="94b67-125">X</span></span>       | <span data-ttu-id="94b67-126">X</span><span class="sxs-lookup"><span data-stu-id="94b67-126">X</span></span>    | <span data-ttu-id="94b67-127">X</span><span class="sxs-lookup"><span data-stu-id="94b67-127">X</span></span>    | <span data-ttu-id="94b67-128">X</span><span class="sxs-lookup"><span data-stu-id="94b67-128">X</span></span>    |     |     |
| [<span data-ttu-id="94b67-129">negate</span><span class="sxs-lookup"><span data-stu-id="94b67-129">negate</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | <span data-ttu-id="94b67-130">\- sich</span><span class="sxs-lookup"><span data-stu-id="94b67-130">\- register</span></span>    | <span data-ttu-id="94b67-131">X</span><span class="sxs-lookup"><span data-stu-id="94b67-131">X</span></span>       | <span data-ttu-id="94b67-132">X</span><span class="sxs-lookup"><span data-stu-id="94b67-132">X</span></span>    | <span data-ttu-id="94b67-133">X</span><span class="sxs-lookup"><span data-stu-id="94b67-133">X</span></span>    | <span data-ttu-id="94b67-134">X</span><span class="sxs-lookup"><span data-stu-id="94b67-134">X</span></span>    |     |     |
| [<span data-ttu-id="94b67-135">Skalieren um 2</span><span class="sxs-lookup"><span data-stu-id="94b67-135">scale by 2</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | <span data-ttu-id="94b67-136">Registrieren von \_ x2</span><span class="sxs-lookup"><span data-stu-id="94b67-136">register\_x2</span></span>   |         |      |      | <span data-ttu-id="94b67-137">X</span><span class="sxs-lookup"><span data-stu-id="94b67-137">X</span></span>    |     |     |
| [<span data-ttu-id="94b67-138">signierte Skalierung</span><span class="sxs-lookup"><span data-stu-id="94b67-138">signed scaling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | <span data-ttu-id="94b67-139">\_bx2 registrieren</span><span class="sxs-lookup"><span data-stu-id="94b67-139">register\_bx2</span></span>  | <span data-ttu-id="94b67-140">X</span><span class="sxs-lookup"><span data-stu-id="94b67-140">X</span></span>       | <span data-ttu-id="94b67-141">X</span><span class="sxs-lookup"><span data-stu-id="94b67-141">X</span></span>    | <span data-ttu-id="94b67-142">X</span><span class="sxs-lookup"><span data-stu-id="94b67-142">X</span></span>    | <span data-ttu-id="94b67-143">X</span><span class="sxs-lookup"><span data-stu-id="94b67-143">X</span></span>    |     |     |
| [<span data-ttu-id="94b67-144">texld-und texcrd-Modifizierer</span><span class="sxs-lookup"><span data-stu-id="94b67-144">texld and texcrd modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | <span data-ttu-id="94b67-145">Registrieren von \_ d\*</span><span class="sxs-lookup"><span data-stu-id="94b67-145">register\_d\*</span></span>  | <span data-ttu-id="94b67-146">X</span><span class="sxs-lookup"><span data-stu-id="94b67-146">X</span></span>       | <span data-ttu-id="94b67-147">X</span><span class="sxs-lookup"><span data-stu-id="94b67-147">X</span></span>    | <span data-ttu-id="94b67-148">X</span><span class="sxs-lookup"><span data-stu-id="94b67-148">X</span></span>    | <span data-ttu-id="94b67-149">X</span><span class="sxs-lookup"><span data-stu-id="94b67-149">X</span></span>    |     |     |
| [<span data-ttu-id="94b67-150">Quellen Register (swizzelnder)</span><span class="sxs-lookup"><span data-stu-id="94b67-150">source register swizzling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | <span data-ttu-id="94b67-151">Register. xyzw</span><span class="sxs-lookup"><span data-stu-id="94b67-151">register.xyzw</span></span>  | <span data-ttu-id="94b67-152">X</span><span class="sxs-lookup"><span data-stu-id="94b67-152">X</span></span>       | <span data-ttu-id="94b67-153">X</span><span class="sxs-lookup"><span data-stu-id="94b67-153">X</span></span>    | <span data-ttu-id="94b67-154">X</span><span class="sxs-lookup"><span data-stu-id="94b67-154">X</span></span>    | <span data-ttu-id="94b67-155">X</span><span class="sxs-lookup"><span data-stu-id="94b67-155">X</span></span>    |     |     |



 

<span data-ttu-id="94b67-156">Modifizierermodifiziererer für die Quelle können nur in arithmetischen Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94b67-156">Source register modifiers can be used only on arithmetic instructions.</span></span> <span data-ttu-id="94b67-157">Sie können nicht für Textur Adress Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94b67-157">They cannot be used on texture address instructions.</span></span> <span data-ttu-id="94b67-158">Eine Ausnahme bildet der " [Scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) "-Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="94b67-158">The exception to this is the [scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) modifier.</span></span> <span data-ttu-id="94b67-159">Bei Version 1 \_ 1 kann die signierte Skala für das Quell Argument einer beliebigen texm- \* Anweisung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94b67-159">For version 1\_1, signed scale can be used on the source argument of any texm\* instruction.</span></span> <span data-ttu-id="94b67-160">Bei Version 1 \_ 2 oder 1 \_ 3 kann die signierte Skala für das Quell Argument einer beliebigen Textur Adress Anweisung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94b67-160">For version 1\_2 or 1\_3, signed scale can be used on the source argument of any texture address instruction.</span></span>

<span data-ttu-id="94b67-161">Bestimmte Einschränkungen für den Modifizierer:</span><span class="sxs-lookup"><span data-stu-id="94b67-161">Some modifier specific restrictions:</span></span>

-   <span data-ttu-id="94b67-162">Negate können entweder mit dem-Modifizierer "Bias", "signed Scaling" oder "scalex2" kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="94b67-162">Negate can be combined with either the bias, signed scaling, or scalex2 modifier.</span></span> <span data-ttu-id="94b67-163">Wenn Sie kombiniert werden, wird Negation zuletzt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94b67-163">When combined, negate is run last.</span></span>
-   <span data-ttu-id="94b67-164">Invert kann nicht mit einem anderen Modifizierer kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="94b67-164">Invert cannot be combined with any other modifier.</span></span>
-   <span data-ttu-id="94b67-165">Invert, Negate, Bias, signierte Skalierung und scalex2 können mit jedem der Selektoren kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="94b67-165">Invert, negate, bias, signed scaling, and scalex2 can be combined with any of the selectors.</span></span>
-   <span data-ttu-id="94b67-166">Modifizierermodifiziererer für die Quelle dürfen nicht in konstanten Registern verwendet werden, da Sie zu nicht definierten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="94b67-166">Source register modifiers should not be used on constant registers because they will cause undefined results.</span></span> <span data-ttu-id="94b67-167">Bei Version 1 \_ 4 sind modifiziererer für Konstanten nicht zulässig, und die Überprüfung wird fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="94b67-167">For version 1\_4, modifiers on constants are not allowed and will fail validation.</span></span>

## <a name="ps_2_0-and-above"></a><span data-ttu-id="94b67-168">PS \_ 2 \_ 0 und höher</span><span class="sxs-lookup"><span data-stu-id="94b67-168">ps\_2\_0 and Above</span></span>

<span data-ttu-id="94b67-169">Bei Version PS \_ 2 \_ 0 und höher wurde die Anzahl der modifiziererer vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="94b67-169">For version ps\_2\_0 and up, the number of modifiers has been simplified.</span></span>

### <a name="negate"></a><span data-ttu-id="94b67-170">Negate</span><span class="sxs-lookup"><span data-stu-id="94b67-170">Negate</span></span>

<span data-ttu-id="94b67-171">Negieren Sie den Inhalt des Quell Registers.</span><span class="sxs-lookup"><span data-stu-id="94b67-171">Negate the contents of the source register.</span></span>



| <span data-ttu-id="94b67-172">Komponentenmodifizierer</span><span class="sxs-lookup"><span data-stu-id="94b67-172">Component modifier</span></span> | <span data-ttu-id="94b67-173">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94b67-173">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="94b67-174">\- r</span><span class="sxs-lookup"><span data-stu-id="94b67-174">\- r</span></span>               | <span data-ttu-id="94b67-175">Quell Negation</span><span class="sxs-lookup"><span data-stu-id="94b67-175">Source negation</span></span> |



 

<span data-ttu-id="94b67-176">Der Negation-Modifizierer kann nicht für das zweite Quell Register dieser Anweisungen verwendet werden: [m3x2-PS](m3x2---ps.md), [M3x3-PS](m3x3---ps.md), [M3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md)und [M4x4-PS](m4x4---ps.md).</span><span class="sxs-lookup"><span data-stu-id="94b67-176">The negate modifier cannot be used on second source register of these instructions: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), and [m4x4 - ps](m4x4---ps.md).</span></span>



| <span data-ttu-id="94b67-177">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="94b67-177">Pixel shader versions</span></span> | <span data-ttu-id="94b67-178">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="94b67-178">2\_0</span></span> | <span data-ttu-id="94b67-179">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="94b67-179">2\_x</span></span> | <span data-ttu-id="94b67-180">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="94b67-180">2\_sw</span></span> | <span data-ttu-id="94b67-181">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="94b67-181">3\_0</span></span> | <span data-ttu-id="94b67-182">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="94b67-182">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| \-                    | <span data-ttu-id="94b67-183">x</span><span class="sxs-lookup"><span data-stu-id="94b67-183">x</span></span>    | <span data-ttu-id="94b67-184">x</span><span class="sxs-lookup"><span data-stu-id="94b67-184">x</span></span>    | <span data-ttu-id="94b67-185">x</span><span class="sxs-lookup"><span data-stu-id="94b67-185">x</span></span>     | <span data-ttu-id="94b67-186">x</span><span class="sxs-lookup"><span data-stu-id="94b67-186">x</span></span>    | <span data-ttu-id="94b67-187">x</span><span class="sxs-lookup"><span data-stu-id="94b67-187">x</span></span>     |



 

### <a name="absolute-value"></a><span data-ttu-id="94b67-188">Absoluter Wert</span><span class="sxs-lookup"><span data-stu-id="94b67-188">Absolute Value</span></span>

<span data-ttu-id="94b67-189">Nehmen Sie den absoluten Wert des Register.</span><span class="sxs-lookup"><span data-stu-id="94b67-189">Take the absolute value of the register.</span></span>



| <span data-ttu-id="94b67-190">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="94b67-190">Pixel shader versions</span></span> | <span data-ttu-id="94b67-191">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="94b67-191">2\_0</span></span> | <span data-ttu-id="94b67-192">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="94b67-192">2\_x</span></span> | <span data-ttu-id="94b67-193">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="94b67-193">2\_sw</span></span> | <span data-ttu-id="94b67-194">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="94b67-194">3\_0</span></span> | <span data-ttu-id="94b67-195">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="94b67-195">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| <span data-ttu-id="94b67-196">abs</span><span class="sxs-lookup"><span data-stu-id="94b67-196">abs</span></span>                   |      |      |       | <span data-ttu-id="94b67-197">x</span><span class="sxs-lookup"><span data-stu-id="94b67-197">x</span></span>    | <span data-ttu-id="94b67-198">x</span><span class="sxs-lookup"><span data-stu-id="94b67-198">x</span></span>     |



 

<span data-ttu-id="94b67-199">Wenn ein Shader der Version 3 aus mindestens einem konstanten float-Register (c \# ) liest, muss einer der folgenden Werte zutreffen.</span><span class="sxs-lookup"><span data-stu-id="94b67-199">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="94b67-200">Alle Konstanten Gleit Komma Register müssen den ABS-Modifizierer verwenden.</span><span class="sxs-lookup"><span data-stu-id="94b67-200">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="94b67-201">Keines der Konstanten Gleit Komma Register kann den ABS-Modifizierer verwenden.</span><span class="sxs-lookup"><span data-stu-id="94b67-201">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94b67-202">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="94b67-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94b67-203">Pixelshadermodifizierern</span><span class="sxs-lookup"><span data-stu-id="94b67-203">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




