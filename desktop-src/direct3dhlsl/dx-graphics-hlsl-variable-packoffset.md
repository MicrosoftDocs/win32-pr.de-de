---
title: packoffset
description: Optionales Shader-Schlüsselwort für konstantes Packen, das die folgende Syntax verwendet
ms.assetid: f0a3031b-d385-430d-83ee-7a8142334ad7
keywords:
- packoffset HLSL
topic_type:
- apiref
api_name:
- packoffset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c92a6375f0724a1910fc0f09b47e1593614f9f1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826079"
---
# <a name="packoffset"></a><span data-ttu-id="70c8d-104">packoffset</span><span class="sxs-lookup"><span data-stu-id="70c8d-104">packoffset</span></span>

<span data-ttu-id="70c8d-105">Optionales Shader-Schlüsselwort für konstantes Packen, das die folgende Syntax verwendet:</span><span class="sxs-lookup"><span data-stu-id="70c8d-105">Optional shader constant packing keyword, which uses the following syntax:</span></span>

<span data-ttu-id="70c8d-106">: packoffset( c \[ Subcomponent \] \[ .component \] )</span><span class="sxs-lookup"><span data-stu-id="70c8d-106">: packoffset( c\[Subcomponent\]\[.component\] )</span></span>



 

## <a name="parameters"></a><span data-ttu-id="70c8d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="70c8d-107">Parameters</span></span>



| <span data-ttu-id="70c8d-108">Element</span><span class="sxs-lookup"><span data-stu-id="70c8d-108">Item</span></span>                                                                                                                                                                                 | <span data-ttu-id="70c8d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70c8d-109">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70c8d-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span><span class="sxs-lookup"><span data-stu-id="70c8d-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span></span><br/>                                                                                                  | <span data-ttu-id="70c8d-111">Erforderliches Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="70c8d-111">Required keyword.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="70c8d-112"><span id="c"></span><span id="C"></span>**C**</span><span class="sxs-lookup"><span data-stu-id="70c8d-112"><span id="c"></span><span id="C"></span>**c**</span></span><br/>                                                                                                                             | <span data-ttu-id="70c8d-113">Das Packen gilt nur für konstante Register (c).</span><span class="sxs-lookup"><span data-stu-id="70c8d-113">Packing applies to constant registers (c) only.</span></span> <br/>                                                                                          |
| <span data-ttu-id="70c8d-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Komponente der \] \[ Unterkomponente\]**</span><span class="sxs-lookup"><span data-stu-id="70c8d-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Subcomponent\]\[.component\]**</span></span><br/> | <span data-ttu-id="70c8d-115">Optionale Unterkomponenten und Komponenten.</span><span class="sxs-lookup"><span data-stu-id="70c8d-115">Optional subcomponents and components.</span></span> <span data-ttu-id="70c8d-116">Eine Unterkomponenten ist eine Registernummer, die eine ganze Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="70c8d-116">A subcomponent is a register number, which is an integer.</span></span> <span data-ttu-id="70c8d-117">Eine Komponente hat die Form \[ .xyzw \] .</span><span class="sxs-lookup"><span data-stu-id="70c8d-117">A component is in the form of \[.xyzw\].</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="70c8d-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="70c8d-118">Remarks</span></span>

<span data-ttu-id="70c8d-119">Verwenden Sie dieses Schlüsselwort, um beim Deklarieren eines Variablentyps manuell eine [Shaderkonstance zu packen.](dx-graphics-hlsl-variable-syntax.md)</span><span class="sxs-lookup"><span data-stu-id="70c8d-119">Use this keyword to manually pack a shader constant when [declaring a variable type](dx-graphics-hlsl-variable-syntax.md).</span></span>

<span data-ttu-id="70c8d-120">Beim Packen einer Konstante können Sie keine konstanten Typen mischen.</span><span class="sxs-lookup"><span data-stu-id="70c8d-120">When packing a constant, you cannot mix constant types.</span></span>

<span data-ttu-id="70c8d-121">Der Compiler verhält sich für globale Konstanten und einheitliche Konstanten etwas anders:</span><span class="sxs-lookup"><span data-stu-id="70c8d-121">The compiler behaves slightly differently for global constants and uniform constants:</span></span>

-   <span data-ttu-id="70c8d-122">Eine globale Konstante.</span><span class="sxs-lookup"><span data-stu-id="70c8d-122">A global constant.</span></span> <span data-ttu-id="70c8d-123">Eine globale Variable wird als globale Konstante zu einem $Global *vom* Compiler hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="70c8d-123">A global variable is added as a global constant to a *$Global* cbuffer by the compiler.</span></span> <span data-ttu-id="70c8d-124">Automatisch gepackte Elemente (die ohne packoffset deklariert sind) werden nach der zuletzt manuell gepackten Variablen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="70c8d-124">Automatically packed elements (those declared without packoffset) will appear after the last manually packed variable.</span></span> <span data-ttu-id="70c8d-125">Sie können Typen beim Packen globaler Konstanten mischen.</span><span class="sxs-lookup"><span data-stu-id="70c8d-125">You may mix types when packing global constants.</span></span>
-   <span data-ttu-id="70c8d-126">Eine einheitliche Konstante.</span><span class="sxs-lookup"><span data-stu-id="70c8d-126">A uniform constant.</span></span> <span data-ttu-id="70c8d-127">Ein einheitlicher Parameter in der Parameterliste einer Funktion wird einem *$Param* konstanten Puffer vom Compiler hinzugefügt, wenn der Shader außerhalb des Effektframework kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="70c8d-127">A uniform parameter in the parameter list of a function will be added to a *$Param* constant buffer by the compiler when the shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="70c8d-128">Bei der Kompilierung innerhalb des Effektframework muss eine einheitliche Konstante in eine im globalen Gültigkeitsbereich definierte einheitliche Variable auflösen.</span><span class="sxs-lookup"><span data-stu-id="70c8d-128">When compiled inside the effect framework, a uniform constant must resolve to a uniform variable defined in global scope.</span></span> <span data-ttu-id="70c8d-129">Eine einheitliche Konstante kann nicht manuell versetzt werden. ihre empfohlenen Verwendung ist nur für die Spezialisierung von Shadern, bei denen sie einen Alias zurück zu globalen Namen erstellen, und nicht als Mittel zur Übergabe von Anwendungsdaten an den Shader.</span><span class="sxs-lookup"><span data-stu-id="70c8d-129">A uniform constant cannot be manually offset; their recommend use is only for specialization of shaders where they alias back to globals, not as a means of passing application data into the shader.</span></span>

<span data-ttu-id="70c8d-130">Im Folgenden finden Sie einige zusätzliche Beispiele: [Packen von Konstanten mithilfe des Shadermodells 4](dx-graphics-hlsl-packing-rules.md).</span><span class="sxs-lookup"><span data-stu-id="70c8d-130">Here are some additional examples: [packing constants using shader model 4](dx-graphics-hlsl-packing-rules.md).</span></span>

## <a name="examples"></a><span data-ttu-id="70c8d-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70c8d-131">Examples</span></span>

<span data-ttu-id="70c8d-132">Im Folgenden finden Sie einige Beispiele für das manuelle Packen von Shaderkonst constants.</span><span class="sxs-lookup"><span data-stu-id="70c8d-132">Here are several examples of manually packing shader constants.</span></span>

<span data-ttu-id="70c8d-133">Packen Sie Unterkomponenten von Vektoren und Skalaren, deren Größe groß genug ist, um das Überschreiten von Registergrenzen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="70c8d-133">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundaries.</span></span> <span data-ttu-id="70c8d-134">Dies sind beispielsweise alle gültig:</span><span class="sxs-lookup"><span data-stu-id="70c8d-134">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
```



## <a name="see-also"></a><span data-ttu-id="70c8d-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70c8d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70c8d-136">Variablensyntax</span><span class="sxs-lookup"><span data-stu-id="70c8d-136">Variable Syntax</span></span>](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[<span data-ttu-id="70c8d-137">Variablen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="70c8d-137">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 





