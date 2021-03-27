---
title: Add-PS
description: Addiert zwei Vektoren. | Add-PS
ms.assetid: f7d29a66-879b-4160-82fd-0a1b2076559a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8c6ef7c14ac54610301f283d076751b0c4d4a5e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981121"
---
# <a name="add---ps"></a><span data-ttu-id="aea4e-104">Add-PS</span><span class="sxs-lookup"><span data-stu-id="aea4e-104">add - ps</span></span>

<span data-ttu-id="aea4e-105">Addiert zwei Vektoren.</span><span class="sxs-lookup"><span data-stu-id="aea4e-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="aea4e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="aea4e-106">Syntax</span></span>



| <span data-ttu-id="aea4e-107">Add DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="aea4e-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="aea4e-108">where</span><span class="sxs-lookup"><span data-stu-id="aea4e-108">where</span></span>

-   <span data-ttu-id="aea4e-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="aea4e-109">dst is the destination register.</span></span>
-   <span data-ttu-id="aea4e-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="aea4e-110">src0 is a source register.</span></span>
-   <span data-ttu-id="aea4e-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="aea4e-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="aea4e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aea4e-112">Remarks</span></span>



| <span data-ttu-id="aea4e-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="aea4e-113">Pixel shader versions</span></span> | <span data-ttu-id="aea4e-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="aea4e-114">1\_1</span></span> | <span data-ttu-id="aea4e-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="aea4e-115">1\_2</span></span> | <span data-ttu-id="aea4e-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="aea4e-116">1\_3</span></span> | <span data-ttu-id="aea4e-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="aea4e-117">1\_4</span></span> | <span data-ttu-id="aea4e-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="aea4e-118">2\_0</span></span> | <span data-ttu-id="aea4e-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="aea4e-119">2\_x</span></span> | <span data-ttu-id="aea4e-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="aea4e-120">2\_sw</span></span> | <span data-ttu-id="aea4e-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="aea4e-121">3\_0</span></span> | <span data-ttu-id="aea4e-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="aea4e-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="aea4e-123">add</span><span class="sxs-lookup"><span data-stu-id="aea4e-123">add</span></span>                   | <span data-ttu-id="aea4e-124">x</span><span class="sxs-lookup"><span data-stu-id="aea4e-124">x</span></span>    | <span data-ttu-id="aea4e-125">x</span><span class="sxs-lookup"><span data-stu-id="aea4e-125">x</span></span>    | <span data-ttu-id="aea4e-126">x</span><span class="sxs-lookup"><span data-stu-id="aea4e-126">x</span></span>    | <span data-ttu-id="aea4e-127">x</span><span class="sxs-lookup"><span data-stu-id="aea4e-127">x</span></span>    | <span data-ttu-id="aea4e-128">x</span><span class="sxs-lookup"><span data-stu-id="aea4e-128">x</span></span>    | <span data-ttu-id="aea4e-129">x</span><span class="sxs-lookup"><span data-stu-id="aea4e-129">x</span></span>    | <span data-ttu-id="aea4e-130">x</span><span class="sxs-lookup"><span data-stu-id="aea4e-130">x</span></span>     | <span data-ttu-id="aea4e-131">x</span><span class="sxs-lookup"><span data-stu-id="aea4e-131">x</span></span>    | <span data-ttu-id="aea4e-132">x</span><span class="sxs-lookup"><span data-stu-id="aea4e-132">x</span></span>     |



 

<span data-ttu-id="aea4e-133">Der folgende Code Ausschnitt zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="aea4e-133">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="instruction-information"></a><span data-ttu-id="aea4e-134">Anweisungs Informationen</span><span class="sxs-lookup"><span data-stu-id="aea4e-134">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="aea4e-135">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="aea4e-135">Minimum operating system</span></span> | <span data-ttu-id="aea4e-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="aea4e-136">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="aea4e-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aea4e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aea4e-138">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="aea4e-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




