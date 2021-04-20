---
title: Interval (restartType)-Element
description: Gibt an, wie lange der Taskplaner versucht, den Task neu zu starten.
ms.assetid: 00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1
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
ms.openlocfilehash: 6e731582364df23bdef800ab5d2cf15dd5c882ae
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734185"
---
# <a name="interval-restarttype-element"></a>Interval (restartType)-Element

Gibt an, wie lange der Taskplaner versucht, den Task neu zu starten. Das Format für diese Zeichenfolge ist (z. B. `P<days>DT<hours>H<minutes>M<seconds>S` ist "PT5M" 5 Minuten, "PT1H" ist 1 Stunde und "PT20M" beträgt 20 Minuten). Die maximal zulässige Zeit beträgt 31 Tage, und die zulässige Mindestzeit beträgt 1 Minute.

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

Das -Element wird durch den komplexen [**restartType-Typ**](taskschedulerschema-restarttype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                               | Abgeleitet von                                                       | BESCHREIBUNG                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md) | [**restartType**](taskschedulerschema-restarttype-complextype.md) | Gibt an, dass der Taskplaner versucht, den Task neu zu starten, wenn der Task aus irgendeinem Grund fehlschlägt.<br/> |



## <a name="remarks"></a>Bemerkungen

Wenn dieses Element angegeben wird, muss auch [**das Count-Element**](taskschedulerschema-count-restarttype-element.md) angegeben werden, um dem Benutzer Taskplaner, wie oft versucht werden soll, den Task neu zu starten.

Informationen zur C++-Entwicklung finden Sie unter [**RestartInterval-Eigenschaft von ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval)

Informationen zur Skriptentwicklung finden Sie [**unter TaskSettings.RestartInterval**](tasksettings-restartinterval.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





