---
title: Wiederholungselement (triggerBaseType)
description: Gibt an, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde.
ms.assetid: d43c7f9a-3a7b-44a9-901b-9ad18c027b1b
keywords:
- Wiederholungselement Taskplaner
topic_type:
- apiref
api_name:
- Repetition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dfcce3e008a9959ca279f64c83a898eb2239d007d8fc32dfb5da5942395055bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959540"
---
# <a name="repetition-triggerbasetype-element"></a>Wiederholungselement (triggerBaseType)

Gibt an, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde.

``` syntax
<xs:element name="Repetition"
    type="repetitionType"
 />
```

Das **Wiederholungselement** wird durch den komplexen [**TriggerBaseType-Typ**](taskschedulerschema-triggerbasetype-complextype.md) definiert.

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



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                   | Typ     | Beschreibung                                                                                                         |
|-------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| [**Duration**](taskschedulerschema-duration-repetitiontype-element.md)                   | duration | Gibt an, wie lange das Muster wiederholt wird.<br/>                                                              |
| [**Intervall**](taskschedulerschema-interval-repetitiontype-element.md)                   | duration | Gibt die Zeitspanne zwischen jedem Neustart der Aufgabe an.<br/>                                           |
| [**StopAtDurationEnd**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | boolean  | Gibt an, dass eine ausgeführte Instanz des Tasks am Ende der Wiederholungsmusterdauer beendet wird.<br/> |



## <a name="remarks"></a>Hinweise

Wenn Sie eine Wiederholungsdauer für eine Aufgabe angeben, müssen Sie auch das Wiederholungsintervall angeben.

Wenn Sie eine Aufgabe registrieren, die einen Trigger mit einem Wiederholungsintervall von einer Minute und einer Wiederholungsdauer von vier Minuten enthält, wird der Task fünfmal gestartet. Die fünf Wiederholungen können im folgenden Muster definiert werden.

1.  Eine Aufgabe beginnt am Anfang der ersten Minute.
2.  Die nächste Aufgabe beginnt am Ende der ersten Minute.
3.  Die nächste Aufgabe beginnt am Ende der zweiten Minute.
4.  Die nächste Aufgabe beginnt am Ende der dritten Minute.
5.  Die nächste Aufgabe beginnt am Ende der vierten Minute.

**Windows Server 2003, Windows XP und Windows 2000:** Wenn Sie eine Aufgabe registrieren, die einen Trigger mit einem Wiederholungsintervall von einer Minute und einer Wiederholungsdauer von vier Minuten enthält, wird die Aufgabe viermal gestartet.

**Windows Vista, Windows 7, Windows Server 2008, Windows 8 und Windows Server 2012:** Wenn Sie die Wiederholungsdauer auf ein exaktes Vielfaches des Intervalls festlegen, ergeben sich in der Regel die oben beschriebenen Zahlen. Unter bestimmten Bedingungen mit hoher Auslastung ist es jedoch möglich, für die Dauer ein Timeout zu erreichen, bevor TaskScheduler das letzte Aufgabenintervall starten kann.

Für die Skriptentwicklung wird das Wiederholungsmuster mithilfe der [**Trigger.Repetition-Eigenschaft**](trigger-repetition.md) angegeben, die von allen Triggerobjekten geerbt wird.

Für die C++-Entwicklung wird das Wiederholungsmuster mithilfe der [**ITRigger::Repetition-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) angegeben, die von allen Triggerschnittstellen geerbt wird.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Starttriggerelement, das ein Wiederholungsmuster für einen Trigger angibt.


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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





