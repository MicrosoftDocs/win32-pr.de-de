---
title: Disallowstartifonakkus (settingstype)-Element
description: Gibt an, dass der Task nicht gestartet wird, wenn der Computer unter "Akkus" ausgeführt wird.
ms.assetid: 48c0fd32-4441-4628-8090-c736f2945b4d
keywords:
- Disallowstartifonakkus-Element Taskplaner
topic_type:
- apiref
api_name:
- DisallowStartIfOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a8d93bcabd0e121c44f4a7212d11491624a08d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743776"
---
# <a name="disallowstartifonbatteries-settingstype-element"></a>Disallowstartifonakkus (settingstype)-Element

Gibt an, dass der Task nicht gestartet wird, wenn der Computer unter "Akkus" ausgeführt wird.

``` syntax
<xs:element name="DisallowStartIfOnBatteries"
    type="boolean"
 />
```

Das **disallowstartifonakkus** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Standardeinstellung für dieses Element ist "true".

Bei der Skripterstellung erfolgt der Zugriff auf diese Informationen über die [**tasksettings. disallowstartifonakkus**](tasksettings-disallowstartifonbatteries.md) -Eigenschaft.

Bei der C++-Entwicklung erfolgt der Zugriff auf diese Informationen über die Eigenschaft [**itasksettings::D isallowstartifonakkus**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) .

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein settings-Element, das nicht zulässt, dass der Task ausgeführt wird, wenn der Computer unter Akkus ausgeführt wird.


```XML
<Settings>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
</Settings>
        
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





