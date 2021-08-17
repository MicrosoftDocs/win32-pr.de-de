---
title: Day (daysOfMonthType) -Element
description: Gibt einen Tag des Monats an, an dem der Task ausgeführt wird.
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
ms.openlocfilehash: 3c238ee5bd873c33f3acd2207ba9ad31869b151924dd20f082669b782d207c59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857953"
---
# <a name="day-daysofmonthtype-element"></a>Day (daysOfMonthType) -Element

Gibt einen Tag des Monats an, an dem der Task ausgeführt wird.

``` syntax
<xs:element name="Day"
    type="dayOfMonthType"
 />
```

Das **Day-Element** wird durch den komplexen [**DaysOfMonthType-Typ**](taskschedulerschema-daysofmonthtype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                            | Abgeleitet von                                                               | Beschreibung                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) | Gibt die Tage des Monats an, an denen der Task ausgeführt wird.<br/> |



## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert den Tageteil eines monatlichen Kalenders, in dem die Aufgabe am 1. und 15. Tag des Monats ausgeführt wird.


```XML
<DaysOfMonth>
    <Day>1</Day>
    <Day>15</Day>
</DaysOfMonth>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





