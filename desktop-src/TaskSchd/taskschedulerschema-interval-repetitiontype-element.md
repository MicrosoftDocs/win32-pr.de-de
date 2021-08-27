---
title: Interval -Element (wiederholungstyp)
description: Gibt die Zeit zwischen jedem Neustart der Aufgabe an.
ms.assetid: 28c6475a-88e3-44ac-92c7-6f463e8460c9
keywords:
- Interval-Taskplaner
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec6f2724f4374ed94fff47e6577a2887ca953cae0af66de9c64971cd80aa2050
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100000"
---
# <a name="interval-repetitiontype-element"></a>Interval -Element (wiederholungstyp)

Gibt die Zeit zwischen jedem Neustart der Aufgabe an. Das Format für diese Zeichenfolge ist (z. B. `P<days>DT<hours>H<minutes>M<seconds>S` ist "PT5M" 5 Minuten, "PT1H" ist 1 Stunde und "PT20M" beträgt 20 Minuten). Die maximal zulässige Zeit beträgt 31 Tage, und die zulässige Mindestzeit beträgt 1 Minute.

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

Das Element wird durch den komplexen [**Wiederholungstyp "repetitionType"**](taskschedulerschema-repetitiontype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                      | Abgeleitet von                                                             | BESCHREIBUNG                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Wiederholen**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**wiederholungstyp**](taskschedulerschema-repetitiontype-complextype.md) | Gibt an, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird das Intervall des Wiederholungsmusters mithilfe der [**RepetitionPattern.Interval-Eigenschaft**](repetitionpattern-interval.md) angegeben.

Für die C++-Entwicklung wird das Intervall des Wiederholungsmusters mithilfe der [**IRepetitionPattern::Interval-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) angegeben.

## <a name="examples"></a>Beispiele

Ein vollständiges Beispiel für den XML-Code für eine Aufgabe, die ein Wiederholungsintervall verwendet, finden Sie unter Beispiel für tägliche [Trigger (XML).](daily-trigger-example--xml-.md)

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

 

 





