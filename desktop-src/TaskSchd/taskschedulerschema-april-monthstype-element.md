---
title: April -Element (monthsType)
description: Gibt an, dass der Task im April ausgeführt wird.
ms.assetid: b642e142-0acc-4b88-a86a-5d539613ead6
keywords:
- April-Element Taskplaner
topic_type:
- apiref
api_name:
- April
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f717e015c320c03b6d41e4c17d04cf3a255f85eb150a3f292933c370a516ae8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125880"
---
# <a name="april-monthstype-element"></a>April -Element (monthsType)

Gibt an, dass der Task im April ausgeführt wird.

``` syntax
<xs:element name="April">
    <xs:complexType />
</xs:element>
```

Das **April-Element** wird durch den komplexen [**Typ monthsType**](taskschedulerschema-monthstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                          | Abgeleitet von                                                     | Beschreibung                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.<br/>             |
| [**Months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.<br/> |



## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen Monatskalender, in dem die Aufgabe im April ausgeführt wird.


```XML
<Months>
    <April/>
</Months>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





