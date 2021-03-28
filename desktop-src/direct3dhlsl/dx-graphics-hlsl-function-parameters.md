---
title: Funktionsargumente
description: Eine Funktion nimmt mindestens ein Eingabe Argument an. Verwenden Sie die folgende Syntax, um jedes Argument zu deklarieren.
ms.assetid: 80e0dbc8-26b7-4250-bb01-6856fc70f6b8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ba35ad04b20b67e45550644e842d69209ca5088
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389797"
---
# <a name="function-arguments"></a><span data-ttu-id="fd94d-103">Funktionsargumente</span><span class="sxs-lookup"><span data-stu-id="fd94d-103">Function Arguments</span></span>

<span data-ttu-id="fd94d-104">Eine Funktion nimmt mindestens ein Eingabe Argument an. Verwenden Sie die folgende Syntax, um jedes Argument zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="fd94d-104">A function takes one or more input arguments; use the following syntax to declare each argument.</span></span>



|                                                                                             |
|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd94d-105">**\[Typname des inputmodifiers \] \[ : Semantic \] \[ interpolationmodifier \] \[ = Initialisierer\]**</span><span class="sxs-lookup"><span data-stu-id="fd94d-105">**\[InputModifier\] Type Name \[: Semantic\] \[InterpolationModifier\] \[= Initializers\]**</span></span> |



 

<span data-ttu-id="fd94d-106">\[\]Modifizierertypname \[ : Semantic \] \[ : Interpolations Modifizierer \] \[ = Initialisierer (s)\]</span><span class="sxs-lookup"><span data-stu-id="fd94d-106">\[Modifier\] Type Name \[: Semantic\] \[: Interpolation Modifier\] \[= Initializer(s)\]</span></span>

<span data-ttu-id="fd94d-107">Wenn mehrere Funktionsargumente vorhanden sind, werden diese durch Kommas getrennt.</span><span class="sxs-lookup"><span data-stu-id="fd94d-107">If there are multiple function arguments, they are separated by commas.</span></span>

## <a name="parameters"></a><span data-ttu-id="fd94d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd94d-108">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fd94d-109">Element</span><span class="sxs-lookup"><span data-stu-id="fd94d-109">Item</span></span></th>
<th><span data-ttu-id="fd94d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd94d-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fd94d-111"><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>Input-Modifizierer</strong></span><span class="sxs-lookup"><span data-stu-id="fd94d-111"><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>InputModifier</strong></span></span><br/></td>
<td><span data-ttu-id="fd94d-112">Optionaler Begriff, der ein Argument als Eingabe, Ausgabe oder beides bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fd94d-112">Optional term that identifies an argument as an input, an output, or both.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fd94d-113">Wert</span><span class="sxs-lookup"><span data-stu-id="fd94d-113">Value</span></span></td>
<td><span data-ttu-id="fd94d-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd94d-114">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd94d-115"><strong>in</strong></span><span class="sxs-lookup"><span data-stu-id="fd94d-115"><strong>in</strong></span></span></td>
<td><span data-ttu-id="fd94d-116">Nur Eingabe</span><span class="sxs-lookup"><span data-stu-id="fd94d-116">Input only</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd94d-117"><strong>INOUT</strong></span><span class="sxs-lookup"><span data-stu-id="fd94d-117"><strong>inout</strong></span></span></td>
<td><span data-ttu-id="fd94d-118">Eingabe und Ausgabe</span><span class="sxs-lookup"><span data-stu-id="fd94d-118">Input and an output</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd94d-119"><strong>out</strong></span><span class="sxs-lookup"><span data-stu-id="fd94d-119"><strong>out</strong></span></span></td>
<td><span data-ttu-id="fd94d-120">Nur Ausgabe</span><span class="sxs-lookup"><span data-stu-id="fd94d-120">Output only</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd94d-121"><strong>uniform-Variable</strong></span><span class="sxs-lookup"><span data-stu-id="fd94d-121"><strong>uniform</strong></span></span></td>
<td><span data-ttu-id="fd94d-122">Nur konstante Daten eingeben</span><span class="sxs-lookup"><span data-stu-id="fd94d-122">Input only constant data</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="fd94d-123">Parameter werden immer als Wert übermittelt.</span><span class="sxs-lookup"><span data-stu-id="fd94d-123">Parameters are always passed by value.</span></span> <span data-ttu-id="fd94d-124">in gibt an, dass der Wert des-Parameters aus der aufrufenden Anwendung kopiert werden soll, bevor die-Funktion beginnt.</span><span class="sxs-lookup"><span data-stu-id="fd94d-124">in indicates that the value of the parameter should be copied in from the calling application before the function begins.</span></span> <span data-ttu-id="fd94d-125">out gibt an, dass der letzte Wert des-Parameters kopiert und an die aufrufende Anwendung zurückgegeben werden soll, wenn die Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fd94d-125">out indicates that the last value of the parameter should be copied out, and returned to the calling application when the function returns.</span></span> <span data-ttu-id="fd94d-126">"INOUT" ist eine Kurzzeit zum Angeben von beidem.</span><span class="sxs-lookup"><span data-stu-id="fd94d-126">inout is a shorthand for specifying both.</span></span></p>
<p><span data-ttu-id="fd94d-127">Ein einheitlicher Wert stammt aus einem konstanten Register. jeder Scheitelpunkt-Shader oder Pixel-Shader-Aufruf hat denselben Anfangswert für eine einheitliche Variable.</span><span class="sxs-lookup"><span data-stu-id="fd94d-127">A uniform value comes from a constant register; each vertex shader or pixel shader invocation see the same initial value for a uniform variable.</span></span> <span data-ttu-id="fd94d-128">Globale Variablen werden so behandelt, als wären Sie als einheitlich deklariert.</span><span class="sxs-lookup"><span data-stu-id="fd94d-128">Global variables are treated as if they are declared uniform.</span></span> <span data-ttu-id="fd94d-129">Bei Funktionen, die nicht auf oberster Ebene stehen, ist Uniform gleichbedeutend mit <strong>in</strong>.</span><span class="sxs-lookup"><span data-stu-id="fd94d-129">For non-top-level functions, uniform is synonymous with <strong>in</strong>.</span></span> <span data-ttu-id="fd94d-130">Wenn keine Parameter Verwendung angegeben ist, wird davon ausgegangen, dass die Parameter Verwendung <strong>in</strong>erfolgt.</span><span class="sxs-lookup"><span data-stu-id="fd94d-130">If no parameter usage is specified, the parameter usage is assumed to be <strong>in</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd94d-131"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Sorte</strong></span><span class="sxs-lookup"><span data-stu-id="fd94d-131"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="fd94d-132">Der Argumenttyp. kann ein beliebiger gültiger HLSL- <a href="dx-graphics-hlsl-data-types.md">Typ</a>sein.</span><span class="sxs-lookup"><span data-stu-id="fd94d-132">The argument type; can be any valid HLSL <a href="dx-graphics-hlsl-data-types.md">type</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd94d-133"><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Benennen</strong></span><span class="sxs-lookup"><span data-stu-id="fd94d-133"><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="fd94d-134">Eine ASCII-Zeichenfolge, die den Namen der Shader-Funktion eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fd94d-134">An ASCII string that uniquely identifies the name of the shader function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd94d-135"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Tischer</strong></span><span class="sxs-lookup"><span data-stu-id="fd94d-135"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Semantic</strong></span></span></p></td>
<td><p><span data-ttu-id="fd94d-136">Optionale Zeichenfolge, die die beabsichtigte Verwendung der Daten identifiziert (siehe <a href="dx-graphics-hlsl-semantics.md">Semantik (DirectX HLSL)</a>).</span><span class="sxs-lookup"><span data-stu-id="fd94d-136">Optional string that identifies the intended usage of the data (see <a href="dx-graphics-hlsl-semantics.md">Semantics (DirectX HLSL)</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd94d-137"><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>Interpolationmodifier</strong></span><span class="sxs-lookup"><span data-stu-id="fd94d-137"><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolationModifier</strong></span></span></p></td>
<td><p><span data-ttu-id="fd94d-138">Optionaler <a href="dx-graphics-hlsl-struct.md">Interpolations Modifizierer</a> , der es einem Shader ermöglicht, die Interpolationsmethode zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="fd94d-138">Optional <a href="dx-graphics-hlsl-struct.md">interpolation modifier</a> which allows a shader to determine the method of interpolation.</span></span> <span data-ttu-id="fd94d-139">Ein Interpolations Modifizierer für ein Funktions Argument gilt nur für ein Argument, das als Eingabe für eine pixelshaderfunktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd94d-139">An interpolation modifier on a function argument only applies to an argument used as an input to a pixel shader function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd94d-140"><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Initialisierer</strong></span><span class="sxs-lookup"><span data-stu-id="fd94d-140"><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Initializers</strong></span></span></p></td>
<td><p><span data-ttu-id="fd94d-141">Optionale Werte für die Initialisierung. zum Initialisieren von Datentypen mit mehreren Komponenten sind mehrere Werte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fd94d-141">Optional values for initialization; multiple values are required to initialize multi-component data types.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="fd94d-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd94d-142">Remarks</span></span>

<span data-ttu-id="fd94d-143">Funktionsargumente werden in einer durch Trennzeichen getrennten Argumentliste in einer Funktionsdeklaration aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fd94d-143">Function arguments are listed in a comma-separated argument list in a function declaration.</span></span> <span data-ttu-id="fd94d-144">Wie bei C-Funktionen muss jedes Argument einen Parameternamen und einen Typ deklarieren. ein Argument für eine HLSL-Funktion kann optional eine Semantik, einen Anfangswert und eine Pixel-Shadereingabe enthalten, die einen Interpolationstyp enthalten können.</span><span class="sxs-lookup"><span data-stu-id="fd94d-144">As in C functions, each argument must have a parameter name and type declared; an argument to an HLSL function optionally can include a semantic, an initial value, and a pixel shader input can include an interpolation type.</span></span>

<span data-ttu-id="fd94d-145">Der *Typ* eines Funktionsarguments könnte eine Struktur sein, die einen Interpolations Modifizierer pro Member enthalten könnte.</span><span class="sxs-lookup"><span data-stu-id="fd94d-145">The *Type* of a function argument could be a structure, which could include a per-member interpolation modifier.</span></span> <span data-ttu-id="fd94d-146">Wenn das Funktions Argument auch einen Interpolations Modifizierer aufweist, überschreibt der funktionsargumentmodifizierer Interpolations Modifizierer, die innerhalb des Typs deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="fd94d-146">If the function argument also has an interpolation modifier, the function argument modifier overrides interpolation modifiers declared within the Type.</span></span>

## <a name="examples"></a><span data-ttu-id="fd94d-147">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd94d-147">Examples</span></span>

<span data-ttu-id="fd94d-148">In diesem Beispiel (aus dem [BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)-Beispiel) werden einheitliche und nicht einheitliche Eingaben für eine Vertex-Shader-Funktion veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="fd94d-148">This example (from the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) illustrates uniform and non-uniform inputs to a vertex shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( 
  float4 vPos : POSITION,
  float3 vNormal : NORMAL,
  float2 vTexCoord0 : TEXCOORD,
  uniform int nNumLights,
  uniform bool bTexture,
  uniform bool bAnimate )
{
  ...
}
```



<span data-ttu-id="fd94d-149">In diesem Beispiel (aus dem [contentstreaming-Beispiel](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) wird eine Eingabe Struktur verwendet, um Argumente an eine Pixel-Shader-Funktion zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="fd94d-149">This example (from the [ContentStreaming Sample](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) uses an input structure to pass arguments to a pixel shader function.</span></span>


```
VSBasicIn input
struct VSBasicIn
{
  float4 Pos    : POSITION;
  float3 Norm   : NORMAL;
  float2 Tex    : TEXCOORD0;
};

PSBasicIn VSBasic(VSBasicIn input)
{
  ...
}
```



## <a name="related-topics"></a><span data-ttu-id="fd94d-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd94d-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd94d-151">Funktionen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd94d-151">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 





