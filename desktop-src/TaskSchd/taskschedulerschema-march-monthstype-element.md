---
title: March (monthsType)-Element
description: Gibt an, dass die Aufgabe im März ausgeführt wird.
ms.assetid: 0cd82405-8e17-483d-88ba-32cae590f6b3
keywords:
- March-Element Taskplaner
topic_type:
- apiref
api_name:
- March
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d90d64e0fd275f57252cd435ae5dc42abfe8ba17613e1b20425fc27c515509e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139183"
---
# <a name="march-monthstype-element"></a>March (monthsType)-Element

Gibt an, dass die Aufgabe im März ausgeführt wird.

``` syntax
<xs:element name="March">
    <xs:complexType />
</xs:element>
```

Das **March-Element** wird durch den komplexen [**monthsType-Typ**](taskschedulerschema-monthstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                          | Abgeleitet von                                                     | Beschreibung                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Monate (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.<br/> |
| [**Monate (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Gibt die Monate des Jahres an, in denen die Aufgabe für einen monatlichen Zeitplan ausgeführt wird.<br/>             |



## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen Kalender für Monate, in dem die Aufgabe im März ausgeführt wird.


```XML
<Months>
    <March/>
</Months>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





