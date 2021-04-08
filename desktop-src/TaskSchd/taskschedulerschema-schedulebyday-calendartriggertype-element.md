---
title: Schedulebyday (calendartriggertype)-Element
description: Gibt einen täglichen Zeitplan an.
ms.assetid: 5a6097ce-a855-4b08-84c5-71f06343805e
keywords:
- täglicher Taskplaner des Auslösers, XML-Element
- Schedulebyday-Element Taskplaner
topic_type:
- apiref
api_name:
- ScheduleByDay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 614777ede63605dc7ed6936bda952c6071bda371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956958"
---
# <a name="schedulebyday-calendartriggertype-element"></a>Schedulebyday (calendartriggertype)-Element

Gibt einen täglichen Zeitplan an. Der Task wird z. b. täglich um 8:00 Uhr täglich, täglich, an jedem dritten Tag usw. gestartet.

``` syntax
<xs:element name="ScheduleByDay"
    type="dailyScheduleType"
 />
```

Das **schedulebyday** -Element wird durch den komplexen Typ [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                             | Abgeleitet von                                                                       | BESCHREIBUNG                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**Calendarausgelöst**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md) | Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                            | type             | BESCHREIBUNG                                                         |
|------------------------------------------------------------------------------------|------------------|---------------------------------------------------------------------|
| [**Daysinterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) | **unsignedByte** | Gibt das Intervall zwischen den Tagen im Zeitplan an.<br/> |



## <a name="remarks"></a>Bemerkungen

Das zuvor aufgeführte untergeordnete Element wird von den komplexen Elementtypen [**dailyscheduletype**](taskschedulerschema-dailyscheduletype-complextype.md) definiert.

Die Uhrzeit, zu der die Aufgabe gestartet wird, wird durch das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element festgelegt.

Bei der Skripterstellung wird ein täglicher-Fehler mithilfe des [**Daily-auslöserobjekts**](weeklytrigger.md) angegeben.

Bei der C++-Entwicklung wird ein täglicher-Fehler mithilfe der [**idaily-**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) Schnittstelle angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen täglichen Kalender--Auslösers, der die Aufgabe täglich startet.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen täglichen Zeitplan angibt, finden Sie unter Beispiel für das [tägliche Beispiel (XML)](daily-trigger-example--xml-.md).

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

 

 





