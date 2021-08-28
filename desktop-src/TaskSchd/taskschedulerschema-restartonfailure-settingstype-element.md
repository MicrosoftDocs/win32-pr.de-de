---
title: RestartOnFailure (settingsType)-Element
description: Gibt an, dass der Taskplaner versucht, den Task neu zu starten, wenn der Task aus irgendeinem Grund fehlschlägt.
ms.assetid: c90d8c62-dd97-4ea6-bd87-37b0915e0b38
keywords:
- RestartOnFailure-Taskplaner
topic_type:
- apiref
api_name:
- RestartOnFailure
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bfe29be7dd329def41e8a6726f141a850eb2daecd05e05d6b5988f543f64864c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072440"
---
# <a name="restartonfailure-settingstype-element"></a>RestartOnFailure (settingsType)-Element

Gibt an, dass der Taskplaner versucht, den Task neu zu starten, wenn der Task aus irgendeinem Grund fehlschlägt.

``` syntax
<xs:element name="RestartOnFailure"
    type="restartType"
    minOccurs="0"
 />
```

Das **RestartOnFailure-Element** wird durch den komplexen [**settingsType-Typ**](taskschedulerschema-settingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                              | type         | BESCHREIBUNG                                                                                        |
|----------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------|
| [**Anzahl**](taskschedulerschema-count-restarttype-element.md)       | unsignedByte | Gibt an, wie oft der Taskplaner versucht, den Task neu zu starten.<br/> |
| [**Intervall**](taskschedulerschema-interval-restarttype-element.md) | duration     | Gibt an, wie lange der Taskplaner versucht, den Task neu zu starten.<br/>                 |



## <a name="remarks"></a>Hinweise

Wenn eine Anwendung Aufgabeneinstellungen angibt, wird über die [**Eigenschaften RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) und [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) der [**ITaskSettings-Schnittstelle auf diese Informationen**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) zugegriffen. Für die Skripterstellung wird über die [**Eigenschaften TaskSettings.RestartCount**](tasksettings-restartcount.md) und [**TaskSettings.RestartInterval auf diese Informationen**](tasksettings-restartinterval.md) zugegriffen.

Beide untergeordneten Elemente müssen festgelegt werden, um anzugeben, wie Taskplaner Aufgabe neu startet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





