---
title: RCP-vs
description: Berechnet die gegenseitige des Quell Skalars. | RCP-vs
ms.assetid: be638a42-b693-461d-ab0a-3a6c0fa1acfc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 145a998cbca9dc3721d9c7d6ba251d539286a3f1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982011"
---
# <a name="rcp---vs"></a><span data-ttu-id="bcec0-104">RCP-vs</span><span class="sxs-lookup"><span data-stu-id="bcec0-104">rcp - vs</span></span>

<span data-ttu-id="bcec0-105">Berechnet die gegenseitige des Quell Skalars.</span><span class="sxs-lookup"><span data-stu-id="bcec0-105">Computes the reciprocal of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcec0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bcec0-106">Syntax</span></span>



| <span data-ttu-id="bcec0-107">RCP DST, src</span><span class="sxs-lookup"><span data-stu-id="bcec0-107">rcp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="bcec0-108">where</span><span class="sxs-lookup"><span data-stu-id="bcec0-108">where</span></span>

-   <span data-ttu-id="bcec0-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="bcec0-109">dst is the destination register.</span></span>
-   <span data-ttu-id="bcec0-110">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="bcec0-110">src is a source register.</span></span> <span data-ttu-id="bcec0-111">Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bcec0-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcec0-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bcec0-112">Remarks</span></span>



| <span data-ttu-id="bcec0-113">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="bcec0-113">Vertex shader versions</span></span> | <span data-ttu-id="bcec0-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="bcec0-114">1\_1</span></span> | <span data-ttu-id="bcec0-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bcec0-115">2\_0</span></span> | <span data-ttu-id="bcec0-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bcec0-116">2\_x</span></span> | <span data-ttu-id="bcec0-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bcec0-117">2\_sw</span></span> | <span data-ttu-id="bcec0-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bcec0-118">3\_0</span></span> | <span data-ttu-id="bcec0-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bcec0-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="bcec0-120">rcp</span><span class="sxs-lookup"><span data-stu-id="bcec0-120">rcp</span></span>                    | <span data-ttu-id="bcec0-121">x</span><span class="sxs-lookup"><span data-stu-id="bcec0-121">x</span></span>    | <span data-ttu-id="bcec0-122">x</span><span class="sxs-lookup"><span data-stu-id="bcec0-122">x</span></span>    | <span data-ttu-id="bcec0-123">x</span><span class="sxs-lookup"><span data-stu-id="bcec0-123">x</span></span>    | <span data-ttu-id="bcec0-124">x</span><span class="sxs-lookup"><span data-stu-id="bcec0-124">x</span></span>     | <span data-ttu-id="bcec0-125">x</span><span class="sxs-lookup"><span data-stu-id="bcec0-125">x</span></span>    | <span data-ttu-id="bcec0-126">x</span><span class="sxs-lookup"><span data-stu-id="bcec0-126">x</span></span>     |



 

<span data-ttu-id="bcec0-127">Das folgende Code Fragment zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="bcec0-127">The following code fragment shows the operations performed.</span></span>


```
float f = src0;
if(f == 0.0f)
{
    f = FLT_MAX;
}
else 
{
    if(f != 1.0)
    {
        f = 1/f;
    }
}

dest = f;
```



<span data-ttu-id="bcec0-128">Die Ausgabe muss genau 1,0 sein, wenn die Eingabe genau 1,0 ist.</span><span class="sxs-lookup"><span data-stu-id="bcec0-128">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="bcec0-129">Eine Quelle von 0,0 ergibt unendlich.</span><span class="sxs-lookup"><span data-stu-id="bcec0-129">A source of 0.0 yields infinity.</span></span>

<span data-ttu-id="bcec0-130">Die Genauigkeit muss mindestens 1.0/(2 ² ²) absolute Fehler im Bereich (1,0, 2,0) betragen, da allgemeine Implementierungen die Mantisse und den Exponenten voneinander trennen.</span><span class="sxs-lookup"><span data-stu-id="bcec0-130">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 2.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="bcec0-131">Wenn die Quelle keine Indizes aufweist, wird die x-Komponente verwendet.</span><span class="sxs-lookup"><span data-stu-id="bcec0-131">If the source has no subscripts, the x-component is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bcec0-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bcec0-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcec0-133">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="bcec0-133">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




