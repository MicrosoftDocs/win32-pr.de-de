---
title: break_comp-PS
description: Unterbrechen Sie die aktuelle Schleife bei den nächstgelegenen ENDLOOP-PS oder ENDREP-PS, basierend auf einem pro-Komponente-Vergleich.
ms.assetid: d21e850f-05db-4a29-b15b-85bb1c1410d0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5088312a16102153ad78afffdcd9ea1275d34e0d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101086"
---
# <a name="break_comp---ps"></a><span data-ttu-id="42543-103">\_Comp-PS Abbrechen</span><span class="sxs-lookup"><span data-stu-id="42543-103">break\_comp - ps</span></span>

<span data-ttu-id="42543-104">Unterbrechen Sie die aktuelle Schleife bei den nächstgelegenen [ENDLOOP-PS](endloop---ps.md) oder [ENDREP-PS](endrep---ps.md), basierend auf einem pro-Komponente-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="42543-104">Break out of the current loop at the nearest [endloop - ps](endloop---ps.md) or [endrep - ps](endrep---ps.md), based on a per-component comparison.</span></span>

## <a name="syntax"></a><span data-ttu-id="42543-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="42543-105">Syntax</span></span>



| <span data-ttu-id="42543-106">Break \_ Comp src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="42543-106">break\_comp src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="42543-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="42543-107">Where:</span></span>

-   <span data-ttu-id="42543-108">\_comp ist ein skalarer (oder einzelner) Vergleich zwischen den beiden Quell Registern.</span><span class="sxs-lookup"><span data-stu-id="42543-108">\_comp is a scalar (or single) comparison between the two source registers.</span></span> <span data-ttu-id="42543-109">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="42543-109">It can be one of the following:</span></span> 

    | <span data-ttu-id="42543-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="42543-110">Syntax</span></span> | <span data-ttu-id="42543-111">Vergleich</span><span class="sxs-lookup"><span data-stu-id="42543-111">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="42543-112">\_siegt</span><span class="sxs-lookup"><span data-stu-id="42543-112">\_gt</span></span>   | <span data-ttu-id="42543-113">Größer als</span><span class="sxs-lookup"><span data-stu-id="42543-113">Greater than</span></span>          |
    | <span data-ttu-id="42543-114">\_General</span><span class="sxs-lookup"><span data-stu-id="42543-114">\_lt</span></span>   | <span data-ttu-id="42543-115">Kleiner als</span><span class="sxs-lookup"><span data-stu-id="42543-115">Less than</span></span>             |
    | <span data-ttu-id="42543-116">\_Färbung</span><span class="sxs-lookup"><span data-stu-id="42543-116">\_ge</span></span>   | <span data-ttu-id="42543-117">Größer als oder gleich</span><span class="sxs-lookup"><span data-stu-id="42543-117">Greater than or equal</span></span> |
    | <span data-ttu-id="42543-118">\_Kirchturm</span><span class="sxs-lookup"><span data-stu-id="42543-118">\_le</span></span>   | <span data-ttu-id="42543-119">Kleiner als oder gleich</span><span class="sxs-lookup"><span data-stu-id="42543-119">Less than or equal</span></span>    |
    | <span data-ttu-id="42543-120">\_stecken</span><span class="sxs-lookup"><span data-stu-id="42543-120">\_eq</span></span>   | <span data-ttu-id="42543-121">Gleich</span><span class="sxs-lookup"><span data-stu-id="42543-121">Equal to</span></span>              |
    | <span data-ttu-id="42543-122">\_NES</span><span class="sxs-lookup"><span data-stu-id="42543-122">\_ne</span></span>   | <span data-ttu-id="42543-123">Ungleich</span><span class="sxs-lookup"><span data-stu-id="42543-123">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="42543-124">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="42543-124">src0 is a source register.</span></span> <span data-ttu-id="42543-125">Bei der Auswahl einer einzelnen Komponente ist das Replizieren von flüchtigen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="42543-125">Replicate swizzle is required if selecting a single component.</span></span>
-   <span data-ttu-id="42543-126">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="42543-126">src1 is a source register.</span></span> <span data-ttu-id="42543-127">Bei der Auswahl einer einzelnen Komponente ist das Replizieren von flüchtigen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="42543-127">Replicate swizzle is required if selecting a single component.</span></span>

## <a name="remarks"></a><span data-ttu-id="42543-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42543-128">Remarks</span></span>

<span data-ttu-id="42543-129">Diese Anweisung wird in den folgenden Versionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42543-129">This instruction is supported in the following versions.</span></span>



| <span data-ttu-id="42543-130">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="42543-130">Pixel shader versions</span></span> | <span data-ttu-id="42543-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="42543-131">1\_1</span></span> | <span data-ttu-id="42543-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="42543-132">1\_2</span></span> | <span data-ttu-id="42543-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="42543-133">1\_3</span></span> | <span data-ttu-id="42543-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="42543-134">1\_4</span></span> | <span data-ttu-id="42543-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="42543-135">2\_0</span></span> | <span data-ttu-id="42543-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="42543-136">2\_x</span></span> | <span data-ttu-id="42543-137">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="42543-137">2\_sw</span></span> | <span data-ttu-id="42543-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="42543-138">3\_0</span></span> | <span data-ttu-id="42543-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="42543-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="42543-140">\_Comp Abbrechen</span><span class="sxs-lookup"><span data-stu-id="42543-140">break\_comp</span></span>           |      |      |      |      |      | <span data-ttu-id="42543-141">x</span><span class="sxs-lookup"><span data-stu-id="42543-141">x</span></span>    | <span data-ttu-id="42543-142">x</span><span class="sxs-lookup"><span data-stu-id="42543-142">x</span></span>     | <span data-ttu-id="42543-143">x</span><span class="sxs-lookup"><span data-stu-id="42543-143">x</span></span>    | <span data-ttu-id="42543-144">x</span><span class="sxs-lookup"><span data-stu-id="42543-144">x</span></span>     |



 

<span data-ttu-id="42543-145">Wenn der Vergleich true ist, wird er wie gezeigt aus der aktuellen Schleife unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="42543-145">When the comparison is true, it breaks out of the current loop, as shown.</span></span>


```
if (!(src0 comparison src1))
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a><span data-ttu-id="42543-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="42543-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42543-147">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="42543-147">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




