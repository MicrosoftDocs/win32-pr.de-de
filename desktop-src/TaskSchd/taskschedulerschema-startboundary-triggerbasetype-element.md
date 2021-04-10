---
title: StartBoundary (triggerbasetype)-Element
description: Gibt das Datum und die Uhrzeit der Aktivierung des Auslösers an.
ms.assetid: 95a62ae5-4eba-49df-a25f-0d1181772833
keywords:
- StartBoundary-Element Taskplaner
topic_type:
- apiref
api_name:
- StartBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d6adf90de2f3b199f98737996fe732f342787b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103182"
---
# <a name="startboundary-triggerbasetype-element"></a>StartBoundary (triggerbasetype)-Element

Gibt das Datum und die Uhrzeit der Aktivierung des Auslösers an.

``` syntax
<xs:element name="StartBoundary"
    type="dateTime"
 />
```

Das **StartBoundary** -Element wird durch den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Typ definiert.

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

Das **<StartBoundary>** -Element ist ein erforderliches Element für Zeit-und Kalender Trigger ( [**<TimeTrigger>**](taskschedulerschema-timetrigger-triggergroup-element.md) und [**<CalendarTrigger>**](taskschedulerschema-calendartrigger-triggergroup-element.md) ).

Bei der Entwicklung von Skripts wird die Endgrenze mithilfe [**der Eigenschaft "" des Typs**](trigger-startboundary.md) "" von "alle Auslöse Objekte" geerbt.

Bei der C++-Entwicklung wird die Endgrenze mithilfe der [**i-Funktion:: StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) -Eigenschaft angegeben, die von den all-auslöserschnittstellen geerbt wird.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Start-Auslöserelement, das eine Start Grenze von 1. Januar 2005:8:00 Uhr definiert.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





