---
title: callnz pred-PS
description: Ruft mit einem Prädikat auf, wenn nicht 0 (null). Führt einen bedingten aufrufbefehl der Anweisung aus, die durch den Bezeichnungs Index gekennzeichnet ist. Das-Prädikat verwendet einen booleschen Wert, um zu bestimmen, ob die Anweisung nicht durchgeführt werden soll.
ms.assetid: 9c839fc7-8b4d-4ca1-b30f-5c3f8fb45eae
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a04bd4b1bfa16d965a90b66e3956674ecb112590
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103948317"
---
# <a name="callnz-pred---ps"></a><span data-ttu-id="ea0d9-105">callnz pred-PS</span><span class="sxs-lookup"><span data-stu-id="ea0d9-105">callnz pred - ps</span></span>

<span data-ttu-id="ea0d9-106">Ruft mit einem Prädikat auf, wenn nicht 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ea0d9-106">Call with a predicate, if not zero.</span></span> <span data-ttu-id="ea0d9-107">Führt einen bedingten aufrufbefehl der Anweisung aus, die durch den Bezeichnungs Index gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="ea0d9-107">Performs a conditional call to the instruction marked by the label index.</span></span> <span data-ttu-id="ea0d9-108">Das-Prädikat verwendet einen booleschen Wert, um zu bestimmen, ob die Anweisung nicht durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea0d9-108">Predication uses a Boolean value to determine whether of not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea0d9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea0d9-109">Syntax</span></span>



| <span data-ttu-id="ea0d9-110">callnz l \# , \[ ! \] P0. Stuben</span><span class="sxs-lookup"><span data-stu-id="ea0d9-110">callnz l\#, \[!\]p0.{x\</span></span>|<span data-ttu-id="ea0d9-111">Teenie</span><span class="sxs-lookup"><span data-stu-id="ea0d9-111">y\</span></span>|<span data-ttu-id="ea0d9-112">z</span><span class="sxs-lookup"><span data-stu-id="ea0d9-112">z\</span></span>|<span data-ttu-id="ea0d9-113">Löw</span><span class="sxs-lookup"><span data-stu-id="ea0d9-113">w}</span></span> |
|----------------------------------|



 

<span data-ttu-id="ea0d9-114">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="ea0d9-114">Where:</span></span>

-   <span data-ttu-id="ea0d9-115">dabei \# ist l eine [Bezeichnung-PS](label---ps.md) , die den Anfang der aufzurufenden Unterroutine kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="ea0d9-115">where l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="ea0d9-116">\[!\] ist ein optionaler Negation-Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="ea0d9-116">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="ea0d9-117">P0 ist das Prädikat Register.</span><span class="sxs-lookup"><span data-stu-id="ea0d9-117">p0 is the predicate register.</span></span> <span data-ttu-id="ea0d9-118">Siehe [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="ea0d9-118">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="ea0d9-119">{x \| y \| z \| w} ist das erforderliche Replizieren von Replizieren auf p0.</span><span class="sxs-lookup"><span data-stu-id="ea0d9-119">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea0d9-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea0d9-120">Remarks</span></span>



| <span data-ttu-id="ea0d9-121">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="ea0d9-121">Pixel shader versions</span></span> | <span data-ttu-id="ea0d9-122">1\_1</span><span class="sxs-lookup"><span data-stu-id="ea0d9-122">1\_1</span></span> | <span data-ttu-id="ea0d9-123">1\_2</span><span class="sxs-lookup"><span data-stu-id="ea0d9-123">1\_2</span></span> | <span data-ttu-id="ea0d9-124">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ea0d9-124">1\_3</span></span> | <span data-ttu-id="ea0d9-125">1\_4</span><span class="sxs-lookup"><span data-stu-id="ea0d9-125">1\_4</span></span> | <span data-ttu-id="ea0d9-126">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ea0d9-126">2\_0</span></span> | <span data-ttu-id="ea0d9-127">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ea0d9-127">2\_x</span></span> | <span data-ttu-id="ea0d9-128">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ea0d9-128">2\_sw</span></span> | <span data-ttu-id="ea0d9-129">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ea0d9-129">3\_0</span></span> | <span data-ttu-id="ea0d9-130">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ea0d9-130">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="ea0d9-131">callnz-präd</span><span class="sxs-lookup"><span data-stu-id="ea0d9-131">callnz pred</span></span>           |      |      |      |      |      | <span data-ttu-id="ea0d9-132">x</span><span class="sxs-lookup"><span data-stu-id="ea0d9-132">x</span></span>    | <span data-ttu-id="ea0d9-133">x</span><span class="sxs-lookup"><span data-stu-id="ea0d9-133">x</span></span>     | <span data-ttu-id="ea0d9-134">x</span><span class="sxs-lookup"><span data-stu-id="ea0d9-134">x</span></span>    | <span data-ttu-id="ea0d9-135">x</span><span class="sxs-lookup"><span data-stu-id="ea0d9-135">x</span></span>     |



 

<span data-ttu-id="ea0d9-136">Diese Anweisung führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="ea0d9-136">This instruction does the following:</span></span>


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a><span data-ttu-id="ea0d9-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ea0d9-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea0d9-138">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="ea0d9-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




