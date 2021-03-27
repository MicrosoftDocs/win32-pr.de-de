---
title: if_comp-PS
description: Startet, wenn bool-PS... Else-PS... der enumerationsblock "enumdif-PS" mit einer Bedingung, die auf Werten basiert, die in einem Shader berechnet werden können. Diese Anweisung wird verwendet, um einen Codeblock auf der Grundlage einer Bedingung zu überspringen.
ms.assetid: a641e347-df28-4a3f-a461-0b6aee758e59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: db30983c83bc7d66e06befd07f4eb1dcdc9b21ea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719350"
---
# <a name="if_comp---ps"></a><span data-ttu-id="a2ad0-104">Wenn \_ Comp-PS</span><span class="sxs-lookup"><span data-stu-id="a2ad0-104">if\_comp - ps</span></span>

<span data-ttu-id="a2ad0-105">Startet, [Wenn bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... der [enumerationsblock "enumdif-PS](endif---ps.md) " mit einer Bedingung, die auf Werten basiert, die in einem Shader berechnet werden können.</span><span class="sxs-lookup"><span data-stu-id="a2ad0-105">Start an [if bool - ps](if-bool---ps.md)...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) block, with a condition based on values that could be computed in a shader.</span></span> <span data-ttu-id="a2ad0-106">Diese Anweisung wird verwendet, um einen Codeblock auf der Grundlage einer Bedingung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="a2ad0-106">This instruction is used to skip a block of code, based on a condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2ad0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2ad0-107">Syntax</span></span>



| <span data-ttu-id="a2ad0-108">If \_ Comp src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="a2ad0-108">if\_comp src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="a2ad0-109">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="a2ad0-109">Where:</span></span>

-   <span data-ttu-id="a2ad0-110">\_comp ist ein Vergleich zwischen den beiden Quell Registern.</span><span class="sxs-lookup"><span data-stu-id="a2ad0-110">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="a2ad0-111">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="a2ad0-111">It can be one of the following:</span></span> 

    | <span data-ttu-id="a2ad0-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2ad0-112">Syntax</span></span> | <span data-ttu-id="a2ad0-113">Vergleich</span><span class="sxs-lookup"><span data-stu-id="a2ad0-113">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="a2ad0-114">\_siegt</span><span class="sxs-lookup"><span data-stu-id="a2ad0-114">\_gt</span></span>   | <span data-ttu-id="a2ad0-115">Größer als</span><span class="sxs-lookup"><span data-stu-id="a2ad0-115">Greater than</span></span>          |
    | <span data-ttu-id="a2ad0-116">\_General</span><span class="sxs-lookup"><span data-stu-id="a2ad0-116">\_lt</span></span>   | <span data-ttu-id="a2ad0-117">Kleiner als</span><span class="sxs-lookup"><span data-stu-id="a2ad0-117">Less than</span></span>             |
    | <span data-ttu-id="a2ad0-118">\_Färbung</span><span class="sxs-lookup"><span data-stu-id="a2ad0-118">\_ge</span></span>   | <span data-ttu-id="a2ad0-119">Größer als oder gleich</span><span class="sxs-lookup"><span data-stu-id="a2ad0-119">Greater than or equal</span></span> |
    | <span data-ttu-id="a2ad0-120">\_Kirchturm</span><span class="sxs-lookup"><span data-stu-id="a2ad0-120">\_le</span></span>   | <span data-ttu-id="a2ad0-121">Kleiner als oder gleich</span><span class="sxs-lookup"><span data-stu-id="a2ad0-121">Less than or equal</span></span>    |
    | <span data-ttu-id="a2ad0-122">\_stecken</span><span class="sxs-lookup"><span data-stu-id="a2ad0-122">\_eq</span></span>   | <span data-ttu-id="a2ad0-123">Gleich</span><span class="sxs-lookup"><span data-stu-id="a2ad0-123">Equal to</span></span>              |
    | <span data-ttu-id="a2ad0-124">\_NES</span><span class="sxs-lookup"><span data-stu-id="a2ad0-124">\_ne</span></span>   | <span data-ttu-id="a2ad0-125">Ungleich</span><span class="sxs-lookup"><span data-stu-id="a2ad0-125">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="a2ad0-126">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="a2ad0-126">src0 is a source register.</span></span> <span data-ttu-id="a2ad0-127">Das Replizieren der Replizierung ist erforderlich, um eine Komponente auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a2ad0-127">Replicate swizzle is required to select a component.</span></span>
-   <span data-ttu-id="a2ad0-128">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="a2ad0-128">src1 is a source register.</span></span> <span data-ttu-id="a2ad0-129">Das Replizieren der Replizierung ist erforderlich, um eine Komponente auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a2ad0-129">Replicate swizzle is required to select a component.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2ad0-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2ad0-130">Remarks</span></span>



| <span data-ttu-id="a2ad0-131">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="a2ad0-131">Pixel shader versions</span></span> | <span data-ttu-id="a2ad0-132">1\_1</span><span class="sxs-lookup"><span data-stu-id="a2ad0-132">1\_1</span></span> | <span data-ttu-id="a2ad0-133">1\_2</span><span class="sxs-lookup"><span data-stu-id="a2ad0-133">1\_2</span></span> | <span data-ttu-id="a2ad0-134">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a2ad0-134">1\_3</span></span> | <span data-ttu-id="a2ad0-135">1\_4</span><span class="sxs-lookup"><span data-stu-id="a2ad0-135">1\_4</span></span> | <span data-ttu-id="a2ad0-136">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a2ad0-136">2\_0</span></span> | <span data-ttu-id="a2ad0-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a2ad0-137">2\_x</span></span> | <span data-ttu-id="a2ad0-138">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a2ad0-138">2\_sw</span></span> | <span data-ttu-id="a2ad0-139">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a2ad0-139">3\_0</span></span> | <span data-ttu-id="a2ad0-140">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a2ad0-140">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a2ad0-141">If \_ comp</span><span class="sxs-lookup"><span data-stu-id="a2ad0-141">if\_comp</span></span>              |      |      |      |      |      | <span data-ttu-id="a2ad0-142">x</span><span class="sxs-lookup"><span data-stu-id="a2ad0-142">x</span></span>    | <span data-ttu-id="a2ad0-143">x</span><span class="sxs-lookup"><span data-stu-id="a2ad0-143">x</span></span>     | <span data-ttu-id="a2ad0-144">x</span><span class="sxs-lookup"><span data-stu-id="a2ad0-144">x</span></span>    | <span data-ttu-id="a2ad0-145">x</span><span class="sxs-lookup"><span data-stu-id="a2ad0-145">x</span></span>     |



 

<span data-ttu-id="a2ad0-146">Diese Anweisung wird verwendet, um einen Codeblock auf der Grundlage einer Bedingung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="a2ad0-146">This instruction is used to skip a block of code, based on a condition.</span></span>


```
if (src0 comparison src1)
   jump to the corresponding else or endif instruction;
```



<span data-ttu-id="a2ad0-147">Achten Sie darauf, die Vergleichs Modi "gleich" und "nicht gleich" für Gleit Komma Zahlen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a2ad0-147">Be careful using the equals and not equals comparison modes on floating point numbers.</span></span> <span data-ttu-id="a2ad0-148">Da während der Ausführung von Gleit Komma Berechnungen eine Rundung stattfindet, kann der Vergleich mit einem Epsilon-Wert (kleine Zahl ungleich null) durchgeführt werden, um Fehler zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="a2ad0-148">Because rounding occurs during during floating point calculations, the comparison can be done against an epsilon value (small nonzero number) to avoid errors.</span></span>

<span data-ttu-id="a2ad0-149">Es gelten folgende Beschränkungen:</span><span class="sxs-lookup"><span data-stu-id="a2ad0-149">Restrictions include:</span></span>

-   <span data-ttu-id="a2ad0-150">Wenn \_ comp... [else-PS](else---ps.md)... [EndIf-PS-](endif---ps.md) Blöcke (zusammen mit den Prädikat- [if](if-bool---ps.md) -Blöcken) können bis zu 24 Ebenen tief verschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="a2ad0-150">if\_comp...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) blocks (along with the predicated [if](if-bool---ps.md) blocks) can be nested up to 24 layers deep.</span></span>
-   <span data-ttu-id="a2ad0-151">src0-und Quelle1-Register erfordern ein replizieren.</span><span class="sxs-lookup"><span data-stu-id="a2ad0-151">src0 and src1 registers require a replicate swizzle.</span></span>
-   <span data-ttu-id="a2ad0-152">, wenn \_ Comp-Blöcke mit einer [else-vs-](else---vs.md) oder [EndIf-vs-](endif---vs.md) Anweisung enden müssen.</span><span class="sxs-lookup"><span data-stu-id="a2ad0-152">if\_comp blocks must end with an [else - vs](else---vs.md) or [endif - vs](endif---vs.md) instruction.</span></span>
-   <span data-ttu-id="a2ad0-153">Wenn \_ comp... [else-PS](else---ps.md)... " [umdif-PS"-](endif---ps.md) Blöcke können einen Schleifen Block nicht durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="a2ad0-153">if\_comp...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) blocks cannot straddle a loop block.</span></span> <span data-ttu-id="a2ad0-154">Der if \_ Comp-Block muss sich vollständig innerhalb oder außerhalb des Schleifen Blocks befinden.</span><span class="sxs-lookup"><span data-stu-id="a2ad0-154">The if\_comp block must be completely inside or outside the loop block.</span></span>

## <a name="example"></a><span data-ttu-id="a2ad0-155">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a2ad0-155">Example</span></span>

<span data-ttu-id="a2ad0-156">Diese Anweisung stellt die bedingte dynamische Fluss Steuerung bereit.</span><span class="sxs-lookup"><span data-stu-id="a2ad0-156">This instruction provides conditional dynamic flow control.</span></span>


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="a2ad0-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a2ad0-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2ad0-158">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="a2ad0-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




