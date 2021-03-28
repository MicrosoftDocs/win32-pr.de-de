---
title: Do-Anweisung (ocidl. h)
description: Führen Sie eine Reihe von Anweisungen kontinuierlich aus, bis der bedingte Ausdruck fehlschlägt.
ms.assetid: 07fd37b0-59c2-404b-a755-7178e4a058e4
keywords:
- Do-Anweisung HLSL
topic_type:
- apiref
api_name:
- do Statement
api_location:
- ocidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46c0ced3c9747f0bfbdf01847b21350a45b68aa6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219503"
---
# <a name="do-statement"></a><span data-ttu-id="b999b-104">Do-Anweisung</span><span class="sxs-lookup"><span data-stu-id="b999b-104">do Statement</span></span>

<span data-ttu-id="b999b-105">Führen Sie eine Reihe von Anweisungen kontinuierlich aus, bis der bedingte Ausdruck fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="b999b-105">Execute a series of statements continuously until the conditional expression fails.</span></span>



|                                                                     |
|---------------------------------------------------------------------|
| <span data-ttu-id="b999b-106">\[*Attribut* \] Do { *Statement Block*;} while ( *bedingt* );</span><span class="sxs-lookup"><span data-stu-id="b999b-106">\[*Attribute*\] do {   *Statement Block*; } while( *Conditional* );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="b999b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b999b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b999b-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Versehen*</span><span class="sxs-lookup"><span data-stu-id="b999b-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="b999b-109">Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="b999b-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="b999b-110">attribute</span><span class="sxs-lookup"><span data-stu-id="b999b-110">Attribute</span></span> | <span data-ttu-id="b999b-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b999b-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b999b-112">fastopt</span><span class="sxs-lookup"><span data-stu-id="b999b-112">fastopt</span></span>   | <span data-ttu-id="b999b-113">Verringert die Kompilierzeit, erzeugt jedoch weniger aggressive Optimierungen.</span><span class="sxs-lookup"><span data-stu-id="b999b-113">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="b999b-114">Wenn Sie dieses Attribut verwenden, entlädt der Compiler keine Schleifen.</span><span class="sxs-lookup"><span data-stu-id="b999b-114">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="b999b-115">Dieses Attribut wirkt sich nur auf shadermodellziele aus, die [unterbrechungsanweisungen](dx-graphics-hlsl-break.md) unterstützen</span><span class="sxs-lookup"><span data-stu-id="b999b-115">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="b999b-116">Dieses Attribut ist im Shader-Modell [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) und [Shader Model 3](dx-graphics-hlsl-sm3.md) und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b999b-116">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="b999b-117">Dies ist besonders nützlich, [](dx-graphics-hlsl-sm4.md) wenn der Compiler Schleifen kompiliert.</span><span class="sxs-lookup"><span data-stu-id="b999b-117">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="b999b-118">Der Compiler simuliert standardmäßig Schleifen, um auszuwerten, ob er die Registrierung aufheben kann.</span><span class="sxs-lookup"><span data-stu-id="b999b-118">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="b999b-119">Verwenden Sie dieses Attribut, um die Kompilierzeit zu verkürzen, wenn der Compiler keine Schleifen aufheben soll.</span><span class="sxs-lookup"><span data-stu-id="b999b-119">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b999b-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Anweisungs Block*</span><span class="sxs-lookup"><span data-stu-id="b999b-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="b999b-121">Eine oder mehrere- [Anweisungen](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="b999b-121">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> <dt>

<span data-ttu-id="b999b-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span><span class="sxs-lookup"><span data-stu-id="b999b-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="b999b-123">Ein bedingter [Ausdruck](dx-graphics-hlsl-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="b999b-123">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="b999b-124">Der Anweisungsblock wird ausgeführt, bevor der Ausdruck ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="b999b-124">The statement block is executed before the expression is evaluated.</span></span> <span data-ttu-id="b999b-125">Die Schleife wird beendet, wenn der Ausdruck zu false ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="b999b-125">The loop is exited when the expression evaluates to false.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b999b-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b999b-126">Requirements</span></span>



| <span data-ttu-id="b999b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b999b-127">Requirement</span></span> | <span data-ttu-id="b999b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b999b-128">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b999b-129">Header</span><span class="sxs-lookup"><span data-stu-id="b999b-129">Header</span></span><br/> | <dl> <span data-ttu-id="b999b-130"><dt>"Ocidl. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b999b-130"><dt>Ocidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b999b-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b999b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b999b-132">Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="b999b-132">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





