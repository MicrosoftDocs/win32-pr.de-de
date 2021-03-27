---
title: LRP-PS
description: Interpoliert linear zwischen dem zweiten und dritten Quell Register durch einen im ersten Quell Register angegebenen Anteil. | LRP-PS
ms.assetid: b360f28e-cb2a-4403-a020-180524df6549
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aec1ac23cc6c86f768d435e4c8169117c1bbe899
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050816"
---
# <a name="lrp---ps"></a><span data-ttu-id="fe76f-104">LRP-PS</span><span class="sxs-lookup"><span data-stu-id="fe76f-104">lrp - ps</span></span>

<span data-ttu-id="fe76f-105">Interpoliert linear zwischen dem zweiten und dritten Quell Register durch einen im ersten Quell Register angegebenen Anteil.</span><span class="sxs-lookup"><span data-stu-id="fe76f-105">Interpolates linearly between the second and third source registers by a proportion specified in the first source register.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe76f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe76f-106">Syntax</span></span>



| <span data-ttu-id="fe76f-107">LRP DST, src0, Quelle1, Quelle2</span><span class="sxs-lookup"><span data-stu-id="fe76f-107">lrp dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="fe76f-108">where</span><span class="sxs-lookup"><span data-stu-id="fe76f-108">where</span></span>

-   <span data-ttu-id="fe76f-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="fe76f-109">dst is the destination register.</span></span>
-   <span data-ttu-id="fe76f-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="fe76f-110">src0 is a source register.</span></span>
-   <span data-ttu-id="fe76f-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="fe76f-111">src1 is a source register.</span></span>
-   <span data-ttu-id="fe76f-112">Quelle2 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="fe76f-112">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe76f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe76f-113">Remarks</span></span>



| <span data-ttu-id="fe76f-114">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="fe76f-114">Pixel shader versions</span></span> | <span data-ttu-id="fe76f-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="fe76f-115">1\_1</span></span> | <span data-ttu-id="fe76f-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="fe76f-116">1\_2</span></span> | <span data-ttu-id="fe76f-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="fe76f-117">1\_3</span></span> | <span data-ttu-id="fe76f-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="fe76f-118">1\_4</span></span> | <span data-ttu-id="fe76f-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fe76f-119">2\_0</span></span> | <span data-ttu-id="fe76f-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fe76f-120">2\_x</span></span> | <span data-ttu-id="fe76f-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="fe76f-121">2\_sw</span></span> | <span data-ttu-id="fe76f-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fe76f-122">3\_0</span></span> | <span data-ttu-id="fe76f-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="fe76f-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="fe76f-124">startet</span><span class="sxs-lookup"><span data-stu-id="fe76f-124">lrp</span></span>                   | <span data-ttu-id="fe76f-125">x</span><span class="sxs-lookup"><span data-stu-id="fe76f-125">x</span></span>    | <span data-ttu-id="fe76f-126">x</span><span class="sxs-lookup"><span data-stu-id="fe76f-126">x</span></span>    | <span data-ttu-id="fe76f-127">x</span><span class="sxs-lookup"><span data-stu-id="fe76f-127">x</span></span>    | <span data-ttu-id="fe76f-128">x</span><span class="sxs-lookup"><span data-stu-id="fe76f-128">x</span></span>    | <span data-ttu-id="fe76f-129">x</span><span class="sxs-lookup"><span data-stu-id="fe76f-129">x</span></span>    | <span data-ttu-id="fe76f-130">x</span><span class="sxs-lookup"><span data-stu-id="fe76f-130">x</span></span>    | <span data-ttu-id="fe76f-131">x</span><span class="sxs-lookup"><span data-stu-id="fe76f-131">x</span></span>     | <span data-ttu-id="fe76f-132">x</span><span class="sxs-lookup"><span data-stu-id="fe76f-132">x</span></span>    | <span data-ttu-id="fe76f-133">x</span><span class="sxs-lookup"><span data-stu-id="fe76f-133">x</span></span>     |



 

<span data-ttu-id="fe76f-134">Diese Anweisung führt die lineare interpolung basierend auf der folgenden Formel aus.</span><span class="sxs-lookup"><span data-stu-id="fe76f-134">This instruction performs the linear interpolation based on the following formula.</span></span>


```
 
dest = src0 * src1 + (1-src0) * src2
// which is the same as
dest = src2 + src0 * (src1 - src2)
```



## <a name="related-topics"></a><span data-ttu-id="fe76f-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe76f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe76f-136">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="fe76f-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




