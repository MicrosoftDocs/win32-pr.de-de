---
title: Sub-vs
description: Subtrahiert Quellen. | Sub-vs
ms.assetid: ccd7ca57-05a9-4ee8-8bda-c8c875476aaf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a4bf15522798e1da5ec0bde5b729f241ff9dabde
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961423"
---
# <a name="sub---vs"></a><span data-ttu-id="5654e-104">Sub-vs</span><span class="sxs-lookup"><span data-stu-id="5654e-104">sub - vs</span></span>

<span data-ttu-id="5654e-105">Subtrahiert Quellen.</span><span class="sxs-lookup"><span data-stu-id="5654e-105">Subtracts sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="5654e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5654e-106">Syntax</span></span>



| <span data-ttu-id="5654e-107">Sub DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="5654e-107">sub dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="5654e-108">where</span><span class="sxs-lookup"><span data-stu-id="5654e-108">where</span></span>

-   <span data-ttu-id="5654e-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="5654e-109">dst is the destination register.</span></span>
-   <span data-ttu-id="5654e-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="5654e-110">src0 is a source register.</span></span>
-   <span data-ttu-id="5654e-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="5654e-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5654e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5654e-112">Remarks</span></span>



| <span data-ttu-id="5654e-113">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="5654e-113">Vertex shader versions</span></span> | <span data-ttu-id="5654e-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="5654e-114">1\_1</span></span> | <span data-ttu-id="5654e-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5654e-115">2\_0</span></span> | <span data-ttu-id="5654e-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5654e-116">2\_x</span></span> | <span data-ttu-id="5654e-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5654e-117">2\_sw</span></span> | <span data-ttu-id="5654e-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5654e-118">3\_0</span></span> | <span data-ttu-id="5654e-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5654e-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5654e-120">sub</span><span class="sxs-lookup"><span data-stu-id="5654e-120">sub</span></span>                    | <span data-ttu-id="5654e-121">x</span><span class="sxs-lookup"><span data-stu-id="5654e-121">x</span></span>    | <span data-ttu-id="5654e-122">x</span><span class="sxs-lookup"><span data-stu-id="5654e-122">x</span></span>    | <span data-ttu-id="5654e-123">x</span><span class="sxs-lookup"><span data-stu-id="5654e-123">x</span></span>    | <span data-ttu-id="5654e-124">x</span><span class="sxs-lookup"><span data-stu-id="5654e-124">x</span></span>     | <span data-ttu-id="5654e-125">x</span><span class="sxs-lookup"><span data-stu-id="5654e-125">x</span></span>    | <span data-ttu-id="5654e-126">x</span><span class="sxs-lookup"><span data-stu-id="5654e-126">x</span></span>     |



 

<span data-ttu-id="5654e-127">Diese Anweisung führt die Subtraktion aus, die in dieser Formel angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5654e-127">This instruction performs the subtraction shown in this formula.</span></span>


```
dest.x = src0.x - src1.x
dest.y = src0.y - src1.y
dest.z = src0.z - src1.z
dest.w = src0.w - src1.w
```



## <a name="related-topics"></a><span data-ttu-id="5654e-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5654e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5654e-129">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="5654e-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




