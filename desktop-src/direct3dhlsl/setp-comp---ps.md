---
title: setp_comp-PS
description: Legen Sie das Prädikat Register fest. | setp_comp-PS
ms.assetid: a9acb685-f9aa-41f1-8ef1-6d104cb76a09
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a68da290ecb04e9cb7ae49c5525997fbf4c112a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219322"
---
# <a name="setp_comp---ps"></a><span data-ttu-id="ce4f2-104">SETP \_ -Comp-PS</span><span class="sxs-lookup"><span data-stu-id="ce4f2-104">setp\_comp - ps</span></span>

<span data-ttu-id="ce4f2-105">Legen Sie das Prädikat Register fest.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-105">Set the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce4f2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce4f2-106">Syntax</span></span>



| <span data-ttu-id="ce4f2-107">SETP \_ Comp DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="ce4f2-107">setp\_comp dst, src0, src1</span></span> |
|----------------------------|



 

<span data-ttu-id="ce4f2-108">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="ce4f2-108">Where:</span></span>

-   <span data-ttu-id="ce4f2-109">\_comp ist ein pro-Kanal-Vergleich zwischen den beiden Quell Registern.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-109">\_comp is a per-channel comparison between the two source registers.</span></span> <span data-ttu-id="ce4f2-110">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="ce4f2-110">It can be one of the following:</span></span> 

    | <span data-ttu-id="ce4f2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce4f2-111">Syntax</span></span> | <span data-ttu-id="ce4f2-112">Vergleich</span><span class="sxs-lookup"><span data-stu-id="ce4f2-112">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="ce4f2-113">\_siegt</span><span class="sxs-lookup"><span data-stu-id="ce4f2-113">\_gt</span></span>   | <span data-ttu-id="ce4f2-114">Größer als</span><span class="sxs-lookup"><span data-stu-id="ce4f2-114">Greater than</span></span>          |
    | <span data-ttu-id="ce4f2-115">\_General</span><span class="sxs-lookup"><span data-stu-id="ce4f2-115">\_lt</span></span>   | <span data-ttu-id="ce4f2-116">Kleiner als</span><span class="sxs-lookup"><span data-stu-id="ce4f2-116">Less than</span></span>             |
    | <span data-ttu-id="ce4f2-117">\_Färbung</span><span class="sxs-lookup"><span data-stu-id="ce4f2-117">\_ge</span></span>   | <span data-ttu-id="ce4f2-118">Größer als oder gleich</span><span class="sxs-lookup"><span data-stu-id="ce4f2-118">Greater than or equal</span></span> |
    | <span data-ttu-id="ce4f2-119">\_Kirchturm</span><span class="sxs-lookup"><span data-stu-id="ce4f2-119">\_le</span></span>   | <span data-ttu-id="ce4f2-120">Kleiner als oder gleich</span><span class="sxs-lookup"><span data-stu-id="ce4f2-120">Less than or equal</span></span>    |
    | <span data-ttu-id="ce4f2-121">\_stecken</span><span class="sxs-lookup"><span data-stu-id="ce4f2-121">\_eq</span></span>   | <span data-ttu-id="ce4f2-122">Gleich</span><span class="sxs-lookup"><span data-stu-id="ce4f2-122">Equal to</span></span>              |
    | <span data-ttu-id="ce4f2-123">\_NES</span><span class="sxs-lookup"><span data-stu-id="ce4f2-123">\_ne</span></span>   | <span data-ttu-id="ce4f2-124">Ungleich</span><span class="sxs-lookup"><span data-stu-id="ce4f2-124">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="ce4f2-125">DST ist das [Registrierungs](dx9-graphics-reference-asm-ps-registers-predicate.md) registerregister, p0.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-125">dst is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) register, p0.</span></span>
-   <span data-ttu-id="ce4f2-126">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-126">src0 is a source register.</span></span>
-   <span data-ttu-id="ce4f2-127">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-127">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce4f2-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce4f2-128">Remarks</span></span>



| <span data-ttu-id="ce4f2-129">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="ce4f2-129">Pixel shader versions</span></span> | <span data-ttu-id="ce4f2-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="ce4f2-130">1\_1</span></span> | <span data-ttu-id="ce4f2-131">1\_2</span><span class="sxs-lookup"><span data-stu-id="ce4f2-131">1\_2</span></span> | <span data-ttu-id="ce4f2-132">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ce4f2-132">1\_3</span></span> | <span data-ttu-id="ce4f2-133">1\_4</span><span class="sxs-lookup"><span data-stu-id="ce4f2-133">1\_4</span></span> | <span data-ttu-id="ce4f2-134">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ce4f2-134">2\_0</span></span> | <span data-ttu-id="ce4f2-135">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ce4f2-135">2\_x</span></span> | <span data-ttu-id="ce4f2-136">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ce4f2-136">2\_sw</span></span> | <span data-ttu-id="ce4f2-137">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ce4f2-137">3\_0</span></span> | <span data-ttu-id="ce4f2-138">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ce4f2-138">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="ce4f2-139">SETP \_ comp</span><span class="sxs-lookup"><span data-stu-id="ce4f2-139">setp\_comp</span></span>            |      |      |      |      |      | <span data-ttu-id="ce4f2-140">x</span><span class="sxs-lookup"><span data-stu-id="ce4f2-140">x</span></span>    | <span data-ttu-id="ce4f2-141">x</span><span class="sxs-lookup"><span data-stu-id="ce4f2-141">x</span></span>     | <span data-ttu-id="ce4f2-142">x</span><span class="sxs-lookup"><span data-stu-id="ce4f2-142">x</span></span>    | <span data-ttu-id="ce4f2-143">x</span><span class="sxs-lookup"><span data-stu-id="ce4f2-143">x</span></span>     |



 

<span data-ttu-id="ce4f2-144">Diese Anweisung funktioniert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ce4f2-144">This instruction operates as:</span></span>


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



<span data-ttu-id="ce4f2-145">Speichern Sie für jeden Kanal, der gemäß der Ziel Schreib Maske geschrieben werden kann, das boolesche Ergebnis der Vergleichsoperation zwischen den entsprechenden Kanälen von src0 und Quelle1 (nachdem die Eigenschaften des quellmodifizierers aufgelöst wurden).</span><span class="sxs-lookup"><span data-stu-id="ce4f2-145">For each channel that can be written according to the destination write mask, save the boolean result of the comparison operation between the corresponding channels of src0 and src1 (after the source modifier swizzles have been resolved).</span></span>

<span data-ttu-id="ce4f2-146">Mit Quell Registern können beliebige Komponenten Streifen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-146">Source registers allow arbitrary component swizzles to be specified.</span></span>

<span data-ttu-id="ce4f2-147">Das Ziel Register ermöglicht willkürliche Schreib Masken.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-147">The destination register allows arbitrary write masks.</span></span>

<span data-ttu-id="ce4f2-148">Das DST-Register muss das Prädikat Register sein.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-148">The dst register must be the predicate register.</span></span>

## <a name="applying-the-predicate-register"></a><span data-ttu-id="ce4f2-149">Anwenden des Prädikats Register</span><span class="sxs-lookup"><span data-stu-id="ce4f2-149">Applying the Predicate Register</span></span>

<span data-ttu-id="ce4f2-150">Wenn das Prädikat Register mit SETP Comp initialisiert wurde \_ , kann es verwendet werden, um eine Anweisung pro Komponente zu steuern.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-150">Once the predicate register has been initialized with setp\_comp, it can be used to control an instruction per component.</span></span> <span data-ttu-id="ce4f2-151">Hier ist die Syntax:</span><span class="sxs-lookup"><span data-stu-id="ce4f2-151">Here's the syntax:</span></span>


```
([!]p0[.swizzle]) instruction dest, src0, ...
```



<span data-ttu-id="ce4f2-152">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="ce4f2-152">Where:</span></span>

-   <span data-ttu-id="ce4f2-153">\[!\] ist ein optionaler boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-153">\[!\] is an optional boolean NOT</span></span>
-   <span data-ttu-id="ce4f2-154">P0 ist das Prädikats Register</span><span class="sxs-lookup"><span data-stu-id="ce4f2-154">p0 is the predicate register</span></span>
-   <span data-ttu-id="ce4f2-155">\[. Swizzle \] ist ein optionales Swizzle, das auf den Inhalt des Prädikats angewendet wird, bevor es zum Maskieren der Anweisung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-155">\[.swizzle\] is an optional swizzle to apply to the contents of the predicate register before using it to mask the instruction.</span></span> <span data-ttu-id="ce4f2-156">Zu den verfügbaren Strichen gehören:. xyzw (Standardwert, wenn kein Wert angegeben ist) oder eine beliebige Replikation:. x/. r,. y/. g,. z/. b oder. a/. w.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-156">The available swizzles are: .xyzw (default when none specified), or any replicate swizzle: .x/.r, .y/.g, .z/.b or .a/.w.</span></span>
-   <span data-ttu-id="ce4f2-157">die Anweisung ist eine beliebige aritmetic-oder Textur Anweisung.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-157">instruction is any aritmetic, or texture instruction.</span></span> <span data-ttu-id="ce4f2-158">Dabei kann es sich nicht um eine statische oder dynamische Fluss Steuerungs Anweisung handeln.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-158">This cannot be a static or dynamic flow control instruction.</span></span>
-   <span data-ttu-id="ce4f2-159">dest, src0,... sind die von der Anweisung benötigten Register</span><span class="sxs-lookup"><span data-stu-id="ce4f2-159">dest, src0, ... are the registers required by the instruction</span></span>

<span data-ttu-id="ce4f2-160">Angenommen, das Prädikat Register wurde mit den Komponenten Werten (true, true, false, false) eingerichtet, die auf diese Anweisung angewendet werden können:</span><span class="sxs-lookup"><span data-stu-id="ce4f2-160">Assuming the predicate register has been set up with (true, true, false, false) component values, it can be applied to this instruction:</span></span>


```
(p0) add r1, r2, r3
```



<span data-ttu-id="ce4f2-161">zum Ausführen einer 2-Komponente hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-161">to perform a 2 component add.</span></span>


```
r1.x = r2.x + r3.x
r1.y = r2.y + r3.y
```



<span data-ttu-id="ce4f2-162">Die z-und w-Komponenten von R1 werden nicht geschrieben, da das Prädikat Register in den Komponenten z und w false enthielt.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-162">The z and w components of r1 will not be written since the predicate register contained false in components z and w.</span></span>

<span data-ttu-id="ce4f2-163">Wenn Sie das Prädikat Register auf eine arithmetische oder Textur Anweisung anwenden, erhöht sich die Anzahl der Anweisungs Slots um 1.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-163">Applying the predicate register to an arithmetic or texture instruction increases its instruction slot count by 1.</span></span>

<span data-ttu-id="ce4f2-164">Das Prädikat Register kann auch auf angewendet werden, [Wenn pred-PS](if-pred---ps.md), [callnz pred-PS](callnz-pred---ps.md) und [breakp-PS-](break-p---ps.md) Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-164">The predicate register can also be applied to [if pred - ps](if-pred---ps.md), [callnz pred - ps](callnz-pred---ps.md) and [breakp - ps](break-p---ps.md) instructions.</span></span> <span data-ttu-id="ce4f2-165">Diese Fluss Steuerungs Anweisungen weisen keine Zunahme der Anweisungs Slot-Anzahl auf, wenn das Prädikat Register verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-165">These flow control instructions do not have any increase in the instruction slot count when using the predicate register.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce4f2-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce4f2-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce4f2-167">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="ce4f2-167">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




