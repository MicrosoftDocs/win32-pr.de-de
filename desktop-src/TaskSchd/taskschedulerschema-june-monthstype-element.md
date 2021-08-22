---
title: June (monthsType)-Element
description: Gibt an, dass die Aufgabe im Juni ausgeführt wird.
ms.assetid: 15b0e8c2-4dc1-4ca3-99c5-bd9a36718904
keywords:
- Juni-element Taskplaner
topic_type:
- apiref
api_name:
- June
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0675c0fb7c399b5d3decadf651a10793c163aeb75cad752e9e2fc0fdc251ba9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072470"
---
# <a name="june-monthstype-element"></a>June (monthsType)-Element

Gibt an, dass die Aufgabe im Juni ausgeführt wird.

``` syntax
<xs:element name="June">
    <xs:complexType />
</xs:element>
```

Das **June-Element** wird durch den komplexen [**monthsType-Typ**](taskschedulerschema-monthstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                          | Abgeleitet von                                                     | BESCHREIBUNG                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Monate (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.<br/> |
| [**Monate (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Gibt die Monate des Jahres an, in denen die Aufgabe für einen monatlichen Zeitplan ausgeführt wird.<br/>             |



## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen Kalender für Monate, in dem die Aufgabe im Juni ausgeführt wird.


```XML
<Months>
    <June/>
</Months>
```



## <a name="requirements"></a>Requirements (Anforderungen)



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

 

 





