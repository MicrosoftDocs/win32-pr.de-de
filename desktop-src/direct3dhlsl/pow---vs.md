---
title: Pow-vs
description: Abs (src0) mit vollständiger Genauigkeit Quelle1. | Pow-vs
ms.assetid: 51da86c6-bafa-42e0-90a5-d1545e39e600
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3263fa19015bc32c94ae714891c3bbb2128c9463
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219174"
---
# <a name="pow---vs"></a><span data-ttu-id="4bb49-104">Pow-vs</span><span class="sxs-lookup"><span data-stu-id="4bb49-104">pow - vs</span></span>

<span data-ttu-id="4bb49-105">Abs (src0) mit vollständiger Genauigkeit<sup>Quelle1</sup>.</span><span class="sxs-lookup"><span data-stu-id="4bb49-105">Full precision abs(src0)<sup>src1</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bb49-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bb49-106">Syntax</span></span>



| <span data-ttu-id="4bb49-107">Pow DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="4bb49-107">pow dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="4bb49-108">where</span><span class="sxs-lookup"><span data-stu-id="4bb49-108">where</span></span>

-   <span data-ttu-id="4bb49-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="4bb49-109">dst is the destination register.</span></span>
-   <span data-ttu-id="4bb49-110">src0 ist ein Eingabe Quellen Register.</span><span class="sxs-lookup"><span data-stu-id="4bb49-110">src0 is an input source register.</span></span> <span data-ttu-id="4bb49-111">Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4bb49-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="4bb49-112">Quelle1 ist ein Eingabe Quellen Register.</span><span class="sxs-lookup"><span data-stu-id="4bb49-112">src1 is an input source register.</span></span> <span data-ttu-id="4bb49-113">Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4bb49-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bb49-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4bb49-114">Remarks</span></span>



| <span data-ttu-id="4bb49-115">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="4bb49-115">Vertex shader versions</span></span> | <span data-ttu-id="4bb49-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="4bb49-116">1\_1</span></span> | <span data-ttu-id="4bb49-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4bb49-117">2\_0</span></span> | <span data-ttu-id="4bb49-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4bb49-118">2\_x</span></span> | <span data-ttu-id="4bb49-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4bb49-119">2\_sw</span></span> | <span data-ttu-id="4bb49-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4bb49-120">3\_0</span></span> | <span data-ttu-id="4bb49-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4bb49-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="4bb49-122">pow</span><span class="sxs-lookup"><span data-stu-id="4bb49-122">pow</span></span>                    |      | <span data-ttu-id="4bb49-123">x</span><span class="sxs-lookup"><span data-stu-id="4bb49-123">x</span></span>    | <span data-ttu-id="4bb49-124">x</span><span class="sxs-lookup"><span data-stu-id="4bb49-124">x</span></span>    | <span data-ttu-id="4bb49-125">x</span><span class="sxs-lookup"><span data-stu-id="4bb49-125">x</span></span>     | <span data-ttu-id="4bb49-126">x</span><span class="sxs-lookup"><span data-stu-id="4bb49-126">x</span></span>    | <span data-ttu-id="4bb49-127">x</span><span class="sxs-lookup"><span data-stu-id="4bb49-127">x</span></span>     |



 

<span data-ttu-id="4bb49-128">Diese Anweisung funktioniert wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4bb49-128">This instruction works as shown here.</span></span>


```
dest = pow(abs(src0), src1);
```



<span data-ttu-id="4bb49-129">Dabei handelt es sich um eine skalare Anweisung. Daher sollten die Quell Register über repliziert werden, um anzugeben, welche Kanäle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4bb49-129">This is a scalar instruction, therefore the source registers should have replicate swizzles to indicate which channels are used.</span></span>

<span data-ttu-id="4bb49-130">Das skalare Ergebnis wird in alle vier Ausgabekanäle repliziert.</span><span class="sxs-lookup"><span data-stu-id="4bb49-130">The scalar result is replicated to all four output channels.</span></span>

<span data-ttu-id="4bb49-131">Diese Anweisung kann als Exp (Quelle1 \* Log (src0)) erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="4bb49-131">This instruction could be expanded as exp(src1 \* log(src0)).</span></span>

<span data-ttu-id="4bb49-132">Die Genauigkeit ist nicht kleiner als 15 Bits.</span><span class="sxs-lookup"><span data-stu-id="4bb49-132">Precision is not lower than 15 bits.</span></span>

<span data-ttu-id="4bb49-133">Das dest-Register muss ein temporäres Register sein und sollte nicht dasselbe Register wie Quelle1 sein.</span><span class="sxs-lookup"><span data-stu-id="4bb49-133">The dest register should be a temporary register, and should not be the same register as src1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bb49-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4bb49-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bb49-135">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="4bb49-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




