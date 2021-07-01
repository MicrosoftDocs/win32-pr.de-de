---
title: for-Anweisung
description: Führt basierend auf der Auswertung des bedingten Ausdrucks iterativ eine Reihe von Anweisungen aus.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- for Statement HLSL
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cbcf06f28a327e18aa9f31b417dc1911411d0c9
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119076"
---
# <a name="for-statement"></a><span data-ttu-id="754f8-104">for-Anweisung</span><span class="sxs-lookup"><span data-stu-id="754f8-104">for Statement</span></span>

<span data-ttu-id="754f8-105">Führt basierend auf der Auswertung des bedingten Ausdrucks iterativ eine Reihe von Anweisungen aus.</span><span class="sxs-lookup"><span data-stu-id="754f8-105">Iteratively executes a series of statements, based on the evaluation of the conditional expression.</span></span>

<span data-ttu-id="754f8-106">\[*Attribut* \] for ( *Initialisierer; Bedingt; Iterator* ) { *Anweisungsblock*; }</span><span class="sxs-lookup"><span data-stu-id="754f8-106">\[*Attribute*\] for ( *Initializer; Conditional; Iterator* ) {   *Statement Block*; }</span></span>



 

## <a name="parameters"></a><span data-ttu-id="754f8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="754f8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="754f8-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*</span><span class="sxs-lookup"><span data-stu-id="754f8-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="754f8-109">Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="754f8-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="754f8-110">Wenn kein Attribut angegeben wird, versucht der Compiler zunächst, eine rollierte Version der Schleife auszugeben. Wenn dies fehlschlägt oder einige Vorgänge einfacher wären, wenn die Schleife nicht ausgeführt wurde, wird auf eine nichtrollierte Version der Schleife zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="754f8-110">When no attribute is specified the compiler will first attempt to emit a rolled version of the loop, and if that fails, or if some operations would be easier if the loop was unrolled, will fall back to an unrolled version of the loop.</span></span>



| <span data-ttu-id="754f8-111">attribute</span><span class="sxs-lookup"><span data-stu-id="754f8-111">Attribute</span></span>             | <span data-ttu-id="754f8-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="754f8-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="754f8-113">unroll(x)</span><span class="sxs-lookup"><span data-stu-id="754f8-113">unroll(x)</span></span>             | <span data-ttu-id="754f8-114">Entrollt die Schleife, bis sie nicht mehr ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="754f8-114">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="754f8-115">Kann optional angeben, wie oft die Schleife maximal ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="754f8-115">Can optionally specify the maximum number of times the loop is to execute.</span></span> <span data-ttu-id="754f8-116">Nicht kompatibel mit dem **\[ \]** Schleifenattribut.</span><span class="sxs-lookup"><span data-stu-id="754f8-116">Not compatible with the **\[loop\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="754f8-117">loop</span><span class="sxs-lookup"><span data-stu-id="754f8-117">loop</span></span>                  | <span data-ttu-id="754f8-118">Generieren Sie Code, der die Flusssteuerung verwendet, um jede Iteration der Schleife auszuführen.</span><span class="sxs-lookup"><span data-stu-id="754f8-118">Generate code that uses flow control to execute each iteration of the loop.</span></span> <span data-ttu-id="754f8-119">Nicht kompatibel mit dem **\[ \] Unroll-Attribut.**</span><span class="sxs-lookup"><span data-stu-id="754f8-119">Not compatible with the **\[unroll\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="754f8-120">fastopt</span><span class="sxs-lookup"><span data-stu-id="754f8-120">fastopt</span></span>               | <span data-ttu-id="754f8-121">Reduziert die Kompilierzeit, erzeugt aber weniger aggressive Optimierungen.</span><span class="sxs-lookup"><span data-stu-id="754f8-121">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="754f8-122">Wenn Sie dieses Attribut verwenden, wird der Compiler die Registrierung von Schleifen nicht aufheben.</span><span class="sxs-lookup"><span data-stu-id="754f8-122">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="754f8-123">Dieses Attribut wirkt sich nur auf Shadermodellziele aus, die [Unterbrechungsanweisungen](dx-graphics-hlsl-break.md) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="754f8-123">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="754f8-124">Dieses Attribut ist im Shadermodell [im Vergleich \_ zu 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) und [im Shadermodell 3](dx-graphics-hlsl-sm3.md) und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="754f8-124">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="754f8-125">Dies ist besonders nützlich im [Shadermodell 4](dx-graphics-hlsl-sm4.md) und höher, wenn der Compiler Schleifen kompiliert.</span><span class="sxs-lookup"><span data-stu-id="754f8-125">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="754f8-126">Der Compiler simuliert standardmäßig Schleifen, um auszuwerten, ob die Registrierung aufheben werden kann.</span><span class="sxs-lookup"><span data-stu-id="754f8-126">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="754f8-127">Wenn der Compiler die Registrierung von Schleifen nicht aufheben soll, verwenden Sie dieses Attribut, um die Kompilierzeit zu verkürzen.</span><span class="sxs-lookup"><span data-stu-id="754f8-127">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span> <br/> |
| <span data-ttu-id="754f8-128">\_UAV-Bedingung zulassen \_</span><span class="sxs-lookup"><span data-stu-id="754f8-128">allow\_uav\_condition</span></span> | <span data-ttu-id="754f8-129">Ermöglicht, dass die Beendigungsbedingung einer Compute-Shaderschleife auf einem UAV-Lesezustand basiert.</span><span class="sxs-lookup"><span data-stu-id="754f8-129">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="754f8-130">Die Schleife darf keine systeminternen Synchronisierungsfunktionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="754f8-130">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="754f8-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Initialisierung*</span><span class="sxs-lookup"><span data-stu-id="754f8-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Initializer*</span></span>
</dt> <dd>

<span data-ttu-id="754f8-132">Der Anfangswert des Schleifenzählers.</span><span class="sxs-lookup"><span data-stu-id="754f8-132">The initial value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="754f8-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Bedingte*</span><span class="sxs-lookup"><span data-stu-id="754f8-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="754f8-134">Ein bedingter [Ausdruck.](dx-graphics-hlsl-expressions.md)</span><span class="sxs-lookup"><span data-stu-id="754f8-134">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="754f8-135">Wenn der bedingte Ausdruck als TRUE ausgewertet wird, wird der Anweisungsblock ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="754f8-135">If the conditional expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="754f8-136">Die Schleife endet, wenn der Ausdruck als FALSE ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="754f8-136">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="754f8-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterator*</span><span class="sxs-lookup"><span data-stu-id="754f8-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterator*</span></span>
</dt> <dd>

<span data-ttu-id="754f8-138">Aktualisieren Sie den Wert des Schleifenzählers.</span><span class="sxs-lookup"><span data-stu-id="754f8-138">Update the value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="754f8-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Anweisungsblock*</span><span class="sxs-lookup"><span data-stu-id="754f8-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="754f8-140">Eine oder mehrere [HLSL-Anweisungen.](dx-graphics-hlsl-statement-blocks.md)</span><span class="sxs-lookup"><span data-stu-id="754f8-140">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="754f8-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="754f8-141">Remarks</span></span>

<span data-ttu-id="754f8-142">Die **\[ Unroll- \]** und **\[ Schleifenattribute \]** schließen sich gegenseitig aus und generieren Compilerfehler, wenn beide angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="754f8-142">The **\[unroll\]** and **\[loop\]** attributes are mutually exclusive and will generate compiler errors when both are specified.</span></span>

<span data-ttu-id="754f8-143">Die Attribute **\[ fastopt \]** und **\[ allow \_ uav \_ condition \]** werden ignoriert, wenn die **\[ Registrierung \]** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="754f8-143">The **\[fastopt\]** and **\[allow\_uav\_condition\]** attributes are ignored if **\[unroll\]** is specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="754f8-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="754f8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="754f8-145">Flusssteuerung</span><span class="sxs-lookup"><span data-stu-id="754f8-145">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





