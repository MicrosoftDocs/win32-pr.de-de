---
title: komplexer NamedValue-Typ
description: Definiert einen Namen, der mit einem Wert in einem Name-Wert-Paar verknüpft ist.
ms.assetid: 5e3ce01a-9be6-4f12-be02-42065aba46cd
keywords:
- komplexer NamedValue-Typ Taskplaner
topic_type:
- apiref
api_name:
- namedValue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39d6990194350dcc032d42838f30bdd7339b0d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956764"
---
# <a name="namedvalue-complex-type"></a>komplexer NamedValue-Typ

Definiert einen Namen, der mit einem Wert in einem Name-Wert-Paar verknüpft ist.

``` syntax
<xs:complexType name="namedValue">
    <xs:simpleContent>
        <xs:extension
            base="nonEmptyString"
        >
            <xs:attribute name="name"
                type="nonEmptyString"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributes



| Name | type                                                                    | BESCHREIBUNG                                                                          |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| name | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Gibt den Namen an, der mit einem Wert in einem Name-Wert-Paar verknüpft ist. <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





