---
title: Runonlyifdle (settingstype)-Element
description: Gibt an, dass der Task nur ausgeführt wird, wenn sich der Computer im Leerlauf befindet.
ms.assetid: 2ef3dd19-4d5c-4399-89b8-d737be4ef85e
keywords:
- Runonlyimedle-Element Taskplaner
topic_type:
- apiref
api_name:
- RunOnlyIfIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c57663d763926d68e5a552ebaf66edff2172e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040869"
---
# <a name="runonlyifidle-settingstype-element"></a>Runonlyifdle (settingstype)-Element

Gibt an, dass der Task nur ausgeführt wird, wenn sich der Computer im Leerlauf befindet.

``` syntax
<xs:element name="RunOnlyIfIdle"
    type="boolean"
 />
```

Das **runonlyimedle** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**runonlyimedle-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle).

Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. runonlyifdle**](tasksettings-runonlyifidle.md).

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

 

 





