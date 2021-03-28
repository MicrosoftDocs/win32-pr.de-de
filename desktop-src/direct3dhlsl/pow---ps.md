---
title: Pow-PS
description: Abs (src0) mit vollständiger Genauigkeit Quelle1. | Pow-PS
ms.assetid: 39037c51-a524-459c-8422-bd7831e2aa3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 84be39ca8f2633482165d76eabfe0f5d0bb22161
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981272"
---
# <a name="pow---ps"></a><span data-ttu-id="e5908-104">Pow-PS</span><span class="sxs-lookup"><span data-stu-id="e5908-104">pow - ps</span></span>

<span data-ttu-id="e5908-105">Abs (src0) mit vollständiger Genauigkeit<sup>Quelle1</sup>.</span><span class="sxs-lookup"><span data-stu-id="e5908-105">Full precision abs(src0)<sup>src1</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5908-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5908-106">Syntax</span></span>



| <span data-ttu-id="e5908-107">Pow DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="e5908-107">pow dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="e5908-108">where</span><span class="sxs-lookup"><span data-stu-id="e5908-108">where</span></span>

-   <span data-ttu-id="e5908-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="e5908-109">dst is the destination register.</span></span>
-   <span data-ttu-id="e5908-110">src0 ist ein Eingabe Quellen Register.</span><span class="sxs-lookup"><span data-stu-id="e5908-110">src0 is an input source register.</span></span> <span data-ttu-id="e5908-111">Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e5908-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="e5908-112">Quelle1 ist ein Eingabe Quellen Register.</span><span class="sxs-lookup"><span data-stu-id="e5908-112">src1 is an input source register.</span></span> <span data-ttu-id="e5908-113">Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e5908-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5908-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5908-114">Remarks</span></span>



| <span data-ttu-id="e5908-115">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="e5908-115">Pixel shader versions</span></span> | <span data-ttu-id="e5908-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="e5908-116">1\_1</span></span> | <span data-ttu-id="e5908-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="e5908-117">1\_2</span></span> | <span data-ttu-id="e5908-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e5908-118">1\_3</span></span> | <span data-ttu-id="e5908-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="e5908-119">1\_4</span></span> | <span data-ttu-id="e5908-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e5908-120">2\_0</span></span> | <span data-ttu-id="e5908-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e5908-121">2\_x</span></span> | <span data-ttu-id="e5908-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e5908-122">2\_sw</span></span> | <span data-ttu-id="e5908-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e5908-123">3\_0</span></span> | <span data-ttu-id="e5908-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e5908-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e5908-125">pow</span><span class="sxs-lookup"><span data-stu-id="e5908-125">pow</span></span>                   |      |      |      |      | <span data-ttu-id="e5908-126">x</span><span class="sxs-lookup"><span data-stu-id="e5908-126">x</span></span>    | <span data-ttu-id="e5908-127">x</span><span class="sxs-lookup"><span data-stu-id="e5908-127">x</span></span>    | <span data-ttu-id="e5908-128">x</span><span class="sxs-lookup"><span data-stu-id="e5908-128">x</span></span>     | <span data-ttu-id="e5908-129">x</span><span class="sxs-lookup"><span data-stu-id="e5908-129">x</span></span>    | <span data-ttu-id="e5908-130">x</span><span class="sxs-lookup"><span data-stu-id="e5908-130">x</span></span>     |



 

<span data-ttu-id="e5908-131">Diese Anweisung funktioniert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e5908-131">This instruction works as follows:</span></span>

<span data-ttu-id="e5908-132">dest. x = dest. y = dest. z = dest. w = \[ Abs (src0) \] <sup>Quelle1</sup>;</span><span class="sxs-lookup"><span data-stu-id="e5908-132">dest.x = dest.y = dest.z = dest.w = \[abs(src0)\]<sup>src1</sup>;</span></span>

<span data-ttu-id="e5908-133">Dabei handelt es sich um eine skalare Anweisung. Daher sollten die Quell Register über repliziert werden, um anzugeben, welche Kanäle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5908-133">This is a scalar instruction, therefore the source registers should have replicate swizzles to indicate which channels are used.</span></span>

<span data-ttu-id="e5908-134">Die Eingabe Potenz (Quelle1) muss ein Skalar sein.</span><span class="sxs-lookup"><span data-stu-id="e5908-134">The input power (src1) must be a scalar.</span></span>

<span data-ttu-id="e5908-135">Das skalare Ergebnis wird in alle vier Ausgabekanäle repliziert.</span><span class="sxs-lookup"><span data-stu-id="e5908-135">The scalar result is replicated to all four output channels.</span></span>

<span data-ttu-id="e5908-136">Diese Anweisung kann als Exp (Quelle1 \* Log (src0)) erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="e5908-136">This instruction could be expanded as exp(src1 \* log(src0)).</span></span>

<span data-ttu-id="e5908-137">Das DST-Register muss ein temporäres Register sein und sollte nicht dasselbe Register wie Quelle1 sein.</span><span class="sxs-lookup"><span data-stu-id="e5908-137">The dst register should be a temporary register, and should not be the same register as src1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5908-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e5908-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5908-139">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="e5908-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




