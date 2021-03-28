---
title: Switch-Anweisung (Urlmon. h)
description: Überträgt die Steuerung abhängig vom Wert eines Selektor an einen anderen Anweisungsblock innerhalb des Switch-Texts.
ms.assetid: d1932ee1-d789-4536-b77d-162aacdbb115
keywords:
- Switch-Anweisung HLSL
topic_type:
- apiref
api_name:
- switch Statement
api_location:
- urlmon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c65049acce4265dd2abdf849119aad5902db9e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761922"
---
# <a name="switch-statement"></a><span data-ttu-id="8cf2a-104">switch-Anweisung</span><span class="sxs-lookup"><span data-stu-id="8cf2a-104">switch Statement</span></span>

<span data-ttu-id="8cf2a-105">Überträgt die Steuerung abhängig vom Wert eines Selektor an einen anderen Anweisungsblock innerhalb des Switch-Texts.</span><span class="sxs-lookup"><span data-stu-id="8cf2a-105">Transfer control to a different statement block within the switch body depending on the value of a selector.</span></span>



|                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf2a-106">\[*Attribut* \] Switch ( *Selektor* ) {Case 0: { *Status Block*;}   Umbruch   Fall 1: { *Status Block*;}   Umbruch   Fall n: { *Status Block*;}   Umbruch   Standard: { *Status Block*;}   Umbruch</span><span class="sxs-lookup"><span data-stu-id="8cf2a-106">\[*Attribute*\] switch( *Selector* ) {   case 0 :     { *StatementBlock*; }   break;   case 1 :     { *StatementBlock*; }   break;   case n :     { *StatementBlock*; }   break;   default :     { *StatementBlock*; }   break;</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="8cf2a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cf2a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cf2a-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Versehen*</span><span class="sxs-lookup"><span data-stu-id="8cf2a-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="8cf2a-109">Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="8cf2a-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="8cf2a-110">Wenn kein Attribut angegeben ist, verwendet der Compiler möglicherweise einen Hardware Switch oder gibt eine Reihe von **if** -Anweisungen aus.</span><span class="sxs-lookup"><span data-stu-id="8cf2a-110">When no attribute is specified, the compiler may use a hardware switch or emit a series of **if** statements.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8cf2a-111">attribute</span><span class="sxs-lookup"><span data-stu-id="8cf2a-111">Attribute</span></span></th>
<th><span data-ttu-id="8cf2a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8cf2a-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8cf2a-113">Vereinfachen</span><span class="sxs-lookup"><span data-stu-id="8cf2a-113">flatten</span></span></td>
<td><span data-ttu-id="8cf2a-114">Kompilieren Sie die Anweisung als eine Reihe von <strong>if</strong> -Anweisungen, die jeweils das <strong>vereinfachen</strong> -Attribut haben.</span><span class="sxs-lookup"><span data-stu-id="8cf2a-114">Compile the statement as a series of <strong>if</strong> statements, each with the <strong>flatten</strong> attribute.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cf2a-115">Verzweigung</span><span class="sxs-lookup"><span data-stu-id="8cf2a-115">branch</span></span></td>
<td><span data-ttu-id="8cf2a-116">Kompilieren Sie die-Anweisung als eine Reihe von <strong>if</strong> -Anweisungen, die jeweils das <strong>Branch</strong> -Attribut haben.</span><span class="sxs-lookup"><span data-stu-id="8cf2a-116">Compile the statement as a series of <strong>if</strong> statements each with the <strong>branch</strong> attribute.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="8cf2a-117">Wenn Sie das <a href="dx-graphics-hlsl-sm2.md">Shadermodell 2. x</a> oder das <a href="dx-graphics-hlsl-sm3.md">Shader-Modell 3,0</a>verwenden, verwenden Sie jedes Mal, wenn Sie dynamische Verzweigungen verwenden, Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="8cf2a-117">When you use <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> or <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, each time you use dynamic branching you consume resources.</span></span> <span data-ttu-id="8cf2a-118">Wenn Sie also die dynamische Verzweigung übermäßig verwenden, wenn Sie diese Profile als Ziel verwenden, können Sie Kompilierungsfehler erhalten.</span><span class="sxs-lookup"><span data-stu-id="8cf2a-118">So, if you use dynamic branching excessively when you target these profiles, you can receive compilation errors.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8cf2a-119">forcecase</span><span class="sxs-lookup"><span data-stu-id="8cf2a-119">forcecase</span></span></td>
<td><span data-ttu-id="8cf2a-120">Erzwingen Sie eine Switch-Anweisung in der Hardware.</span><span class="sxs-lookup"><span data-stu-id="8cf2a-120">Force a switch statement in the hardware.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="8cf2a-121">Erfordert 10_0 oder <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">höhere</a> Hardware.</span><span class="sxs-lookup"><span data-stu-id="8cf2a-121">Requires <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10_0 or later hardware.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cf2a-122">Aufruf</span><span class="sxs-lookup"><span data-stu-id="8cf2a-122">call</span></span></td>
<td><span data-ttu-id="8cf2a-123">Die Textteile der einzelnen Fälle im Switch werden in Hardware Unterroutinen verschoben, und der Switch ist eine Reihe von Unterroutine aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8cf2a-123">The bodies of the individual cases in the switch will be moved into hardware subroutines and the switch will be a series of subroutine calls.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="8cf2a-124">Erfordert 10_0 oder <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">höhere</a> Hardware.</span><span class="sxs-lookup"><span data-stu-id="8cf2a-124">Requires <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10_0 or later hardware.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="8cf2a-125"><span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Ktor*</span><span class="sxs-lookup"><span data-stu-id="8cf2a-125"><span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Selector*</span></span>
</dt> <dd>

<span data-ttu-id="8cf2a-126">Eine Variable.</span><span class="sxs-lookup"><span data-stu-id="8cf2a-126">A variable.</span></span> <span data-ttu-id="8cf2a-127">Die Case-Anweisungen innerhalb der geschweiften Klammern prüfen jeweils diese Variable, um festzustellen, ob der switchValue mit dem jeweiligen casevalue übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="8cf2a-127">The case statements inside the curly brackets will each check this variable to see if the SwitchValue matches their particular CaseValue.</span></span>

</dd> <dt>

<span data-ttu-id="8cf2a-128"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*Status Block*</span><span class="sxs-lookup"><span data-stu-id="8cf2a-128"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="8cf2a-129">Eine oder mehrere- [Anweisungen](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="8cf2a-129">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cf2a-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8cf2a-130">Remarks</span></span>


```
[branch] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



<span data-ttu-id="8cf2a-131">Entspricht:</span><span class="sxs-lookup"><span data-stu-id="8cf2a-131">Is equivalent to:</span></span>


```
[branch] if( a == 2 )
    return 3;
else if( a == 1 )
    return 1;
else if( a == 0 )
    return 0;
else
    return 6;
```



<span data-ttu-id="8cf2a-132">Im folgenden finden Sie Beispiel Verwendungen von forcecase-und callflowcontrol-Attributen:</span><span class="sxs-lookup"><span data-stu-id="8cf2a-132">Here are example usages of forcecase and call flow control attributes:</span></span>


```
[forcecase] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}

[call] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



## <a name="requirements"></a><span data-ttu-id="8cf2a-133">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8cf2a-133">Requirements</span></span>



| <span data-ttu-id="8cf2a-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cf2a-134">Requirement</span></span> | <span data-ttu-id="8cf2a-135">Wert</span><span class="sxs-lookup"><span data-stu-id="8cf2a-135">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf2a-136">Header</span><span class="sxs-lookup"><span data-stu-id="8cf2a-136">Header</span></span><br/> | <dl> <span data-ttu-id="8cf2a-137"><dt>Urlmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cf2a-137"><dt>Urlmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cf2a-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8cf2a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cf2a-139">Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="8cf2a-139">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

