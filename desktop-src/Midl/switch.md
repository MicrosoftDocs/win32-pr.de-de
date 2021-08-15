---
title: switch-Attribut
description: Das switch-Schlüsselwort wählt die Diskriminanz für eine gekapselte \_ Union aus.
ms.assetid: 66179b68-852f-4943-9105-e9fb310f3c2e
keywords:
- switch-Attribut MIDL
topic_type:
- apiref
api_name:
- switch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422b52a339a83cbaf59a9d65c0ed0e4e7e41533dcbf0be962147327145588a7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013548"
---
# <a name="switch-attribute"></a>switch-Attribut

Das **switch-Schlüsselwort** wählt die Diskriminanz für eine [**gekapselte \_ Union**](encapsulated-unions.md)aus.

``` syntax
switch (switch-type switch-name)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*switch-type* 
</dt> <dd>

Gibt einen [**int-,**](int.md) [**char-,**](-char.md) [**enum-Typ**](enum.md) oder einen Bezeichner an, der in einen dieser Typen aufgelöst wird.

</dd> <dt>

*switch-name* 
</dt> <dd>

Gibt den Namen der Variablen vom Typ *switch-type* an, die als union-diskriminant fungiert.

</dd> </dl>

## <a name="examples"></a>Beispiele

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[Nicht gekapselte Unions](nonencapsulated-unions.md)
</dt> <dt>

[**switch \_ ist**](switch-is.md)
</dt> <dt>

[**\_switch-Typ**](switch-type.md)
</dt> <dt>

[**Union**](union.md)
</dt> </dl>

 

 




