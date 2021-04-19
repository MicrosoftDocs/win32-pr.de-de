---
title: Dienstag (daysofweektype)-Element
description: Gibt an, dass der Task am Dienstag ausgeführt wird.
ms.assetid: 588608e9-33f9-405d-8b4b-35f11ab403db
keywords:
- Dienstag-Element Taskplaner
topic_type:
- apiref
api_name:
- Tuesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ed48803d0cad5dae409202869c600e7e7a60643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345936"
---
# <a name="tuesday-daysofweektype-element"></a>Dienstag (daysofweektype)-Element

Gibt an, dass der Task am Dienstag ausgeführt wird.

``` syntax
<xs:element name="Tuesday">
    <xs:complexType />
</xs:element>
```

Das **Dienstag** -Element wird durch den komplexen Typ [**daysofweektype**](taskschedulerschema-daysofweektype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                                  | Abgeleitet von                                                             | BESCHREIBUNG                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlydayosweekscheduletype)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysofweektype**](taskschedulerschema-daysofweektype-complextype.md) | Gibt die Wochentage an, an denen der Task für einen monatlichen Wochentag ausgeführt wird.<br/> |
| [**DaysOfWeek (weeklyscheduletype)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysofweektype**](taskschedulerschema-daysofweektype-complextype.md) | Gibt die Wochentage an, an denen der Task für einen wöchentlichen Zeitplan ausgeführt wird.<br/>              |



## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen Wochentag-Kalender, der eine Aufgabe am Dienstag startet.


```XML
<DaysOfWeek>
    <Tuesday/>
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

 

 





