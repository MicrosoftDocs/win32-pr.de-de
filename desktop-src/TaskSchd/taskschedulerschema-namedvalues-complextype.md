---
title: komplexer namedValues-Typ
description: Definiert ein Name-Wert-Paar, in dem der Name dem Wert zugeordnet ist.
ms.assetid: 07c512fd-3eab-4238-8d75-83827a958a1e
keywords:
- komplexer namedValues-Typ Taskplaner
topic_type:
- apiref
api_name:
- namedValues
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f18c9fddab58f33ffc724a3e8df7bd65583cb88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742161"
---
# <a name="namedvalues-complex-type"></a>komplexer namedValues-Typ

Definiert ein Name-Wert-Paar, in dem der Name dem Wert zugeordnet ist.

``` syntax
<xs:complexType name="namedValues">
    <xs:sequence>
        <xs:element name="Value"
            type="namedValue"
            minOccurs="1"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                        | type                                                | BESCHREIBUNG                                                                         |
|----------------------------------------------------------------|-----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Wert**](taskschedulerschema-value-namedvalues-element.md) | [**NamedValue**](schema-namedvalue-complextype.md) | Gibt den Wert an, der einem Namen in einem Name-Wert-Paar zugeordnet ist.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





