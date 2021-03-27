---
title: Log-vs
description: Protokoll der vollständigen Genauigkeit (x). | Log-vs
ms.assetid: 53c91825-ec54-4b04-bf08-52d4b1c5122d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9e0564ab5b38943017e61bde171d0db3060ca0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219276"
---
# <a name="log---vs"></a><span data-ttu-id="d7f6c-104">Log-vs</span><span class="sxs-lookup"><span data-stu-id="d7f6c-104">log - vs</span></span>

<span data-ttu-id="d7f6c-105">Protokoll der vollständigen Genauigkeit (x).</span><span class="sxs-lookup"><span data-stu-id="d7f6c-105">Full precision log₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f6c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7f6c-106">Syntax</span></span>



| <span data-ttu-id="d7f6c-107">Log DST, src</span><span class="sxs-lookup"><span data-stu-id="d7f6c-107">log dst, src</span></span> |
|--------------|



 

<span data-ttu-id="d7f6c-108">where</span><span class="sxs-lookup"><span data-stu-id="d7f6c-108">where</span></span>

-   <span data-ttu-id="d7f6c-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="d7f6c-109">dst is the destination register.</span></span>
-   <span data-ttu-id="d7f6c-110">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="d7f6c-110">src is a source register.</span></span> <span data-ttu-id="d7f6c-111">Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d7f6c-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7f6c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7f6c-112">Remarks</span></span>



| <span data-ttu-id="d7f6c-113">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="d7f6c-113">Vertex shader versions</span></span> | <span data-ttu-id="d7f6c-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="d7f6c-114">1\_1</span></span> | <span data-ttu-id="d7f6c-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d7f6c-115">2\_0</span></span> | <span data-ttu-id="d7f6c-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d7f6c-116">2\_x</span></span> | <span data-ttu-id="d7f6c-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d7f6c-117">2\_sw</span></span> | <span data-ttu-id="d7f6c-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d7f6c-118">3\_0</span></span> | <span data-ttu-id="d7f6c-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d7f6c-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="d7f6c-120">log</span><span class="sxs-lookup"><span data-stu-id="d7f6c-120">log</span></span>                    | <span data-ttu-id="d7f6c-121">x</span><span class="sxs-lookup"><span data-stu-id="d7f6c-121">x</span></span>    | <span data-ttu-id="d7f6c-122">x</span><span class="sxs-lookup"><span data-stu-id="d7f6c-122">x</span></span>    | <span data-ttu-id="d7f6c-123">x</span><span class="sxs-lookup"><span data-stu-id="d7f6c-123">x</span></span>    | <span data-ttu-id="d7f6c-124">x</span><span class="sxs-lookup"><span data-stu-id="d7f6c-124">x</span></span>     | <span data-ttu-id="d7f6c-125">x</span><span class="sxs-lookup"><span data-stu-id="d7f6c-125">x</span></span>    | <span data-ttu-id="d7f6c-126">x</span><span class="sxs-lookup"><span data-stu-id="d7f6c-126">x</span></span>     |



 

<span data-ttu-id="d7f6c-127">Das folgende Code Fragment zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="d7f6c-127">The following code fragment shows the operations performed.</span></span>


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



<span data-ttu-id="d7f6c-128">Diese Anweisung akzeptiert eine skalare Quelle, deren Signier Bit ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="d7f6c-128">This instruction accepts a scalar source whose sign bit is ignored.</span></span> <span data-ttu-id="d7f6c-129">Das Ergebnis wird in alle vier Kanäle repliziert.</span><span class="sxs-lookup"><span data-stu-id="d7f6c-129">The result is replicated to all four channels.</span></span>

<span data-ttu-id="d7f6c-130">Diese Anweisung stellt 21 Bits Genauigkeit bereit.</span><span class="sxs-lookup"><span data-stu-id="d7f6c-130">This instruction provides 21 bits of precision.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7f6c-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d7f6c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7f6c-132">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="d7f6c-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




