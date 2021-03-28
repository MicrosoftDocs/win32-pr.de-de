---
title: while-Anweisung
description: Führt einen Anweisungsblock aus, bis der bedingte Ausdruck fehlschlägt.
ms.assetid: 0fe420db-3c09-40bd-b689-f85c02e2f817
keywords:
- While-Anweisung HLSL
topic_type:
- apiref
api_name:
- while Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 190d5474b5e016b41426db67a0c96d98787f79ff
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037856"
---
# <a name="while-statement"></a><span data-ttu-id="51769-104">while-Anweisung</span><span class="sxs-lookup"><span data-stu-id="51769-104">while Statement</span></span>

<span data-ttu-id="51769-105">Führt einen Anweisungsblock aus, bis der bedingte Ausdruck fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="51769-105">Executes a statement block until the conditional expression fails.</span></span>



|                                                                  |
|------------------------------------------------------------------|
| <span data-ttu-id="51769-106">\[*Attribut* \] while ( *Conditional* ) { *Statement Block*;}</span><span class="sxs-lookup"><span data-stu-id="51769-106">\[*Attribute*\] while ( *Conditional* ) {   *Statement Block*; }</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="51769-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="51769-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51769-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Versehen*</span><span class="sxs-lookup"><span data-stu-id="51769-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="51769-109">Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="51769-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="51769-110">attribute</span><span class="sxs-lookup"><span data-stu-id="51769-110">Attribute</span></span>             | <span data-ttu-id="51769-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51769-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51769-112">Aufheben der Registrierung (x)</span><span class="sxs-lookup"><span data-stu-id="51769-112">unroll(x)</span></span>             | <span data-ttu-id="51769-113">Entsperren Sie die Schleife, bis die Ausführung beendet ist.</span><span class="sxs-lookup"><span data-stu-id="51769-113">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="51769-114">Optional können Sie angeben, wie oft die Schleife maximal ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="51769-114">Optionally, you can specify the maximum number of times the loop can execute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="51769-115">loop</span><span class="sxs-lookup"><span data-stu-id="51769-115">loop</span></span>                  | <span data-ttu-id="51769-116">Verwenden von Fluss Steuerungs Anweisungen im kompilierten Shader; Heben Sie die rollforwardschleife nicht auf.</span><span class="sxs-lookup"><span data-stu-id="51769-116">Use flow-control statements in the compiled shader; do not unroll the loop.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="51769-117">fastopt</span><span class="sxs-lookup"><span data-stu-id="51769-117">fastopt</span></span>               | <span data-ttu-id="51769-118">Verringert die Kompilierzeit, erzeugt jedoch weniger aggressive Optimierungen.</span><span class="sxs-lookup"><span data-stu-id="51769-118">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="51769-119">Wenn Sie dieses Attribut verwenden, entlädt der Compiler keine Schleifen.</span><span class="sxs-lookup"><span data-stu-id="51769-119">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="51769-120">Dieses Attribut wirkt sich nur auf shadermodellziele aus, die [unterbrechungsanweisungen](dx-graphics-hlsl-break.md) unterstützen</span><span class="sxs-lookup"><span data-stu-id="51769-120">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="51769-121">Dieses Attribut ist im Shader-Modell [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) und [Shader Model 3](dx-graphics-hlsl-sm3.md) und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="51769-121">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="51769-122">Dies ist besonders nützlich, [](dx-graphics-hlsl-sm4.md) wenn der Compiler Schleifen kompiliert.</span><span class="sxs-lookup"><span data-stu-id="51769-122">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="51769-123">Der Compiler simuliert standardmäßig Schleifen, um auszuwerten, ob er die Registrierung aufheben kann.</span><span class="sxs-lookup"><span data-stu-id="51769-123">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="51769-124">Verwenden Sie dieses Attribut, um die Kompilierzeit zu verkürzen, wenn der Compiler keine Schleifen aufheben soll.</span><span class="sxs-lookup"><span data-stu-id="51769-124">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |
| <span data-ttu-id="51769-125">\_UAV- \_ Bedingung zulassen</span><span class="sxs-lookup"><span data-stu-id="51769-125">allow\_uav\_condition</span></span> | <span data-ttu-id="51769-126">Ermöglicht, dass die Beendigungs Bedingung einer COMPUTE-Shader-Schleife auf einem UAV-Lesevorgang basiert.</span><span class="sxs-lookup"><span data-stu-id="51769-126">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="51769-127">Die Schleife darf keine systeminternen Synchronisierungs Funktionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="51769-127">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="51769-128"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span><span class="sxs-lookup"><span data-stu-id="51769-128"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="51769-129">Ein bedingter [Ausdruck](dx-graphics-hlsl-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="51769-129">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="51769-130">Wenn der Ausdruck als "true" ausgewertet wird, wird der Anweisungsblock ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51769-130">If the expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="51769-131">Die Schleife endet, wenn der Ausdruck zu false ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="51769-131">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="51769-132"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Anweisungs Block*</span><span class="sxs-lookup"><span data-stu-id="51769-132"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="51769-133">Eine oder mehrere- [Anweisungen](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="51769-133">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="51769-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="51769-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51769-135">Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="51769-135">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





