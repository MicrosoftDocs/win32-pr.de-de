---
title: setp_comp vs
description: Legen Sie das Prädikat Register fest. | setp_comp vs
ms.assetid: bfead3f8-f7fe-4fc1-939f-8e5fbc3e0adf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77d9e5f46e9fb8bbcfb96e56d13cd6f7cebfecc2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104393978"
---
# <a name="setp_comp---vs"></a><span data-ttu-id="ce383-104">SETP \_ -Comp-vs</span><span class="sxs-lookup"><span data-stu-id="ce383-104">setp\_comp - vs</span></span>

<span data-ttu-id="ce383-105">Legen Sie das Prädikat Register fest.</span><span class="sxs-lookup"><span data-stu-id="ce383-105">Set the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce383-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce383-106">Syntax</span></span>



| <span data-ttu-id="ce383-107">SETP \_ Comp DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="ce383-107">setp\_comp dst, src0, src1</span></span> |
|----------------------------|



 

<span data-ttu-id="ce383-108">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="ce383-108">Where:</span></span>

-   <span data-ttu-id="ce383-109">\_comp ist ein pro-Kanal-Vergleich zwischen den beiden Quell Registern.</span><span class="sxs-lookup"><span data-stu-id="ce383-109">\_comp is a per-channel comparison between the two source registers.</span></span> <span data-ttu-id="ce383-110">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="ce383-110">It can be one of the following:</span></span> 

    | <span data-ttu-id="ce383-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce383-111">Syntax</span></span> | <span data-ttu-id="ce383-112">Vergleich</span><span class="sxs-lookup"><span data-stu-id="ce383-112">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="ce383-113">\_siegt</span><span class="sxs-lookup"><span data-stu-id="ce383-113">\_gt</span></span>   | <span data-ttu-id="ce383-114">Größer als</span><span class="sxs-lookup"><span data-stu-id="ce383-114">Greater than</span></span>          |
    | <span data-ttu-id="ce383-115">\_General</span><span class="sxs-lookup"><span data-stu-id="ce383-115">\_lt</span></span>   | <span data-ttu-id="ce383-116">Kleiner als</span><span class="sxs-lookup"><span data-stu-id="ce383-116">Less than</span></span>             |
    | <span data-ttu-id="ce383-117">\_Färbung</span><span class="sxs-lookup"><span data-stu-id="ce383-117">\_ge</span></span>   | <span data-ttu-id="ce383-118">Größer als oder gleich</span><span class="sxs-lookup"><span data-stu-id="ce383-118">Greater than or equal</span></span> |
    | <span data-ttu-id="ce383-119">\_Kirchturm</span><span class="sxs-lookup"><span data-stu-id="ce383-119">\_le</span></span>   | <span data-ttu-id="ce383-120">Kleiner als oder gleich</span><span class="sxs-lookup"><span data-stu-id="ce383-120">Less than or equal</span></span>    |
    | <span data-ttu-id="ce383-121">\_stecken</span><span class="sxs-lookup"><span data-stu-id="ce383-121">\_eq</span></span>   | <span data-ttu-id="ce383-122">Gleich</span><span class="sxs-lookup"><span data-stu-id="ce383-122">Equal to</span></span>              |
    | <span data-ttu-id="ce383-123">\_NES</span><span class="sxs-lookup"><span data-stu-id="ce383-123">\_ne</span></span>   | <span data-ttu-id="ce383-124">Ungleich</span><span class="sxs-lookup"><span data-stu-id="ce383-124">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="ce383-125">DST ist das [Registrierungs](dx9-graphics-reference-asm-vs-registers-predicate.md) registerregister, p0.</span><span class="sxs-lookup"><span data-stu-id="ce383-125">dst is the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) register, p0.</span></span>
-   <span data-ttu-id="ce383-126">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="ce383-126">src0 is a source register.</span></span>
-   <span data-ttu-id="ce383-127">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="ce383-127">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce383-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce383-128">Remarks</span></span>



| <span data-ttu-id="ce383-129">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="ce383-129">Vertex shader versions</span></span> | <span data-ttu-id="ce383-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="ce383-130">1\_1</span></span> | <span data-ttu-id="ce383-131">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ce383-131">2\_0</span></span> | <span data-ttu-id="ce383-132">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ce383-132">2\_x</span></span> | <span data-ttu-id="ce383-133">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ce383-133">2\_sw</span></span> | <span data-ttu-id="ce383-134">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ce383-134">3\_0</span></span> | <span data-ttu-id="ce383-135">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ce383-135">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="ce383-136">SETP \_ comp</span><span class="sxs-lookup"><span data-stu-id="ce383-136">setp\_comp</span></span>             |      |      | <span data-ttu-id="ce383-137">x</span><span class="sxs-lookup"><span data-stu-id="ce383-137">x</span></span>    | <span data-ttu-id="ce383-138">x</span><span class="sxs-lookup"><span data-stu-id="ce383-138">x</span></span>     | <span data-ttu-id="ce383-139">x</span><span class="sxs-lookup"><span data-stu-id="ce383-139">x</span></span>    | <span data-ttu-id="ce383-140">x</span><span class="sxs-lookup"><span data-stu-id="ce383-140">x</span></span>     |



 

<span data-ttu-id="ce383-141">Diese Anweisung funktioniert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ce383-141">This instruction operates as:</span></span>


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



<span data-ttu-id="ce383-142">Speichern Sie für jeden Kanal, der gemäß der Ziel Schreib Maske geschrieben werden kann, das boolesche Ergebnis der Vergleichsoperation zwischen den entsprechenden Kanälen von src0 und Quelle1 (nachdem die Eigenschaften des quellmodifizierers aufgelöst wurden).</span><span class="sxs-lookup"><span data-stu-id="ce383-142">For each channel that can be written according to the destination write mask, save the boolean result of the comparison operation between the corresponding channels of src0 and src1 (after the source modifier swizzles have been resolved).</span></span>

<span data-ttu-id="ce383-143">Mit Quell Registern können beliebige Komponenten Streifen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ce383-143">Source registers allow arbitrary component swizzles to be specified.</span></span>

<span data-ttu-id="ce383-144">Das Ziel Register ermöglicht willkürliche Schreib Masken.</span><span class="sxs-lookup"><span data-stu-id="ce383-144">The destination register allows arbitrary write masks.</span></span>

<span data-ttu-id="ce383-145">Das dest-Register muss das Prädikat Register sein.</span><span class="sxs-lookup"><span data-stu-id="ce383-145">The dest register must be the predicate register.</span></span>

## <a name="applying-the-predicate-register"></a><span data-ttu-id="ce383-146">Anwenden des Prädikats Register</span><span class="sxs-lookup"><span data-stu-id="ce383-146">Applying the Predicate Register</span></span>

<span data-ttu-id="ce383-147">Wenn das Prädikat Register mit SETP initialisiert wurde, kann es verwendet werden, um eine Anweisung pro Komponente zu steuern.</span><span class="sxs-lookup"><span data-stu-id="ce383-147">Once the predicate register has been initialized with setp, it can be used to control an instruction per component.</span></span> <span data-ttu-id="ce383-148">Hier ist die Syntax:</span><span class="sxs-lookup"><span data-stu-id="ce383-148">Here's the syntax:</span></span>


```
([!]p0[.swizzle]) instruction dest, srcReg, ...
```



<span data-ttu-id="ce383-149">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="ce383-149">Where:</span></span>

-   <span data-ttu-id="ce383-150">\[!\] ist ein optionaler boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="ce383-150">\[!\] is an optional boolean NOT</span></span>
-   <span data-ttu-id="ce383-151">P0 ist das Prädikats Register</span><span class="sxs-lookup"><span data-stu-id="ce383-151">p0 is the predicate register</span></span>
-   <span data-ttu-id="ce383-152">\[. Swizzle \] ist ein optionales Swizzle, das auf den Inhalt des Prädikats angewendet wird, bevor es zum Maskieren der Anweisung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ce383-152">\[.swizzle\] is an optional swizzle to apply to the contents of the predicate register before using it to mask the instruction.</span></span> <span data-ttu-id="ce383-153">Zu den verfügbaren Strichen gehören:. xyzw (Standardwert, wenn kein Wert angegeben ist) oder eine beliebige Replikation:. x/. r,. y/. g,. z/. b oder. a/. w.</span><span class="sxs-lookup"><span data-stu-id="ce383-153">The available swizzles are: .xyzw (default when none specified), or any replicate swizzle: .x/.r, .y/.g, .z/.b or .a/.w.</span></span>
-   <span data-ttu-id="ce383-154">die Anweisung ist eine beliebige aritmetic-oder Textur Anweisung.</span><span class="sxs-lookup"><span data-stu-id="ce383-154">instruction is any aritmetic, or texture instruction.</span></span> <span data-ttu-id="ce383-155">Dabei kann es sich nicht um eine statische oder dynamische Fluss Steuerungs Anweisung handeln.</span><span class="sxs-lookup"><span data-stu-id="ce383-155">This cannot be a static or dynamic flow control instruction.</span></span>
-   <span data-ttu-id="ce383-156">dest, srkreg,... sind die von der Anweisung benötigten Register</span><span class="sxs-lookup"><span data-stu-id="ce383-156">dest, srcReg, ... are the registers required by the instruction</span></span>

<span data-ttu-id="ce383-157">Angenommen, das Prädikat Register wurde mit den Komponenten Werten (true, true, false, false) eingerichtet, die auf diese Anweisung angewendet werden können:</span><span class="sxs-lookup"><span data-stu-id="ce383-157">Assuming the predicate register has been set up with (true, true, false, false) component values, it can be applied to this instruction:</span></span>


```
// given r0 = 0,0,1,1
// given r1 = 1,1,0,0
setp_le p0, r0, r1
(p0) add r2, r3, r4
```



<span data-ttu-id="ce383-158">zum Ausführen einer 2-Komponente hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ce383-158">to perform a 2 component add.</span></span>


```
r2.x = r3.x + r4.x
r2.y = r3.y + r4.y
```



<span data-ttu-id="ce383-159">Die x-und y-Komponenten von R2 werden nicht geschrieben, da das Prädikat Register in den Komponenten z und w false enthielt.</span><span class="sxs-lookup"><span data-stu-id="ce383-159">The x and y components of r2 will not be written since the predicate register contained false in components z and w.</span></span>

<span data-ttu-id="ce383-160">Wenn Sie das Prädikat Register auf eine arithmetische oder Textur Anweisung anwenden, erhöht sich die Anzahl der Anweisungs Slots um 1.</span><span class="sxs-lookup"><span data-stu-id="ce383-160">Applying the predicate register to an arithmetic or texture instruction increases its instruction slot count by 1.</span></span>

<span data-ttu-id="ce383-161">Das Prädikat Register kann auch auf angewendet werden, wenn es sich um [pred-vs](if-pred---vs.md), [callnz pred-vs](callnz-pred---vs.md) und [breakp-vs-](breakp---vs.md) Anweisungen handelt.</span><span class="sxs-lookup"><span data-stu-id="ce383-161">The predicate register can also be applied to [if pred - vs](if-pred---vs.md), [callnz pred - vs](callnz-pred---vs.md) and [breakp - vs](breakp---vs.md) instructions.</span></span> <span data-ttu-id="ce383-162">Diese Fluss Steuerungs Anweisungen weisen keine Zunahme der Anweisungs Slot-Anzahl auf, wenn das Prädikat Register verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ce383-162">These flow control instructions do not have any increase in the instruction slot count when using the predicate register.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce383-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce383-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce383-164">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="ce383-164">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




