---
title: RCP-PS
description: Berechnet die gegenseitige des Quell Skalars. | RCP-PS
ms.assetid: d8dfc2b3-4404-47ec-aeaf-1adb7e7a342e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2df8ad2d673d96dced84630b1a641c7e4f27ceb2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981729"
---
# <a name="rcp---ps"></a><span data-ttu-id="a9bbc-104">RCP-PS</span><span class="sxs-lookup"><span data-stu-id="a9bbc-104">rcp - ps</span></span>

<span data-ttu-id="a9bbc-105">Berechnet die gegenseitige des Quell Skalars.</span><span class="sxs-lookup"><span data-stu-id="a9bbc-105">Computes the reciprocal of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9bbc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9bbc-106">Syntax</span></span>



| <span data-ttu-id="a9bbc-107">RCP DST, src</span><span class="sxs-lookup"><span data-stu-id="a9bbc-107">rcp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="a9bbc-108">where</span><span class="sxs-lookup"><span data-stu-id="a9bbc-108">where</span></span>

-   <span data-ttu-id="a9bbc-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="a9bbc-109">dst is the destination register.</span></span>
-   <span data-ttu-id="a9bbc-110">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="a9bbc-110">src is a source register.</span></span> <span data-ttu-id="a9bbc-111">Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a9bbc-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9bbc-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9bbc-112">Remarks</span></span>



| <span data-ttu-id="a9bbc-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="a9bbc-113">Pixel shader versions</span></span> | <span data-ttu-id="a9bbc-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="a9bbc-114">1\_1</span></span> | <span data-ttu-id="a9bbc-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="a9bbc-115">1\_2</span></span> | <span data-ttu-id="a9bbc-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a9bbc-116">1\_3</span></span> | <span data-ttu-id="a9bbc-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="a9bbc-117">1\_4</span></span> | <span data-ttu-id="a9bbc-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a9bbc-118">2\_0</span></span> | <span data-ttu-id="a9bbc-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a9bbc-119">2\_x</span></span> | <span data-ttu-id="a9bbc-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a9bbc-120">2\_sw</span></span> | <span data-ttu-id="a9bbc-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a9bbc-121">3\_0</span></span> | <span data-ttu-id="a9bbc-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a9bbc-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a9bbc-123">rcp</span><span class="sxs-lookup"><span data-stu-id="a9bbc-123">rcp</span></span>                   |      |      |      |      | <span data-ttu-id="a9bbc-124">x</span><span class="sxs-lookup"><span data-stu-id="a9bbc-124">x</span></span>    | <span data-ttu-id="a9bbc-125">x</span><span class="sxs-lookup"><span data-stu-id="a9bbc-125">x</span></span>    | <span data-ttu-id="a9bbc-126">x</span><span class="sxs-lookup"><span data-stu-id="a9bbc-126">x</span></span>     | <span data-ttu-id="a9bbc-127">x</span><span class="sxs-lookup"><span data-stu-id="a9bbc-127">x</span></span>    | <span data-ttu-id="a9bbc-128">x</span><span class="sxs-lookup"><span data-stu-id="a9bbc-128">x</span></span>     |



 

<span data-ttu-id="a9bbc-129">Die Ausgabe muss genau 1,0 sein, wenn die Eingabe genau 1,0 ist.</span><span class="sxs-lookup"><span data-stu-id="a9bbc-129">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="a9bbc-130">Eine Quelle von 0,0 ergibt unendlich.</span><span class="sxs-lookup"><span data-stu-id="a9bbc-130">A source of 0.0 yields infinity.</span></span>

<span data-ttu-id="a9bbc-131">Das skalare Ergebnis wird in allen Kanälen in der Ziel Schreib Maske repliziert.</span><span class="sxs-lookup"><span data-stu-id="a9bbc-131">The scalar result is replicated to all channels in the destination write mask.</span></span>

<span data-ttu-id="a9bbc-132">Die Genauigkeit muss mindestens 1.0/(2 ² ²) absolute Fehler im Bereich (1,0, 2,0) betragen, da allgemeine Implementierungen die Mantisse und den Exponenten voneinander trennen.</span><span class="sxs-lookup"><span data-stu-id="a9bbc-132">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 2.0) because common implementations will separate mantissa and exponent.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9bbc-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a9bbc-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9bbc-134">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="a9bbc-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




