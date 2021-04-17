---
title: NRM-PS
description: Normalisieren Sie einen 3D-Vektor. | NRM-PS
ms.assetid: 4881037d-3ad1-4afb-b4ad-d615c6b8fe34
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 165f1b8fa6adce4ffba079eff025ed1a3d8ce61e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352859"
---
# <a name="nrm---ps"></a><span data-ttu-id="af5e8-104">NRM-PS</span><span class="sxs-lookup"><span data-stu-id="af5e8-104">nrm - ps</span></span>

<span data-ttu-id="af5e8-105">Normalisieren Sie einen 3D-Vektor.</span><span class="sxs-lookup"><span data-stu-id="af5e8-105">Normalize a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="af5e8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="af5e8-106">Syntax</span></span>



| <span data-ttu-id="af5e8-107">NRM DST, src</span><span class="sxs-lookup"><span data-stu-id="af5e8-107">nrm dst, src</span></span> |
|--------------|



 

<span data-ttu-id="af5e8-108">where</span><span class="sxs-lookup"><span data-stu-id="af5e8-108">where</span></span>

-   <span data-ttu-id="af5e8-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="af5e8-109">dst is the destination register.</span></span>
-   <span data-ttu-id="af5e8-110">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="af5e8-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="af5e8-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af5e8-111">Remarks</span></span>



| <span data-ttu-id="af5e8-112">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="af5e8-112">Pixel shader versions</span></span> | <span data-ttu-id="af5e8-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="af5e8-113">1\_1</span></span> | <span data-ttu-id="af5e8-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="af5e8-114">1\_2</span></span> | <span data-ttu-id="af5e8-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="af5e8-115">1\_3</span></span> | <span data-ttu-id="af5e8-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="af5e8-116">1\_4</span></span> | <span data-ttu-id="af5e8-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="af5e8-117">2\_0</span></span> | <span data-ttu-id="af5e8-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="af5e8-118">2\_x</span></span> | <span data-ttu-id="af5e8-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="af5e8-119">2\_sw</span></span> | <span data-ttu-id="af5e8-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="af5e8-120">3\_0</span></span> | <span data-ttu-id="af5e8-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="af5e8-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="af5e8-122">NRM</span><span class="sxs-lookup"><span data-stu-id="af5e8-122">nrm</span></span>                   |      |      |      |      | <span data-ttu-id="af5e8-123">x</span><span class="sxs-lookup"><span data-stu-id="af5e8-123">x</span></span>    | <span data-ttu-id="af5e8-124">x</span><span class="sxs-lookup"><span data-stu-id="af5e8-124">x</span></span>    | <span data-ttu-id="af5e8-125">x</span><span class="sxs-lookup"><span data-stu-id="af5e8-125">x</span></span>     | <span data-ttu-id="af5e8-126">x</span><span class="sxs-lookup"><span data-stu-id="af5e8-126">x</span></span>    | <span data-ttu-id="af5e8-127">x</span><span class="sxs-lookup"><span data-stu-id="af5e8-127">x</span></span>     |



 

<span data-ttu-id="af5e8-128">Diese Anweisung funktioniert konzeptionell, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="af5e8-128">This instruction works conceptually as shown here.</span></span>

<span data-ttu-id="af5e8-129">squarerootof thesum = (src0. x \* src0. x + src0. y \* src0. y + src0. z \* src0. z)<sup>1/2</sup>;</span><span class="sxs-lookup"><span data-stu-id="af5e8-129">squareRootOfTheSum = (src0.x\*src0.x + src0.y\*src0.y + src0.z\*src0.z)<sup>1/2</sup>;</span></span>


```
dest.x = src0.x * (1 / squareRootOfTheSum);
dest.y = src0.y * (1 / squareRootOfTheSum);
dest.z = src0.z * (1 / squareRootOfTheSum);
dest.w = src0.w * (1 / squareRootOfTheSum);
```



<span data-ttu-id="af5e8-130">Die Register "dest" und "src" dürfen nicht identisch sein.</span><span class="sxs-lookup"><span data-stu-id="af5e8-130">The dest and src registers cannot be the same.</span></span> <span data-ttu-id="af5e8-131">Das dest-Register muss ein temporäres Register sein.</span><span class="sxs-lookup"><span data-stu-id="af5e8-131">The dest register must be a temporary register.</span></span>

<span data-ttu-id="af5e8-132">Diese Anweisung führt die lineare interpolung basierend auf der folgenden Formel aus.</span><span class="sxs-lookup"><span data-stu-id="af5e8-132">This instruction performs the linear interpolation based on the following formula.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="af5e8-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="af5e8-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af5e8-134">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="af5e8-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




