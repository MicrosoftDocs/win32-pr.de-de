---
title: actionsType Complex Type
description: Definiert die untergeordneten Elemente und das Attribut für das Actions-Element.
ms.assetid: 01577b65-4bfa-4b9f-b9b9-6b2b0dbd582a
keywords:
- actionsType complex type Taskplaner
topic_type:
- apiref
api_name:
- actionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d84cab2f0977a3b5bf980f594f1b26b543d8e5e7de000959488e874e640dc9d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010930"
---
# <a name="actionstype-complex-type"></a>actionsType Complex Type

Definiert die untergeordneten Elemente und das Attribut für das [**Actions-Element.**](taskschedulerschema-actions-tasktype-element.md)

``` syntax
<xs:complexType name="actionsType">
    <xs:sequence>
        <xs:group
            maxOccurs="32"
            ref="actionGroup"
         />
    </xs:sequence>
    <xs:attribute name="Context"
        type="IDREF"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a>Attributes



| Name    | type  | BESCHREIBUNG                                                                                          |
|---------|-------|------------------------------------------------------------------------------------------------------|
| Kontext | IDREF | Prinzipalbezeichner des verwendeten , der der Sicherheitskontext für die Aktionen der Aufgabe ist.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Komplexe Schematypen](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





