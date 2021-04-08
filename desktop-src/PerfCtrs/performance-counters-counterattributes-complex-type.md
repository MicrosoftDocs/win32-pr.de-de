---
description: Definiert eine Liste, die bis zu fünf Counter-Attribute enthält.
ms.assetid: d710c3d2-2886-4f1a-bd27-f11451d2f3c6
title: komplexer counterAttribute-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfcb94b131e1343565d5763ae2ea4d95e53f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959756"
---
# <a name="counterattributes-complex-type"></a>komplexer counterAttribute-Typ

Definiert eine Liste, die bis zu fünf Counter-Attribute enthält.

``` syntax
<xs:complexType name="counterAttributes">
    <xs:choice
        minOccurs="1"
        maxOccurs="5"
    >
        <xs:element name="counterAttribute"
            type="man:counterAttribute"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element              | type                                                                               | BESCHREIBUNG                                                                                                |
|----------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| **Counter Attribute** | [**man: counterAttribute**](performance-counters-counterattribute-complex-type.md) | Ein Counter-Attribut, das angibt, wie die gegen Daten in einer Consumeranwendung angezeigt werden.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




