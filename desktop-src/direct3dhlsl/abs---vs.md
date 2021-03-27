---
title: ABS-vs
description: Berechnet den absoluten Wert. | ABS-vs
ms.assetid: d3b4cf06-dc87-4c71-aa2d-5ade4cf98caa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 07667954de97e2a1da3999237930fb33796d9030
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219128"
---
# <a name="abs---vs"></a><span data-ttu-id="81bf3-104">ABS-vs</span><span class="sxs-lookup"><span data-stu-id="81bf3-104">abs - vs</span></span>

<span data-ttu-id="81bf3-105">Berechnet den absoluten Wert.</span><span class="sxs-lookup"><span data-stu-id="81bf3-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="81bf3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="81bf3-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="81bf3-107">ABS DST, src</span><span class="sxs-lookup"><span data-stu-id="81bf3-107">abs dst, src</span></span> |



 

<span data-ttu-id="81bf3-108">where</span><span class="sxs-lookup"><span data-stu-id="81bf3-108">where</span></span>

-   <span data-ttu-id="81bf3-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="81bf3-109">dst is the destination register.</span></span>
-   <span data-ttu-id="81bf3-110">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="81bf3-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="81bf3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81bf3-111">Remarks</span></span>



|                        |      |      |      |       |      |       |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="81bf3-112">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="81bf3-112">Vertex shader versions</span></span> | <span data-ttu-id="81bf3-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="81bf3-113">1\_1</span></span> | <span data-ttu-id="81bf3-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="81bf3-114">2\_0</span></span> | <span data-ttu-id="81bf3-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="81bf3-115">2\_x</span></span> | <span data-ttu-id="81bf3-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="81bf3-116">2\_sw</span></span> | <span data-ttu-id="81bf3-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="81bf3-117">3\_0</span></span> | <span data-ttu-id="81bf3-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="81bf3-118">3\_sw</span></span> |
| <span data-ttu-id="81bf3-119">abs</span><span class="sxs-lookup"><span data-stu-id="81bf3-119">abs</span></span>                    |      | <span data-ttu-id="81bf3-120">x</span><span class="sxs-lookup"><span data-stu-id="81bf3-120">x</span></span>    | <span data-ttu-id="81bf3-121">x</span><span class="sxs-lookup"><span data-stu-id="81bf3-121">x</span></span>    | <span data-ttu-id="81bf3-122">x</span><span class="sxs-lookup"><span data-stu-id="81bf3-122">x</span></span>     | <span data-ttu-id="81bf3-123">x</span><span class="sxs-lookup"><span data-stu-id="81bf3-123">x</span></span>    | <span data-ttu-id="81bf3-124">x</span><span class="sxs-lookup"><span data-stu-id="81bf3-124">x</span></span>     |



 

<span data-ttu-id="81bf3-125">Diese Anweisung funktioniert wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="81bf3-125">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a><span data-ttu-id="81bf3-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="81bf3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81bf3-127">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="81bf3-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




