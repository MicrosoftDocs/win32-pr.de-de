---
title: Week (weeksType)-Element
description: Gibt eine bestimmte Woche des Monats an.
ms.assetid: 0cec07da-e9e7-43ef-9f54-48d00114ba1f
keywords:
- Week-Taskplaner
topic_type:
- apiref
api_name:
- Week
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a999eaa5ec7d4ed36b86fc292f4c0d5e8c474fd1df8f5f4b9da5b90f2dcca641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758206"
---
# <a name="week-weekstype-element"></a>Week (weeksType)-Element

Gibt eine bestimmte Woche des Monats an.

``` syntax
<xs:element name="Week"
    type="weekType"
 />
```

Das **Week-Element** wird durch den komplexen [**WeeksType-Typ**](taskschedulerschema-weekstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                        | Abgeleitet von                                                   | Beschreibung                                                           |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------------------|
| [**Weeks (monthlyDayOfWeekScheduleType)**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) | [**weeksType**](taskschedulerschema-weekstype-complextype.md) | Gibt die Wochen des Monats an, in denen die Aufgabe ausgeführt wird.<br/> |



## <a name="remarks"></a>Hinweise

Wenn Sie die Wochen des Monats angeben, verwenden Sie die Zahlen 1-4 für die ersten vier Wochen des Monats, oder verwenden Sie die Zeichenfolge "Last", um die letzte Woche des Monats anzugeben.

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

 

 





