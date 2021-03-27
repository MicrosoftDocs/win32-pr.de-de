---
title: Add-vs
description: Addiert zwei Vektoren. | Add-vs
ms.assetid: f66d3264-68be-4a4f-84fc-cc0f6c4245c9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 678e7f815a819be2abf1d985516fe081d3c09c94
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869696"
---
# <a name="add---vs"></a><span data-ttu-id="e2b32-104">Add-vs</span><span class="sxs-lookup"><span data-stu-id="e2b32-104">add - vs</span></span>

<span data-ttu-id="e2b32-105">Addiert zwei Vektoren.</span><span class="sxs-lookup"><span data-stu-id="e2b32-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2b32-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2b32-106">Syntax</span></span>



| <span data-ttu-id="e2b32-107">Add DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="e2b32-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="e2b32-108">where</span><span class="sxs-lookup"><span data-stu-id="e2b32-108">where</span></span>

-   <span data-ttu-id="e2b32-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="e2b32-109">dst is the destination register.</span></span>
-   <span data-ttu-id="e2b32-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="e2b32-110">src0 is a source register.</span></span>
-   <span data-ttu-id="e2b32-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="e2b32-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2b32-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2b32-112">Remarks</span></span>



| <span data-ttu-id="e2b32-113">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="e2b32-113">Vertex shader versions</span></span> | <span data-ttu-id="e2b32-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="e2b32-114">1\_1</span></span> | <span data-ttu-id="e2b32-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e2b32-115">2\_0</span></span> | <span data-ttu-id="e2b32-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e2b32-116">2\_x</span></span> | <span data-ttu-id="e2b32-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e2b32-117">2\_sw</span></span> | <span data-ttu-id="e2b32-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e2b32-118">3\_0</span></span> | <span data-ttu-id="e2b32-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e2b32-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="e2b32-120">add</span><span class="sxs-lookup"><span data-stu-id="e2b32-120">add</span></span>                    | <span data-ttu-id="e2b32-121">x</span><span class="sxs-lookup"><span data-stu-id="e2b32-121">x</span></span>    | <span data-ttu-id="e2b32-122">x</span><span class="sxs-lookup"><span data-stu-id="e2b32-122">x</span></span>    | <span data-ttu-id="e2b32-123">x</span><span class="sxs-lookup"><span data-stu-id="e2b32-123">x</span></span>    | <span data-ttu-id="e2b32-124">x</span><span class="sxs-lookup"><span data-stu-id="e2b32-124">x</span></span>     | <span data-ttu-id="e2b32-125">x</span><span class="sxs-lookup"><span data-stu-id="e2b32-125">x</span></span>    | <span data-ttu-id="e2b32-126">x</span><span class="sxs-lookup"><span data-stu-id="e2b32-126">x</span></span>     |



 

<span data-ttu-id="e2b32-127">Das folgende Code Fragment zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="e2b32-127">The following code fragment shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="e2b32-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e2b32-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2b32-129">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="e2b32-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




