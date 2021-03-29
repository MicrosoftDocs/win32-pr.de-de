---
title: dp2add-PS
description: Führt ein 2D-Punktprodukt und eine skalare Addition aus.
ms.assetid: 4226ee34-2e68-4536-b171-68f3b967182e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 88d3d28cc64bdb7caa1b7456e87711c3dbee2b13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101070"
---
# <a name="dp2add---ps"></a><span data-ttu-id="f5b55-103">dp2add-PS</span><span class="sxs-lookup"><span data-stu-id="f5b55-103">dp2add - ps</span></span>

<span data-ttu-id="f5b55-104">Führt ein 2D-Punktprodukt und eine skalare Addition aus.</span><span class="sxs-lookup"><span data-stu-id="f5b55-104">Performs a 2D dot product and a scalar addition.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5b55-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5b55-105">Syntax</span></span>


```
dp2add dst, src0, src1, src2.{x|y|z|w}
```



<span data-ttu-id="f5b55-106">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="f5b55-106">Where:</span></span>

-   <span data-ttu-id="f5b55-107">DST ist ein Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="f5b55-107">dst is a destination register.</span></span>
-   <span data-ttu-id="f5b55-108">src0, Quelle1 und Quelle2 sind drei Quell Register.</span><span class="sxs-lookup"><span data-stu-id="f5b55-108">src0, src1, and src2 are three source registers.</span></span>
-   <span data-ttu-id="f5b55-109">{x \| y \| z \| w} ist das erforderliche Replizieren von Replizieren auf Quelle2.</span><span class="sxs-lookup"><span data-stu-id="f5b55-109">{x\|y\|z\|w} is the required replicate swizzle on src2.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5b55-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5b55-110">Remarks</span></span>



| <span data-ttu-id="f5b55-111">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="f5b55-111">Pixel shader versions</span></span> | <span data-ttu-id="f5b55-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="f5b55-112">1\_1</span></span> | <span data-ttu-id="f5b55-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="f5b55-113">1\_2</span></span> | <span data-ttu-id="f5b55-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f5b55-114">1\_3</span></span> | <span data-ttu-id="f5b55-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="f5b55-115">1\_4</span></span> | <span data-ttu-id="f5b55-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f5b55-116">2\_0</span></span> | <span data-ttu-id="f5b55-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f5b55-117">2\_x</span></span> | <span data-ttu-id="f5b55-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f5b55-118">2\_sw</span></span> | <span data-ttu-id="f5b55-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f5b55-119">3\_0</span></span> | <span data-ttu-id="f5b55-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f5b55-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f5b55-121">dp2add</span><span class="sxs-lookup"><span data-stu-id="f5b55-121">dp2add</span></span>                |      |      |      |      | <span data-ttu-id="f5b55-122">x</span><span class="sxs-lookup"><span data-stu-id="f5b55-122">x</span></span>    | <span data-ttu-id="f5b55-123">x</span><span class="sxs-lookup"><span data-stu-id="f5b55-123">x</span></span>    | <span data-ttu-id="f5b55-124">x</span><span class="sxs-lookup"><span data-stu-id="f5b55-124">x</span></span>     | <span data-ttu-id="f5b55-125">x</span><span class="sxs-lookup"><span data-stu-id="f5b55-125">x</span></span>    | <span data-ttu-id="f5b55-126">x</span><span class="sxs-lookup"><span data-stu-id="f5b55-126">x</span></span>     |



 

<span data-ttu-id="f5b55-127">Der Skalarwert für Add wird durch das Replizieren von Replizieren auf Quelle2 ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f5b55-127">The scalar value for add is chosen by the replicate swizzle on src2.</span></span>

<span data-ttu-id="f5b55-128">Der folgende Code Ausschnitt zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="f5b55-128">The following code snippet shows the operations performed.</span></span>


```
dest = src0.r * src1.r + src0.g * src1.g + src2.replicate_swizzle
// The scalar result is replicated to the write mask components
```



## <a name="related-topics"></a><span data-ttu-id="f5b55-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f5b55-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5b55-130">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="f5b55-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




