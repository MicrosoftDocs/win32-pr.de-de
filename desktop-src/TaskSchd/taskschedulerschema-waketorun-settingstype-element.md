---
title: WakeToRun-Element (settingsType)
description: Gibt an, dass Taskplaner den Computer aktiviert, wenn die Aufgabe ausgeführt werden soll.
ms.assetid: 5fb53016-5778-463d-bb32-3c1da2de6fc2
keywords:
- WakeToRun-Element Taskplaner
topic_type:
- apiref
api_name:
- WakeToRun
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12d16f9f06685a427a8f3e7c4f2356dff0bc6415e50379ba752a4bc3a3fec8e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872060"
---
# <a name="waketorun-settingstype-element"></a>WakeToRun-Element (settingsType)

Gibt an, dass Taskplaner den Computer aktiviert, wenn die Aufgabe ausgeführt werden soll.

``` syntax
<xs:element name="WakeToRun"
    type="boolean"
 />
```

Das **WakeToRun-Element** wird durch den komplexen [**SettingsType-Typ**](taskschedulerschema-settingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="remarks"></a>Hinweise

Wenn der Taskplaner-Dienst den Computer aktiviert, um eine Aufgabe auszuführen, bleibt der Bildschirm möglicherweise deaktiviert, auch wenn sich der Computer nicht mehr im Standbymodus oder Ruhezustand befindet. Der Bildschirm wird eingeschaltet, wenn Windows Vista erkennt, dass ein Benutzer den Computer wieder verwendet hat.

Informationen zur C++-Entwicklung finden Sie unter [**WakeToRun-Eigenschaft von ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun)

Informationen zur Skriptentwicklung finden Sie unter [**TaskSettings.WakeToRun.**](tasksettings-waketorun.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





