---
title: for-Anweisung
description: Führt iterativ eine Reihe von-Anweisungen basierend auf der Auswertung des bedingten Ausdrucks aus.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- für Anweisungs-HLSL
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50f8c18ebc23455563b4b3e6bfee72bfa9d3ec4c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100890"
---
# <a name="for-statement"></a><span data-ttu-id="07e85-104">for-Anweisung</span><span class="sxs-lookup"><span data-stu-id="07e85-104">for Statement</span></span>

<span data-ttu-id="07e85-105">Führt iterativ eine Reihe von-Anweisungen basierend auf der Auswertung des bedingten Ausdrucks aus.</span><span class="sxs-lookup"><span data-stu-id="07e85-105">Iteratively executes a series of statements, based on the evaluation of the conditional expression.</span></span>



|                                                                                       |
|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07e85-106">\[*Attribut* \] for ( *Initialisierer; Conditional Iterator* ) { *Anweisungs Block*;}</span><span class="sxs-lookup"><span data-stu-id="07e85-106">\[*Attribute*\] for ( *Initializer; Conditional; Iterator* ) {   *Statement Block*; }</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="07e85-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="07e85-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07e85-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Versehen*</span><span class="sxs-lookup"><span data-stu-id="07e85-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="07e85-109">Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="07e85-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="07e85-110">Wenn kein Attribut angegeben wird, versucht der Compiler zunächst, eine gerollerte Version der Schleife auszugeben. wenn dies nicht der Fall ist, oder wenn bei der Ausführung der Schleife ein Fehler auftritt, wird auf eine nicht rollende Version der Schleife zurückgegriffen.</span><span class="sxs-lookup"><span data-stu-id="07e85-110">When no attribute is specified the compiler will first attempt to emit a rolled version of the loop, and if that fails, or if some operations would be easier if the loop was unrolled, will fall back to an unrolled version of the loop.</span></span>



| <span data-ttu-id="07e85-111">attribute</span><span class="sxs-lookup"><span data-stu-id="07e85-111">Attribute</span></span>             | <span data-ttu-id="07e85-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07e85-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07e85-113">Aufheben der Registrierung (x)</span><span class="sxs-lookup"><span data-stu-id="07e85-113">unroll(x)</span></span>             | <span data-ttu-id="07e85-114">Entsperren Sie die Schleife, bis die Ausführung beendet ist.</span><span class="sxs-lookup"><span data-stu-id="07e85-114">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="07e85-115">Optional können Sie angeben, wie oft die Schleife maximal ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="07e85-115">Can optionally specify the maximum number of times the loop is to execute.</span></span> <span data-ttu-id="07e85-116">Nicht kompatibel mit dem **\[ Schleifen \]** Attribut.</span><span class="sxs-lookup"><span data-stu-id="07e85-116">Not compatible with the **\[loop\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="07e85-117">loop</span><span class="sxs-lookup"><span data-stu-id="07e85-117">loop</span></span>                  | <span data-ttu-id="07e85-118">Generieren Sie Code, der die Fluss Steuerung verwendet, um jede Iterations Schleife auszuführen.</span><span class="sxs-lookup"><span data-stu-id="07e85-118">Generate code that uses flow control to execute each iteration of the loop.</span></span> <span data-ttu-id="07e85-119">Nicht kompatibel mit dem Attribut " **\[ Auflösen \]** ".</span><span class="sxs-lookup"><span data-stu-id="07e85-119">Not compatible with the **\[unroll\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="07e85-120">fastopt</span><span class="sxs-lookup"><span data-stu-id="07e85-120">fastopt</span></span>               | <span data-ttu-id="07e85-121">Verringert die Kompilierzeit, erzeugt jedoch weniger aggressive Optimierungen.</span><span class="sxs-lookup"><span data-stu-id="07e85-121">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="07e85-122">Wenn Sie dieses Attribut verwenden, entlädt der Compiler keine Schleifen.</span><span class="sxs-lookup"><span data-stu-id="07e85-122">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="07e85-123">Dieses Attribut wirkt sich nur auf shadermodellziele aus, die [unterbrechungsanweisungen](dx-graphics-hlsl-break.md) unterstützen</span><span class="sxs-lookup"><span data-stu-id="07e85-123">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="07e85-124">Dieses Attribut ist im Shader-Modell [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) und [Shader Model 3](dx-graphics-hlsl-sm3.md) und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="07e85-124">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="07e85-125">Dies ist besonders nützlich, [](dx-graphics-hlsl-sm4.md) wenn der Compiler Schleifen kompiliert.</span><span class="sxs-lookup"><span data-stu-id="07e85-125">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="07e85-126">Der Compiler simuliert standardmäßig Schleifen, um auszuwerten, ob er die Registrierung aufheben kann.</span><span class="sxs-lookup"><span data-stu-id="07e85-126">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="07e85-127">Verwenden Sie dieses Attribut, um die Kompilierzeit zu verkürzen, wenn der Compiler keine Schleifen aufheben soll.</span><span class="sxs-lookup"><span data-stu-id="07e85-127">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span> <br/> |
| <span data-ttu-id="07e85-128">\_UAV- \_ Bedingung zulassen</span><span class="sxs-lookup"><span data-stu-id="07e85-128">allow\_uav\_condition</span></span> | <span data-ttu-id="07e85-129">Ermöglicht, dass die Beendigungs Bedingung einer COMPUTE-Shader-Schleife auf einem UAV-Lesevorgang basiert.</span><span class="sxs-lookup"><span data-stu-id="07e85-129">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="07e85-130">Die Schleife darf keine systeminternen Synchronisierungs Funktionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="07e85-130">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="07e85-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Initialisierer*</span><span class="sxs-lookup"><span data-stu-id="07e85-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Initializer*</span></span>
</dt> <dd>

<span data-ttu-id="07e85-132">Der Anfangswert des Schleifenzählers.</span><span class="sxs-lookup"><span data-stu-id="07e85-132">The initial value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="07e85-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span><span class="sxs-lookup"><span data-stu-id="07e85-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="07e85-134">Ein bedingter [Ausdruck](dx-graphics-hlsl-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="07e85-134">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="07e85-135">Wenn für den bedingten Ausdruck true ausgewertet wird, wird der Anweisungsblock ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07e85-135">If the conditional expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="07e85-136">Die Schleife endet, wenn der Ausdruck zu false ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="07e85-136">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="07e85-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterator*</span><span class="sxs-lookup"><span data-stu-id="07e85-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterator*</span></span>
</dt> <dd>

<span data-ttu-id="07e85-138">Aktualisieren Sie den Wert des Schleifen Zählers.</span><span class="sxs-lookup"><span data-stu-id="07e85-138">Update the value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="07e85-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Anweisungs Block*</span><span class="sxs-lookup"><span data-stu-id="07e85-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="07e85-140">Mindestens eine [HLSL-Anweisung](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="07e85-140">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07e85-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07e85-141">Remarks</span></span>

<span data-ttu-id="07e85-142">Die Attribute " **\[ Auflösen \]** " und " **\[ Loop \]** " schließen sich gegenseitig aus und generieren Compilerfehler, wenn beide angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="07e85-142">The **\[unroll\]** and **\[loop\]** attributes are mutually exclusive and will generate compiler errors when both are specified.</span></span>

<span data-ttu-id="07e85-143">Die Attribute **\[ fastopt \]** und **\[ \_ UAV \_ - \]** **\[ \]** Bedingung zulassen werden ignoriert, wenn die Option zum Aufheben der Registrierung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="07e85-143">The **\[fastopt\]** and **\[allow\_uav\_condition\]** attributes are ignored if **\[unroll\]** is specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="07e85-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="07e85-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07e85-145">Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="07e85-145">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





