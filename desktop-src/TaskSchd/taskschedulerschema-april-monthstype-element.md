---
title: April (monthstype)-Element
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
ms.openlocfilehash: ecde82e5091adf51c2e42b682e36dba6d45e85c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105885"
---
# <a name="april-monthstype-element"></a>April (monthstype)-Element

Gibt an, dass der Task im April ausgeführt wird.

``` syntax
<xs:element name="April">
    <xs:complexType />
</xs:element>
```

Das **April** -Element wird durch den komplexen [**monthstype**](taskschedulerschema-monthstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                          | Abgeleitet von                                                     | BESCHREIBUNG                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Monate (monthlydayosweekscheduletype)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthstype**](taskschedulerschema-monthstype-complextype.md) | Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.<br/>             |
| [**Monate (monthlyscheduletype)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthstype**](taskschedulerschema-monthstype-complextype.md) | Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.<br/> |



## <a name="examples"></a>Beispiele

Im folgenden XML-Code wird ein Monatskalender definiert, in dem die Aufgabe im April ausgeführt wird.


```XML
<Months>
    <April/>
</Months>
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

 

 





