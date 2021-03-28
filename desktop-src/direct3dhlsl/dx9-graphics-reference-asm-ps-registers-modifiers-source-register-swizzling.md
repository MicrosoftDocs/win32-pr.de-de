---
title: Quellen Register (swizzelnder) (HLSL PS-Referenz)
description: Swizzling bezieht sich auf die Möglichkeit, beliebige Quell Registrierungs Komponenten in beliebige temporäre Register Komponenten zu kopieren. Das Schwenken wirkt sich nicht auf die Quell Registrierungsdaten aus. Bevor eine Anweisung ausgeführt wird, werden die Daten in einem Quell Register in ein temporäres Register kopiert.
ms.assetid: 27aee6a8-5185-4236-b3e4-44addf230c34
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ffc655129740f112a3ade9eb40c0bbe29dfc1fb
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313793"
---
# <a name="source-register-swizzling-hlsl-ps-reference"></a><span data-ttu-id="da621-105">Quellen Register (swizzelnder) (HLSL PS-Referenz)</span><span class="sxs-lookup"><span data-stu-id="da621-105">Source register swizzling (HLSL PS reference)</span></span>

<span data-ttu-id="da621-106">Swizzling bezieht sich auf die Möglichkeit, beliebige Quell Registrierungs Komponenten in beliebige temporäre Register Komponenten zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="da621-106">Swizzling refers to the ability to copy any source register component to any temporary register component.</span></span> <span data-ttu-id="da621-107">Das Schwenken wirkt sich nicht auf die Quell Registrierungsdaten aus.</span><span class="sxs-lookup"><span data-stu-id="da621-107">Swizzling does not affect the source register data.</span></span> <span data-ttu-id="da621-108">Bevor eine Anweisung ausgeführt wird, werden die Daten in einem Quell Register in ein temporäres Register kopiert.</span><span class="sxs-lookup"><span data-stu-id="da621-108">Before an instruction runs, the data in a source register is copied to a temporary register.</span></span>

## <a name="source-swizzling"></a><span data-ttu-id="da621-109">Quellen Schwimmen</span><span class="sxs-lookup"><span data-stu-id="da621-109">Source Swizzling</span></span>

<span data-ttu-id="da621-110">Quell-wischen ermöglicht es einer einzelnen Komponente eines Quell Registers, den Wert einer der vier Komponenten des gleichen Quell Registers zu übernehmen, bevor das Register für die Berechnung gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="da621-110">Source swizzle allows individual component of a source register to take on the value of any of the four components of the same source register before the register is read for computation.</span></span>

<span data-ttu-id="da621-111">Beispielsweise bedeutet das. zxxy-Swizzle:</span><span class="sxs-lookup"><span data-stu-id="da621-111">For example, the .zxxy swizzle means:</span></span>

-   <span data-ttu-id="da621-112">. x-Komponente übernimmt den Wert der. z-Komponente.</span><span class="sxs-lookup"><span data-stu-id="da621-112">.x component will take on the value of .z component</span></span>
-   <span data-ttu-id="da621-113">. y-Komponente übernimmt den Wert der x-Komponente.</span><span class="sxs-lookup"><span data-stu-id="da621-113">.y component will take on the value of .x component</span></span>
-   <span data-ttu-id="da621-114">. z-Komponente übernimmt den Wert der x-Komponente.</span><span class="sxs-lookup"><span data-stu-id="da621-114">.z component will take on the value of .x component</span></span>
-   <span data-ttu-id="da621-115">. w-Komponente übernimmt den Wert der. y-Komponente.</span><span class="sxs-lookup"><span data-stu-id="da621-115">.w component will take on the value of .y component</span></span>

<span data-ttu-id="da621-116">Die Komponenten können in beliebiger Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="da621-116">The components can appear in any order.</span></span> <span data-ttu-id="da621-117">Wenn weniger als vier Komponenten angegeben werden, wird die letzte Komponente wiederholt.</span><span class="sxs-lookup"><span data-stu-id="da621-117">If fewer than four components are specified, the last component is repeated.</span></span> <span data-ttu-id="da621-118">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="da621-118">For example:</span></span>


```
.xy  = .xyyy
.wzx = .wzxx
.z   = .zzzz
```



<span data-ttu-id="da621-119">Wenn keine Komponente angegeben ist, wird kein schwenken angewendet.</span><span class="sxs-lookup"><span data-stu-id="da621-119">If no component is specified, no swizzling is applied.</span></span>

<span data-ttu-id="da621-120">Einige Anweisungen weisen Einschränkungen für den Quellpfad auf.</span><span class="sxs-lookup"><span data-stu-id="da621-120">Some instructions have restrictions for source swizzle.</span></span> <span data-ttu-id="da621-121">Sie sind auf den Referenzseiten der angesehenen Anweisung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="da621-121">They are listed in the respected instruction reference pages.</span></span>



| <span data-ttu-id="da621-122">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="da621-122">Pixel shader versions</span></span> | <span data-ttu-id="da621-123">1\_1</span><span class="sxs-lookup"><span data-stu-id="da621-123">1\_1</span></span> | <span data-ttu-id="da621-124">1\_2</span><span class="sxs-lookup"><span data-stu-id="da621-124">1\_2</span></span> | <span data-ttu-id="da621-125">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="da621-125">1\_3</span></span> | <span data-ttu-id="da621-126">1\_4</span><span class="sxs-lookup"><span data-stu-id="da621-126">1\_4</span></span> | <span data-ttu-id="da621-127">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="da621-127">2\_0</span></span> | <span data-ttu-id="da621-128">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="da621-128">2\_x</span></span> | <span data-ttu-id="da621-129">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="da621-129">2\_sw</span></span> | <span data-ttu-id="da621-130">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="da621-130">3\_0</span></span> | <span data-ttu-id="da621-131">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="da621-131">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="da621-132">.x</span><span class="sxs-lookup"><span data-stu-id="da621-132">.x</span></span>                    |      |      |      | <span data-ttu-id="da621-133">x</span><span class="sxs-lookup"><span data-stu-id="da621-133">x</span></span>    | <span data-ttu-id="da621-134">x</span><span class="sxs-lookup"><span data-stu-id="da621-134">x</span></span>    | <span data-ttu-id="da621-135">x</span><span class="sxs-lookup"><span data-stu-id="da621-135">x</span></span>    | <span data-ttu-id="da621-136">x</span><span class="sxs-lookup"><span data-stu-id="da621-136">x</span></span>     | <span data-ttu-id="da621-137">x</span><span class="sxs-lookup"><span data-stu-id="da621-137">x</span></span>    | <span data-ttu-id="da621-138">x</span><span class="sxs-lookup"><span data-stu-id="da621-138">x</span></span>     |
| <span data-ttu-id="da621-139">. y</span><span class="sxs-lookup"><span data-stu-id="da621-139">.y</span></span>                    |      |      |      | <span data-ttu-id="da621-140">x</span><span class="sxs-lookup"><span data-stu-id="da621-140">x</span></span>    | <span data-ttu-id="da621-141">x</span><span class="sxs-lookup"><span data-stu-id="da621-141">x</span></span>    | <span data-ttu-id="da621-142">x</span><span class="sxs-lookup"><span data-stu-id="da621-142">x</span></span>    | <span data-ttu-id="da621-143">x</span><span class="sxs-lookup"><span data-stu-id="da621-143">x</span></span>     | <span data-ttu-id="da621-144">x</span><span class="sxs-lookup"><span data-stu-id="da621-144">x</span></span>    | <span data-ttu-id="da621-145">x</span><span class="sxs-lookup"><span data-stu-id="da621-145">x</span></span>     |
| <span data-ttu-id="da621-146">. z</span><span class="sxs-lookup"><span data-stu-id="da621-146">.z</span></span>                    | <span data-ttu-id="da621-147">x\*</span><span class="sxs-lookup"><span data-stu-id="da621-147">x\*</span></span>  | <span data-ttu-id="da621-148">x\*</span><span class="sxs-lookup"><span data-stu-id="da621-148">x\*</span></span>  | <span data-ttu-id="da621-149">x\*</span><span class="sxs-lookup"><span data-stu-id="da621-149">x\*</span></span>  | <span data-ttu-id="da621-150">x</span><span class="sxs-lookup"><span data-stu-id="da621-150">x</span></span>    | <span data-ttu-id="da621-151">x</span><span class="sxs-lookup"><span data-stu-id="da621-151">x</span></span>    | <span data-ttu-id="da621-152">x</span><span class="sxs-lookup"><span data-stu-id="da621-152">x</span></span>    | <span data-ttu-id="da621-153">x</span><span class="sxs-lookup"><span data-stu-id="da621-153">x</span></span>     | <span data-ttu-id="da621-154">x</span><span class="sxs-lookup"><span data-stu-id="da621-154">x</span></span>    | <span data-ttu-id="da621-155">x</span><span class="sxs-lookup"><span data-stu-id="da621-155">x</span></span>     |
| <span data-ttu-id="da621-156">. w</span><span class="sxs-lookup"><span data-stu-id="da621-156">.w</span></span>                    | <span data-ttu-id="da621-157">x</span><span class="sxs-lookup"><span data-stu-id="da621-157">x</span></span>    | <span data-ttu-id="da621-158">x</span><span class="sxs-lookup"><span data-stu-id="da621-158">x</span></span>    | <span data-ttu-id="da621-159">x</span><span class="sxs-lookup"><span data-stu-id="da621-159">x</span></span>    | <span data-ttu-id="da621-160">x</span><span class="sxs-lookup"><span data-stu-id="da621-160">x</span></span>    | <span data-ttu-id="da621-161">x</span><span class="sxs-lookup"><span data-stu-id="da621-161">x</span></span>    | <span data-ttu-id="da621-162">x</span><span class="sxs-lookup"><span data-stu-id="da621-162">x</span></span>    | <span data-ttu-id="da621-163">x</span><span class="sxs-lookup"><span data-stu-id="da621-163">x</span></span>     | <span data-ttu-id="da621-164">x</span><span class="sxs-lookup"><span data-stu-id="da621-164">x</span></span>    | <span data-ttu-id="da621-165">x</span><span class="sxs-lookup"><span data-stu-id="da621-165">x</span></span>     |
| <span data-ttu-id="da621-166">. xyzw (Standard)</span><span class="sxs-lookup"><span data-stu-id="da621-166">.xyzw (default)</span></span>       | <span data-ttu-id="da621-167">x</span><span class="sxs-lookup"><span data-stu-id="da621-167">x</span></span>    | <span data-ttu-id="da621-168">x</span><span class="sxs-lookup"><span data-stu-id="da621-168">x</span></span>    | <span data-ttu-id="da621-169">x</span><span class="sxs-lookup"><span data-stu-id="da621-169">x</span></span>    | <span data-ttu-id="da621-170">x</span><span class="sxs-lookup"><span data-stu-id="da621-170">x</span></span>    | <span data-ttu-id="da621-171">x</span><span class="sxs-lookup"><span data-stu-id="da621-171">x</span></span>    | <span data-ttu-id="da621-172">x</span><span class="sxs-lookup"><span data-stu-id="da621-172">x</span></span>    | <span data-ttu-id="da621-173">x</span><span class="sxs-lookup"><span data-stu-id="da621-173">x</span></span>     | <span data-ttu-id="da621-174">x</span><span class="sxs-lookup"><span data-stu-id="da621-174">x</span></span>    | <span data-ttu-id="da621-175">x</span><span class="sxs-lookup"><span data-stu-id="da621-175">x</span></span>     |
| <span data-ttu-id="da621-176">. yzxw</span><span class="sxs-lookup"><span data-stu-id="da621-176">.yzxw</span></span>                 |      |      |      |      | <span data-ttu-id="da621-177">x</span><span class="sxs-lookup"><span data-stu-id="da621-177">x</span></span>    | <span data-ttu-id="da621-178">x</span><span class="sxs-lookup"><span data-stu-id="da621-178">x</span></span>    | <span data-ttu-id="da621-179">x</span><span class="sxs-lookup"><span data-stu-id="da621-179">x</span></span>     | <span data-ttu-id="da621-180">x</span><span class="sxs-lookup"><span data-stu-id="da621-180">x</span></span>    | <span data-ttu-id="da621-181">x</span><span class="sxs-lookup"><span data-stu-id="da621-181">x</span></span>     |
| <span data-ttu-id="da621-182">. zxyw</span><span class="sxs-lookup"><span data-stu-id="da621-182">.zxyw</span></span>                 |      |      |      |      | <span data-ttu-id="da621-183">x</span><span class="sxs-lookup"><span data-stu-id="da621-183">x</span></span>    | <span data-ttu-id="da621-184">x</span><span class="sxs-lookup"><span data-stu-id="da621-184">x</span></span>    | <span data-ttu-id="da621-185">x</span><span class="sxs-lookup"><span data-stu-id="da621-185">x</span></span>     | <span data-ttu-id="da621-186">x</span><span class="sxs-lookup"><span data-stu-id="da621-186">x</span></span>    | <span data-ttu-id="da621-187">x</span><span class="sxs-lookup"><span data-stu-id="da621-187">x</span></span>     |
| <span data-ttu-id="da621-188">wzyx-Datei</span><span class="sxs-lookup"><span data-stu-id="da621-188">.wzyx</span></span>                 |      |      |      |      | <span data-ttu-id="da621-189">x</span><span class="sxs-lookup"><span data-stu-id="da621-189">x</span></span>    | <span data-ttu-id="da621-190">x</span><span class="sxs-lookup"><span data-stu-id="da621-190">x</span></span>    | <span data-ttu-id="da621-191">x</span><span class="sxs-lookup"><span data-stu-id="da621-191">x</span></span>     | <span data-ttu-id="da621-192">x</span><span class="sxs-lookup"><span data-stu-id="da621-192">x</span></span>    | <span data-ttu-id="da621-193">x</span><span class="sxs-lookup"><span data-stu-id="da621-193">x</span></span>     |
| <span data-ttu-id="da621-194">beliebiger Swizzle</span><span class="sxs-lookup"><span data-stu-id="da621-194">arbitrary swizzle</span></span>     |      |      |      |      |      | <span data-ttu-id="da621-195">x</span><span class="sxs-lookup"><span data-stu-id="da621-195">x</span></span>    | <span data-ttu-id="da621-196">x</span><span class="sxs-lookup"><span data-stu-id="da621-196">x</span></span>     | <span data-ttu-id="da621-197">x</span><span class="sxs-lookup"><span data-stu-id="da621-197">x</span></span>    | <span data-ttu-id="da621-198">x</span><span class="sxs-lookup"><span data-stu-id="da621-198">x</span></span>     |



 

<span data-ttu-id="da621-199">\* Nur verfügbar, wenn die Ziel Schreib Maske. w (. a) ist.</span><span class="sxs-lookup"><span data-stu-id="da621-199">\* Only available if destination write mask is .w (.a).</span></span>

## <a name="arbitrary-swizzle"></a><span data-ttu-id="da621-200">Beliebiger Swizzle</span><span class="sxs-lookup"><span data-stu-id="da621-200">Arbitrary Swizzle</span></span>

<span data-ttu-id="da621-201">Auf Quell Register können in beliebiger Reihenfolge Streifen angewendet werden. Das heißt, jedes Quell Register kann jede beliebige Komponenten Maske in beliebiger Reihenfolge verwenden.</span><span class="sxs-lookup"><span data-stu-id="da621-201">Swizzles can be applied to source registers in an arbitrary order; that is, any source register can take any component mask, in any order.</span></span>

## <a name="replicate-swizzle"></a><span data-ttu-id="da621-202">Flüchtigen Replikat</span><span class="sxs-lookup"><span data-stu-id="da621-202">Replicate Swizzle</span></span>

<span data-ttu-id="da621-203">Replizieren von Swizzle kopiert eine Komponente in eine andere.</span><span class="sxs-lookup"><span data-stu-id="da621-203">Replicate swizzle copies one component to another.</span></span> <span data-ttu-id="da621-204">Dies ist genau eine der. x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-Entsprechungen) müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="da621-204">This is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da621-205">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="da621-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da621-206">Pixel-Shader-quellregistrierungs Modifizierern</span><span class="sxs-lookup"><span data-stu-id="da621-206">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> <dt>

[<span data-ttu-id="da621-207">PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Register</span><span class="sxs-lookup"><span data-stu-id="da621-207">ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[<span data-ttu-id="da621-208">PS \_ 2 \_ 0-Register</span><span class="sxs-lookup"><span data-stu-id="da621-208">ps\_2\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[<span data-ttu-id="da621-209">PS \_ 2 \_ x-Register</span><span class="sxs-lookup"><span data-stu-id="da621-209">ps\_2\_x Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[<span data-ttu-id="da621-210">PS \_ 3 \_ 0-Register</span><span class="sxs-lookup"><span data-stu-id="da621-210">ps\_3\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




