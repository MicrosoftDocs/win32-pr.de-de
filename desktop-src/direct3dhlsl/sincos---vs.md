---
title: SinCos-vs
description: Berechnet Sinus und Kosinus im Bogenmaße. | SinCos-vs
ms.assetid: 733a3980-ceaf-43dc-a862-923c369e4a65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca70a319852346c6e75ba544489d033a861d4c3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961484"
---
# <a name="sincos---vs"></a><span data-ttu-id="2aa7c-104">SinCos-vs</span><span class="sxs-lookup"><span data-stu-id="2aa7c-104">sincos - vs</span></span>

<span data-ttu-id="2aa7c-105">Berechnet Sinus und Kosinus im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="2aa7c-105">Computes sine and cosine, in radians.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aa7c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2aa7c-106">Syntax</span></span>

### <a name="vs_2_0-and-vs_2_x"></a><span data-ttu-id="2aa7c-107">vs \_ 2 \_ 0 und vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2aa7c-107">vs\_2\_0 and vs\_2\_x</span></span>



| <span data-ttu-id="2aa7c-108">SinCos DST. Stuben</span><span class="sxs-lookup"><span data-stu-id="2aa7c-108">sincos dst.{x\</span></span>|<span data-ttu-id="2aa7c-109">Teenie</span><span class="sxs-lookup"><span data-stu-id="2aa7c-109">y\</span></span>|<span data-ttu-id="2aa7c-110">XY}, src0. Stuben</span><span class="sxs-lookup"><span data-stu-id="2aa7c-110">xy}, src0.{x\</span></span>|<span data-ttu-id="2aa7c-111">Teenie</span><span class="sxs-lookup"><span data-stu-id="2aa7c-111">y\</span></span>|<span data-ttu-id="2aa7c-112">z</span><span class="sxs-lookup"><span data-stu-id="2aa7c-112">z\</span></span>|<span data-ttu-id="2aa7c-113">w}, Quelle1, Quelle2</span><span class="sxs-lookup"><span data-stu-id="2aa7c-113">w}, src1, src2</span></span> |
|------------------------------------------------------|



 

<span data-ttu-id="2aa7c-114">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="2aa7c-114">Where:</span></span>

-   <span data-ttu-id="2aa7c-115">DST ist das Ziel Register und muss ein [temporäres Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ) sein.</span><span class="sxs-lookup"><span data-stu-id="2aa7c-115">dst is the destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="2aa7c-116">Das Ziel Register muss genau eine der folgenden drei Masken aufweisen:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="2aa7c-116">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="2aa7c-117">src0 ist ein Quell Register, das den Eingabe Winkel bereitstellt, der innerhalb von \[ -Pi, + Pi liegen muss \] .</span><span class="sxs-lookup"><span data-stu-id="2aa7c-117">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="2aa7c-118">{x \| y \| z \| w} ist das erforderliche Replizieren von replizieren.</span><span class="sxs-lookup"><span data-stu-id="2aa7c-118">{x\|y\|z\|w} is the required replicate swizzle.</span></span>
-   <span data-ttu-id="2aa7c-119">Quelle1 und Quelle2 sind Quell Register und müssen zwei unterschiedliche [Konstante float-Register](dx9-graphics-reference-asm-vs-registers-constant-float.md) (c \# ) aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2aa7c-119">src1 and src2 are source registers and must be two different [Constant Float Register](dx9-graphics-reference-asm-vs-registers-constant-float.md) (c\#).</span></span> <span data-ttu-id="2aa7c-120">Die Werte von Quelle1 und Quelle2 müssen der der Makros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) bzw. [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) sein.</span><span class="sxs-lookup"><span data-stu-id="2aa7c-120">The values of src1 and src2 must be that of the macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) and [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) respectively.</span></span>

### <a name="vs_3_0"></a><span data-ttu-id="2aa7c-121">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2aa7c-121">vs\_3\_0</span></span>



| <span data-ttu-id="2aa7c-122">SinCos DST. Stuben</span><span class="sxs-lookup"><span data-stu-id="2aa7c-122">sincos dst.{x\</span></span>|<span data-ttu-id="2aa7c-123">Teenie</span><span class="sxs-lookup"><span data-stu-id="2aa7c-123">y\</span></span>|<span data-ttu-id="2aa7c-124">XY}, src0. Stuben</span><span class="sxs-lookup"><span data-stu-id="2aa7c-124">xy}, src0.{x\</span></span>|<span data-ttu-id="2aa7c-125">Teenie</span><span class="sxs-lookup"><span data-stu-id="2aa7c-125">y\</span></span>|<span data-ttu-id="2aa7c-126">z</span><span class="sxs-lookup"><span data-stu-id="2aa7c-126">z\</span></span>|<span data-ttu-id="2aa7c-127">Löw</span><span class="sxs-lookup"><span data-stu-id="2aa7c-127">w}</span></span> |
|------------------------------------------|



 

<span data-ttu-id="2aa7c-128">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="2aa7c-128">Where:</span></span>

-   <span data-ttu-id="2aa7c-129">DST ist ein Ziel Register, das ein [temporäres Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r) sein muss \# .</span><span class="sxs-lookup"><span data-stu-id="2aa7c-129">dst is a destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="2aa7c-130">Das Ziel Register muss genau eine der folgenden drei Masken aufweisen:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="2aa7c-130">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="2aa7c-131">src0 ist ein Quell Register, das den Eingabe Winkel bereitstellt, der innerhalb von \[ -Pi, + Pi liegen muss \] .</span><span class="sxs-lookup"><span data-stu-id="2aa7c-131">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="2aa7c-132">{x \| y \| z \| w} ist das erforderliche Replizieren von replizieren.</span><span class="sxs-lookup"><span data-stu-id="2aa7c-132">{x\|y\|z\|w} is the required replicate swizzle.</span></span>

## <a name="remarks"></a><span data-ttu-id="2aa7c-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2aa7c-133">Remarks</span></span>



| <span data-ttu-id="2aa7c-134">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="2aa7c-134">Vertex shader versions</span></span> | <span data-ttu-id="2aa7c-135">1\_1</span><span class="sxs-lookup"><span data-stu-id="2aa7c-135">1\_1</span></span> | <span data-ttu-id="2aa7c-136">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2aa7c-136">2\_0</span></span> | <span data-ttu-id="2aa7c-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2aa7c-137">2\_x</span></span> | <span data-ttu-id="2aa7c-138">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2aa7c-138">2\_sw</span></span> | <span data-ttu-id="2aa7c-139">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2aa7c-139">3\_0</span></span> | <span data-ttu-id="2aa7c-140">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2aa7c-140">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="2aa7c-141">SinCos</span><span class="sxs-lookup"><span data-stu-id="2aa7c-141">sincos</span></span>                 |      | <span data-ttu-id="2aa7c-142">x</span><span class="sxs-lookup"><span data-stu-id="2aa7c-142">x</span></span>    | <span data-ttu-id="2aa7c-143">x</span><span class="sxs-lookup"><span data-stu-id="2aa7c-143">x</span></span>    | <span data-ttu-id="2aa7c-144">x</span><span class="sxs-lookup"><span data-stu-id="2aa7c-144">x</span></span>     | <span data-ttu-id="2aa7c-145">x</span><span class="sxs-lookup"><span data-stu-id="2aa7c-145">x</span></span>    | <span data-ttu-id="2aa7c-146">x</span><span class="sxs-lookup"><span data-stu-id="2aa7c-146">x</span></span>     |



 

### <a name="vs_2_0-and-vs_2_x-remarks"></a><span data-ttu-id="2aa7c-147">\_ \_ Anmerkungen zu vs 2 0 und vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2aa7c-147">vs\_2\_0 and vs\_2\_x Remarks</span></span>

<span data-ttu-id="2aa7c-148">Für vs \_ 2 \_ 0 und vs \_ 2 \_ x können SinCos mit Prädikaten verwendet werden, jedoch mit einer Einschränkung für das ausweichende des [Prädikats](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0): nur replizieren (. x \| . y \| . z \| . w) ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="2aa7c-148">For vs\_2\_0 and vs\_2\_x, sincos can be used with predication, but with one restriction to the swizzle of the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0): only replicate swizzle (.x \| .y \| .z \| .w) is allowed.</span></span>

<span data-ttu-id="2aa7c-149">Für vs \_ 2 \_ 0 und vs \_ 2 \_ x verhält sich die-Anweisung wie folgt: (V = der skalare Wert von src0 mit einem replizierten Swizzle):</span><span class="sxs-lookup"><span data-stu-id="2aa7c-149">For vs\_2\_0 and vs\_2\_x, the instruction operates as follows: (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="2aa7c-150">Wenn die Schreib Maske den Wert. x hat:</span><span class="sxs-lookup"><span data-stu-id="2aa7c-150">If the write mask is .x:</span></span>
    ```
    dest.x = cos( V )
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="2aa7c-151">Wenn die Schreib Maske ". y" lautet:</span><span class="sxs-lookup"><span data-stu-id="2aa7c-151">If the write mask is .y:</span></span>
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="2aa7c-152">Wenn die Schreib Maske. XY lautet:</span><span class="sxs-lookup"><span data-stu-id="2aa7c-152">If the write mask is .xy:</span></span>
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="vs_3_0-remarks"></a><span data-ttu-id="2aa7c-153">vs \_ 3 \_ 0-Hinweise</span><span class="sxs-lookup"><span data-stu-id="2aa7c-153">vs\_3\_0 Remarks</span></span>

<span data-ttu-id="2aa7c-154">Für vs \_ 3 \_ 0 kann SinCos mit einem Prädikat ohne Einschränkung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2aa7c-154">For vs\_3\_0, sincos can be used with predication without any restriction.</span></span> <span data-ttu-id="2aa7c-155">Siehe [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="2aa7c-155">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>

<span data-ttu-id="2aa7c-156">Für vs \_ 3 \_ 0 funktioniert die-Anweisung wie folgt: (V = der Skalarwert von src0 mit einem replizierten Swizzle)</span><span class="sxs-lookup"><span data-stu-id="2aa7c-156">For vs\_3\_0, the instruction operates as follows: (V = the scalar value from src0 with a replicate swizzle)</span></span>

-   <span data-ttu-id="2aa7c-157">Wenn die Schreib Maske den Wert. x hat:</span><span class="sxs-lookup"><span data-stu-id="2aa7c-157">If the write mask is .x:</span></span>
    ```
    dest.x = cos( V )
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="2aa7c-158">Wenn die Schreib Maske ". y" lautet:</span><span class="sxs-lookup"><span data-stu-id="2aa7c-158">If the write mask is .y:</span></span>
    ```
    dest.x is not touched by the instruction
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="2aa7c-159">Wenn die Schreib Maske. XY lautet:</span><span class="sxs-lookup"><span data-stu-id="2aa7c-159">If the write mask is .xy:</span></span>
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

<span data-ttu-id="2aa7c-160">Die Anwendung kann \[ \] mit dem folgenden shaderpseudocode einen beliebigen Winkel (im Bogenmaße) zum Range-Pi und PI zuordnen:</span><span class="sxs-lookup"><span data-stu-id="2aa7c-160">The application can map an arbitrary angle (in radians) to the range \[-pi, +pi\] using the following shader pseudocode:</span></span>


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a><span data-ttu-id="2aa7c-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2aa7c-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2aa7c-162">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="2aa7c-162">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
