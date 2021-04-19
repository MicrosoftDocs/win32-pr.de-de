---
title: Stopifgoingonakkus-Element (settingstype)
description: Gibt an, dass der Task angehalten wird, wenn der Computer auf die Batterie geht.
ms.assetid: 0d772dbb-a552-45ed-9dc0-7159f6ef12ed
keywords:
- Stopifgoingonakkus-Element Taskplaner
topic_type:
- apiref
api_name:
- StopIfGoingOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7de57cde928760c15dd671010880e824c8979f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340777"
---
# <a name="stopifgoingonbatteries-settingstype-element"></a>Stopifgoingonakkus-Element (settingstype)

Gibt an, dass der Task angehalten wird, wenn der Computer auf die Batterie geht.

``` syntax
<xs:element name="StopIfGoingOnBatteries"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

Das **stopifgoingonakkus** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Standardeinstellung für dieses Element ist false. Beachten Sie, dass sich der Standardwert gegenüber früheren Versionen von Taskplaner geändert hat.

Bei der Skripterstellung wird diese Einstellung mithilfe der [**Task Settings. stopifgoingonakkus**](tasksettings-stopifgoingonbatteries.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird diese Einstellung mithilfe der [**itasksettings:: stopifgoingonakkus**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein settings-Element, das eine harte Beendigung der Aufgabe ermöglicht.


```XML
<Settings>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
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

 

 





