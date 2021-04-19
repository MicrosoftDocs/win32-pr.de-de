---
description: Definiert eine-Struktur, die einen oder mehrere-Werte enthält.
ms.assetid: 3085d490-4ac1-491c-bce0-8af46b16fab9
title: komplexer Strukturtyp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc59103a1a98b0baf1559ead159221ea42288936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348013"
---
# <a name="struct-complex-type"></a>komplexer Strukturtyp

Definiert eine-Struktur, die einen oder mehrere-Werte enthält.

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



| Name | type                                                                    | BESCHREIBUNG                                                                                                                                      |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| name | [**man: csymboltype**](performance-counters-csymboltype-simple-type.md) | Der Name der Struktur.<br/>                                                                                                            |
| type | [**man: csymboltype**](performance-counters-csymboltype-simple-type.md) | Ein symbolischer Name, der die-Struktur bezeichnet. Das [ctrpp](ctrpp.md) -Tool erstellt eine Struktur Variable mit diesem Namen, die Sie verwenden können.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




