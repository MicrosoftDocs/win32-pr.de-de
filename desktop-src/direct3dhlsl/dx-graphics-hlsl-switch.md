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
# <a name="switch-statement"></a>switch-Anweisung

Überträgt die Steuerung abhängig vom Wert eines Selektor an einen anderen Anweisungsblock innerhalb des Switch-Texts.



|                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[*Attribut* \] Switch ( *Selektor* ) {Case 0: { *Status Block*;}   Umbruch   Fall 1: { *Status Block*;}   Umbruch   Fall n: { *Status Block*;}   Umbruch   Standard: { *Status Block*;}   Umbruch |



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Versehen*
</dt> <dd>

Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird. Wenn kein Attribut angegeben ist, verwendet der Compiler möglicherweise einen Hardware Switch oder gibt eine Reihe von **if** -Anweisungen aus.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vereinfachen</td>
<td>Kompilieren Sie die Anweisung als eine Reihe von <strong>if</strong> -Anweisungen, die jeweils das <strong>vereinfachen</strong> -Attribut haben.</td>
</tr>
<tr class="even">
<td>Verzweigung</td>
<td>Kompilieren Sie die-Anweisung als eine Reihe von <strong>if</strong> -Anweisungen, die jeweils das <strong>Branch</strong> -Attribut haben.
<blockquote>
[!Note]<br />
Wenn Sie das <a href="dx-graphics-hlsl-sm2.md">Shadermodell 2. x</a> oder das <a href="dx-graphics-hlsl-sm3.md">Shader-Modell 3,0</a>verwenden, verwenden Sie jedes Mal, wenn Sie dynamische Verzweigungen verwenden, Ressourcen. Wenn Sie also die dynamische Verzweigung übermäßig verwenden, wenn Sie diese Profile als Ziel verwenden, können Sie Kompilierungsfehler erhalten.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>forcecase</td>
<td>Erzwingen Sie eine Switch-Anweisung in der Hardware.
<blockquote>
[!Note]<br />
Erfordert 10_0 oder <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">höhere</a> Hardware.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Aufruf</td>
<td>Die Textteile der einzelnen Fälle im Switch werden in Hardware Unterroutinen verschoben, und der Switch ist eine Reihe von Unterroutine aufrufen.
<blockquote>
[!Note]<br />
Erfordert 10_0 oder <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">höhere</a> Hardware.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Ktor*
</dt> <dd>

Eine Variable. Die Case-Anweisungen innerhalb der geschweiften Klammern prüfen jeweils diese Variable, um festzustellen, ob der switchValue mit dem jeweiligen casevalue übereinstimmt.

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*Status Block*
</dt> <dd>

Eine oder mehrere- [Anweisungen](dx-graphics-hlsl-statement-blocks.md).

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



Im folgenden finden Sie Beispiel Verwendungen von forcecase-und callflowcontrol-Attributen:


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
| Header<br/> | <dl> <dt>Urlmon. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Fluss Steuerung](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

