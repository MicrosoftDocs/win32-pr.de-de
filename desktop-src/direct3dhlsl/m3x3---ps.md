---
title: M3x3-PS
description: Multipliziert einen 3-Komponenten Vektor mit einer 3X3-Matrix. | M3x3-PS
ms.assetid: 71342e05-69a6-41f4-bafb-643f0ceb0a59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ac72acd2133c8b34393bdd1ab7de8aec1df4db5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981912"
---
# <a name="m3x3---ps"></a><span data-ttu-id="efeaa-104">M3x3-PS</span><span class="sxs-lookup"><span data-stu-id="efeaa-104">m3x3 - ps</span></span>

<span data-ttu-id="efeaa-105">Multipliziert einen 3-Komponenten Vektor mit einer 3X3-Matrix.</span><span class="sxs-lookup"><span data-stu-id="efeaa-105">Multiplies a 3-component vector by a 3x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="efeaa-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="efeaa-106">Syntax</span></span>



| <span data-ttu-id="efeaa-107">M3x3 DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="efeaa-107">m3x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="efeaa-108">where</span><span class="sxs-lookup"><span data-stu-id="efeaa-108">where</span></span>

-   <span data-ttu-id="efeaa-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="efeaa-109">dst is the destination register.</span></span> <span data-ttu-id="efeaa-110">Das Ergebnis ist ein Vektor mit drei Komponenten.</span><span class="sxs-lookup"><span data-stu-id="efeaa-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="efeaa-111">src0 ist ein Quell Register, das einen 3-Komponenten Vektor darstellt.</span><span class="sxs-lookup"><span data-stu-id="efeaa-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="efeaa-112">Quelle1 ist ein Quell Register, das eine 3X3-Matrix darstellt, die dem ersten von drei aufeinander folgenden Registern entspricht.</span><span class="sxs-lookup"><span data-stu-id="efeaa-112">src1 is a source register representing a 3x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="efeaa-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="efeaa-113">Remarks</span></span>



| <span data-ttu-id="efeaa-114">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="efeaa-114">Pixel shader versions</span></span> | <span data-ttu-id="efeaa-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="efeaa-115">1\_1</span></span> | <span data-ttu-id="efeaa-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="efeaa-116">1\_2</span></span> | <span data-ttu-id="efeaa-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="efeaa-117">1\_3</span></span> | <span data-ttu-id="efeaa-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="efeaa-118">1\_4</span></span> | <span data-ttu-id="efeaa-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="efeaa-119">2\_0</span></span> | <span data-ttu-id="efeaa-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="efeaa-120">2\_x</span></span> | <span data-ttu-id="efeaa-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="efeaa-121">2\_sw</span></span> | <span data-ttu-id="efeaa-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="efeaa-122">3\_0</span></span> | <span data-ttu-id="efeaa-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="efeaa-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="efeaa-124">m3x3</span><span class="sxs-lookup"><span data-stu-id="efeaa-124">m3x3</span></span>                  |      |      |      |      | <span data-ttu-id="efeaa-125">x</span><span class="sxs-lookup"><span data-stu-id="efeaa-125">x</span></span>    | <span data-ttu-id="efeaa-126">x</span><span class="sxs-lookup"><span data-stu-id="efeaa-126">x</span></span>    | <span data-ttu-id="efeaa-127">x</span><span class="sxs-lookup"><span data-stu-id="efeaa-127">x</span></span>     | <span data-ttu-id="efeaa-128">x</span><span class="sxs-lookup"><span data-stu-id="efeaa-128">x</span></span>    | <span data-ttu-id="efeaa-129">x</span><span class="sxs-lookup"><span data-stu-id="efeaa-129">x</span></span>     |



 

<span data-ttu-id="efeaa-130">Die XYZ-Maske ist für das Ziel Register erforderlich.</span><span class="sxs-lookup"><span data-stu-id="efeaa-130">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="efeaa-131">Negate-und Swizzle-Modifizierern sind für src0, aber nicht für Quelle1 zulässig.</span><span class="sxs-lookup"><span data-stu-id="efeaa-131">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="efeaa-132">Der folgende Code Ausschnitt zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="efeaa-132">The following code snippet shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



<span data-ttu-id="efeaa-133">Der Eingabe Vektor befindet sich im Register src0.</span><span class="sxs-lookup"><span data-stu-id="efeaa-133">The input vector is in register src0.</span></span> <span data-ttu-id="efeaa-134">Die 3X3-Eingabe Matrix befindet sich im Register Quelle1 und den nächsten zwei höheren Registern, wie in der folgenden Erweiterung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="efeaa-134">The input 3x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="efeaa-135">Ein 3D-Ergebnis wird erzeugt, wobei das andere Element des Ziel Registers (dest. w) nicht betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="efeaa-135">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="efeaa-136">Dieser Vorgang wird häufig verwendet, um normale Vektoren während der Beleuchtungsberechnungen zu transformieren.</span><span class="sxs-lookup"><span data-stu-id="efeaa-136">This operation is commonly used for transforming normal vectors during lighting computations.</span></span> <span data-ttu-id="efeaa-137">Diese Anweisung wird als Satz von Punkt Produkten implementiert, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="efeaa-137">This instruction is implemented as a set of dot products as shown below.</span></span>


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a><span data-ttu-id="efeaa-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="efeaa-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efeaa-139">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="efeaa-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




