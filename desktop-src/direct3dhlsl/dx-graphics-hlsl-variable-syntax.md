---
title: Variablensyntax
description: Verwenden Sie die folgenden Syntax Regeln, um HLSL-Variablen zu deklarieren.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- extern, Variable Syntax (DirectX HLSL)
- nointerpolations, Variablen Syntax (DirectX HLSL)
- Shared, Variable Syntax (DirectX HLSL)
- groupshared, Variablen Syntax (DirectX HLSL)
- static, Variable Syntax (DirectX HLSL)
- Uniform, Variable Syntax (DirectX HLSL)
- volatile, Variable Syntax (DirectX HLSL)
- genaue Variable Syntax (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6e63bafa62a9857af678e0848c81237dcd0d585
ms.sourcegitcommit: 4e0bde7dfa48a0b60bca4a5230eb2b05be3778d3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2020
ms.locfileid: "104993646"
---
# <a name="variable-syntax"></a><span data-ttu-id="f85f3-111">Variablensyntax</span><span class="sxs-lookup"><span data-stu-id="f85f3-111">Variable Syntax</span></span>

<span data-ttu-id="f85f3-112">Verwenden Sie die folgenden Syntax Regeln, um HLSL-Variablen zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="f85f3-112">Use the following syntax rules to declare HLSL variables.</span></span>



|                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f85f3-113">\[*Speicher \_* \] \[ *Klassentyp \_ Modifizierer* \] *Typname* \[ *Index* \] \[ *: Semantik* \] \[ *: packoffset* \] \[ *: Register* \] ;    \[  \] Anmerkungen \[ *= Anfänglich \_ Wert*                    \]</span><span class="sxs-lookup"><span data-stu-id="f85f3-113">\[*Storage\_Class*\] \[*Type\_Modifier*\] *Type Name*\[*Index*\]     \[*: Semantic*\]     \[*: Packoffset*\]     \[*: Register*\];    \[*Annotations*\]     \[*= Initial\_Value*\]</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="f85f3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f85f3-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f85f3-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Speicher \_ Klasse*</span><span class="sxs-lookup"><span data-stu-id="f85f3-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Storage\_Class*</span></span> 
</dt> <dd>

<span data-ttu-id="f85f3-116">Optionale Speicherklassenmodifizierer, die dem Compiler Hinweise zum Gültigkeitsbereich und zur Lebensdauer von Variablen die modifiziererer können in beliebiger Reihenfolge angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f85f3-116">Optional storage-class modifiers that give the compiler hints about variable scope and lifetime; the modifiers can be specified in any order.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f85f3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f85f3-117">Value</span></span></th>
<th><span data-ttu-id="f85f3-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f85f3-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f85f3-119"><strong>extern</strong></span><span class="sxs-lookup"><span data-stu-id="f85f3-119"><strong>extern</strong></span></span></td>
<td><span data-ttu-id="f85f3-120">Markieren Sie eine globale Variable als externe Eingabe für den Shader. Dies ist die Standard Markierung für alle globalen Variablen.</span><span class="sxs-lookup"><span data-stu-id="f85f3-120">Mark a global variable as an external input to the shader; this is the default marking for all global variables.</span></span> <span data-ttu-id="f85f3-121">Kann nicht mit <strong>static</strong>kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="f85f3-121">Cannot be combined with <strong>static</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f85f3-122"><strong>nointerpolations</strong></span><span class="sxs-lookup"><span data-stu-id="f85f3-122"><strong>nointerpolation</strong></span></span></td>
<td><span data-ttu-id="f85f3-123">Interpolieren Sie die Ausgaben eines Vertex-Shaders nicht, bevor Sie Sie an einen PixelShader übergeben.</span><span class="sxs-lookup"><span data-stu-id="f85f3-123">Do not interpolate the outputs of a vertex shader before passing them to a pixel shader.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f85f3-124"><strong>sesten</strong></span><span class="sxs-lookup"><span data-stu-id="f85f3-124"><strong>precise</strong></span></span></td>
<td><span data-ttu-id="f85f3-125">Wenn <strong>das Schlüsselwort</strong> für eine Variable angewendet wird, werden alle Berechnungen, die für die Erstellung des Werts der Variablen verwendet werden, auf folgende Weise eingeschränkt:</span><span class="sxs-lookup"><span data-stu-id="f85f3-125">The <strong>precise</strong> keyword when applied to a variable will restrict any calculations used to produce the value assigned to that variable in the following ways:</span></span>

*   <span data-ttu-id="f85f3-126">Separate Vorgänge werden getrennt beibehalten.</span><span class="sxs-lookup"><span data-stu-id="f85f3-126">Separate operations are kept separate.</span></span> <span data-ttu-id="f85f3-127">Wenn beispielsweise eine mul und ein Hinzufügevorgang in einen Mad-Vorgang unterteilt worden wären, erzwingt <strong>präzise</strong> , dass die Vorgänge getrennt bleiben.</span><span class="sxs-lookup"><span data-stu-id="f85f3-127">For example, where a mul and add operation might have been fused into a mad operation, <strong>precise</strong> forces the operations to remain separate.</span></span> <span data-ttu-id="f85f3-128">Stattdessen müssen Sie die intrinsische Funktion "Mad" explizit verwenden.</span><span class="sxs-lookup"><span data-stu-id="f85f3-128">Instead, you must explicitly use the mad intrinsic function.</span></span>
*   <span data-ttu-id="f85f3-129">Die Reihenfolge der Vorgänge wird beibehalten.</span><span class="sxs-lookup"><span data-stu-id="f85f3-129">Order of operations are maintained.</span></span> <span data-ttu-id="f85f3-130">Wenn die Reihenfolge der Anweisungen zum Verbessern der Leistung gemischt wurde, stellt <strong>präzise</strong> sicher, dass der Compiler die Bestellung wie geschrieben beibehält.</span><span class="sxs-lookup"><span data-stu-id="f85f3-130">Where the order of instructions might have been shuffled to improve performance, <strong>precise</strong> ensures that the compiler preserves the order as written.</span></span>
*   <span data-ttu-id="f85f3-131">Unsichere IEEE-Vorgänge sind eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="f85f3-131">IEEE unsafe operations are restricted.</span></span> <span data-ttu-id="f85f3-132">Wenn der Compiler möglicherweise schnelle mathematische Vorgänge verwendet hat, die keine Nan-(not a Number) und INF-Werte (unendlich) berücksichtigen, erzwingt <strong>präzise</strong> die IEEE-Anforderungen bezüglich der Nan-und INF-Werte, die beachtet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f85f3-132">Where the compiler might have used fast math operations that don't account for NaN (not a number) and INF (infinite) values, <strong>precise</strong> forces IEEE requirements concerning NaN and INF values to be respected.</span></span> <span data-ttu-id="f85f3-133">Ohne <strong>genaue</strong>Sicherheit sind diese Optimierungen und mathematischen Vorgänge nicht IEEE-sicher.</span><span class="sxs-lookup"><span data-stu-id="f85f3-133">Without <strong>precise</strong>, these optimizations and mathematical operations are not IEEE safe.</span></span>
*   <span data-ttu-id="f85f3-134">Wenn Sie eine Variable <strong>genau</strong> qualifizieren, werden keine Vorgänge durchführt, die die Variable <strong>genau</strong>verwenden.</span><span class="sxs-lookup"><span data-stu-id="f85f3-134">Qualifying a variable <strong>precise</strong> doesn't make operations that use the variable <strong>precise</strong>.</span></span> <span data-ttu-id="f85f3-135">Da die <strong>genaue</strong> Verteilung nur an Vorgänge durchführt, die zu den Werten beitragen, die der <strong>exakten</strong>qualifizierten Variablen zugewiesen sind, kann das korrekte Ausführen gewünschter Berechnungen knifflig sein. Daher empfiehlt <strong>es sich,</strong> die Shader-Ausgaben <strong>genau</strong> direkt zu markieren, wenn Sie Sie deklarieren, und zwar unabhängig davon, ob es sich um ein Strukturfeld oder einen Output-Parameter handelt.</span><span class="sxs-lookup"><span data-stu-id="f85f3-135">Since <strong>precise</strong> propagates only to operations that contribute to the values that are assigned to the <strong>precise</strong>-qualified variable, correctly making desired calculations <strong>precise</strong> can be tricky, so we recommended that you mark the shader outputs <strong>precise</strong> directly where you declare them, whether that's on a structure field, or on an output parameter, or the return type of the entry function.</span></span>

<span data-ttu-id="f85f3-136">Die Möglichkeit, Optimierungen auf diese Weise zu steuern, behält die Ergebnis Invarianz für die geänderte Ausgabevariable bei, indem Optimierungen deaktiviert werden, die die endgültigen Ergebnisse aufgrund von Unterschieden in kumulierten Genauigkeits unterschieden beeinflussen können.</span><span class="sxs-lookup"><span data-stu-id="f85f3-136">The ability to control optimizations in this way maintains result invariance for the modified output variable by disabling optimizations that might affect final results due to differences in accumulated precision differences.</span></span> <span data-ttu-id="f85f3-137">Es ist nützlich, wenn Shader für Mosaik Vorgänge Wasser strenge patchnähte oder Übereinstimmungs Werte über mehrere Durchgänge beibehalten möchten.</span><span class="sxs-lookup"><span data-stu-id="f85f3-137">It is useful when you want shaders for tessellation to maintain water-tight patch seams or match depth values over multiple passes.</span></span>

<span data-ttu-id="f85f3-138">[Beispielcode](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl):</span><span class="sxs-lookup"><span data-stu-id="f85f3-138">[Sample code](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl):</span></span> 
```HLSL
matrix g_mWorldViewProjection;
void main(in float3 InPos : Position, out precise float4 OutPos : SV_Position)
{
  // operation is precise because it contributes to the precise parameter OutPos
  OutPos = mul( float4( InPos, 1.0 ), g_mWorldViewProjection );
}
```
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="f85f3-139"><strong>Genu</strong></span><span class="sxs-lookup"><span data-stu-id="f85f3-139"><strong>shared</strong></span></span></td>
<td><span data-ttu-id="f85f3-140">Markieren einer Variablen für die Freigabe zwischen Effekten Dies ist ein Hinweis für den Compiler.</span><span class="sxs-lookup"><span data-stu-id="f85f3-140">Mark a variable for sharing between effects; this is a hint to the compiler.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f85f3-141"><strong>groupshared</strong></span><span class="sxs-lookup"><span data-stu-id="f85f3-141"><strong>groupshared</strong></span></span></td>
<td><span data-ttu-id="f85f3-142">Markieren Sie eine Variable für den Thread Gruppen freigegebenen Arbeitsspeicher für Compute-Shader.</span><span class="sxs-lookup"><span data-stu-id="f85f3-142">Mark a variable for thread-group-shared memory for compute shaders.</span></span> <span data-ttu-id="f85f3-143">In d3d10 ist die maximale Gesamtgröße aller Variablen mit der groupshared-Speicher Klasse 16 KB. in D3D11 beträgt die maximale Größe 32 KB.</span><span class="sxs-lookup"><span data-stu-id="f85f3-143">In D3D10 the maximum total size of all variables with the groupshared storage class is 16kb, in D3D11 the maximum size is 32kb.</span></span> <span data-ttu-id="f85f3-144">Siehe Beispiele.</span><span class="sxs-lookup"><span data-stu-id="f85f3-144">See examples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f85f3-145"><strong>static</strong></span><span class="sxs-lookup"><span data-stu-id="f85f3-145"><strong>static</strong></span></span></td>
<td><span data-ttu-id="f85f3-146">Markieren Sie eine lokale Variable, sodass Sie einmal initialisiert wird und zwischen Funktionsaufrufen besteht.</span><span class="sxs-lookup"><span data-stu-id="f85f3-146">Mark a local variable so that it is initialized one time and persists between function calls.</span></span> <span data-ttu-id="f85f3-147">Wenn die Deklaration keinen Initialisierer enthält, wird der Wert auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f85f3-147">If the declaration does not include an initializer, the value is set to zero.</span></span> <span data-ttu-id="f85f3-148">Eine globale Variable, die als <strong>statisch</strong> gekennzeichnet ist, ist für eine Anwendung nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="f85f3-148">A global variable marked <strong>static</strong> is not visible to an application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f85f3-149"><strong>uniform-Variable</strong></span><span class="sxs-lookup"><span data-stu-id="f85f3-149"><strong>uniform</strong></span></span></td>
<td><span data-ttu-id="f85f3-150">Markieren einer Variablen, deren Daten während der Ausführung eines Shaders konstant sind (z. b. eine Material Farbe in einem Scheitelpunkt-Shader); globale Variablen werden standardmäßig als <strong>einheitlich</strong> betrachtet.</span><span class="sxs-lookup"><span data-stu-id="f85f3-150">Mark a variable whose data is constant throughout the execution of a shader (such as a material color in a vertex shader); global variables are considered <strong>uniform</strong> by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f85f3-151"><strong>volatile</strong></span><span class="sxs-lookup"><span data-stu-id="f85f3-151"><strong>volatile</strong></span></span></td>
<td><span data-ttu-id="f85f3-152">Markieren einer Variablen, die häufig geändert wird; Dies ist ein Hinweis für den Compiler.</span><span class="sxs-lookup"><span data-stu-id="f85f3-152">Mark a variable that changes frequently; this is a hint to the compiler.</span></span> <span data-ttu-id="f85f3-153">Dieser Speicherklassenmodifizierer gilt nur für eine lokale Variable.</span><span class="sxs-lookup"><span data-stu-id="f85f3-153">This storage class modifier only applies to a local variable.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f85f3-154">Der HLSL-Compiler ignoriert zurzeit diesen Speicherklassenmodifizierer.</span><span class="sxs-lookup"><span data-stu-id="f85f3-154">The HLSL compiler currently ignores this storage class modifier.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="f85f3-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*\_Typmodifizierer*</span><span class="sxs-lookup"><span data-stu-id="f85f3-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*Type\_Modifier*</span></span>
</dt> <dd>

<span data-ttu-id="f85f3-156">Optionaler Modifizierer vom Typ "Variable".</span><span class="sxs-lookup"><span data-stu-id="f85f3-156">Optional variable-type modifier.</span></span>



| <span data-ttu-id="f85f3-157">Wert</span><span class="sxs-lookup"><span data-stu-id="f85f3-157">Value</span></span>             | <span data-ttu-id="f85f3-158">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f85f3-158">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f85f3-159">**const**</span><span class="sxs-lookup"><span data-stu-id="f85f3-159">**const**</span></span>         | <span data-ttu-id="f85f3-160">Markieren Sie eine Variable, die nicht von einem Shader geändert werden kann. Daher muss Sie in der Variablen Deklaration initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f85f3-160">Mark a variable that cannot be changed by a shader, therefore, it must be initialized in the variable declaration.</span></span> <span data-ttu-id="f85f3-161">Globale Variablen werden standardmäßig als **konstant** erachtet (unterdrücken Sie dieses Verhalten, indem Sie dem Compiler das/GEC-Flag bereitstellen).</span><span class="sxs-lookup"><span data-stu-id="f85f3-161">Global variables are considered **const** by default (suppress this behavior by supplying the /Gec flag to the compiler).</span></span> |
| <span data-ttu-id="f85f3-162">**\_Hauptzeile**</span><span class="sxs-lookup"><span data-stu-id="f85f3-162">**row\_major**</span></span>    | <span data-ttu-id="f85f3-163">Markieren Sie eine Variable, die vier Komponenten in einer einzelnen Zeile speichert, sodass Sie in einem einzelnen Konstanten Register gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="f85f3-163">Mark a variable that stores four components in a single row so they can be stored in a single constant register.</span></span>                                                                                                                             |
| <span data-ttu-id="f85f3-164">**\_Haupt Spalte**</span><span class="sxs-lookup"><span data-stu-id="f85f3-164">**column\_major**</span></span> | <span data-ttu-id="f85f3-165">Markieren Sie eine Variable, die vier Komponenten in einer einzelnen Spalte speichert, um die mathematische Matrix zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="f85f3-165">Mark a variable that stores 4 components in a single column to optimize matrix math.</span></span>                                                                                                                                                         |



 

> [!Note]  
> <span data-ttu-id="f85f3-166">Wenn Sie keinen Typmodifiziererwert angeben, verwendet der Compiler die **Spalte \_ Major** als Standardwert.</span><span class="sxs-lookup"><span data-stu-id="f85f3-166">If you do not specify a type-modifier value, the compiler uses **column\_major** as the default value.</span></span>

 

</dd> <dt>

<span data-ttu-id="f85f3-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Sorte*</span><span class="sxs-lookup"><span data-stu-id="f85f3-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Type*</span></span>
</dt> <dd>

<span data-ttu-id="f85f3-168">Jeder in den [Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)aufgeführte HLSL-Typ.</span><span class="sxs-lookup"><span data-stu-id="f85f3-168">Any HLSL type listed in [Data Types (DirectX HLSL)](dx-graphics-hlsl-data-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="f85f3-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Name* \[ *Index*\]</span><span class="sxs-lookup"><span data-stu-id="f85f3-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Name*\[*Index*\]</span></span>
</dt> <dd>

<span data-ttu-id="f85f3-170">Eine ASCII-Zeichenfolge, die eine Shader-Variable eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f85f3-170">ASCII string that uniquely identifies a shader variable.</span></span> <span data-ttu-id="f85f3-171">Um ein optionales Array zu definieren, verwenden Sie den **Index** für die Array Größe, die eine positive Ganzzahl = 1 ist.</span><span class="sxs-lookup"><span data-stu-id="f85f3-171">To define an optional array, use **index** for the array size, which is a positive integer = 1.</span></span>

</dd> <dt>

<span data-ttu-id="f85f3-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Tischer*</span><span class="sxs-lookup"><span data-stu-id="f85f3-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="f85f3-173">Optionale Parameter Verwendungs Informationen, die vom Compiler verwendet werden, um shadereingaben und-Ausgaben zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="f85f3-173">Optional parameter-usage information, used by the compiler to link shader inputs and outputs.</span></span> <span data-ttu-id="f85f3-174">Es gibt mehrere vordefinierte [Semantik](dx-graphics-hlsl-semantics.md) für Scheitelpunkt-und Pixel-Shader.</span><span class="sxs-lookup"><span data-stu-id="f85f3-174">There are several predefined [semantics](dx-graphics-hlsl-semantics.md) for vertex and pixel shaders.</span></span> <span data-ttu-id="f85f3-175">Der Compiler ignoriert Semantik, es sei denn, Sie sind für eine globale Variable deklariert, oder ein Parameter, der an einen Shader übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f85f3-175">The compiler ignores semantics unless they are declared on a global variable, or a parameter passed into a shader.</span></span>

</dd> <dt>

<span data-ttu-id="f85f3-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span><span class="sxs-lookup"><span data-stu-id="f85f3-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span></span>
</dt> <dd>

<span data-ttu-id="f85f3-177">Optionales Schlüsselwort zum manuellen Packen von shaderkonstanten.</span><span class="sxs-lookup"><span data-stu-id="f85f3-177">Optional keyword for manually packing shader constants.</span></span> <span data-ttu-id="f85f3-178">Siehe [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).</span><span class="sxs-lookup"><span data-stu-id="f85f3-178">See [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).</span></span>

</dd> <dt>

<span data-ttu-id="f85f3-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Sich*</span><span class="sxs-lookup"><span data-stu-id="f85f3-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Register*</span></span>
</dt> <dd>

<span data-ttu-id="f85f3-180">Optionales Schlüsselwort zum manuellen Zuweisen einer shadervariablen zu einem bestimmten Register.</span><span class="sxs-lookup"><span data-stu-id="f85f3-180">Optional keyword for manually assigning a shader variable to a particular register.</span></span> <span data-ttu-id="f85f3-181">Weitere Informationen finden Sie unter [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).</span><span class="sxs-lookup"><span data-stu-id="f85f3-181">See [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).</span></span>

</dd> <dt>

<span data-ttu-id="f85f3-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Anmerkung (e)*</span><span class="sxs-lookup"><span data-stu-id="f85f3-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Annotation(s)*</span></span>
</dt> <dd>

<span data-ttu-id="f85f3-183">Optionale Metadaten in Form einer Zeichenfolge, die an eine globale Variable angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="f85f3-183">Optional metadata, in the form of a string, attached to a global variable.</span></span> <span data-ttu-id="f85f3-184">Eine Anmerkung wird vom Effect-Framework verwendet und von HLSL ignoriert. Ausführlichere Informationen finden Sie unter [Anmerkung-Syntax](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span><span class="sxs-lookup"><span data-stu-id="f85f3-184">An annotation is used by the effect framework and ignored by HLSL; to see more detailed syntax, see [annotation syntax](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span></span>

</dd> <dt>

<span data-ttu-id="f85f3-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*Anfangs \_ Wert*</span><span class="sxs-lookup"><span data-stu-id="f85f3-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*Initial\_Value*</span></span>
</dt> <dd>

<span data-ttu-id="f85f3-186">Optionaler Anfangswert (en); die Anzahl der Werte sollte mit der Anzahl der Komponenten im *Typ* identisch sein.</span><span class="sxs-lookup"><span data-stu-id="f85f3-186">Optional initial value(s); the number of values should match the number of components in *Type*.</span></span> <span data-ttu-id="f85f3-187">Jede globale Variable, die als **extern** gekennzeichnet ist, muss mit einem Literalwert initialisiert werden. jede Variable, die als **statisch** gekennzeichnet ist, muss mit einer-Konstante initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f85f3-187">Each global variable marked **extern** must be initialized with a literal value; each variable marked **static** must be initialized with a constant.</span></span>

<span data-ttu-id="f85f3-188">Globale Variablen, die nicht als **statisch** oder **extern** gekennzeichnet sind, werden nicht in den Shader kompiliert.</span><span class="sxs-lookup"><span data-stu-id="f85f3-188">Global variables that are not marked **static** or **extern** are not compiled into the shader.</span></span> <span data-ttu-id="f85f3-189">Der Compiler legt die Standardwerte für globale Variablen nicht automatisch fest und kann nicht in Optimierungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f85f3-189">The compiler does not automatically set default values for global variables and cannot use them in optimizations.</span></span> <span data-ttu-id="f85f3-190">Um diesen Typ globaler Variablen zu initialisieren, verwenden Sie Reflektion, um den Wert zu erhalten, und kopieren Sie dann den Wert in einen konstanten Puffer.</span><span class="sxs-lookup"><span data-stu-id="f85f3-190">To initialize this type of global variable, use reflection to get its value and then copy the value to a constant buffer.</span></span> <span data-ttu-id="f85f3-191">Beispielsweise können Sie die [**ID3D11ShaderReflection:: getvariablebyname**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) -Methode zum Aufrufen der Variablen verwenden, die [**ID3D11ShaderReflectionVariable:: getdesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) -Methode verwenden, um die Beschreibung der shadervariablen abzurufen, und den Anfangswert aus dem **DefaultValue** -Member der [**D3D11 \_ Shader- \_ Variablen \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) -Struktur erhalten.</span><span class="sxs-lookup"><span data-stu-id="f85f3-191">For example, you can use the [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) method to get the variable, use the [**ID3D11ShaderReflectionVariable::GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) method to get the shader-variable description, and get the initial value from the **DefaultValue** member of the [**D3D11\_SHADER\_VARIABLE\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) structure.</span></span> <span data-ttu-id="f85f3-192">Um den Wert in den konstanten Puffer zu kopieren, müssen Sie sicherstellen, dass der Puffer mit CPU-Schreibzugriff ([**D3D11 \_ CPU \_ Access \_ Write**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)) erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f85f3-192">To copy the value to the constant buffer, you must ensure that the buffer was created with CPU write access ([**D3D11\_CPU\_ACCESS\_WRITE**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)).</span></span> <span data-ttu-id="f85f3-193">Weitere Informationen zum Erstellen eines konstanten Puffers finden Sie unter Gewusst [wie: Erstellen eines konstanten Puffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span><span class="sxs-lookup"><span data-stu-id="f85f3-193">For more information about how to create a constant buffer, see [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="f85f3-194">Sie können auch das [Effects-Framework](../direct3d11/d3d11-graphics-programming-guide-effects.md) verwenden, um die Spiegelung automatisch zu verarbeiten und den Anfangswert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f85f3-194">You can also use the [effects framework](../direct3d11/d3d11-graphics-programming-guide-effects.md) to automatically process the reflecting and setting the initial value.</span></span> <span data-ttu-id="f85f3-195">Beispielsweise können Sie die [**ID3DX11EffectPass:: apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="f85f3-195">For example, you can use the [**ID3DX11EffectPass::Apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) method.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f85f3-196">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f85f3-196">Examples</span></span>

<span data-ttu-id="f85f3-197">Im folgenden finden Sie einige Beispiele für Shader-Variable-Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="f85f3-197">Here are several examples of shader-variable declarations.</span></span>


```
float fVar;
```




```
float4 color;
float fVar = 3.1f;

int iVar[3];

int iVar[3] = {1,2,3};

uniform float4 position : SV_POSITION; 
const float4 lightDirection = {0,0,1};
      
```



### <a name="group-shared"></a><span data-ttu-id="f85f3-198">Gruppe freigegeben</span><span class="sxs-lookup"><span data-stu-id="f85f3-198">Group Shared</span></span>

<span data-ttu-id="f85f3-199">Mit HLSL können Threads eines Compute-Shaders Werte über gemeinsam genutzten Arbeitsspeicher austauschen.</span><span class="sxs-lookup"><span data-stu-id="f85f3-199">HLSL enables threads of a compute shader to exchange values via shared memory.</span></span> <span data-ttu-id="f85f3-200">HLSL bietet Barriere, wie z. b. [**groupmemorybarrierwithgroupsync**](groupmemorybarrierwithgroupsync.md), usw., um die korrekte Reihenfolge von Lese-und Schreibvorgängen im Shader zu gewährleisten und Daten Rassen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="f85f3-200">HLSL provides barrier primitives such as [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md), and so on to ensure the correct ordering of reads and writes to shared memory in the shader and to avoid data races.</span></span>

> [!Note]  
> <span data-ttu-id="f85f3-201">Hardware führt Threads in Gruppen (Warps oder Wave-Fronts) aus, und die Sperrungs Synchronisierung kann manchmal ausgelassen werden, um die Leistung zu erhöhen, wenn nur die Synchronisierung von Threads, die derselben Gruppe angehören, korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="f85f3-201">Hardware executes threads in groups (warps or wave-fronts), and barrier synchronization can sometimes be omitted to increase performance when only synchronizing threads that belong to the same group is correct.</span></span> <span data-ttu-id="f85f3-202">Diese Auslassung wird jedoch aus folgenden Gründen dringend davon abgeraten:</span><span class="sxs-lookup"><span data-stu-id="f85f3-202">But we highly discourage this omission for these reasons:</span></span>
>
> -   <span data-ttu-id="f85f3-203">Diese Auslassung führt zu nicht portablen Code, der möglicherweise nicht auf Hardware funktioniert und auf Software-rasterizern, die in der Regel Threads in kleineren Gruppen ausführen, nicht funktioniert.</span><span class="sxs-lookup"><span data-stu-id="f85f3-203">This omission results in non-portable code, which might not work on some hardware and doesn't work on software rasterizers that typically execute threads in smaller groups.</span></span>
> -   <span data-ttu-id="f85f3-204">Die Leistungsverbesserungen, die mit dieser Unterstreichung erzielt werden können, sind im Vergleich zur Verwendung der gesamten Thread Barriere geringfügig.</span><span class="sxs-lookup"><span data-stu-id="f85f3-204">The performance improvements that you might achieve with this omission will be minor compared to using all-thread barrier.</span></span>

 

<span data-ttu-id="f85f3-205">In Direct3D 10 gibt es beim Schreiben in **groupshared** keine Synchronisierung von Threads. Dies bedeutet, dass jeder Thread auf eine einzelne Position in einem Array zum Schreiben beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="f85f3-205">In Direct3D 10 there is no synchronization of threads when writing to **groupshared**, so this means that each thread is limited to a single location in an array for writing.</span></span> <span data-ttu-id="f85f3-206">Verwenden Sie den System Wert [SV \_ groupIndex](dx-graphics-hlsl-semantics.md) , um beim Schreiben in dieses Array zu indizieren, um sicherzustellen, dass keine zwei Threads miteinander kollidieren können.</span><span class="sxs-lookup"><span data-stu-id="f85f3-206">Use the [SV\_GroupIndex](dx-graphics-hlsl-semantics.md) system value to index into this array when writing to ensure that no two threads can collide.</span></span> <span data-ttu-id="f85f3-207">Im Hinblick auf den Lesevorgang haben alle Threads Zugriff auf das gesamte Array zum Lesen.</span><span class="sxs-lookup"><span data-stu-id="f85f3-207">In terms of reading, all threads have access to the entire array for reading.</span></span>


```
struct GSData
{
    float4 Color;
    float Factor;
}

groupshared GSData data[5*5*1];

[numthreads(5,5,1)]
void main( uint index : SV_GroupIndex )
{
    data[index].Color = (float4)0;
    data[index].Factor = 2.0f;
    GroupMemoryBarrierWithGroupSync();
    ...
}
```



### <a name="packing"></a><span data-ttu-id="f85f3-208">Verpacken</span><span class="sxs-lookup"><span data-stu-id="f85f3-208">Packing</span></span>

<span data-ttu-id="f85f3-209">Pack-unter Komponenten von Vektoren und skalaren, deren Größe groß genug ist, um das Überschreiten von Register boundarys zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="f85f3-209">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundarys.</span></span> <span data-ttu-id="f85f3-210">Diese sind z. b. gültig:</span><span class="sxs-lookup"><span data-stu-id="f85f3-210">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



<span data-ttu-id="f85f3-211">Verpackungstypen können nicht gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="f85f3-211">Cannot mix packing types.</span></span>

<span data-ttu-id="f85f3-212">Wie das Register Schlüsselwort kann ein packoffset als Ziel spezifisch festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f85f3-212">Like the register keyword, a packoffset can be target specific.</span></span> <span data-ttu-id="f85f3-213">Die unter Komponenten Verpackung ist nur mit dem packoffset-Schlüsselwort, nicht mit dem Register-Schlüsselwort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f85f3-213">Subcomponent packing is only available with the packoffset keyword, not the register keyword.</span></span> <span data-ttu-id="f85f3-214">Innerhalb einer cBuffer-Deklaration wird das Register-Schlüsselwort für Direct3D 10-Ziele ignoriert, da es für plattformübergreifende Kompatibilität angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="f85f3-214">Inside a cbuffer declaration, the register keyword is ignored for Direct3D 10 targets as it is assumed to be for cross-platform compatibility.</span></span>

<span data-ttu-id="f85f3-215">Gepackte Elemente können sich überlappen, und der Compiler gibt keinen Fehler oder keine Warnung aus.</span><span class="sxs-lookup"><span data-stu-id="f85f3-215">Packed elements may overlap and the compiler will give no error or warning.</span></span> <span data-ttu-id="f85f3-216">In diesem Beispiel überlappen sich Element2 und Element3 mit Element1. x und Element1. y.</span><span class="sxs-lookup"><span data-stu-id="f85f3-216">In this example, Element2 and Element3 will overlap with Element1.x and Element1.y.</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c0);
    float1 Element3 : packoffset(c0.y);
}
        
```



<span data-ttu-id="f85f3-217">Ein Beispiel, in dem packoffset verwendet wird: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="f85f3-217">A sample that uses packoffset is: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f85f3-218">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f85f3-218">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f85f3-219">Variablen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f85f3-219">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

