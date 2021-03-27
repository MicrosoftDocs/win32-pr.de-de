---
title: Rep-PS
description: Rep starten... ENDREP-PS-Block.
ms.assetid: vs|directx_sdk|~\rep___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6873a6aee9e31b1f28ba2755b1869cddb177306
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719386"
---
# <a name="rep---ps"></a><span data-ttu-id="d45a1-103">Rep-PS</span><span class="sxs-lookup"><span data-stu-id="d45a1-103">rep - ps</span></span>

<span data-ttu-id="d45a1-104">Rep starten... [ENDREP-PS-](endrep---ps.md) Block.</span><span class="sxs-lookup"><span data-stu-id="d45a1-104">Start a rep...[endrep - ps](endrep---ps.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="d45a1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d45a1-105">Syntax</span></span>



| <span data-ttu-id="d45a1-106">Rep i\#</span><span class="sxs-lookup"><span data-stu-id="d45a1-106">rep i\#</span></span> |
|---------|



 

<span data-ttu-id="d45a1-107">\#dabei handelt es sich um ein ganzzahliges Register, das die Wiederholungs Anzahl in der. x-Komponente angibt.</span><span class="sxs-lookup"><span data-stu-id="d45a1-107">where i\# is an integer register that specifies the repeat count in the .x component.</span></span> <span data-ttu-id="d45a1-108">Siehe [konstanter ganzzahliges Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="d45a1-108">See [Constant Integer Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d45a1-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d45a1-109">Remarks</span></span>



| <span data-ttu-id="d45a1-110">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="d45a1-110">Pixel shader versions</span></span> | <span data-ttu-id="d45a1-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="d45a1-111">1\_1</span></span> | <span data-ttu-id="d45a1-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="d45a1-112">1\_2</span></span> | <span data-ttu-id="d45a1-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="d45a1-113">1\_3</span></span> | <span data-ttu-id="d45a1-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="d45a1-114">1\_4</span></span> | <span data-ttu-id="d45a1-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d45a1-115">2\_0</span></span> | <span data-ttu-id="d45a1-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d45a1-116">2\_x</span></span> | <span data-ttu-id="d45a1-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d45a1-117">2\_sw</span></span> | <span data-ttu-id="d45a1-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d45a1-118">3\_0</span></span> | <span data-ttu-id="d45a1-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d45a1-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="d45a1-120">Sprecherin</span><span class="sxs-lookup"><span data-stu-id="d45a1-120">rep</span></span>                   |      |      |      |      |      | <span data-ttu-id="d45a1-121">x</span><span class="sxs-lookup"><span data-stu-id="d45a1-121">x</span></span>    | <span data-ttu-id="d45a1-122">x</span><span class="sxs-lookup"><span data-stu-id="d45a1-122">x</span></span>     | <span data-ttu-id="d45a1-123">x</span><span class="sxs-lookup"><span data-stu-id="d45a1-123">x</span></span>    | <span data-ttu-id="d45a1-124">x</span><span class="sxs-lookup"><span data-stu-id="d45a1-124">x</span></span>     |



 

-   <span data-ttu-id="d45a1-125">i \# . x gibt die Iterations Anzahl an.</span><span class="sxs-lookup"><span data-stu-id="d45a1-125">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="d45a1-126">Der zulässige Bereich ist \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="d45a1-126">The legal range is \[0, 255\].</span></span> <span data-ttu-id="d45a1-127">Beachten Sie, dass diese Anweisung den Wert von i. x nicht Inkrement oder Dekrement erhöht \# .</span><span class="sxs-lookup"><span data-stu-id="d45a1-127">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="d45a1-128">i \# . yzw wird nicht vom Wiederholungs Block verwendet.</span><span class="sxs-lookup"><span data-stu-id="d45a1-128">i\#.yzw are not used by the repeat block.</span></span>
-   <span data-ttu-id="d45a1-129">Wiederholungs Blöcke können eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="d45a1-129">Repeat blocks may be nested.</span></span> <span data-ttu-id="d45a1-130">Siehe [Fluss Steuerungs Einschränkungen](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="d45a1-130">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="d45a1-131">Wiederholungs Blöcke dürfen sich entweder vollständig innerhalb eines if- \* Blocks oder vollständig umschließen.</span><span class="sxs-lookup"><span data-stu-id="d45a1-131">Repeat blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="d45a1-132">Es sind keine überspannen zulässig.</span><span class="sxs-lookup"><span data-stu-id="d45a1-132">No straddling is allowed.</span></span>
-   <span data-ttu-id="d45a1-133">Die Verwendung desselben i \# -Codes für verschiedene oder schllige Rep-Anweisungen ist in Ordnung. jede Schleife wird basierend auf der angegebenen Anzahl durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="d45a1-133">Using the same i\# for different or nested rep instructions is fine - each loop will iterate based on the specified count.</span></span>

## <a name="example"></a><span data-ttu-id="d45a1-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d45a1-134">Example</span></span>


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a><span data-ttu-id="d45a1-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d45a1-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d45a1-136">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="d45a1-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




