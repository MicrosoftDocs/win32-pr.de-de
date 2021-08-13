---
title: StartBoundary (triggerBaseType)-Element
description: Gibt das Datum und die Uhrzeit der Aktivierung des Triggers an.
ms.assetid: 95a62ae5-4eba-49df-a25f-0d1181772833
keywords:
- StartBoundary-Taskplaner
topic_type:
- apiref
api_name:
- StartBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32b91557d812888d9bb6e970be37703537bb3d7645c8a0422df19d5d5fe37a5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119401964"
---
# <a name="startboundary-triggerbasetype-element"></a>StartBoundary (triggerBaseType)-Element

Gibt das Datum und die Uhrzeit der Aktivierung des Triggers an.

``` syntax
<xs:element name="StartBoundary"
    type="dateTime"
 />
```

Das **StartBoundary-Element** wird durch den komplexen [**TriggerBaseType-Typ**](taskschedulerschema-triggerbasetype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                     | Abgeleitet von                                                                               | BESCHREIBUNG                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | Gibt einen Trigger an, der eine Aufgabe startet, wenn das System gestartet wird.<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen DOW-Trigger (Day-of-the-Week) an.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)               | Gibt einen Trigger an, der eine Aufgabe startet, wenn ein Systemereignis auftritt.<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | Gibt einen Trigger an, der eine Aufgabe startet, wenn der Computer in den Leerlaufzustand übergeht.<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | Gibt einen Trigger an, der eine Aufgabe startet, wenn sich ein Benutzer anmeldet.<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Gibt einen Trigger an, der eine Aufgabe startet, wenn die Aufgabe registriert wird.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                 | Gibt einen Trigger an, der eine Aufgabe startet, wenn der Trigger aktiviert wird.<br/>             |



## <a name="remarks"></a>Hinweise

Das **<StartBoundary>** -Element ist ein erforderliches Element für Zeit- und Kalendertrigger ( [**<TimeTrigger>**](taskschedulerschema-timetrigger-triggergroup-element.md) und [**<CalendarTrigger>**](taskschedulerschema-calendartrigger-triggergroup-element.md) ).

Für die Skriptentwicklung wird die Endgrenze mithilfe der [**Trigger.StartBoundary-Eigenschaft**](trigger-startboundary.md) angegeben, die von allen Triggerobjekten geerbt wird.

Für die C++-Entwicklung wird die Endgrenze mithilfe der [**ITrigger::StartBoundary-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) angegeben, die von allen Triggerschnittstellen geerbt wird.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Starttriggerelement, das eine Startgrenze vom 1. Januar 2005: 8:00 Uhr definiert.


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



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

 

 





