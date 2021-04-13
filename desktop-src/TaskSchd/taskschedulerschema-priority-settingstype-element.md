---
title: Priority (settingstype)-Element
description: Gibt die Prioritätsstufe für den Task an.
ms.assetid: 4885fffa-b7d9-4f5e-b6e8-6f18b01c2427
keywords:
- Priority-Element Taskplaner
topic_type:
- apiref
api_name:
- Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ecda59ecbbe23550363fb30706d73bca54fcd925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391632"
---
# <a name="priority-settingstype-element"></a>Priority (settingstype)-Element

Gibt die Prioritätsstufe für den Task an.

``` syntax
<xs:element name="Priority"
    type="priorityType"
    default="7"
    minOccurs="0"
 />
```

Das **Priority** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.<br/> |



## <a name="remarks"></a>Bemerkungen

Prioritätsstufe 0 ist die höchste Priorität, und Prioritätsstufe 10 ist die niedrigste Priorität. Der Standardwert ist 7. Der minimale und der maximale Wert werden vom einfachen [**prioritytype**](taskschedulerschema-prioritytype-simpletype.md) -Typ festgelegt. Die Prioritätsstufen 7 und 8 werden für Hintergrundaufgaben verwendet, und die Prioritätsstufen 4, 5 und 6 werden für interaktive Aufgaben verwendet.

Die Aktion der Aufgabe wird in einem Prozess mit einer Priorität gestartet, die auf einem Prioritäts Klassen Wert basiert. Ein Wert für die Prioritätsstufe (Thread Priorität) wird für com-Handler-, Meldungs-und e-Mail-Aufgaben Aktionen verwendet. Weitere Informationen zu den Werten für die Prioritäts Klasse und Prioritätsstufen finden Sie unter [Planungs Prioritäten](/windows/desktop/ProcThread/scheduling-priorities). In der folgenden Tabelle sind die möglichen Werte für das **Prioritäts** Element sowie die entsprechenden Werte für die Prioritäts Klasse und die Prioritäts Ebene aufgeführt.



| Aufgaben Priorität | Prioritäts Klasse                 | Prioritätsstufe                   |
|---------------|--------------------------------|----------------------------------|
| 0             | Realtime \_ priority- \_ Klasse      | Thread \_ Prioritäts \_ Zeit \_ kritisch |
| 1             | Klasse mit hoher \_ Priorität \_          | Thread \_ Priorität \_ höchste        |
| 2             | oberhalb der \_ normalen \_ Prioritäts \_ Klasse | Thread \_ Priorität \_ oberhalb des \_ normalen  |
| 3             | oberhalb der \_ normalen \_ Prioritäts \_ Klasse | Thread \_ Priorität \_ oberhalb des \_ normalen  |
| 4             | Klasse der normalen \_ Priorität \_        | Thread \_ Priorität \_ Normal         |
| 5             | Klasse der normalen \_ Priorität \_        | Thread \_ Priorität \_ Normal         |
| 6             | Klasse der normalen \_ Priorität \_        | Thread \_ Priorität \_ Normal         |
| 7             | unterhalb der \_ normalen \_ Prioritäts \_ Klasse | Thread \_ Priorität \_ unterhalb von \_ Normal  |
| 8             | unterhalb der \_ normalen \_ Prioritäts \_ Klasse | Thread \_ Priorität \_ unterhalb von \_ Normal  |
| 9             | inaktive \_ Prioritäts \_ Klasse          | Thread \_ Priorität \_ niedrigste         |
| 10            | inaktive \_ Prioritäts \_ Klasse          | Thread \_ Priorität im \_ Leerlauf           |



 

Informationen zur C++-Entwicklung finden Sie unter [**Priority-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).

Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. Priority**](tasksettings-priority.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

