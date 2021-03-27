---
title: SinCos-PS
description: Berechnet Sinus und Kosinus im Bogenmaße. | SinCos-PS
ms.assetid: 639237ea-1b7a-4959-9093-78f134c11863
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1e7ccdca91af206862384ae14cf25a85d0817814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995542"
---
# <a name="sincos---ps"></a><span data-ttu-id="a75d6-104">SinCos-PS</span><span class="sxs-lookup"><span data-stu-id="a75d6-104">sincos - ps</span></span>

<span data-ttu-id="a75d6-105">Berechnet Sinus und Kosinus im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="a75d6-105">Computes sine and cosine, in radians.</span></span>

## <a name="syntax"></a><span data-ttu-id="a75d6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a75d6-106">Syntax</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="a75d6-107">PS \_ 2 \_ 0 und PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a75d6-107">ps\_2\_0 and ps\_2\_x</span></span>



| <span data-ttu-id="a75d6-108">SinCos DST. Stuben</span><span class="sxs-lookup"><span data-stu-id="a75d6-108">sincos dst.{x\</span></span>|<span data-ttu-id="a75d6-109">Teenie</span><span class="sxs-lookup"><span data-stu-id="a75d6-109">y\</span></span>|<span data-ttu-id="a75d6-110">XY}, src0. Stuben</span><span class="sxs-lookup"><span data-stu-id="a75d6-110">xy}, src0.{x\</span></span>|<span data-ttu-id="a75d6-111">Teenie</span><span class="sxs-lookup"><span data-stu-id="a75d6-111">y\</span></span>|<span data-ttu-id="a75d6-112">z</span><span class="sxs-lookup"><span data-stu-id="a75d6-112">z\</span></span>|<span data-ttu-id="a75d6-113">w}, Quelle1, Quelle2</span><span class="sxs-lookup"><span data-stu-id="a75d6-113">w}, src1, src2</span></span> |
|------------------------------------------------------|



 

<span data-ttu-id="a75d6-114">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="a75d6-114">Where:</span></span>

-   <span data-ttu-id="a75d6-115">DST ist das Ziel Register und muss ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) sein.</span><span class="sxs-lookup"><span data-stu-id="a75d6-115">dst is the destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="a75d6-116">Das Ziel Register muss genau eine der folgenden drei Masken aufweisen:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="a75d6-116">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="a75d6-117">src0 ist ein Quell Register, das den Eingabe Winkel bereitstellt, der innerhalb von \[ -Pi, + Pi liegen muss \] .</span><span class="sxs-lookup"><span data-stu-id="a75d6-117">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="a75d6-118">{x \| y \| z \| w} ist das erforderliche Replizieren von replizieren.</span><span class="sxs-lookup"><span data-stu-id="a75d6-118">{x\|y\|z\|w} is the required replicate swizzle.</span></span>
-   <span data-ttu-id="a75d6-119">Quelle1 und Quelle2 sind Quell Register und müssen zwei unterschiedliche [Konstante float-Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c \# ) aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a75d6-119">src1 and src2 are source registers and must be two different [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c\#).</span></span> <span data-ttu-id="a75d6-120">Die Werte von Quelle1 und Quelle2 müssen der der Makros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) bzw. [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) sein.</span><span class="sxs-lookup"><span data-stu-id="a75d6-120">The values of src1 and src2 must be that of the macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) and [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) respectively.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="a75d6-121">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a75d6-121">ps\_3\_0</span></span>



| <span data-ttu-id="a75d6-122">SinCos DST. Stuben</span><span class="sxs-lookup"><span data-stu-id="a75d6-122">sincos dst.{x\</span></span>|<span data-ttu-id="a75d6-123">Teenie</span><span class="sxs-lookup"><span data-stu-id="a75d6-123">y\</span></span>|<span data-ttu-id="a75d6-124">XY}, src0. Stuben</span><span class="sxs-lookup"><span data-stu-id="a75d6-124">xy}, src0.{x\</span></span>|<span data-ttu-id="a75d6-125">Teenie</span><span class="sxs-lookup"><span data-stu-id="a75d6-125">y\</span></span>|<span data-ttu-id="a75d6-126">z</span><span class="sxs-lookup"><span data-stu-id="a75d6-126">z\</span></span>|<span data-ttu-id="a75d6-127">Löw</span><span class="sxs-lookup"><span data-stu-id="a75d6-127">w}</span></span> |
|------------------------------------------|



 

<span data-ttu-id="a75d6-128">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="a75d6-128">Where:</span></span>

-   <span data-ttu-id="a75d6-129">DST ist ein Ziel Register, das ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r) sein muss \# .</span><span class="sxs-lookup"><span data-stu-id="a75d6-129">dst is a destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="a75d6-130">Das Ziel Register muss genau eine der folgenden drei Masken aufweisen:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="a75d6-130">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="a75d6-131">src0 ist ein Quell Register, das den Eingabe Winkel bereitstellt, der innerhalb von \[ -Pi, + Pi liegen muss \] .</span><span class="sxs-lookup"><span data-stu-id="a75d6-131">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="a75d6-132">{x \| y \| z \| w} ist das erforderliche Replizieren von replizieren.</span><span class="sxs-lookup"><span data-stu-id="a75d6-132">{x\|y\|z\|w} is the required replicate swizzle.</span></span>

## <a name="remarks"></a><span data-ttu-id="a75d6-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a75d6-133">Remarks</span></span>



| <span data-ttu-id="a75d6-134">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="a75d6-134">Pixel shader versions</span></span> | <span data-ttu-id="a75d6-135">1\_1</span><span class="sxs-lookup"><span data-stu-id="a75d6-135">1\_1</span></span> | <span data-ttu-id="a75d6-136">1\_2</span><span class="sxs-lookup"><span data-stu-id="a75d6-136">1\_2</span></span> | <span data-ttu-id="a75d6-137">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a75d6-137">1\_3</span></span> | <span data-ttu-id="a75d6-138">1\_4</span><span class="sxs-lookup"><span data-stu-id="a75d6-138">1\_4</span></span> | <span data-ttu-id="a75d6-139">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a75d6-139">2\_0</span></span> | <span data-ttu-id="a75d6-140">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a75d6-140">2\_x</span></span> | <span data-ttu-id="a75d6-141">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a75d6-141">2\_sw</span></span> | <span data-ttu-id="a75d6-142">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a75d6-142">3\_0</span></span> | <span data-ttu-id="a75d6-143">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a75d6-143">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a75d6-144">SinCos</span><span class="sxs-lookup"><span data-stu-id="a75d6-144">sincos</span></span>                |      |      |      |      | <span data-ttu-id="a75d6-145">x</span><span class="sxs-lookup"><span data-stu-id="a75d6-145">x</span></span>    | <span data-ttu-id="a75d6-146">x</span><span class="sxs-lookup"><span data-stu-id="a75d6-146">x</span></span>    | <span data-ttu-id="a75d6-147">x</span><span class="sxs-lookup"><span data-stu-id="a75d6-147">x</span></span>     | <span data-ttu-id="a75d6-148">x</span><span class="sxs-lookup"><span data-stu-id="a75d6-148">x</span></span>    | <span data-ttu-id="a75d6-149">x</span><span class="sxs-lookup"><span data-stu-id="a75d6-149">x</span></span>     |



 

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="a75d6-150">PS \_ 2 \_ 0 und PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a75d6-150">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="a75d6-151">Für PS \_ 2 \_ 0 und PS \_ 2 \_ x kann SinCos mit dem Prädikat verwendet werden, jedoch mit einer Einschränkung für das ausweichende des [Prädikats](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0): nur replizieren (. x \| . y \| . z \| . w) ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="a75d6-151">For ps\_2\_0 and ps\_2\_x, sincos can be used with predication, but with one restriction to the swizzle of the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0): only replicate swizzle (.x \| .y \| .z \| .w) is allowed.</span></span>

<span data-ttu-id="a75d6-152">Für PS \_ 2 \_ 0 und PS \_ 2 \_ x funktioniert die-Anweisung wie folgt (V = der Skalarwert von src0 mit einem replizierten Swizzle):</span><span class="sxs-lookup"><span data-stu-id="a75d6-152">For ps\_2\_0 and ps\_2\_x, the instruction operates as follows (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="a75d6-153">Wenn die Schreib Maske den Wert. x hat:</span><span class="sxs-lookup"><span data-stu-id="a75d6-153">If the write mask is .x:</span></span>
    ```
    dest.x = cos(V)
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="a75d6-154">Wenn die Schreib Maske ". y" lautet:</span><span class="sxs-lookup"><span data-stu-id="a75d6-154">If the write mask is .y:</span></span>
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="a75d6-155">Wenn die Schreib Maske. XY lautet:</span><span class="sxs-lookup"><span data-stu-id="a75d6-155">If the write mask is .xy:</span></span>
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="ps_3_0"></a><span data-ttu-id="a75d6-156">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a75d6-156">ps\_3\_0</span></span>

<span data-ttu-id="a75d6-157">Für PS \_ 3 \_ 0 kann SinCos mit Prädikat ohne Einschränkung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a75d6-157">For ps\_3\_0, sincos can be used with predication without any restriction.</span></span> <span data-ttu-id="a75d6-158">Siehe [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="a75d6-158">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>

<span data-ttu-id="a75d6-159">Für PS \_ 3 \_ 0 funktioniert die-Anweisung wie folgt (V = der Skalarwert von src0 mit einem replizierten Swizzle):</span><span class="sxs-lookup"><span data-stu-id="a75d6-159">For ps\_3\_0, the instruction operates as follows (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="a75d6-160">Wenn die Schreib Maske den Wert. x hat:</span><span class="sxs-lookup"><span data-stu-id="a75d6-160">If the write mask is .x:</span></span>
    ```
    dest.x = cos(V)
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="a75d6-161">Wenn die Schreib Maske ". y" lautet:</span><span class="sxs-lookup"><span data-stu-id="a75d6-161">If the write mask is .y:</span></span>
    ```
    dest.x is not touched by the instruction
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="a75d6-162">Wenn die Schreib Maske. XY lautet:</span><span class="sxs-lookup"><span data-stu-id="a75d6-162">If the write mask is .xy:</span></span>
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

<span data-ttu-id="a75d6-163">Die Anwendung kann \[ \] mit dem folgenden shaderpseudocode einen beliebigen Winkel (im Bogenmaße) zum Range-Pi und PI zuordnen:</span><span class="sxs-lookup"><span data-stu-id="a75d6-163">The application can map an arbitrary angle (in radians) to the range \[-pi, +pi\] using the following shader pseudocode:</span></span>


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a><span data-ttu-id="a75d6-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a75d6-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a75d6-165">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="a75d6-165">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
