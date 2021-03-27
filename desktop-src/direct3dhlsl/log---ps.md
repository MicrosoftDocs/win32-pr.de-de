---
title: Log-PS
description: Protokoll der vollständigen Genauigkeit (x). | Log-PS
ms.assetid: e540a082-5916-4111-b908-bb229c9e7dc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8face264d5221cf4b39f99260bec476ee5742f0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982017"
---
# <a name="log---ps"></a><span data-ttu-id="694a9-104">Log-PS</span><span class="sxs-lookup"><span data-stu-id="694a9-104">log - ps</span></span>

<span data-ttu-id="694a9-105">Protokoll der vollständigen Genauigkeit (x).</span><span class="sxs-lookup"><span data-stu-id="694a9-105">Full precision log₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="694a9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="694a9-106">Syntax</span></span>



| <span data-ttu-id="694a9-107">Log DST, src</span><span class="sxs-lookup"><span data-stu-id="694a9-107">log dst, src</span></span> |
|--------------|



 

<span data-ttu-id="694a9-108">where</span><span class="sxs-lookup"><span data-stu-id="694a9-108">where</span></span>

-   <span data-ttu-id="694a9-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="694a9-109">dst is the destination register.</span></span>
-   <span data-ttu-id="694a9-110">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="694a9-110">src is a source register.</span></span> <span data-ttu-id="694a9-111">Das Quell Register erfordert die explizite Verwendung von "replizieren". Das heißt, es muss genau eine der x-, y-,. z-, w. w-, d. h. die. r-,. g-,. b-,. a-Entsprechungen) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="694a9-111">Source register requires explicit use of replicate swizzle; that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="694a9-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="694a9-112">Remarks</span></span>



| <span data-ttu-id="694a9-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="694a9-113">Pixel shader versions</span></span> | <span data-ttu-id="694a9-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="694a9-114">1\_1</span></span> | <span data-ttu-id="694a9-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="694a9-115">1\_2</span></span> | <span data-ttu-id="694a9-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="694a9-116">1\_3</span></span> | <span data-ttu-id="694a9-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="694a9-117">1\_4</span></span> | <span data-ttu-id="694a9-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="694a9-118">2\_0</span></span> | <span data-ttu-id="694a9-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="694a9-119">2\_x</span></span> | <span data-ttu-id="694a9-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="694a9-120">2\_sw</span></span> | <span data-ttu-id="694a9-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="694a9-121">3\_0</span></span> | <span data-ttu-id="694a9-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="694a9-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="694a9-123">log</span><span class="sxs-lookup"><span data-stu-id="694a9-123">log</span></span>                   |      |      |      |      | <span data-ttu-id="694a9-124">x</span><span class="sxs-lookup"><span data-stu-id="694a9-124">x</span></span>    | <span data-ttu-id="694a9-125">x</span><span class="sxs-lookup"><span data-stu-id="694a9-125">x</span></span>    | <span data-ttu-id="694a9-126">x</span><span class="sxs-lookup"><span data-stu-id="694a9-126">x</span></span>     | <span data-ttu-id="694a9-127">x</span><span class="sxs-lookup"><span data-stu-id="694a9-127">x</span></span>    | <span data-ttu-id="694a9-128">x</span><span class="sxs-lookup"><span data-stu-id="694a9-128">x</span></span>     |



 

<span data-ttu-id="694a9-129">Der folgende Code Ausschnitt zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="694a9-129">The following code snippet shows the operations performed.</span></span>


```
float v = abs(src);
if (v != 0)
{
    dest.x = dest.y = dest.z = dest.w = 
        (float)(log(v)/log(2));  
}
else
{
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;
}
```



<span data-ttu-id="694a9-130">Diese Anweisung akzeptiert eine skalare Quelle, deren Signier Bit ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="694a9-130">This instruction accepts a scalar source whose sign bit is ignored.</span></span> <span data-ttu-id="694a9-131">Das Ergebnis wird in alle vier Kanäle repliziert.</span><span class="sxs-lookup"><span data-stu-id="694a9-131">The result is replicated to all four channels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="694a9-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="694a9-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="694a9-133">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="694a9-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




