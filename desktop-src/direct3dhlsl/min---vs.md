---
title: min-vs
description: Berechnet den minimalen der Quellen. | min-vs
ms.assetid: cecfe98b-8efd-4fbf-a7b5-d228de724e71
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eda47b75398b8643f7010ff7468f72f4a7d8c199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981776"
---
# <a name="min---vs"></a><span data-ttu-id="d8597-104">min-vs</span><span class="sxs-lookup"><span data-stu-id="d8597-104">min - vs</span></span>

<span data-ttu-id="d8597-105">Berechnet den minimalen der Quellen.</span><span class="sxs-lookup"><span data-stu-id="d8597-105">Calculates the minimum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8597-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8597-106">Syntax</span></span>



| <span data-ttu-id="d8597-107">Min. DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="d8597-107">min dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="d8597-108">where</span><span class="sxs-lookup"><span data-stu-id="d8597-108">where</span></span>

-   <span data-ttu-id="d8597-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="d8597-109">dst is the destination register.</span></span>
-   <span data-ttu-id="d8597-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="d8597-110">src0 is a source register.</span></span>
-   <span data-ttu-id="d8597-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="d8597-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8597-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8597-112">Remarks</span></span>



| <span data-ttu-id="d8597-113">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="d8597-113">Vertex shader versions</span></span> | <span data-ttu-id="d8597-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="d8597-114">1\_1</span></span> | <span data-ttu-id="d8597-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d8597-115">2\_0</span></span> | <span data-ttu-id="d8597-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d8597-116">2\_x</span></span> | <span data-ttu-id="d8597-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d8597-117">2\_sw</span></span> | <span data-ttu-id="d8597-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d8597-118">3\_0</span></span> | <span data-ttu-id="d8597-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d8597-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="d8597-120">Min</span><span class="sxs-lookup"><span data-stu-id="d8597-120">min</span></span>                    | <span data-ttu-id="d8597-121">x</span><span class="sxs-lookup"><span data-stu-id="d8597-121">x</span></span>    | <span data-ttu-id="d8597-122">x</span><span class="sxs-lookup"><span data-stu-id="d8597-122">x</span></span>    | <span data-ttu-id="d8597-123">x</span><span class="sxs-lookup"><span data-stu-id="d8597-123">x</span></span>    | <span data-ttu-id="d8597-124">x</span><span class="sxs-lookup"><span data-stu-id="d8597-124">x</span></span>     | <span data-ttu-id="d8597-125">x</span><span class="sxs-lookup"><span data-stu-id="d8597-125">x</span></span>    | <span data-ttu-id="d8597-126">x</span><span class="sxs-lookup"><span data-stu-id="d8597-126">x</span></span>     |



 

<span data-ttu-id="d8597-127">Das folgende Code Fragment zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="d8597-127">The following code fragment shows the operations performed.</span></span>


```
dest.x=(src0.x < src1.x) ? src0.x : src1.x;
dest.y=(src0.y < src1.y) ? src0.y : src1.y;
dest.z=(src0.z < src1.z) ? src0.z : src1.z;
dest.w=(src0.w < src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="d8597-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8597-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8597-129">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="d8597-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




