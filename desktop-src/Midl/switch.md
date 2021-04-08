---
title: Switch-Attribut
description: Das Schlüsselwort Switch wählt die Diskriminante für eine gekapselte \_ Union aus.
ms.assetid: 66179b68-852f-4943-9105-e9fb310f3c2e
keywords:
- Attribut-Mittel l wechseln
topic_type:
- apiref
api_name:
- switch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdf9342789d5603a3b64d778bd60364eebde50e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948221"
---
# <a name="switch-attribute"></a>Switch-Attribut

Das Schlüsselwort **Switch** wählt die Diskriminante für eine [**gekapselte \_ Union**](encapsulated-unions.md)aus.

``` syntax
switch (switch-type switch-name)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Switch-Type* 
</dt> <dd>

Gibt einen [**int**](int.md)-, [**char**](-char.md)-, [**Enumeration**](enum.md) -Typ oder einen Bezeichner an, der zu einem dieser Typen aufgelöst wird.

</dd> <dt>

*SwitchName* 
</dt> <dd>

Gibt den Namen der Variablen vom Typ *Switch-Type* an, der als Union-diskriminant fungiert.

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

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[Nicht gekapselt Unions](nonencapsulated-unions.md)
</dt> <dt>

[**Switch \_ ist**](switch-is.md)
</dt> <dt>

[**\_Switchtyp**](switch-type.md)
</dt> <dt>

[**Union**](union.md)
</dt> </dl>

 

 




