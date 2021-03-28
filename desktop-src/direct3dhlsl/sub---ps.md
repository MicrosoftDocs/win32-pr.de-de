---
title: Sub-PS
description: Subtrahiert Quellen. | Sub-PS
ms.assetid: e130724f-63bf-4d7f-bc9f-6a4441a788b8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4998892aa06eff55632600a9c2f7fe359c11f830
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761607"
---
# <a name="sub---ps"></a><span data-ttu-id="47cc7-104">Sub-PS</span><span class="sxs-lookup"><span data-stu-id="47cc7-104">sub - ps</span></span>

<span data-ttu-id="47cc7-105">Subtrahiert Quellen.</span><span class="sxs-lookup"><span data-stu-id="47cc7-105">Subtracts sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="47cc7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="47cc7-106">Syntax</span></span>



| <span data-ttu-id="47cc7-107">Sub DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="47cc7-107">sub dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="47cc7-108">where</span><span class="sxs-lookup"><span data-stu-id="47cc7-108">where</span></span>

-   <span data-ttu-id="47cc7-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="47cc7-109">dst is the destination register.</span></span>
-   <span data-ttu-id="47cc7-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="47cc7-110">src0 is a source register.</span></span>
-   <span data-ttu-id="47cc7-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="47cc7-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="47cc7-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47cc7-112">Remarks</span></span>



| <span data-ttu-id="47cc7-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="47cc7-113">Pixel shader versions</span></span> | <span data-ttu-id="47cc7-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="47cc7-114">1\_1</span></span> | <span data-ttu-id="47cc7-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="47cc7-115">1\_2</span></span> | <span data-ttu-id="47cc7-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="47cc7-116">1\_3</span></span> | <span data-ttu-id="47cc7-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="47cc7-117">1\_4</span></span> | <span data-ttu-id="47cc7-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="47cc7-118">2\_0</span></span> | <span data-ttu-id="47cc7-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="47cc7-119">2\_x</span></span> | <span data-ttu-id="47cc7-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="47cc7-120">2\_sw</span></span> | <span data-ttu-id="47cc7-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="47cc7-121">3\_0</span></span> | <span data-ttu-id="47cc7-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="47cc7-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="47cc7-123">sub</span><span class="sxs-lookup"><span data-stu-id="47cc7-123">sub</span></span>                   | <span data-ttu-id="47cc7-124">x</span><span class="sxs-lookup"><span data-stu-id="47cc7-124">x</span></span>    | <span data-ttu-id="47cc7-125">x</span><span class="sxs-lookup"><span data-stu-id="47cc7-125">x</span></span>    | <span data-ttu-id="47cc7-126">x</span><span class="sxs-lookup"><span data-stu-id="47cc7-126">x</span></span>    | <span data-ttu-id="47cc7-127">x</span><span class="sxs-lookup"><span data-stu-id="47cc7-127">x</span></span>    | <span data-ttu-id="47cc7-128">x</span><span class="sxs-lookup"><span data-stu-id="47cc7-128">x</span></span>    | <span data-ttu-id="47cc7-129">x</span><span class="sxs-lookup"><span data-stu-id="47cc7-129">x</span></span>    | <span data-ttu-id="47cc7-130">x</span><span class="sxs-lookup"><span data-stu-id="47cc7-130">x</span></span>     | <span data-ttu-id="47cc7-131">x</span><span class="sxs-lookup"><span data-stu-id="47cc7-131">x</span></span>    | <span data-ttu-id="47cc7-132">x</span><span class="sxs-lookup"><span data-stu-id="47cc7-132">x</span></span>     |



 

<span data-ttu-id="47cc7-133">Diese Anweisung führt die Subtraktion aus, die in dieser Formel angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="47cc7-133">This instruction performs the subtraction shown in this formula.</span></span>


```
dest = src0 - src1
```



## <a name="related-topics"></a><span data-ttu-id="47cc7-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47cc7-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47cc7-135">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="47cc7-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




