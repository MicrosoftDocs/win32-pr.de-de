---
title: callnz pred-vs
description: Mit einem Prädikat wird aufgerufen, wenn nicht 0 (null). Führt einen bedingten aufrufbefehl der Anweisung aus, die durch den Bezeichnungs Index gekennzeichnet ist. Das-Prädikat verwendet einen booleschen Wert, um zu bestimmen, ob die Anweisung nicht durchgeführt werden soll.
ms.assetid: 3417f3e3-7e73-4131-8069-09c0de1469a7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3c3de590dfee56013c76402c840a959e8f9306c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038332"
---
# <a name="callnz-pred---vs"></a><span data-ttu-id="98975-105">callnz pred-vs</span><span class="sxs-lookup"><span data-stu-id="98975-105">callnz pred - vs</span></span>

<span data-ttu-id="98975-106">Mit einem Prädikat wird aufgerufen, wenn nicht 0 (null).</span><span class="sxs-lookup"><span data-stu-id="98975-106">Call if not zero, with a predicate.</span></span> <span data-ttu-id="98975-107">Führt einen bedingten aufrufbefehl der Anweisung aus, die durch den Bezeichnungs Index gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="98975-107">Performs a conditional call to the instruction marked by the label index.</span></span> <span data-ttu-id="98975-108">Das-Prädikat verwendet einen booleschen Wert, um zu bestimmen, ob die Anweisung nicht durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="98975-108">Predication uses a boolean value to determine whether of not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="98975-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="98975-109">Syntax</span></span>



| <span data-ttu-id="98975-110">callnz l \# , \[ ! \] P0. Stuben</span><span class="sxs-lookup"><span data-stu-id="98975-110">callnz l\#, \[!\]p0.{x\</span></span>|<span data-ttu-id="98975-111">Teenie</span><span class="sxs-lookup"><span data-stu-id="98975-111">y\</span></span>|<span data-ttu-id="98975-112">z</span><span class="sxs-lookup"><span data-stu-id="98975-112">z\</span></span>|<span data-ttu-id="98975-113">Löw</span><span class="sxs-lookup"><span data-stu-id="98975-113">w}</span></span> |
|----------------------------------|



 

<span data-ttu-id="98975-114">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="98975-114">where:</span></span>

-   <span data-ttu-id="98975-115">l \# ist eine [Bezeichnung-vs](label---vs.md) , die den Anfang der aufzurufenden Unterroutine markiert.</span><span class="sxs-lookup"><span data-stu-id="98975-115">l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="98975-116">\[!\] ist ein optionaler Negation-Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="98975-116">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="98975-117">P0 ist das [Prädikat Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="98975-117">p0 is the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="98975-118">{x \| y \| z \| w} ist das erforderliche Replizieren von Replizieren auf p0.</span><span class="sxs-lookup"><span data-stu-id="98975-118">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="98975-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98975-119">Remarks</span></span>



| <span data-ttu-id="98975-120">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="98975-120">Vertex shader versions</span></span> | <span data-ttu-id="98975-121">1\_1</span><span class="sxs-lookup"><span data-stu-id="98975-121">1\_1</span></span> | <span data-ttu-id="98975-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="98975-122">2\_0</span></span> | <span data-ttu-id="98975-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="98975-123">2\_x</span></span> | <span data-ttu-id="98975-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="98975-124">2\_sw</span></span> | <span data-ttu-id="98975-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="98975-125">3\_0</span></span> | <span data-ttu-id="98975-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="98975-126">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="98975-127">callnz-präd</span><span class="sxs-lookup"><span data-stu-id="98975-127">callnz pred</span></span>            |      |      | <span data-ttu-id="98975-128">x</span><span class="sxs-lookup"><span data-stu-id="98975-128">x</span></span>    | <span data-ttu-id="98975-129">x</span><span class="sxs-lookup"><span data-stu-id="98975-129">x</span></span>     | <span data-ttu-id="98975-130">x</span><span class="sxs-lookup"><span data-stu-id="98975-130">x</span></span>    | <span data-ttu-id="98975-131">x</span><span class="sxs-lookup"><span data-stu-id="98975-131">x</span></span>     |



 

<span data-ttu-id="98975-132">Diese Anweisung führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="98975-132">This instruction does the following:</span></span>


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



<span data-ttu-id="98975-133">Diese Anweisung verwendet einen Vertex-Shader-Anweisungs Slot.</span><span class="sxs-lookup"><span data-stu-id="98975-133">This instruction consumes one vertex shader instruction slot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98975-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="98975-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98975-135">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="98975-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




