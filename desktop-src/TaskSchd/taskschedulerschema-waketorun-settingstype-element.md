---
title: Waketor (settingstype)-Element
description: Gibt an, dass der Computer von Taskplaner reaktiviert wird, wenn der Task ausgeführt werden soll.
ms.assetid: 5fb53016-5778-463d-bb32-3c1da2de6fc2
keywords:
- Waketor-Element Taskplaner
topic_type:
- apiref
api_name:
- WakeToRun
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23eeaa06073fa9259c1a48137cf3676baa402d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341029"
---
# <a name="waketorun-settingstype-element"></a>Waketor (settingstype)-Element

Gibt an, dass der Computer von Taskplaner reaktiviert wird, wenn der Task ausgeführt werden soll.

``` syntax
<xs:element name="WakeToRun"
    type="boolean"
 />
```

Das **waketor-** Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.<br/> |



## <a name="remarks"></a>Bemerkungen

Wenn der Taskplaner-Dienst den Computer zum Ausführen einer Aufgabe aktiviert, bleibt der Bildschirm möglicherweise deaktiviert, auch wenn sich der Computer nicht mehr im Standbymodus oder Ruhezustand befindet. Der Bildschirm wird eingeschaltet, wenn Windows Vista erkennt, dass ein Benutzer die Verwendung des Computers zurückgegeben hat.

Informationen zur C++-Entwicklung finden Sie unter [**der Eigenschaft "waketor" von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).

Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. wakescripun**](tasksettings-waketorun.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





