---
title: callnz bool-vs
description: Wenn nicht 0 (null). Führt einen bedingten aufrufbefehl der Anweisung aus, die durch den Bezeichnungs Index gekennzeichnet ist. | callnz bool-vs
ms.assetid: 9be030b9-fa21-459f-bd6c-f34ad6f177fc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3932f4c5d50445b3220a0460a5c434a1ff8aae4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995763"
---
# <a name="callnz-bool---vs"></a><span data-ttu-id="e11dd-105">callnz bool-vs</span><span class="sxs-lookup"><span data-stu-id="e11dd-105">callnz bool - vs</span></span>

<span data-ttu-id="e11dd-106">Wenn nicht 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e11dd-106">Call if not zero.</span></span> <span data-ttu-id="e11dd-107">Führt einen bedingten aufrufbefehl der Anweisung aus, die durch den Bezeichnungs Index gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="e11dd-107">Performs a conditional call to the instruction marked by the label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e11dd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e11dd-108">Syntax</span></span>



| <span data-ttu-id="e11dd-109">callnz l \# , \[ ! \] b\#</span><span class="sxs-lookup"><span data-stu-id="e11dd-109">callnz l\#, \[!\]b\#</span></span> |
|----------------------|



 

<span data-ttu-id="e11dd-110">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="e11dd-110">where:</span></span>

-   <span data-ttu-id="e11dd-111">Where l \# ist eine [Bezeichnung-vs](label---vs.md) , die den Anfang der aufzurufenden Unterroutine kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e11dd-111">where l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="e11dd-112">\[!\] der optionale boolesche not-Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="e11dd-112">\[!\] is the optional boolean NOT modifier.</span></span>
-   <span data-ttu-id="e11dd-113">b \# identifiziert ein [konstantes boolesches Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="e11dd-113">b\# identifies a [Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e11dd-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e11dd-114">Remarks</span></span>



| <span data-ttu-id="e11dd-115">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="e11dd-115">Vertex shader versions</span></span> | <span data-ttu-id="e11dd-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="e11dd-116">1\_1</span></span> | <span data-ttu-id="e11dd-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e11dd-117">2\_0</span></span> | <span data-ttu-id="e11dd-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e11dd-118">2\_x</span></span> | <span data-ttu-id="e11dd-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e11dd-119">2\_sw</span></span> | <span data-ttu-id="e11dd-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e11dd-120">3\_0</span></span> | <span data-ttu-id="e11dd-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e11dd-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="e11dd-122">callnz bool</span><span class="sxs-lookup"><span data-stu-id="e11dd-122">callnz bool</span></span>            |      | <span data-ttu-id="e11dd-123">x</span><span class="sxs-lookup"><span data-stu-id="e11dd-123">x</span></span>    | <span data-ttu-id="e11dd-124">x</span><span class="sxs-lookup"><span data-stu-id="e11dd-124">x</span></span>    | <span data-ttu-id="e11dd-125">x</span><span class="sxs-lookup"><span data-stu-id="e11dd-125">x</span></span>     | <span data-ttu-id="e11dd-126">x</span><span class="sxs-lookup"><span data-stu-id="e11dd-126">x</span></span>    | <span data-ttu-id="e11dd-127">x</span><span class="sxs-lookup"><span data-stu-id="e11dd-127">x</span></span>     |



 

<span data-ttu-id="e11dd-128">Diese Anweisung führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="e11dd-128">This instruction does the following:</span></span>


```
if (specified boolean register is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



<span data-ttu-id="e11dd-129">Diese Anweisung verwendet einen Vertex-Shader-Anweisungs Slot.</span><span class="sxs-lookup"><span data-stu-id="e11dd-129">This instruction consumes one vertex shader instruction slot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e11dd-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e11dd-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e11dd-131">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="e11dd-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




