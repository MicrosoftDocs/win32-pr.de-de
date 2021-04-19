---
title: Disallowstartonremoteappsession (settingstype)-Element
description: Gibt an, dass der Task nicht gestartet wird, wenn er für die Durchführung in einer lokal (Schiene) lokalen Anwendung ausgelöst wird.
ms.assetid: 8323d8d9-fb6a-4876-9967-cc2344c77de3
keywords:
- Disallowstartonremoteappsession-Element Taskplaner
topic_type:
- apiref
api_name:
- DisallowStartOnRemoteAppSession
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 11e3d0a367f2385e78cf1ec56231bbf7632fe05b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342416"
---
# <a name="disallowstartonremoteappsession-settingstype-element"></a>Disallowstartonremoteappsession (settingstype)-Element

Gibt an, dass der Task nicht gestartet wird, wenn er für die Durchführung in einer lokal (Schiene) lokalen Anwendung ausgelöst wird.

``` syntax
<xs:element name="DisallowStartOnRemoteAppSession"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

Das **disallowstartonremoteappsession** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Standardeinstellung für dieses Element ist false.

Bei der C++-Entwicklung erfolgt der Zugriff auf diese Informationen über die [**ITaskSettings2::D isallowstartonremoteappsession**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) -Eigenschaft.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein settings-Element, das nicht zulässt, dass der Task gestartet wird, wenn die Aufgabe für die Durchführung in einer Eisenbahn Sitzung ausgelöst wird.


```XML
<Settings>
    <DisallowStartOnRemoteAppSession>true</DisallowStartOnRemoteAppSession>
</Settings>
        
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





