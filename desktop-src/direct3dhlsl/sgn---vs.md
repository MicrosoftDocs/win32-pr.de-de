---
title: SGN-vs
description: Berechnet das Vorzeichen der Eingabe.
ms.assetid: b03530d1-c621-483e-bd94-31abafeb2e6e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8573ff7e33a127d7c30af1fe512fbd3da298d0eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389543"
---
# <a name="sgn---vs"></a><span data-ttu-id="3884b-103">SGN-vs</span><span class="sxs-lookup"><span data-stu-id="3884b-103">sgn - vs</span></span>

<span data-ttu-id="3884b-104">Berechnet das Vorzeichen der Eingabe.</span><span class="sxs-lookup"><span data-stu-id="3884b-104">Computes the sign of the input.</span></span>

## <a name="syntax"></a><span data-ttu-id="3884b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3884b-105">Syntax</span></span>



| <span data-ttu-id="3884b-106">SGN DST, src0, Quelle1, Quelle2</span><span class="sxs-lookup"><span data-stu-id="3884b-106">sgn dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="3884b-107">where</span><span class="sxs-lookup"><span data-stu-id="3884b-107">where</span></span>

-   <span data-ttu-id="3884b-108">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="3884b-108">dst is the destination register.</span></span>
-   <span data-ttu-id="3884b-109">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="3884b-109">src0 is a source register.</span></span>
-   <span data-ttu-id="3884b-110">Quelle1 ist ein temporäres Register, das Zwischenergebnisse enthält.</span><span class="sxs-lookup"><span data-stu-id="3884b-110">src1 is a temporary register that holds intermediate results.</span></span> <span data-ttu-id="3884b-111">Nach der Ausführung sind die Inhalte nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="3884b-111">Following execution, contents are undefined.</span></span>
-   <span data-ttu-id="3884b-112">Quelle2 ist ein temporäres Register, das Zwischenergebnisse enthält.</span><span class="sxs-lookup"><span data-stu-id="3884b-112">src2 is a temporary register that holds intermediate results.</span></span> <span data-ttu-id="3884b-113">Nach der Ausführung sind die Inhalte nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="3884b-113">Following execution, contents are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="3884b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3884b-114">Remarks</span></span>



| <span data-ttu-id="3884b-115">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="3884b-115">Vertex shader versions</span></span> | <span data-ttu-id="3884b-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="3884b-116">1\_1</span></span> | <span data-ttu-id="3884b-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3884b-117">2\_0</span></span> | <span data-ttu-id="3884b-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3884b-118">2\_x</span></span> | <span data-ttu-id="3884b-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3884b-119">2\_sw</span></span> | <span data-ttu-id="3884b-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3884b-120">3\_0</span></span> | <span data-ttu-id="3884b-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3884b-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="3884b-122">SGN</span><span class="sxs-lookup"><span data-stu-id="3884b-122">sgn</span></span>                    |      | <span data-ttu-id="3884b-123">x</span><span class="sxs-lookup"><span data-stu-id="3884b-123">x</span></span>    | <span data-ttu-id="3884b-124">x</span><span class="sxs-lookup"><span data-stu-id="3884b-124">x</span></span>    | <span data-ttu-id="3884b-125">x</span><span class="sxs-lookup"><span data-stu-id="3884b-125">x</span></span>     | <span data-ttu-id="3884b-126">x</span><span class="sxs-lookup"><span data-stu-id="3884b-126">x</span></span>    | <span data-ttu-id="3884b-127">x</span><span class="sxs-lookup"><span data-stu-id="3884b-127">x</span></span>     |



 

<span data-ttu-id="3884b-128">Diese Anweisung funktioniert wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="3884b-128">This instruction works as shown below.</span></span>


```
for each component in src0
{
   if (src0.component < 0) 
       dest.component = -1; 
   else
       if (src0.component == 0) 
           dest.component = 0; 
       else 
           dest.component = 1;
}
```



<span data-ttu-id="3884b-129">Quelle1 und Quelle2 müssen unterschiedliche [temporäre Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3884b-129">src1 and src2 must be different [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3884b-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3884b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3884b-131">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="3884b-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




