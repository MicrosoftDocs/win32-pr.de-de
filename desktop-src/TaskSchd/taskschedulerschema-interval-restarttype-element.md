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
ms.openlocfilehash: 2362a5d6ec1a6a9d0d876ef0673f4775e2db3ade0a83696ad2b993e31e02a9ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099990"
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



## <a name="remarks"></a>Hinweise

Wenn dieses Element angegeben wird, muss auch [**das Count-Element**](taskschedulerschema-count-restarttype-element.md) angegeben werden, um dem Benutzer Taskplaner, wie oft versucht werden soll, den Task neu zu starten.

Informationen zur C++-Entwicklung finden Sie unter [**RestartInterval-Eigenschaft von ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval)

Informationen zur Skriptentwicklung finden Sie [**unter TaskSettings.RestartInterval**](tasksettings-restartinterval.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





