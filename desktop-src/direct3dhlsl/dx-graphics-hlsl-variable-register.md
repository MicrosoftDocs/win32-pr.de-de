---
title: Registrieren
description: Registrieren
ms.assetid: 45149f8c-8b76-4247-98d7-d141d7268da3
keywords:
- HLSL registrieren
topic_type:
- apiref
api_name:
- register
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b378cd97bc9779951d62873d393009c98d32823
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390347"
---
# <a name="register"></a><span data-ttu-id="9b99c-104">Registrieren</span><span class="sxs-lookup"><span data-stu-id="9b99c-104">register</span></span>

<span data-ttu-id="9b99c-105">Optionales Schlüsselwort zum Zuweisen einer shadervariablen zu einem bestimmten Register, das folgende Syntax verwendet:</span><span class="sxs-lookup"><span data-stu-id="9b99c-105">Optional keyword for assigning a shader variable to a particular register, which uses the following syntax:</span></span>



| <span data-ttu-id="9b99c-106">: Register ( *\[ Shader \_ - \] Profil*, *Typ \# \[ unter \] Komponente* )</span><span class="sxs-lookup"><span data-stu-id="9b99c-106">: register ( *\[shader\_profile\]*, *Type\#\[subcomponent\]* )</span></span> |
|----------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="9b99c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b99c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b99c-108"><span id="register"></span><span id="REGISTER"></span>sich</span><span class="sxs-lookup"><span data-stu-id="9b99c-108"><span id="register"></span><span id="REGISTER"></span>register</span></span>
</dt> <dd>

<span data-ttu-id="9b99c-109">Erforderliches Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="9b99c-109">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="9b99c-110"><span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[Shader- \_ Profil\]*</span><span class="sxs-lookup"><span data-stu-id="9b99c-110"><span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[shader\_profile\]*</span></span>
</dt> <dd>

<span data-ttu-id="9b99c-111">Optionales [Shader-Profil](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax), das ein Shader-Ziel oder einfach **PS** oder **vs** sein kann</span><span class="sxs-lookup"><span data-stu-id="9b99c-111">Optional [shader profile](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax), which can be a shader target or simply **ps** or **vs**.</span></span>

</dd> <dt>

<span data-ttu-id="9b99c-112"><span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*\# \[ Typsubcomponent\]*</span><span class="sxs-lookup"><span data-stu-id="9b99c-112"><span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*Type\#\[subcomponent\]*</span></span>
</dt> <dd>

<span data-ttu-id="9b99c-113">Registrieren Sie den Typ, die Zahl und die unter Komponenten Deklaration.</span><span class="sxs-lookup"><span data-stu-id="9b99c-113">Register type, number, and subcomponent declaration.</span></span>

-   <span data-ttu-id="9b99c-114">Der Typ ist einer der folgenden:</span><span class="sxs-lookup"><span data-stu-id="9b99c-114">Type is one of the following:</span></span>

    

    | <span data-ttu-id="9b99c-115">type</span><span class="sxs-lookup"><span data-stu-id="9b99c-115">Type</span></span> | <span data-ttu-id="9b99c-116">Register Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b99c-116">Register Description</span></span>       |
    |------|----------------------------|
    | <span data-ttu-id="9b99c-117">b</span><span class="sxs-lookup"><span data-stu-id="9b99c-117">b</span></span>    | <span data-ttu-id="9b99c-118">Konstanter Puffer</span><span class="sxs-lookup"><span data-stu-id="9b99c-118">Constant buffer</span></span>            |
    | <span data-ttu-id="9b99c-119">t</span><span class="sxs-lookup"><span data-stu-id="9b99c-119">t</span></span>    | <span data-ttu-id="9b99c-120">Textur-und Textur Puffer</span><span class="sxs-lookup"><span data-stu-id="9b99c-120">Texture and texture buffer</span></span> |
    | <span data-ttu-id="9b99c-121">c</span><span class="sxs-lookup"><span data-stu-id="9b99c-121">c</span></span>    | <span data-ttu-id="9b99c-122">Puffer Offset</span><span class="sxs-lookup"><span data-stu-id="9b99c-122">Buffer offset</span></span>              |
    | <span data-ttu-id="9b99c-123">s</span><span class="sxs-lookup"><span data-stu-id="9b99c-123">s</span></span>    | <span data-ttu-id="9b99c-124">Sampler</span><span class="sxs-lookup"><span data-stu-id="9b99c-124">Sampler</span></span>                    |
    | <span data-ttu-id="9b99c-125">u</span><span class="sxs-lookup"><span data-stu-id="9b99c-125">u</span></span>    | <span data-ttu-id="9b99c-126">Ansicht für ungeordnete Zugriffe</span><span class="sxs-lookup"><span data-stu-id="9b99c-126">Unordered Access View</span></span>      |

    

     

-   <span data-ttu-id="9b99c-127">*\#* die Registernummer, bei der es sich um eine ganzzahlige Zahl handelt.</span><span class="sxs-lookup"><span data-stu-id="9b99c-127">*\#* is the register number, which is an integer number.</span></span>
-   <span data-ttu-id="9b99c-128">Die *Unterkomponente* ist eine optionale ganzzahlige Zahl.</span><span class="sxs-lookup"><span data-stu-id="9b99c-128">The *subcomponent* is an optional integer number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b99c-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b99c-129">Remarks</span></span>

<span data-ttu-id="9b99c-130">Sie können einer Variablen Deklaration eine oder mehrere Registrierungs Zuweisungen hinzufügen, die durch Leerzeichen getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="9b99c-130">You may add one or more register assignments to the same variable declaration, separated by spaces.</span></span>

<span data-ttu-id="9b99c-131">Bei Direct3D 10-Variablen im globalen Gültigkeitsbereich verhält sich das **Register** -Schlüsselwort genauso wie das Schlüsselwort " [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) ".</span><span class="sxs-lookup"><span data-stu-id="9b99c-131">For Direct3D 10 variables in global scope, the **register** keyword acts the same as the [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) keyword.</span></span>

## <a name="examples"></a><span data-ttu-id="9b99c-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b99c-132">Examples</span></span>

<span data-ttu-id="9b99c-133">Hier einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="9b99c-133">Here are some examples:</span></span>


```
sampler myVar : register( ps_5_0, s ); 
```




```
sampler myVar : register( vs, s[8] );
```




```
sampler myVar : register( ps, s[2] ) 
              : register( ps_5_0, s[0] ) 
              : register( vs, s[8] );
```



## <a name="see-also"></a><span data-ttu-id="9b99c-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9b99c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b99c-135">Variablensyntax</span><span class="sxs-lookup"><span data-stu-id="9b99c-135">Variable Syntax</span></span>](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[<span data-ttu-id="9b99c-136">Variablen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b99c-136">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 