---
title: DaysInterval (dailyScheduleType) -Element
description: Gibt das Intervall zwischen den Tagen im Zeitplan an.
ms.assetid: 495ea1c0-37eb-4b12-8241-bfc6489e33ed
keywords:
- DaysInterval-Element Taskplaner
topic_type:
- apiref
api_name:
- DaysInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e35df4f102801f7d52faeb384f9a1113e00abbf034026d19b5b7b6e7b4c90ed7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621100"
---
# <a name="daysinterval-dailyscheduletype-element"></a>DaysInterval (dailyScheduleType) -Element

Gibt das Intervall zwischen den Tagen im Zeitplan an.

``` syntax
<xs:element name="DaysInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedInt"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="365"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das -Element wird durch den [**komplexen DailyScheduleType-Typ**](taskschedulerschema-dailyscheduletype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                | Abgeleitet von                                                                   | Beschreibung                            |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|----------------------------------------|
| [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) | [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) | Gibt einen täglichen Zeitplan an.<br/> |



## <a name="remarks"></a>Hinweise

Bei der Skriptentwicklung wird das Tageintervall für einen täglichen Trigger von der [**DailyTrigger.DaysInterval-Eigenschaft**](dailytrigger-daysinterval.md) angegeben.

Bei der C++-Entwicklung wird das Tageintervall für einen täglichen Trigger durch die [**IDailyTrigger::D aysInterval-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen täglichen Kalendertrigger, der die Aufgabe jeden Tag startet.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



Ein vollständiges Beispiel für den XML-Code für eine Aufgabe, die einen täglichen Zeitplan angibt, finden Sie unter Beispiel für tägliche [Trigger (XML).](daily-trigger-example--xml-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





