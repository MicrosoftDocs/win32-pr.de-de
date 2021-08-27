---
title: StopAtDurationEnd -Element (wiederholungstyp)
description: Gibt an, dass eine ausgeführte Instanz der Aufgabe am Ende der Wiederholungsmusterdauer beendet wird.
ms.assetid: 4e34b5b2-ac93-4951-9de4-3e89614517d1
keywords:
- StopAtDurationEnd-Taskplaner
topic_type:
- apiref
api_name:
- StopAtDurationEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 896aa6db4ce5bf2c0dddf666024c143754afc97ec76bfb557e6431f593689857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010540"
---
# <a name="stopatdurationend-repetitiontype-element"></a>StopAtDurationEnd -Element (wiederholungstyp)

Gibt an, dass eine ausgeführte Instanz der Aufgabe am Ende der Wiederholungsmusterdauer beendet wird. Dies gilt nur, wenn Wiederholungen festgelegt sind.

``` syntax
<xs:element name="StopAtDurationEnd"
 type="boolean"
 />
```

Das **StopAtDurationEnd-Element** wird durch den komplexen [**Typ "repetitionType"**](taskschedulerschema-repetitiontype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element

| Element | Abgeleitet von | BESCHREIBUNG |
|-|-|-|
| [**Wiederholen**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**wiederholungstyp**](taskschedulerschema-repetitiontype-complextype.md) | Gibt an, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde.<br/> |

## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird diese Einstellung mithilfe der [**Eigenschaft "RepetitionPattern.StopAtDurationEnd"**](repetitionpattern-stopatdurationend.md) angegeben.

Für die C++-Entwicklung wird diese Einstellung mithilfe der [**IRepetitionPattern::StopAtDurationEnd-Eigenschaft**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) angegeben.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |

## <a name="see-also"></a>Siehe auch

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)

[Aufgabenplanung](task-scheduler-start-page.md)
