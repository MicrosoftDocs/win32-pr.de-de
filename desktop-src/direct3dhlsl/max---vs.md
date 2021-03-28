---
title: Max-vs
description: Berechnet das Maximum der Quellen. | Max-vs
ms.assetid: 93fb8fb2-c722-43e5-bfe4-a2e9d3cd2049
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 923da795210fe2be62a6dd84a53f0127fef21077
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981745"
---
# <a name="max---vs"></a><span data-ttu-id="0871a-104">Max-vs</span><span class="sxs-lookup"><span data-stu-id="0871a-104">max - vs</span></span>

<span data-ttu-id="0871a-105">Berechnet das Maximum der Quellen.</span><span class="sxs-lookup"><span data-stu-id="0871a-105">Calculates the maximum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="0871a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0871a-106">Syntax</span></span>



| <span data-ttu-id="0871a-107">Max. DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="0871a-107">max dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="0871a-108">where</span><span class="sxs-lookup"><span data-stu-id="0871a-108">where</span></span>

-   <span data-ttu-id="0871a-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="0871a-109">dst is the destination register.</span></span>
-   <span data-ttu-id="0871a-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="0871a-110">src0 is a source register.</span></span>
-   <span data-ttu-id="0871a-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="0871a-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="0871a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0871a-112">Remarks</span></span>



| <span data-ttu-id="0871a-113">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="0871a-113">Vertex shader versions</span></span> | <span data-ttu-id="0871a-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="0871a-114">1\_1</span></span> | <span data-ttu-id="0871a-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0871a-115">2\_0</span></span> | <span data-ttu-id="0871a-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0871a-116">2\_x</span></span> | <span data-ttu-id="0871a-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0871a-117">2\_sw</span></span> | <span data-ttu-id="0871a-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0871a-118">3\_0</span></span> | <span data-ttu-id="0871a-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0871a-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="0871a-120">max</span><span class="sxs-lookup"><span data-stu-id="0871a-120">max</span></span>                    | <span data-ttu-id="0871a-121">x</span><span class="sxs-lookup"><span data-stu-id="0871a-121">x</span></span>    | <span data-ttu-id="0871a-122">x</span><span class="sxs-lookup"><span data-stu-id="0871a-122">x</span></span>    | <span data-ttu-id="0871a-123">x</span><span class="sxs-lookup"><span data-stu-id="0871a-123">x</span></span>    | <span data-ttu-id="0871a-124">x</span><span class="sxs-lookup"><span data-stu-id="0871a-124">x</span></span>     | <span data-ttu-id="0871a-125">x</span><span class="sxs-lookup"><span data-stu-id="0871a-125">x</span></span>    | <span data-ttu-id="0871a-126">x</span><span class="sxs-lookup"><span data-stu-id="0871a-126">x</span></span>     |



 

<span data-ttu-id="0871a-127">Das folgende Code Fragment zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="0871a-127">The following code fragment shows the operations performed.</span></span>


```
dest.x=(src0.x >= src1.x) ? src0.x : src1.x;
dest.y=(src0.y >= src1.y) ? src0.y : src1.y;
dest.z=(src0.z >= src1.z) ? src0.z : src1.z;
dest.w=(src0.w >= src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="0871a-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0871a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0871a-129">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="0871a-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




