---
title: abs - ps
description: Berechnet den absoluten Wert. | abs - ps
ms.assetid: e97db550-2a03-421a-86f4-a6fc5f8e0bca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3e7af7b2d30e9d9f2092cb6671610f008ec781d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994877"
---
# <a name="abs---ps"></a><span data-ttu-id="fd4f4-104">abs - ps</span><span class="sxs-lookup"><span data-stu-id="fd4f4-104">abs - ps</span></span>

<span data-ttu-id="fd4f4-105">Berechnet den absoluten Wert.</span><span class="sxs-lookup"><span data-stu-id="fd4f4-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd4f4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd4f4-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="fd4f4-107">abs dst, src</span><span class="sxs-lookup"><span data-stu-id="fd4f4-107">abs dst, src</span></span> |



 

<span data-ttu-id="fd4f4-108">where</span><span class="sxs-lookup"><span data-stu-id="fd4f4-108">where</span></span>

-   <span data-ttu-id="fd4f4-109">dst ist das Zielregister.</span><span class="sxs-lookup"><span data-stu-id="fd4f4-109">dst is the destination register.</span></span>
-   <span data-ttu-id="fd4f4-110">src ist ein Quellregister.</span><span class="sxs-lookup"><span data-stu-id="fd4f4-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd4f4-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fd4f4-111">Remarks</span></span>



| <span data-ttu-id="fd4f4-112">Pixel-Shaderversionen</span><span class="sxs-lookup"><span data-stu-id="fd4f4-112">Pixel shader versions</span></span> | <span data-ttu-id="fd4f4-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="fd4f4-113">1\_1</span></span> | <span data-ttu-id="fd4f4-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="fd4f4-114">1\_2</span></span> | <span data-ttu-id="fd4f4-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="fd4f4-115">1\_3</span></span> | <span data-ttu-id="fd4f4-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="fd4f4-116">1\_4</span></span> | <span data-ttu-id="fd4f4-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fd4f4-117">2\_0</span></span> | <span data-ttu-id="fd4f4-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fd4f4-118">2\_x</span></span> | <span data-ttu-id="fd4f4-119">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="fd4f4-119">2\_sw</span></span> | <span data-ttu-id="fd4f4-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fd4f4-120">3\_0</span></span> | <span data-ttu-id="fd4f4-121">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="fd4f4-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="fd4f4-122">abs</span><span class="sxs-lookup"><span data-stu-id="fd4f4-122">abs</span></span>                   |      |      |      |      | <span data-ttu-id="fd4f4-123">x</span><span class="sxs-lookup"><span data-stu-id="fd4f4-123">x</span></span>    | <span data-ttu-id="fd4f4-124">x</span><span class="sxs-lookup"><span data-stu-id="fd4f4-124">x</span></span>    | <span data-ttu-id="fd4f4-125">x</span><span class="sxs-lookup"><span data-stu-id="fd4f4-125">x</span></span>     | <span data-ttu-id="fd4f4-126">x</span><span class="sxs-lookup"><span data-stu-id="fd4f4-126">x</span></span>    | <span data-ttu-id="fd4f4-127">x</span><span class="sxs-lookup"><span data-stu-id="fd4f4-127">x</span></span>     |



 

<span data-ttu-id="fd4f4-128">Diese Anweisung funktioniert wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="fd4f4-128">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="instruction-information"></a><span data-ttu-id="fd4f4-129">Anweisungsinformationen</span><span class="sxs-lookup"><span data-stu-id="fd4f4-129">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="fd4f4-130">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="fd4f4-130">Minimum operating system</span></span> | <span data-ttu-id="fd4f4-131">Windows 98</span><span class="sxs-lookup"><span data-stu-id="fd4f4-131">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fd4f4-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd4f4-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd4f4-133">Anweisungen für Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="fd4f4-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




