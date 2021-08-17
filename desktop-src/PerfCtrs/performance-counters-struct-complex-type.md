---
description: Definiert eine -Struktur, die einen oder mehrere Zählerwerte enthält.
ms.assetid: 3085d490-4ac1-491c-bce0-8af46b16fab9
title: Komplexer struct-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29796a259810cd03739c45338709966bd765f0c1fd9026777f435acb2c5de253
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978850"
---
# <a name="struct-complex-type"></a>Komplexer struct-Typ

Definiert eine -Struktur, die einen oder mehrere Zählerwerte enthält.

``` syntax
<xs:complexType name="struct">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="man:CSymbolType"
                use="required"
             />
            <xs:attribute name="type"
                type="man:CSymbolType"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributes



| Name | type                                                                    | Beschreibung                                                                                                                                      |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| name | [**man:CSymbolType**](performance-counters-csymboltype-simple-type.md) | Der Name der Struktur.<br/>                                                                                                            |
| Type | [**man:CSymbolType**](performance-counters-csymboltype-simple-type.md) | Ein symbolischer Name, der die Struktur identifiziert. Das [CTRPP-Tool](ctrpp.md) erstellt eine Strukturvariable mit diesem Namen, die Sie verwenden können.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




