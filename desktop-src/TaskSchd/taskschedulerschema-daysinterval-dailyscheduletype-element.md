---
title: Daysinterval-Element (dailyscheduletype)
description: Gibt das Intervall zwischen den Tagen im Zeitplan an.
ms.assetid: 495ea1c0-37eb-4b12-8241-bfc6489e33ed
keywords:
- Daysinterval-Element Taskplaner
topic_type:
- apiref
api_name:
- DaysInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97b50581aa4825b31983a234a5eb47ff7b7b7e06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949521"
---
# <a name="daysinterval-dailyscheduletype-element"></a>Daysinterval-Element (dailyscheduletype)

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

Das-Element wird durch den komplexen Typ " [**dailyscheduletype**](taskschedulerschema-dailyscheduletype-complextype.md) " definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                | Abgeleitet von                                                                   | BESCHREIBUNG                            |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|----------------------------------------|
| [**Schedulebyday**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) | [**dailyscheduletype**](taskschedulerschema-dailyscheduletype-complextype.md) | Gibt einen täglichen Zeitplan an.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skript Entwicklung wird das Tage Intervall für einen täglichen-Befehl von der [**Daily-Eigenschaft. daysinterval**](dailytrigger-daysinterval.md) angegeben.

Bei der C++-Entwicklung wird das Tage Intervall für einen täglichen-Befehl durch die [**idaily-Funktion::D aysinterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) -Eigenschaft angegeben.

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

 

 





