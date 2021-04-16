---
title: Wiederholungs Element (triggerbasetype)
description: Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.
ms.assetid: d43c7f9a-3a7b-44a9-901b-9ad18c027b1b
keywords:
- Wiederholungs Element Taskplaner
topic_type:
- apiref
api_name:
- Repetition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ebd6f9f77998e5e975e24ff752a475e3880c0aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477778"
---
# <a name="repetition-triggerbasetype-element"></a>Wiederholungs Element (triggerbasetype)

Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.

``` syntax
<xs:element name="Repetition"
    type="repetitionType"
 />
```

Das **Wiederholungs** Element wird durch den komplexen Typ [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) definiert.

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



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                   | type     | BESCHREIBUNG                                                                                                         |
|-------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| [**Duration**](taskschedulerschema-duration-repetitiontype-element.md)                   | duration | Gibt an, wie lange das Muster wiederholt wird.<br/>                                                              |
| [**Intervall**](taskschedulerschema-interval-repetitiontype-element.md)                   | duration | Gibt die Zeitspanne zwischen den einzelnen Neustarts der Aufgabe an.<br/>                                           |
| [**Stopatdurationend**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | boolean  | Gibt an, dass eine laufende Instanz der Aufgabe am Ende der Wiederholungsmuster Dauer beendet wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Wenn Sie eine Wiederholungs Dauer für eine Aufgabe angeben, müssen Sie auch das Wiederholungsintervall angeben.

Wenn Sie eine Aufgabe registrieren, die einen-Auslösers mit einem Wiederholungsintervall von einer Minute und einer Wiederholungs Dauer von vier Minuten enthält, wird die Aufgabe fünfmal gestartet. Die fünf Wiederholungen können mithilfe des folgenden Musters definiert werden.

1.  Eine Aufgabe beginnt am Anfang der ersten Minute.
2.  Die nächste Aufgabe beginnt am Ende der ersten Minute.
3.  Die nächste Aufgabe beginnt am Ende der zweiten Minute.
4.  Die nächste Aufgabe beginnt am Ende der dritten Minute.
5.  Die nächste Aufgabe beginnt am Ende der vierten Minute.

**Windows Server 2003, Windows XP und Windows 2000:** Wenn Sie eine Aufgabe registrieren, die einen-Auslösers mit einem Wiederholungsintervall von einer Minute und einer Wiederholungs Dauer von vier Minuten enthält, wird die Aufgabe viermal gestartet.

**Windows Vista, Windows 7, Windows Server 2008, Windows 8 und Windows Server 2012:** Wenn die Wiederholungs Dauer auf das genaue Vielfache des Intervalls festgelegt wird, ergibt sich in der Regel die oben beschriebene Anzahl. Unter bestimmten starken Ladebedingungen ist es jedoch möglich, dass die Dauer Zeitüberschreitung liegt, bevor TaskScheduler das abschließende Aufgaben Intervall starten kann.

Bei der Skripterstellung wird das Wiederholungsmuster mithilfe [**der Eigenschaft "" des "**](trigger-repetition.md) "

Bei der C++-Entwicklung wird das Wiederholungsmuster mithilfe der [**i-Funktion:: Wiederholungs**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) Eigenschaft angegeben, die von allen-auslöserschnittstellen geerbt wird.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein startauslöserelement, das ein Wiederholungsmuster für einen-Auslösers angibt


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition>
        <Interval></Interval>
        <Duration></Duration>
        <StopAtDurationEnd>true</StopAtDirationEnd>
    </Repetition>
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

 

 





