---
title: DST-vs
description: Berechnet einen Entfernungs Vektor. | DST-vs
ms.assetid: 4315a29f-58e7-427f-aaa0-1fe1a81eb392
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e41c1da0eae001d314e2682a3295a0b88b993ee1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869727"
---
# <a name="dst---vs"></a><span data-ttu-id="e7cd6-104">DST-vs</span><span class="sxs-lookup"><span data-stu-id="e7cd6-104">dst - vs</span></span>

<span data-ttu-id="e7cd6-105">Berechnet einen Entfernungs Vektor.</span><span class="sxs-lookup"><span data-stu-id="e7cd6-105">Calculates a distance vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7cd6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7cd6-106">Syntax</span></span>



| <span data-ttu-id="e7cd6-107">DST dest, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="e7cd6-107">dst dest, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="e7cd6-108">where</span><span class="sxs-lookup"><span data-stu-id="e7cd6-108">where</span></span>

-   <span data-ttu-id="e7cd6-109">dest ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="e7cd6-109">dest is the destination register.</span></span>
-   <span data-ttu-id="e7cd6-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="e7cd6-110">src0 is a source register.</span></span>
-   <span data-ttu-id="e7cd6-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="e7cd6-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7cd6-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7cd6-112">Remarks</span></span>



| <span data-ttu-id="e7cd6-113">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="e7cd6-113">Vertex shader versions</span></span> | <span data-ttu-id="e7cd6-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="e7cd6-114">1\_1</span></span> | <span data-ttu-id="e7cd6-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e7cd6-115">2\_0</span></span> | <span data-ttu-id="e7cd6-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e7cd6-116">2\_x</span></span> | <span data-ttu-id="e7cd6-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e7cd6-117">2\_sw</span></span> | <span data-ttu-id="e7cd6-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e7cd6-118">3\_0</span></span> | <span data-ttu-id="e7cd6-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e7cd6-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="e7cd6-120">DST</span><span class="sxs-lookup"><span data-stu-id="e7cd6-120">dst</span></span>                    | <span data-ttu-id="e7cd6-121">x</span><span class="sxs-lookup"><span data-stu-id="e7cd6-121">x</span></span>    | <span data-ttu-id="e7cd6-122">x</span><span class="sxs-lookup"><span data-stu-id="e7cd6-122">x</span></span>    | <span data-ttu-id="e7cd6-123">x</span><span class="sxs-lookup"><span data-stu-id="e7cd6-123">x</span></span>    | <span data-ttu-id="e7cd6-124">x</span><span class="sxs-lookup"><span data-stu-id="e7cd6-124">x</span></span>     | <span data-ttu-id="e7cd6-125">x</span><span class="sxs-lookup"><span data-stu-id="e7cd6-125">x</span></span>    | <span data-ttu-id="e7cd6-126">x</span><span class="sxs-lookup"><span data-stu-id="e7cd6-126">x</span></span>     |



 

<span data-ttu-id="e7cd6-127">Das folgende Code Fragment zeigt die Vorgänge, die ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="e7cd6-127">The following code fragment shows the operations performed:</span></span>


```
dest.x = 1;
dest.y = src0.y * src1.y;
dest.z = src0.z;
dest.w = src1.w;
```



<span data-ttu-id="e7cd6-128">Der erste Quell Operand (src0) wird als Vektor angenommen (ignoriert, d \* d, d, \* ignoriert), und der zweite Quell Operand (Quelle1) wird als Vektor angenommen (ignoriert, 1/d, ignoriert, 1/d).</span><span class="sxs-lookup"><span data-stu-id="e7cd6-128">The first source operand (src0) is assumed to be the vector (ignored, d\*d, d\*d, ignored) and the second source operand (src1) is assumed to be the vector (ignored, 1/d, ignored, 1/d).</span></span> <span data-ttu-id="e7cd6-129">Das Ziel (dest) ist der Ergebnis Vektor (1, d, d \* d, 1/d).</span><span class="sxs-lookup"><span data-stu-id="e7cd6-129">The destination (dest) is the result vector (1, d, d\*d, 1/d).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7cd6-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e7cd6-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7cd6-131">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="e7cd6-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




