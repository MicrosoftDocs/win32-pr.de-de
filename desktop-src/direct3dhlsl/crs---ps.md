---
title: CRS-PS
description: Berechnet ein Kreuz Produkt mit der rechten Regel. | CRS-PS
ms.assetid: 602fa7cc-4e2b-4d90-90d8-df00d5812c81
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b6098c8bf01bf0d8cce886276c1d1081720ea667
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352568"
---
# <a name="crs---ps"></a><span data-ttu-id="c1d91-104">CRS-PS</span><span class="sxs-lookup"><span data-stu-id="c1d91-104">crs - ps</span></span>

<span data-ttu-id="c1d91-105">Berechnet ein Kreuz Produkt mit der rechten Regel.</span><span class="sxs-lookup"><span data-stu-id="c1d91-105">Computes a cross product using the right-hand rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1d91-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1d91-106">Syntax</span></span>



| <span data-ttu-id="c1d91-107">CRS DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="c1d91-107">crs dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="c1d91-108">where</span><span class="sxs-lookup"><span data-stu-id="c1d91-108">where</span></span>

-   <span data-ttu-id="c1d91-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="c1d91-109">dst is the destination register.</span></span>
-   <span data-ttu-id="c1d91-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="c1d91-110">src0 is a source register.</span></span>
-   <span data-ttu-id="c1d91-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="c1d91-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1d91-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1d91-112">Remarks</span></span>



| <span data-ttu-id="c1d91-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="c1d91-113">Pixel shader versions</span></span> | <span data-ttu-id="c1d91-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="c1d91-114">1\_1</span></span> | <span data-ttu-id="c1d91-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="c1d91-115">1\_2</span></span> | <span data-ttu-id="c1d91-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c1d91-116">1\_3</span></span> | <span data-ttu-id="c1d91-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="c1d91-117">1\_4</span></span> | <span data-ttu-id="c1d91-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c1d91-118">2\_0</span></span> | <span data-ttu-id="c1d91-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c1d91-119">2\_x</span></span> | <span data-ttu-id="c1d91-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c1d91-120">2\_sw</span></span> | <span data-ttu-id="c1d91-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c1d91-121">3\_0</span></span> | <span data-ttu-id="c1d91-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c1d91-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c1d91-123">Renn</span><span class="sxs-lookup"><span data-stu-id="c1d91-123">crs</span></span>                   |      |      |      |      | <span data-ttu-id="c1d91-124">x</span><span class="sxs-lookup"><span data-stu-id="c1d91-124">x</span></span>    | <span data-ttu-id="c1d91-125">x</span><span class="sxs-lookup"><span data-stu-id="c1d91-125">x</span></span>    | <span data-ttu-id="c1d91-126">x</span><span class="sxs-lookup"><span data-stu-id="c1d91-126">x</span></span>     | <span data-ttu-id="c1d91-127">x</span><span class="sxs-lookup"><span data-stu-id="c1d91-127">x</span></span>    | <span data-ttu-id="c1d91-128">x</span><span class="sxs-lookup"><span data-stu-id="c1d91-128">x</span></span>     |



 

<span data-ttu-id="c1d91-129">Diese Anweisung funktioniert wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c1d91-129">This instruction works as shown here.</span></span>


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



<span data-ttu-id="c1d91-130">Einige Einschränkungen bei der Verwendung:</span><span class="sxs-lookup"><span data-stu-id="c1d91-130">Some restrictions on use:</span></span>

-   <span data-ttu-id="c1d91-131">src0 darf nicht mit dem registrierten Register identisch sein.</span><span class="sxs-lookup"><span data-stu-id="c1d91-131">src0 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="c1d91-132">Quelle1 darf nicht mit dem registrierten Register identisch sein.</span><span class="sxs-lookup"><span data-stu-id="c1d91-132">src1 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="c1d91-133">src0 darf nicht über das standardswizzle (. xyzw) verfügen.</span><span class="sxs-lookup"><span data-stu-id="c1d91-133">src0 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="c1d91-134">Quelle1 darf nicht über das standardswizzle (. xyzw) verfügen.</span><span class="sxs-lookup"><span data-stu-id="c1d91-134">src1 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="c1d91-135">dest muss genau eine der folgenden sieben Masken haben:. x \| . y \| . z \| . XY \| . XZ \| . YZ \| . xyz.</span><span class="sxs-lookup"><span data-stu-id="c1d91-135">dest has to have exactly one of the following seven masks: .x \| .y \| .z \| .xy \| .xz \| .yz \| .xyz.</span></span>
-   <span data-ttu-id="c1d91-136">dest muss ein temporäres Register sein.</span><span class="sxs-lookup"><span data-stu-id="c1d91-136">dest must be a temporary register.</span></span>
-   <span data-ttu-id="c1d91-137">"dest" darf nicht identisch mit "src0" oder "Quelle1" sein.</span><span class="sxs-lookup"><span data-stu-id="c1d91-137">dest must not be the same register as src0 or src1</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1d91-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c1d91-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1d91-139">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="c1d91-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




