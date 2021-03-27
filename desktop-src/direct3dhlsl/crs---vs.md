---
title: CRS-vs
description: Berechnet ein Kreuz Produkt mit der rechten Regel. | CRS-vs
ms.assetid: 102108f5-acc8-49ce-a84b-b8060decbaa7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fee30fab91b4f491efd4311919245ec2cb98b555
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352559"
---
# <a name="crs---vs"></a><span data-ttu-id="a84d7-104">CRS-vs</span><span class="sxs-lookup"><span data-stu-id="a84d7-104">crs - vs</span></span>

<span data-ttu-id="a84d7-105">Berechnet ein Kreuz Produkt mit der rechten Regel.</span><span class="sxs-lookup"><span data-stu-id="a84d7-105">Computes a cross product using the right-hand rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="a84d7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a84d7-106">Syntax</span></span>



| <span data-ttu-id="a84d7-107">CRS DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="a84d7-107">crs dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="a84d7-108">where</span><span class="sxs-lookup"><span data-stu-id="a84d7-108">where</span></span>

-   <span data-ttu-id="a84d7-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="a84d7-109">dst is the destination register.</span></span>
-   <span data-ttu-id="a84d7-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="a84d7-110">src0 is a source register.</span></span>
-   <span data-ttu-id="a84d7-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="a84d7-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="a84d7-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a84d7-112">Remarks</span></span>



| <span data-ttu-id="a84d7-113">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="a84d7-113">Vertex shader versions</span></span> | <span data-ttu-id="a84d7-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="a84d7-114">1\_1</span></span> | <span data-ttu-id="a84d7-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a84d7-115">2\_0</span></span> | <span data-ttu-id="a84d7-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a84d7-116">2\_x</span></span> | <span data-ttu-id="a84d7-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a84d7-117">2\_sw</span></span> | <span data-ttu-id="a84d7-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a84d7-118">3\_0</span></span> | <span data-ttu-id="a84d7-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a84d7-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a84d7-120">Renn</span><span class="sxs-lookup"><span data-stu-id="a84d7-120">crs</span></span>                    |      | <span data-ttu-id="a84d7-121">x</span><span class="sxs-lookup"><span data-stu-id="a84d7-121">x</span></span>    | <span data-ttu-id="a84d7-122">x</span><span class="sxs-lookup"><span data-stu-id="a84d7-122">x</span></span>    | <span data-ttu-id="a84d7-123">x</span><span class="sxs-lookup"><span data-stu-id="a84d7-123">x</span></span>     | <span data-ttu-id="a84d7-124">x</span><span class="sxs-lookup"><span data-stu-id="a84d7-124">x</span></span>    | <span data-ttu-id="a84d7-125">x</span><span class="sxs-lookup"><span data-stu-id="a84d7-125">x</span></span>     |



 

<span data-ttu-id="a84d7-126">Diese Anweisung funktioniert wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a84d7-126">This instruction works as shown here.</span></span>


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



<span data-ttu-id="a84d7-127">Einige Einschränkungen bei der Verwendung:</span><span class="sxs-lookup"><span data-stu-id="a84d7-127">Some restrictions on use:</span></span>

-   <span data-ttu-id="a84d7-128">src0 darf nicht mit dem registrierten Register identisch sein.</span><span class="sxs-lookup"><span data-stu-id="a84d7-128">src0 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="a84d7-129">Quelle1 darf nicht mit dem registrierten Register identisch sein.</span><span class="sxs-lookup"><span data-stu-id="a84d7-129">src1 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="a84d7-130">src0 darf nicht über das standardswizzle (. xyzw) verfügen.</span><span class="sxs-lookup"><span data-stu-id="a84d7-130">src0 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="a84d7-131">Quelle1 darf nicht über das standardswizzle (. xyzw) verfügen.</span><span class="sxs-lookup"><span data-stu-id="a84d7-131">src1 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="a84d7-132">dest muss genau eine der folgenden sieben Masken haben:. x \| . y \| . z \| . XY \| . XZ \| . YZ \| . xyz.</span><span class="sxs-lookup"><span data-stu-id="a84d7-132">dest has to have exactly one of the following seven masks: .x \| .y \| .z \| .xy \| .xz \| .yz \| .xyz.</span></span>
-   <span data-ttu-id="a84d7-133">dest muss ein temporäres Register sein.</span><span class="sxs-lookup"><span data-stu-id="a84d7-133">dest must be a temporary register.</span></span>
-   <span data-ttu-id="a84d7-134">"dest" darf nicht identisch mit "src0" oder "Quelle1" sein.</span><span class="sxs-lookup"><span data-stu-id="a84d7-134">dest must not be the same register as src0 or src1</span></span>

## <a name="related-topics"></a><span data-ttu-id="a84d7-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a84d7-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a84d7-136">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="a84d7-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




