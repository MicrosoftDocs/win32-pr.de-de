---
title: Day (daysofmonthtype)-Element
description: Gibt den Tag des Monats an, in dem die Aufgabe ausgeführt wird.
ms.assetid: b213df09-9301-4a51-b000-edfdafbe861e
keywords:
- Day-Element Taskplaner
topic_type:
- apiref
api_name:
- Day
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e8e06169d2b758264f181263a5cb717977a1602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040336"
---
# <a name="day-daysofmonthtype-element"></a>Day (daysofmonthtype)-Element

Gibt den Tag des Monats an, in dem die Aufgabe ausgeführt wird.

``` syntax
<xs:element name="Day"
    type="dayOfMonthType"
 />
```

Das **Day** -Element wird durch den komplexen [**tagsofmonthtype**](taskschedulerschema-daysofmonthtype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                            | Abgeleitet von                                                               | BESCHREIBUNG                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**daysofmonthtype**](taskschedulerschema-daysofmonthtype-complextype.md) | Gibt die Tage des Monats an, in denen der Task ausgeführt wird.<br/> |



## <a name="examples"></a>Beispiele

Im folgenden XML-Code wird der Tage Teil eines monatlichen Kalenders definiert, der die Aufgabe am 1. und 15. Tag des Monats ausführt.


```XML
<DaysOfMonth>
    <Day>1</Day>
    <Day>15</Day>
</DaysOfMonth>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





