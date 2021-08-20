---
title: komplexer headerFieldType-Typ
description: Definiert die Elemente, die zum Erstellen eines Headerfelds in einer E-Mail verwendet werden.
ms.assetid: 66036875-1116-46eb-b2f5-8c8ad8373ab1
keywords:
- komplexer headerFieldType-Typ Taskplaner
topic_type:
- apiref
api_name:
- headerFieldType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78c4fb3a8ca85cea5b765fc1fc4521f968efd76e9169613dc4a1565a43ee1b36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131829"
---
# <a name="headerfieldtype-complex-type"></a>komplexer headerFieldType-Typ

Definiert die Elemente, die zum Erstellen eines Headerfelds in einer E-Mail verwendet werden.

``` syntax
<xs:complexType name="headerFieldType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
         />
        <xs:element name="Value"
            type="string"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                            | Typ                                                                    | Beschreibung                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Name**](taskschedulerschema-name-headerfieldtype-element.md)   | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Gibt den Namen des Headerfelds in einer E-Mail an.<br/> |
| [**Wert**](taskschedulerschema-value-headerfieldtype-element.md) | **string**                                                              | Gibt den Wert eines Headerfelds in einer E-Mail an.<br/>  |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





