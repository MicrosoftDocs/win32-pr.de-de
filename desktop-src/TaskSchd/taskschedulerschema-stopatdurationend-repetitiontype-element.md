---
title: Stopatdurationend (repetitiontype)-Element
description: Gibt an, dass eine laufende Instanz der Aufgabe am Ende der Wiederholungsmuster Dauer beendet wird.
ms.assetid: 4e34b5b2-ac93-4951-9de4-3e89614517d1
keywords:
- Stopatdurationend-Element Taskplaner
topic_type:
- apiref
api_name:
- StopAtDurationEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a95f15f3a62d05b9bc28dc9f50b924979e2b748c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343064"
---
# <a name="stopatdurationend-repetitiontype-element"></a>Stopatdurationend (repetitiontype)-Element

Gibt an, dass eine laufende Instanz der Aufgabe am Ende der Wiederholungsmuster Dauer beendet wird. Dies gilt nur, wenn Wiederholungen festgelegt sind.

``` syntax
<xs:element name="StopAtDurationEnd"
 type="boolean"
 />
```

Das **stopatdurationend** -Element wird durch den komplexen Typ " [**wiederholtiontype**](taskschedulerschema-repetitiontype-complextype.md) " definiert.

## <a name="parent-element"></a>Übergeordnetes Element

| Element | Abgeleitet von | BESCHREIBUNG |
|-|-|-|
| [**Wiederholen**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**Wiederholungstyp**](taskschedulerschema-repetitiontype-complextype.md) | Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.<br/> |

## <a name="remarks"></a>Bemerkungen

Bei der Skripterstellung wird diese Einstellung mithilfe der [**wiederholungspattern. stopatdurationend**](repetitionpattern-stopatdurationend.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird diese Einstellung mithilfe der [**irepetitionpattern:: stopatdurationend**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) -Eigenschaft angegeben.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |

## <a name="see-also"></a>Siehe auch

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)

[Aufgabenplanung](task-scheduler-start-page.md)
