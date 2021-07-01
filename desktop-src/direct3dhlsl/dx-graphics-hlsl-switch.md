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
# <a name="switch-statement"></a>switch-Anweisung

Übertragen Sie die Steuerung abhängig vom Wert eines Selektors in einen anderen Anweisungsblock innerhalb des Switch-Textkörpers.


\[*Attribut* \] switch( *Selector* ) { case 0 : { *StatementBlock*; }   break;   Fall 1: { *StatementBlock*; }   break;   case n : { *StatementBlock*; }   break;   default: { *StatementBlock;*}   break;



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*
</dt> <dd>

Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird. Wenn kein Attribut angegeben ist, kann der Compiler einen Hardwareschalter verwenden oder eine Reihe von **if-Anweisungen** aus geben.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vereinfachen</td>
<td>Kompilieren Sie die <strong></strong> -Anweisung als eine Reihe von if-Anweisungen, die jeweils das <strong>flatten-Attribut</strong> enthalten.</td>
</tr>
<tr class="even">
<td>Verzweigung</td>
<td>Kompilieren Sie die <strong></strong> -Anweisung als eine Reihe von if-Anweisungen, die jeweils das <strong>Branchattribut</strong> enthalten.
<blockquote>
[!Note]<br />
Wenn Sie <a href="dx-graphics-hlsl-sm2.md">shader Model 2.x</a> oder <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>verwenden, nutzen Sie bei jeder Verwendung dynamischer Verzweigung Ressourcen. Wenn Sie dynamische Verzweigung also übermäßig verwenden, wenn Sie diese Profile als Ziel verwenden, können Kompilierungsfehler auftreten.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>forcecase</td>
<td>Erzwingen Sie eine Switch-Anweisung in der Hardware.
<blockquote>
[!Note]<br />
Erfordert <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">Hardware auf Featureebene</a> 10_0 oder höher.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Aufruf</td>
<td>Die Körper der einzelnen Fälle im Switch werden in Hardwareunterroutinen verschoben, und der Switch ist eine Reihe von Unterroutinenaufrufen.
<blockquote>
[!Note]<br />
Erfordert <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">Hardware auf Featureebene</a> 10_0 oder höher.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Selector*
</dt> <dd>

Eine Variable. Die case-Anweisungen in den eckigen Klammern überprüfen jeweils diese Variable, um zu überprüfen, ob switchValue mit ihrem jeweiligen CaseValue-Wert entspricht.

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*
</dt> <dd>

Mindestens eine [-Anweisung.](dx-graphics-hlsl-statement-blocks.md)

</dd> </dl>

## <a name="remarks"></a>Bemerkungen


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



Entspricht:


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



Im Folgenden finden Sie Beispielverwendungen von ForceCase- und Aufrufflusssteuerungsattributen:


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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Urlmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Flusssteuerung](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

