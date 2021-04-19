---
title: Hidden (settingstype)-Element
description: Gibt an, dass die Aufgabe nicht standardmäßig in der Benutzeroberfläche angezeigt wird.
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
ms.openlocfilehash: ef5ad479fe3107ed8fa79f0f86307254a9f33c4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344722"
---
# <a name="hidden-settingstype-element"></a>Hidden (settingstype)-Element

Gibt an, dass die Aufgabe nicht standardmäßig in der Benutzeroberfläche angezeigt wird. Administratoren können diese Einstellung jedoch überschreiben, indem Sie einen "Master Switch" verwenden, der alle Aufgaben in der Benutzeroberfläche sichtbar macht.

``` syntax
<xs:element name="Hidden"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

Das **Hidden** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                    |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die Taskplaner verwendet, um den Task auszuführen.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**Hidden-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden).

Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. Hidden**](tasksettings-hidden.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





