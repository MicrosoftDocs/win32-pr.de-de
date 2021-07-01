---
title: do-Anweisung (Ocidl.h)
description: Führen Sie eine Reihe von Anweisungen kontinuierlich aus, bis der bedingte Ausdruck fehlschlägt.
ms.assetid: 07fd37b0-59c2-404b-a755-7178e4a058e4
keywords:
- do-Anweisung HLSL
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
ms.openlocfilehash: a1f019af77ef0021ad0574bf703ff2a2a52ac0f6
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118785"
---
# <a name="do-statement"></a><span data-ttu-id="b0dd2-104">do-Anweisung</span><span class="sxs-lookup"><span data-stu-id="b0dd2-104">do Statement</span></span>

<span data-ttu-id="b0dd2-105">Führen Sie eine Reihe von Anweisungen kontinuierlich aus, bis der bedingte Ausdruck fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="b0dd2-105">Execute a series of statements continuously until the conditional expression fails.</span></span>

<span data-ttu-id="b0dd2-106">\[*Attribut* \] do { *Statement Block*; } while( *Conditional* );</span><span class="sxs-lookup"><span data-stu-id="b0dd2-106">\[*Attribute*\] do {   *Statement Block*; } while( *Conditional* );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="b0dd2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0dd2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0dd2-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*</span><span class="sxs-lookup"><span data-stu-id="b0dd2-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="b0dd2-109">Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="b0dd2-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="b0dd2-110">attribute</span><span class="sxs-lookup"><span data-stu-id="b0dd2-110">Attribute</span></span> | <span data-ttu-id="b0dd2-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0dd2-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0dd2-112">fastopt</span><span class="sxs-lookup"><span data-stu-id="b0dd2-112">fastopt</span></span>   | <span data-ttu-id="b0dd2-113">Reduziert die Kompilierzeit, erzeugt jedoch weniger aggressive Optimierungen.</span><span class="sxs-lookup"><span data-stu-id="b0dd2-113">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="b0dd2-114">Wenn Sie dieses Attribut verwenden, werden die Schleifen vom Compiler nicht gerollt.</span><span class="sxs-lookup"><span data-stu-id="b0dd2-114">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="b0dd2-115">Dieses Attribut wirkt sich nur auf Shadermodellziele aus, die [Break-Anweisungen](dx-graphics-hlsl-break.md) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b0dd2-115">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="b0dd2-116">Dieses Attribut ist im Shadermodell im Vergleich [ \_ zu 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) und [Shadermodell 3 und](dx-graphics-hlsl-sm3.md) höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b0dd2-116">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="b0dd2-117">Dies ist besonders nützlich in [Shadermodell 4](dx-graphics-hlsl-sm4.md) und höher, wenn der Compiler Schleifen kompiliert.</span><span class="sxs-lookup"><span data-stu-id="b0dd2-117">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="b0dd2-118">Der Compiler simuliert standardmäßig Schleifen, um zu bewerten, ob er deren Registrierung wieder aufzeilen kann.</span><span class="sxs-lookup"><span data-stu-id="b0dd2-118">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="b0dd2-119">Wenn sie nicht möchten, dass der Compiler Schleifen aufrollt, verwenden Sie dieses Attribut, um die Kompilierzeit zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="b0dd2-119">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b0dd2-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Anweisungsblock*</span><span class="sxs-lookup"><span data-stu-id="b0dd2-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="b0dd2-121">Mindestens eine [-Anweisung.](dx-graphics-hlsl-statement-blocks.md)</span><span class="sxs-lookup"><span data-stu-id="b0dd2-121">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0dd2-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Bedingte*</span><span class="sxs-lookup"><span data-stu-id="b0dd2-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="b0dd2-123">Ein bedingter [Ausdruck.](dx-graphics-hlsl-expressions.md)</span><span class="sxs-lookup"><span data-stu-id="b0dd2-123">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="b0dd2-124">Der Anweisungsblock wird ausgeführt, bevor der Ausdruck ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="b0dd2-124">The statement block is executed before the expression is evaluated.</span></span> <span data-ttu-id="b0dd2-125">Die Schleife wird beendet, wenn der Ausdruck zu FALSE ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="b0dd2-125">The loop is exited when the expression evaluates to false.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0dd2-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b0dd2-126">Requirements</span></span>



| <span data-ttu-id="b0dd2-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0dd2-127">Requirement</span></span> | <span data-ttu-id="b0dd2-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b0dd2-128">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b0dd2-129">Header</span><span class="sxs-lookup"><span data-stu-id="b0dd2-129">Header</span></span><br/> | <dl> <span data-ttu-id="b0dd2-130"><dt>Ocidl.h</dt></span><span class="sxs-lookup"><span data-stu-id="b0dd2-130"><dt>Ocidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0dd2-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0dd2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0dd2-132">Flusssteuerung</span><span class="sxs-lookup"><span data-stu-id="b0dd2-132">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





