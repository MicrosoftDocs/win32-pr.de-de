---
title: switch_type-Attribut
description: Das Attribut \switch type\ gibt den Typ der Variablen an, die als union \_ discriminant verwendet wird. Der Switchtyp kann eine ganze Zahl, ein Zeichen, ein boolescher Wert oder ein Enumerationstyp sein.
ms.assetid: e4c6d33b-d4db-42b7-9d18-fd14bf1fb530
keywords:
- switch_type MIDL-Attribut
topic_type:
- apiref
api_name:
- switch_type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8695a17c60f9785d7782d77db839499306a9577755e8a6838540f5a0fc2cea48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146233"
---
# <a name="switch_type-attribute"></a>switch \_ type-Attribut

Das **\[ \_ \] Switchtypattribut** identifiziert den Typ der Variablen, die als Union diskriminant verwendet wird. Der Switchtyp kann eine ganze Zahl, ein Zeichen, ein boolescher Wert oder ein Enumerationstyp sein.

``` syntax
switch_type(switch-type-specifier)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*switch-type-specifier* 
</dt> <dd>

Gibt einen [**int-,**](int.md) [**char-,**](char-idl.md) [**boolean-**](boolean.md)oder [**enum-Typ**](enum.md) oder einen Bezeichner eines solchen Typs an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Während das **\[ \_ \] Switchtypattribut** den Variablentyp identifiziert, gibt der Switch is-Attribut den Namen des Parameters an, der die **\[** [**\_**](switch-is.md) **\]** Union diskriminant ist. Das **\[ \_ \] Switchtypattribut** gilt für Parameter oder Member von Strukturen oder Unions.

Die Union und ihre Diskriminanz müssen auf der gleichen logischen Ebene angegeben werden. Wenn die Union ein Parameter ist, muss die Union diskriminant ein anderer Parameter sein. Wenn die Union ein Feld einer -Struktur ist, muss der Diskriminant ein anderes Feld der -Struktur auf der gleichen Ebene wie das Union-Feld sein.

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

[**Boolean**](boolean.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[Gekapselte Unions](encapsulated-unions.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[Nicht kapselte Unions](nonencapsulated-unions.md)
</dt> <dt>

[**switch \_ ist**](switch-is.md)
</dt> <dt>

[**Union**](union.md)
</dt> </dl>

 

 




