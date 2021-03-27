---
title: NRM-vs
description: Normalisieren Sie einen 3D-Vektor. | NRM-vs
ms.assetid: 735e9971-c0c3-4648-8362-58bda6fac46a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e696277136826294392149c4b7430e4c75f9d9a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219256"
---
# <a name="nrm---vs"></a><span data-ttu-id="14b2f-104">NRM-vs</span><span class="sxs-lookup"><span data-stu-id="14b2f-104">nrm - vs</span></span>

<span data-ttu-id="14b2f-105">Normalisieren Sie einen 3D-Vektor.</span><span class="sxs-lookup"><span data-stu-id="14b2f-105">Normalize a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="14b2f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="14b2f-106">Syntax</span></span>



| <span data-ttu-id="14b2f-107">NRM DST, src</span><span class="sxs-lookup"><span data-stu-id="14b2f-107">nrm dst, src</span></span> |
|--------------|



 

<span data-ttu-id="14b2f-108">where</span><span class="sxs-lookup"><span data-stu-id="14b2f-108">where</span></span>

-   <span data-ttu-id="14b2f-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="14b2f-109">dst is the destination register.</span></span>
-   <span data-ttu-id="14b2f-110">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="14b2f-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="14b2f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14b2f-111">Remarks</span></span>



| <span data-ttu-id="14b2f-112">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="14b2f-112">Vertex shader versions</span></span> | <span data-ttu-id="14b2f-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="14b2f-113">1\_1</span></span> | <span data-ttu-id="14b2f-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="14b2f-114">2\_0</span></span> | <span data-ttu-id="14b2f-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="14b2f-115">2\_x</span></span> | <span data-ttu-id="14b2f-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="14b2f-116">2\_sw</span></span> | <span data-ttu-id="14b2f-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="14b2f-117">3\_0</span></span> | <span data-ttu-id="14b2f-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="14b2f-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="14b2f-119">NRM</span><span class="sxs-lookup"><span data-stu-id="14b2f-119">nrm</span></span>                    |      | <span data-ttu-id="14b2f-120">x</span><span class="sxs-lookup"><span data-stu-id="14b2f-120">x</span></span>    | <span data-ttu-id="14b2f-121">x</span><span class="sxs-lookup"><span data-stu-id="14b2f-121">x</span></span>    | <span data-ttu-id="14b2f-122">x</span><span class="sxs-lookup"><span data-stu-id="14b2f-122">x</span></span>     | <span data-ttu-id="14b2f-123">x</span><span class="sxs-lookup"><span data-stu-id="14b2f-123">x</span></span>    | <span data-ttu-id="14b2f-124">x</span><span class="sxs-lookup"><span data-stu-id="14b2f-124">x</span></span>     |



 

<span data-ttu-id="14b2f-125">Diese Anweisung funktioniert konzeptionell, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="14b2f-125">This instruction works conceptually as shown here.</span></span>

<span data-ttu-id="14b2f-126">squarerootof thesum = (src0. x \* src0. x + src0. y \* src0. y + src0. z \* src0. z)<sup>1/2</sup>;</span><span class="sxs-lookup"><span data-stu-id="14b2f-126">squareRootOfTheSum = (src0.x\*src0.x + src0.y\*src0.y + src0.z\*src0.z)<sup>1/2</sup>;</span></span>


```
dest.x = src0.x * (1 / squareRootOfTheSum);
dest.y = src0.y * (1 / squareRootOfTheSum);
dest.z = src0.z * (1 / squareRootOfTheSum);
dest.w = src0.w * (1 / squareRootOfTheSum);
```



<span data-ttu-id="14b2f-127">Die Register "dest" und "src" dürfen nicht identisch sein.</span><span class="sxs-lookup"><span data-stu-id="14b2f-127">The dest and src registers cannot be the same.</span></span> <span data-ttu-id="14b2f-128">Das dest-Register muss ein temporäres Register sein.</span><span class="sxs-lookup"><span data-stu-id="14b2f-128">The dest register must be a temporary register.</span></span>

<span data-ttu-id="14b2f-129">Diese Anweisung führt die lineare interpolung basierend auf der folgenden Formel aus.</span><span class="sxs-lookup"><span data-stu-id="14b2f-129">This instruction performs the linear interpolation based on the following formula.</span></span>


```
float f = src0.x*src0.x + src0.y*src0.y + src0.z*src0.z;
if (f != 0)
    f = (float)(1/sqrt(f));
else
    f = FLT_MAX;

dest.x = src0.x*f;
dest.y = src0.y*f;
dest.z = src0.z*f;
dest.w = src0.w*f;
```



## <a name="related-topics"></a><span data-ttu-id="14b2f-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="14b2f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14b2f-131">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="14b2f-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




