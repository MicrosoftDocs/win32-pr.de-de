---
description: Definiert eine Liste von-Strukturen, die Gegenwerte enthalten.
ms.assetid: 6f6b33ed-6440-456c-8379-61a37798c95f
title: komplexer Strukturen-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c36de698d1e0eb136f17034e0740851fc751d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362226"
---
# <a name="structs-complex-type"></a>komplexer Strukturen-Typ

Definiert eine Liste von-Strukturen, die Gegenwerte enthalten.

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
| **struct** | [**man: struct**](performance-counters-struct-complex-type.md) | Der Name einer-Struktur, die die Werte für den Zählers enthält.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




