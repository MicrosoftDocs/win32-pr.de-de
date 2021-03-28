---
title: Schleife-PS
description: Startet eine Schleife... ENDLOOP-PS-Block.
ms.assetid: vs|directx_sdk|~\loop___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cf4c71641003d460e9752dcf33f983c70a82e4f6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038340"
---
# <a name="loop---ps"></a><span data-ttu-id="eea31-103">Schleife-PS</span><span class="sxs-lookup"><span data-stu-id="eea31-103">loop - ps</span></span>

<span data-ttu-id="eea31-104">Startet eine Schleife... [ENDLOOP-PS-](endloop---ps.md) Block.</span><span class="sxs-lookup"><span data-stu-id="eea31-104">Starts a loop...[endloop - ps](endloop---ps.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="eea31-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eea31-105">Syntax</span></span>



| <span data-ttu-id="eea31-106">Schleife Al, i\#</span><span class="sxs-lookup"><span data-stu-id="eea31-106">loop aL, i\#</span></span> |
|--------------|



 

<span data-ttu-id="eea31-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="eea31-107">Where:</span></span>

-   <span data-ttu-id="eea31-108">Al ist das [Schleifen Zähler Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) , das die aktuelle Schleifen Anzahl enthält.</span><span class="sxs-lookup"><span data-stu-id="eea31-108">aL is the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) holding the current loop count.</span></span>
-   <span data-ttu-id="eea31-109">Ich bin \# ein [konstantes ganzzahliges Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="eea31-109">i\# is a [Constant Integer Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span></span> <span data-ttu-id="eea31-110">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="eea31-110">See remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="eea31-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eea31-111">Remarks</span></span>



| <span data-ttu-id="eea31-112">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="eea31-112">Pixel shader versions</span></span> | <span data-ttu-id="eea31-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="eea31-113">1\_1</span></span> | <span data-ttu-id="eea31-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="eea31-114">1\_2</span></span> | <span data-ttu-id="eea31-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="eea31-115">1\_3</span></span> | <span data-ttu-id="eea31-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="eea31-116">1\_4</span></span> | <span data-ttu-id="eea31-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="eea31-117">2\_0</span></span> | <span data-ttu-id="eea31-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="eea31-118">2\_x</span></span> | <span data-ttu-id="eea31-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="eea31-119">2\_sw</span></span> | <span data-ttu-id="eea31-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="eea31-120">3\_0</span></span> | <span data-ttu-id="eea31-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="eea31-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="eea31-122">loop</span><span class="sxs-lookup"><span data-stu-id="eea31-122">loop</span></span>                  |      |      |      |      |      |      |       | <span data-ttu-id="eea31-123">x</span><span class="sxs-lookup"><span data-stu-id="eea31-123">x</span></span>    | <span data-ttu-id="eea31-124">x</span><span class="sxs-lookup"><span data-stu-id="eea31-124">x</span></span>     |



 

-   <span data-ttu-id="eea31-125">Das [Schleifen Zähler Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al) enthält die aktuelle Schleifen Anzahl und kann für die relative Adressierung in ein [Eingabe Farb Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) im Schleifen Block verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eea31-125">The [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) holds the current loop count and can be used for relative addressing into [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) inside the loop block.</span></span>
-   <span data-ttu-id="eea31-126">i \# . x gibt die Iterations Anzahl an.</span><span class="sxs-lookup"><span data-stu-id="eea31-126">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="eea31-127">Der zulässige Bereich ist \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="eea31-127">The legal range is \[0, 255\].</span></span> <span data-ttu-id="eea31-128">Beachten Sie, dass diese Anweisung den Wert von i. x nicht Inkrement oder Dekrement erhöht \# .</span><span class="sxs-lookup"><span data-stu-id="eea31-128">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="eea31-129">i \# . y gibt den Anfangswert des Register für das [Schleifen Leistungs Zähl Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al) an.</span><span class="sxs-lookup"><span data-stu-id="eea31-129">i\#.y specifies the initial value of the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) register.</span></span> <span data-ttu-id="eea31-130">Der zulässige Bereich ist \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="eea31-130">The legal range is \[0, 255\].</span></span> <span data-ttu-id="eea31-131">Beachten Sie, dass diese Anweisung den Wert von i. y nicht Inkrement oder Dekrement erhöht \# .</span><span class="sxs-lookup"><span data-stu-id="eea31-131">Note that this instruction does not increment or decrement the value of i\#.y.</span></span>
-   <span data-ttu-id="eea31-132">i \# . z gibt die Schritt-/Schritt-Größe an.</span><span class="sxs-lookup"><span data-stu-id="eea31-132">i\#.z specifies the step/stride size.</span></span> <span data-ttu-id="eea31-133">Der zulässige Bereich ist \[ -128, 127 \] .</span><span class="sxs-lookup"><span data-stu-id="eea31-133">The legal range is \[-128, 127\].</span></span>
-   <span data-ttu-id="eea31-134">i \# . w wird nicht vom Schleifen Block verwendet und muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="eea31-134">i\#.w is not used by the loop block and has to be 0.</span></span>
-   <span data-ttu-id="eea31-135">Schleifen Blöcke können eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="eea31-135">Loop blocks may be nested.</span></span> <span data-ttu-id="eea31-136">Siehe [Fluss Steuerungs Einschränkungen](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="eea31-136">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="eea31-137">Beim Einfügen bezieht sich der Wert des [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al) auf den unmittelbar einschließenden Schleifen Block.</span><span class="sxs-lookup"><span data-stu-id="eea31-137">When nested, the value of the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) refers to the immediate enclosing loop block.</span></span>
-   <span data-ttu-id="eea31-138">Schleifen Blöcke dürfen sich entweder vollständig innerhalb eines if- \* Blocks oder vollständig umschließen.</span><span class="sxs-lookup"><span data-stu-id="eea31-138">Loop blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="eea31-139">Es sind keine überspannen zulässig.</span><span class="sxs-lookup"><span data-stu-id="eea31-139">No straddling is allowed.</span></span>

## <a name="example"></a><span data-ttu-id="eea31-140">Beispiel</span><span class="sxs-lookup"><span data-stu-id="eea31-140">Example</span></span>


```
loop aL, i3
    add r1, r0, v2[ aL ]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="eea31-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eea31-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eea31-142">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="eea31-142">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




