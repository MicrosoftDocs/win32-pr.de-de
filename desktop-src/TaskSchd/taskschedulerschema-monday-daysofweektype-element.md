---
title: Montag (daysofweektype)-Element
description: Gibt an, dass der Task am Montag ausgeführt wird.
ms.assetid: 2b7ce0c1-c635-47d0-b482-5c93c0028c92
keywords:
- Montag-Element Taskplaner
topic_type:
- apiref
api_name:
- Monday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3967db32a6ccd536e2e389e84de4eec05b333634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478165"
---
# <a name="monday-daysofweektype-element"></a>Montag (daysofweektype)-Element

Gibt an, dass der Task am Montag ausgeführt wird.

``` syntax
<xs:element name="Monday">
    <xs:complexType />
</xs:element>
```

Das **Montag** -Element wird durch den komplexen Typ " [**weeklyscheduletype**](taskschedulerschema-weeklyscheduletype-complextype.md) " definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                                  | Abgeleitet von                                                             | BESCHREIBUNG                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlydayosweekscheduletype)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysofweektype**](taskschedulerschema-daysofweektype-complextype.md) | Gibt die Wochentage an, an denen der Task für einen monatlichen Wochentag ausgeführt wird.<br/> |
| [**DaysOfWeek (weeklyscheduletype)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysofweektype**](taskschedulerschema-daysofweektype-complextype.md) | Gibt die Wochentage an, an denen der Task für einen wöchentlichen Zeitplan ausgeführt wird.<br/>              |



## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen Wochentag-Kalender, der eine Aufgabe am Montag startet.


```XML
<DaysOfWeek>
    <Monday/>
</DaysOfWeek>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





