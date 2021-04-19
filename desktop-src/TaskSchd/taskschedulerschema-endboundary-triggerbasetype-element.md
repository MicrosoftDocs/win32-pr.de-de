---
title: Endboundary (triggerbasetype)-Element
description: Gibt das Datum und die Uhrzeit der Deaktivierung des Auslösers an. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.
ms.assetid: 84731c0b-3fb8-44dd-be1a-67547add1f9e
keywords:
- Endboundary-Element Taskplaner
topic_type:
- apiref
api_name:
- EndBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d687655498301595c1ab888fcc179ec0694f0aef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341589"
---
# <a name="endboundary-triggerbasetype-element"></a>Endboundary (triggerbasetype)-Element

Gibt das Datum und die Uhrzeit der Deaktivierung des Auslösers an. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.

``` syntax
<xs:element name="EndBoundary"
    type="dateTime"
 />
```

Das **endboundary** -Element wird durch den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Typ definiert.

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

Bei der Entwicklung von Skripts wird die Endgrenze mithilfe der "" [**-Eigenschaft von**](trigger-endboundary.md) "" für alle Auslöse Objekte geerbt.

Bei der C++-Entwicklung wird die Endgrenze mithilfe der [**i-Funktion:: endboundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) -Eigenschaft angegeben, die von den all-auslöserschnittstellen geerbt wird.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Start-Auslöserelement, das eine Endgrenze von 1. Januar 2007:8:00 Uhr definiert.


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

 

 





