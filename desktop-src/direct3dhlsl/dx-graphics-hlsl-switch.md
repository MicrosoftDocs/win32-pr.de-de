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
ms.openlocfilehash: 8527853bf88b073f3505f4b4170ff6165f7f9aa7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477486"
---
# <a name="switch-statement"></a>switch-Anweisung

Übertragen Sie die Steuerung abhängig vom Wert eines Selektors in einen anderen Anweisungsblock innerhalb des Switch-Textkörpers.


\[*Attribut* \] switch( *Selector* ) { case 0 : { *StatementBlock*; }   break;   Fall 1: { *StatementBlock*; }   break;   case n : { *StatementBlock*; }   break;   default: { *StatementBlock;*}   break;



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*
</dt> <dd>

Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird. Wenn kein Attribut angegeben ist, kann der Compiler einen Hardwareschalter verwenden oder eine Reihe von **if-Anweisungen** aus geben.




| Attribut | BESCHREIBUNG | 
|-----------|-------------|
| Vereinfachen | Kompilieren Sie die -Anweisung als eine Reihe von if-Anweisungen, jeweils mit <strong>dem flatten-Attribut.</strong> <strong></strong> | 
| Verzweigung | Kompilieren Sie die <strong></strong> -Anweisung als eine Reihe von if-Anweisungen, die jeweils das <strong>Branchattribut</strong> enthalten.<blockquote>[!Note]<br />Wenn Sie <a href="dx-graphics-hlsl-sm2.md">shader Model 2.x</a> oder <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>verwenden, nutzen Sie bei jeder Verwendung dynamischer Verzweigung Ressourcen. Wenn Sie dynamische Verzweigung also übermäßig verwenden, wenn Sie diese Profile als Ziel verwenden, können Kompilierungsfehler auftreten.</blockquote><br /> | 
| forcecase | Erzwingen Sie eine Switch-Anweisung in der Hardware.<blockquote>[!Note]<br />Erfordert <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">Hardware auf Featureebene</a> 10_0 oder höher.</blockquote><br /> | 
| Aufruf | Die Körper der einzelnen Fälle im Switch werden in Hardwareunterroutinen verschoben, und der Switch ist eine Reihe von Unterroutinenaufrufen.<blockquote>[!Note]<br />Erfordert <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">Hardware auf Featureebene</a> 10_0 oder höher.</blockquote><br /> | 




 

</dd> <dt>

<span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Selector*
</dt> <dd>

Eine Variable. Die case-Anweisungen in den eckigen Klammern überprüfen jeweils diese Variable, um zu überprüfen, ob switchValue mit ihrem jeweiligen CaseValue-Wert entspricht.

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*
</dt> <dd>

Mindestens eine [-Anweisung.](dx-graphics-hlsl-statement-blocks.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Urlmon.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Flow Steuerung](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

