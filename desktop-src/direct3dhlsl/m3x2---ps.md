---
title: m3x2-PS
description: Multipliziert einen 3-Komponenten Vektor mit einer 3 x 2-Matrix. | m3x2-PS
ms.assetid: a88e6228-a61a-408c-8d89-a5706dd146d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26532c78fa829b9c2a41f715b814ee8a0f44c879
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982012"
---
# <a name="m3x2---ps"></a><span data-ttu-id="f3632-104">m3x2-PS</span><span class="sxs-lookup"><span data-stu-id="f3632-104">m3x2 - ps</span></span>

<span data-ttu-id="f3632-105">Multipliziert einen 3-Komponenten Vektor mit einer 3 x 2-Matrix.</span><span class="sxs-lookup"><span data-stu-id="f3632-105">Multiplies a 3-component vector by a 3x2 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3632-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3632-106">Syntax</span></span>



| <span data-ttu-id="f3632-107">m3x2 DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="f3632-107">m3x2 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="f3632-108">where</span><span class="sxs-lookup"><span data-stu-id="f3632-108">where</span></span>

-   <span data-ttu-id="f3632-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="f3632-109">dst is the destination register.</span></span> <span data-ttu-id="f3632-110">Das Ergebnis ist ein Vektor mit zwei Komponenten.</span><span class="sxs-lookup"><span data-stu-id="f3632-110">Result is a 2-component vector.</span></span>
-   <span data-ttu-id="f3632-111">src0 ist ein Quell Register, das einen 3-Komponenten Vektor darstellt.</span><span class="sxs-lookup"><span data-stu-id="f3632-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="f3632-112">Quelle1 ist ein Quell Register, das eine 3 x 2-Matrix darstellt, die dem ersten von 2 aufeinander folgenden Registern entspricht.</span><span class="sxs-lookup"><span data-stu-id="f3632-112">src1 is a source register representing a 3x2 matrix, which corresponds to the first of 2 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3632-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3632-113">Remarks</span></span>



| <span data-ttu-id="f3632-114">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="f3632-114">Pixel shader versions</span></span> | <span data-ttu-id="f3632-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="f3632-115">1\_1</span></span> | <span data-ttu-id="f3632-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="f3632-116">1\_2</span></span> | <span data-ttu-id="f3632-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f3632-117">1\_3</span></span> | <span data-ttu-id="f3632-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="f3632-118">1\_4</span></span> | <span data-ttu-id="f3632-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f3632-119">2\_0</span></span> | <span data-ttu-id="f3632-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f3632-120">2\_x</span></span> | <span data-ttu-id="f3632-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f3632-121">2\_sw</span></span> | <span data-ttu-id="f3632-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f3632-122">3\_0</span></span> | <span data-ttu-id="f3632-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f3632-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f3632-124">m3x2</span><span class="sxs-lookup"><span data-stu-id="f3632-124">m3x2</span></span>                  |      |      |      |      | <span data-ttu-id="f3632-125">x</span><span class="sxs-lookup"><span data-stu-id="f3632-125">x</span></span>    | <span data-ttu-id="f3632-126">x</span><span class="sxs-lookup"><span data-stu-id="f3632-126">x</span></span>    | <span data-ttu-id="f3632-127">x</span><span class="sxs-lookup"><span data-stu-id="f3632-127">x</span></span>     | <span data-ttu-id="f3632-128">x</span><span class="sxs-lookup"><span data-stu-id="f3632-128">x</span></span>    | <span data-ttu-id="f3632-129">x</span><span class="sxs-lookup"><span data-stu-id="f3632-129">x</span></span>     |



 

<span data-ttu-id="f3632-130">Die XY-Maske ist für das Ziel Register erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f3632-130">The xy mask is required for the destination register.</span></span> <span data-ttu-id="f3632-131">Negate-und Swizzle-Modifizierern sind für src0, aber nicht für Quelle1 zulässig.</span><span class="sxs-lookup"><span data-stu-id="f3632-131">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="f3632-132">Die folgenden Gleichungen zeigen die Funktionsweise der Anweisung:</span><span class="sxs-lookup"><span data-stu-id="f3632-132">The following equations show how the instruction operates:</span></span>


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
```



<span data-ttu-id="f3632-133">Der Eingabe Vektor befindet sich im Register src0.</span><span class="sxs-lookup"><span data-stu-id="f3632-133">The input vector is in register src0.</span></span> <span data-ttu-id="f3632-134">Die 3 x 2-Eingabe Matrix befindet sich in Register Quelle1 und das nächste höhere Register in derselben Register Datei, wie in der folgenden Erweiterung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f3632-134">The input 3x2 matrix is in register src1 and the next higher register in the same register file, as shown in the following expansion.</span></span> <span data-ttu-id="f3632-135">Ein 2D-Ergebnis wird erzeugt, wobei die anderen Elemente des Ziel Registers (dest. z und dest. w) nicht betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="f3632-135">A 2D result is produced, leaving the other elements of the destination register (dest.z and dest.w) unaffected.</span></span>

<span data-ttu-id="f3632-136">Dieser Vorgang wird häufig für 2D-Transformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="f3632-136">This operation is commonly used for 2D transforms.</span></span> <span data-ttu-id="f3632-137">Diese Anweisung wird als Paar von Punkt Produkten implementiert, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f3632-137">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



<span data-ttu-id="f3632-138">Die Modifizierern "Swizzle" und "Negation" sind für das Quelle1 Register ungültig.</span><span class="sxs-lookup"><span data-stu-id="f3632-138">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="f3632-139">Das DST-und src0-Register oder eine beliebige Registrierung von Quelle1 + i dürfen nicht identisch sein.</span><span class="sxs-lookup"><span data-stu-id="f3632-139">The dst and src0 register, or any of src1+i registers, cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3632-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f3632-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3632-141">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="f3632-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




