---
title: Triggers -Element (taskType)
description: Gibt die Trigger an, die die Aufgabe starten.
ms.assetid: 4bf8e85e-3742-433d-821f-736fb2ff7139
keywords:
- Triggers-Taskplaner
topic_type:
- apiref
api_name:
- Triggers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d067c9e315006c55e07e972e5616525750d8a383d7ed8294f7d39a6acf32caff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610884"
---
# <a name="triggers-tasktype-element"></a>Triggers -Element (taskType)

Gibt die Trigger an, die die Aufgabe starten.

``` syntax
<xs:element name="Triggers"
    type="triggersType"
 />
```

Das **Triggers-Element** wird durch den komplexen [**triggersType-Typ**](taskschedulerschema-triggerstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                          | Abgeleitet von                                                 | Beschreibung                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Aufgabe**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Definiert die Aufgabe, die vom Dienst Taskplaner wird.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                     | type                                                                                       | Beschreibung                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | Gibt einen Trigger an, der eine Aufgabe startet, wenn das System gestartet wird.<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen DOW-Trigger (Day-of-the-Week) an.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)               | Gibt einen Trigger an, der eine Aufgabe startet, wenn ein Systemereignis auftritt.<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | Gibt einen Trigger an, der eine Aufgabe startet, wenn der Computer in den Leerlaufzustand übergeht.<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | Gibt einen Trigger an, der eine Aufgabe startet, wenn sich ein Benutzer anmeldet.<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Gibt einen Trigger an, der eine Aufgabe startet, wenn der Task registriert wird.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                 | Gibt einen Trigger an, der eine Aufgabe startet, wenn der Trigger aktiviert wird.<br/>             |



## <a name="remarks"></a>Hinweise

Die oben aufgeführten untergeordneten Elemente können in beliebiger Reihenfolge hinzugefügt werden.

Für die C++-Entwicklung werden die Trigger einer Aufgabe mithilfe der [**Triggers-Eigenschaft von ITaskDefinition angegeben.**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers)

Für die Skriptentwicklung werden die Trigger einer Aufgabe mithilfe der [**TaskDefinition.Triggers-Eigenschaft**](taskdefinition-triggers.md) angegeben.

## <a name="examples"></a>Beispiele

Ein vollständiges Xml-Beispiel für eine Aufgabe, die einen Trigger angibt, finden Sie unter [Time Trigger Example (XML) .](time-trigger-example--xml-.md)

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

 

 





