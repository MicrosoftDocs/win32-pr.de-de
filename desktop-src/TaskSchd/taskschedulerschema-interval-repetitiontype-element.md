---
title: Interval (repetitionType)-Element
description: Gibt die Zeitspanne zwischen jedem Neustart der Aufgabe an.
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
ms.openlocfilehash: bfb87884438f1a39a5bd6f08eb9bb855311eb5d3
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734195"
---
# <a name="interval-repetitiontype-element"></a>Interval (repetitionType)-Element

Gibt die Zeitspanne zwischen jedem Neustart der Aufgabe an. Das Format für diese Zeichenfolge lautet `P<days>DT<hours>H<minutes>M<seconds>S` (z. B. "PT5M" ist 5 Minuten, "PT1H" ist 1 Stunde und "PT20M" ist 20 Minuten). Die maximal zulässige Zeit beträgt 31 Tage, und die zulässige Mindestzeit beträgt 1 Minute.

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

Das Element wird durch den komplexen [**Wiederholungstyp**](taskschedulerschema-repetitiontype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                      | Abgeleitet von                                                             | BESCHREIBUNG                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Wiederholen**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**wiederholungstyp**](taskschedulerschema-repetitiontype-complextype.md) | Gibt an, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde.<br/> |



## <a name="remarks"></a>Bemerkungen

Für die Skriptentwicklung wird das Intervall des Wiederholungsmusters mithilfe der [**RepetitionPattern.Interval-Eigenschaft**](repetitionpattern-interval.md) angegeben.

Für die C++-Entwicklung wird das Intervall des Wiederholungsmusters mithilfe der [**IRepetitionPattern::Interval-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) angegeben.

## <a name="examples"></a>Beispiele

Ein vollständiges Beispiel für den XML-Code für eine Aufgabe, die ein Wiederholungsintervall verwendet, finden Sie unter Beispiel für [täglichen Trigger (XML).](daily-trigger-example--xml-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





