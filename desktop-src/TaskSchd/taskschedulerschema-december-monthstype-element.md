---
title: December (monthsType)-Element
description: Gibt an, dass die Aufgabe im Dezember ausgeführt wird.
ms.assetid: 42f3cfb2-8e82-46a0-b3ef-42e83d329124
keywords:
- December-Element Taskplaner
topic_type:
- apiref
api_name:
- December
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9212641956abc4e52f455a83ac6d5e58a8560fa44cd68068dc809280b30e5faf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516920"
---
# <a name="december-monthstype-element"></a>December (monthsType)-Element

Gibt an, dass die Aufgabe im Dezember ausgeführt wird.

``` syntax
<xs:element name="December">
    <xs:complexType />
</xs:element>
```

Das **December-Element** wird durch den komplexen [**monthsType-Typ**](taskschedulerschema-monthstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                          | Abgeleitet von                                                     | Beschreibung                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Monate (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.<br/> |
| [**Monate (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Gibt die Monate des Jahres an, in denen die Aufgabe für einen monatlichen Zeitplan ausgeführt wird.<br/>             |



## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen Kalender für Monate, in dem die Aufgabe im Dezember ausgeführt wird.


```XML
<Months>
    <December/>
</Months>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





