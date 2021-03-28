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
ms.openlocfilehash: 416c14c18fa1d0b76f4d13b609b895b0c64c2594
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104992903"
---
# <a name="struct-type"></a><span data-ttu-id="56e3e-104">Strukturtyp</span><span class="sxs-lookup"><span data-stu-id="56e3e-104">Struct Type</span></span>

<span data-ttu-id="56e3e-105">Verwenden Sie die folgende Syntax, um eine Struktur mithilfe von HLSL zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="56e3e-105">Use the following syntax to declare a structure using HLSL.</span></span>



|                                                                                           |
|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="56e3e-106">Struktur *Name*{ \[ *interpolationmodifier* \] *Type* \[ *R* x *C* \] *Mitgliedschaft Name*;     ... };</span><span class="sxs-lookup"><span data-stu-id="56e3e-106">struct *Name*{     \[*InterpolationModifier*\] *Type*\[*R* x *C*\] *MemberName*;     ... };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="56e3e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="56e3e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56e3e-108"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Benennen*</span><span class="sxs-lookup"><span data-stu-id="56e3e-108"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="56e3e-109">Eine ASCII-Zeichenfolge, die den Namen der Struktur eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="56e3e-109">An ASCII string that uniquely identifies the structure name.</span></span>

</dd> <dt>

<span data-ttu-id="56e3e-110"><span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*Interpolationmodifier*\]</span><span class="sxs-lookup"><span data-stu-id="56e3e-110"><span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]</span></span>
</dt> <dd>

<span data-ttu-id="56e3e-111">Optionaler Modifizierer, der einen Interpolationstyp angibt.</span><span class="sxs-lookup"><span data-stu-id="56e3e-111">Optional modifier that specifies an interpolation type.</span></span> <span data-ttu-id="56e3e-112">Weitere Informationen finden Sie im Abschnitt [Hinweise](#remarks).</span><span class="sxs-lookup"><span data-stu-id="56e3e-112">See [Remarks](#remarks) for details.</span></span>

</dd> <dt>

<span data-ttu-id="56e3e-113"><span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Typ* \[ *R* x *C*\]</span><span class="sxs-lookup"><span data-stu-id="56e3e-113"><span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Type*\[*R* x *C*\]</span></span>
</dt> <dd>

<span data-ttu-id="56e3e-114">Der Elementtyp mit einer optionalen Row (*R*) x Column (*C*)-Array Größe.</span><span class="sxs-lookup"><span data-stu-id="56e3e-114">The member type with an optional row (*R*) x column (*C*) array size.</span></span> <span data-ttu-id="56e3e-115">Eine-Struktur enthält mindestens ein Element. Wenn Sie mehr als ein Element enthält, sind die Elemente alle vom gleichen Typ.</span><span class="sxs-lookup"><span data-stu-id="56e3e-115">A structure contains at least one element; if it contains more than one element, the elements are all of the same type.</span></span> <span data-ttu-id="56e3e-116">Die Anzahl von Zeilen und Spalten ist eine ganze Zahl ohne Vorzeichen zwischen 1 und 4 einschließlich.</span><span class="sxs-lookup"><span data-stu-id="56e3e-116">The number of rows and columns are unsigned integers between 1 and 4 inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="56e3e-117"><span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*Membername*</span><span class="sxs-lookup"><span data-stu-id="56e3e-117"><span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*MemberName*</span></span>
</dt> <dd>

<span data-ttu-id="56e3e-118">Eine ASCII-Zeichenfolge, die den Elementnamen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="56e3e-118">An ASCII string that uniquely identifies the member name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56e3e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56e3e-119">Remarks</span></span>

<span data-ttu-id="56e3e-120">Ein interpolationsmodifizierer kann für beliebige Strukturmember oder für ein Argument einer Pixel-Shader-Funktion angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="56e3e-120">An interpolation modifier can be specified on any structure member or on an argument to a pixel shader function.</span></span> <span data-ttu-id="56e3e-121">Wenn ein Modifizierer an beiden Stellen angezeigt wird, überschreibt der äußere Modifizierer (der Pixelshader-argumentmodifizierer) den in-Modifizierer (Strukturmodifizierer).</span><span class="sxs-lookup"><span data-stu-id="56e3e-121">If a modifier appears in both places, the outside modifier (the pixel shader argument modifier) overrules the inside modifier (the structure modifier).</span></span>

<span data-ttu-id="56e3e-122">Wenn ein Shader oder ein Effekt kompiliert wird, packt der Shader-Compiler Strukturelemente gemäß den [HLSL-Verpackungs Regeln](dx-graphics-hlsl-packing-rules.md).</span><span class="sxs-lookup"><span data-stu-id="56e3e-122">When compiling a shader or an effect, the shader compiler packs structure members according to [HLSL packing rules](dx-graphics-hlsl-packing-rules.md).</span></span>

### <a name="interpolation-modifiers-introduced-in-shader-model-4"></a><span data-ttu-id="56e3e-123">Im Shader-Modell 4 eingeführte Interpolations Modifizierer</span><span class="sxs-lookup"><span data-stu-id="56e3e-123">Interpolation Modifiers Introduced in Shader Model 4</span></span>

<span data-ttu-id="56e3e-124">Vertex-Shader-Ausgaben, die für Pixel-shadereingaben verwendet werden, werden linear interpoliert, um bei der rasterisierung pro Pixel-Werte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="56e3e-124">Vertex shader outputs that are used for pixel shader inputs are linearly interpolated to get per-pixel values during rasterization.</span></span> <span data-ttu-id="56e3e-125">Verwenden Sie zum Festlegen der Interpolationsmethode einen der folgenden Werte, die in [Shadermodell 4](dx-graphics-hlsl-sm4.md) oder höher unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="56e3e-125">To set the method of interpolation, use any of the following values, which are supported in [shader model 4](dx-graphics-hlsl-sm4.md) or later.</span></span> <span data-ttu-id="56e3e-126">Der-Modifizierer wird für jede Vertexshader-Ausgabe ignoriert, die nicht als Pixel-Shadereingabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="56e3e-126">The modifier is ignored on any vertex shader output that is not used as a pixel shader input.</span></span>



| <span data-ttu-id="56e3e-127">Interpolations Modifizierer</span><span class="sxs-lookup"><span data-stu-id="56e3e-127">Interpolation Modifier</span></span> | <span data-ttu-id="56e3e-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56e3e-128">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56e3e-129">**AK**</span><span class="sxs-lookup"><span data-stu-id="56e3e-129">**linear**</span></span>             | <span data-ttu-id="56e3e-130">Interpolieren zwischen shadereingaben; " **linear** " ist der Standardwert, wenn kein Interpolations Modifizierer angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="56e3e-130">Interpolate between shader inputs; **linear** is the default value if no interpolation modifier is specified.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="56e3e-131">**Schwerpunkt**</span><span class="sxs-lookup"><span data-stu-id="56e3e-131">**centroid**</span></span>           | <span data-ttu-id="56e3e-132">Interpolieren Sie zwischen Stichproben, die sich im abgedeckten Bereich des Pixels befinden (Dies erfordert möglicherweise das extrapolieren von Endpunkten von einem Pixel Center).</span><span class="sxs-lookup"><span data-stu-id="56e3e-132">Interpolate between samples that are somewhere within the covered area of the pixel (this may require extrapolating end points from a pixel center).</span></span> <span data-ttu-id="56e3e-133">Die Centroid-Stichprobenentnahme kann das Antialiasing verbessern, wenn ein Pixel teilweise abgedeckt wird (selbst wenn das Pixel Center nicht abgedeckt ist).</span><span class="sxs-lookup"><span data-stu-id="56e3e-133">Centroid sampling may improve antialiasing if a pixel is partially covered (even if the pixel center is not covered).</span></span> <span data-ttu-id="56e3e-134">Der **Schwerpunkt** -Modifizierer muss entweder mit dem **linearen** oder dem **noperktiven** -Modifizierer kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="56e3e-134">The **centroid** modifier must be combined with either the **linear** or **noperspective** modifier.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="56e3e-135">**nointerpolations**</span><span class="sxs-lookup"><span data-stu-id="56e3e-135">**nointerpolation**</span></span>    | <span data-ttu-id="56e3e-136">Nicht interpolieren.</span><span class="sxs-lookup"><span data-stu-id="56e3e-136">Do not interpolate .</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="56e3e-137">**noperer**</span><span class="sxs-lookup"><span data-stu-id="56e3e-137">**noperspective**</span></span>      | <span data-ttu-id="56e3e-138">Führen Sie während der Interpolations Zeit keine perspektivische Korrektur durch.</span><span class="sxs-lookup"><span data-stu-id="56e3e-138">Do not perform perspective-correction during interpolation.</span></span> <span data-ttu-id="56e3e-139">Der **noperspemodifizierer** kann mit dem **Schwerpunkt** -Modifizierer kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="56e3e-139">The **noperspective** modifier can be combined with the **centroid** modifier.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="56e3e-140">**Blutprobe**</span><span class="sxs-lookup"><span data-stu-id="56e3e-140">**sample**</span></span>             | <span data-ttu-id="56e3e-141">**Verfügbar im Shader-Modell 4,1 und** höher Interpolieren Sie an einer Beispiel Position statt im Pixel Center.</span><span class="sxs-lookup"><span data-stu-id="56e3e-141">**Available in shader model 4.1 and later** Interpolate at sample location rather than at the pixel center.</span></span> <span data-ttu-id="56e3e-142">Dies bewirkt, dass der Pixelshader pro-Stichprobe anstatt pro Pixel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56e3e-142">This causes the pixel shader to execute per-sample rather than per-pixel.</span></span> <span data-ttu-id="56e3e-143">Eine andere Möglichkeit, die Ausführung pro Stichprobe zu verursachen, besteht darin, eine Eingabe mit [Semantik SV \_ sampleindex](dx-graphics-hlsl-semantics.md)zu haben, die das aktuelle Beispiel angibt.</span><span class="sxs-lookup"><span data-stu-id="56e3e-143">Another way to cause per-sample execution is to have an input with [semantic SV\_SampleIndex](dx-graphics-hlsl-semantics.md), which indicates the current sample.</span></span> <span data-ttu-id="56e3e-144">Nur die Eingaben mit angegebenem **Beispiel** (bzw. das Einfügen von SV \_ sampleindex) unterscheiden sich zwischen shaderaufrufen im Pixel, während andere Eingaben, die keine Modifizierern angeben (z. b. Wenn Sie Modifizierern für verschiedene Eingaben mischen), immer noch im Pixel Center interpolieren.</span><span class="sxs-lookup"><span data-stu-id="56e3e-144">Only the inputs with **sample** specified (or inputting SV\_SampleIndex) differ between shader invocations in the pixel, whereas other inputs that do not specify modifiers (for example, if you mix modifiers on different inputs) still interpolate at the pixel center.</span></span> <span data-ttu-id="56e3e-145">Sowohl der Pixelshader-Aufruf als auch der tiefen-/Schablone-Test erfolgt für jedes abgedeckte Beispiel im Pixel.</span><span class="sxs-lookup"><span data-stu-id="56e3e-145">Both pixel shader invocation and depth/stencil testing occur for every covered sample in the pixel.</span></span> <span data-ttu-id="56e3e-146">Dies wird manchmal als *Supersampling* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="56e3e-146">This is sometimes known as *supersampling*.</span></span> <span data-ttu-id="56e3e-147">Im Gegensatz dazu wird der Pixelshader beim Fehlen von Sample Frequency-aufrufen, die als *mehrfach Stichprobe* bezeichnet werden, einmal pro Pixel aufgerufen, unabhängig davon, wie viele Stichproben abgedeckt werden, während tiefe-/Schablone-Tests bei der Stichproben Häufigkeit stattfinden.</span><span class="sxs-lookup"><span data-stu-id="56e3e-147">In contrast, in the absence of sample frequency invocation, known as *multisampling*, the pixel shader is invoked once per pixel regardless of how many samples are covered, while depth/stencil testing occurs at sample frequency.</span></span> <span data-ttu-id="56e3e-148">Beide Modi bieten äquivalente Edge-Antialiasing.</span><span class="sxs-lookup"><span data-stu-id="56e3e-148">Both modes provide equivalent edge antialiasing.</span></span> <span data-ttu-id="56e3e-149">Supersampling bietet jedoch eine bessere Schattierungs Qualität, indem der Pixelshader häufiger aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="56e3e-149">However, supersampling provides better shading quality by invoking the pixel shader more frequently.</span></span><br/> |



 

<dl> <span data-ttu-id="56e3e-150">1.Wenn ein int/uint-Typ verwendet wird, ist die einzige gültige Option **nointerpolation.**</span><span class="sxs-lookup"><span data-stu-id="56e3e-150">1. When using an int/uint type, the only valid option is **nointerpolation**.</span></span>  
</dl>

<span data-ttu-id="56e3e-151">Interpolations Modifizierer können auf Strukturmember oder [Funktionsargumente](dx-graphics-hlsl-function-parameters.md)oder beides angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="56e3e-151">Interpolation modifiers can be applied to structure members or [function arguments](dx-graphics-hlsl-function-parameters.md), or both.</span></span>

## <a name="examples"></a><span data-ttu-id="56e3e-152">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56e3e-152">Examples</span></span>

<span data-ttu-id="56e3e-153">Hier sind einige Beispiel Struktur Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="56e3e-153">Here are some example structure declarations.</span></span>


```
struct struct1
{
  int    a;
}
```



<span data-ttu-id="56e3e-154">Diese Deklaration enthält ein Array.</span><span class="sxs-lookup"><span data-stu-id="56e3e-154">This declaration includes an array.</span></span>


```
struct struct2
{
  int    a;
  float  b;
  int4x4 iMatrix;
}
```



<span data-ttu-id="56e3e-155">Diese Deklaration enthält einen Interpolations Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="56e3e-155">This declaration includes an interpolation modifier.</span></span>


```
struct In
{
  centroid float2 Texcoord;
};
```



## <a name="see-also"></a><span data-ttu-id="56e3e-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="56e3e-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56e3e-157">Datentypen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="56e3e-157">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





