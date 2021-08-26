---
title: ExecutionTimeLimit (triggerBaseType)-Element
description: Gibt die maximale Zeitspanne an, in der der Task vom Trigger gestartet werden kann.
ms.assetid: f78e7c7b-d069-4920-9435-020f6e081eff
keywords:
- ExecutionTimeLimit-Element Taskplaner
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e958c6a2b873bb78e66645ce2a2ae8100e2acbc
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812519"
---
# <a name="executiontimelimit-triggerbasetype-element"></a>ExecutionTimeLimit (triggerBaseType)-Element

Die maximale Zeit, die der vom Trigger gestartete Task ausführen darf. Das Format für diese Zeichenfolge lautet PnYnMnDTnHnMnS, wobei nY die Anzahl der Jahre, nM die Anzahl der Monate, nD die Anzahl der Tage, "T" das Datums-/Uhrzeittrennzeichen, nH die Anzahl der Stunden, nM die Anzahl der Minuten und nS die Anzahl von Sekunden ist (z. B. PT5M gibt 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an). Weitere Informationen zum Dauertyp finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
 />
```

Das **ExecutionTimeLimit-Element** wird durch den komplexen [**TriggerBaseType-Typ**](taskschedulerschema-boottriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                     | Abgeleitet von                                                                               | Beschreibung                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | Gibt einen Trigger an, der eine Aufgabe startet, wenn das System gestartet wird.<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen DOW-Trigger (Day-of-the-Week) an.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)               | Gibt einen Trigger an, der eine Aufgabe startet, wenn ein Systemereignis auftritt.<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | Gibt einen Trigger an, der eine Aufgabe startet, wenn der Computer in den Leerlauf wechselt.<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | Gibt einen Trigger an, der eine Aufgabe startet, wenn sich ein Benutzer anmeldet.<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Gibt einen Trigger an, der eine Aufgabe startet, wenn der Task registriert wird.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                 | Gibt einen Trigger an, der eine Aufgabe startet, wenn der Trigger aktiviert wird.<br/>             |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird das Ausführungszeitlimit mithilfe der [**Trigger.ExecutionTimeLimit-Eigenschaft**](trigger-executiontimelimit.md) angegeben, die von allen Triggerobjekten geerbt wird.

Für die C++-Entwicklung wird das Ausführungszeitlimit mithilfe der [**ITrigger::ExecutionTimeLimit-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) angegeben, die von allen Triggerschnittstellen geerbt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





