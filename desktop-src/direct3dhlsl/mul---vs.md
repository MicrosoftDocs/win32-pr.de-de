---
title: Mul-vs
description: Multipliziert Quellen mit dem Ziel. | Mul-vs
ms.assetid: 0b048cc2-b165-418f-893e-6dee28ca5ad3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e33ac35831b19f771f4f5b64d94bcc47c6657db5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995486"
---
# <a name="mul---vs"></a><span data-ttu-id="0e444-104">Mul-vs</span><span class="sxs-lookup"><span data-stu-id="0e444-104">mul - vs</span></span>

<span data-ttu-id="0e444-105">Multipliziert Quellen mit dem Ziel.</span><span class="sxs-lookup"><span data-stu-id="0e444-105">Multiplies sources into the destination.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e444-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e444-106">Syntax</span></span>



| <span data-ttu-id="0e444-107">Mul DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="0e444-107">mul dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="0e444-108">where</span><span class="sxs-lookup"><span data-stu-id="0e444-108">where</span></span>

-   <span data-ttu-id="0e444-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="0e444-109">dst is the destination register.</span></span>
-   <span data-ttu-id="0e444-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="0e444-110">src0 is a source register.</span></span>
-   <span data-ttu-id="0e444-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="0e444-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e444-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e444-112">Remarks</span></span>



| <span data-ttu-id="0e444-113">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="0e444-113">Vertex shader versions</span></span> | <span data-ttu-id="0e444-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="0e444-114">1\_1</span></span> | <span data-ttu-id="0e444-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0e444-115">2\_0</span></span> | <span data-ttu-id="0e444-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0e444-116">2\_x</span></span> | <span data-ttu-id="0e444-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0e444-117">2\_sw</span></span> | <span data-ttu-id="0e444-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0e444-118">3\_0</span></span> | <span data-ttu-id="0e444-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0e444-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="0e444-120">mul</span><span class="sxs-lookup"><span data-stu-id="0e444-120">mul</span></span>                    | <span data-ttu-id="0e444-121">x</span><span class="sxs-lookup"><span data-stu-id="0e444-121">x</span></span>    | <span data-ttu-id="0e444-122">x</span><span class="sxs-lookup"><span data-stu-id="0e444-122">x</span></span>    | <span data-ttu-id="0e444-123">x</span><span class="sxs-lookup"><span data-stu-id="0e444-123">x</span></span>    | <span data-ttu-id="0e444-124">x</span><span class="sxs-lookup"><span data-stu-id="0e444-124">x</span></span>     | <span data-ttu-id="0e444-125">x</span><span class="sxs-lookup"><span data-stu-id="0e444-125">x</span></span>    | <span data-ttu-id="0e444-126">x</span><span class="sxs-lookup"><span data-stu-id="0e444-126">x</span></span>     |



 

<span data-ttu-id="0e444-127">Das folgende Code Fragment zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="0e444-127">The following code fragment shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x;
dest.y = src0.y * src1.y;
dest.z = src0.z * src1.z;
dest.w = src0.w * src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="0e444-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0e444-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e444-129">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="0e444-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




