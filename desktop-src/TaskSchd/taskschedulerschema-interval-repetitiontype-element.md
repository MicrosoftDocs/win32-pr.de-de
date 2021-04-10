---
title: Interval (repetitiontype)-Element
description: Gibt die Zeitspanne zwischen den einzelnen Neustarts der Aufgabe an.
ms.assetid: 28c6475a-88e3-44ac-92c7-6f463e8460c9
keywords:
- Interval-Element Taskplaner
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9720bc2257d4c0b45116089bfdd4113335fc6b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949643"
---
# <a name="interval-repetitiontype-element"></a>Interval (repetitiontype)-Element

Gibt die Zeitspanne zwischen den einzelnen Neustarts der Aufgabe an. Das Format für diese Zeichenfolge ist P <days> dt <hours> H <minutes> M <seconds> S ("PT5M" ist beispielsweise 5 Minuten, "PT1H" ist 1 Stunde, und "PT20M" beträgt 20 Minuten). Die maximal zulässige Dauer beträgt 31 Tage, und die zulässige Mindestanzahl beträgt 1 Minute.

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
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

Bei der Skripterstellung wird das Intervall des Wiederholungs Musters mithilfe der [**repetitionpattern. Interval**](repetitionpattern-interval.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird das Intervall des Wiederholungs Musters mithilfe der [**irepetitionpattern:: Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die ein Wiederholungsintervall verwendet, finden Sie unter Beispiel für das [tägliche Beispiel (XML)](daily-trigger-example--xml-.md).

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

 

 





