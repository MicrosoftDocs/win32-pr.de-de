---
title: CMP-PS
description: Wählen Sie Quelle1 if src0 0 aus. Andernfalls wählen Sie Quelle2 aus. Der Vergleich erfolgt pro Kanal.
ms.assetid: 8fabd548-3f5e-4b78-bf1e-16e4f1548ccd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da3da1062d02e995876a1f67e5c4e19518774760
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038329"
---
# <a name="cmp---ps"></a><span data-ttu-id="86860-105">CMP-PS</span><span class="sxs-lookup"><span data-stu-id="86860-105">cmp - ps</span></span>

<span data-ttu-id="86860-106">Wählen Sie Quelle1, wenn src0 >= 0 aus.</span><span class="sxs-lookup"><span data-stu-id="86860-106">Choose src1 if src0 >= 0.</span></span> <span data-ttu-id="86860-107">Andernfalls wählen Sie Quelle2 aus.</span><span class="sxs-lookup"><span data-stu-id="86860-107">Otherwise, choose src2.</span></span> <span data-ttu-id="86860-108">Der Vergleich erfolgt pro Kanal.</span><span class="sxs-lookup"><span data-stu-id="86860-108">The comparison is done per channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="86860-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="86860-109">Syntax</span></span>



| <span data-ttu-id="86860-110">CMP DST, src0, Quelle1, Quelle2</span><span class="sxs-lookup"><span data-stu-id="86860-110">cmp dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="86860-111">where</span><span class="sxs-lookup"><span data-stu-id="86860-111">where</span></span>

-   <span data-ttu-id="86860-112">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="86860-112">dst is the destination register.</span></span>
-   <span data-ttu-id="86860-113">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="86860-113">src0 is a source register.</span></span>
-   <span data-ttu-id="86860-114">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="86860-114">src1 is a source register.</span></span>
-   <span data-ttu-id="86860-115">Quelle2 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="86860-115">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="86860-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86860-116">Remarks</span></span>



| <span data-ttu-id="86860-117">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="86860-117">Pixel shader versions</span></span> | <span data-ttu-id="86860-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="86860-118">1\_1</span></span> | <span data-ttu-id="86860-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="86860-119">1\_2</span></span> | <span data-ttu-id="86860-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="86860-120">1\_3</span></span> | <span data-ttu-id="86860-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="86860-121">1\_4</span></span> | <span data-ttu-id="86860-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="86860-122">2\_0</span></span> | <span data-ttu-id="86860-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="86860-123">2\_x</span></span> | <span data-ttu-id="86860-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="86860-124">2\_sw</span></span> | <span data-ttu-id="86860-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="86860-125">3\_0</span></span> | <span data-ttu-id="86860-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="86860-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="86860-127">CMP</span><span class="sxs-lookup"><span data-stu-id="86860-127">cmp</span></span>                   |      | <span data-ttu-id="86860-128">x</span><span class="sxs-lookup"><span data-stu-id="86860-128">x</span></span>    | <span data-ttu-id="86860-129">x</span><span class="sxs-lookup"><span data-stu-id="86860-129">x</span></span>    | <span data-ttu-id="86860-130">x</span><span class="sxs-lookup"><span data-stu-id="86860-130">x</span></span>    | <span data-ttu-id="86860-131">x</span><span class="sxs-lookup"><span data-stu-id="86860-131">x</span></span>    | <span data-ttu-id="86860-132">x</span><span class="sxs-lookup"><span data-stu-id="86860-132">x</span></span>    | <span data-ttu-id="86860-133">x</span><span class="sxs-lookup"><span data-stu-id="86860-133">x</span></span>     | <span data-ttu-id="86860-134">x</span><span class="sxs-lookup"><span data-stu-id="86860-134">x</span></span>    | <span data-ttu-id="86860-135">x</span><span class="sxs-lookup"><span data-stu-id="86860-135">x</span></span>     |



 

<span data-ttu-id="86860-136">Für die Versionen 1 \_ 2 und 1 3 gelten einige zusätzliche Einschränkungen \_ :</span><span class="sxs-lookup"><span data-stu-id="86860-136">There are a few additional limitations for versions 1\_2 and 1\_3:</span></span>

-   <span data-ttu-id="86860-137">Jeder Shader kann bis zu maximal drei CMP-Anweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="86860-137">Each shader can use up to a maximum of three cmp instructions.</span></span>
-   <span data-ttu-id="86860-138">Das Ziel Register darf nicht mit einem der Quell Register identisch sein.</span><span class="sxs-lookup"><span data-stu-id="86860-138">The destination register cannot be the same as any of the source registers.</span></span>

<span data-ttu-id="86860-139">In diesem Beispiel wird ein Vergleich mit vier Kanälen durchführt.</span><span class="sxs-lookup"><span data-stu-id="86860-139">This example does a four-channel comparison.</span></span>


```
ps_1_4
def c0, -0.6, 0.6, 0, 0.6
def c1  0,0,0,0
def c2  1,1,1,1

mov r1, c1
mov r2, c2

cmp r0, c0, r1, r2   // r0 is assigned 1,0,0,0 based on the following:

// r0.x = c2.x because c0.x < 0
// r0.y = c1.y because c0.y >= 0
// r0.z = c1.z because c0.z >= 0
// r0.w = c1.w because c0.w >= 0
```



## <a name="related-topics"></a><span data-ttu-id="86860-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="86860-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86860-141">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="86860-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




