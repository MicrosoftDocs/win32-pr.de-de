---
title: Duration (repetitiontype)-Element
description: Gibt an, wie lange das Muster wiederholt wird.
ms.assetid: a24f3827-18b2-465e-b132-77dce139e0d4
keywords:
- Duration-Element Taskplaner
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3772abb0224b03db4985de126e1d9cc0058ab5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341327"
---
# <a name="duration-repetitiontype-element"></a>Duration (repetitiontype)-Element

Gibt an, wie lange das Muster wiederholt wird. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> . Wenn für die Dauer kein Wert angegeben wird, wird das Muster unbegrenzt wiederholt. Der Mindestwert ist eine Minute.

``` syntax
<xs:element name="Duration"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das-Element wird durch den komplexen Typ " [**wiederholtiontype**](taskschedulerschema-repetitiontype-complextype.md) " definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                      | Abgeleitet von                                                             | BESCHREIBUNG                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Wiederholen**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**Wiederholungstyp**](taskschedulerschema-repetitiontype-complextype.md) | Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei Skript Anwendungen wird die Dauer des Musters mithilfe der [**wiederholtionpattern. Duration**](repetitionpattern-duration.md) -Eigenschaft angegeben.

Für C++-Anwendungen wird die Dauer des Musters mithilfe der [**irepetitionpattern::D urations**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Wiederholungsmuster für einen-Auslösers.


```XML
<Repetition>
    <Interval></Interval>
    <Duration></Duration>
    <StopAtDurationEnd>true</StopAtDirationEnd>
</Repetition>
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

 

 





