---
title: Modifizierer für ps_1_X
description: Anweisungsmodifizierer beeinflussen das Ergebnis der Anweisung, bevor sie in das Zielregister geschrieben wird. Erfahren Sie mehr über Modifizierer ps_1_X.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c97196040a8f5f9888cb2fb354dcc18ca3743c7
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988725"
---
# <a name="modifiers-for-ps_1_x"></a><span data-ttu-id="f1b08-104">Modifizierer für ps \_ 1 \_ X</span><span class="sxs-lookup"><span data-stu-id="f1b08-104">Modifiers for ps\_1\_X</span></span>

<span data-ttu-id="f1b08-105">Anweisungsmodifizierer beeinflussen das Ergebnis der Anweisung, bevor sie in das Zielregister geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f1b08-105">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span> <span data-ttu-id="f1b08-106">Verwenden Sie sie beispielsweise, um das Ergebnis durch den Faktor 2 zu multiplizieren oder zu dividieren oder um das Ergebnis zwischen 0 und 1 zu klammern.</span><span class="sxs-lookup"><span data-stu-id="f1b08-106">For instance, use them to multiply or divide the result by a factor of two, or to clamp the result between zero and one.</span></span> <span data-ttu-id="f1b08-107">Anweisungsmodifizierer werden angewendet, nachdem die Anweisung ausgeführt wurde, aber bevor das Ergebnis in das Zielregister geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f1b08-107">Instruction modifiers are applied after the instruction runs but before writing the result to the destination register.</span></span>

<span data-ttu-id="f1b08-108">Eine Liste der Modifizierer ist unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f1b08-108">A list of the modifiers is shown below.</span></span>



| <span data-ttu-id="f1b08-109">Modifizierer</span><span class="sxs-lookup"><span data-stu-id="f1b08-109">Modifier</span></span> | <span data-ttu-id="f1b08-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1b08-110">Description</span></span>                   | <span data-ttu-id="f1b08-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1b08-111">Syntax</span></span>           | <span data-ttu-id="f1b08-112">Version</span><span class="sxs-lookup"><span data-stu-id="f1b08-112">Version</span></span> |      |      |      |
|----------|-------------------------------|------------------|---------|------|------|------|
|          |                               |                  | <span data-ttu-id="f1b08-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="f1b08-113">1\_1</span></span>    | <span data-ttu-id="f1b08-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="f1b08-114">1\_2</span></span> | <span data-ttu-id="f1b08-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f1b08-115">1\_3</span></span> | <span data-ttu-id="f1b08-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="f1b08-116">1\_4</span></span> |
| <span data-ttu-id="f1b08-117">\_x2</span><span class="sxs-lookup"><span data-stu-id="f1b08-117">\_x2</span></span>     | <span data-ttu-id="f1b08-118">Multiplizieren mit 2</span><span class="sxs-lookup"><span data-stu-id="f1b08-118">Multiply by 2</span></span>                 | <span data-ttu-id="f1b08-119">Anweisung \_ x2</span><span class="sxs-lookup"><span data-stu-id="f1b08-119">instruction\_x2</span></span>  | <span data-ttu-id="f1b08-120">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-120">X</span></span>       | <span data-ttu-id="f1b08-121">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-121">X</span></span>    | <span data-ttu-id="f1b08-122">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-122">X</span></span>    | <span data-ttu-id="f1b08-123">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-123">X</span></span>    |
| <span data-ttu-id="f1b08-124">\_x4</span><span class="sxs-lookup"><span data-stu-id="f1b08-124">\_x4</span></span>     | <span data-ttu-id="f1b08-125">Multiplizieren mit 4</span><span class="sxs-lookup"><span data-stu-id="f1b08-125">Multiply by 4</span></span>                 | <span data-ttu-id="f1b08-126">Anweisung \_ x4</span><span class="sxs-lookup"><span data-stu-id="f1b08-126">instruction\_x4</span></span>  | <span data-ttu-id="f1b08-127">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-127">X</span></span>       | <span data-ttu-id="f1b08-128">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-128">X</span></span>    | <span data-ttu-id="f1b08-129">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-129">X</span></span>    | <span data-ttu-id="f1b08-130">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-130">X</span></span>    |
| <span data-ttu-id="f1b08-131">\_x8</span><span class="sxs-lookup"><span data-stu-id="f1b08-131">\_x8</span></span>     | <span data-ttu-id="f1b08-132">Multiplizieren mit 8</span><span class="sxs-lookup"><span data-stu-id="f1b08-132">Multiply by 8</span></span>                 | <span data-ttu-id="f1b08-133">Anweisung \_ x8</span><span class="sxs-lookup"><span data-stu-id="f1b08-133">instruction\_x8</span></span>  |         |      |      | <span data-ttu-id="f1b08-134">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-134">X</span></span>    |
| <span data-ttu-id="f1b08-135">\_d2</span><span class="sxs-lookup"><span data-stu-id="f1b08-135">\_d2</span></span>     | <span data-ttu-id="f1b08-136">Division durch 2</span><span class="sxs-lookup"><span data-stu-id="f1b08-136">Divide by 2</span></span>                   | <span data-ttu-id="f1b08-137">Anweisung \_ d2</span><span class="sxs-lookup"><span data-stu-id="f1b08-137">instruction\_d2</span></span>  | <span data-ttu-id="f1b08-138">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-138">X</span></span>       | <span data-ttu-id="f1b08-139">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-139">X</span></span>    | <span data-ttu-id="f1b08-140">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-140">X</span></span>    | <span data-ttu-id="f1b08-141">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-141">X</span></span>    |
| <span data-ttu-id="f1b08-142">\_d4</span><span class="sxs-lookup"><span data-stu-id="f1b08-142">\_d4</span></span>     | <span data-ttu-id="f1b08-143">Division durch 4</span><span class="sxs-lookup"><span data-stu-id="f1b08-143">Divide by 4</span></span>                   | <span data-ttu-id="f1b08-144">Anweisung \_ d4</span><span class="sxs-lookup"><span data-stu-id="f1b08-144">instruction\_d4</span></span>  |         |      |      | <span data-ttu-id="f1b08-145">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-145">X</span></span>    |
| <span data-ttu-id="f1b08-146">\_d8</span><span class="sxs-lookup"><span data-stu-id="f1b08-146">\_d8</span></span>     | <span data-ttu-id="f1b08-147">Division durch 8</span><span class="sxs-lookup"><span data-stu-id="f1b08-147">Divide by 8</span></span>                   | <span data-ttu-id="f1b08-148">Anweisung \_ d8</span><span class="sxs-lookup"><span data-stu-id="f1b08-148">instruction\_d8</span></span>  |         |      |      | <span data-ttu-id="f1b08-149">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-149">X</span></span>    |
| <span data-ttu-id="f1b08-150">\_Sat</span><span class="sxs-lookup"><span data-stu-id="f1b08-150">\_sat</span></span>    | <span data-ttu-id="f1b08-151">Saturate (Klammer von 0 und 1)</span><span class="sxs-lookup"><span data-stu-id="f1b08-151">Saturate (clamp from 0 and 1)</span></span> | <span data-ttu-id="f1b08-152">Anweisung \_ sa</span><span class="sxs-lookup"><span data-stu-id="f1b08-152">instruction\_sat</span></span> | <span data-ttu-id="f1b08-153">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-153">X</span></span>       | <span data-ttu-id="f1b08-154">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-154">X</span></span>    | <span data-ttu-id="f1b08-155">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-155">X</span></span>    | <span data-ttu-id="f1b08-156">X</span><span class="sxs-lookup"><span data-stu-id="f1b08-156">X</span></span>    |



 

-   <span data-ttu-id="f1b08-157">Der Multiplikationsmodifizierer multipliziert die Registerdaten mit einer Zweierleistung, nachdem sie gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="f1b08-157">The multiply modifier multiplies the register data by a power of two after it is read.</span></span> <span data-ttu-id="f1b08-158">Dies ist identisch mit einer Verschiebung nach links.</span><span class="sxs-lookup"><span data-stu-id="f1b08-158">This is the same as a shift left.</span></span>
-   <span data-ttu-id="f1b08-159">Der Divide-Modifizierer dividiert die Registerdaten nach dem Lesen durch eine Zweierkraft.</span><span class="sxs-lookup"><span data-stu-id="f1b08-159">The divide modifier divides the register data by a power of two after it is read.</span></span> <span data-ttu-id="f1b08-160">Dies ist identisch mit einer Verschiebung nach rechts.</span><span class="sxs-lookup"><span data-stu-id="f1b08-160">This is the same as a shift right.</span></span>
-   <span data-ttu-id="f1b08-161">Der Saturate-Modifizierer klammert den Bereich der Registerwerte von 0 bis 1.</span><span class="sxs-lookup"><span data-stu-id="f1b08-161">The saturate modifier clamps the range of register values from zero to one.</span></span>

<span data-ttu-id="f1b08-162">Anweisungsmodifizierer können für arithmetische Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1b08-162">Instruction modifiers can be used on arithmetic instructions.</span></span> <span data-ttu-id="f1b08-163">Sie dürfen nicht für Texturadressenanweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1b08-163">They may not be used on texture address instructions.</span></span>

<span data-ttu-id="f1b08-164">Multiplikationsmodifizierer</span><span class="sxs-lookup"><span data-stu-id="f1b08-164">Multiply modifier</span></span>

<span data-ttu-id="f1b08-165">In diesem Beispiel wird das Zielregister (dest) mit der Summe der beiden Farben in den Quellopernden (src0 und src1) geladen und das Ergebnis mit zwei multipliziert.</span><span class="sxs-lookup"><span data-stu-id="f1b08-165">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and multiplies the result by two.</span></span>


```
add_x2 dest, src0, src1
```



<span data-ttu-id="f1b08-166">In diesem Beispiel werden zwei Anweisungsmodifizierer kombiniert.</span><span class="sxs-lookup"><span data-stu-id="f1b08-166">This example combines two instruction modifiers.</span></span> <span data-ttu-id="f1b08-167">Zunächst werden zwei Farben in den Quellopernden (src0 und src1) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f1b08-167">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="f1b08-168">Das Ergebnis wird dann mit zwei multipliziert und für jede Komponente zwischen 0,0 und 1,0 geklammert.</span><span class="sxs-lookup"><span data-stu-id="f1b08-168">The result is then multiplied by two, and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="f1b08-169">Das Ergebnis wird im Zielregister gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f1b08-169">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



<span data-ttu-id="f1b08-170">Divide-Modifizierer</span><span class="sxs-lookup"><span data-stu-id="f1b08-170">Divide modifier</span></span>

<span data-ttu-id="f1b08-171">In diesem Beispiel wird das Zielregister (dest) mit der Summe der beiden Farben in den Quellopernden (src0 und src1) geladen und das Ergebnis durch zwei dividiert.</span><span class="sxs-lookup"><span data-stu-id="f1b08-171">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and divides the result by two.</span></span>


```
add_d2 dest, src0, src1
```



<span data-ttu-id="f1b08-172">Saturate-Modifizierer</span><span class="sxs-lookup"><span data-stu-id="f1b08-172">Saturate modifier</span></span>

<span data-ttu-id="f1b08-173">Bei arithmetischen Anweisungen klammert der Sättigungsmodifizierer das Ergebnis dieser Anweisung für jede Komponente in den Bereich 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="f1b08-173">For arithmetic instructions, the saturation modifier clamps the result of this instruction into the range 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="f1b08-174">Im folgenden Beispiel wird die Verwendung dieses Anweisungsmodifizierers veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f1b08-174">The following example shows how to use this instruction modifier.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



<span data-ttu-id="f1b08-175">Dieser Vorgang erfolgt nach jedem Multiplikations- oder Divisionsanweisungsmodifizierer.</span><span class="sxs-lookup"><span data-stu-id="f1b08-175">This operation occurs after any multiply or divide instruction modifier.</span></span> <span data-ttu-id="f1b08-176">\_Sat wird am häufigsten verwendet, um Punktproduktergebnisse zu klammern.</span><span class="sxs-lookup"><span data-stu-id="f1b08-176">\_sat is most often used to clamp dot product results.</span></span> <span data-ttu-id="f1b08-177">Sie ermöglicht jedoch auch eine konsistente Emulation von Multipassmethoden, bei denen der Framepuffer immer im Bereich von 0 bis 1 liegt, und der DirectX 6- und 7.0-Multitextursyntax, bei der die Sättigung in jeder Phase definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f1b08-177">However, it also enables consistent emulation of multipass methods where the frame buffer is always in the range 0 to 1, and of DirectX 6 and 7.0 multitexture syntax, in which saturation is defined to occur at every stage.</span></span>

<span data-ttu-id="f1b08-178">In diesem Beispiel wird das Zielregister (dest) mit der Summe der beiden Farben in den Quellopernden (src0 und src1) geladen und das Ergebnis für jede Komponente in den Bereich 0,0 bis 1,0 klammert.</span><span class="sxs-lookup"><span data-stu-id="f1b08-178">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1), and clamps the result into the range 0.0 to 1.0 for each component.</span></span>


```
add_sat dest, src0, src1
```



<span data-ttu-id="f1b08-179">In diesem Beispiel werden zwei Anweisungsmodifizierer kombiniert.</span><span class="sxs-lookup"><span data-stu-id="f1b08-179">This example combines two instruction modifiers.</span></span> <span data-ttu-id="f1b08-180">Zunächst werden zwei Farben in den Quellopernden (src0 und src1) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f1b08-180">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="f1b08-181">Das Ergebnis wird mit zwei multipliziert und für jede Komponente zwischen 0,0 und 1,0 geklammert.</span><span class="sxs-lookup"><span data-stu-id="f1b08-181">The result is multiplied by two and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="f1b08-182">Das Ergebnis wird im Zielregister gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f1b08-182">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a><span data-ttu-id="f1b08-183">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f1b08-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1b08-184">Anweisungen zum Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="f1b08-184">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




