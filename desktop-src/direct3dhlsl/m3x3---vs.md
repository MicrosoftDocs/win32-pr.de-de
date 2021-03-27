---
title: M3x3-vs
description: Multipliziert einen 3-Komponenten Vektor mit einer 3X3-Matrix. | M3x3-vs
ms.assetid: 6a749ed0-097d-4354-bc70-fbcd879eafab
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e75cdb4b098b92ea358c32e40b3948c7ac73e0cf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104394001"
---
# <a name="m3x3---vs"></a><span data-ttu-id="e4bab-104">M3x3-vs</span><span class="sxs-lookup"><span data-stu-id="e4bab-104">m3x3 - vs</span></span>

<span data-ttu-id="e4bab-105">Multipliziert einen 3-Komponenten Vektor mit einer 3X3-Matrix.</span><span class="sxs-lookup"><span data-stu-id="e4bab-105">Multiplies a 3-component vector by a 3x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4bab-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4bab-106">Syntax</span></span>



| <span data-ttu-id="e4bab-107">M3x3 DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="e4bab-107">m3x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="e4bab-108">where</span><span class="sxs-lookup"><span data-stu-id="e4bab-108">where</span></span>

-   <span data-ttu-id="e4bab-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="e4bab-109">dst is the destination register.</span></span> <span data-ttu-id="e4bab-110">Das Ergebnis ist ein Vektor mit drei Komponenten.</span><span class="sxs-lookup"><span data-stu-id="e4bab-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="e4bab-111">src0 ist ein Quell Register, das einen 3-Komponenten Vektor darstellt.</span><span class="sxs-lookup"><span data-stu-id="e4bab-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="e4bab-112">Quelle1 ist ein Quell Register, das eine 3X3-Matrix darstellt, die dem ersten von drei aufeinander folgenden Registern entspricht.</span><span class="sxs-lookup"><span data-stu-id="e4bab-112">src1 is a source register representing a 3x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4bab-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4bab-113">Remarks</span></span>



| <span data-ttu-id="e4bab-114">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="e4bab-114">Vertex shader versions</span></span> | <span data-ttu-id="e4bab-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="e4bab-115">1\_1</span></span> | <span data-ttu-id="e4bab-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e4bab-116">2\_0</span></span> | <span data-ttu-id="e4bab-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e4bab-117">2\_x</span></span> | <span data-ttu-id="e4bab-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e4bab-118">2\_sw</span></span> | <span data-ttu-id="e4bab-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e4bab-119">3\_0</span></span> | <span data-ttu-id="e4bab-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e4bab-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="e4bab-121">m3x3</span><span class="sxs-lookup"><span data-stu-id="e4bab-121">m3x3</span></span>                   | <span data-ttu-id="e4bab-122">x</span><span class="sxs-lookup"><span data-stu-id="e4bab-122">x</span></span>    | <span data-ttu-id="e4bab-123">x</span><span class="sxs-lookup"><span data-stu-id="e4bab-123">x</span></span>    | <span data-ttu-id="e4bab-124">x</span><span class="sxs-lookup"><span data-stu-id="e4bab-124">x</span></span>    | <span data-ttu-id="e4bab-125">x</span><span class="sxs-lookup"><span data-stu-id="e4bab-125">x</span></span>     | <span data-ttu-id="e4bab-126">x</span><span class="sxs-lookup"><span data-stu-id="e4bab-126">x</span></span>    | <span data-ttu-id="e4bab-127">x</span><span class="sxs-lookup"><span data-stu-id="e4bab-127">x</span></span>     |



 

<span data-ttu-id="e4bab-128">Die XYZ-Maske ist für das Ziel Register erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e4bab-128">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="e4bab-129">Negate-und Swizzle-Modifizierern sind für src0, aber nicht für Quelle1 zulässig.</span><span class="sxs-lookup"><span data-stu-id="e4bab-129">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="e4bab-130">Das folgende Code Fragment zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="e4bab-130">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



<span data-ttu-id="e4bab-131">Der Eingabe Vektor befindet sich im Register src0.</span><span class="sxs-lookup"><span data-stu-id="e4bab-131">The input vector is in register src0.</span></span> <span data-ttu-id="e4bab-132">Die 3X3-Eingabe Matrix befindet sich im Register Quelle1 und den nächsten zwei höheren Registern, wie in der folgenden Erweiterung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e4bab-132">The input 3x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="e4bab-133">Ein 3D-Ergebnis wird erzeugt, wobei das andere Element des Ziel Registers (dest. w) nicht betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="e4bab-133">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="e4bab-134">Dieser Vorgang wird häufig verwendet, um normale Vektoren während der Beleuchtungsberechnungen zu transformieren.</span><span class="sxs-lookup"><span data-stu-id="e4bab-134">This operation is commonly used for transforming normal vectors during lighting computations.</span></span> <span data-ttu-id="e4bab-135">Diese Anweisung wird als Paar von Punkt Produkten implementiert, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e4bab-135">This instruction is implemented as a pair of dot products as shown below.</span></span>


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a><span data-ttu-id="e4bab-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4bab-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4bab-137">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="e4bab-137">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




