---
title: Schleifen-vs
description: Schleife starten... ENDLOOP-Block.
ms.assetid: vs|directx_sdk|~\loop___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6a96a1ce53b850ec8feeba282055e8111b275bfd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993110"
---
# <a name="loop---vs"></a><span data-ttu-id="5559c-103">Schleifen-vs</span><span class="sxs-lookup"><span data-stu-id="5559c-103">loop - vs</span></span>

<span data-ttu-id="5559c-104">Schleife starten... [ENDLOOP](endloop---vs.md) -Block.</span><span class="sxs-lookup"><span data-stu-id="5559c-104">Start a loop...[endloop](endloop---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="5559c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5559c-105">Syntax</span></span>



| <span data-ttu-id="5559c-106">Schleife Al, i\#</span><span class="sxs-lookup"><span data-stu-id="5559c-106">loop aL, i\#</span></span> |
|--------------|



 

<span data-ttu-id="5559c-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="5559c-107">Where:</span></span>

-   <span data-ttu-id="5559c-108">Al ist das [Schleifen Zähler Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) , das die aktuelle Schleifen Anzahl enthält.</span><span class="sxs-lookup"><span data-stu-id="5559c-108">aL is the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) holding the current loop count.</span></span>
-   <span data-ttu-id="5559c-109">Ich bin \# ein [konstantes ganzzahliges Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="5559c-109">i\# is a [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span></span> <span data-ttu-id="5559c-110">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="5559c-110">See remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="5559c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5559c-111">Remarks</span></span>



| <span data-ttu-id="5559c-112">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="5559c-112">Vertex shader versions</span></span> | <span data-ttu-id="5559c-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="5559c-113">1\_1</span></span> | <span data-ttu-id="5559c-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5559c-114">2\_0</span></span> | <span data-ttu-id="5559c-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5559c-115">2\_x</span></span> | <span data-ttu-id="5559c-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5559c-116">2\_sw</span></span> | <span data-ttu-id="5559c-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5559c-117">3\_0</span></span> | <span data-ttu-id="5559c-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5559c-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5559c-119">loop</span><span class="sxs-lookup"><span data-stu-id="5559c-119">loop</span></span>                   |      | <span data-ttu-id="5559c-120">x</span><span class="sxs-lookup"><span data-stu-id="5559c-120">x</span></span>    | <span data-ttu-id="5559c-121">x</span><span class="sxs-lookup"><span data-stu-id="5559c-121">x</span></span>    | <span data-ttu-id="5559c-122">x</span><span class="sxs-lookup"><span data-stu-id="5559c-122">x</span></span>     | <span data-ttu-id="5559c-123">x</span><span class="sxs-lookup"><span data-stu-id="5559c-123">x</span></span>    | <span data-ttu-id="5559c-124">x</span><span class="sxs-lookup"><span data-stu-id="5559c-124">x</span></span>     |



 

-   <span data-ttu-id="5559c-125">Das [Schleifen Zähler Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) enthält die aktuelle Schleifen Anzahl und kann für die relative Adressierung in [Konstanten integerregister](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (c \# ) oder [Ausgabe Registern](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) im Schleifen Block verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5559c-125">The [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) holds the current loop count, and can be used for relative addressing into [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (c\#) or [Output Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#) inside the loop block.</span></span>
-   <span data-ttu-id="5559c-126">i \# . x gibt die Iterations Anzahl an.</span><span class="sxs-lookup"><span data-stu-id="5559c-126">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="5559c-127">Der zulässige Bereich ist \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="5559c-127">The legal range is \[0, 255\].</span></span> <span data-ttu-id="5559c-128">Beachten Sie, dass diese Anweisung den Wert von i. x nicht Inkrement oder Dekrement erhöht \# .</span><span class="sxs-lookup"><span data-stu-id="5559c-128">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="5559c-129">i \# . y gibt den Anfangswert des Register für das [Schleifen Leistungs Zähl Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) an.</span><span class="sxs-lookup"><span data-stu-id="5559c-129">i\#.y specifies the initial value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) register.</span></span> <span data-ttu-id="5559c-130">Der zulässige Bereich ist \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="5559c-130">The legal range is \[0, 255\].</span></span> <span data-ttu-id="5559c-131">Beachten Sie, dass diese Anweisung den Wert von i. y nicht Inkrement oder Dekrement erhöht \# .</span><span class="sxs-lookup"><span data-stu-id="5559c-131">Note that this instruction does not increment or decrement the value of i\#.y.</span></span>
-   <span data-ttu-id="5559c-132">i \# . z gibt die Schritt-/Schritt-Größe an.</span><span class="sxs-lookup"><span data-stu-id="5559c-132">i\#.z specifies the step/stride size.</span></span> <span data-ttu-id="5559c-133">Der zulässige Bereich ist \[ -128, 127 \] .</span><span class="sxs-lookup"><span data-stu-id="5559c-133">The legal range is \[-128, 127\].</span></span>
-   <span data-ttu-id="5559c-134">i \# . w wird nicht verwendet und muss auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5559c-134">i\#.w is not used and must be set to 0.</span></span>
-   <span data-ttu-id="5559c-135">Schleifen Blöcke können eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="5559c-135">Loop blocks may be nested.</span></span> <span data-ttu-id="5559c-136">Siehe Schachtelungs [Limits der Fluss Steuerung](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="5559c-136">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="5559c-137">Beim Einfügen bezieht sich der Wert des [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) auf den unmittelbar einschließenden Schleifen Block.</span><span class="sxs-lookup"><span data-stu-id="5559c-137">When nested, the value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) refers to the immediate enclosing loop block.</span></span>
-   <span data-ttu-id="5559c-138">Schleifen Blöcke dürfen sich entweder vollständig innerhalb eines if- \* Blocks oder vollständig umschließen.</span><span class="sxs-lookup"><span data-stu-id="5559c-138">Loop blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="5559c-139">Es sind keine überspannen zulässig.</span><span class="sxs-lookup"><span data-stu-id="5559c-139">No straddling is allowed.</span></span>

## <a name="example"></a><span data-ttu-id="5559c-140">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5559c-140">Example</span></span>


```
loop aL, i3
    add r1, r0, c2[aL]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="5559c-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5559c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5559c-142">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="5559c-142">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




