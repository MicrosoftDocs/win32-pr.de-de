---
title: Rep-vs
description: Rep starten... ENDREP-Block.
ms.assetid: vs|directx_sdk|~\rep___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5441d5d134ee2d60e14db9f273ec374323f93902
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389524"
---
# <a name="rep---vs"></a><span data-ttu-id="5b503-103">Rep-vs</span><span class="sxs-lookup"><span data-stu-id="5b503-103">rep - vs</span></span>

<span data-ttu-id="5b503-104">Rep starten... [ENDREP](endrep---vs.md) -Block.</span><span class="sxs-lookup"><span data-stu-id="5b503-104">Start a rep...[endrep](endrep---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b503-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b503-105">Syntax</span></span>



| <span data-ttu-id="5b503-106">Rep i\#</span><span class="sxs-lookup"><span data-stu-id="5b503-106">rep i\#</span></span> |
|---------|



 

<span data-ttu-id="5b503-107">\#dabei handelt es sich um ein ganzzahliges Register, das die Wiederholungs Anzahl in der. x-Komponente angibt.</span><span class="sxs-lookup"><span data-stu-id="5b503-107">where i\# is an integer register that specifies the repeat count in the .x component.</span></span> <span data-ttu-id="5b503-108">Siehe [konstanter ganzzahliges Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="5b503-108">See [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5b503-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b503-109">Remarks</span></span>



| <span data-ttu-id="5b503-110">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="5b503-110">Vertex shader versions</span></span> | <span data-ttu-id="5b503-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="5b503-111">1\_1</span></span> | <span data-ttu-id="5b503-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5b503-112">2\_0</span></span> | <span data-ttu-id="5b503-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5b503-113">2\_x</span></span> | <span data-ttu-id="5b503-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5b503-114">2\_sw</span></span> | <span data-ttu-id="5b503-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5b503-115">3\_0</span></span> | <span data-ttu-id="5b503-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5b503-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5b503-117">Sprecherin</span><span class="sxs-lookup"><span data-stu-id="5b503-117">rep</span></span>                    |      | <span data-ttu-id="5b503-118">x</span><span class="sxs-lookup"><span data-stu-id="5b503-118">x</span></span>    | <span data-ttu-id="5b503-119">x</span><span class="sxs-lookup"><span data-stu-id="5b503-119">x</span></span>    | <span data-ttu-id="5b503-120">x</span><span class="sxs-lookup"><span data-stu-id="5b503-120">x</span></span>     | <span data-ttu-id="5b503-121">x</span><span class="sxs-lookup"><span data-stu-id="5b503-121">x</span></span>    | <span data-ttu-id="5b503-122">x</span><span class="sxs-lookup"><span data-stu-id="5b503-122">x</span></span>     |



 

-   <span data-ttu-id="5b503-123">i \# . x gibt die Iterations Anzahl an.</span><span class="sxs-lookup"><span data-stu-id="5b503-123">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="5b503-124">Der zulässige Bereich ist \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="5b503-124">The legal range is \[0, 255\].</span></span> <span data-ttu-id="5b503-125">Beachten Sie, dass diese Anweisung den Wert von i. x nicht Inkrement oder Dekrement erhöht \# .</span><span class="sxs-lookup"><span data-stu-id="5b503-125">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="5b503-126">i \# . yzw wird nicht vom Wiederholungs Block verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b503-126">i\#.yzw are not used by the repeat block.</span></span>
-   <span data-ttu-id="5b503-127">Wiederholungs Blöcke können eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="5b503-127">Repeat blocks may be nested.</span></span> <span data-ttu-id="5b503-128">Siehe Schachtelungs [Limits der Fluss Steuerung](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="5b503-128">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="5b503-129">Wiederholungs Blöcke dürfen sich entweder vollständig innerhalb eines if- \* Blocks oder vollständig umschließen.</span><span class="sxs-lookup"><span data-stu-id="5b503-129">Repeat blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="5b503-130">Es sind keine überspannen zulässig.</span><span class="sxs-lookup"><span data-stu-id="5b503-130">No straddling is allowed.</span></span>
-   <span data-ttu-id="5b503-131">Die Verwendung desselben i \# -Codes für verschiedene oder schllige Rep-Anweisungen ist in Ordnung. jede Schleife wird basierend auf der angegebenen Anzahl durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="5b503-131">Using the same i\# for different or nested rep instructions is fine - each loop will iterate based on the specified count.</span></span>

## <a name="example"></a><span data-ttu-id="5b503-132">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5b503-132">Example</span></span>


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a><span data-ttu-id="5b503-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5b503-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b503-134">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="5b503-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




