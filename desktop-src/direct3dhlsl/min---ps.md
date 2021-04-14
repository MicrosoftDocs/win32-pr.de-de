---
title: min-PS
description: Berechnet den minimalen der Quellen. | min-PS
ms.assetid: 2ee6208d-a353-4747-8037-c21dd1a05016
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3a735b38769a30e9dccf544785d931641469f5dc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981568"
---
# <a name="min---ps"></a><span data-ttu-id="c2f21-104">min-PS</span><span class="sxs-lookup"><span data-stu-id="c2f21-104">min - ps</span></span>

<span data-ttu-id="c2f21-105">Berechnet den minimalen der Quellen.</span><span class="sxs-lookup"><span data-stu-id="c2f21-105">Calculates the minimum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2f21-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2f21-106">Syntax</span></span>



| <span data-ttu-id="c2f21-107">Min. DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="c2f21-107">min dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="c2f21-108">where</span><span class="sxs-lookup"><span data-stu-id="c2f21-108">where</span></span>

-   <span data-ttu-id="c2f21-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="c2f21-109">dst is the destination register.</span></span>
-   <span data-ttu-id="c2f21-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="c2f21-110">src0 is a source register.</span></span>
-   <span data-ttu-id="c2f21-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="c2f21-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2f21-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2f21-112">Remarks</span></span>



| <span data-ttu-id="c2f21-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="c2f21-113">Pixel shader versions</span></span> | <span data-ttu-id="c2f21-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="c2f21-114">1\_1</span></span> | <span data-ttu-id="c2f21-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="c2f21-115">1\_2</span></span> | <span data-ttu-id="c2f21-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c2f21-116">1\_3</span></span> | <span data-ttu-id="c2f21-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="c2f21-117">1\_4</span></span> | <span data-ttu-id="c2f21-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c2f21-118">2\_0</span></span> | <span data-ttu-id="c2f21-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c2f21-119">2\_x</span></span> | <span data-ttu-id="c2f21-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c2f21-120">2\_sw</span></span> | <span data-ttu-id="c2f21-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c2f21-121">3\_0</span></span> | <span data-ttu-id="c2f21-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c2f21-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c2f21-123">Min</span><span class="sxs-lookup"><span data-stu-id="c2f21-123">min</span></span>                   |      |      |      |      | <span data-ttu-id="c2f21-124">x</span><span class="sxs-lookup"><span data-stu-id="c2f21-124">x</span></span>    | <span data-ttu-id="c2f21-125">x</span><span class="sxs-lookup"><span data-stu-id="c2f21-125">x</span></span>    | <span data-ttu-id="c2f21-126">x</span><span class="sxs-lookup"><span data-stu-id="c2f21-126">x</span></span>     | <span data-ttu-id="c2f21-127">x</span><span class="sxs-lookup"><span data-stu-id="c2f21-127">x</span></span>    | <span data-ttu-id="c2f21-128">x</span><span class="sxs-lookup"><span data-stu-id="c2f21-128">x</span></span>     |



 

<span data-ttu-id="c2f21-129">Der folgende Code Ausschnitt zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="c2f21-129">The following code snippet shows the operations performed.</span></span>


```
dest.x=(src0.x < src1.x) ? src0.x : src1.x;
dest.y=(src0.y < src1.y) ? src0.y : src1.y;
dest.z=(src0.z < src1.z) ? src0.z : src1.z;
dest.w=(src0.w < src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="c2f21-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c2f21-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2f21-131">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="c2f21-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




