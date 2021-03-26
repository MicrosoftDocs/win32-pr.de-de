---
title: Ziel Registrierungs-Schreib Maske
description: Eine Schreib Maske steuert, welche Komponenten eines Ziel Registers geschrieben werden, nachdem eine Anweisung abgeschlossen wurde.
ms.assetid: 376a28c8-8a88-4807-a8ab-f59448d965e8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f649770b84174dbb716967e9d941034c3966f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948085"
---
# <a name="destination-register-write-mask"></a><span data-ttu-id="34d36-103">Ziel Registrierungs-Schreib Maske</span><span class="sxs-lookup"><span data-stu-id="34d36-103">Destination Register Write Mask</span></span>

<span data-ttu-id="34d36-104">Eine Schreib Maske steuert, welche Komponenten eines Ziel Registers geschrieben werden, nachdem eine Anweisung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="34d36-104">A write mask controls which components of a destination register are written after an instruction is completed.</span></span> <span data-ttu-id="34d36-105">Eine Ausgabe Schreib Maske ist zulässig, solange die Komponenten in der Reihenfolge von. RGBA oder. xyzw vorliegen.</span><span class="sxs-lookup"><span data-stu-id="34d36-105">An output write mask is allowed as long as the components are in the order of .rgba or .xyzw.</span></span> <span data-ttu-id="34d36-106">Das heißt, dass RBA und XW gültige Masken sind.</span><span class="sxs-lookup"><span data-stu-id="34d36-106">That is, .rba and .xw are valid masks.</span></span> <span data-ttu-id="34d36-107">Textur Register verfügen über einen Regelsatz, und nicht Textur Register verfügen über einen anderen Satz von Regeln.</span><span class="sxs-lookup"><span data-stu-id="34d36-107">Texture registers have one set of rules and non-texture registers have another set of rules.</span></span>

## <a name="syntax"></a><span data-ttu-id="34d36-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="34d36-108">Syntax</span></span>



| <span data-ttu-id="34d36-109">DST. Write-Ask</span><span class="sxs-lookup"><span data-stu-id="34d36-109">dst.writemask</span></span> |
|---------------|



 

<span data-ttu-id="34d36-110">where</span><span class="sxs-lookup"><span data-stu-id="34d36-110">where</span></span>

-   <span data-ttu-id="34d36-111">DST ist ein Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="34d36-111">dst is a destination register.</span></span>
-   <span data-ttu-id="34d36-112">beim Schreiben von Schreib Vorwörtern handelt es sich um eine Sequenz von Masken, die entweder festgelegt sind: (x, y, z, w) oder (rot, grün, blau, Alpha).</span><span class="sxs-lookup"><span data-stu-id="34d36-112">writemask is a sequence of masks from either set: (x,y,z,w) or (red, green, blue, alpha).</span></span>

## <a name="remarks"></a><span data-ttu-id="34d36-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34d36-113">Remarks</span></span>

<span data-ttu-id="34d36-114">Die folgenden Ziel Schreib Masken sind verfügbar.</span><span class="sxs-lookup"><span data-stu-id="34d36-114">The following destination write masks are available.</span></span>



| <span data-ttu-id="34d36-115">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="34d36-115">Pixel shader versions</span></span> | <span data-ttu-id="34d36-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="34d36-116">1\_1</span></span> | <span data-ttu-id="34d36-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="34d36-117">1\_2</span></span> | <span data-ttu-id="34d36-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="34d36-118">1\_3</span></span> | <span data-ttu-id="34d36-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="34d36-119">1\_4</span></span> | <span data-ttu-id="34d36-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="34d36-120">2\_0</span></span> | <span data-ttu-id="34d36-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="34d36-121">2\_x</span></span> | <span data-ttu-id="34d36-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="34d36-122">2\_sw</span></span> | <span data-ttu-id="34d36-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="34d36-123">3\_0</span></span> | <span data-ttu-id="34d36-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="34d36-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="34d36-125">. xyzw (Standard)</span><span class="sxs-lookup"><span data-stu-id="34d36-125">.xyzw (default)</span></span>       | <span data-ttu-id="34d36-126">x</span><span class="sxs-lookup"><span data-stu-id="34d36-126">x</span></span>    | <span data-ttu-id="34d36-127">x</span><span class="sxs-lookup"><span data-stu-id="34d36-127">x</span></span>    | <span data-ttu-id="34d36-128">x</span><span class="sxs-lookup"><span data-stu-id="34d36-128">x</span></span>    | <span data-ttu-id="34d36-129">x</span><span class="sxs-lookup"><span data-stu-id="34d36-129">x</span></span>    | <span data-ttu-id="34d36-130">x</span><span class="sxs-lookup"><span data-stu-id="34d36-130">x</span></span>    | <span data-ttu-id="34d36-131">x</span><span class="sxs-lookup"><span data-stu-id="34d36-131">x</span></span>    | <span data-ttu-id="34d36-132">x</span><span class="sxs-lookup"><span data-stu-id="34d36-132">x</span></span>     | <span data-ttu-id="34d36-133">x</span><span class="sxs-lookup"><span data-stu-id="34d36-133">x</span></span>    | <span data-ttu-id="34d36-134">x</span><span class="sxs-lookup"><span data-stu-id="34d36-134">x</span></span>     |
| <span data-ttu-id="34d36-135">. XYZ</span><span class="sxs-lookup"><span data-stu-id="34d36-135">.xyz</span></span>                  | <span data-ttu-id="34d36-136">x</span><span class="sxs-lookup"><span data-stu-id="34d36-136">x</span></span>    | <span data-ttu-id="34d36-137">x</span><span class="sxs-lookup"><span data-stu-id="34d36-137">x</span></span>    | <span data-ttu-id="34d36-138">x</span><span class="sxs-lookup"><span data-stu-id="34d36-138">x</span></span>    | <span data-ttu-id="34d36-139">x</span><span class="sxs-lookup"><span data-stu-id="34d36-139">x</span></span>    | <span data-ttu-id="34d36-140">x</span><span class="sxs-lookup"><span data-stu-id="34d36-140">x</span></span>    | <span data-ttu-id="34d36-141">x</span><span class="sxs-lookup"><span data-stu-id="34d36-141">x</span></span>    | <span data-ttu-id="34d36-142">x</span><span class="sxs-lookup"><span data-stu-id="34d36-142">x</span></span>     | <span data-ttu-id="34d36-143">x</span><span class="sxs-lookup"><span data-stu-id="34d36-143">x</span></span>    | <span data-ttu-id="34d36-144">x</span><span class="sxs-lookup"><span data-stu-id="34d36-144">x</span></span>     |
| <span data-ttu-id="34d36-145">. w</span><span class="sxs-lookup"><span data-stu-id="34d36-145">.w</span></span>                    | <span data-ttu-id="34d36-146">x</span><span class="sxs-lookup"><span data-stu-id="34d36-146">x</span></span>    | <span data-ttu-id="34d36-147">x</span><span class="sxs-lookup"><span data-stu-id="34d36-147">x</span></span>    | <span data-ttu-id="34d36-148">x</span><span class="sxs-lookup"><span data-stu-id="34d36-148">x</span></span>    | <span data-ttu-id="34d36-149">x</span><span class="sxs-lookup"><span data-stu-id="34d36-149">x</span></span>    | <span data-ttu-id="34d36-150">x</span><span class="sxs-lookup"><span data-stu-id="34d36-150">x</span></span>    | <span data-ttu-id="34d36-151">x</span><span class="sxs-lookup"><span data-stu-id="34d36-151">x</span></span>    | <span data-ttu-id="34d36-152">x</span><span class="sxs-lookup"><span data-stu-id="34d36-152">x</span></span>     | <span data-ttu-id="34d36-153">x</span><span class="sxs-lookup"><span data-stu-id="34d36-153">x</span></span>    | <span data-ttu-id="34d36-154">x</span><span class="sxs-lookup"><span data-stu-id="34d36-154">x</span></span>     |
| <span data-ttu-id="34d36-155">beliebige Maske</span><span class="sxs-lookup"><span data-stu-id="34d36-155">arbitrary mask</span></span>        |      |      |      | <span data-ttu-id="34d36-156">x</span><span class="sxs-lookup"><span data-stu-id="34d36-156">x</span></span>    | <span data-ttu-id="34d36-157">x</span><span class="sxs-lookup"><span data-stu-id="34d36-157">x</span></span>    | <span data-ttu-id="34d36-158">x</span><span class="sxs-lookup"><span data-stu-id="34d36-158">x</span></span>    | <span data-ttu-id="34d36-159">x</span><span class="sxs-lookup"><span data-stu-id="34d36-159">x</span></span>     | <span data-ttu-id="34d36-160">x</span><span class="sxs-lookup"><span data-stu-id="34d36-160">x</span></span>    | <span data-ttu-id="34d36-161">x</span><span class="sxs-lookup"><span data-stu-id="34d36-161">x</span></span>     |



 

<span data-ttu-id="34d36-162">Mit der beliebigen Maske können alle Kanäle kombiniert werden, um eine Maske zu bilden.</span><span class="sxs-lookup"><span data-stu-id="34d36-162">The arbitrary mask allows any set of channels to be combined to produce a mask.</span></span> <span data-ttu-id="34d36-163">Die Kanäle müssen in der Reihenfolge r, g, b, a aufgeführt werden, z. b. "Register. RBA", mit der die roten, blauen und Alphakanäle des Ziels aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="34d36-163">The channels must be listed in the order r, g, b, a - for example, register.rba, which updates the red, blue, and alpha channels of the destination.</span></span> <span data-ttu-id="34d36-164">Die beliebige Maske ist in Version 1 \_ 4 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="34d36-164">The arbitrary mask is available in version 1\_4 or higher.</span></span>

<span data-ttu-id="34d36-165">Wenn keine Ziel Schreib Maske angegeben ist, wird die Ziel Schreib Maske standardmäßig auf den RGBA-Fall festgelegt.</span><span class="sxs-lookup"><span data-stu-id="34d36-165">If no destination write mask is specified, the destination write mask defaults to the rgba case.</span></span> <span data-ttu-id="34d36-166">Anders ausgedrückt: alle Kanäle im Ziel Register werden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="34d36-166">In other words, all channels in the destination register are updated.</span></span>

<span data-ttu-id="34d36-167">Für die Versionen 1 \_ 0 bis 1 \_ 3 kann die arithmetische Anweisung [DP3-PS](dp3---ps.md) DP3 nur die. RGB-oder. RGBA-Ausgabe Schreib Masken verwenden.</span><span class="sxs-lookup"><span data-stu-id="34d36-167">For versions 1\_0 to 1\_3, the [dp3 - ps](dp3---ps.md) dp3 arithmetic instruction can use only the .rgb or .rgba output write masks.</span></span>

<span data-ttu-id="34d36-168">Ziel Register-Schreib Masken werden nur für arithmetische Operationen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="34d36-168">Destination register write masks are supported for arithmetic operations only.</span></span> <span data-ttu-id="34d36-169">Sie können nicht für Textur Adressierungs Anweisungen verwendet werden, mit Ausnahme der Anweisungen der Version 1 \_ 4, [texcrd-PS](texcrd---ps.md) und [texld-PS \_ 2 \_ 0 und höher](texld---ps-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="34d36-169">They cannot be used on texture addressing instructions, with the exception of the version 1\_4 instructions, [texcrd - ps](texcrd---ps.md) and [texld - ps\_2\_0 and up](texld---ps-2-0.md).</span></span>

<span data-ttu-id="34d36-170">Standardmäßig werden alle vier Farbkanäle geschrieben.</span><span class="sxs-lookup"><span data-stu-id="34d36-170">The default is to write all four color channels.</span></span>


```
// All four color channels can be written by explicitly listing them.
mul r0.rgba, t0, v0

// Or, the default mask can be used to write all four channels.
mul r0, t0, v0
```



<span data-ttu-id="34d36-171">Die Alpha-Schreib Maske wird auch als skalare Schreib Maske bezeichnet, da Sie die skalare Pipeline verwendet.</span><span class="sxs-lookup"><span data-stu-id="34d36-171">The alpha write mask is also referred to as the scalar write mask, because it uses the scalar pipeline.</span></span>


```
add r0.a, t1, v1
```



<span data-ttu-id="34d36-172">Mit dieser Anweisung wird die Summe der Alpha Komponente von T1 und der Alpha Komponente V1 in r0. a eingefügt.</span><span class="sxs-lookup"><span data-stu-id="34d36-172">So this instruction effectively puts the sum of the alpha component of t1 and the alpha component of v1 into r0.a.</span></span>

<span data-ttu-id="34d36-173">Die Farb Schreib Maske wird verwendet, um das Schreiben in die Farbkanäle zu steuern.</span><span class="sxs-lookup"><span data-stu-id="34d36-173">The color write mask is used to control writing to the color channels.</span></span>


```
// The color write mask is also referred to as the vector write mask, 
//   because it uses the vector pipeline.
mul r0.rgb, t0, v0
```



<span data-ttu-id="34d36-174">Für Version 1 \_ 4 können Ziel Schreib Masken in jeder beliebigen Kombination verwendet werden, solange die Masken nach r, g, b, a geordnet sind.</span><span class="sxs-lookup"><span data-stu-id="34d36-174">For version 1\_4, destination write masks can be used in any combination as long as the masks are ordered r,g,b,a.</span></span>


```
// This example updates the red, blue, and alpha channels.
mov r0.rba, r1
```



<span data-ttu-id="34d36-175">Eine gemeinsam ausgestellte Anweisung ermöglicht es, zwei möglicherweise unterschiedliche Anweisungen gleichzeitig auszuführen.</span><span class="sxs-lookup"><span data-stu-id="34d36-175">A co-issued instruction allows two potentially different instructions to be issued simultaneously.</span></span> <span data-ttu-id="34d36-176">Dies wird durch Ausführen der Anweisungen in der Alpha Pipeline und der RGB-Pipeline erreicht.</span><span class="sxs-lookup"><span data-stu-id="34d36-176">This is accomplished by executing the instructions in the alpha pipeline and the RGB pipeline.</span></span>


```
  mul r0.rgb, t0, v0
+ add r1.a,   t1, c1
```



<span data-ttu-id="34d36-177">Der Vorteil von paarweise Einfügeanweisungen besteht darin, dass es möglich ist, verschiedene Vorgänge parallel in der Vektor-und skalarpipeline durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="34d36-177">The advantage of pairing instructions this way is that it allows different operations to be performed in the vector and scalar pipeline in parallel.</span></span>

<span data-ttu-id="34d36-178">Diese Vertex-Shader-Ausgabe Register sind auf die folgenden Schreib Masken beschränkt:</span><span class="sxs-lookup"><span data-stu-id="34d36-178">These vertex shader output registers are restricted to the following write masks:</span></span>



| <span data-ttu-id="34d36-179">Registriungstyp</span><span class="sxs-lookup"><span data-stu-id="34d36-179">Register Type</span></span> | <span data-ttu-id="34d36-180">Erforderliche Schreib Maske</span><span class="sxs-lookup"><span data-stu-id="34d36-180">Required Write Mask</span></span>                                              |
|---------------|------------------------------------------------------------------|
| <span data-ttu-id="34d36-181">onebel</span><span class="sxs-lookup"><span data-stu-id="34d36-181">oFog</span></span>          | <span data-ttu-id="34d36-182">für dieses skalarregister ist keine explizite Schreib Maske zulässig.</span><span class="sxs-lookup"><span data-stu-id="34d36-182">no explicit write mask is allowed on this scalar register</span></span>        |
| <span data-ttu-id="34d36-183">oPts</span><span class="sxs-lookup"><span data-stu-id="34d36-183">oPts</span></span>          | <span data-ttu-id="34d36-184">für dieses skalarregister ist keine explizite Schreib Maske zulässig.</span><span class="sxs-lookup"><span data-stu-id="34d36-184">no explicit write mask is allowed on this scalar register</span></span>        |
| <span data-ttu-id="34d36-185">OPOS</span><span class="sxs-lookup"><span data-stu-id="34d36-185">oPos</span></span>          | <span data-ttu-id="34d36-186">. xyzw (Standardeinstellung)</span><span class="sxs-lookup"><span data-stu-id="34d36-186">.xyzw(which is the default)</span></span>                                      |
| <span data-ttu-id="34d36-187">TS\#</span><span class="sxs-lookup"><span data-stu-id="34d36-187">oT\#</span></span>          | <span data-ttu-id="34d36-188">kombinierte Maske:. x \| . XY \| . XYZ \| . xyzw (Standardeinstellung)</span><span class="sxs-lookup"><span data-stu-id="34d36-188">combined mask: .x \| .xy \| .xyz \| .xyzw (which is the default)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="34d36-189">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="34d36-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34d36-190">Pixelshadermodifizierern</span><span class="sxs-lookup"><span data-stu-id="34d36-190">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




