---
title: Wenn bool-PS
description: Beginn eines If-Blocks.
ms.assetid: cff53072-1c73-4cf8-9ecd-11032a9c4bbb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92c3158a09aeb871ef367133c07278b0f3b87390
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719355"
---
# <a name="if-bool---ps"></a><span data-ttu-id="72840-103">Wenn bool-PS</span><span class="sxs-lookup"><span data-stu-id="72840-103">if bool - ps</span></span>

<span data-ttu-id="72840-104">Beginn eines If-Blocks.</span><span class="sxs-lookup"><span data-stu-id="72840-104">Start of an if block.</span></span>

## <a name="syntax"></a><span data-ttu-id="72840-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="72840-105">Syntax</span></span>



| <span data-ttu-id="72840-106">Wenn bool</span><span class="sxs-lookup"><span data-stu-id="72840-106">if bool</span></span> |
|---------|



 

<span data-ttu-id="72840-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="72840-107">Where:</span></span>

-   <span data-ttu-id="72840-108">bool ist eine boolesche (Boolean) Registernummer.</span><span class="sxs-lookup"><span data-stu-id="72840-108">bool is a bool (Boolean) register number.</span></span> <span data-ttu-id="72840-109">Siehe [konstantes boolesches Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="72840-109">See [Constant Boolean Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="72840-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72840-110">Remarks</span></span>



| <span data-ttu-id="72840-111">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="72840-111">Pixel shader versions</span></span> | <span data-ttu-id="72840-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="72840-112">1\_1</span></span> | <span data-ttu-id="72840-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="72840-113">1\_2</span></span> | <span data-ttu-id="72840-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="72840-114">1\_3</span></span> | <span data-ttu-id="72840-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="72840-115">1\_4</span></span> | <span data-ttu-id="72840-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="72840-116">2\_0</span></span> | <span data-ttu-id="72840-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="72840-117">2\_x</span></span> | <span data-ttu-id="72840-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="72840-118">2\_sw</span></span> | <span data-ttu-id="72840-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="72840-119">3\_0</span></span> | <span data-ttu-id="72840-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="72840-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="72840-121">Wenn bool</span><span class="sxs-lookup"><span data-stu-id="72840-121">if bool</span></span>               |      |      |      |      |      | <span data-ttu-id="72840-122">x</span><span class="sxs-lookup"><span data-stu-id="72840-122">x</span></span>    | <span data-ttu-id="72840-123">x</span><span class="sxs-lookup"><span data-stu-id="72840-123">x</span></span>     | <span data-ttu-id="72840-124">x</span><span class="sxs-lookup"><span data-stu-id="72840-124">x</span></span>    | <span data-ttu-id="72840-125">x</span><span class="sxs-lookup"><span data-stu-id="72840-125">x</span></span>     |



 

<span data-ttu-id="72840-126">Wenn das boolesche Quell Konto in der if-Anweisung den Wert true hat, wird der Code, der von der if-Anweisung und der entsprechenden [EndIf-PS](endif---ps.md) oder [else-PS](else---ps.md) eingeschlossen wird, ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72840-126">If the source Boolean register in the if statement is true, the code enclosed by the if statement and the matching [endif - ps](endif---ps.md) or [else - ps](else---ps.md) is executed.</span></span> <span data-ttu-id="72840-127">Andernfalls wird der Code, der von der Else-PS... EndIf-PS-Anweisungen werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72840-127">Otherwise, the code enclosed by the else - ps...endif - ps statements is executed.</span></span> <span data-ttu-id="72840-128">Diese Anweisung verwendet einen Anweisungs Slot.</span><span class="sxs-lookup"><span data-stu-id="72840-128">This instruction consumes one instruction slot.</span></span>

<span data-ttu-id="72840-129">Ein If-Block kann eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="72840-129">An if block can be nested.</span></span>

<span data-ttu-id="72840-130">Ein If-Block kann einen Schleifen Block nicht verspannen.</span><span class="sxs-lookup"><span data-stu-id="72840-130">An if block cannot straddle a loop block.</span></span>

<span data-ttu-id="72840-131">Auf einen If-Block kann ein Anweisungsblock und/oder eine [else-PS](else---ps.md) -Anweisung und/oder eine [EndIf-PS-](endif---ps.md) Anweisung folgen.</span><span class="sxs-lookup"><span data-stu-id="72840-131">An if block can be followed by a statement block, and/or an [else - ps](else---ps.md) instruction, and/or an [endif - ps](endif---ps.md) instruction.</span></span>

## <a name="example"></a><span data-ttu-id="72840-132">Beispiel</span><span class="sxs-lookup"><span data-stu-id="72840-132">Example</span></span>

<span data-ttu-id="72840-133">Diese Anweisung stellt bedingte statische Fluss Steuerung bereit.</span><span class="sxs-lookup"><span data-stu-id="72840-133">This instruction provides conditional static flow control.</span></span>


```
defb b3, true

if b3
// Instructions to run if b3 is nonzero
else
// Instructions to run otherwise
endif
```



## <a name="related-topics"></a><span data-ttu-id="72840-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="72840-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72840-135">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="72840-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="72840-136">Else-PS</span><span class="sxs-lookup"><span data-stu-id="72840-136">else - ps</span></span>](else---ps.md)
</dt> <dt>

[<span data-ttu-id="72840-137">in-PS-PS</span><span class="sxs-lookup"><span data-stu-id="72840-137">endif - ps</span></span>](endif---ps.md)
</dt> </dl>

 

 




