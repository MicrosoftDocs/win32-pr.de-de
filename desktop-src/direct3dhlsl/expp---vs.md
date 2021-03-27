---
title: EXPP-vs
description: Stellt eine exponentielle partielle Genauigkeit von 2X bereit.
ms.assetid: ac080ac9-5dfd-49e4-92ea-50bb26844ff6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0d57e2723c90eee8df728aa540baeab86932e773
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719404"
---
# <a name="expp---vs"></a><span data-ttu-id="5be77-103">EXPP-vs</span><span class="sxs-lookup"><span data-stu-id="5be77-103">expp - vs</span></span>

<span data-ttu-id="5be77-104">Stellt eine exponentielle partielle Genauigkeit 2<sup>x</sup>bereit.</span><span class="sxs-lookup"><span data-stu-id="5be77-104">Provides partial precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="5be77-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5be77-105">Syntax</span></span>



| <span data-ttu-id="5be77-106">EXPP DST, src. Stuben</span><span class="sxs-lookup"><span data-stu-id="5be77-106">expp dst, src.{x\</span></span>|<span data-ttu-id="5be77-107">Teenie</span><span class="sxs-lookup"><span data-stu-id="5be77-107">y\</span></span>|<span data-ttu-id="5be77-108">z</span><span class="sxs-lookup"><span data-stu-id="5be77-108">z\</span></span>|<span data-ttu-id="5be77-109">Löw</span><span class="sxs-lookup"><span data-stu-id="5be77-109">w}</span></span> |
|----------------------------|



 

<span data-ttu-id="5be77-110">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="5be77-110">Where:</span></span>

-   <span data-ttu-id="5be77-111">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="5be77-111">dst is the destination register.</span></span>
-   <span data-ttu-id="5be77-112">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="5be77-112">src is a source register.</span></span> <span data-ttu-id="5be77-113">Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5be77-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="5be77-114">{x \| y \| z \| w} ist das erforderliche Replizieren von replizieren für das Quell Register.</span><span class="sxs-lookup"><span data-stu-id="5be77-114">{x\|y\|z\|w} is the required replicate swizzle on source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5be77-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5be77-115">Remarks</span></span>



| <span data-ttu-id="5be77-116">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="5be77-116">Vertex shader versions</span></span> | <span data-ttu-id="5be77-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="5be77-117">1\_1</span></span> | <span data-ttu-id="5be77-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5be77-118">2\_0</span></span> | <span data-ttu-id="5be77-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5be77-119">2\_x</span></span> | <span data-ttu-id="5be77-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5be77-120">2\_sw</span></span> | <span data-ttu-id="5be77-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5be77-121">3\_0</span></span> | <span data-ttu-id="5be77-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5be77-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5be77-123">EXPP</span><span class="sxs-lookup"><span data-stu-id="5be77-123">expp</span></span>                   | <span data-ttu-id="5be77-124">x</span><span class="sxs-lookup"><span data-stu-id="5be77-124">x</span></span>    | <span data-ttu-id="5be77-125">x</span><span class="sxs-lookup"><span data-stu-id="5be77-125">x</span></span>    | <span data-ttu-id="5be77-126">x</span><span class="sxs-lookup"><span data-stu-id="5be77-126">x</span></span>    | <span data-ttu-id="5be77-127">x</span><span class="sxs-lookup"><span data-stu-id="5be77-127">x</span></span>     | <span data-ttu-id="5be77-128">x</span><span class="sxs-lookup"><span data-stu-id="5be77-128">x</span></span>    | <span data-ttu-id="5be77-129">x</span><span class="sxs-lookup"><span data-stu-id="5be77-129">x</span></span>     |



 

### <a name="vs_1_1"></a><span data-ttu-id="5be77-130">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="5be77-130">vs\_1\_1</span></span>

<span data-ttu-id="5be77-131">Die [Exp-vs-](exp---vs.md) Anweisung ist abhängig von den Scheitelpunkt-Shader-Versionen unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="5be77-131">The [exp - vs](exp---vs.md) instruction operates differently depending on vertex shader versions.</span></span>

<span data-ttu-id="5be77-132">In vs \_ 1 \_ 1 ergibt die EXPP-Anweisung die folgenden Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="5be77-132">In vs\_1\_1, the expp instruction gives the following results:</span></span>


```
v = the scalar value from the source register with a replicate swizzle

dest.x = pow(2, floor(v))
dest.y = v - floor(v)
dest.z = pow(2, v) (partial-precision)
dest.w = 1
```



<span data-ttu-id="5be77-133">In vs \_ 2 \_ 0 und aufwärts führt die EXPP-Anweisung die folgenden Ergebnisse aus:</span><span class="sxs-lookup"><span data-stu-id="5be77-133">In vs\_2\_0 and up, the expp instruction gives the following results:</span></span>


```
v = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow(2, v) (partial-precision)
```



### <a name="vs_2_0"></a><span data-ttu-id="5be77-134">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5be77-134">vs\_2\_0</span></span>

<span data-ttu-id="5be77-135">In vs \_ 2 \_ 0 und oben funktioniert die-Anweisung wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5be77-135">In vs\_2\_0 and up, the instruction works like this:</span></span>


```
float V = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow( 2, V ) (partial-precision)
```



<span data-ttu-id="5be77-136">Die-Anweisung bietet mindestens 10 Bits an Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="5be77-136">The instruction provides at least 10 bits of precision.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5be77-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5be77-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5be77-138">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="5be77-138">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




