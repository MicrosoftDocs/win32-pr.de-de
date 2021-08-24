---
title: Hidden(settingsType)-Element
description: Gibt an, dass die Aufgabe standardmäßig nicht auf der Benutzeroberfläche angezeigt wird.
ms.assetid: a08c270f-6d4e-4473-9538-c1e1e21b3b10
keywords:
- Hidden-Element Taskplaner
topic_type:
- apiref
api_name:
- Hidden
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9820008ead01930eff23a50408f4952d08e9190984432f65c3d9e5f4eedbef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658910"
---
# <a name="hidden-settingstype-element"></a>Hidden(settingsType)-Element

Gibt an, dass die Aufgabe standardmäßig nicht auf der Benutzeroberfläche angezeigt wird. Administratoren können diese Einstellung jedoch überschreiben, indem sie einen "Masterschalter" verwenden, der alle Aufgaben auf der Benutzeroberfläche sichtbar macht.

``` syntax
<xs:element name="Hidden"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

Das **Hidden-Element** wird durch den komplexen [**SettingsType-Typ**](taskschedulerschema-settingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | Beschreibung                                                                    |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**Hidden Property of ITaskSettings (Ausgeblendete Eigenschaft von ITaskSettings).**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden)

Informationen zur Skriptentwicklung finden Sie unter [**TaskSettings.Hidden.**](tasksettings-hidden.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





