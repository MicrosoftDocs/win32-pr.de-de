---
title: Exp-vs
description: Bietet eine exponentielle vollständige Genauigkeit (2X). | Exp-vs
ms.assetid: 3644046b-3257-4257-9880-146ca50f6b0b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5b49b69e1270075aef4368dedca5791c2784657
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995709"
---
# <a name="exp---vs"></a><span data-ttu-id="5bfb9-104">Exp-vs</span><span class="sxs-lookup"><span data-stu-id="5bfb9-104">exp - vs</span></span>

<span data-ttu-id="5bfb9-105">Bietet eine exponentielle vollständige Genauigkeit 2<sup>x</sup>.</span><span class="sxs-lookup"><span data-stu-id="5bfb9-105">Provides full precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bfb9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bfb9-106">Syntax</span></span>



| <span data-ttu-id="5bfb9-107">Exp DST, src</span><span class="sxs-lookup"><span data-stu-id="5bfb9-107">exp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="5bfb9-108">where</span><span class="sxs-lookup"><span data-stu-id="5bfb9-108">where</span></span>

-   <span data-ttu-id="5bfb9-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="5bfb9-109">dst is the destination register.</span></span>
-   <span data-ttu-id="5bfb9-110">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="5bfb9-110">src is a source register.</span></span> <span data-ttu-id="5bfb9-111">Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5bfb9-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span> <span data-ttu-id="5bfb9-112">Weitere Informationen finden Sie unter [Quellen Register: schwenken](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="5bfb9-112">See [Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5bfb9-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bfb9-113">Remarks</span></span>



| <span data-ttu-id="5bfb9-114">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="5bfb9-114">Vertex shader versions</span></span> | <span data-ttu-id="5bfb9-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="5bfb9-115">1\_1</span></span> | <span data-ttu-id="5bfb9-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5bfb9-116">2\_0</span></span> | <span data-ttu-id="5bfb9-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5bfb9-117">2\_x</span></span> | <span data-ttu-id="5bfb9-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5bfb9-118">2\_sw</span></span> | <span data-ttu-id="5bfb9-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5bfb9-119">3\_0</span></span> | <span data-ttu-id="5bfb9-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5bfb9-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5bfb9-121">exp</span><span class="sxs-lookup"><span data-stu-id="5bfb9-121">exp</span></span>                    | <span data-ttu-id="5bfb9-122">x</span><span class="sxs-lookup"><span data-stu-id="5bfb9-122">x</span></span>    | <span data-ttu-id="5bfb9-123">x</span><span class="sxs-lookup"><span data-stu-id="5bfb9-123">x</span></span>    | <span data-ttu-id="5bfb9-124">x</span><span class="sxs-lookup"><span data-stu-id="5bfb9-124">x</span></span>    | <span data-ttu-id="5bfb9-125">x</span><span class="sxs-lookup"><span data-stu-id="5bfb9-125">x</span></span>     | <span data-ttu-id="5bfb9-126">x</span><span class="sxs-lookup"><span data-stu-id="5bfb9-126">x</span></span>    | <span data-ttu-id="5bfb9-127">x</span><span class="sxs-lookup"><span data-stu-id="5bfb9-127">x</span></span>     |



 

<span data-ttu-id="5bfb9-128">Diese Anweisung bietet mindestens 21 Bits an Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="5bfb9-128">This instruction provides at least 21 bits of precision.</span></span>

<span data-ttu-id="5bfb9-129">Das folgende Code Fragment zeigt die Vorgänge, die ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="5bfb9-129">The following code fragment shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a><span data-ttu-id="5bfb9-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5bfb9-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bfb9-131">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="5bfb9-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




