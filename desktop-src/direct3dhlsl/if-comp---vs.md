---
title: if_comp vs
description: Starten Sie einen, wenn bool-vs... Else-vs... der enumerationsblock "enumdif-vs" mit einer Bedingung, die auf Werten basiert, die in einem Shader berechnet werden können. Diese Anweisung wird verwendet, um einen Codeblock auf der Grundlage einer Bedingung zu überspringen.
ms.assetid: a3fe93c6-be26-4216-a601-3be52a74be06
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dadbe9620367efc75f821a711de89eb3498d247f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992959"
---
# <a name="if_comp---vs"></a><span data-ttu-id="4aad9-104">Wenn \_ Comp-vs</span><span class="sxs-lookup"><span data-stu-id="4aad9-104">if\_comp - vs</span></span>

<span data-ttu-id="4aad9-105">Starten Sie einen, [Wenn bool-vs](if-bool---vs.md)... [else-vs](else---vs.md)... der [enumerationsblock "enumdif-vs](endif---vs.md) " mit einer Bedingung, die auf Werten basiert, die in einem Shader berechnet werden können.</span><span class="sxs-lookup"><span data-stu-id="4aad9-105">Start an [if bool - vs](if-bool---vs.md)...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) block, with a condition based on values that could be computed in a shader.</span></span> <span data-ttu-id="4aad9-106">Diese Anweisung wird verwendet, um einen Codeblock auf der Grundlage einer Bedingung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="4aad9-106">This instruction is used to skip a block of code, based on a condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aad9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4aad9-107">Syntax</span></span>



| <span data-ttu-id="4aad9-108">If \_ Comp src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="4aad9-108">if\_comp src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="4aad9-109">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="4aad9-109">Where:</span></span>

-   <span data-ttu-id="4aad9-110">\_comp ist ein Vergleich zwischen den beiden Quell Registern.</span><span class="sxs-lookup"><span data-stu-id="4aad9-110">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="4aad9-111">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="4aad9-111">It can be one of the following:</span></span> 

    | <span data-ttu-id="4aad9-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="4aad9-112">Syntax</span></span> | <span data-ttu-id="4aad9-113">Vergleich</span><span class="sxs-lookup"><span data-stu-id="4aad9-113">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="4aad9-114">\_siegt</span><span class="sxs-lookup"><span data-stu-id="4aad9-114">\_gt</span></span>   | <span data-ttu-id="4aad9-115">Größer als</span><span class="sxs-lookup"><span data-stu-id="4aad9-115">Greater than</span></span>          |
    | <span data-ttu-id="4aad9-116">\_General</span><span class="sxs-lookup"><span data-stu-id="4aad9-116">\_lt</span></span>   | <span data-ttu-id="4aad9-117">Kleiner als</span><span class="sxs-lookup"><span data-stu-id="4aad9-117">Less than</span></span>             |
    | <span data-ttu-id="4aad9-118">\_Färbung</span><span class="sxs-lookup"><span data-stu-id="4aad9-118">\_ge</span></span>   | <span data-ttu-id="4aad9-119">Größer als oder gleich</span><span class="sxs-lookup"><span data-stu-id="4aad9-119">Greater than or equal</span></span> |
    | <span data-ttu-id="4aad9-120">\_Kirchturm</span><span class="sxs-lookup"><span data-stu-id="4aad9-120">\_le</span></span>   | <span data-ttu-id="4aad9-121">Kleiner als oder gleich</span><span class="sxs-lookup"><span data-stu-id="4aad9-121">Less than or equal</span></span>    |
    | <span data-ttu-id="4aad9-122">\_stecken</span><span class="sxs-lookup"><span data-stu-id="4aad9-122">\_eq</span></span>   | <span data-ttu-id="4aad9-123">Gleich</span><span class="sxs-lookup"><span data-stu-id="4aad9-123">Equal to</span></span>              |
    | <span data-ttu-id="4aad9-124">\_NES</span><span class="sxs-lookup"><span data-stu-id="4aad9-124">\_ne</span></span>   | <span data-ttu-id="4aad9-125">Ungleich</span><span class="sxs-lookup"><span data-stu-id="4aad9-125">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="4aad9-126">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="4aad9-126">src0 is a source register.</span></span> <span data-ttu-id="4aad9-127">Das Replizieren der Replizierung ist erforderlich, um eine Komponente auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="4aad9-127">Replicate swizzle is required to select a component.</span></span>
-   <span data-ttu-id="4aad9-128">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="4aad9-128">src1 is a source register.</span></span> <span data-ttu-id="4aad9-129">Das Replizieren der Replizierung ist erforderlich, um eine Komponente auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="4aad9-129">Replicate swizzle is required to select a component.</span></span>

## <a name="remarks"></a><span data-ttu-id="4aad9-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4aad9-130">Remarks</span></span>



| <span data-ttu-id="4aad9-131">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="4aad9-131">Vertex shader versions</span></span> | <span data-ttu-id="4aad9-132">1\_1</span><span class="sxs-lookup"><span data-stu-id="4aad9-132">1\_1</span></span> | <span data-ttu-id="4aad9-133">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4aad9-133">2\_0</span></span> | <span data-ttu-id="4aad9-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4aad9-134">2\_x</span></span> | <span data-ttu-id="4aad9-135">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4aad9-135">2\_sw</span></span> | <span data-ttu-id="4aad9-136">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4aad9-136">3\_0</span></span> | <span data-ttu-id="4aad9-137">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4aad9-137">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="4aad9-138">If \_ comp</span><span class="sxs-lookup"><span data-stu-id="4aad9-138">if\_comp</span></span>               |      |      | <span data-ttu-id="4aad9-139">x</span><span class="sxs-lookup"><span data-stu-id="4aad9-139">x</span></span>    | <span data-ttu-id="4aad9-140">x</span><span class="sxs-lookup"><span data-stu-id="4aad9-140">x</span></span>     | <span data-ttu-id="4aad9-141">x</span><span class="sxs-lookup"><span data-stu-id="4aad9-141">x</span></span>    | <span data-ttu-id="4aad9-142">x</span><span class="sxs-lookup"><span data-stu-id="4aad9-142">x</span></span>     |



 

<span data-ttu-id="4aad9-143">Diese Anweisung wird verwendet, um einen Codeblock auf der Grundlage einer Bedingung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="4aad9-143">This instruction is used to skip a block of code, based on a condition.</span></span>


```
if_lt src0, src1
   jump to the corresponding else or endif instruction;
```



<span data-ttu-id="4aad9-144">Achten Sie darauf, die Vergleichs Modi "gleich" und "nicht gleich" für Gleit Komma Zahlen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4aad9-144">Be careful using the equals and not equals comparison modes on floating point numbers.</span></span> <span data-ttu-id="4aad9-145">Da während der Ausführung von Gleit Komma Berechnungen eine Rundung stattfindet, kann der Vergleich mit einem Epsilon-Wert (kleine Zahl ungleich null) durchgeführt werden, um Fehler zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="4aad9-145">Because rounding occurs during during floating point calculations, the comparison can be done against an epsilon value (small nonzero number) to avoid errors.</span></span>

<span data-ttu-id="4aad9-146">Es gelten folgende Beschränkungen:</span><span class="sxs-lookup"><span data-stu-id="4aad9-146">Restrictions include:</span></span>

-   <span data-ttu-id="4aad9-147">Wenn \_ comp... [else-vs](else---vs.md)... [EndIf-vs-](endif---vs.md) Blöcke (zusammen mit den Prädikat-if-Blöcken) können bis zu 24 Ebenen tief verschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="4aad9-147">if\_comp...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) blocks (along with the predicated if blocks) can be nested up to 24 layers deep.</span></span>
-   <span data-ttu-id="4aad9-148">src0-und Quelle1-Register erfordern ein replizieren.</span><span class="sxs-lookup"><span data-stu-id="4aad9-148">src0 and src1 registers require a replicate swizzle.</span></span>
-   <span data-ttu-id="4aad9-149">, wenn \_ Comp-Blöcke mit einer [else-vs-](else---vs.md) oder [EndIf-vs-](endif---vs.md) Anweisung enden müssen.</span><span class="sxs-lookup"><span data-stu-id="4aad9-149">if\_comp blocks must end with an [else - vs](else---vs.md) or [endif - vs](endif---vs.md) instruction.</span></span>
-   <span data-ttu-id="4aad9-150">Wenn \_ comp... [else-vs](else---vs.md)... " [umdif-vs-](endif---vs.md) Blöcke" können einen Schleifen Block nicht durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="4aad9-150">if\_comp...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) blocks cannot straddle a loop block.</span></span> <span data-ttu-id="4aad9-151">Der if \_ Comp-Block muss sich vollständig innerhalb oder außerhalb des [Schleifen-vs-](loop---vs.md) Blocks befinden.</span><span class="sxs-lookup"><span data-stu-id="4aad9-151">The if\_comp block must be completely inside, or outside the [loop - vs](loop---vs.md) block.</span></span>

## <a name="example"></a><span data-ttu-id="4aad9-152">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4aad9-152">Example</span></span>

<span data-ttu-id="4aad9-153">Diese Anweisung stellt die bedingte dynamische Fluss Steuerung bereit.</span><span class="sxs-lookup"><span data-stu-id="4aad9-153">This instruction provides conditional dynamic flow control.</span></span>


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="4aad9-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4aad9-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4aad9-155">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="4aad9-155">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




