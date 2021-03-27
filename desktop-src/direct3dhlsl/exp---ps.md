---
title: Exp-PS
description: Bietet eine exponentielle vollständige Genauigkeit (2X). | Exp-PS
ms.assetid: 09e4446f-4149-4ec8-b3e3-2045b55bd591
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: acd7c50c1f0d6ff08ee5d66e50fdd3e56939f0d9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050756"
---
# <a name="exp---ps"></a><span data-ttu-id="b3b02-104">Exp-PS</span><span class="sxs-lookup"><span data-stu-id="b3b02-104">exp - ps</span></span>

<span data-ttu-id="b3b02-105">Bietet eine exponentielle vollständige Genauigkeit 2<sup>x</sup>.</span><span class="sxs-lookup"><span data-stu-id="b3b02-105">Provides full precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3b02-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3b02-106">Syntax</span></span>



| <span data-ttu-id="b3b02-107">Exp DST, src</span><span class="sxs-lookup"><span data-stu-id="b3b02-107">exp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="b3b02-108">where</span><span class="sxs-lookup"><span data-stu-id="b3b02-108">where</span></span>

-   <span data-ttu-id="b3b02-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="b3b02-109">dst is the destination register.</span></span>
-   <span data-ttu-id="b3b02-110">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="b3b02-110">src is a source register.</span></span> <span data-ttu-id="b3b02-111">Das Quell Register erfordert die explizite Verwendung von "replizieren". Das heißt, es muss genau eine der x-, y-,. z-, w. w-, d. h. die. r-,. g-,. b-,. a-Entsprechungen) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b3b02-111">Source register requires explicit use of replicate swizzle; that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span> <span data-ttu-id="b3b02-112">Weitere Informationen finden Sie unter [Quellen Register: schwenken](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="b3b02-112">See [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b3b02-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3b02-113">Remarks</span></span>



| <span data-ttu-id="b3b02-114">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="b3b02-114">Pixel shader versions</span></span> | <span data-ttu-id="b3b02-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="b3b02-115">1\_1</span></span> | <span data-ttu-id="b3b02-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="b3b02-116">1\_2</span></span> | <span data-ttu-id="b3b02-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b3b02-117">1\_3</span></span> | <span data-ttu-id="b3b02-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="b3b02-118">1\_4</span></span> | <span data-ttu-id="b3b02-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b3b02-119">2\_0</span></span> | <span data-ttu-id="b3b02-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b3b02-120">2\_x</span></span> | <span data-ttu-id="b3b02-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b3b02-121">2\_sw</span></span> | <span data-ttu-id="b3b02-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b3b02-122">3\_0</span></span> | <span data-ttu-id="b3b02-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b3b02-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b3b02-124">exp</span><span class="sxs-lookup"><span data-stu-id="b3b02-124">exp</span></span>                   |      |      |      |      | <span data-ttu-id="b3b02-125">x</span><span class="sxs-lookup"><span data-stu-id="b3b02-125">x</span></span>    | <span data-ttu-id="b3b02-126">x</span><span class="sxs-lookup"><span data-stu-id="b3b02-126">x</span></span>    | <span data-ttu-id="b3b02-127">x</span><span class="sxs-lookup"><span data-stu-id="b3b02-127">x</span></span>     | <span data-ttu-id="b3b02-128">x</span><span class="sxs-lookup"><span data-stu-id="b3b02-128">x</span></span>    | <span data-ttu-id="b3b02-129">x</span><span class="sxs-lookup"><span data-stu-id="b3b02-129">x</span></span>     |



 

<span data-ttu-id="b3b02-130">Der folgende Code Ausschnitt zeigt die Vorgänge, die ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="b3b02-130">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a><span data-ttu-id="b3b02-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b3b02-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3b02-132">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="b3b02-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




