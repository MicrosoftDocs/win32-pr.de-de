---
title: abs – ps
description: Berechnet den absoluten Wert. | abs – ps
ms.assetid: e97db550-2a03-421a-86f4-a6fc5f8e0bca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f4f22261a114333ed77d67d7c0ac2738d3522054
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343326"
---
# <a name="abs---ps"></a><span data-ttu-id="08589-104">abs – ps</span><span class="sxs-lookup"><span data-stu-id="08589-104">abs - ps</span></span>

<span data-ttu-id="08589-105">Berechnet den absoluten Wert.</span><span class="sxs-lookup"><span data-stu-id="08589-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="08589-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="08589-106">Syntax</span></span>

<span data-ttu-id="08589-107">**abs dst, src**</span><span class="sxs-lookup"><span data-stu-id="08589-107">**abs dst, src**</span></span>

<span data-ttu-id="08589-108">where</span><span class="sxs-lookup"><span data-stu-id="08589-108">where</span></span>

-   <span data-ttu-id="08589-109">dst ist das Zielregister.</span><span class="sxs-lookup"><span data-stu-id="08589-109">dst is the destination register.</span></span>
-   <span data-ttu-id="08589-110">src ist ein Quellregister.</span><span class="sxs-lookup"><span data-stu-id="08589-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="08589-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="08589-111">Remarks</span></span>



| <span data-ttu-id="08589-112">Pixelshaderversionen</span><span class="sxs-lookup"><span data-stu-id="08589-112">Pixel shader versions</span></span> | <span data-ttu-id="08589-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="08589-113">1\_1</span></span> | <span data-ttu-id="08589-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="08589-114">1\_2</span></span> | <span data-ttu-id="08589-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="08589-115">1\_3</span></span> | <span data-ttu-id="08589-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="08589-116">1\_4</span></span> | <span data-ttu-id="08589-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="08589-117">2\_0</span></span> | <span data-ttu-id="08589-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="08589-118">2\_x</span></span> | <span data-ttu-id="08589-119">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="08589-119">2\_sw</span></span> | <span data-ttu-id="08589-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="08589-120">3\_0</span></span> | <span data-ttu-id="08589-121">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="08589-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="08589-122">abs</span><span class="sxs-lookup"><span data-stu-id="08589-122">abs</span></span>                   |      |      |      |      | <span data-ttu-id="08589-123">x</span><span class="sxs-lookup"><span data-stu-id="08589-123">x</span></span>    | <span data-ttu-id="08589-124">x</span><span class="sxs-lookup"><span data-stu-id="08589-124">x</span></span>    | <span data-ttu-id="08589-125">x</span><span class="sxs-lookup"><span data-stu-id="08589-125">x</span></span>     | <span data-ttu-id="08589-126">x</span><span class="sxs-lookup"><span data-stu-id="08589-126">x</span></span>    | <span data-ttu-id="08589-127">x</span><span class="sxs-lookup"><span data-stu-id="08589-127">x</span></span>     |



 

<span data-ttu-id="08589-128">Diese Anweisung funktioniert wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="08589-128">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="instruction-information"></a><span data-ttu-id="08589-129">Anweisungsinformationen</span><span class="sxs-lookup"><span data-stu-id="08589-129">Instruction Information</span></span>



| <span data-ttu-id="08589-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08589-130">Requirement</span></span>                         | <span data-ttu-id="08589-131">Wert</span><span class="sxs-lookup"><span data-stu-id="08589-131">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="08589-132">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="08589-132">Minimum operating system</span></span> | <span data-ttu-id="08589-133">Windows 98</span><span class="sxs-lookup"><span data-stu-id="08589-133">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="08589-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08589-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08589-135">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="08589-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




