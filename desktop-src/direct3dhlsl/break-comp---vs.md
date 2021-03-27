---
title: break_comp vs
description: Unterbrechen Sie die aktuelle Schleife bedingt bei den nächstgelegenen endschleifen-vs oder ENDREP-vs.
ms.assetid: 01745e03-874a-4594-b6ab-12db22d0cb4a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 631998aeba6612d945495d8115a74d00f7e657c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857779"
---
# <a name="break_comp---vs"></a><span data-ttu-id="4e4ad-103">" \_ Comp-vs" Abbrechen</span><span class="sxs-lookup"><span data-stu-id="4e4ad-103">break\_comp - vs</span></span>

<span data-ttu-id="4e4ad-104">Unterbrechen Sie die aktuelle Schleife bedingt bei den nächstgelegenen [endschleifen-vs](endloop---vs.md) oder [ENDREP-vs](endrep---vs.md).</span><span class="sxs-lookup"><span data-stu-id="4e4ad-104">Conditionally break out of the current loop at the nearest [endloop - vs](endloop---vs.md) or [endrep - vs](endrep---vs.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4e4ad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e4ad-105">Syntax</span></span>



| <span data-ttu-id="4e4ad-106">Break \_ Comp src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="4e4ad-106">break\_comp src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="4e4ad-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="4e4ad-107">Where:</span></span>

-   <span data-ttu-id="4e4ad-108">\_comp ist ein Vergleich zwischen den beiden Quell Registern.</span><span class="sxs-lookup"><span data-stu-id="4e4ad-108">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="4e4ad-109">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="4e4ad-109">It can be one of the following:</span></span> 

    | <span data-ttu-id="4e4ad-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e4ad-110">Syntax</span></span> | <span data-ttu-id="4e4ad-111">Vergleich</span><span class="sxs-lookup"><span data-stu-id="4e4ad-111">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="4e4ad-112">\_siegt</span><span class="sxs-lookup"><span data-stu-id="4e4ad-112">\_gt</span></span>   | <span data-ttu-id="4e4ad-113">Größer als</span><span class="sxs-lookup"><span data-stu-id="4e4ad-113">Greater than</span></span>          |
    | <span data-ttu-id="4e4ad-114">\_General</span><span class="sxs-lookup"><span data-stu-id="4e4ad-114">\_lt</span></span>   | <span data-ttu-id="4e4ad-115">Kleiner als</span><span class="sxs-lookup"><span data-stu-id="4e4ad-115">Less than</span></span>             |
    | <span data-ttu-id="4e4ad-116">\_Färbung</span><span class="sxs-lookup"><span data-stu-id="4e4ad-116">\_ge</span></span>   | <span data-ttu-id="4e4ad-117">Größer als oder gleich</span><span class="sxs-lookup"><span data-stu-id="4e4ad-117">Greater than or equal</span></span> |
    | <span data-ttu-id="4e4ad-118">\_Kirchturm</span><span class="sxs-lookup"><span data-stu-id="4e4ad-118">\_le</span></span>   | <span data-ttu-id="4e4ad-119">Kleiner als oder gleich</span><span class="sxs-lookup"><span data-stu-id="4e4ad-119">Less than or equal</span></span>    |
    | <span data-ttu-id="4e4ad-120">\_stecken</span><span class="sxs-lookup"><span data-stu-id="4e4ad-120">\_eq</span></span>   | <span data-ttu-id="4e4ad-121">Gleich</span><span class="sxs-lookup"><span data-stu-id="4e4ad-121">Equal to</span></span>              |
    | <span data-ttu-id="4e4ad-122">\_NES</span><span class="sxs-lookup"><span data-stu-id="4e4ad-122">\_ne</span></span>   | <span data-ttu-id="4e4ad-123">Ungleich</span><span class="sxs-lookup"><span data-stu-id="4e4ad-123">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="4e4ad-124">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="4e4ad-124">src0 is a source register.</span></span> <span data-ttu-id="4e4ad-125">Das Replizieren der Replizierung ist erforderlich, um eine einzelne Komponente auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="4e4ad-125">Replicate swizzle is required to select a single component.</span></span>
-   <span data-ttu-id="4e4ad-126">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="4e4ad-126">src1 is a source register.</span></span> <span data-ttu-id="4e4ad-127">Das Replizieren der Replizierung ist erforderlich, um eine einzelne Komponente auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="4e4ad-127">Replicate swizzle is required to select a single component.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e4ad-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e4ad-128">Remarks</span></span>

<span data-ttu-id="4e4ad-129">Diese Anweisung wird in den folgenden Versionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4e4ad-129">This instruction is supported in the following versions.</span></span>



| <span data-ttu-id="4e4ad-130">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="4e4ad-130">Vertex shader versions</span></span> | <span data-ttu-id="4e4ad-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="4e4ad-131">1\_1</span></span> | <span data-ttu-id="4e4ad-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4e4ad-132">2\_0</span></span> | <span data-ttu-id="4e4ad-133">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4e4ad-133">2\_x</span></span> | <span data-ttu-id="4e4ad-134">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4e4ad-134">2\_sw</span></span> | <span data-ttu-id="4e4ad-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4e4ad-135">3\_0</span></span> | <span data-ttu-id="4e4ad-136">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4e4ad-136">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="4e4ad-137">\_Comp Abbrechen</span><span class="sxs-lookup"><span data-stu-id="4e4ad-137">break\_comp</span></span>            |      |      | <span data-ttu-id="4e4ad-138">x</span><span class="sxs-lookup"><span data-stu-id="4e4ad-138">x</span></span>    | <span data-ttu-id="4e4ad-139">x</span><span class="sxs-lookup"><span data-stu-id="4e4ad-139">x</span></span>     | <span data-ttu-id="4e4ad-140">x</span><span class="sxs-lookup"><span data-stu-id="4e4ad-140">x</span></span>    | <span data-ttu-id="4e4ad-141">x</span><span class="sxs-lookup"><span data-stu-id="4e4ad-141">x</span></span>     |



 

<span data-ttu-id="4e4ad-142">Wenn der Vergleich true ist, wird er wie gezeigt aus der aktuellen Schleife unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="4e4ad-142">When the comparison is true, it breaks out of the current loop, as shown.</span></span>


```
if (src0 comparison src1)
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a><span data-ttu-id="4e4ad-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4e4ad-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e4ad-144">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="4e4ad-144">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




