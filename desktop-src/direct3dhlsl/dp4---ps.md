---
title: DP4-PS
description: Berechnet das vier-Komponenten-Punktprodukt der Quell Register. | DP4-PS
ms.assetid: 83ef6097-cacf-4498-842b-3eb03e57bd6f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2562259af164b8680d54e9a120abaa405fd781c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050772"
---
# <a name="dp4---ps"></a><span data-ttu-id="f5df9-104">DP4-PS</span><span class="sxs-lookup"><span data-stu-id="f5df9-104">dp4 - ps</span></span>

<span data-ttu-id="f5df9-105">Berechnet das vier-Komponenten-Punktprodukt der Quell Register.</span><span class="sxs-lookup"><span data-stu-id="f5df9-105">Computes the four-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5df9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5df9-106">Syntax</span></span>



| <span data-ttu-id="f5df9-107">DP4 DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="f5df9-107">dp4 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="f5df9-108">where</span><span class="sxs-lookup"><span data-stu-id="f5df9-108">where</span></span>

-   <span data-ttu-id="f5df9-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="f5df9-109">dst is the destination register.</span></span>
-   <span data-ttu-id="f5df9-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="f5df9-110">src0 is a source register.</span></span>
-   <span data-ttu-id="f5df9-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="f5df9-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5df9-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5df9-112">Remarks</span></span>



| <span data-ttu-id="f5df9-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="f5df9-113">Pixel shader versions</span></span> | <span data-ttu-id="f5df9-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="f5df9-114">1\_1</span></span> | <span data-ttu-id="f5df9-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="f5df9-115">1\_2</span></span> | <span data-ttu-id="f5df9-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f5df9-116">1\_3</span></span> | <span data-ttu-id="f5df9-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="f5df9-117">1\_4</span></span> | <span data-ttu-id="f5df9-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f5df9-118">2\_0</span></span> | <span data-ttu-id="f5df9-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f5df9-119">2\_x</span></span> | <span data-ttu-id="f5df9-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f5df9-120">2\_sw</span></span> | <span data-ttu-id="f5df9-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f5df9-121">3\_0</span></span> | <span data-ttu-id="f5df9-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f5df9-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f5df9-123">dp4</span><span class="sxs-lookup"><span data-stu-id="f5df9-123">dp4</span></span>                   |      | <span data-ttu-id="f5df9-124">x</span><span class="sxs-lookup"><span data-stu-id="f5df9-124">x</span></span>    | <span data-ttu-id="f5df9-125">x</span><span class="sxs-lookup"><span data-stu-id="f5df9-125">x</span></span>    | <span data-ttu-id="f5df9-126">x</span><span class="sxs-lookup"><span data-stu-id="f5df9-126">x</span></span>    | <span data-ttu-id="f5df9-127">x</span><span class="sxs-lookup"><span data-stu-id="f5df9-127">x</span></span>    | <span data-ttu-id="f5df9-128">x</span><span class="sxs-lookup"><span data-stu-id="f5df9-128">x</span></span>    | <span data-ttu-id="f5df9-129">x</span><span class="sxs-lookup"><span data-stu-id="f5df9-129">x</span></span>     | <span data-ttu-id="f5df9-130">x</span><span class="sxs-lookup"><span data-stu-id="f5df9-130">x</span></span>    | <span data-ttu-id="f5df9-131">x</span><span class="sxs-lookup"><span data-stu-id="f5df9-131">x</span></span>     |



 

<span data-ttu-id="f5df9-132">Der folgende Code Ausschnitt zeigt die Vorgänge, die ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="f5df9-132">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = 
    (src0.x * src1.x) + (src0.y * src1.y) + 
    (src0.z * src1.z) + (src0.w * src1.w);
```



<span data-ttu-id="f5df9-133">Einschränkungen für PS \_ 1 \_ 2 und PS \_ 1 \_ 3:</span><span class="sxs-lookup"><span data-stu-id="f5df9-133">Limitations for ps\_1\_2 and ps\_1\_3:</span></span>

-   <span data-ttu-id="f5df9-134">Jeder Shader kann bis zu maximal vier DP4-Anweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5df9-134">Each shader can use up to a maximum of four dp4 instructions.</span></span>
-   <span data-ttu-id="f5df9-135">Jede DP4-Anweisung zählt als zwei arithmetische Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="f5df9-135">Each dp4 instruction counts as two arithmetic instructions.</span></span>

<span data-ttu-id="f5df9-136">Einschränkungen für 1 \_ X-Versionen:</span><span class="sxs-lookup"><span data-stu-id="f5df9-136">Limitations for 1\_X versions:</span></span>

-   <span data-ttu-id="f5df9-137">Diese Anweisung kann nicht gemeinsam ausgestellt werden, da DP4 sowohl in der Vektor-als auch in der Alpha Pipeline ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5df9-137">This instruction cannot be co-issued because dp4 runs in both the vector and alpha pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5df9-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f5df9-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5df9-139">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="f5df9-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




