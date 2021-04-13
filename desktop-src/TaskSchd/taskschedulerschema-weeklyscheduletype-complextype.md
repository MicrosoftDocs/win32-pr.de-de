---
title: komplexer weeklyscheduletype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das schedulebyweek-Element.
ms.assetid: 048832fa-2262-4461-9cfc-823a4eb7a1df
keywords:
- der komplexe Typ "weeklyscheduletype" Taskplaner
topic_type:
- apiref
api_name:
- weeklyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 797e01c20e749593d64bad12f017af8be613992e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391757"
---
# <a name="weeklyscheduletype-complex-type"></a>komplexer weeklyscheduletype-Typ

Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**schedulebyweek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) -Element.

``` syntax
<xs:complexType name="weeklyScheduleType">
    <xs:all>
        <xs:element name="WeeksInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="52"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                               | type                                                                     | BESCHREIBUNG                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [**daysofweektype**](taskschedulerschema-daysofweektype-complextype.md) | Gibt die Wochentage an, an denen der Task ausgeführt wird.<br/>    |
| [**Weeksinterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) |                                                                          | Gibt das Intervall zwischen den Wochen im Zeitplan an.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





