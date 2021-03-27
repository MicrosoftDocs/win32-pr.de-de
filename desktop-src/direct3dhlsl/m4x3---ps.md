---
title: m4x3-PS
description: Multipliziert einen 4-Komponenten Vektor mit einer 4X3-Matrix. | m4x3-PS
ms.assetid: cf9ae4c3-6cdf-4c6f-b34c-0ebd3c8a4123
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7787268906c2c9e92dc1e3fa1ec87c4af3079255
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981936"
---
# <a name="m4x3---ps"></a><span data-ttu-id="c5cf1-104">m4x3-PS</span><span class="sxs-lookup"><span data-stu-id="c5cf1-104">m4x3 - ps</span></span>

<span data-ttu-id="c5cf1-105">Multipliziert einen 4-Komponenten Vektor mit einer 4X3-Matrix.</span><span class="sxs-lookup"><span data-stu-id="c5cf1-105">Multiplies a 4-component vector by a 4x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5cf1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5cf1-106">Syntax</span></span>



| <span data-ttu-id="c5cf1-107">m4x3 DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="c5cf1-107">m4x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="c5cf1-108">where</span><span class="sxs-lookup"><span data-stu-id="c5cf1-108">where</span></span>

-   <span data-ttu-id="c5cf1-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="c5cf1-109">dst is the destination register.</span></span> <span data-ttu-id="c5cf1-110">Das Ergebnis ist ein Vektor mit drei Komponenten.</span><span class="sxs-lookup"><span data-stu-id="c5cf1-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="c5cf1-111">src0 ist ein Quell Register, das einen 4-Komponenten Vektor darstellt.</span><span class="sxs-lookup"><span data-stu-id="c5cf1-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="c5cf1-112">Quelle1 ist ein Quell Register, das eine 4X3-Matrix darstellt, die dem ersten von drei aufeinander folgenden Registern entspricht.</span><span class="sxs-lookup"><span data-stu-id="c5cf1-112">src1 is a source register representing a 4x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5cf1-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5cf1-113">Remarks</span></span>



| <span data-ttu-id="c5cf1-114">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="c5cf1-114">Pixel shader versions</span></span> | <span data-ttu-id="c5cf1-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="c5cf1-115">1\_1</span></span> | <span data-ttu-id="c5cf1-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="c5cf1-116">1\_2</span></span> | <span data-ttu-id="c5cf1-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c5cf1-117">1\_3</span></span> | <span data-ttu-id="c5cf1-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="c5cf1-118">1\_4</span></span> | <span data-ttu-id="c5cf1-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c5cf1-119">2\_0</span></span> | <span data-ttu-id="c5cf1-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c5cf1-120">2\_x</span></span> | <span data-ttu-id="c5cf1-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c5cf1-121">2\_sw</span></span> | <span data-ttu-id="c5cf1-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c5cf1-122">3\_0</span></span> | <span data-ttu-id="c5cf1-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c5cf1-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c5cf1-124">m4x3</span><span class="sxs-lookup"><span data-stu-id="c5cf1-124">m4x3</span></span>                  |      |      |      |      | <span data-ttu-id="c5cf1-125">x</span><span class="sxs-lookup"><span data-stu-id="c5cf1-125">x</span></span>    | <span data-ttu-id="c5cf1-126">x</span><span class="sxs-lookup"><span data-stu-id="c5cf1-126">x</span></span>    | <span data-ttu-id="c5cf1-127">x</span><span class="sxs-lookup"><span data-stu-id="c5cf1-127">x</span></span>     | <span data-ttu-id="c5cf1-128">x</span><span class="sxs-lookup"><span data-stu-id="c5cf1-128">x</span></span>    | <span data-ttu-id="c5cf1-129">x</span><span class="sxs-lookup"><span data-stu-id="c5cf1-129">x</span></span>     |



 

<span data-ttu-id="c5cf1-130">Die XYZ-Maske ist für das Ziel Register erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c5cf1-130">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="c5cf1-131">Negate-und Swizzle-Modifizierern sind für src0, aber nicht für Quelle1 zulässig.</span><span class="sxs-lookup"><span data-stu-id="c5cf1-131">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="c5cf1-132">Der folgende Code Ausschnitt zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="c5cf1-132">The following code snippet shows the operations performed.</span></span>


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
```



<span data-ttu-id="c5cf1-133">Der Eingabe Vektor befindet sich im Register src0.</span><span class="sxs-lookup"><span data-stu-id="c5cf1-133">The input vector is in register src0.</span></span> <span data-ttu-id="c5cf1-134">Die Eingabe 4X3-Matrix befindet sich im Register Quelle1 und den nächsten zwei höheren Registern, wie in der folgenden Erweiterung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c5cf1-134">The input 4x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="c5cf1-135">Ein 3D-Ergebnis wird erzeugt, wobei das andere Element des Ziel Registers (dest. w) nicht betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="c5cf1-135">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="c5cf1-136">Dieser Vorgang wird häufig verwendet, um einen Positions Vektor durch eine Matrix zu transformieren, die keine Projective Auswirkung hat, wie z. b. bei Transformationen im Modellbereich.</span><span class="sxs-lookup"><span data-stu-id="c5cf1-136">This operation is commonly used for transforming a position vector by a matrix that has no projective effect, such as occurs in model-space transformations.</span></span> <span data-ttu-id="c5cf1-137">Diese Anweisung wird als Satz von Punkt Produkten implementiert, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c5cf1-137">This instruction is implemented as a set of dot products as shown below.</span></span>


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



<span data-ttu-id="c5cf1-138">Die Modifizierern "Swizzle" und "Negation" sind für das Quelle1 Register ungültig.</span><span class="sxs-lookup"><span data-stu-id="c5cf1-138">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="c5cf1-139">Das DST-und src0-Register dürfen nicht identisch sein.</span><span class="sxs-lookup"><span data-stu-id="c5cf1-139">The dst and src0 register cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5cf1-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c5cf1-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5cf1-141">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="c5cf1-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




