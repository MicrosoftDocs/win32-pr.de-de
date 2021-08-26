---
title: DisallowStartOnRemoteAppSession (settingsType)-Element
description: Gibt an, dass der Task nicht gestartet wird, wenn er ausgelöst wird, um in einer Rail-Sitzung (Remote Applications Integrated Locally) ausgeführt zu werden.
ms.assetid: 8323d8d9-fb6a-4876-9967-cc2344c77de3
keywords:
- DisallowStartOnRemoteAppSession-Element Taskplaner
topic_type:
- apiref
api_name:
- DisallowStartOnRemoteAppSession
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d2f7834ecd57fa10aaaabfa21945f1e908834d535d50f94b4dd21e6ca45c0a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010800"
---
# <a name="disallowstartonremoteappsession-settingstype-element"></a>DisallowStartOnRemoteAppSession (settingsType)-Element

Gibt an, dass der Task nicht gestartet wird, wenn er ausgelöst wird, um in einer Rail-Sitzung (Remote Applications Integrated Locally) ausgeführt zu werden.

``` syntax
<xs:element name="DisallowStartOnRemoteAppSession"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

Das **DisallowStartOnRemoteAppSession-Element** wird durch den komplexen [**settingsType-Typ**](taskschedulerschema-settingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | Beschreibung                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="remarks"></a>Hinweise

Die Standardeinstellung für dieses Element ist False.

Für die C++-Entwicklung erfolgt der Zugriff auf diese Informationen über die [**ITaskSettings2::D isallowStartOnRemoteAppSession-Eigenschaft.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession)

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Einstellungselement, das den Task nicht starten kann, wenn die Ausführung des Tasks in einer RAIL-Sitzung ausgelöst wird.


```XML
<Settings>
    <DisallowStartOnRemoteAppSession>true</DisallowStartOnRemoteAppSession>
</Settings>
        
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





