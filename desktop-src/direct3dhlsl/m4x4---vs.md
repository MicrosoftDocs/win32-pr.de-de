---
title: M4x4-vs
description: Multipliziert einen 4-Komponenten Vektor mit einer 4 x 4-Matrix. | M4x4-vs
ms.assetid: 016100ac-e316-41fd-a606-271be7394a1a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 846802f46cd829b3e610ec016a546c5302895bd9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219190"
---
# <a name="m4x4---vs"></a><span data-ttu-id="d2bf3-104">M4x4-vs</span><span class="sxs-lookup"><span data-stu-id="d2bf3-104">m4x4 - vs</span></span>

<span data-ttu-id="d2bf3-105">Multipliziert einen 4-Komponenten Vektor mit einer 4 x 4-Matrix.</span><span class="sxs-lookup"><span data-stu-id="d2bf3-105">Multiplies a 4-component vector by a 4x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2bf3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2bf3-106">Syntax</span></span>



| <span data-ttu-id="d2bf3-107">M4x4 DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="d2bf3-107">m4x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="d2bf3-108">where</span><span class="sxs-lookup"><span data-stu-id="d2bf3-108">where</span></span>

-   <span data-ttu-id="d2bf3-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="d2bf3-109">dst is the destination register.</span></span> <span data-ttu-id="d2bf3-110">Das Ergebnis ist ein Vektor mit 4 Komponenten.</span><span class="sxs-lookup"><span data-stu-id="d2bf3-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="d2bf3-111">src0 ist ein Quell Register, das einen 4-Komponenten Vektor darstellt.</span><span class="sxs-lookup"><span data-stu-id="d2bf3-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="d2bf3-112">Quelle1 ist ein Quell Register, das eine 4X4-Matrix darstellt, die dem ersten von vier aufeinander folgenden Registern entspricht.</span><span class="sxs-lookup"><span data-stu-id="d2bf3-112">src1 is a source register representing a 4x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2bf3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2bf3-113">Remarks</span></span>



| <span data-ttu-id="d2bf3-114">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="d2bf3-114">Vertex shader versions</span></span> | <span data-ttu-id="d2bf3-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="d2bf3-115">1\_1</span></span> | <span data-ttu-id="d2bf3-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d2bf3-116">2\_0</span></span> | <span data-ttu-id="d2bf3-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d2bf3-117">2\_x</span></span> | <span data-ttu-id="d2bf3-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d2bf3-118">2\_sw</span></span> | <span data-ttu-id="d2bf3-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d2bf3-119">3\_0</span></span> | <span data-ttu-id="d2bf3-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d2bf3-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="d2bf3-121">m4x4</span><span class="sxs-lookup"><span data-stu-id="d2bf3-121">m4x4</span></span>                   | <span data-ttu-id="d2bf3-122">x</span><span class="sxs-lookup"><span data-stu-id="d2bf3-122">x</span></span>    | <span data-ttu-id="d2bf3-123">x</span><span class="sxs-lookup"><span data-stu-id="d2bf3-123">x</span></span>    | <span data-ttu-id="d2bf3-124">x</span><span class="sxs-lookup"><span data-stu-id="d2bf3-124">x</span></span>    | <span data-ttu-id="d2bf3-125">x</span><span class="sxs-lookup"><span data-stu-id="d2bf3-125">x</span></span>     | <span data-ttu-id="d2bf3-126">x</span><span class="sxs-lookup"><span data-stu-id="d2bf3-126">x</span></span>    | <span data-ttu-id="d2bf3-127">x</span><span class="sxs-lookup"><span data-stu-id="d2bf3-127">x</span></span>     |



 

<span data-ttu-id="d2bf3-128">Die xyzw-Maske (Standard) ist für das Ziel Register erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d2bf3-128">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="d2bf3-129">Negate-und Swizzle-Modifizierern sind für src0, aber nicht für Quelle1 zulässig.</span><span class="sxs-lookup"><span data-stu-id="d2bf3-129">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="d2bf3-130">Die Modifizierern "Swizzle" und "Negation" sind für das src0 Register ungültig.</span><span class="sxs-lookup"><span data-stu-id="d2bf3-130">Swizzle and negate modifiers are invalid for the src0 register.</span></span> <span data-ttu-id="d2bf3-131">Die dest-und src0-Register dürfen nicht identisch sein.</span><span class="sxs-lookup"><span data-stu-id="d2bf3-131">The dest and src0 registers cannot be the same.</span></span>

<span data-ttu-id="d2bf3-132">Das folgende Code Fragment zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="d2bf3-132">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + 
        (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + 
        (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + 
        (src0.w * src3.w);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z) + 
        (src0.w * src4.w);
```



<span data-ttu-id="d2bf3-133">Der Eingabe Vektor befindet sich im Register src0.</span><span class="sxs-lookup"><span data-stu-id="d2bf3-133">The input vector is in register src0.</span></span> <span data-ttu-id="d2bf3-134">Die Eingabe 4X4-Matrix befindet sich in Register Quelle1 und die nächsten drei höheren Register, wie in der folgenden Erweiterung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2bf3-134">The input 4x4 matrix is in register src1, and the next three higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="d2bf3-135">Dieser Vorgang wird häufig verwendet, um eine Position durch eine Projektions Matrix zu transformieren.</span><span class="sxs-lookup"><span data-stu-id="d2bf3-135">This operation is commonly used for transforming a position by a projection matrix.</span></span> <span data-ttu-id="d2bf3-136">Diese Anweisung wird als eine Reihe von Punkt Produkten implementiert, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2bf3-136">This instruction is implemented as a series of dot products as shown here.</span></span>


```
m4x4   r0.xyzw, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
dp4   r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="d2bf3-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d2bf3-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2bf3-138">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="d2bf3-138">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




