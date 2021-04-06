---
title: Trigger (TaskType)-Element
description: Gibt die Trigger an, die den Task starten.
ms.assetid: 4bf8e85e-3742-433d-821f-736fb2ff7139
keywords:
- Trigger-Element Taskplaner
topic_type:
- apiref
api_name:
- Triggers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06994c395fbfbc5b0c6244c9d17930bc4afac885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743753"
---
# <a name="triggers-tasktype-element"></a>Trigger (TaskType)-Element

Gibt die Trigger an, die den Task starten.

``` syntax
<xs:element name="Triggers"
    type="triggersType"
 />
```

Das **Trigger** -Element wird durch den komplexen [**triggerstype**](taskschedulerschema-triggerstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                          | Abgeleitet von                                                 | BESCHREIBUNG                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Aufgabe**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Definiert den Task, der vom Taskplaner-Dienst ausgeführt wird.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                     | type                                                                                       | BESCHREIBUNG                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**Boottrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**boottriggertype**](taskschedulerschema-boottriggertype-complextype.md)                 | Gibt einen-Fehler an, mit dem eine Aufgabe gestartet wird, wenn das System gestartet wird.<br/>                 |
| [**Calendarausgelöst**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md)         | Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventtriggertype**](taskschedulerschema-eventtriggertype-complextype.md)               | Gibt einen-Fehler an, der einen Task startet, wenn ein System Ereignis auftritt.<br/>                |
| [**Idle-Auslösung**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idletriggertype**](taskschedulerschema-idletriggertype-complextype.md)                 | Gibt einen-Auslösers an, der einen Task startet, wenn der Computer in den Leerlauf wechselt.<br/> |
| [**Logonauslöst**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logontriggertype**](taskschedulerschema-logontriggertype-complextype.md)               | Gibt einen-Vorgang an, der einen Task startet, wenn sich ein Benutzer anmeldet.<br/>                       |
| [**Registration-Auslösers**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationtriggertype**](taskschedulerschema-registrationtriggertype-complextype.md) | Gibt einen-Typ an, der einen Task startet, wenn der Task registriert wird.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timetriggertype**](taskschedulerschema-timetriggertype-complextype.md)                 | Gibt einen-Auslösers an, der einen Task startet, wenn der--ausgelöst wird<br/>             |



## <a name="remarks"></a>Bemerkungen

Die oben aufgeführten untergeordneten Elemente können in beliebiger Reihenfolge hinzugefügt werden.

Bei der C++-Entwicklung werden die Trigger einer Aufgabe mithilfe der Triggers- [**Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers)angegeben.

Bei der Skripterstellung werden die Trigger einer Aufgabe mithilfe der [**Taskdefinition.**](taskdefinition-triggers.md) Triggers-Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen-Auslösers angibt, finden Sie unter [time-auslöserbeispiel (XML)](time-trigger-example--xml-.md)

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

 

 





