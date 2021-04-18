---
title: Calendartrigger (triggergroup)-Element
description: Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.
ms.assetid: 9b9218bf-222c-4ece-8b37-5c5d8b765015
keywords:
- Calendar-auslöserTaskplaner, XML-Element
- Calendarauslöserelement Taskplaner
topic_type:
- apiref
api_name:
- CalendarTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02c061d8821dffa82eca8756ab26acadc6bb9281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338749"
---
# <a name="calendartrigger-triggergroup-element"></a>Calendartrigger (triggergroup)-Element

Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.

``` syntax
<xs:element name="CalendarTrigger"
    type="calendarTriggerType"
 />
```

Das **calendartrigger** -Element wird durch den komplexen Typ [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggerstype**](taskschedulerschema-triggerstype-complextype.md) | Gibt die Trigger an, die den Task starten.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                                            | type                                                                                                 | BESCHREIBUNG                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktiviert (triggerbasetype)**](taskschedulerschema-enabled-triggerbasetype-element.md)                                           | boolean                                                                                              | Gibt an, dass der-Wert aktiviert ist.<br/>                                                                                  |
| [**Endboundary (triggerbasetype)**](taskschedulerschema-endboundary-triggerbasetype-element.md)                                   | dateTime                                                                                             | Gibt das Datum und die Uhrzeit der Deaktivierung des Auslösers an. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.<br/> |
| [**Executiontimelimit (triggerbasetype)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)                     | duration                                                                                             | Gibt die maximale Zeitspanne an, in der der Task vom-Vorgang gestartet werden kann.<br/>                                   |
| [**Wiederholung (triggerbasetype)**](taskschedulerschema-repetition-triggerbasetype-element.md)                                     | [**Wiederholungstyp**](taskschedulerschema-repetitiontype-complextype.md)                             | Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.<br/>          |
| [**Schedulebyday (calendartriggertype)**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [**dailyscheduletype**](taskschedulerschema-dailyscheduletype-complextype.md)                       | Gibt einen täglichen Zeitplan an.<br/>                                                                                             |
| [**Schedulebymonth (calendartriggertype)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [**monthlyscheduletype**](taskschedulerschema-monthlyscheduletype-complextype.md)                   | Gibt einen monatlichen Zeitplan an.<br/>                                                                                           |
| [**Schedulebymonthdayoatweek (calendartriggertype)**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlydayosweekscheduletype**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Gibt einen-Vorgang an, durch den ein Auftrag an einem monatlichen Wochentag gestartet wird.<br/>                                                |
| [**Schedulebyweek (calendartriggertype)**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [**weeklyscheduletype**](taskschedulerschema-weeklyscheduletype-complextype.md)                     | Gibt einen wöchentlichen Zeitplan an.<br/>                                                                                            |
| [**StartBoundary (triggerbasetype)**](taskschedulerschema-startboundary-triggerbasetype-element.md)                               | dateTime                                                                                             | Gibt das Datum und die Uhrzeit der Aktivierung des Auslösers an. Dieses Element ist erforderlich.<br/>                                    |



## <a name="attributes"></a>Attributes



| Name | type | BESCHREIBUNG                               |
|------|------|-------------------------------------------|
| Id   | id   | Der Bezeichner des Auslösers.<br/> |



## <a name="remarks"></a>Bemerkungen

Das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element ist ein erforderliches Element für Zeit-und Kalender Trigger ([**timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) und **calendartrigger**).

Die oben aufgeführten untergeordneten Elemente werden von den komplexen Elementtypen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) und [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md) definiert.

Bei der Skript Entwicklung werden Kalender Trigger mithilfe eines der folgenden Objekte angegeben.

-   [**Dailylöst**](dailytrigger.md)
-   [**Weeklyauslösers**](weeklytrigger.md)
-   [**Monthly-auslöst**](monthlytrigger.md)
-   [**Monthlydowlöst**](monthlydowtrigger.md)

Bei der C++-Entwicklung werden Kalender Trigger mithilfe einer der folgenden Schnittstellen angegeben.

-   [**Idaily-Fehler**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [**Iweeklylöst**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)
-   [**Imonthly-Auslösung**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [**Imonthlydowlöst**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)

## <a name="examples"></a>Beispiele

Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen Kalender--Auslösers angibt, finden Sie unter Beispiel für das [tägliche Beispiel (XML)](daily-trigger-example--xml-.md)

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

 

 





