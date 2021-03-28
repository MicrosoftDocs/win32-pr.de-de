---
title: Mad-vs
description: Multipliziert und fügt Quellen hinzu.
ms.assetid: 059f0bf6-d143-4efc-b074-0ed026edb008
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 01e96bb63395fe9e5dd27a17fbb5c0ddd9bf3c17
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313668"
---
# <a name="mad---vs"></a><span data-ttu-id="63df8-103">Mad-vs</span><span class="sxs-lookup"><span data-stu-id="63df8-103">mad - vs</span></span>

<span data-ttu-id="63df8-104">Multipliziert und fügt Quellen hinzu.</span><span class="sxs-lookup"><span data-stu-id="63df8-104">Multiplies and adds sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="63df8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="63df8-105">Syntax</span></span>



| <span data-ttu-id="63df8-106">Mad DST, src0, Quelle1, Quelle2</span><span class="sxs-lookup"><span data-stu-id="63df8-106">mad dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="63df8-107">where</span><span class="sxs-lookup"><span data-stu-id="63df8-107">where</span></span>

-   <span data-ttu-id="63df8-108">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="63df8-108">dst is the destination register.</span></span>
-   <span data-ttu-id="63df8-109">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="63df8-109">src0 is a source register.</span></span>
-   <span data-ttu-id="63df8-110">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="63df8-110">src1 is a source register.</span></span>
-   <span data-ttu-id="63df8-111">Quelle2 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="63df8-111">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="63df8-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63df8-112">Remarks</span></span>



| <span data-ttu-id="63df8-113">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="63df8-113">Vertex shader versions</span></span> | <span data-ttu-id="63df8-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="63df8-114">1\_1</span></span> | <span data-ttu-id="63df8-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="63df8-115">2\_0</span></span> | <span data-ttu-id="63df8-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="63df8-116">2\_x</span></span> | <span data-ttu-id="63df8-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="63df8-117">2\_sw</span></span> | <span data-ttu-id="63df8-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="63df8-118">3\_0</span></span> | <span data-ttu-id="63df8-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="63df8-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="63df8-120">geworden</span><span class="sxs-lookup"><span data-stu-id="63df8-120">mad</span></span>                    | <span data-ttu-id="63df8-121">x</span><span class="sxs-lookup"><span data-stu-id="63df8-121">x</span></span>    | <span data-ttu-id="63df8-122">x</span><span class="sxs-lookup"><span data-stu-id="63df8-122">x</span></span>    | <span data-ttu-id="63df8-123">x</span><span class="sxs-lookup"><span data-stu-id="63df8-123">x</span></span>    | <span data-ttu-id="63df8-124">x</span><span class="sxs-lookup"><span data-stu-id="63df8-124">x</span></span>     | <span data-ttu-id="63df8-125">x</span><span class="sxs-lookup"><span data-stu-id="63df8-125">x</span></span>    | <span data-ttu-id="63df8-126">x</span><span class="sxs-lookup"><span data-stu-id="63df8-126">x</span></span>     |



 

<span data-ttu-id="63df8-127">Das folgende Code Fragment zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="63df8-127">The following code fragment shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x + src2.x;
dest.y = src0.y * src1.y + src2.y;
dest.z = src0.z * src1.z + src2.z;
dest.w = src0.w * src1.w + src2.w;
```



## <a name="related-topics"></a><span data-ttu-id="63df8-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="63df8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63df8-129">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="63df8-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




