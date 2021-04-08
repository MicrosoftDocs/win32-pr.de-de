---
title: Interval (restarttype)-Element
description: Gibt an, wie lange der Taskplaner versucht, den Task neu zu starten.
ms.assetid: 00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1
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
ms.openlocfilehash: c97e754e0b29a43d6ba419bd806404fe1b85b2b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949517"
---
# <a name="interval-restarttype-element"></a>Interval (restarttype)-Element

Gibt an, wie lange der Taskplaner versucht, den Task neu zu starten. Das Format für diese Zeichenfolge ist P <days> dt <hours> H <minutes> M <seconds> S ("PT5M" ist beispielsweise 5 Minuten, "PT1H" ist 1 Stunde, und "PT20M" beträgt 20 Minuten). Die maximal zulässige Dauer beträgt 31 Tage, und die zulässige Mindestanzahl beträgt 1 Minute.

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

Das-Element wird durch den komplexen [**restarttype**](taskschedulerschema-restarttype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                               | Abgeleitet von                                                       | BESCHREIBUNG                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**Neustartonfailure**](taskschedulerschema-restartonfailure-settingstype-element.md) | [**neustarttype**](taskschedulerschema-restarttype-complextype.md) | Gibt an, dass der Taskplaner den Task neu starten soll, wenn die Aufgabe aus irgendeinem Grund fehlschlägt.<br/> |



## <a name="remarks"></a>Bemerkungen

Wenn dieses Element angegeben ist, muss auch das [**count**](taskschedulerschema-count-restarttype-element.md) -Element angegeben werden, um den Taskplaner anzugeben, wie oft versucht werden soll, den Task neu zu starten.

Informationen zur C++-Entwicklung finden Sie unter [**restartinterval-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).

Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. restartinterval**](tasksettings-restartinterval.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





