---
title: while-Anweisung
description: Führt einen Anweisungsblock aus, bis der bedingte Ausdruck fehlschlägt.
ms.assetid: 0fe420db-3c09-40bd-b689-f85c02e2f817
keywords:
- while Statement HLSL
topic_type:
- apiref
api_name:
- while Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bf1f0049ac474e7840753a8cfe05c972aa346c1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826673"
---
# <a name="while-statement"></a><span data-ttu-id="57426-104">while-Anweisung</span><span class="sxs-lookup"><span data-stu-id="57426-104">while Statement</span></span>

<span data-ttu-id="57426-105">Führt einen Anweisungsblock aus, bis der bedingte Ausdruck fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="57426-105">Executes a statement block until the conditional expression fails.</span></span>

<span data-ttu-id="57426-106">\[*Attribut* \] while ( *Conditional* ) { *Statement Block*; }</span><span class="sxs-lookup"><span data-stu-id="57426-106">\[*Attribute*\] while ( *Conditional* ) {   *Statement Block*; }</span></span>



 

## <a name="parameters"></a><span data-ttu-id="57426-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="57426-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57426-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*</span><span class="sxs-lookup"><span data-stu-id="57426-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="57426-109">Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="57426-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="57426-110">attribute</span><span class="sxs-lookup"><span data-stu-id="57426-110">Attribute</span></span>             | <span data-ttu-id="57426-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57426-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57426-112">unroll(x)</span><span class="sxs-lookup"><span data-stu-id="57426-112">unroll(x)</span></span>             | <span data-ttu-id="57426-113">Entrollt die Schleife, bis sie nicht mehr ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="57426-113">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="57426-114">Optional können Sie angeben, wie oft die Schleife maximal ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="57426-114">Optionally, you can specify the maximum number of times the loop can execute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="57426-115">loop</span><span class="sxs-lookup"><span data-stu-id="57426-115">loop</span></span>                  | <span data-ttu-id="57426-116">Verwenden Sie Flusssteuerungsanweisungen im kompilierten Shader. Die Schleife darf nicht entladen werden.</span><span class="sxs-lookup"><span data-stu-id="57426-116">Use flow-control statements in the compiled shader; do not unroll the loop.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="57426-117">fastopt</span><span class="sxs-lookup"><span data-stu-id="57426-117">fastopt</span></span>               | <span data-ttu-id="57426-118">Reduziert die Kompilierzeit, erzeugt aber weniger aggressive Optimierungen.</span><span class="sxs-lookup"><span data-stu-id="57426-118">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="57426-119">Wenn Sie dieses Attribut verwenden, wird der Compiler die Registrierung von Schleifen nicht aufheben.</span><span class="sxs-lookup"><span data-stu-id="57426-119">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="57426-120">Dieses Attribut wirkt sich nur auf Shadermodellziele aus, die [Unterbrechungsanweisungen](dx-graphics-hlsl-break.md) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="57426-120">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="57426-121">Dieses Attribut ist im Shadermodell [im Vergleich \_ zu 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) und [im Shadermodell 3](dx-graphics-hlsl-sm3.md) und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="57426-121">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="57426-122">Dies ist besonders nützlich in [Shadermodell 4](dx-graphics-hlsl-sm4.md) und höher, wenn der Compiler Schleifen kompiliert.</span><span class="sxs-lookup"><span data-stu-id="57426-122">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="57426-123">Der Compiler simuliert standardmäßig Schleifen, um zu bewerten, ob sie die Registrierung aufheben können.</span><span class="sxs-lookup"><span data-stu-id="57426-123">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="57426-124">Wenn der Compiler die Registrierung von Schleifen nicht aufheben soll, verwenden Sie dieses Attribut, um die Kompilierzeit zu verkürzen.</span><span class="sxs-lookup"><span data-stu-id="57426-124">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |
| <span data-ttu-id="57426-125">\_UAV-Bedingung zulassen \_</span><span class="sxs-lookup"><span data-stu-id="57426-125">allow\_uav\_condition</span></span> | <span data-ttu-id="57426-126">Ermöglicht, dass die Beendigungsbedingung einer Compute-Shaderschleife auf einem UAV-Lesezustand basiert.</span><span class="sxs-lookup"><span data-stu-id="57426-126">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="57426-127">Die Schleife darf keine systeminternen Synchronisierungsfunktionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="57426-127">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="57426-128"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Bedingte*</span><span class="sxs-lookup"><span data-stu-id="57426-128"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="57426-129">Ein bedingter [Ausdruck.](dx-graphics-hlsl-expressions.md)</span><span class="sxs-lookup"><span data-stu-id="57426-129">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="57426-130">Wenn der Ausdruck als TRUE ausgewertet wird, wird der Anweisungsblock ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="57426-130">If the expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="57426-131">Die Schleife endet, wenn der Ausdruck als FALSE ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="57426-131">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="57426-132"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Anweisungsblock*</span><span class="sxs-lookup"><span data-stu-id="57426-132"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="57426-133">Mindestens eine [-Anweisungen.](dx-graphics-hlsl-statement-blocks.md)</span><span class="sxs-lookup"><span data-stu-id="57426-133">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="57426-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57426-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57426-135">Flusssteuerung</span><span class="sxs-lookup"><span data-stu-id="57426-135">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





