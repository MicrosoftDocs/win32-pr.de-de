---
title: Variablensyntax
description: Verwenden Sie die folgenden Syntaxregeln, um HLSL-Variablen zu deklarieren.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- extern, Variable Syntax (DirectX HLSL)
- nointerpolation, Variable Syntax (DirectX HLSL)
- shared, Variable Syntax (DirectX HLSL)
- groupshared, Variable Syntax (DirectX HLSL)
- static, Variable Syntax (DirectX HLSL)
- Uniform, Variable Syntax (DirectX HLSL)
- volatile, Variable Syntax (DirectX HLSL)
- precise, Variable Syntax (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 446444e09b0b6aff3e0ba8ca8b12cfbf6dc94128
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826068"
---
# <a name="variable-syntax"></a><span data-ttu-id="4922f-111">Variablensyntax</span><span class="sxs-lookup"><span data-stu-id="4922f-111">Variable Syntax</span></span>

<span data-ttu-id="4922f-112">Verwenden Sie die folgenden Syntaxregeln, um HLSL-Variablen zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="4922f-112">Use the following syntax rules to declare HLSL variables.</span></span>

<span data-ttu-id="4922f-113">\[*Speicher \_* \] \[ *Typnamenindex \_ des* \] *Klassentypmodifizierers* \[  \] \[ *: Semantik* \] \[ *: Packoffset* \] \[ *: Register* \] ;    \[  \] Anmerkungen \[ *= Initial \_ Wert*                    \]</span><span class="sxs-lookup"><span data-stu-id="4922f-113">\[*Storage\_Class*\] \[*Type\_Modifier*\] *Type Name*\[*Index*\]     \[*: Semantic*\]     \[*: Packoffset*\]     \[*: Register*\];    \[*Annotations*\]     \[*= Initial\_Value*\]</span></span>



 

## <a name="parameters"></a><span data-ttu-id="4922f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4922f-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4922f-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*\_Storage-Klasse*</span><span class="sxs-lookup"><span data-stu-id="4922f-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Storage\_Class*</span></span> 
</dt> <dd>

<span data-ttu-id="4922f-116">Optionale Speicherklassenmodifizierer, die dem Compiler Hinweise zum Variablenbereich und zur Lebensdauer geben; die Modifizierer können in beliebiger Reihenfolge angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4922f-116">Optional storage-class modifiers that give the compiler hints about variable scope and lifetime; the modifiers can be specified in any order.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4922f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4922f-117">Value</span></span></th>
<th><span data-ttu-id="4922f-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4922f-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4922f-119"><strong>extern</strong></span><span class="sxs-lookup"><span data-stu-id="4922f-119"><strong>extern</strong></span></span></td>
<td><span data-ttu-id="4922f-120">Markieren Sie eine globale Variable als externe Eingabe für den Shader. dies ist die Standardmarkierung für alle globalen Variablen.</span><span class="sxs-lookup"><span data-stu-id="4922f-120">Mark a global variable as an external input to the shader; this is the default marking for all global variables.</span></span> <span data-ttu-id="4922f-121">Kann nicht mit statischem <strong>kombiniert werden.</strong></span><span class="sxs-lookup"><span data-stu-id="4922f-121">Cannot be combined with <strong>static</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4922f-122"><strong>nointerpolation</strong></span><span class="sxs-lookup"><span data-stu-id="4922f-122"><strong>nointerpolation</strong></span></span></td>
<td><span data-ttu-id="4922f-123">Interpolieren Sie die Ausgaben eines Vertex-Shaders nicht, bevor Sie sie an einen Pixel-Shader übergeben.</span><span class="sxs-lookup"><span data-stu-id="4922f-123">Do not interpolate the outputs of a vertex shader before passing them to a pixel shader.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4922f-124"><strong>Präzise</strong></span><span class="sxs-lookup"><span data-stu-id="4922f-124"><strong>precise</strong></span></span></td>
<td><span data-ttu-id="4922f-125">Das <strong>genaue</strong> Schlüsselwort, wenn es auf eine Variable angewendet wird, schränkt alle Berechnungen ein, die verwendet werden, um den dieser Variablen zugewiesenen Wert auf folgende Weise zu erzeugen:</span><span class="sxs-lookup"><span data-stu-id="4922f-125">The <strong>precise</strong> keyword when applied to a variable will restrict any calculations used to produce the value assigned to that variable in the following ways:</span></span>

*   <span data-ttu-id="4922f-126">Separate Vorgänge werden getrennt gehalten.</span><span class="sxs-lookup"><span data-stu-id="4922f-126">Separate operations are kept separate.</span></span> <span data-ttu-id="4922f-127">Wenn z. B. ein mul- und add-Vorgang <strong></strong> in einen unsinnigen Vorgang verschlangen wurde, zwingt präzise die Vorgänge, getrennt zu bleiben.</span><span class="sxs-lookup"><span data-stu-id="4922f-127">For example, where a mul and add operation might have been fused into a mad operation, <strong>precise</strong> forces the operations to remain separate.</span></span> <span data-ttu-id="4922f-128">Stattdessen müssen Sie explizit die intrinsische Funktion "mad" verwenden.</span><span class="sxs-lookup"><span data-stu-id="4922f-128">Instead, you must explicitly use the mad intrinsic function.</span></span>
*   <span data-ttu-id="4922f-129">Die Reihenfolge der Vorgänge wird beibehalten.</span><span class="sxs-lookup"><span data-stu-id="4922f-129">Order of operations are maintained.</span></span> <span data-ttu-id="4922f-130">Wenn die Reihenfolge der Anweisungen möglicherweise gemischt wurde, um die Leistung zu <strong>verbessern,</strong> stellt präzise sicher, dass der Compiler die Reihenfolge wie geschrieben beibwahrt.</span><span class="sxs-lookup"><span data-stu-id="4922f-130">Where the order of instructions might have been shuffled to improve performance, <strong>precise</strong> ensures that the compiler preserves the order as written.</span></span>
*   <span data-ttu-id="4922f-131">Unsichere IEEE-Vorgänge sind eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="4922f-131">IEEE unsafe operations are restricted.</span></span> <span data-ttu-id="4922f-132">Wenn der Compiler möglicherweise schnelle mathematische Operationen verwendet hat, die keine NaN-Werte (keine Zahl) und INF-Werte (unendlich) <strong>berücksichtigen,</strong> erzwingt präzise die Einhaltung von IEEE-Anforderungen in Bezug auf NaN- und INF-Werte.</span><span class="sxs-lookup"><span data-stu-id="4922f-132">Where the compiler might have used fast math operations that don't account for NaN (not a number) and INF (infinite) values, <strong>precise</strong> forces IEEE requirements concerning NaN and INF values to be respected.</span></span> <span data-ttu-id="4922f-133">Ohne <strong>präzise</strong>sind diese Optimierungen und mathematischen Operationen nicht IEEE-sicher.</span><span class="sxs-lookup"><span data-stu-id="4922f-133">Without <strong>precise</strong>, these optimizations and mathematical operations are not IEEE safe.</span></span>
*   <span data-ttu-id="4922f-134">Wenn Sie eine Variable <strong>präzise qualifizieren,</strong> werden Vorgänge, die die Variable verwenden, nicht <strong>präzise.</strong></span><span class="sxs-lookup"><span data-stu-id="4922f-134">Qualifying a variable <strong>precise</strong> doesn't make operations that use the variable <strong>precise</strong>.</span></span> <span data-ttu-id="4922f-135">Da <strong></strong> präzise nur an Vorgänge weitergibt, die zu den <strong></strong>Werten beitragen, die der genau <strong></strong> qualifizierten Variablen zugewiesen sind, kann es schwierig <strong></strong> sein, die gewünschten Berechnungen richtig zu bestimmen. Daher wird empfohlen, die Shader-Ausgaben direkt dort zu markieren, wo Sie sie deklarieren, unabhängig davon, ob es sich um ein Strukturfeld, einen Ausgabeparameter oder den Rückgabetyp der Eingabefunktion handelt.</span><span class="sxs-lookup"><span data-stu-id="4922f-135">Since <strong>precise</strong> propagates only to operations that contribute to the values that are assigned to the <strong>precise</strong>-qualified variable, correctly making desired calculations <strong>precise</strong> can be tricky, so we recommended that you mark the shader outputs <strong>precise</strong> directly where you declare them, whether that's on a structure field, or on an output parameter, or the return type of the entry function.</span></span>

<span data-ttu-id="4922f-136">Die Möglichkeit, Optimierungen auf diese Weise zu steuern, behält die Ergebnisinvarianz für die geänderte Ausgabevariable bei, indem Optimierungen deaktiviert werden, die sich aufgrund von Unterschieden bei akkumulierten Genauigkeitsunterschieden auf Endergebnisse auswirken können.</span><span class="sxs-lookup"><span data-stu-id="4922f-136">The ability to control optimizations in this way maintains result invariance for the modified output variable by disabling optimizations that might affect final results due to differences in accumulated precision differences.</span></span> <span data-ttu-id="4922f-137">Dies ist hilfreich, wenn Shader für Mosaik die wasserdichten Patchnähte bzw. die Übereinstimmung von Tiefenwerten über mehrere Durchläufe hinweg verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="4922f-137">It is useful when you want shaders for tessellation to maintain water-tight patch seams or match depth values over multiple passes.</span></span>

<span data-ttu-id="4922f-138">[Beispielcode:](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl)</span><span class="sxs-lookup"><span data-stu-id="4922f-138">[Sample code](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl):</span></span> 
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
<td><span data-ttu-id="4922f-139"><strong>geteilt</strong></span><span class="sxs-lookup"><span data-stu-id="4922f-139"><strong>shared</strong></span></span></td>
<td><span data-ttu-id="4922f-140">Markieren Sie eine Variable für die Freigabe zwischen Effekten. dies ist ein Hinweis an den Compiler.</span><span class="sxs-lookup"><span data-stu-id="4922f-140">Mark a variable for sharing between effects; this is a hint to the compiler.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4922f-141"><strong>groupshared</strong></span><span class="sxs-lookup"><span data-stu-id="4922f-141"><strong>groupshared</strong></span></span></td>
<td><span data-ttu-id="4922f-142">Markieren Sie eine Variable für freigegebenen Threadgruppenspeicher für Compute-Shader.</span><span class="sxs-lookup"><span data-stu-id="4922f-142">Mark a variable for thread-group-shared memory for compute shaders.</span></span> <span data-ttu-id="4922f-143">In D3D10 beträgt die maximale Gesamtgröße aller Variablen mit der groupshared-Speicherklasse 16 KB, in D3D11 beträgt die maximale Größe 32 KB.</span><span class="sxs-lookup"><span data-stu-id="4922f-143">In D3D10 the maximum total size of all variables with the groupshared storage class is 16kb, in D3D11 the maximum size is 32kb.</span></span> <span data-ttu-id="4922f-144">Siehe Beispiele.</span><span class="sxs-lookup"><span data-stu-id="4922f-144">See examples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4922f-145"><strong>static</strong></span><span class="sxs-lookup"><span data-stu-id="4922f-145"><strong>static</strong></span></span></td>
<td><span data-ttu-id="4922f-146">Markieren Sie eine lokale Variable so, dass sie einmal initialisiert wird und zwischen Funktionsaufrufen beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="4922f-146">Mark a local variable so that it is initialized one time and persists between function calls.</span></span> <span data-ttu-id="4922f-147">Wenn die Deklaration keinen Initialisierer enthält, wird der Wert auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4922f-147">If the declaration does not include an initializer, the value is set to zero.</span></span> <span data-ttu-id="4922f-148">Eine als statisch <strong>markierte globale Variable</strong> ist für eine Anwendung nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="4922f-148">A global variable marked <strong>static</strong> is not visible to an application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4922f-149"><strong>uniform-Variable</strong></span><span class="sxs-lookup"><span data-stu-id="4922f-149"><strong>uniform</strong></span></span></td>
<td><span data-ttu-id="4922f-150">Markieren Sie eine Variable, deren Daten während der ausführung eines Shaders konstant sind (z. B. eine Materialfarbe in einem Vertex-Shader). globale Variablen werden standardmäßig <strong>als einheitlich</strong> betrachtet.</span><span class="sxs-lookup"><span data-stu-id="4922f-150">Mark a variable whose data is constant throughout the execution of a shader (such as a material color in a vertex shader); global variables are considered <strong>uniform</strong> by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4922f-151"><strong>volatile</strong></span><span class="sxs-lookup"><span data-stu-id="4922f-151"><strong>volatile</strong></span></span></td>
<td><span data-ttu-id="4922f-152">Markieren Sie eine Variable, die sich häufig ändert. dies ist ein Hinweis an den Compiler.</span><span class="sxs-lookup"><span data-stu-id="4922f-152">Mark a variable that changes frequently; this is a hint to the compiler.</span></span> <span data-ttu-id="4922f-153">Dieser Speicherklassenmodifizierer gilt nur für eine lokale Variable.</span><span class="sxs-lookup"><span data-stu-id="4922f-153">This storage class modifier only applies to a local variable.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4922f-154">Der HLSL-Compiler ignoriert diesen Speicherklassenmodifizierer derzeit.</span><span class="sxs-lookup"><span data-stu-id="4922f-154">The HLSL compiler currently ignores this storage class modifier.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="4922f-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*\_Typmodifizierer*</span><span class="sxs-lookup"><span data-stu-id="4922f-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*Type\_Modifier*</span></span>
</dt> <dd>

<span data-ttu-id="4922f-156">Optionaler Variablentypmodifizierer.</span><span class="sxs-lookup"><span data-stu-id="4922f-156">Optional variable-type modifier.</span></span>



| <span data-ttu-id="4922f-157">Wert</span><span class="sxs-lookup"><span data-stu-id="4922f-157">Value</span></span>             | <span data-ttu-id="4922f-158">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4922f-158">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4922f-159">**const**</span><span class="sxs-lookup"><span data-stu-id="4922f-159">**const**</span></span>         | <span data-ttu-id="4922f-160">Markieren Sie eine Variable, die nicht von einem Shader geändert werden kann. Daher muss sie in der Variablendeklaration initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4922f-160">Mark a variable that cannot be changed by a shader, therefore, it must be initialized in the variable declaration.</span></span> <span data-ttu-id="4922f-161">Globale Variablen werden standardmäßig als **const** betrachtet (unterdrücken Sie dieses Verhalten, indem Sie das Flag /Gec an den Compiler übergeben).</span><span class="sxs-lookup"><span data-stu-id="4922f-161">Global variables are considered **const** by default (suppress this behavior by supplying the /Gec flag to the compiler).</span></span> |
| <span data-ttu-id="4922f-162">**\_Zeilen-Hauptzeile**</span><span class="sxs-lookup"><span data-stu-id="4922f-162">**row\_major**</span></span>    | <span data-ttu-id="4922f-163">Markieren Sie eine Variable, die vier Komponenten in einer einzelnen Zeile speichert, damit sie in einem einzelnen konstanten Register gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="4922f-163">Mark a variable that stores four components in a single row so they can be stored in a single constant register.</span></span>                                                                                                                             |
| <span data-ttu-id="4922f-164">**\_Spalten-Hauptspalte**</span><span class="sxs-lookup"><span data-stu-id="4922f-164">**column\_major**</span></span> | <span data-ttu-id="4922f-165">Markieren Sie eine Variable, die 4 Komponenten in einer einzelnen Spalte speichert, um die Matrixmatrizen zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="4922f-165">Mark a variable that stores 4 components in a single column to optimize matrix math.</span></span>                                                                                                                                                         |



 

> [!Note]  
> <span data-ttu-id="4922f-166">Wenn Sie keinen Typmodifiziererwert angeben, verwendet der Compiler **die \_ Spalten-Hauptspalte** als Standardwert.</span><span class="sxs-lookup"><span data-stu-id="4922f-166">If you do not specify a type-modifier value, the compiler uses **column\_major** as the default value.</span></span>

 

</dd> <dt>

<span data-ttu-id="4922f-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Typ*</span><span class="sxs-lookup"><span data-stu-id="4922f-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Type*</span></span>
</dt> <dd>

<span data-ttu-id="4922f-168">Alle HLSL-Typen, die unter [Datentypen (DirectX HLSL) aufgeführt sind.](dx-graphics-hlsl-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="4922f-168">Any HLSL type listed in [Data Types (DirectX HLSL)](dx-graphics-hlsl-data-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="4922f-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Name* \[ *Index*\]</span><span class="sxs-lookup"><span data-stu-id="4922f-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Name*\[*Index*\]</span></span>
</dt> <dd>

<span data-ttu-id="4922f-170">ASCII-Zeichenfolge, die eine Shadervariable eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4922f-170">ASCII string that uniquely identifies a shader variable.</span></span> <span data-ttu-id="4922f-171">Um ein optionales Array zu definieren, verwenden Sie **index** für die Arraygröße, bei der es sich um eine positive ganze Zahl = 1 handelt.</span><span class="sxs-lookup"><span data-stu-id="4922f-171">To define an optional array, use **index** for the array size, which is a positive integer = 1.</span></span>

</dd> <dt>

<span data-ttu-id="4922f-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantische*</span><span class="sxs-lookup"><span data-stu-id="4922f-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="4922f-173">Optionale Parameterverwendungsinformationen, die vom Compiler verwendet werden, um Shadereingaben und -ausgaben zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="4922f-173">Optional parameter-usage information, used by the compiler to link shader inputs and outputs.</span></span> <span data-ttu-id="4922f-174">Es gibt mehrere vordefinierte [Semantik für](dx-graphics-hlsl-semantics.md) Vertex- und Pixel-Shader.</span><span class="sxs-lookup"><span data-stu-id="4922f-174">There are several predefined [semantics](dx-graphics-hlsl-semantics.md) for vertex and pixel shaders.</span></span> <span data-ttu-id="4922f-175">Der Compiler ignoriert die Semantik, es sei denn, sie werden für eine globale Variable deklariert oder ein Parameter, der an einen Shader übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="4922f-175">The compiler ignores semantics unless they are declared on a global variable, or a parameter passed into a shader.</span></span>

</dd> <dt>

<span data-ttu-id="4922f-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span><span class="sxs-lookup"><span data-stu-id="4922f-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span></span>
</dt> <dd>

<span data-ttu-id="4922f-177">Optionales Schlüsselwort zum manuellen Packen von Shaderkonst constants.</span><span class="sxs-lookup"><span data-stu-id="4922f-177">Optional keyword for manually packing shader constants.</span></span> <span data-ttu-id="4922f-178">Weitere Informationen [finden Sie unter packoffset (DirectX HLSL).](dx-graphics-hlsl-variable-packoffset.md)</span><span class="sxs-lookup"><span data-stu-id="4922f-178">See [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).</span></span>

</dd> <dt>

<span data-ttu-id="4922f-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Registrieren*</span><span class="sxs-lookup"><span data-stu-id="4922f-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Register*</span></span>
</dt> <dd>

<span data-ttu-id="4922f-180">Optionales Schlüsselwort zum manuellen Zuweisen einer Shadervariablen zu einem bestimmten Register.</span><span class="sxs-lookup"><span data-stu-id="4922f-180">Optional keyword for manually assigning a shader variable to a particular register.</span></span> <span data-ttu-id="4922f-181">Weitere [Informationen finden Sie unter register (DirectX HLSL).](dx-graphics-hlsl-variable-register.md)</span><span class="sxs-lookup"><span data-stu-id="4922f-181">See [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).</span></span>

</dd> <dt>

<span data-ttu-id="4922f-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Anmerkungen*</span><span class="sxs-lookup"><span data-stu-id="4922f-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Annotation(s)*</span></span>
</dt> <dd>

<span data-ttu-id="4922f-183">Optionale Metadaten in Form einer Zeichenfolge, die an eine globale Variable angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="4922f-183">Optional metadata, in the form of a string, attached to a global variable.</span></span> <span data-ttu-id="4922f-184">Eine Anmerkung wird vom Effektframework verwendet und von HLSL ignoriert. Eine ausführlichere Syntax finden Sie unter [Anmerkungssyntax](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span><span class="sxs-lookup"><span data-stu-id="4922f-184">An annotation is used by the effect framework and ignored by HLSL; to see more detailed syntax, see [annotation syntax](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span></span>

</dd> <dt>

<span data-ttu-id="4922f-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*\_Anfangswert*</span><span class="sxs-lookup"><span data-stu-id="4922f-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*Initial\_Value*</span></span>
</dt> <dd>

<span data-ttu-id="4922f-186">Optionale Anfangswert(en); Die Anzahl der Werte sollte mit der Anzahl der Komponenten im Typ *übereinstimmen.*</span><span class="sxs-lookup"><span data-stu-id="4922f-186">Optional initial value(s); the number of values should match the number of components in *Type*.</span></span> <span data-ttu-id="4922f-187">Jede globale Variable, die **als extern markiert** ist, muss mit einem Literalwert initialisiert werden. Jede als **statisch markierte** Variable muss mit einer Konstante initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4922f-187">Each global variable marked **extern** must be initialized with a literal value; each variable marked **static** must be initialized with a constant.</span></span>

<span data-ttu-id="4922f-188">Globale Variablen, die nicht als **statisch oder** **extern** gekennzeichnet sind, werden nicht in den Shader kompiliert.</span><span class="sxs-lookup"><span data-stu-id="4922f-188">Global variables that are not marked **static** or **extern** are not compiled into the shader.</span></span> <span data-ttu-id="4922f-189">Der Compiler setzt nicht automatisch Standardwerte für globale Variablen und kann sie nicht in Optimierungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4922f-189">The compiler does not automatically set default values for global variables and cannot use them in optimizations.</span></span> <span data-ttu-id="4922f-190">Um diesen Typ einer globalen Variablen zu initialisieren, verwenden Sie reflektion, um ihren Wert zu erhalten, und kopieren Sie den Wert dann in einen konstanten Puffer.</span><span class="sxs-lookup"><span data-stu-id="4922f-190">To initialize this type of global variable, use reflection to get its value and then copy the value to a constant buffer.</span></span> <span data-ttu-id="4922f-191">Beispielsweise können Sie die [**ID3D11ShaderReflection::GetVariableByName-Methode**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) verwenden, um die Variable zu erhalten, die [**ID3D11ShaderReflectionVariable::GetDesc-Methode**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) verwenden, um die Beschreibung der Shadervariablen zu erhalten, und den Anfangswert aus dem **DefaultValue-Element** der [**D3D11 \_ SHADER \_ VARIABLE \_ DESC-Struktur**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) erhalten.</span><span class="sxs-lookup"><span data-stu-id="4922f-191">For example, you can use the [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) method to get the variable, use the [**ID3D11ShaderReflectionVariable::GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) method to get the shader-variable description, and get the initial value from the **DefaultValue** member of the [**D3D11\_SHADER\_VARIABLE\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) structure.</span></span> <span data-ttu-id="4922f-192">Um den Wert in den Konstantenpuffer zu kopieren, müssen Sie sicherstellen, dass der Puffer mit CPU-Schreibzugriff [**(D3D11 \_ CPU \_ ACCESS \_ WRITE) erstellt wurde.**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)</span><span class="sxs-lookup"><span data-stu-id="4922f-192">To copy the value to the constant buffer, you must ensure that the buffer was created with CPU write access ([**D3D11\_CPU\_ACCESS\_WRITE**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)).</span></span> <span data-ttu-id="4922f-193">Weitere Informationen zum Erstellen eines konstanten Puffers finden Sie unter [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span><span class="sxs-lookup"><span data-stu-id="4922f-193">For more information about how to create a constant buffer, see [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="4922f-194">Sie können auch das [Effektframework verwenden,](../direct3d11/d3d11-graphics-programming-guide-effects.md) um das reflektierende automatisch zu verarbeiten und den Anfangswert zu setzen.</span><span class="sxs-lookup"><span data-stu-id="4922f-194">You can also use the [effects framework](../direct3d11/d3d11-graphics-programming-guide-effects.md) to automatically process the reflecting and setting the initial value.</span></span> <span data-ttu-id="4922f-195">Beispielsweise können Sie die [**ID3DX11EffectPass::Apply-Methode**](/windows/desktop/direct3d11/id3dx11effectpass-apply) verwenden.</span><span class="sxs-lookup"><span data-stu-id="4922f-195">For example, you can use the [**ID3DX11EffectPass::Apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) method.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="4922f-196">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4922f-196">Examples</span></span>

<span data-ttu-id="4922f-197">Im Folgenden finden Sie einige Beispiele für Shadervariablendeklarationen.</span><span class="sxs-lookup"><span data-stu-id="4922f-197">Here are several examples of shader-variable declarations.</span></span>


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



### <a name="group-shared"></a><span data-ttu-id="4922f-198">Freigegebene Gruppe</span><span class="sxs-lookup"><span data-stu-id="4922f-198">Group Shared</span></span>

<span data-ttu-id="4922f-199">HLSL ermöglicht Threads eines Compute-Shaders den Austausch von Werten über freigegebenen Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="4922f-199">HLSL enables threads of a compute shader to exchange values via shared memory.</span></span> <span data-ttu-id="4922f-200">HLSL stellt Barriereprimitiven wie [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md)und so weiter zur Verfügung, um die richtige Reihenfolge von Lese- und Schreibvorgängen in freigegebenen Speicher im Shader sicherzustellen und Datenprobleme zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="4922f-200">HLSL provides barrier primitives such as [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md), and so on to ensure the correct ordering of reads and writes to shared memory in the shader and to avoid data races.</span></span>

> [!Note]  
> <span data-ttu-id="4922f-201">Die Hardware führt Threads in Gruppen aus (Warps oder Wellenfronten), und die Barrieresynchronisierung kann manchmal weggelassen werden, um die Leistung zu erhöhen, wenn nur die Synchronisierung von Threads, die derselben Gruppe angehören, korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="4922f-201">Hardware executes threads in groups (warps or wave-fronts), and barrier synchronization can sometimes be omitted to increase performance when only synchronizing threads that belong to the same group is correct.</span></span> <span data-ttu-id="4922f-202">Wir raten jedoch dringend davon ab, diese Auslassung aus folgenden Gründen zu vermeiden:</span><span class="sxs-lookup"><span data-stu-id="4922f-202">But we highly discourage this omission for these reasons:</span></span>
>
> -   <span data-ttu-id="4922f-203">Diese Auslassung führt zu nicht portablem Code, der auf einigen Hardwarekomponenten möglicherweise nicht funktioniert und nicht für Softwarerasterizer funktioniert, die in der Regel Threads in kleineren Gruppen ausführen.</span><span class="sxs-lookup"><span data-stu-id="4922f-203">This omission results in non-portable code, which might not work on some hardware and doesn't work on software rasterizers that typically execute threads in smaller groups.</span></span>
> -   <span data-ttu-id="4922f-204">Die Leistungsverbesserungen, die Sie mit dieser Auslassung erzielen können, sind im Vergleich zur Verwendung der Allthread-Barriere geringfügig.</span><span class="sxs-lookup"><span data-stu-id="4922f-204">The performance improvements that you might achieve with this omission will be minor compared to using all-thread barrier.</span></span>

 

<span data-ttu-id="4922f-205">In Direct3D 10 erfolgt beim Schreiben in **groupshared** keine Synchronisierung von Threads. Dies bedeutet, dass jeder Thread zum Schreiben auf einen einzelnen Speicherort in einem Array beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="4922f-205">In Direct3D 10 there is no synchronization of threads when writing to **groupshared**, so this means that each thread is limited to a single location in an array for writing.</span></span> <span data-ttu-id="4922f-206">Verwenden Sie den [Systemwert SV \_ GroupIndex,](dx-graphics-hlsl-semantics.md) um beim Schreiben in dieses Array zu indizieren, um sicherzustellen, dass keine zwei Threads miteinander in Konflikt treten können.</span><span class="sxs-lookup"><span data-stu-id="4922f-206">Use the [SV\_GroupIndex](dx-graphics-hlsl-semantics.md) system value to index into this array when writing to ensure that no two threads can collide.</span></span> <span data-ttu-id="4922f-207">Im Hinblick auf das Lesen haben alle Threads Zugriff auf das gesamte Array zum Lesen.</span><span class="sxs-lookup"><span data-stu-id="4922f-207">In terms of reading, all threads have access to the entire array for reading.</span></span>


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



### <a name="packing"></a><span data-ttu-id="4922f-208">Verpackung</span><span class="sxs-lookup"><span data-stu-id="4922f-208">Packing</span></span>

<span data-ttu-id="4922f-209">Packen Sie Unterkomponenten von Vektoren und Skalaren, deren Größe groß genug ist, um das Überschreiten von Registergrenzen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="4922f-209">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundarys.</span></span> <span data-ttu-id="4922f-210">Dies sind z. B. alle gültig:</span><span class="sxs-lookup"><span data-stu-id="4922f-210">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



<span data-ttu-id="4922f-211">Komprimierungstypen können nicht kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="4922f-211">Cannot mix packing types.</span></span>

<span data-ttu-id="4922f-212">Wie das Schlüsselwort register kann ein packoffset zielspezifisch sein.</span><span class="sxs-lookup"><span data-stu-id="4922f-212">Like the register keyword, a packoffset can be target specific.</span></span> <span data-ttu-id="4922f-213">Das Packen von Unterkomponenten ist nur mit dem Schlüsselwort packoffset und nicht mit dem Schlüsselwort register verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4922f-213">Subcomponent packing is only available with the packoffset keyword, not the register keyword.</span></span> <span data-ttu-id="4922f-214">Innerhalb einer cbuffer-Deklaration wird das Registerschlüsselwort für Direct3D 10-Ziele ignoriert, da es aus Gründen der plattformübergreifenden Kompatibilität angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="4922f-214">Inside a cbuffer declaration, the register keyword is ignored for Direct3D 10 targets as it is assumed to be for cross-platform compatibility.</span></span>

<span data-ttu-id="4922f-215">Gepackte Elemente können sich überlappen, und der Compiler gibt keinen Fehler oder keine Warnung aus.</span><span class="sxs-lookup"><span data-stu-id="4922f-215">Packed elements may overlap and the compiler will give no error or warning.</span></span> <span data-ttu-id="4922f-216">In diesem Beispiel überlappen sich Element2 und Element3 mit Element1.x und Element1.y.</span><span class="sxs-lookup"><span data-stu-id="4922f-216">In this example, Element2 and Element3 will overlap with Element1.x and Element1.y.</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c0);
    float1 Element3 : packoffset(c0.y);
}
        
```



<span data-ttu-id="4922f-217">Ein Beispiel, das packoffset verwendet, [ist: HLSLWithoutFX10-Beispiel.](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="4922f-217">A sample that uses packoffset is: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4922f-218">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4922f-218">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4922f-219">Variablen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4922f-219">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

