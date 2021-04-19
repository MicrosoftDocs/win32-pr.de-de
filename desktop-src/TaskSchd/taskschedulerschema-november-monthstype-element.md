---
title: November-Element (monthstype)
description: Gibt an, dass der Task im November ausgeführt wird.
ms.assetid: 45f8c47b-3884-4f18-8275-f29f82ee32e2
keywords:
- November-Element Taskplaner
topic_type:
- apiref
api_name:
- November
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 295b63a4ff4dad1ec07504bb43c4a471d4389159
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342454"
---
# <a name="november-monthstype-element"></a>November-Element (monthstype)

Gibt an, dass der Task im November ausgeführt wird.

``` syntax
<xs:element name="November">
    <xs:complexType />
</xs:element>
```

Das **November** -Element wird durch den komplexen [**monthstype**](taskschedulerschema-monthstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                          | Abgeleitet von                                                     | BESCHREIBUNG                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Monate (monthlydayosweekscheduletype)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthstype**](taskschedulerschema-monthstype-complextype.md) | Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.<br/> |
| [**Monate (monthlyscheduletype)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthstype**](taskschedulerschema-monthstype-complextype.md) | Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.<br/>             |



## <a name="examples"></a>Beispiele

Im folgenden XML-Code wird ein Monatskalender definiert, in dem die Aufgabe im November ausgeführt wird.


```XML
<Months>
    <November/>
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

 

 





