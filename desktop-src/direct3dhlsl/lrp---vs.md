---
title: LRP-vs
description: Interpoliert linear zwischen dem zweiten und dritten Quell Register durch einen im ersten Quell Register angegebenen Anteil. | LRP-vs
ms.assetid: 8438bcf3-9b00-4963-b2a3-54fd1c345961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 485d7720dc2c71ee599db93d179de8e665bfab77
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995567"
---
# <a name="lrp---vs"></a><span data-ttu-id="62490-104">LRP-vs</span><span class="sxs-lookup"><span data-stu-id="62490-104">lrp - vs</span></span>

<span data-ttu-id="62490-105">Interpoliert linear zwischen dem zweiten und dritten Quell Register durch einen im ersten Quell Register angegebenen Anteil.</span><span class="sxs-lookup"><span data-stu-id="62490-105">Interpolates linearly between the second and third source registers by a proportion specified in the first source register.</span></span>

## <a name="syntax"></a><span data-ttu-id="62490-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="62490-106">Syntax</span></span>



| <span data-ttu-id="62490-107">LRP DST, src0, Quelle1, Quelle2</span><span class="sxs-lookup"><span data-stu-id="62490-107">lrp dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="62490-108">where</span><span class="sxs-lookup"><span data-stu-id="62490-108">where</span></span>

-   <span data-ttu-id="62490-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="62490-109">dst is the destination register.</span></span>
-   <span data-ttu-id="62490-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="62490-110">src0 is a source register.</span></span>
-   <span data-ttu-id="62490-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="62490-111">src1 is a source register.</span></span>
-   <span data-ttu-id="62490-112">Quelle2 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="62490-112">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="62490-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62490-113">Remarks</span></span>



| <span data-ttu-id="62490-114">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="62490-114">Vertex shader versions</span></span> | <span data-ttu-id="62490-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="62490-115">1\_1</span></span> | <span data-ttu-id="62490-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="62490-116">2\_0</span></span> | <span data-ttu-id="62490-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="62490-117">2\_x</span></span> | <span data-ttu-id="62490-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="62490-118">2\_sw</span></span> | <span data-ttu-id="62490-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="62490-119">3\_0</span></span> | <span data-ttu-id="62490-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="62490-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="62490-121">startet</span><span class="sxs-lookup"><span data-stu-id="62490-121">lrp</span></span>                    |      | <span data-ttu-id="62490-122">x</span><span class="sxs-lookup"><span data-stu-id="62490-122">x</span></span>    | <span data-ttu-id="62490-123">x</span><span class="sxs-lookup"><span data-stu-id="62490-123">x</span></span>    | <span data-ttu-id="62490-124">x</span><span class="sxs-lookup"><span data-stu-id="62490-124">x</span></span>     | <span data-ttu-id="62490-125">x</span><span class="sxs-lookup"><span data-stu-id="62490-125">x</span></span>    | <span data-ttu-id="62490-126">x</span><span class="sxs-lookup"><span data-stu-id="62490-126">x</span></span>     |



 

<span data-ttu-id="62490-127">Diese Anweisung führt die lineare interpolung basierend auf der folgenden Formel aus.</span><span class="sxs-lookup"><span data-stu-id="62490-127">This instruction performs the linear interpolation based on the following formula.</span></span>


```
dest.x = src0.x * (src1.x - src2.x) + src2.x;
dest.y = src0.y * (src1.y - src2.y) + src2.y;
dest.z = src0.z * (src1.z - src2.z) + src2.z;
dest.w = src0.w * (src1.w - src2.w) + src2.w;
```



## <a name="related-topics"></a><span data-ttu-id="62490-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="62490-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62490-129">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="62490-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




