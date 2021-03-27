---
title: callnz bool-PS
description: Wenn nicht 0 (null). Führt einen bedingten aufrufbefehl der Anweisung aus, die durch den Bezeichnungs Index gekennzeichnet ist. | callnz bool-PS
ms.assetid: 1b9ff276-c2b8-46cc-96ac-a5b5455c5cc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0516e62ce07c60866715591bc59123f38dc5c272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995764"
---
# <a name="callnz-bool---ps"></a><span data-ttu-id="a6187-105">callnz bool-PS</span><span class="sxs-lookup"><span data-stu-id="a6187-105">callnz bool - ps</span></span>

<span data-ttu-id="a6187-106">Wenn nicht 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a6187-106">Call if not zero.</span></span> <span data-ttu-id="a6187-107">Führt einen bedingten aufrufbefehl der Anweisung aus, die durch den Bezeichnungs Index gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="a6187-107">Performs a conditional call to the instruction marked by the label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6187-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6187-108">Syntax</span></span>



| <span data-ttu-id="a6187-109">callnz l \# , \[ ! \] b\#</span><span class="sxs-lookup"><span data-stu-id="a6187-109">callnz l\#, \[!\]b\#</span></span> |
|----------------------|



 

<span data-ttu-id="a6187-110">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="a6187-110">Where:</span></span>

-   <span data-ttu-id="a6187-111">l \# ist eine [Bezeichnung-PS](label---ps.md) , die den Anfang der aufzurufenden Unterroutine markiert.</span><span class="sxs-lookup"><span data-stu-id="a6187-111">l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="a6187-112">\[!\] ist ein optionaler Negation-Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="a6187-112">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="a6187-113">b \# identifiziert ein [konstantes boolesches Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="a6187-113">b\# identifies a [Constant Boolean Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a6187-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6187-114">Remarks</span></span>



| <span data-ttu-id="a6187-115">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="a6187-115">Pixel shader versions</span></span> | <span data-ttu-id="a6187-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="a6187-116">1\_1</span></span> | <span data-ttu-id="a6187-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="a6187-117">1\_2</span></span> | <span data-ttu-id="a6187-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a6187-118">1\_3</span></span> | <span data-ttu-id="a6187-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="a6187-119">1\_4</span></span> | <span data-ttu-id="a6187-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a6187-120">2\_0</span></span> | <span data-ttu-id="a6187-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a6187-121">2\_x</span></span> | <span data-ttu-id="a6187-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a6187-122">2\_sw</span></span> | <span data-ttu-id="a6187-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a6187-123">3\_0</span></span> | <span data-ttu-id="a6187-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a6187-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a6187-125">callnz bool</span><span class="sxs-lookup"><span data-stu-id="a6187-125">callnz bool</span></span>           |      |      |      |      |      | <span data-ttu-id="a6187-126">x</span><span class="sxs-lookup"><span data-stu-id="a6187-126">x</span></span>    | <span data-ttu-id="a6187-127">x</span><span class="sxs-lookup"><span data-stu-id="a6187-127">x</span></span>     | <span data-ttu-id="a6187-128">x</span><span class="sxs-lookup"><span data-stu-id="a6187-128">x</span></span>    | <span data-ttu-id="a6187-129">x</span><span class="sxs-lookup"><span data-stu-id="a6187-129">x</span></span>     |



 

<span data-ttu-id="a6187-130">Diese Anweisung führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="a6187-130">This instruction does the following:</span></span>


```
if (specified Boolean register is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a><span data-ttu-id="a6187-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a6187-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6187-132">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="a6187-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




