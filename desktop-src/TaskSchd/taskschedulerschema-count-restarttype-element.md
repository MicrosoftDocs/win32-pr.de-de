---
title: Count (restarttype)-Element
description: Gibt an, wie oft das Taskplaner versucht, den Task neu zu starten.
ms.assetid: 67466c14-c9dd-49c8-a6ed-df7531fc63b8
keywords:
- Count-Element Taskplaner
topic_type:
- apiref
api_name:
- Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 655f636b725e48749540d67710afa57b3c45c89c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475969"
---
# <a name="count-restarttype-element"></a>Count (restarttype)-Element

Gibt an, wie oft das Taskplaner versucht, den Task neu zu starten.

``` syntax
<xs:element name="Count">
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
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

Wenn dieses Element angegeben ist, muss auch das [**Interval**](taskschedulerschema-interval-restarttype-element.md) -Element angegeben werden, um dem Taskplaner zu zeigen, wie lange versucht werden soll, den Task neu zu starten.

Informationen zur C++-Entwicklung finden Sie unter [**restartcount-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount).

Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. restartcount**](tasksettings-restartcount.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





