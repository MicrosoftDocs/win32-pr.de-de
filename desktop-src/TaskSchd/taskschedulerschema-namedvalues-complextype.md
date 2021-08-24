---
title: NamedValues Complex Type
description: Definiert ein Name-Wert-Paar, in dem der Name dem Wert zugeordnet ist.
ms.assetid: 07c512fd-3eab-4238-8d75-83827a958a1e
keywords:
- 'NamedValues: komplexer Taskplaner'
topic_type:
- apiref
api_name:
- namedValues
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d54e7c33d0b7ab2e5be3c4de6f3f648398a7e65670c0379f5621ae9e8a8bd46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513936"
---
# <a name="namedvalues-complex-type"></a>NamedValues Complex Type

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



| Element                                                        | Typ                                                | Beschreibung                                                                         |
|----------------------------------------------------------------|-----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Wert**](taskschedulerschema-value-namedvalues-element.md) | [**namedValue**](schema-namedvalue-complextype.md) | Gibt den Wert an, der einem Namen in einem Name-Wert-Paar zugeordnet ist.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





