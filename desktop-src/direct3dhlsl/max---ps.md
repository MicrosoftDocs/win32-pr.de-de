---
title: Max-PS
description: Berechnet das Maximum der Quellen. | Max-PS
ms.assetid: 3d3bef5b-0ff7-441b-8681-a3f4cde0ae4f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c6186f0bd57acd4862a62a4c0a30ae92118b75ce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982071"
---
# <a name="max---ps"></a><span data-ttu-id="5027c-104">Max-PS</span><span class="sxs-lookup"><span data-stu-id="5027c-104">max - ps</span></span>

<span data-ttu-id="5027c-105">Berechnet das Maximum der Quellen.</span><span class="sxs-lookup"><span data-stu-id="5027c-105">Calculates the maximum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="5027c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5027c-106">Syntax</span></span>



| <span data-ttu-id="5027c-107">Max. DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="5027c-107">max dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="5027c-108">where</span><span class="sxs-lookup"><span data-stu-id="5027c-108">where</span></span>

-   <span data-ttu-id="5027c-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="5027c-109">dst is the destination register.</span></span>
-   <span data-ttu-id="5027c-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="5027c-110">src0 is a source register.</span></span>
-   <span data-ttu-id="5027c-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="5027c-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5027c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5027c-112">Remarks</span></span>



| <span data-ttu-id="5027c-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="5027c-113">Pixel shader versions</span></span> | <span data-ttu-id="5027c-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="5027c-114">1\_1</span></span> | <span data-ttu-id="5027c-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="5027c-115">1\_2</span></span> | <span data-ttu-id="5027c-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5027c-116">1\_3</span></span> | <span data-ttu-id="5027c-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="5027c-117">1\_4</span></span> | <span data-ttu-id="5027c-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5027c-118">2\_0</span></span> | <span data-ttu-id="5027c-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5027c-119">2\_x</span></span> | <span data-ttu-id="5027c-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5027c-120">2\_sw</span></span> | <span data-ttu-id="5027c-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5027c-121">3\_0</span></span> | <span data-ttu-id="5027c-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5027c-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5027c-123">max</span><span class="sxs-lookup"><span data-stu-id="5027c-123">max</span></span>                   |      |      |      |      | <span data-ttu-id="5027c-124">x</span><span class="sxs-lookup"><span data-stu-id="5027c-124">x</span></span>    | <span data-ttu-id="5027c-125">x</span><span class="sxs-lookup"><span data-stu-id="5027c-125">x</span></span>    | <span data-ttu-id="5027c-126">x</span><span class="sxs-lookup"><span data-stu-id="5027c-126">x</span></span>     | <span data-ttu-id="5027c-127">x</span><span class="sxs-lookup"><span data-stu-id="5027c-127">x</span></span>    | <span data-ttu-id="5027c-128">x</span><span class="sxs-lookup"><span data-stu-id="5027c-128">x</span></span>     |



 

<span data-ttu-id="5027c-129">Der folgende Code Ausschnitt zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="5027c-129">The following code snippet shows the operations performed.</span></span>


```
dest.x=(src0.x >= src1.x) ? src0.x : src1.x;
dest.y=(src0.y >= src1.y) ? src0.y : src1.y;
dest.z=(src0.z >= src1.z) ? src0.z : src1.z;
dest.w=(src0.w >= src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="5027c-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5027c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5027c-131">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="5027c-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




