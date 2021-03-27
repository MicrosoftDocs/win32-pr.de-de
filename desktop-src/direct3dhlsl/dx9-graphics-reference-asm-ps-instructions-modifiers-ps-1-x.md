---
title: Modifiziererer für ps_1_X
description: Anweisungsmodifiziererer wirken sich auf das Ergebnis der Anweisung aus, bevor Sie in das Ziel Register geschrieben wird.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bbc8a9b13f7ffc29cf84bc839409f29bea6c8c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856959"
---
# <a name="modifiers-for-ps_1_x"></a><span data-ttu-id="99937-103">Modifiziererer für PS \_ 1 \_ X</span><span class="sxs-lookup"><span data-stu-id="99937-103">Modifiers for ps\_1\_X</span></span>

<span data-ttu-id="99937-104">Anweisungsmodifiziererer wirken sich auf das Ergebnis der Anweisung aus, bevor Sie in das Ziel Register geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="99937-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span> <span data-ttu-id="99937-105">Verwenden Sie diese beispielsweise, um das Ergebnis durch einen Faktor von zwei zu multiplizieren oder aufzuteilen, oder um das Ergebnis zwischen null und eins zu binden.</span><span class="sxs-lookup"><span data-stu-id="99937-105">For instance, use them to multiply or divide the result by a factor of two, or to clamp the result between zero and one.</span></span> <span data-ttu-id="99937-106">Anweisungsmodifiziererer werden angewendet, nachdem die Anweisung ausgeführt wurde, aber bevor das Ergebnis in das Ziel Register geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="99937-106">Instruction modifiers are applied after the instruction runs but before writing the result to the destination register.</span></span>

<span data-ttu-id="99937-107">Eine Liste der Modifizierer ist unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="99937-107">A list of the modifiers is shown below.</span></span>



| <span data-ttu-id="99937-108">Modifizierer</span><span class="sxs-lookup"><span data-stu-id="99937-108">Modifier</span></span> | <span data-ttu-id="99937-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99937-109">Description</span></span>                   | <span data-ttu-id="99937-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="99937-110">Syntax</span></span>           | <span data-ttu-id="99937-111">Version</span><span class="sxs-lookup"><span data-stu-id="99937-111">Version</span></span> |      |      |      |
|----------|-------------------------------|------------------|---------|------|------|------|
|          |                               |                  | <span data-ttu-id="99937-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="99937-112">1\_1</span></span>    | <span data-ttu-id="99937-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="99937-113">1\_2</span></span> | <span data-ttu-id="99937-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="99937-114">1\_3</span></span> | <span data-ttu-id="99937-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="99937-115">1\_4</span></span> |
| <span data-ttu-id="99937-116">\_x2</span><span class="sxs-lookup"><span data-stu-id="99937-116">\_x2</span></span>     | <span data-ttu-id="99937-117">Multiplizieren um 2</span><span class="sxs-lookup"><span data-stu-id="99937-117">Multiply by 2</span></span>                 | <span data-ttu-id="99937-118">Anweisung \_ x2</span><span class="sxs-lookup"><span data-stu-id="99937-118">instruction\_x2</span></span>  | <span data-ttu-id="99937-119">X</span><span class="sxs-lookup"><span data-stu-id="99937-119">X</span></span>       | <span data-ttu-id="99937-120">X</span><span class="sxs-lookup"><span data-stu-id="99937-120">X</span></span>    | <span data-ttu-id="99937-121">X</span><span class="sxs-lookup"><span data-stu-id="99937-121">X</span></span>    | <span data-ttu-id="99937-122">X</span><span class="sxs-lookup"><span data-stu-id="99937-122">X</span></span>    |
| <span data-ttu-id="99937-123">\_x4</span><span class="sxs-lookup"><span data-stu-id="99937-123">\_x4</span></span>     | <span data-ttu-id="99937-124">Multiplizieren um 4</span><span class="sxs-lookup"><span data-stu-id="99937-124">Multiply by 4</span></span>                 | <span data-ttu-id="99937-125">Anweisung \_ X4</span><span class="sxs-lookup"><span data-stu-id="99937-125">instruction\_x4</span></span>  | <span data-ttu-id="99937-126">X</span><span class="sxs-lookup"><span data-stu-id="99937-126">X</span></span>       | <span data-ttu-id="99937-127">X</span><span class="sxs-lookup"><span data-stu-id="99937-127">X</span></span>    | <span data-ttu-id="99937-128">X</span><span class="sxs-lookup"><span data-stu-id="99937-128">X</span></span>    | <span data-ttu-id="99937-129">X</span><span class="sxs-lookup"><span data-stu-id="99937-129">X</span></span>    |
| <span data-ttu-id="99937-130">\_x8</span><span class="sxs-lookup"><span data-stu-id="99937-130">\_x8</span></span>     | <span data-ttu-id="99937-131">Multiplizieren um 8</span><span class="sxs-lookup"><span data-stu-id="99937-131">Multiply by 8</span></span>                 | <span data-ttu-id="99937-132">Anweisung \_ x8</span><span class="sxs-lookup"><span data-stu-id="99937-132">instruction\_x8</span></span>  |         |      |      | <span data-ttu-id="99937-133">X</span><span class="sxs-lookup"><span data-stu-id="99937-133">X</span></span>    |
| <span data-ttu-id="99937-134">\_D2</span><span class="sxs-lookup"><span data-stu-id="99937-134">\_d2</span></span>     | <span data-ttu-id="99937-135">Dividieren durch 2</span><span class="sxs-lookup"><span data-stu-id="99937-135">Divide by 2</span></span>                   | <span data-ttu-id="99937-136">Anweisung \_ D2</span><span class="sxs-lookup"><span data-stu-id="99937-136">instruction\_d2</span></span>  | <span data-ttu-id="99937-137">X</span><span class="sxs-lookup"><span data-stu-id="99937-137">X</span></span>       | <span data-ttu-id="99937-138">X</span><span class="sxs-lookup"><span data-stu-id="99937-138">X</span></span>    | <span data-ttu-id="99937-139">X</span><span class="sxs-lookup"><span data-stu-id="99937-139">X</span></span>    | <span data-ttu-id="99937-140">X</span><span class="sxs-lookup"><span data-stu-id="99937-140">X</span></span>    |
| <span data-ttu-id="99937-141">\_D4</span><span class="sxs-lookup"><span data-stu-id="99937-141">\_d4</span></span>     | <span data-ttu-id="99937-142">Dividieren durch 4</span><span class="sxs-lookup"><span data-stu-id="99937-142">Divide by 4</span></span>                   | <span data-ttu-id="99937-143">Anweisung \_ D4</span><span class="sxs-lookup"><span data-stu-id="99937-143">instruction\_d4</span></span>  |         |      |      | <span data-ttu-id="99937-144">X</span><span class="sxs-lookup"><span data-stu-id="99937-144">X</span></span>    |
| <span data-ttu-id="99937-145">\_D8</span><span class="sxs-lookup"><span data-stu-id="99937-145">\_d8</span></span>     | <span data-ttu-id="99937-146">Dividieren durch 8</span><span class="sxs-lookup"><span data-stu-id="99937-146">Divide by 8</span></span>                   | <span data-ttu-id="99937-147">Anweisung \_ D8</span><span class="sxs-lookup"><span data-stu-id="99937-147">instruction\_d8</span></span>  |         |      |      | <span data-ttu-id="99937-148">X</span><span class="sxs-lookup"><span data-stu-id="99937-148">X</span></span>    |
| <span data-ttu-id="99937-149">\_gesetzt</span><span class="sxs-lookup"><span data-stu-id="99937-149">\_sat</span></span>    | <span data-ttu-id="99937-150">Vollständig (Klammer zwischen 0 und 1)</span><span class="sxs-lookup"><span data-stu-id="99937-150">Saturate (clamp from 0 and 1)</span></span> | <span data-ttu-id="99937-151">Anweisung \_ Sat</span><span class="sxs-lookup"><span data-stu-id="99937-151">instruction\_sat</span></span> | <span data-ttu-id="99937-152">X</span><span class="sxs-lookup"><span data-stu-id="99937-152">X</span></span>       | <span data-ttu-id="99937-153">X</span><span class="sxs-lookup"><span data-stu-id="99937-153">X</span></span>    | <span data-ttu-id="99937-154">X</span><span class="sxs-lookup"><span data-stu-id="99937-154">X</span></span>    | <span data-ttu-id="99937-155">X</span><span class="sxs-lookup"><span data-stu-id="99937-155">X</span></span>    |



 

-   <span data-ttu-id="99937-156">Der Multiplikations Modifizierer multipliziert die Register Daten mit einer Potenz von zwei, nachdem Sie gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="99937-156">The multiply modifier multiplies the register data by a power of two after it is read.</span></span> <span data-ttu-id="99937-157">Dies ist das gleiche wie bei einer UMSCHALT links.</span><span class="sxs-lookup"><span data-stu-id="99937-157">This is the same as a shift left.</span></span>
-   <span data-ttu-id="99937-158">Der Divide-Modifizierer dividiert die Register Daten durch eine Potenz von zwei, nachdem Sie gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="99937-158">The divide modifier divides the register data by a power of two after it is read.</span></span> <span data-ttu-id="99937-159">Dies ist das gleiche wie ein UMSCHALT Recht.</span><span class="sxs-lookup"><span data-stu-id="99937-159">This is the same as a shift right.</span></span>
-   <span data-ttu-id="99937-160">Der Bezeichner "Bezeichner" bindet den Bereich der Registerwerte von 0 (null) auf 1.</span><span class="sxs-lookup"><span data-stu-id="99937-160">The saturate modifier clamps the range of register values from zero to one.</span></span>

<span data-ttu-id="99937-161">Anweisungsmodifiziererer können in arithmetischen Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99937-161">Instruction modifiers can be used on arithmetic instructions.</span></span> <span data-ttu-id="99937-162">Sie dürfen nicht in Textur Adress Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99937-162">They may not be used on texture address instructions.</span></span>

<span data-ttu-id="99937-163">Modifizierer multiplizieren</span><span class="sxs-lookup"><span data-stu-id="99937-163">Multiply modifier</span></span>

<span data-ttu-id="99937-164">In diesem Beispiel wird das Ziel Register (dest) mit der Summe der beiden Farben in den Quell Operanden (src0 und Quelle1) geladen und das Ergebnis mit zwei multipliziert.</span><span class="sxs-lookup"><span data-stu-id="99937-164">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and multiplies the result by two.</span></span>


```
add_x2 dest, src0, src1
```



<span data-ttu-id="99937-165">In diesem Beispiel werden zwei Anweisungs Modifizierer kombiniert.</span><span class="sxs-lookup"><span data-stu-id="99937-165">This example combines two instruction modifiers.</span></span> <span data-ttu-id="99937-166">Zuerst werden zwei Farben in den Quell Operanden (src0 und Quelle1) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="99937-166">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="99937-167">Das Ergebnis wird dann mit zwei multipliziert und für jede Komponente zwischen 0,0 und 1,0 gebunden.</span><span class="sxs-lookup"><span data-stu-id="99937-167">The result is then multiplied by two, and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="99937-168">Das Ergebnis wird im Ziel Register gespeichert.</span><span class="sxs-lookup"><span data-stu-id="99937-168">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



<span data-ttu-id="99937-169">Divide-Modifizierer</span><span class="sxs-lookup"><span data-stu-id="99937-169">Divide modifier</span></span>

<span data-ttu-id="99937-170">In diesem Beispiel wird das Ziel Register (dest) mit der Summe der beiden Farben in den Quell Operanden (src0 und Quelle1) geladen und das Ergebnis durch zwei dividiert.</span><span class="sxs-lookup"><span data-stu-id="99937-170">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and divides the result by two.</span></span>


```
add_d2 dest, src0, src1
```



<span data-ttu-id="99937-171">-Modifizierer</span><span class="sxs-lookup"><span data-stu-id="99937-171">Saturate modifier</span></span>

<span data-ttu-id="99937-172">Bei arithmetischen Anweisungen bindet der Sättigungs Modifizierer das Ergebnis dieser Anweisung für jede Komponente in den Bereich 0,0 bis 1,0.</span><span class="sxs-lookup"><span data-stu-id="99937-172">For arithmetic instructions, the saturation modifier clamps the result of this instruction into the range 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="99937-173">Im folgenden Beispiel wird gezeigt, wie dieser Anweisungs Modifizierer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="99937-173">The following example shows how to use this instruction modifier.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



<span data-ttu-id="99937-174">Dieser Vorgang tritt nach jedem Multiplikations-oder Teilungs Anweisungs Modifizierer auf.</span><span class="sxs-lookup"><span data-stu-id="99937-174">This operation occurs after any multiply or divide instruction modifier.</span></span> <span data-ttu-id="99937-175">\_"Sat" wird am häufigsten verwendet, um Punktprodukt Ergebnisse zu binden.</span><span class="sxs-lookup"><span data-stu-id="99937-175">\_sat is most often used to clamp dot product results.</span></span> <span data-ttu-id="99937-176">Sie ermöglicht jedoch auch eine konsistente Emulation von Multipass-Methoden, bei denen sich der Frame Puffer immer im Bereich von 0 bis 1 und in der Multitextur-Syntax von DirectX 6 und 7,0 befindet, in der die Sättigung definiert ist, die in jeder Phase auftritt.</span><span class="sxs-lookup"><span data-stu-id="99937-176">However, it also enables consistent emulation of multipass methods where the frame buffer is always in the range 0 to 1, and of DirectX 6 and 7.0 multitexture syntax, in which saturation is defined to occur at every stage.</span></span>

<span data-ttu-id="99937-177">In diesem Beispiel wird das Ziel Register (dest) mit der Summe der beiden Farben in den Quell Operanden (src0 und Quelle1) geladen, und das Ergebnis wird für jede Komponente in den Bereich 0,0 bis 1,0 geklammert.</span><span class="sxs-lookup"><span data-stu-id="99937-177">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1), and clamps the result into the range 0.0 to 1.0 for each component.</span></span>


```
add_sat dest, src0, src1
```



<span data-ttu-id="99937-178">In diesem Beispiel werden zwei Anweisungs Modifizierer kombiniert.</span><span class="sxs-lookup"><span data-stu-id="99937-178">This example combines two instruction modifiers.</span></span> <span data-ttu-id="99937-179">Zuerst werden zwei Farben in den Quell Operanden (src0 und Quelle1) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="99937-179">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="99937-180">Das Ergebnis wird mit zwei multipliziert und für jede Komponente zwischen 0,0 und 1,0 gebunden.</span><span class="sxs-lookup"><span data-stu-id="99937-180">The result is multiplied by two and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="99937-181">Das Ergebnis wird im Ziel Register gespeichert.</span><span class="sxs-lookup"><span data-stu-id="99937-181">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a><span data-ttu-id="99937-182">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="99937-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99937-183">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="99937-183">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




