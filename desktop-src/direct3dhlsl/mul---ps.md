---
title: Mul-PS
description: Multipliziert Quellen mit dem Ziel. | Mul-PS
ms.assetid: 03823c10-9631-4468-8488-4bd17224d16c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fefe89d4fdbe5f75965f2707a5ceb2c1673e1326
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995716"
---
# <a name="mul---ps"></a><span data-ttu-id="20f13-104">Mul-PS</span><span class="sxs-lookup"><span data-stu-id="20f13-104">mul - ps</span></span>

<span data-ttu-id="20f13-105">Multipliziert Quellen mit dem Ziel.</span><span class="sxs-lookup"><span data-stu-id="20f13-105">Multiplies sources into the destination.</span></span>

## <a name="syntax"></a><span data-ttu-id="20f13-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="20f13-106">Syntax</span></span>



| <span data-ttu-id="20f13-107">Mul DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="20f13-107">mul dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="20f13-108">where</span><span class="sxs-lookup"><span data-stu-id="20f13-108">where</span></span>

-   <span data-ttu-id="20f13-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="20f13-109">dst is the destination register.</span></span>
-   <span data-ttu-id="20f13-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="20f13-110">src0 is a source register.</span></span>
-   <span data-ttu-id="20f13-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="20f13-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="20f13-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20f13-112">Remarks</span></span>



| <span data-ttu-id="20f13-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="20f13-113">Pixel shader versions</span></span> | <span data-ttu-id="20f13-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="20f13-114">1\_1</span></span> | <span data-ttu-id="20f13-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="20f13-115">1\_2</span></span> | <span data-ttu-id="20f13-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="20f13-116">1\_3</span></span> | <span data-ttu-id="20f13-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="20f13-117">1\_4</span></span> | <span data-ttu-id="20f13-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="20f13-118">2\_0</span></span> | <span data-ttu-id="20f13-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="20f13-119">2\_x</span></span> | <span data-ttu-id="20f13-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="20f13-120">2\_sw</span></span> | <span data-ttu-id="20f13-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="20f13-121">3\_0</span></span> | <span data-ttu-id="20f13-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="20f13-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="20f13-123">mul</span><span class="sxs-lookup"><span data-stu-id="20f13-123">mul</span></span>                   | <span data-ttu-id="20f13-124">x</span><span class="sxs-lookup"><span data-stu-id="20f13-124">x</span></span>    | <span data-ttu-id="20f13-125">x</span><span class="sxs-lookup"><span data-stu-id="20f13-125">x</span></span>    | <span data-ttu-id="20f13-126">x</span><span class="sxs-lookup"><span data-stu-id="20f13-126">x</span></span>    | <span data-ttu-id="20f13-127">x</span><span class="sxs-lookup"><span data-stu-id="20f13-127">x</span></span>    | <span data-ttu-id="20f13-128">x</span><span class="sxs-lookup"><span data-stu-id="20f13-128">x</span></span>    | <span data-ttu-id="20f13-129">x</span><span class="sxs-lookup"><span data-stu-id="20f13-129">x</span></span>    | <span data-ttu-id="20f13-130">x</span><span class="sxs-lookup"><span data-stu-id="20f13-130">x</span></span>     | <span data-ttu-id="20f13-131">x</span><span class="sxs-lookup"><span data-stu-id="20f13-131">x</span></span>    | <span data-ttu-id="20f13-132">x</span><span class="sxs-lookup"><span data-stu-id="20f13-132">x</span></span>     |



 

<span data-ttu-id="20f13-133">Der folgende Code Ausschnitt zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="20f13-133">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x;
dest.y = src0.y * src1.y;
dest.z = src0.z * src1.z;
dest.w = src0.w * src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="20f13-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="20f13-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20f13-135">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="20f13-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




