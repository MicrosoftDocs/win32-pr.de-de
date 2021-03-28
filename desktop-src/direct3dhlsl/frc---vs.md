---
title: FRC-vs
description: Gibt den Bruchteil der einzelnen Eingabe Komponenten zurück. | FRC-vs
ms.assetid: 6b6a4475-b665-4de0-9423-88ea8103e606
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6990d5489058d217888f34caf0305badc4cab46d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353409"
---
# <a name="frc---vs"></a><span data-ttu-id="f9fc0-104">FRC-vs</span><span class="sxs-lookup"><span data-stu-id="f9fc0-104">frc - vs</span></span>

<span data-ttu-id="f9fc0-105">Gibt den Bruchteil der einzelnen Eingabe Komponenten zurück.</span><span class="sxs-lookup"><span data-stu-id="f9fc0-105">Returns the fractional portion of each input component.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9fc0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9fc0-106">Syntax</span></span>



| <span data-ttu-id="f9fc0-107">FRC-DST, src</span><span class="sxs-lookup"><span data-stu-id="f9fc0-107">frc dst, src</span></span> |
|--------------|



 

<span data-ttu-id="f9fc0-108">where</span><span class="sxs-lookup"><span data-stu-id="f9fc0-108">where</span></span>

-   <span data-ttu-id="f9fc0-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="f9fc0-109">dst is the destination register.</span></span>
-   <span data-ttu-id="f9fc0-110">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="f9fc0-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9fc0-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9fc0-111">Remarks</span></span>



| <span data-ttu-id="f9fc0-112">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="f9fc0-112">Vertex shader versions</span></span> | <span data-ttu-id="f9fc0-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="f9fc0-113">1\_1</span></span> | <span data-ttu-id="f9fc0-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f9fc0-114">2\_0</span></span> | <span data-ttu-id="f9fc0-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f9fc0-115">2\_x</span></span> | <span data-ttu-id="f9fc0-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f9fc0-116">2\_sw</span></span> | <span data-ttu-id="f9fc0-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f9fc0-117">3\_0</span></span> | <span data-ttu-id="f9fc0-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f9fc0-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="f9fc0-119">FRC</span><span class="sxs-lookup"><span data-stu-id="f9fc0-119">frc</span></span>                    | <span data-ttu-id="f9fc0-120">x</span><span class="sxs-lookup"><span data-stu-id="f9fc0-120">x</span></span>    | <span data-ttu-id="f9fc0-121">x</span><span class="sxs-lookup"><span data-stu-id="f9fc0-121">x</span></span>    | <span data-ttu-id="f9fc0-122">x</span><span class="sxs-lookup"><span data-stu-id="f9fc0-122">x</span></span>    | <span data-ttu-id="f9fc0-123">x</span><span class="sxs-lookup"><span data-stu-id="f9fc0-123">x</span></span>     | <span data-ttu-id="f9fc0-124">x</span><span class="sxs-lookup"><span data-stu-id="f9fc0-124">x</span></span>    | <span data-ttu-id="f9fc0-125">x</span><span class="sxs-lookup"><span data-stu-id="f9fc0-125">x</span></span>     |



 

<span data-ttu-id="f9fc0-126">Das folgende Code Fragment zeigt konzeptionell, wie die Anweisung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="f9fc0-126">The following code fragment shows conceptually how the instruction operates.</span></span>


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



<span data-ttu-id="f9fc0-127">Die Floor-Funktion konvertiert das Argument, das an die größte Ganzzahl, die kleiner oder gleich dem Argument ist, an die größte Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="f9fc0-127">The floor function converts the argument passed in to the greatest integer that is less than (or equal to) the argument.</span></span> <span data-ttu-id="f9fc0-128">Diese wird in einen float-Wert konvertiert und dann den ursprünglichen Wert von Abbildung subtrahiert.</span><span class="sxs-lookup"><span data-stu-id="f9fc0-128">This is converted to a float and then subtracted fom the original value.</span></span> <span data-ttu-id="f9fc0-129">Der resultierende Bruch Wert liegt zwischen 0,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="f9fc0-129">The resulting fractional value ranges from 0.0 through 1.0.</span></span>

<span data-ttu-id="f9fc0-130">Bei Version 1 \_ 1 sind die zulässigen Schreib Masken. y und. XY (. x ist nicht zulässig).</span><span class="sxs-lookup"><span data-stu-id="f9fc0-130">For version 1\_1, the allowable write masks are .y and .xy (.x is not allowed).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9fc0-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9fc0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9fc0-132">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="f9fc0-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




