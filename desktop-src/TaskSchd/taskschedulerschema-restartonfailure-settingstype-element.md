---
title: Restartonfailure (settingstype)-Element
description: Gibt an, dass der Taskplaner den Task neu starten soll, wenn die Aufgabe aus irgendeinem Grund fehlschlägt.
ms.assetid: c90d8c62-dd97-4ea6-bd87-37b0915e0b38
keywords:
- Restartonfailure-Element Taskplaner
topic_type:
- apiref
api_name:
- RestartOnFailure
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4239d21362d589cae84252c728387b2a2b6159e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213748"
---
# <a name="restartonfailure-settingstype-element"></a>Restartonfailure (settingstype)-Element

Gibt an, dass der Taskplaner den Task neu starten soll, wenn die Aufgabe aus irgendeinem Grund fehlschlägt.

``` syntax
<xs:element name="RestartOnFailure"
    type="restartType"
    minOccurs="0"
 />
```

Das **restartonfailure** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                              | type         | BESCHREIBUNG                                                                                        |
|----------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------|
| [**Countdown**](taskschedulerschema-count-restarttype-element.md)       | unsignedByte | Gibt an, wie oft das Taskplaner versucht, den Task neu zu starten.<br/> |
| [**Intervall**](taskschedulerschema-interval-restarttype-element.md) | duration     | Gibt an, wie lange der Taskplaner versucht, den Task neu zu starten.<br/>                 |



## <a name="remarks"></a>Bemerkungen

Wenn eine Anwendung Task Einstellungen angibt, erfolgt der Zugriff auf diese Informationen über die Eigenschaften [**restartcount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) und [**restartinterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) der [**itasksettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) -Schnittstelle. Bei der Skripterstellung erfolgt der Zugriff auf diese Informationen über die Eigenschaften " [**tasksettings. restartcount**](tasksettings-restartcount.md) " und " [**tasksettings. restartinterval**](tasksettings-restartinterval.md) ".

Beide untergeordneten Elemente müssen festgelegt werden, um anzugeben, wie die Taskplaner den Task neu startet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





