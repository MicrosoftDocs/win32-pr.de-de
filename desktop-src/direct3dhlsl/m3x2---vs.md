---
title: m3x2-vs
description: Multipliziert einen 3-Komponenten Vektor mit einer 3 x 2-Matrix. | m3x2-vs
ms.assetid: 4ef3bd47-3e38-4d9d-a8f5-6ee9c08de69c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 870a8d4918870930faa536ead01dab2947d5faea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219193"
---
# <a name="m3x2---vs"></a><span data-ttu-id="9c79b-104">m3x2-vs</span><span class="sxs-lookup"><span data-stu-id="9c79b-104">m3x2 - vs</span></span>

<span data-ttu-id="9c79b-105">Multipliziert einen 3-Komponenten Vektor mit einer 3 x 2-Matrix.</span><span class="sxs-lookup"><span data-stu-id="9c79b-105">Multiplies a 3-component vector by a 3x2 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c79b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c79b-106">Syntax</span></span>



| <span data-ttu-id="9c79b-107">m3x2 DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="9c79b-107">m3x2 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="9c79b-108">where</span><span class="sxs-lookup"><span data-stu-id="9c79b-108">where</span></span>

-   <span data-ttu-id="9c79b-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="9c79b-109">dst is the destination register.</span></span> <span data-ttu-id="9c79b-110">Das Ergebnis ist ein Vektor mit zwei Komponenten.</span><span class="sxs-lookup"><span data-stu-id="9c79b-110">Result is a 2-component vector.</span></span>
-   <span data-ttu-id="9c79b-111">src0 ist ein Quell Register, das einen 3-Komponenten Vektor darstellt.</span><span class="sxs-lookup"><span data-stu-id="9c79b-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="9c79b-112">Quelle1 ist ein Quell Register, das eine 3 x 2-Matrix darstellt, die dem ersten von 2 aufeinander folgenden Registern entspricht.</span><span class="sxs-lookup"><span data-stu-id="9c79b-112">src1 is a source register representing a 3x2 matrix, which corresponds to the first of 2 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c79b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c79b-113">Remarks</span></span>



| <span data-ttu-id="9c79b-114">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="9c79b-114">Vertex shader versions</span></span> | <span data-ttu-id="9c79b-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="9c79b-115">1\_1</span></span> | <span data-ttu-id="9c79b-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9c79b-116">2\_0</span></span> | <span data-ttu-id="9c79b-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9c79b-117">2\_x</span></span> | <span data-ttu-id="9c79b-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9c79b-118">2\_sw</span></span> | <span data-ttu-id="9c79b-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9c79b-119">3\_0</span></span> | <span data-ttu-id="9c79b-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9c79b-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="9c79b-121">m3x2</span><span class="sxs-lookup"><span data-stu-id="9c79b-121">m3x2</span></span>                   | <span data-ttu-id="9c79b-122">x</span><span class="sxs-lookup"><span data-stu-id="9c79b-122">x</span></span>    | <span data-ttu-id="9c79b-123">x</span><span class="sxs-lookup"><span data-stu-id="9c79b-123">x</span></span>    | <span data-ttu-id="9c79b-124">x</span><span class="sxs-lookup"><span data-stu-id="9c79b-124">x</span></span>    | <span data-ttu-id="9c79b-125">x</span><span class="sxs-lookup"><span data-stu-id="9c79b-125">x</span></span>     | <span data-ttu-id="9c79b-126">x</span><span class="sxs-lookup"><span data-stu-id="9c79b-126">x</span></span>    | <span data-ttu-id="9c79b-127">x</span><span class="sxs-lookup"><span data-stu-id="9c79b-127">x</span></span>     |



 

<span data-ttu-id="9c79b-128">Die XY-Maske ist für das Ziel Register erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9c79b-128">The xy mask is required for the destination register.</span></span> <span data-ttu-id="9c79b-129">Negate-und Swizzle-Modifizierern sind für src0, aber nicht für Quelle1 zulässig.</span><span class="sxs-lookup"><span data-stu-id="9c79b-129">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="9c79b-130">Die folgenden Gleichungen zeigen die Funktionsweise der Anweisung:</span><span class="sxs-lookup"><span data-stu-id="9c79b-130">The following equations show how the instruction operates:</span></span>


```
dest.x = (src0.x * src1.x) + (src0.x * src1.y) + (src0.x * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
```



<span data-ttu-id="9c79b-131">Der Eingabe Vektor befindet sich im Register src0.</span><span class="sxs-lookup"><span data-stu-id="9c79b-131">The input vector is in register src0.</span></span> <span data-ttu-id="9c79b-132">Die 3 x 2-Eingabe Matrix befindet sich in Register Quelle1 und das nächste höhere Register in derselben Register Datei, wie in der folgenden Erweiterung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9c79b-132">The input 3x2 matrix is in register src1 and the next higher register in the same register file, as shown in the following expansion.</span></span> <span data-ttu-id="9c79b-133">Ein 2D-Ergebnis wird erzeugt, wobei die anderen Elemente des Ziel Registers (dest. z und dest. w) nicht betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="9c79b-133">A 2D result is produced, leaving the other elements of the destination register (dest.z and dest.w) unaffected.</span></span>

<span data-ttu-id="9c79b-134">Dieser Vorgang wird häufig für 2D-Transformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c79b-134">This operation is commonly used for 2D transforms.</span></span> <span data-ttu-id="9c79b-135">Diese Anweisung wird als Paar von Punkt Produkten implementiert, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9c79b-135">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



<span data-ttu-id="9c79b-136">Die Modifizierern "Swizzle" und "Negation" sind für das Quelle1 Register ungültig.</span><span class="sxs-lookup"><span data-stu-id="9c79b-136">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="9c79b-137">Das dest-und src0-Register oder eine beliebige Registrierung von Quelle1 + i darf nicht identisch sein.</span><span class="sxs-lookup"><span data-stu-id="9c79b-137">The dest and src0 register, or any of src1+i registers, cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c79b-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c79b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c79b-139">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="9c79b-139">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




