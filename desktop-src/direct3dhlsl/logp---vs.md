---
title: LogP-vs
description: LogP-Teil Genauigkeit (x).
ms.assetid: 8547ca8a-7bde-4e41-9e65-f7fcd65454c1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a261d63ad47dcf12728b8bcd0025ec578ede0b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038341"
---
# <a name="logp---vs"></a><span data-ttu-id="77191-103">LogP-vs</span><span class="sxs-lookup"><span data-stu-id="77191-103">logp - vs</span></span>

<span data-ttu-id="77191-104">LogP-Teil Genauigkeit (x).</span><span class="sxs-lookup"><span data-stu-id="77191-104">Partial precision logp₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="77191-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="77191-105">Syntax</span></span>



| <span data-ttu-id="77191-106">LogP DST, src</span><span class="sxs-lookup"><span data-stu-id="77191-106">logp dst, src</span></span> |
|---------------|



 

<span data-ttu-id="77191-107">where</span><span class="sxs-lookup"><span data-stu-id="77191-107">where</span></span>

-   <span data-ttu-id="77191-108">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="77191-108">dst is the destination register.</span></span>
-   <span data-ttu-id="77191-109">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="77191-109">src is a source register.</span></span> <span data-ttu-id="77191-110">Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="77191-110">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="77191-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77191-111">Remarks</span></span>



| <span data-ttu-id="77191-112">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="77191-112">Vertex shader versions</span></span> | <span data-ttu-id="77191-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="77191-113">1\_1</span></span> | <span data-ttu-id="77191-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="77191-114">2\_0</span></span> | <span data-ttu-id="77191-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="77191-115">2\_x</span></span> | <span data-ttu-id="77191-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="77191-116">2\_sw</span></span> | <span data-ttu-id="77191-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="77191-117">3\_0</span></span> | <span data-ttu-id="77191-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="77191-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="77191-119">LogP</span><span class="sxs-lookup"><span data-stu-id="77191-119">logp</span></span>                   | <span data-ttu-id="77191-120">x</span><span class="sxs-lookup"><span data-stu-id="77191-120">x</span></span>    | <span data-ttu-id="77191-121">x</span><span class="sxs-lookup"><span data-stu-id="77191-121">x</span></span>    | <span data-ttu-id="77191-122">x</span><span class="sxs-lookup"><span data-stu-id="77191-122">x</span></span>    | <span data-ttu-id="77191-123">x</span><span class="sxs-lookup"><span data-stu-id="77191-123">x</span></span>     | <span data-ttu-id="77191-124">x</span><span class="sxs-lookup"><span data-stu-id="77191-124">x</span></span>    | <span data-ttu-id="77191-125">x</span><span class="sxs-lookup"><span data-stu-id="77191-125">x</span></span>     |



 

<span data-ttu-id="77191-126">Das folgende Code Fragment zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="77191-126">The following code fragment shows the operations performed.</span></span>


```
float f = abs(src);
if (f != 0)
    dest.x = dest.y = dest.z = dest.w = (float)(log(f)/log(2));
else
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;   
```



<span data-ttu-id="77191-127">Diese Anweisung bietet Logarithmus Basis 2 partielle Genauigkeit (bis zu 10 Bits).</span><span class="sxs-lookup"><span data-stu-id="77191-127">This instruction provides logarithm base 2 partial precision, up to 10 bits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77191-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="77191-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77191-129">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="77191-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




