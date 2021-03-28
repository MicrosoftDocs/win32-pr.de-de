---
title: Anweisungsmodifiziererer (HLSL vs-Referenz)
description: Anweisungs Modifizierer
ms.assetid: b713d847-c858-4492-918c-7a105f751624
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 573f2ef618c4cd29092fb38fb4c805bdeeecc219
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104472076"
---
# <a name="instruction-modifiers-hlsl-vs-reference"></a><span data-ttu-id="69be4-103">Anweisungsmodifiziererer (HLSL vs-Referenz)</span><span class="sxs-lookup"><span data-stu-id="69be4-103">Instruction modifiers (HLSL VS reference)</span></span>

<span data-ttu-id="69be4-104">Anweisungsmodifiziererer wirken sich auf das Ergebnis der Anweisung aus, bevor Sie in das Ziel Register geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="69be4-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

## <a name="_sat"></a><span data-ttu-id="69be4-105">\_gesetzt</span><span class="sxs-lookup"><span data-stu-id="69be4-105">\_sat</span></span>

<span data-ttu-id="69be4-106">Füllt das Anweisungs Ergebnis (oder bindet es) \[ \] vor dem Schreiben in das Ziel Register in 0, 1 Bereich.</span><span class="sxs-lookup"><span data-stu-id="69be4-106">Saturates (or clamps) the instruction result to \[0,1\] range before writing to the destination register.</span></span>

<span data-ttu-id="69be4-107">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="69be4-107">For example:</span></span>


```
add_sat dst, src0, src1
```



<span data-ttu-id="69be4-108">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="69be4-108">Where:</span></span>

<span data-ttu-id="69be4-109">DST = Klammer \_ zwischen \_ 0 \_ und \_ 1 (src0 + Quelle1)</span><span class="sxs-lookup"><span data-stu-id="69be4-109">dst = clamp\_between\_0\_and\_1(src0 + src1)</span></span>

<span data-ttu-id="69be4-110">Der \_ Sat-Anweisungs Modifizierer kostet keine zusätzlichen Anweisungs Slots.</span><span class="sxs-lookup"><span data-stu-id="69be4-110">The \_sat instruction modifier costs no additional instruction slots.</span></span>

<span data-ttu-id="69be4-111">Wenn unterstützt, \_ kann der Sat-anweisungsmodifizierer mit einer beliebigen Anweisung verwendet werden, mit Ausnahme von: [FRC-vs](frc---vs.md), [SinCos-vs](sincos---vs.md)und [texldl-vs](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="69be4-111">If supported, the \_sat instruction modifier can be used with any instruction except: [frc - vs](frc---vs.md), [sincos - vs](sincos---vs.md), and [texldl - vs](texldl---vs.md).</span></span>



| <span data-ttu-id="69be4-112">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="69be4-112">Vertex shader versions</span></span> | <span data-ttu-id="69be4-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="69be4-113">1\_1</span></span> | <span data-ttu-id="69be4-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="69be4-114">2\_0</span></span> | <span data-ttu-id="69be4-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="69be4-115">2\_x</span></span> | <span data-ttu-id="69be4-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="69be4-116">2\_sw</span></span> | <span data-ttu-id="69be4-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="69be4-117">3\_0</span></span> | <span data-ttu-id="69be4-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="69be4-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="69be4-119">\_gesetzt</span><span class="sxs-lookup"><span data-stu-id="69be4-119">\_sat</span></span>                  |      |      |      |       | <span data-ttu-id="69be4-120">x</span><span class="sxs-lookup"><span data-stu-id="69be4-120">x</span></span>    | <span data-ttu-id="69be4-121">x</span><span class="sxs-lookup"><span data-stu-id="69be4-121">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="69be4-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="69be4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69be4-123">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="69be4-123">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




