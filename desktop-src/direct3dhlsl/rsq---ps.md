---
title: RSQ-PS
description: Berechnet die gegenseitige Quadratwurzel (nur positiv) des Quell Skalars. | RSQ-PS
ms.assetid: deb1bd12-6347-4b1e-b21b-f3ef48da4c13
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13777810c67ba38b2c8f47f0c0db0cf9b70771ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981552"
---
# <a name="rsq---ps"></a><span data-ttu-id="7a1c0-104">RSQ-PS</span><span class="sxs-lookup"><span data-stu-id="7a1c0-104">rsq - ps</span></span>

<span data-ttu-id="7a1c0-105">Berechnet die gegenseitige Quadratwurzel (nur positiv) des Quell Skalars.</span><span class="sxs-lookup"><span data-stu-id="7a1c0-105">Computes the reciprocal square root (positive only) of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a1c0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a1c0-106">Syntax</span></span>



| <span data-ttu-id="7a1c0-107">RSQ DST, src</span><span class="sxs-lookup"><span data-stu-id="7a1c0-107">rsq dst, src</span></span> |
|--------------|



 

<span data-ttu-id="7a1c0-108">where</span><span class="sxs-lookup"><span data-stu-id="7a1c0-108">where</span></span>

-   <span data-ttu-id="7a1c0-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="7a1c0-109">dst is the destination register.</span></span>
-   <span data-ttu-id="7a1c0-110">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="7a1c0-110">src is a source register.</span></span> <span data-ttu-id="7a1c0-111">Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7a1c0-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a1c0-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a1c0-112">Remarks</span></span>



| <span data-ttu-id="7a1c0-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="7a1c0-113">Pixel shader versions</span></span> | <span data-ttu-id="7a1c0-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="7a1c0-114">1\_1</span></span> | <span data-ttu-id="7a1c0-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="7a1c0-115">1\_2</span></span> | <span data-ttu-id="7a1c0-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7a1c0-116">1\_3</span></span> | <span data-ttu-id="7a1c0-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="7a1c0-117">1\_4</span></span> | <span data-ttu-id="7a1c0-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7a1c0-118">2\_0</span></span> | <span data-ttu-id="7a1c0-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7a1c0-119">2\_x</span></span> | <span data-ttu-id="7a1c0-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7a1c0-120">2\_sw</span></span> | <span data-ttu-id="7a1c0-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7a1c0-121">3\_0</span></span> | <span data-ttu-id="7a1c0-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7a1c0-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7a1c0-123">RSQ</span><span class="sxs-lookup"><span data-stu-id="7a1c0-123">rsq</span></span>                   |      |      |      |      | <span data-ttu-id="7a1c0-124">x</span><span class="sxs-lookup"><span data-stu-id="7a1c0-124">x</span></span>    | <span data-ttu-id="7a1c0-125">x</span><span class="sxs-lookup"><span data-stu-id="7a1c0-125">x</span></span>    | <span data-ttu-id="7a1c0-126">x</span><span class="sxs-lookup"><span data-stu-id="7a1c0-126">x</span></span>     | <span data-ttu-id="7a1c0-127">x</span><span class="sxs-lookup"><span data-stu-id="7a1c0-127">x</span></span>    | <span data-ttu-id="7a1c0-128">x</span><span class="sxs-lookup"><span data-stu-id="7a1c0-128">x</span></span>     |



 

<span data-ttu-id="7a1c0-129">Der absolute Wert wird vor der Verarbeitung übernommen.</span><span class="sxs-lookup"><span data-stu-id="7a1c0-129">The absolute value is taken before processing.</span></span>

<span data-ttu-id="7a1c0-130">Die Genauigkeit muss mindestens 1.0/(2 ² ²) absolute Fehler im Bereich (1,0, 4,0) betragen, da allgemeine Implementierungen die Mantisse und den Exponenten voneinander trennen.</span><span class="sxs-lookup"><span data-stu-id="7a1c0-130">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 4.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="7a1c0-131">Die Ausgabe muss genau 1,0 sein, wenn die Eingabe genau 1,0 ist.</span><span class="sxs-lookup"><span data-stu-id="7a1c0-131">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="7a1c0-132">Eine Quelle von 0,0 ergibt unendlich.</span><span class="sxs-lookup"><span data-stu-id="7a1c0-132">A source of 0.0 yields infinity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a1c0-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7a1c0-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a1c0-134">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="7a1c0-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




