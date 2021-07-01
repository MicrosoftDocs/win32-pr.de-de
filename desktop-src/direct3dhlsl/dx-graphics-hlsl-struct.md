---
title: Strukturtyp
description: Strukturtyp
ms.assetid: 896030b0-07cd-41bd-8c94-e173eabc81dd
keywords:
- Strukturtyp HLSL
topic_type:
- apiref
api_name:
- Struct Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89435e9c8757d2e732bc6237b02a508d3af4b4db
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119095"
---
# <a name="struct-type"></a><span data-ttu-id="adc32-104">Strukturtyp</span><span class="sxs-lookup"><span data-stu-id="adc32-104">Struct Type</span></span>

<span data-ttu-id="adc32-105">Verwenden Sie die folgende Syntax, um eine -Struktur mitHILFE von HLSL zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="adc32-105">Use the following syntax to declare a structure using HLSL.</span></span>

<span data-ttu-id="adc32-106">Strukturname { \[ *InterpolationModifier* \] *Type* \[ *R* x *C* \] *MemberName*;     ... };</span><span class="sxs-lookup"><span data-stu-id="adc32-106">struct *Name*{     \[*InterpolationModifier*\] *Type*\[*R* x *C*\] *MemberName*;     ... };</span></span>



 

## <a name="parameters"></a><span data-ttu-id="adc32-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="adc32-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adc32-108"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Namen*</span><span class="sxs-lookup"><span data-stu-id="adc32-108"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="adc32-109">Eine ASCII-Zeichenfolge, die den Strukturnamen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="adc32-109">An ASCII string that uniquely identifies the structure name.</span></span>

</dd> <dt>

<span data-ttu-id="adc32-110"><span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]</span><span class="sxs-lookup"><span data-stu-id="adc32-110"><span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]</span></span>
</dt> <dd>

<span data-ttu-id="adc32-111">Optionaler Modifizierer, der einen Interpolationstyp angibt.</span><span class="sxs-lookup"><span data-stu-id="adc32-111">Optional modifier that specifies an interpolation type.</span></span> <span data-ttu-id="adc32-112">Weitere Informationen finden Sie im Abschnitt [Hinweise](#remarks).</span><span class="sxs-lookup"><span data-stu-id="adc32-112">See [Remarks](#remarks) for details.</span></span>

</dd> <dt>

<span data-ttu-id="adc32-113"><span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Typ* \[ *R* x *C*\]</span><span class="sxs-lookup"><span data-stu-id="adc32-113"><span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Type*\[*R* x *C*\]</span></span>
</dt> <dd>

<span data-ttu-id="adc32-114">Der Membertyp mit einer optionalen Zeilengröße (*R*) x Spalte (*C*) Arraygröße.</span><span class="sxs-lookup"><span data-stu-id="adc32-114">The member type with an optional row (*R*) x column (*C*) array size.</span></span> <span data-ttu-id="adc32-115">Eine -Struktur enthält mindestens ein -Element. Wenn sie mehr als ein Element enthält, sind alle Elemente vom gleichen Typ.</span><span class="sxs-lookup"><span data-stu-id="adc32-115">A structure contains at least one element; if it contains more than one element, the elements are all of the same type.</span></span> <span data-ttu-id="adc32-116">Die Anzahl der Zeilen und Spalten sind ganze Zahlen ohne Vorzeichen zwischen 1 und einschließlich 4.</span><span class="sxs-lookup"><span data-stu-id="adc32-116">The number of rows and columns are unsigned integers between 1 and 4 inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="adc32-117"><span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*Membername*</span><span class="sxs-lookup"><span data-stu-id="adc32-117"><span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*MemberName*</span></span>
</dt> <dd>

<span data-ttu-id="adc32-118">Eine ASCII-Zeichenfolge, die den Membernamen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="adc32-118">An ASCII string that uniquely identifies the member name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="adc32-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="adc32-119">Remarks</span></span>

<span data-ttu-id="adc32-120">Ein Interpolationsmodifizierer kann für jeden Struktur member oder für ein Argument für eine Pixel-Shaderfunktion angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="adc32-120">An interpolation modifier can be specified on any structure member or on an argument to a pixel shader function.</span></span> <span data-ttu-id="adc32-121">Wenn ein Modifizierer an beiden Stellen angezeigt wird, überstimmt der modifizierer outside (der Modifizierer für Das Pixel-Shaderargument) den Inside-Modifizierer (den Strukturmodifizierer).</span><span class="sxs-lookup"><span data-stu-id="adc32-121">If a modifier appears in both places, the outside modifier (the pixel shader argument modifier) overrules the inside modifier (the structure modifier).</span></span>

<span data-ttu-id="adc32-122">Beim Kompilieren eines Shaders oder Effekts packt der Shadercompiler Strukturmitglieder gemäß [HLSL-Füllregeln.](dx-graphics-hlsl-packing-rules.md)</span><span class="sxs-lookup"><span data-stu-id="adc32-122">When compiling a shader or an effect, the shader compiler packs structure members according to [HLSL packing rules](dx-graphics-hlsl-packing-rules.md).</span></span>

### <a name="interpolation-modifiers-introduced-in-shader-model-4"></a><span data-ttu-id="adc32-123">In Shadermodell 4 eingeführte Interpolationsmodifizierer</span><span class="sxs-lookup"><span data-stu-id="adc32-123">Interpolation Modifiers Introduced in Shader Model 4</span></span>

<span data-ttu-id="adc32-124">Vertex-Shader-Ausgaben, die für Pixel-Shadereingaben verwendet werden, werden linear interpoliert, um während der Rasterung Pixelwerte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="adc32-124">Vertex shader outputs that are used for pixel shader inputs are linearly interpolated to get per-pixel values during rasterization.</span></span> <span data-ttu-id="adc32-125">Verwenden Sie zum Festlegen der Interpolationsmethode einen der folgenden Werte, die in [Shadermodell 4](dx-graphics-hlsl-sm4.md) oder höher unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="adc32-125">To set the method of interpolation, use any of the following values, which are supported in [shader model 4](dx-graphics-hlsl-sm4.md) or later.</span></span> <span data-ttu-id="adc32-126">Der Modifizierer wird bei jeder Vertex-Shaderausgabe ignoriert, die nicht als Pixel-Shadereingabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="adc32-126">The modifier is ignored on any vertex shader output that is not used as a pixel shader input.</span></span>



| <span data-ttu-id="adc32-127">Interpolationsmodifizierer</span><span class="sxs-lookup"><span data-stu-id="adc32-127">Interpolation Modifier</span></span> | <span data-ttu-id="adc32-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="adc32-128">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adc32-129">**Lineare**</span><span class="sxs-lookup"><span data-stu-id="adc32-129">**linear**</span></span>             | <span data-ttu-id="adc32-130">Interpolieren zwischen Shadereingaben; **linear** ist der Standardwert, wenn kein Interpolationsmodifizierer angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="adc32-130">Interpolate between shader inputs; **linear** is the default value if no interpolation modifier is specified.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="adc32-131">**Schwerpunkt**</span><span class="sxs-lookup"><span data-stu-id="adc32-131">**centroid**</span></span>           | <span data-ttu-id="adc32-132">Interpolieren Zwischen Stichproben, die sich innerhalb des abgedeckten Bereichs des Pixels befinden (dies erfordert möglicherweise extrapolierte Endpunkte von einem Pixelcenter).</span><span class="sxs-lookup"><span data-stu-id="adc32-132">Interpolate between samples that are somewhere within the covered area of the pixel (this may require extrapolating end points from a pixel center).</span></span> <span data-ttu-id="adc32-133">Die Schwerpunkt-Stichprobenentnahme kann das Antialiasing verbessern, wenn ein Pixel teilweise abgedeckt ist (auch wenn der Pixelmittelpunkt nicht abgedeckt ist).</span><span class="sxs-lookup"><span data-stu-id="adc32-133">Centroid sampling may improve antialiasing if a pixel is partially covered (even if the pixel center is not covered).</span></span> <span data-ttu-id="adc32-134">Der **Schwerpunktmodifizierer** muss entweder mit dem **linearen** modifizierer oder **noperspective-Modifizierer** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="adc32-134">The **centroid** modifier must be combined with either the **linear** or **noperspective** modifier.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="adc32-135">**nointerpolation**</span><span class="sxs-lookup"><span data-stu-id="adc32-135">**nointerpolation**</span></span>    | <span data-ttu-id="adc32-136">Interpolieren Sie nicht .</span><span class="sxs-lookup"><span data-stu-id="adc32-136">Do not interpolate .</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="adc32-137">**noperspective**</span><span class="sxs-lookup"><span data-stu-id="adc32-137">**noperspective**</span></span>      | <span data-ttu-id="adc32-138">Führen Sie während der Interpolation keine Perspektivkorrektur durch.</span><span class="sxs-lookup"><span data-stu-id="adc32-138">Do not perform perspective-correction during interpolation.</span></span> <span data-ttu-id="adc32-139">Der **modifizierer noperspective** kann mit dem Modifizierer **"schwerpunkt"** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="adc32-139">The **noperspective** modifier can be combined with the **centroid** modifier.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="adc32-140">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="adc32-140">**sample**</span></span>             | <span data-ttu-id="adc32-141">**Verfügbar in Shadermodell 4.1 und höher** Interpolieren Sie an der Beispielposition und nicht in der Pixelmitte.</span><span class="sxs-lookup"><span data-stu-id="adc32-141">**Available in shader model 4.1 and later** Interpolate at sample location rather than at the pixel center.</span></span> <span data-ttu-id="adc32-142">Dies bewirkt, dass der Pixel-Shader pro Stichprobe und nicht pro Pixel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="adc32-142">This causes the pixel shader to execute per-sample rather than per-pixel.</span></span> <span data-ttu-id="adc32-143">Eine weitere Möglichkeit, die Ausführung pro Beispiel zu verursachen, ist eine Eingabe mit semantic [SV \_ SampleIndex,](dx-graphics-hlsl-semantics.md)die das aktuelle Beispiel angibt.</span><span class="sxs-lookup"><span data-stu-id="adc32-143">Another way to cause per-sample execution is to have an input with [semantic SV\_SampleIndex](dx-graphics-hlsl-semantics.md), which indicates the current sample.</span></span> <span data-ttu-id="adc32-144">Nur die  Eingaben mit angegebenem Beispiel (oder Eingabe von SV SampleIndex) unterscheiden sich zwischen Shaderaufrufen im Pixel, während andere Eingaben, die keine Modifizierer angeben (z. B. wenn Sie Modifizierer für verschiedene Eingaben mischen), weiterhin in der Pixelmitte \_ interpolieren.</span><span class="sxs-lookup"><span data-stu-id="adc32-144">Only the inputs with **sample** specified (or inputting SV\_SampleIndex) differ between shader invocations in the pixel, whereas other inputs that do not specify modifiers (for example, if you mix modifiers on different inputs) still interpolate at the pixel center.</span></span> <span data-ttu-id="adc32-145">Sowohl der Shaderaufruf als auch der Tiefen-/Schablonentest erfolgen für jedes abgedeckte Beispiel im Pixel.</span><span class="sxs-lookup"><span data-stu-id="adc32-145">Both pixel shader invocation and depth/stencil testing occur for every covered sample in the pixel.</span></span> <span data-ttu-id="adc32-146">Dies wird manchmal als *Supersampling bezeichnet.*</span><span class="sxs-lookup"><span data-stu-id="adc32-146">This is sometimes known as *supersampling*.</span></span> <span data-ttu-id="adc32-147">Im Gegensatz dazu wird der Pixel-Shader in Ermangelung eines Beispielhäufigkeitsaufrufs, der als *Multisampling* bezeichnet wird, einmal pro Pixel aufgerufen, unabhängig davon, wie viele Stichproben abgedeckt sind, während Tiefen-/Schablonentests mit Stichprobenhäufigkeit durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="adc32-147">In contrast, in the absence of sample frequency invocation, known as *multisampling*, the pixel shader is invoked once per pixel regardless of how many samples are covered, while depth/stencil testing occurs at sample frequency.</span></span> <span data-ttu-id="adc32-148">Beide Modi bieten entsprechende Edge-Antialiasing.</span><span class="sxs-lookup"><span data-stu-id="adc32-148">Both modes provide equivalent edge antialiasing.</span></span> <span data-ttu-id="adc32-149">Die Übersampling-Methode bietet jedoch eine bessere Schattierungsqualität, indem der Pixel-Shader häufiger aufruft.</span><span class="sxs-lookup"><span data-stu-id="adc32-149">However, supersampling provides better shading quality by invoking the pixel shader more frequently.</span></span><br/> |



 

<dl> <span data-ttu-id="adc32-150">1. Bei Verwendung eines int/uint-Typs ist **nointerpolation** die einzige gültige Option.</span><span class="sxs-lookup"><span data-stu-id="adc32-150">1. When using an int/uint type, the only valid option is **nointerpolation**.</span></span>  
</dl>

<span data-ttu-id="adc32-151">Interpolationsmodifizierer können auf Strukturmitglieder oder [Funktionsargumente oder](dx-graphics-hlsl-function-parameters.md)beides angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="adc32-151">Interpolation modifiers can be applied to structure members or [function arguments](dx-graphics-hlsl-function-parameters.md), or both.</span></span>

## <a name="examples"></a><span data-ttu-id="adc32-152">Beispiele</span><span class="sxs-lookup"><span data-stu-id="adc32-152">Examples</span></span>

<span data-ttu-id="adc32-153">Im Folgenden finden Sie einige Beispielstrukturdeklarationen.</span><span class="sxs-lookup"><span data-stu-id="adc32-153">Here are some example structure declarations.</span></span>


```
struct struct1
{
  int    a;
}
```



<span data-ttu-id="adc32-154">Diese Deklaration enthält ein Array.</span><span class="sxs-lookup"><span data-stu-id="adc32-154">This declaration includes an array.</span></span>


```
struct struct2
{
  int    a;
  float  b;
  int4x4 iMatrix;
}
```



<span data-ttu-id="adc32-155">Diese Deklaration enthält einen Interpolationsmodifizierer.</span><span class="sxs-lookup"><span data-stu-id="adc32-155">This declaration includes an interpolation modifier.</span></span>


```
struct In
{
  centroid float2 Texcoord;
};
```



## <a name="see-also"></a><span data-ttu-id="adc32-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adc32-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adc32-157">Datentypen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="adc32-157">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





