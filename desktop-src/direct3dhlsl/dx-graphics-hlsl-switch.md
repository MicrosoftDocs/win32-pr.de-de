---
title: switch-Anweisung (Urlmon.h)
description: Übertragen Sie die Steuerung abhängig vom Wert eines Selektors in einen anderen Anweisungsblock innerhalb des Switch-Textkörpers.
ms.assetid: d1932ee1-d789-4536-b77d-162aacdbb115
keywords:
- switch-Anweisung HLSL
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
ms.openlocfilehash: 4af131ca3a126cd6f1fd54160418bfbe70cc9cce
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119085"
---
# <a name="switch-statement"></a><span data-ttu-id="aba28-104">switch-Anweisung</span><span class="sxs-lookup"><span data-stu-id="aba28-104">switch Statement</span></span>

<span data-ttu-id="aba28-105">Übertragen Sie die Steuerung abhängig vom Wert eines Selektors in einen anderen Anweisungsblock innerhalb des Switch-Textkörpers.</span><span class="sxs-lookup"><span data-stu-id="aba28-105">Transfer control to a different statement block within the switch body depending on the value of a selector.</span></span>


<span data-ttu-id="aba28-106">\[*Attribut* \] switch( *Selector* ) { case 0 : { *StatementBlock*; }   break;   Fall 1: { *StatementBlock*; }   break;   case n : { *StatementBlock*; }   break;   default: { *StatementBlock;*}   break;</span><span class="sxs-lookup"><span data-stu-id="aba28-106">\[*Attribute*\] switch( *Selector* ) {   case 0 :     { *StatementBlock*; }   break;   case 1 :     { *StatementBlock*; }   break;   case n :     { *StatementBlock*; }   break;   default :     { *StatementBlock*; }   break;</span></span>



 

## <a name="parameters"></a><span data-ttu-id="aba28-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="aba28-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aba28-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*</span><span class="sxs-lookup"><span data-stu-id="aba28-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="aba28-109">Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="aba28-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="aba28-110">Wenn kein Attribut angegeben ist, kann der Compiler einen Hardwareschalter verwenden oder eine Reihe von **if-Anweisungen** aus geben.</span><span class="sxs-lookup"><span data-stu-id="aba28-110">When no attribute is specified, the compiler may use a hardware switch or emit a series of **if** statements.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aba28-111">attribute</span><span class="sxs-lookup"><span data-stu-id="aba28-111">Attribute</span></span></th>
<th><span data-ttu-id="aba28-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aba28-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aba28-113">Vereinfachen</span><span class="sxs-lookup"><span data-stu-id="aba28-113">flatten</span></span></td>
<td><span data-ttu-id="aba28-114">Kompilieren Sie die <strong></strong> -Anweisung als eine Reihe von if-Anweisungen, die jeweils das <strong>flatten-Attribut</strong> enthalten.</span><span class="sxs-lookup"><span data-stu-id="aba28-114">Compile the statement as a series of <strong>if</strong> statements, each with the <strong>flatten</strong> attribute.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aba28-115">Verzweigung</span><span class="sxs-lookup"><span data-stu-id="aba28-115">branch</span></span></td>
<td><span data-ttu-id="aba28-116">Kompilieren Sie die <strong></strong> -Anweisung als eine Reihe von if-Anweisungen, die jeweils das <strong>Branchattribut</strong> enthalten.</span><span class="sxs-lookup"><span data-stu-id="aba28-116">Compile the statement as a series of <strong>if</strong> statements each with the <strong>branch</strong> attribute.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="aba28-117">Wenn Sie <a href="dx-graphics-hlsl-sm2.md">shader Model 2.x</a> oder <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>verwenden, nutzen Sie bei jeder Verwendung dynamischer Verzweigung Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="aba28-117">When you use <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> or <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, each time you use dynamic branching you consume resources.</span></span> <span data-ttu-id="aba28-118">Wenn Sie dynamische Verzweigung also übermäßig verwenden, wenn Sie diese Profile als Ziel verwenden, können Kompilierungsfehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="aba28-118">So, if you use dynamic branching excessively when you target these profiles, you can receive compilation errors.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aba28-119">forcecase</span><span class="sxs-lookup"><span data-stu-id="aba28-119">forcecase</span></span></td>
<td><span data-ttu-id="aba28-120">Erzwingen Sie eine Switch-Anweisung in der Hardware.</span><span class="sxs-lookup"><span data-stu-id="aba28-120">Force a switch statement in the hardware.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="aba28-121">Erfordert <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">Hardware auf Featureebene</a> 10_0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="aba28-121">Requires <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10_0 or later hardware.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aba28-122">Aufruf</span><span class="sxs-lookup"><span data-stu-id="aba28-122">call</span></span></td>
<td><span data-ttu-id="aba28-123">Die Körper der einzelnen Fälle im Switch werden in Hardwareunterroutinen verschoben, und der Switch ist eine Reihe von Unterroutinenaufrufen.</span><span class="sxs-lookup"><span data-stu-id="aba28-123">The bodies of the individual cases in the switch will be moved into hardware subroutines and the switch will be a series of subroutine calls.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="aba28-124">Erfordert <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">Hardware auf Featureebene</a> 10_0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="aba28-124">Requires <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10_0 or later hardware.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="aba28-125"><span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Selector*</span><span class="sxs-lookup"><span data-stu-id="aba28-125"><span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Selector*</span></span>
</dt> <dd>

<span data-ttu-id="aba28-126">Eine Variable.</span><span class="sxs-lookup"><span data-stu-id="aba28-126">A variable.</span></span> <span data-ttu-id="aba28-127">Die case-Anweisungen in den eckigen Klammern überprüfen jeweils diese Variable, um zu überprüfen, ob switchValue mit ihrem jeweiligen CaseValue-Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="aba28-127">The case statements inside the curly brackets will each check this variable to see if the SwitchValue matches their particular CaseValue.</span></span>

</dd> <dt>

<span data-ttu-id="aba28-128"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span><span class="sxs-lookup"><span data-stu-id="aba28-128"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="aba28-129">Mindestens eine [-Anweisung.](dx-graphics-hlsl-statement-blocks.md)</span><span class="sxs-lookup"><span data-stu-id="aba28-129">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aba28-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aba28-130">Remarks</span></span>


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



<span data-ttu-id="aba28-131">Entspricht:</span><span class="sxs-lookup"><span data-stu-id="aba28-131">Is equivalent to:</span></span>


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



<span data-ttu-id="aba28-132">Im Folgenden finden Sie Beispielverwendungen von ForceCase- und Aufrufflusssteuerungsattributen:</span><span class="sxs-lookup"><span data-stu-id="aba28-132">Here are example usages of forcecase and call flow control attributes:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="aba28-133">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="aba28-133">Requirements</span></span>



| <span data-ttu-id="aba28-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aba28-134">Requirement</span></span> | <span data-ttu-id="aba28-135">Wert</span><span class="sxs-lookup"><span data-stu-id="aba28-135">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aba28-136">Header</span><span class="sxs-lookup"><span data-stu-id="aba28-136">Header</span></span><br/> | <dl> <span data-ttu-id="aba28-137"><dt>Urlmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="aba28-137"><dt>Urlmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aba28-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aba28-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aba28-139">Flusssteuerung</span><span class="sxs-lookup"><span data-stu-id="aba28-139">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

