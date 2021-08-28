---
title: DisallowStartIfOnElement (settingsType)
description: Gibt an, dass der Task nicht gestartet wird, wenn der Computer mit Akkus ausgeführt wird.
ms.assetid: 48c0fd32-4441-4628-8090-c736f2945b4d
keywords:
- DisallowStartIfOnElement-Taskplaner
topic_type:
- apiref
api_name:
- DisallowStartIfOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efd78b3e868c41431521b4c584a4044b9086362cf55d86466eb38ed75fcee148
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100040"
---
# <a name="disallowstartifonbatteries-settingstype-element"></a>DisallowStartIfOnElement (settingsType)

Gibt an, dass der Task nicht gestartet wird, wenn der Computer mit Akkus ausgeführt wird.

``` syntax
<xs:element name="DisallowStartIfOnBatteries"
    type="boolean"
 />
```

Das **DisallowStartIfOn Wies-Element** wird durch den komplexen [**settingsType-Typ**](taskschedulerschema-settingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="remarks"></a>Hinweise

Die Standardeinstellung für dieses Element ist True.

Für die Skriptentwicklung erfolgt der Zugriff auf diese Informationen über die [**TaskSettings.DisallowStartIfOn Wies-Eigenschaft.**](tasksettings-disallowstartifonbatteries.md)

Bei der C++-Entwicklung erfolgt der Zugriff auf diese Informationen über die [**ITaskSettings::D isallowStartIfOn Wies-Eigenschaft.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries)

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Einstellungselement, das die Ausführung des Task nicht zu erlaubt, wenn der Computer auf Akkus ausgeführt wird.


```XML
<Settings>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
</Settings>
        
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





