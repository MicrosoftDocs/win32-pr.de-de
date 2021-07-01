---
title: Modifizierer für ps_1_X
description: Anweisungsmodifizierer beeinflussen das Ergebnis der Anweisung, bevor sie in das Zielregister geschrieben wird. Erfahren Sie mehr über Modifizierer für ps_1_X.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9291d818252c95bc11fae72bd3311ec733a45fa
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129939"
---
# <a name="modifiers-for-ps_1_x"></a><span data-ttu-id="e78c7-104">Modifizierer für PS \_ 1 \_ X</span><span class="sxs-lookup"><span data-stu-id="e78c7-104">Modifiers for ps\_1\_X</span></span>

<span data-ttu-id="e78c7-105">Anweisungsmodifizierer beeinflussen das Ergebnis der Anweisung, bevor sie in das Zielregister geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="e78c7-105">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span> <span data-ttu-id="e78c7-106">Verwenden Sie sie beispielsweise, um das Ergebnis mit einem Faktor von zwei zu multiplizieren oder zu dividieren oder um das Ergebnis zwischen 0 und 1 zu binden.</span><span class="sxs-lookup"><span data-stu-id="e78c7-106">For instance, use them to multiply or divide the result by a factor of two, or to clamp the result between zero and one.</span></span> <span data-ttu-id="e78c7-107">Anweisungsmodifizierer werden angewendet, nachdem die Anweisung ausgeführt wurde, aber bevor das Ergebnis in das Zielregister geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="e78c7-107">Instruction modifiers are applied after the instruction runs but before writing the result to the destination register.</span></span>

<span data-ttu-id="e78c7-108">Eine Liste der Modifizierer ist unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e78c7-108">A list of the modifiers is shown below.</span></span>



| <span data-ttu-id="e78c7-109">Modifizierer</span><span class="sxs-lookup"><span data-stu-id="e78c7-109">Modifier</span></span> | <span data-ttu-id="e78c7-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e78c7-110">Description</span></span>                   | <span data-ttu-id="e78c7-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e78c7-111">Syntax</span></span>           | <span data-ttu-id="e78c7-112">Version 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e78c7-112">Version 1\_1</span></span> | <span data-ttu-id="e78c7-113">Version 1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="e78c7-113">Version 1\_2</span></span>     |<span data-ttu-id="e78c7-114">Version 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e78c7-114">Version  1\_3</span></span>    | <span data-ttu-id="e78c7-115">Version 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="e78c7-115">Version 1\_4</span></span>    |
|----------|-------------------------------|------------------|---------|------|------|------|
| <span data-ttu-id="e78c7-116">\_x2</span><span class="sxs-lookup"><span data-stu-id="e78c7-116">\_x2</span></span>     | <span data-ttu-id="e78c7-117">Multiplizieren mit 2</span><span class="sxs-lookup"><span data-stu-id="e78c7-117">Multiply by 2</span></span>                 | <span data-ttu-id="e78c7-118">Anweisung \_ x2</span><span class="sxs-lookup"><span data-stu-id="e78c7-118">instruction\_x2</span></span>  | <span data-ttu-id="e78c7-119">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-119">X</span></span>       | <span data-ttu-id="e78c7-120">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-120">X</span></span>    | <span data-ttu-id="e78c7-121">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-121">X</span></span>    | <span data-ttu-id="e78c7-122">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-122">X</span></span>    |
| <span data-ttu-id="e78c7-123">\_x4</span><span class="sxs-lookup"><span data-stu-id="e78c7-123">\_x4</span></span>     | <span data-ttu-id="e78c7-124">Multiplizieren mit 4</span><span class="sxs-lookup"><span data-stu-id="e78c7-124">Multiply by 4</span></span>                 | <span data-ttu-id="e78c7-125">Anweisung \_ x4</span><span class="sxs-lookup"><span data-stu-id="e78c7-125">instruction\_x4</span></span>  | <span data-ttu-id="e78c7-126">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-126">X</span></span>       | <span data-ttu-id="e78c7-127">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-127">X</span></span>    | <span data-ttu-id="e78c7-128">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-128">X</span></span>    | <span data-ttu-id="e78c7-129">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-129">X</span></span>    |
| <span data-ttu-id="e78c7-130">\_x8</span><span class="sxs-lookup"><span data-stu-id="e78c7-130">\_x8</span></span>     | <span data-ttu-id="e78c7-131">Multiplizieren mit 8</span><span class="sxs-lookup"><span data-stu-id="e78c7-131">Multiply by 8</span></span>                 | <span data-ttu-id="e78c7-132">Anweisung \_ x8</span><span class="sxs-lookup"><span data-stu-id="e78c7-132">instruction\_x8</span></span>  |         |      |      | <span data-ttu-id="e78c7-133">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-133">X</span></span>    |
| <span data-ttu-id="e78c7-134">\_d2</span><span class="sxs-lookup"><span data-stu-id="e78c7-134">\_d2</span></span>     | <span data-ttu-id="e78c7-135">Dividieren durch 2</span><span class="sxs-lookup"><span data-stu-id="e78c7-135">Divide by 2</span></span>                   | <span data-ttu-id="e78c7-136">Anweisung \_ d2</span><span class="sxs-lookup"><span data-stu-id="e78c7-136">instruction\_d2</span></span>  | <span data-ttu-id="e78c7-137">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-137">X</span></span>       | <span data-ttu-id="e78c7-138">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-138">X</span></span>    | <span data-ttu-id="e78c7-139">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-139">X</span></span>    | <span data-ttu-id="e78c7-140">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-140">X</span></span>    |
| <span data-ttu-id="e78c7-141">\_d4</span><span class="sxs-lookup"><span data-stu-id="e78c7-141">\_d4</span></span>     | <span data-ttu-id="e78c7-142">Dividieren durch 4</span><span class="sxs-lookup"><span data-stu-id="e78c7-142">Divide by 4</span></span>                   | <span data-ttu-id="e78c7-143">Anweisung \_ d4</span><span class="sxs-lookup"><span data-stu-id="e78c7-143">instruction\_d4</span></span>  |         |      |      | <span data-ttu-id="e78c7-144">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-144">X</span></span>    |
| <span data-ttu-id="e78c7-145">\_d8</span><span class="sxs-lookup"><span data-stu-id="e78c7-145">\_d8</span></span>     | <span data-ttu-id="e78c7-146">Dividieren durch 8</span><span class="sxs-lookup"><span data-stu-id="e78c7-146">Divide by 8</span></span>                   | <span data-ttu-id="e78c7-147">Anweisung \_ d8</span><span class="sxs-lookup"><span data-stu-id="e78c7-147">instruction\_d8</span></span>  |         |      |      | <span data-ttu-id="e78c7-148">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-148">X</span></span>    |
| <span data-ttu-id="e78c7-149">\_sat</span><span class="sxs-lookup"><span data-stu-id="e78c7-149">\_sat</span></span>    | <span data-ttu-id="e78c7-150">Saturate (Klammer von 0 und 1)</span><span class="sxs-lookup"><span data-stu-id="e78c7-150">Saturate (clamp from 0 and 1)</span></span> | <span data-ttu-id="e78c7-151">\_Anweisungs-Sat</span><span class="sxs-lookup"><span data-stu-id="e78c7-151">instruction\_sat</span></span> | <span data-ttu-id="e78c7-152">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-152">X</span></span>       | <span data-ttu-id="e78c7-153">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-153">X</span></span>    | <span data-ttu-id="e78c7-154">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-154">X</span></span>    | <span data-ttu-id="e78c7-155">X</span><span class="sxs-lookup"><span data-stu-id="e78c7-155">X</span></span>    |



 

-   <span data-ttu-id="e78c7-156">Der Multiplikationsmodifizierer multipliziert die Registerdaten nach dem Lesen mit einer Potenz von zwei.</span><span class="sxs-lookup"><span data-stu-id="e78c7-156">The multiply modifier multiplies the register data by a power of two after it is read.</span></span> <span data-ttu-id="e78c7-157">Dies entspricht einer Verschiebung nach links.</span><span class="sxs-lookup"><span data-stu-id="e78c7-157">This is the same as a shift left.</span></span>
-   <span data-ttu-id="e78c7-158">Der Divisionsmodifizierer dividiert die Registerdaten durch eine Potenz von zwei, nachdem sie gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="e78c7-158">The divide modifier divides the register data by a power of two after it is read.</span></span> <span data-ttu-id="e78c7-159">Dies entspricht einer Verschiebung nach rechts.</span><span class="sxs-lookup"><span data-stu-id="e78c7-159">This is the same as a shift right.</span></span>
-   <span data-ttu-id="e78c7-160">Mit dem Saturate-Modifizierer wird der Bereich der Registerwerte von 0 (null) bis 1 (1) klammern.</span><span class="sxs-lookup"><span data-stu-id="e78c7-160">The saturate modifier clamps the range of register values from zero to one.</span></span>

<span data-ttu-id="e78c7-161">Anweisungsmodifizierer können für arithmetische Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e78c7-161">Instruction modifiers can be used on arithmetic instructions.</span></span> <span data-ttu-id="e78c7-162">Sie dürfen nicht für Texturadressanweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e78c7-162">They may not be used on texture address instructions.</span></span>

<span data-ttu-id="e78c7-163">Multiplikationsmodifizierer</span><span class="sxs-lookup"><span data-stu-id="e78c7-163">Multiply modifier</span></span>

<span data-ttu-id="e78c7-164">In diesem Beispiel wird das Zielregister (dest) mit der Summe der beiden Farben in den Quellopernden (src0 und src1) geladen und das Ergebnis mit zwei multipliziert.</span><span class="sxs-lookup"><span data-stu-id="e78c7-164">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and multiplies the result by two.</span></span>


```
add_x2 dest, src0, src1
```



<span data-ttu-id="e78c7-165">In diesem Beispiel werden zwei Anweisungsmodifizierer kombiniert.</span><span class="sxs-lookup"><span data-stu-id="e78c7-165">This example combines two instruction modifiers.</span></span> <span data-ttu-id="e78c7-166">Zunächst werden zwei Farben in den Quellopernden (src0 und src1) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e78c7-166">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="e78c7-167">Das Ergebnis wird dann mit zwei multipliziert und für jede Komponente zwischen 0,0 und 1,0 gebunden.</span><span class="sxs-lookup"><span data-stu-id="e78c7-167">The result is then multiplied by two, and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="e78c7-168">Das Ergebnis wird im Zielregister gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e78c7-168">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



<span data-ttu-id="e78c7-169">Division-Modifizierer</span><span class="sxs-lookup"><span data-stu-id="e78c7-169">Divide modifier</span></span>

<span data-ttu-id="e78c7-170">In diesem Beispiel wird das Zielregister (dest) mit der Summe der beiden Farben in den Quellopernden (src0 und src1) geladen und das Ergebnis durch zwei dividiert.</span><span class="sxs-lookup"><span data-stu-id="e78c7-170">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and divides the result by two.</span></span>


```
add_d2 dest, src0, src1
```



<span data-ttu-id="e78c7-171">Saturate-Modifizierer</span><span class="sxs-lookup"><span data-stu-id="e78c7-171">Saturate modifier</span></span>

<span data-ttu-id="e78c7-172">Bei arithmetischen Anweisungen klammern die Sättigungsmodifizierer das Ergebnis dieser Anweisung in den Bereich von 0,0 bis 1,0 für jede Komponente ein.</span><span class="sxs-lookup"><span data-stu-id="e78c7-172">For arithmetic instructions, the saturation modifier clamps the result of this instruction into the range 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="e78c7-173">Im folgenden Beispiel wird die Verwendung dieses Anweisungsmodifizierer veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e78c7-173">The following example shows how to use this instruction modifier.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



<span data-ttu-id="e78c7-174">Dieser Vorgang tritt nach jedem Multiplikations- oder Divisionsanweisungsmodifizierer auf.</span><span class="sxs-lookup"><span data-stu-id="e78c7-174">This operation occurs after any multiply or divide instruction modifier.</span></span> <span data-ttu-id="e78c7-175">\_sat wird am häufigsten verwendet, um Punktproduktergebnisse zu klammern.</span><span class="sxs-lookup"><span data-stu-id="e78c7-175">\_sat is most often used to clamp dot product results.</span></span> <span data-ttu-id="e78c7-176">Sie ermöglicht jedoch auch eine konsistente Emulation von Multipass-Methoden, bei denen sich der Framepuffer immer im Bereich von 0 bis 1 und in der Multitexture-Syntax von DirectX 6 und 7.0 befindet, in der die Sättigung in jeder Phase definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e78c7-176">However, it also enables consistent emulation of multipass methods where the frame buffer is always in the range 0 to 1, and of DirectX 6 and 7.0 multitexture syntax, in which saturation is defined to occur at every stage.</span></span>

<span data-ttu-id="e78c7-177">In diesem Beispiel wird das Zielregister (dest) mit der Summe der beiden Farben in den Quellopernden (src0 und src1) geladen und das Ergebnis für jede Komponente in den Bereich von 0,0 bis 1,0 eingebunden.</span><span class="sxs-lookup"><span data-stu-id="e78c7-177">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1), and clamps the result into the range 0.0 to 1.0 for each component.</span></span>


```
add_sat dest, src0, src1
```



<span data-ttu-id="e78c7-178">In diesem Beispiel werden zwei Anweisungsmodifizierer kombiniert.</span><span class="sxs-lookup"><span data-stu-id="e78c7-178">This example combines two instruction modifiers.</span></span> <span data-ttu-id="e78c7-179">Zunächst werden zwei Farben in den Quellopernden (src0 und src1) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e78c7-179">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="e78c7-180">Das Ergebnis wird mit zwei multipliziert und für jede Komponente zwischen 0,0 und 1,0 gebunden.</span><span class="sxs-lookup"><span data-stu-id="e78c7-180">The result is multiplied by two and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="e78c7-181">Das Ergebnis wird im Zielregister gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e78c7-181">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a><span data-ttu-id="e78c7-182">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e78c7-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e78c7-183">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="e78c7-183">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




