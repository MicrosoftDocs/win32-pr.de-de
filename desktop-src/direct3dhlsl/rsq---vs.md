---
title: RSQ-vs
description: Berechnet die gegenseitige Quadratwurzel (nur positiv) des Quell Skalars. | RSQ-vs
ms.assetid: 1ac37dad-0cea-41af-8dae-f299896462b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f477d6f7d8a7ff94472c689bf5844183e2f016ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981800"
---
# <a name="rsq---vs"></a><span data-ttu-id="ac8b3-104">RSQ-vs</span><span class="sxs-lookup"><span data-stu-id="ac8b3-104">rsq - vs</span></span>

<span data-ttu-id="ac8b3-105">Berechnet die gegenseitige Quadratwurzel (nur positiv) des Quell Skalars.</span><span class="sxs-lookup"><span data-stu-id="ac8b3-105">Computes the reciprocal square root (positive only) of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac8b3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac8b3-106">Syntax</span></span>



| <span data-ttu-id="ac8b3-107">RSQ DST, src</span><span class="sxs-lookup"><span data-stu-id="ac8b3-107">rsq dst, src</span></span> |
|--------------|



 

<span data-ttu-id="ac8b3-108">where</span><span class="sxs-lookup"><span data-stu-id="ac8b3-108">where</span></span>

-   <span data-ttu-id="ac8b3-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="ac8b3-109">dst is the destination register.</span></span>
-   <span data-ttu-id="ac8b3-110">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="ac8b3-110">src is a source register.</span></span> <span data-ttu-id="ac8b3-111">Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ac8b3-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac8b3-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac8b3-112">Remarks</span></span>



| <span data-ttu-id="ac8b3-113">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="ac8b3-113">Vertex shader versions</span></span> | <span data-ttu-id="ac8b3-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="ac8b3-114">1\_1</span></span> | <span data-ttu-id="ac8b3-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ac8b3-115">2\_0</span></span> | <span data-ttu-id="ac8b3-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ac8b3-116">2\_x</span></span> | <span data-ttu-id="ac8b3-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ac8b3-117">2\_sw</span></span> | <span data-ttu-id="ac8b3-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ac8b3-118">3\_0</span></span> | <span data-ttu-id="ac8b3-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ac8b3-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="ac8b3-120">RSQ</span><span class="sxs-lookup"><span data-stu-id="ac8b3-120">rsq</span></span>                    | <span data-ttu-id="ac8b3-121">x</span><span class="sxs-lookup"><span data-stu-id="ac8b3-121">x</span></span>    | <span data-ttu-id="ac8b3-122">x</span><span class="sxs-lookup"><span data-stu-id="ac8b3-122">x</span></span>    | <span data-ttu-id="ac8b3-123">x</span><span class="sxs-lookup"><span data-stu-id="ac8b3-123">x</span></span>    | <span data-ttu-id="ac8b3-124">x</span><span class="sxs-lookup"><span data-stu-id="ac8b3-124">x</span></span>     | <span data-ttu-id="ac8b3-125">x</span><span class="sxs-lookup"><span data-stu-id="ac8b3-125">x</span></span>    | <span data-ttu-id="ac8b3-126">x</span><span class="sxs-lookup"><span data-stu-id="ac8b3-126">x</span></span>     |



 

<span data-ttu-id="ac8b3-127">Das folgende Code Fragment zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="ac8b3-127">The following code fragment shows the operations performed.</span></span>


```
float f = abs(src0);
if (f == 0)
    f = FLT_MAX
else
{
    if (f != 1.0)
        f = 1.0/(float)sqrt(f);
}

dest.z = dest.y = dest.z = dest.w = f;
```



<span data-ttu-id="ac8b3-128">Der absolute Wert wird vor der Verarbeitung übernommen.</span><span class="sxs-lookup"><span data-stu-id="ac8b3-128">The absolute value is taken before processing.</span></span>

<span data-ttu-id="ac8b3-129">Die Genauigkeit muss mindestens 1.0/(2 ² ²) absolute Fehler im Bereich (1,0, 4,0) betragen, da allgemeine Implementierungen die Mantisse und den Exponenten voneinander trennen.</span><span class="sxs-lookup"><span data-stu-id="ac8b3-129">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 4.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="ac8b3-130">Wenn die Quelle keine Indizes aufweist, wird die x-Komponente verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac8b3-130">If source has no subscripts, the x-component is used.</span></span> <span data-ttu-id="ac8b3-131">Die Ausgabe muss genau 1,0 sein, wenn die Eingabe genau 1,0 ist.</span><span class="sxs-lookup"><span data-stu-id="ac8b3-131">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="ac8b3-132">Eine Quelle von 0,0 ergibt unendlich.</span><span class="sxs-lookup"><span data-stu-id="ac8b3-132">A source of 0.0 yields infinity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac8b3-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ac8b3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac8b3-134">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="ac8b3-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




