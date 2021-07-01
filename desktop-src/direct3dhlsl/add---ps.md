---
title: add - ps
description: Fügt zwei Vektoren hinzu. | add - ps
ms.assetid: f7d29a66-879b-4160-82fd-0a1b2076559a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54092caf19a486b68b92ef63d992f11289a51c93
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113130089"
---
# <a name="add---ps"></a><span data-ttu-id="b855d-104">add - ps</span><span class="sxs-lookup"><span data-stu-id="b855d-104">add - ps</span></span>

<span data-ttu-id="b855d-105">Fügt zwei Vektoren hinzu.</span><span class="sxs-lookup"><span data-stu-id="b855d-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="b855d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b855d-106">Syntax</span></span>



| <span data-ttu-id="b855d-107">add dst, src0, src1</span><span class="sxs-lookup"><span data-stu-id="b855d-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="b855d-108">where</span><span class="sxs-lookup"><span data-stu-id="b855d-108">where</span></span>

-   <span data-ttu-id="b855d-109">dst ist das Zielregister.</span><span class="sxs-lookup"><span data-stu-id="b855d-109">dst is the destination register.</span></span>
-   <span data-ttu-id="b855d-110">src0 ist ein Quellregister.</span><span class="sxs-lookup"><span data-stu-id="b855d-110">src0 is a source register.</span></span>
-   <span data-ttu-id="b855d-111">src1 ist ein Quellregister.</span><span class="sxs-lookup"><span data-stu-id="b855d-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="b855d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b855d-112">Remarks</span></span>



| <span data-ttu-id="b855d-113">Pixel-Shaderversionen</span><span class="sxs-lookup"><span data-stu-id="b855d-113">Pixel shader versions</span></span> | <span data-ttu-id="b855d-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="b855d-114">1\_1</span></span> | <span data-ttu-id="b855d-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="b855d-115">1\_2</span></span> | <span data-ttu-id="b855d-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b855d-116">1\_3</span></span> | <span data-ttu-id="b855d-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="b855d-117">1\_4</span></span> | <span data-ttu-id="b855d-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b855d-118">2\_0</span></span> | <span data-ttu-id="b855d-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b855d-119">2\_x</span></span> | <span data-ttu-id="b855d-120">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="b855d-120">2\_sw</span></span> | <span data-ttu-id="b855d-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b855d-121">3\_0</span></span> | <span data-ttu-id="b855d-122">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="b855d-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b855d-123">add</span><span class="sxs-lookup"><span data-stu-id="b855d-123">add</span></span>                   | <span data-ttu-id="b855d-124">x</span><span class="sxs-lookup"><span data-stu-id="b855d-124">x</span></span>    | <span data-ttu-id="b855d-125">x</span><span class="sxs-lookup"><span data-stu-id="b855d-125">x</span></span>    | <span data-ttu-id="b855d-126">x</span><span class="sxs-lookup"><span data-stu-id="b855d-126">x</span></span>    | <span data-ttu-id="b855d-127">x</span><span class="sxs-lookup"><span data-stu-id="b855d-127">x</span></span>    | <span data-ttu-id="b855d-128">x</span><span class="sxs-lookup"><span data-stu-id="b855d-128">x</span></span>    | <span data-ttu-id="b855d-129">x</span><span class="sxs-lookup"><span data-stu-id="b855d-129">x</span></span>    | <span data-ttu-id="b855d-130">x</span><span class="sxs-lookup"><span data-stu-id="b855d-130">x</span></span>     | <span data-ttu-id="b855d-131">x</span><span class="sxs-lookup"><span data-stu-id="b855d-131">x</span></span>    | <span data-ttu-id="b855d-132">x</span><span class="sxs-lookup"><span data-stu-id="b855d-132">x</span></span>     |



 

<span data-ttu-id="b855d-133">Der folgende Codeausschnitt zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="b855d-133">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="instruction-information"></a><span data-ttu-id="b855d-134">Anweisungsinformationen</span><span class="sxs-lookup"><span data-stu-id="b855d-134">Instruction Information</span></span>



|   <span data-ttu-id="b855d-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b855d-135">Requirement</span></span>                       | <span data-ttu-id="b855d-136">Wert</span><span class="sxs-lookup"><span data-stu-id="b855d-136">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="b855d-137">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="b855d-137">Minimum operating system</span></span> | <span data-ttu-id="b855d-138">Windows 98</span><span class="sxs-lookup"><span data-stu-id="b855d-138">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b855d-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b855d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b855d-140">Anweisungen zum Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="b855d-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




