---
title: m4x3-vs
description: Multipliziert einen 4-Komponenten Vektor mit einer 4X3-Matrix. | m4x3-vs
ms.assetid: 12dd31bd-2078-44a1-912e-72c8f377bc4c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7608b1187cc90cf4914bdd42a197cc6044d53734
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981304"
---
# <a name="m4x3---vs"></a><span data-ttu-id="b2f6a-104">m4x3-vs</span><span class="sxs-lookup"><span data-stu-id="b2f6a-104">m4x3 - vs</span></span>

<span data-ttu-id="b2f6a-105">Multipliziert einen 4-Komponenten Vektor mit einer 4X3-Matrix.</span><span class="sxs-lookup"><span data-stu-id="b2f6a-105">Multiplies a 4-component vector by a 4x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2f6a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2f6a-106">Syntax</span></span>



| <span data-ttu-id="b2f6a-107">m4x3 DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="b2f6a-107">m4x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="b2f6a-108">where</span><span class="sxs-lookup"><span data-stu-id="b2f6a-108">where</span></span>

-   <span data-ttu-id="b2f6a-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="b2f6a-109">dst is the destination register.</span></span> <span data-ttu-id="b2f6a-110">Das Ergebnis ist ein Vektor mit drei Komponenten.</span><span class="sxs-lookup"><span data-stu-id="b2f6a-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="b2f6a-111">src0 ist ein Quell Register, das einen 4-Komponenten Vektor darstellt.</span><span class="sxs-lookup"><span data-stu-id="b2f6a-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="b2f6a-112">Quelle1 ist ein Quell Register, das eine 4X3-Matrix darstellt, die dem ersten von drei aufeinander folgenden Registern entspricht.</span><span class="sxs-lookup"><span data-stu-id="b2f6a-112">src1 is a source register representing a 4x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2f6a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2f6a-113">Remarks</span></span>



| <span data-ttu-id="b2f6a-114">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="b2f6a-114">Vertex shader versions</span></span> | <span data-ttu-id="b2f6a-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="b2f6a-115">1\_1</span></span> | <span data-ttu-id="b2f6a-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b2f6a-116">2\_0</span></span> | <span data-ttu-id="b2f6a-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b2f6a-117">2\_x</span></span> | <span data-ttu-id="b2f6a-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b2f6a-118">2\_sw</span></span> | <span data-ttu-id="b2f6a-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b2f6a-119">3\_0</span></span> | <span data-ttu-id="b2f6a-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b2f6a-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="b2f6a-121">m4x3</span><span class="sxs-lookup"><span data-stu-id="b2f6a-121">m4x3</span></span>                   | <span data-ttu-id="b2f6a-122">x</span><span class="sxs-lookup"><span data-stu-id="b2f6a-122">x</span></span>    | <span data-ttu-id="b2f6a-123">x</span><span class="sxs-lookup"><span data-stu-id="b2f6a-123">x</span></span>    | <span data-ttu-id="b2f6a-124">x</span><span class="sxs-lookup"><span data-stu-id="b2f6a-124">x</span></span>    | <span data-ttu-id="b2f6a-125">x</span><span class="sxs-lookup"><span data-stu-id="b2f6a-125">x</span></span>     | <span data-ttu-id="b2f6a-126">x</span><span class="sxs-lookup"><span data-stu-id="b2f6a-126">x</span></span>    | <span data-ttu-id="b2f6a-127">x</span><span class="sxs-lookup"><span data-stu-id="b2f6a-127">x</span></span>     |



 

<span data-ttu-id="b2f6a-128">Die XYZ-Maske ist für das Ziel Register erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b2f6a-128">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="b2f6a-129">Negate-und Swizzle-Modifizierern sind für src0, aber nicht für Quelle1 zulässig.</span><span class="sxs-lookup"><span data-stu-id="b2f6a-129">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="b2f6a-130">Das folgende Code Fragment zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="b2f6a-130">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + (src0.w * src3.w);
```



<span data-ttu-id="b2f6a-131">Der Eingabe Vektor befindet sich im Register src0.</span><span class="sxs-lookup"><span data-stu-id="b2f6a-131">The input vector is in register src0.</span></span> <span data-ttu-id="b2f6a-132">Die Eingabe 4X3-Matrix befindet sich im Register Quelle1 und den nächsten zwei höheren Registern, wie in der folgenden Erweiterung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2f6a-132">The input 4x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="b2f6a-133">Ein 3D-Ergebnis wird erzeugt, wobei das andere Element des Ziel Registers (dest. w) nicht betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="b2f6a-133">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="b2f6a-134">Dieser Vorgang wird häufig verwendet, um einen Positions Vektor durch eine Matrix zu transformieren, die keine Projective Auswirkung hat, wie z. b. bei Transformationen im Modellbereich.</span><span class="sxs-lookup"><span data-stu-id="b2f6a-134">This operation is commonly used for transforming a position vector by a matrix that has no projective effect, such as occurs in model-space transformations.</span></span> <span data-ttu-id="b2f6a-135">Diese Anweisung wird als Paar von Punkt Produkten implementiert, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2f6a-135">This instruction is implemented as a pair of dot products as shown below.</span></span>


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



<span data-ttu-id="b2f6a-136">Die Modifizierern "Swizzle" und "Negation" sind für das Quelle1 Register ungültig.</span><span class="sxs-lookup"><span data-stu-id="b2f6a-136">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="b2f6a-137">Das DST-und src0-Register dürfen nicht identisch sein.</span><span class="sxs-lookup"><span data-stu-id="b2f6a-137">The dst and src0 register cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2f6a-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b2f6a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2f6a-139">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="b2f6a-139">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




