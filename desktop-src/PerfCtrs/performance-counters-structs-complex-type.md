---
description: Definiert eine Liste von Strukturen, die Indikatorwerte enthalten.
ms.assetid: 6f6b33ed-6440-456c-8379-61a37798c95f
title: Komplexe Typen von Strukturen
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0dfa7f72ee537d857f19301aa4df906d94b0bf7ba9e3f7a76bdb6ab82c84dfd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314420"
---
# <a name="structs-complex-type"></a>Komplexe Typen von Strukturen

Definiert eine Liste von Strukturen, die Indikatorwerte enthalten.

``` syntax
<xs:complexType name="structs">
    <xs:choice
        minOccurs="1"
        maxOccurs="unbounded"
    >
        <xs:element name="struct"
            type="man:struct"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element    | type                                                           | BESCHREIBUNG                                                      |
|------------|----------------------------------------------------------------|------------------------------------------------------------------|
| **struct** | [**man:struct**](performance-counters-struct-complex-type.md) | Der Name einer Struktur, die Indikatorwerte enthält.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




