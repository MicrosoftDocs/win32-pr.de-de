---
title: FRC-PS
description: Gibt den Bruchteil der einzelnen Eingabe Komponenten zurück. | FRC-PS
ms.assetid: 378bc516-c81e-4538-8d6f-987536b19467
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a16dd518333efa1dce878c1418547bc0527d1d64
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353418"
---
# <a name="frc---ps"></a><span data-ttu-id="30ecd-104">FRC-PS</span><span class="sxs-lookup"><span data-stu-id="30ecd-104">frc - ps</span></span>

<span data-ttu-id="30ecd-105">Gibt den Bruchteil der einzelnen Eingabe Komponenten zurück.</span><span class="sxs-lookup"><span data-stu-id="30ecd-105">Returns the fractional portion of each input component.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ecd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="30ecd-106">Syntax</span></span>



| <span data-ttu-id="30ecd-107">FRC-DST, src</span><span class="sxs-lookup"><span data-stu-id="30ecd-107">frc dst, src</span></span> |
|--------------|



 

<span data-ttu-id="30ecd-108">where</span><span class="sxs-lookup"><span data-stu-id="30ecd-108">where</span></span>

-   <span data-ttu-id="30ecd-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="30ecd-109">dst is the destination register.</span></span>
-   <span data-ttu-id="30ecd-110">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="30ecd-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="30ecd-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30ecd-111">Remarks</span></span>



| <span data-ttu-id="30ecd-112">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="30ecd-112">Pixel shader versions</span></span> | <span data-ttu-id="30ecd-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="30ecd-113">1\_1</span></span> | <span data-ttu-id="30ecd-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="30ecd-114">1\_2</span></span> | <span data-ttu-id="30ecd-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="30ecd-115">1\_3</span></span> | <span data-ttu-id="30ecd-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="30ecd-116">1\_4</span></span> | <span data-ttu-id="30ecd-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="30ecd-117">2\_0</span></span> | <span data-ttu-id="30ecd-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="30ecd-118">2\_x</span></span> | <span data-ttu-id="30ecd-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="30ecd-119">2\_sw</span></span> | <span data-ttu-id="30ecd-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="30ecd-120">3\_0</span></span> | <span data-ttu-id="30ecd-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="30ecd-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="30ecd-122">FRC</span><span class="sxs-lookup"><span data-stu-id="30ecd-122">frc</span></span>                   |      |      |      |      | <span data-ttu-id="30ecd-123">x</span><span class="sxs-lookup"><span data-stu-id="30ecd-123">x</span></span>    | <span data-ttu-id="30ecd-124">x</span><span class="sxs-lookup"><span data-stu-id="30ecd-124">x</span></span>    | <span data-ttu-id="30ecd-125">x</span><span class="sxs-lookup"><span data-stu-id="30ecd-125">x</span></span>     | <span data-ttu-id="30ecd-126">x</span><span class="sxs-lookup"><span data-stu-id="30ecd-126">x</span></span>    | <span data-ttu-id="30ecd-127">x</span><span class="sxs-lookup"><span data-stu-id="30ecd-127">x</span></span>     |



 

<span data-ttu-id="30ecd-128">Der folgende Code Ausschnitt zeigt konzeptionell, wie die Anweisung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="30ecd-128">The following code snippet shows conceptually how the instruction operates.</span></span>


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



<span data-ttu-id="30ecd-129">Die Floor-Funktion konvertiert das Argument, das an die größte Ganzzahl, die kleiner oder gleich dem Argument ist, an die größte Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="30ecd-129">The floor function converts the argument passed in to the greatest integer that is less than (or equal to) the argument.</span></span> <span data-ttu-id="30ecd-130">Diese wird in einen float-Wert konvertiert und dann den ursprünglichen Wert von Abbildung subtrahiert.</span><span class="sxs-lookup"><span data-stu-id="30ecd-130">This is converted to a float and then subtracted fom the original value.</span></span> <span data-ttu-id="30ecd-131">Der resultierende Bruch Wert liegt zwischen 0,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="30ecd-131">The resulting fractional value ranges from 0.0 through 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30ecd-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="30ecd-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30ecd-133">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="30ecd-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




