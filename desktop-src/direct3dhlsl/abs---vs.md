---
title: abs – vs
description: Berechnet den absoluten Wert. | abs – vs
ms.assetid: d3b4cf06-dc87-4c71-aa2d-5ade4cf98caa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4d73ee738f575d93c2316e4ec47dced7cb128d3
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994747"
---
# <a name="abs---vs"></a><span data-ttu-id="e6823-104">abs – vs</span><span class="sxs-lookup"><span data-stu-id="e6823-104">abs - vs</span></span>

<span data-ttu-id="e6823-105">Berechnet den absoluten Wert.</span><span class="sxs-lookup"><span data-stu-id="e6823-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6823-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6823-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="e6823-107">abs dst, src</span><span class="sxs-lookup"><span data-stu-id="e6823-107">abs dst, src</span></span> |



 

<span data-ttu-id="e6823-108">where</span><span class="sxs-lookup"><span data-stu-id="e6823-108">where</span></span>

-   <span data-ttu-id="e6823-109">dst ist das Zielregister.</span><span class="sxs-lookup"><span data-stu-id="e6823-109">dst is the destination register.</span></span>
-   <span data-ttu-id="e6823-110">src ist ein Quellregister.</span><span class="sxs-lookup"><span data-stu-id="e6823-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6823-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e6823-111">Remarks</span></span>



| <span data-ttu-id="e6823-112">Vertex-Shaderversionen</span><span class="sxs-lookup"><span data-stu-id="e6823-112">Vertex shader versions</span></span> | <span data-ttu-id="e6823-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="e6823-113">1\_1</span></span> | <span data-ttu-id="e6823-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e6823-114">2\_0</span></span> | <span data-ttu-id="e6823-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e6823-115">2\_x</span></span> | <span data-ttu-id="e6823-116">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e6823-116">2\_sw</span></span> | <span data-ttu-id="e6823-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e6823-117">3\_0</span></span> | <span data-ttu-id="e6823-118">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e6823-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="e6823-119">abs</span><span class="sxs-lookup"><span data-stu-id="e6823-119">abs</span></span>                    |      | <span data-ttu-id="e6823-120">x</span><span class="sxs-lookup"><span data-stu-id="e6823-120">x</span></span>    | <span data-ttu-id="e6823-121">x</span><span class="sxs-lookup"><span data-stu-id="e6823-121">x</span></span>    | <span data-ttu-id="e6823-122">x</span><span class="sxs-lookup"><span data-stu-id="e6823-122">x</span></span>     | <span data-ttu-id="e6823-123">x</span><span class="sxs-lookup"><span data-stu-id="e6823-123">x</span></span>    | <span data-ttu-id="e6823-124">x</span><span class="sxs-lookup"><span data-stu-id="e6823-124">x</span></span>     |



 

<span data-ttu-id="e6823-125">Diese Anweisung funktioniert wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6823-125">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a><span data-ttu-id="e6823-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e6823-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6823-127">Vertex-Shader-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="e6823-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




