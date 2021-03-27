---
title: DP4-vs
description: Berechnet das vier-Komponenten-Punktprodukt der Quell Register. | DP4-vs
ms.assetid: ee3d3c8d-6031-4264-80ba-2b200a721310
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 747695436094dd5d2e9787e3eeca525b292f14c4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981401"
---
# <a name="dp4---vs"></a><span data-ttu-id="8337a-104">DP4-vs</span><span class="sxs-lookup"><span data-stu-id="8337a-104">dp4 - vs</span></span>

<span data-ttu-id="8337a-105">Berechnet das vier-Komponenten-Punktprodukt der Quell Register.</span><span class="sxs-lookup"><span data-stu-id="8337a-105">Computes the four-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="8337a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8337a-106">Syntax</span></span>



| <span data-ttu-id="8337a-107">DP4 DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="8337a-107">dp4 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="8337a-108">where</span><span class="sxs-lookup"><span data-stu-id="8337a-108">where</span></span>

-   <span data-ttu-id="8337a-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="8337a-109">dst is the destination register.</span></span>
-   <span data-ttu-id="8337a-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="8337a-110">src0 is a source register.</span></span>
-   <span data-ttu-id="8337a-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="8337a-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="8337a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8337a-112">Remarks</span></span>



| <span data-ttu-id="8337a-113">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="8337a-113">Vertex shader versions</span></span> | <span data-ttu-id="8337a-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="8337a-114">1\_1</span></span> | <span data-ttu-id="8337a-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8337a-115">2\_0</span></span> | <span data-ttu-id="8337a-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8337a-116">2\_x</span></span> | <span data-ttu-id="8337a-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8337a-117">2\_sw</span></span> | <span data-ttu-id="8337a-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8337a-118">3\_0</span></span> | <span data-ttu-id="8337a-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8337a-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="8337a-120">dp4</span><span class="sxs-lookup"><span data-stu-id="8337a-120">dp4</span></span>                    | <span data-ttu-id="8337a-121">x</span><span class="sxs-lookup"><span data-stu-id="8337a-121">x</span></span>    | <span data-ttu-id="8337a-122">x</span><span class="sxs-lookup"><span data-stu-id="8337a-122">x</span></span>    | <span data-ttu-id="8337a-123">x</span><span class="sxs-lookup"><span data-stu-id="8337a-123">x</span></span>    | <span data-ttu-id="8337a-124">x</span><span class="sxs-lookup"><span data-stu-id="8337a-124">x</span></span>     | <span data-ttu-id="8337a-125">x</span><span class="sxs-lookup"><span data-stu-id="8337a-125">x</span></span>    | <span data-ttu-id="8337a-126">x</span><span class="sxs-lookup"><span data-stu-id="8337a-126">x</span></span>     |



 

<span data-ttu-id="8337a-127">Das folgende Code Fragment zeigt die Vorgänge, die ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="8337a-127">The following code fragment shows the operations performed:</span></span>


```
dest.w = (src0.x * src1.x) + (src0.y * src1.y) + 
         (src0.z * src1.z) + (src0.w * src1.w);
dest.x = dest.y = dest.z = dest.w;
```



## <a name="related-topics"></a><span data-ttu-id="8337a-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8337a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8337a-129">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="8337a-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




