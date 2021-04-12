---
title: Executiontimelimit (triggerbasetype)-Element
description: Gibt die maximale Zeitspanne an, in der der Task vom-Vorgang gestartet werden kann.
ms.assetid: f78e7c7b-d069-4920-9435-020f6e081eff
keywords:
- Executiontimelimit-Element Taskplaner
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fbe56fb0431ab109b1a19030ae6ba20af55492ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478183"
---
# <a name="executiontimelimit-triggerbasetype-element"></a>Executiontimelimit (triggerbasetype)-Element

Gibt die maximale Zeitspanne an, in der der Task vom-Vorgang gestartet werden kann. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
 />
```

Das **executiontimelimit** -Element wird durch den komplexen [**triggerbasetype**](taskschedulerschema-boottriggertype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                     | Abgeleitet von                                                                               | BESCHREIBUNG                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**Boottrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**boottriggertype**](taskschedulerschema-boottriggertype-complextype.md)                 | Gibt einen-Fehler an, mit dem eine Aufgabe gestartet wird, wenn das System gestartet wird.<br/>                 |
| [**Calendarausgelöst**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md)         | Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventtriggertype**](taskschedulerschema-eventtriggertype-complextype.md)               | Gibt einen-Fehler an, der einen Task startet, wenn ein System Ereignis auftritt.<br/>                |
| [**Idle-Auslösung**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idletriggertype**](taskschedulerschema-idletriggertype-complextype.md)                 | Gibt einen-Auslösers an, der einen Task startet, wenn der Computer in den Leerlauf wechselt.<br/> |
| [**Logonauslöst**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logontriggertype**](taskschedulerschema-logontriggertype-complextype.md)               | Gibt einen-Vorgang an, der einen Task startet, wenn sich ein Benutzer anmeldet.<br/>                       |
| [**Registration-Auslösers**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationtriggertype**](taskschedulerschema-registrationtriggertype-complextype.md) | Gibt einen-Typ an, der einen Task startet, wenn der Task registriert wird.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timetriggertype**](taskschedulerschema-timetriggertype-complextype.md)                 | Gibt einen-Auslösers an, der einen Task startet, wenn der--ausgelöst wird<br/>             |



## <a name="remarks"></a>Bemerkungen

Bei der Skripterstellung wird das Ausführungszeit Limit mithilfe der [**Trigger.Executiontimelimit**](trigger-executiontimelimit.md) -Eigenschaft angegeben, die von den all-Triggerobjekten geerbt wird.

Bei der C++-Entwicklung wird das Ausführungszeit Limit mithilfe der [**ITrigger: executiontimelimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) -Eigenschaft angegeben, die von den all-triggerschnittstellen geerbt wird.

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

 

 





