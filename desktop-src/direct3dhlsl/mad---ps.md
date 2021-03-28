---
title: Mad-PS
description: Multiplizieren und Hinzufügen von Anweisungen. Legt das Ziel Register auf (src0 \ Quelle1) + Quelle2 fest.
ms.assetid: 0bcf5dcc-3657-4ee0-9aeb-bd2d8feea7a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3570f5826f91b35b07478e1ea34940a27d706cf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389554"
---
# <a name="mad---ps"></a><span data-ttu-id="e83ea-104">Mad-PS</span><span class="sxs-lookup"><span data-stu-id="e83ea-104">mad - ps</span></span>

<span data-ttu-id="e83ea-105">Multiplizieren und Hinzufügen von Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="e83ea-105">Multiply and add instruction.</span></span> <span data-ttu-id="e83ea-106">Legt das Ziel Register auf (src0 \* Quelle1) + Quelle2 fest.</span><span class="sxs-lookup"><span data-stu-id="e83ea-106">Sets the destination register to (src0 \* src1) + src2.</span></span>

## <a name="syntax"></a><span data-ttu-id="e83ea-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e83ea-107">Syntax</span></span>



| <span data-ttu-id="e83ea-108">Mad DST, src0, Quelle1, Quelle2</span><span class="sxs-lookup"><span data-stu-id="e83ea-108">mad dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="e83ea-109">where</span><span class="sxs-lookup"><span data-stu-id="e83ea-109">where</span></span>

-   <span data-ttu-id="e83ea-110">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="e83ea-110">dst is the destination register.</span></span>
-   <span data-ttu-id="e83ea-111">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="e83ea-111">src0 is a source register.</span></span>
-   <span data-ttu-id="e83ea-112">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="e83ea-112">src1 is a source register.</span></span>
-   <span data-ttu-id="e83ea-113">Quelle2 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="e83ea-113">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e83ea-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e83ea-114">Remarks</span></span>



| <span data-ttu-id="e83ea-115">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="e83ea-115">Pixel shader versions</span></span> | <span data-ttu-id="e83ea-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="e83ea-116">1\_1</span></span> | <span data-ttu-id="e83ea-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="e83ea-117">1\_2</span></span> | <span data-ttu-id="e83ea-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e83ea-118">1\_3</span></span> | <span data-ttu-id="e83ea-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="e83ea-119">1\_4</span></span> | <span data-ttu-id="e83ea-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e83ea-120">2\_0</span></span> | <span data-ttu-id="e83ea-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e83ea-121">2\_x</span></span> | <span data-ttu-id="e83ea-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e83ea-122">2\_sw</span></span> | <span data-ttu-id="e83ea-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e83ea-123">3\_0</span></span> | <span data-ttu-id="e83ea-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e83ea-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e83ea-125">geworden</span><span class="sxs-lookup"><span data-stu-id="e83ea-125">mad</span></span>                   | <span data-ttu-id="e83ea-126">x</span><span class="sxs-lookup"><span data-stu-id="e83ea-126">x</span></span>    | <span data-ttu-id="e83ea-127">x</span><span class="sxs-lookup"><span data-stu-id="e83ea-127">x</span></span>    | <span data-ttu-id="e83ea-128">x</span><span class="sxs-lookup"><span data-stu-id="e83ea-128">x</span></span>    | <span data-ttu-id="e83ea-129">x</span><span class="sxs-lookup"><span data-stu-id="e83ea-129">x</span></span>    | <span data-ttu-id="e83ea-130">x</span><span class="sxs-lookup"><span data-stu-id="e83ea-130">x</span></span>    | <span data-ttu-id="e83ea-131">x</span><span class="sxs-lookup"><span data-stu-id="e83ea-131">x</span></span>    | <span data-ttu-id="e83ea-132">x</span><span class="sxs-lookup"><span data-stu-id="e83ea-132">x</span></span>     | <span data-ttu-id="e83ea-133">x</span><span class="sxs-lookup"><span data-stu-id="e83ea-133">x</span></span>    | <span data-ttu-id="e83ea-134">x</span><span class="sxs-lookup"><span data-stu-id="e83ea-134">x</span></span>     |



 

<span data-ttu-id="e83ea-135">Der folgende Code Ausschnitt zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="e83ea-135">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x + src2.x;
dest.y = src0.y * src1.y + src2.y;
dest.z = src0.z * src1.z + src2.z;
dest.w = src0.w * src1.w + src2.w;
```



## <a name="related-topics"></a><span data-ttu-id="e83ea-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e83ea-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e83ea-137">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="e83ea-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




