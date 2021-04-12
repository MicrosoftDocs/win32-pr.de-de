---
title: komplexer weekstype-Typ
description: Definiert das untergeordnete Element und die Sequenzierungs Informationen für das Week-Element.
ms.assetid: c9e8814c-b8f9-426d-943d-ca3efa5d914b
keywords:
- komplexer weekstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- weeksType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 597cc72c043a478a414187f63a9aa89516dee658
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105350"
---
# <a name="weekstype-complex-type"></a>komplexer weekstype-Typ

Definiert das untergeordnete Element und die Sequenzierungs Informationen für das [**Week**](taskschedulerschema-week-weekstype-element.md) -Element.

``` syntax
<xs:complexType name="weeksType">
    <xs:sequence>
        <xs:element name="Week"
            type="weekType"
            minOccurs="0"
            maxOccurs="5"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                    | type                                                        | BESCHREIBUNG                                             |
|------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------|
| [**Mitte**](taskschedulerschema-week-weekstype-element.md) | [**weektype**](taskschedulerschema-weektype-simpletype.md) | Gibt die Woche an, in der die Aufgabe ausgeführt wird.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





