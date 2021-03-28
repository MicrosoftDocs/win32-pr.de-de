---
title: M3x4-PS
description: Multipliziert einen 3-Komponenten Vektor mit einer rund m3-Matrix. | M3x4-PS
ms.assetid: b749d3cd-2acf-450c-94f2-fea5e1c8f4d2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c245f4765853301a7c8319c8038b9ed342e3715
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981960"
---
# <a name="m3x4---ps"></a><span data-ttu-id="f144d-104">M3x4-PS</span><span class="sxs-lookup"><span data-stu-id="f144d-104">m3x4 - ps</span></span>

<span data-ttu-id="f144d-105">Multipliziert einen 3-Komponenten Vektor mit einer rund m3-Matrix.</span><span class="sxs-lookup"><span data-stu-id="f144d-105">Multiplies a 3-component vector by a 3x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f144d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f144d-106">Syntax</span></span>



| <span data-ttu-id="f144d-107">M3x4 DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="f144d-107">m3x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="f144d-108">where</span><span class="sxs-lookup"><span data-stu-id="f144d-108">where</span></span>

-   <span data-ttu-id="f144d-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="f144d-109">dst is the destination register.</span></span> <span data-ttu-id="f144d-110">Das Ergebnis ist ein Vektor mit 4 Komponenten.</span><span class="sxs-lookup"><span data-stu-id="f144d-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="f144d-111">src0 ist ein Quell Register, das einen 3-Komponenten Vektor darstellt.</span><span class="sxs-lookup"><span data-stu-id="f144d-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="f144d-112">Quelle1 ist ein Quell Register, das eine rund m3-Matrix darstellt, die dem ersten von vier aufeinander folgenden Registern entspricht.</span><span class="sxs-lookup"><span data-stu-id="f144d-112">src1 is a source register representing a 3x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="f144d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f144d-113">Remarks</span></span>



| <span data-ttu-id="f144d-114">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="f144d-114">Pixel shader versions</span></span> | <span data-ttu-id="f144d-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="f144d-115">1\_1</span></span> | <span data-ttu-id="f144d-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="f144d-116">1\_2</span></span> | <span data-ttu-id="f144d-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f144d-117">1\_3</span></span> | <span data-ttu-id="f144d-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="f144d-118">1\_4</span></span> | <span data-ttu-id="f144d-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f144d-119">2\_0</span></span> | <span data-ttu-id="f144d-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f144d-120">2\_x</span></span> | <span data-ttu-id="f144d-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f144d-121">2\_sw</span></span> | <span data-ttu-id="f144d-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f144d-122">3\_0</span></span> | <span data-ttu-id="f144d-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f144d-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f144d-124">m3x4</span><span class="sxs-lookup"><span data-stu-id="f144d-124">m3x4</span></span>                  |      |      |      |      | <span data-ttu-id="f144d-125">x</span><span class="sxs-lookup"><span data-stu-id="f144d-125">x</span></span>    | <span data-ttu-id="f144d-126">x</span><span class="sxs-lookup"><span data-stu-id="f144d-126">x</span></span>    | <span data-ttu-id="f144d-127">x</span><span class="sxs-lookup"><span data-stu-id="f144d-127">x</span></span>     | <span data-ttu-id="f144d-128">x</span><span class="sxs-lookup"><span data-stu-id="f144d-128">x</span></span>    | <span data-ttu-id="f144d-129">x</span><span class="sxs-lookup"><span data-stu-id="f144d-129">x</span></span>     |



 

<span data-ttu-id="f144d-130">Die xyzw-Maske (Standard) ist für das Ziel Register erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f144d-130">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="f144d-131">Negate-und Swizzle-Modifizierern sind für src0, aber nicht für Quelle1 zulässig.</span><span class="sxs-lookup"><span data-stu-id="f144d-131">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="f144d-132">Der folgende Code Ausschnitt zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="f144d-132">The following code snippet shows the operations performed.</span></span>


```
 
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z);
```



<span data-ttu-id="f144d-133">Der Eingabe Vektor befindet sich im Register src0.</span><span class="sxs-lookup"><span data-stu-id="f144d-133">The input vector is in register src0.</span></span> <span data-ttu-id="f144d-134">Die rund m3-Eingabe Matrix befindet sich in Register Quelle1 und den nächsten zwei höheren Registern, wie in der folgenden Erweiterung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f144d-134">The input 3x4 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="f144d-135">Dieser Vorgang wird häufig verwendet, um einen Positions Vektor durch eine Matrix zu transformieren, die einen projectiven Effekt hat, aber keine Übersetzung anwendet.</span><span class="sxs-lookup"><span data-stu-id="f144d-135">This operation is commonly used for transforming a position vector by a matrix that has a projective effect but applies no translation.</span></span> <span data-ttu-id="f144d-136">Diese Anweisung wird als Paar von Punkt Produkten implementiert, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f144d-136">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="f144d-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f144d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f144d-138">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="f144d-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




