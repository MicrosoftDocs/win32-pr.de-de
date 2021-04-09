---
title: switch_type-Attribut
description: Das Attribut \ Switch \_ Type \ gibt den Typ der Variablen an, die als Union-diskriminant verwendet wird. Der Switchtyp kann ein Integer-, Zeichen-, boolescher oder Enumerationstyp sein.
ms.assetid: e4c6d33b-d4db-42b7-9d18-fd14bf1fb530
keywords:
- Switch_type Attribut-Mittel l
topic_type:
- apiref
api_name:
- switch_type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14184c5838d9f671f75536714d73c3f6ebf00a0a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857455"
---
# <a name="switch_type-attribute"></a>Switch \_ Type-Attribut

Das **\[ \_ SwitchType \]** -Attribut identifiziert den Typ der Variablen, die als uniondiskriminant verwendet wird. Der Switchtyp kann ein Integer-, Zeichen-, boolescher oder Enumerationstyp sein.

``` syntax
switch_type(switch-type-specifier)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Switch-Type-Spezifizierer* 
</dt> <dd>

Gibt einen [**int**](int.md)-, [**char**](char-idl.md)-, [**Boolean**](boolean.md)-oder [**Enumeration**](enum.md) -Typ oder einen Bezeichner eines solchen Typs an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Während das **\[ \_ SwitchType \]** -Attribut den Variablentyp identifiziert, gibt der **\[** [**Switch \_ is**](switch-is.md) - **\]** Attribut den Namen des Parameters an, der die Union-Diskriminante ist. Das **\[ Switch \_ Type \]** -Attribut gilt für Parameter oder Member von Strukturen oder Unions.

Die Union und ihre Diskriminante müssen auf derselben logischen Ebene angegeben werden. Wenn die Union ein Parameter ist, muss der Union-diskriminant ein anderer Parameter sein. Wenn die Union ein Feld einer Struktur ist, muss die Diskriminante ein weiteres Feld der Struktur auf derselben Ebene wie das Union-Feld sein.

## <a name="examples"></a>Beispiele

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Booleschen**](boolean.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[Gekapselt Unions](encapsulated-unions.md)
</dt> <dt>

[**Enumeration**](enum.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[Nicht gekapselt Unions](nonencapsulated-unions.md)
</dt> <dt>

[**Switch \_ ist**](switch-is.md)
</dt> <dt>

[**Union**](union.md)
</dt> </dl>

 

 




