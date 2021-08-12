---
title: UseUnifiedSchedulingEngine (settingsType)-Element
description: Gibt an, dass die einheitliche Zeitplanungs-Engine zum Ausführen dieser Aufgabe verwendet wird.
ms.assetid: 93436f14-1caf-4ec8-bf74-a198b7dcb27c
keywords:
- UseUnifiedSchedulingEngine-Taskplaner
topic_type:
- apiref
api_name:
- UseUnifiedSchedulingEngine
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: faf27ea132fb47e35cd248e183fbec0584cb5d44414d6cacda6baac0d595c32d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610453"
---
# <a name="useunifiedschedulingengine-settingstype-element"></a>UseUnifiedSchedulingEngine (settingsType)-Element

Gibt an, dass die einheitliche Zeitplanungs-Engine zum Ausführen dieser Aufgabe verwendet wird.

``` syntax
<xs:element name="UseUnifiedSchedulingEngine"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

Das **UseUnifiedSchedulingEngine-Element** wird durch den komplexen [**settingsType-Typ**](taskschedulerschema-settingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | Beschreibung                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="remarks"></a>Hinweise

Die Standardeinstellung für dieses Element ist False.

Bei der C++-Entwicklung erfolgt der Zugriff auf diese Informationen über die [**ITaskSettings2::UseUnifiedSchedulingEngine-Eigenschaft.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine)

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Einstellungselement, das angibt, dass die einheitliche Zeitplanungs-Engine zum Ausführen dieser Aufgabe verwendet wird.


```XML
<Settings>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
</Settings>
        
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





