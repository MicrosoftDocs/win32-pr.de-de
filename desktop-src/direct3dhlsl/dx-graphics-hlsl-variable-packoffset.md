---
title: packoffset
description: 'Optionales Shader Constant Packaging-Schlüsselwort, das die folgende Syntax verwendet:'
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
ms.openlocfilehash: 6feeaa586abe30fa8a36c28d0298dc408cdfb099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312461"
---
# <a name="packoffset"></a><span data-ttu-id="5319c-104">packoffset</span><span class="sxs-lookup"><span data-stu-id="5319c-104">packoffset</span></span>

<span data-ttu-id="5319c-105">Optionales Shader Constant Packaging-Schlüsselwort, das die folgende Syntax verwendet:</span><span class="sxs-lookup"><span data-stu-id="5319c-105">Optional shader constant packing keyword, which uses the following syntax:</span></span>



|                                                 |
|-------------------------------------------------|
| <span data-ttu-id="5319c-106">: packoffset (c- \[ Unterkomponente \] \[ . Component \] )</span><span class="sxs-lookup"><span data-stu-id="5319c-106">: packoffset( c\[Subcomponent\]\[.component\] )</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="5319c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5319c-107">Parameters</span></span>



| <span data-ttu-id="5319c-108">Element</span><span class="sxs-lookup"><span data-stu-id="5319c-108">Item</span></span>                                                                                                                                                                                 | <span data-ttu-id="5319c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5319c-109">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5319c-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span><span class="sxs-lookup"><span data-stu-id="5319c-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span></span><br/>                                                                                                  | <span data-ttu-id="5319c-111">Erforderliches Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="5319c-111">Required keyword.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="5319c-112"><span id="c"></span><span id="C"></span>**scher**</span><span class="sxs-lookup"><span data-stu-id="5319c-112"><span id="c"></span><span id="C"></span>**c**</span></span><br/>                                                                                                                             | <span data-ttu-id="5319c-113">Die Verpackung gilt nur für konstante Register (c).</span><span class="sxs-lookup"><span data-stu-id="5319c-113">Packing applies to constant registers (c) only.</span></span> <br/>                                                                                          |
| <span data-ttu-id="5319c-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Subcomponent \] \[ . Component\]**</span><span class="sxs-lookup"><span data-stu-id="5319c-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Subcomponent\]\[.component\]**</span></span><br/> | <span data-ttu-id="5319c-115">Optionale unter Komponenten und Komponenten.</span><span class="sxs-lookup"><span data-stu-id="5319c-115">Optional subcomponents and components.</span></span> <span data-ttu-id="5319c-116">Eine Unterkomponente ist eine Registernummer, bei der es sich um eine ganze Zahl handelt.</span><span class="sxs-lookup"><span data-stu-id="5319c-116">A subcomponent is a register number, which is an integer.</span></span> <span data-ttu-id="5319c-117">Eine Komponente hat die Form " \[ . xyzw" \] .</span><span class="sxs-lookup"><span data-stu-id="5319c-117">A component is in the form of \[.xyzw\].</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5319c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5319c-118">Remarks</span></span>

<span data-ttu-id="5319c-119">Verwenden Sie dieses Schlüsselwort, um beim [Deklarieren eines Variablen Typs](dx-graphics-hlsl-variable-syntax.md)eine shaderkonstante manuell zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="5319c-119">Use this keyword to manually pack a shader constant when [declaring a variable type](dx-graphics-hlsl-variable-syntax.md).</span></span>

<span data-ttu-id="5319c-120">Beim Verpacken einer Konstanten können keine Konstanten Typen gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="5319c-120">When packing a constant, you cannot mix constant types.</span></span>

<span data-ttu-id="5319c-121">Der Compiler verhält sich bei globalen Konstanten und einheitlichen Konstanten etwas anders:</span><span class="sxs-lookup"><span data-stu-id="5319c-121">The compiler behaves slightly differently for global constants and uniform constants:</span></span>

-   <span data-ttu-id="5319c-122">Eine globale Konstante.</span><span class="sxs-lookup"><span data-stu-id="5319c-122">A global constant.</span></span> <span data-ttu-id="5319c-123">Eine globale Variable wird einem *$Global* cBuffer vom Compiler als globale Konstante hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5319c-123">A global variable is added as a global constant to a *$Global* cbuffer by the compiler.</span></span> <span data-ttu-id="5319c-124">Automatisch gepackte Elemente (die ohne packoffset deklariert werden) werden nach der letzten manuell gepackten Variable angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5319c-124">Automatically packed elements (those declared without packoffset) will appear after the last manually packed variable.</span></span> <span data-ttu-id="5319c-125">Beim Packen von globalen Konstanten können Typen gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="5319c-125">You may mix types when packing global constants.</span></span>
-   <span data-ttu-id="5319c-126">Eine einheitliche Konstante.</span><span class="sxs-lookup"><span data-stu-id="5319c-126">A uniform constant.</span></span> <span data-ttu-id="5319c-127">Ein einheitlicher Parameter in der Parameterliste einer Funktion wird dem *$param* Konstanten Puffer vom Compiler hinzugefügt, wenn der Shader außerhalb des Effects-Frameworks kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="5319c-127">A uniform parameter in the parameter list of a function will be added to a *$Param* constant buffer by the compiler when the shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="5319c-128">Bei der Kompilierung innerhalb des Effect-Frameworks muss eine einheitliche Konstante in eine im globalen Gültigkeitsbereich definierte einheitliche Variable aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="5319c-128">When compiled inside the effect framework, a uniform constant must resolve to a uniform variable defined in global scope.</span></span> <span data-ttu-id="5319c-129">Eine einheitliche Konstante kann nicht manuell versetzt werden. die empfohlene Verwendung ist nur für die Spezialisierung von Shadern, bei denen Sie an globale Daten zurückgegeben werden, nicht als Mittel zum Übergeben von Anwendungsdaten an den Shader.</span><span class="sxs-lookup"><span data-stu-id="5319c-129">A uniform constant cannot be manually offset; their recommend use is only for specialization of shaders where they alias back to globals, not as a means of passing application data into the shader.</span></span>

<span data-ttu-id="5319c-130">Hier sind einige zusätzliche Beispiele: [Verpacken von Konstanten mithilfe von Shadermodell 4](dx-graphics-hlsl-packing-rules.md).</span><span class="sxs-lookup"><span data-stu-id="5319c-130">Here are some additional examples: [packing constants using shader model 4](dx-graphics-hlsl-packing-rules.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5319c-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5319c-131">Examples</span></span>

<span data-ttu-id="5319c-132">Im folgenden finden Sie einige Beispiele für das manuelle Packen von shaderkonstanten.</span><span class="sxs-lookup"><span data-stu-id="5319c-132">Here are several examples of manually packing shader constants.</span></span>

<span data-ttu-id="5319c-133">Pack-unter Komponenten von Vektoren und skalaren, deren Größe groß genug ist, um das Überschreiten von Registrierungs Grenzen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="5319c-133">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundaries.</span></span> <span data-ttu-id="5319c-134">Diese sind z. b. gültig:</span><span class="sxs-lookup"><span data-stu-id="5319c-134">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
```



## <a name="see-also"></a><span data-ttu-id="5319c-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5319c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5319c-136">Variablensyntax</span><span class="sxs-lookup"><span data-stu-id="5319c-136">Variable Syntax</span></span>](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[<span data-ttu-id="5319c-137">Variablen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5319c-137">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 





