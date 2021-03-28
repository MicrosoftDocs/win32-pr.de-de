---
title: if-Anweisung
description: Führen Sie bedingt eine Reihe von-Anweisungen basierend auf der Auswertung des bedingten Ausdrucks aus.
ms.assetid: ed4e347b-b5ee-40bc-a3f8-36e83ccf45b8
keywords:
- if-Anweisung HLSL
topic_type:
- apiref
api_name:
- if Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e8a3c20e73b9783d39b4f4cbdb7c0be5b75fcda
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104038490"
---
# <a name="if-statement"></a><span data-ttu-id="16e6e-104">if-Anweisung</span><span class="sxs-lookup"><span data-stu-id="16e6e-104">if Statement</span></span>

<span data-ttu-id="16e6e-105">Führen Sie bedingt eine Reihe von-Anweisungen basierend auf der Auswertung des bedingten Ausdrucks aus.</span><span class="sxs-lookup"><span data-stu-id="16e6e-105">Conditionally execute a series of statements, based on the evaluation of the conditional expression.</span></span>



|                                                               |
|---------------------------------------------------------------|
| <span data-ttu-id="16e6e-106">\[*Attribut* \] if ( *Conditional* ) { *Statement Block*;}</span><span class="sxs-lookup"><span data-stu-id="16e6e-106">\[*Attribute*\] if ( *Conditional* ) {   *Statement Block*; }</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="16e6e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="16e6e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16e6e-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Versehen*</span><span class="sxs-lookup"><span data-stu-id="16e6e-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="16e6e-109">Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="16e6e-109">An optional parameter that controls how the statement is compiled.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="16e6e-110">attribute</span><span class="sxs-lookup"><span data-stu-id="16e6e-110">Attribute</span></span></th>
<th><span data-ttu-id="16e6e-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16e6e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="16e6e-112">Verzweigung</span><span class="sxs-lookup"><span data-stu-id="16e6e-112">branch</span></span></td>
<td><span data-ttu-id="16e6e-113">Wertet nur eine Seite der if-Anweisung aus, abhängig von der angegebenen Bedingung.</span><span class="sxs-lookup"><span data-stu-id="16e6e-113">Evaluate only one side of the if statement depending on the given condition.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="16e6e-114">Wenn Sie das <a href="dx-graphics-hlsl-sm2.md">Shadermodell 2. x</a> oder das <a href="dx-graphics-hlsl-sm3.md">Shader-Modell 3,0</a>verwenden, verwenden Sie jedes Mal, wenn Sie dynamische Verzweigungen verwenden, Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="16e6e-114">When you use <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> or <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, each time you use dynamic branching you consume resources.</span></span> <span data-ttu-id="16e6e-115">Wenn Sie also die dynamische Verzweigung übermäßig verwenden, wenn Sie diese Profile als Ziel verwenden, können Sie Kompilierungsfehler erhalten.</span><span class="sxs-lookup"><span data-stu-id="16e6e-115">So, if you use dynamic branching excessively when you target these profiles, you can receive compilation errors.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16e6e-116">Vereinfachen</span><span class="sxs-lookup"><span data-stu-id="16e6e-116">flatten</span></span></td>
<td><span data-ttu-id="16e6e-117">Evaluieren Sie beide Seiten der if-Anweisung, und wählen Sie zwischen den beiden resultierenden Werten aus.</span><span class="sxs-lookup"><span data-stu-id="16e6e-117">Evaluate both sides of the if statement and choose between the two resulting values.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="16e6e-118"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span><span class="sxs-lookup"><span data-stu-id="16e6e-118"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="16e6e-119">Ein bedingter [Ausdruck](dx-graphics-hlsl-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="16e6e-119">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="16e6e-120">Der Ausdruck wird ausgewertet, und wenn true, wird der Anweisungsblock ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16e6e-120">The expression is evaluated, and if true, the statement block is executed.</span></span>

</dd> <dt>

<span data-ttu-id="16e6e-121"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Anweisungs Block*</span><span class="sxs-lookup"><span data-stu-id="16e6e-121"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="16e6e-122">Mindestens eine [HLSL-Anweisung](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="16e6e-122">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16e6e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16e6e-123">Remarks</span></span>

<span data-ttu-id="16e6e-124">Wenn der Compiler die branchmethode zum Kompilieren einer if-Anweisung verwendet, wird Code generiert, der die Auswertung einer Seite der if-Anweisung abhängig von der angegebenen Bedingung durchführt.</span><span class="sxs-lookup"><span data-stu-id="16e6e-124">When the compiler uses the branch method for compiling an if statement it will generate code that will evaluate only one side of the if statement depending on the given condition.</span></span> <span data-ttu-id="16e6e-125">Beispielsweise in der if-Anweisung:</span><span class="sxs-lookup"><span data-stu-id="16e6e-125">For example, in the if statement:</span></span>


```
[branch] if(x)
{
    x = sqrt(x);
}
```



<span data-ttu-id="16e6e-126">Die **if** -Anweisung verfügt über einen impliziten Else-Block, der x = x entspricht.</span><span class="sxs-lookup"><span data-stu-id="16e6e-126">The **if** statement has an implicit else block, which is equivalent to x = x.</span></span> <span data-ttu-id="16e6e-127">Da der Compiler die branchmethode mit dem vorangehenden Verzweigungs Attribut verwendet hat, wertet der kompilierte Code x aus und führt nur die Seite aus, die ausgeführt werden soll. Wenn x 0 (null) ist, wird die **else** -Seite ausgeführt, und wenn Sie ungleich NULL ist, wird die Seite **dann** ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16e6e-127">Because we have told the compiler to use the branch method with the preceding branch attribute, the compiled code will evaluate x and execute only the side that should be executed; if x is zero, then it will execute the **else** side, and if it is non-zero it will execute the **then** side.</span></span>

<span data-ttu-id="16e6e-128">Wenn das **vereinfachen** -Attribut verwendet wird, wertet der kompilierte Code beide Seiten der **if** -Anweisung aus und wählt zwischen den beiden resultierenden Werten aus, wobei der ursprüngliche Wert von x verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="16e6e-128">Conversely, if the **flatten** attribute is used, then the compiled code will evaluate both sides of the **if** statement and choose between the two resulting values using the original value of x.</span></span> <span data-ttu-id="16e6e-129">Im folgenden finden Sie ein Beispiel für die Verwendung des vereinfachen-Attributs:</span><span class="sxs-lookup"><span data-stu-id="16e6e-129">Here is an example of a usage of the flatten attribute:</span></span>


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



<span data-ttu-id="16e6e-130">Es gibt bestimmte Fälle, in denen die Verwendung der Verzweigungen oder der vereinfachen Attribute einen Kompilierungsfehler erzeugen kann.</span><span class="sxs-lookup"><span data-stu-id="16e6e-130">There are certain cases where using the branch or flatten attributes may generate a compile error.</span></span> <span data-ttu-id="16e6e-131">Das Branch-Attribut schlägt möglicherweise fehl, wenn eine Seite der if-Anweisung eine Farbverlaufs Funktion enthält, z. b. [**tex2D**](dx-graphics-hlsl-tex2d.md).</span><span class="sxs-lookup"><span data-stu-id="16e6e-131">The branch attribute may fail if either side of the if statement contains a gradient function, such as [**tex2D**](dx-graphics-hlsl-tex2d.md).</span></span> <span data-ttu-id="16e6e-132">Beim vereinfachen-Attribut tritt möglicherweise ein Fehler auf, wenn beide Seiten der if-Anweisung eine Stream anfügen-Anweisung oder eine andere Anweisung mit Nebeneffekten enthalten.</span><span class="sxs-lookup"><span data-stu-id="16e6e-132">The flatten attribute may fail if either side of the if statement contains a stream append statement or any other statement that has side-effects.</span></span>

<span data-ttu-id="16e6e-133">Eine **if** -Anweisung kann auch einen optionalen Else-Block verwenden.</span><span class="sxs-lookup"><span data-stu-id="16e6e-133">An **if** statement can also use an optional else block.</span></span> <span data-ttu-id="16e6e-134">Wenn der **if** -Ausdruck true ist, wird der Code im Anweisungsblock verarbeitet, der der if-Anweisung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="16e6e-134">If the **if** expression is true, the code in the statement block associated with the if statement is processed.</span></span> <span data-ttu-id="16e6e-135">Andernfalls wird der dem optionalen Else-Block zugeordnete Anweisungsblock verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="16e6e-135">Otherwise, the statement block associated with the optional else block is processed.</span></span>

## <a name="see-also"></a><span data-ttu-id="16e6e-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="16e6e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16e6e-137">Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="16e6e-137">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





