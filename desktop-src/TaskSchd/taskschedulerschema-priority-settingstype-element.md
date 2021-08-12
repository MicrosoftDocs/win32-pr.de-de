---
title: Priority (settingsType)-Element
description: Gibt die Prioritätsebene für den Task an.
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
ms.openlocfilehash: 11b71c88f63e7a3beb3c1c9ec8e1f3253bcd05a567ec5cd077f62175561ce2c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611892"
---
# <a name="priority-settingstype-element"></a>Priority (settingsType)-Element

Gibt die Prioritätsebene für den Task an.

``` syntax
<xs:element name="Priority"
    type="priorityType"
    default="7"
    minOccurs="0"
 />
```

Das **Priority-Element** wird durch den komplexen [**SettingsType-Typ**](taskschedulerschema-settingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | Beschreibung                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="remarks"></a>Hinweise

Prioritätsstufe 0 ist die höchste Priorität, und Prioritätsstufe 10 ist die niedrigste Priorität. Der Standardwert ist 7. Die Mindest- und Höchstwerte werden durch den einfachen [**PriorityType-Typ**](taskschedulerschema-prioritytype-simpletype.md) festgelegt. Die Prioritätsstufen 7 und 8 werden für Hintergrundaufgaben und die Prioritätsstufen 4, 5 und 6 für interaktive Aufgaben verwendet.

Die Aktion der Aufgabe wird in einem Prozess mit einer Priorität gestartet, die auf einem Priority Class-Wert basiert. Ein Wert auf Prioritätsebene (Threadpriorität) wird für COM-Handler, Meldungsfeld und E-Mail-Aufgabenaktionen verwendet. Weitere Informationen zu den Prioritätsklassen- und Prioritätsebenenwerten finden Sie unter [Zeitplanungsprioritäten.](/windows/desktop/ProcThread/scheduling-priorities) In der folgenden Tabelle sind die möglichen Werte für das **Priority-Element** und die entsprechenden Priority Class- und Priority Level-Werte aufgeführt.



| Aufgabenpriorität | Priority-Klasse                 | Prioritätsstufe                   |
|---------------|--------------------------------|----------------------------------|
| 0             | REALTIME \_ PRIORITY \_ CLASS      | \_ZEITKRITISCH FÜR THREADPRIORITÄT \_ \_ |
| 1             | KLASSE MIT HOHER \_ PRIORITÄT \_          | \_HÖCHSTE \_ THREADPRIORITÄT        |
| 2             | OBERHALB \_ DER NORMALEN \_ \_ PRIORITÄTSKLASSE | \_ \_ THREADPRIORITÄT ÜBER \_ NORMAL  |
| 3             | OBERHALB \_ DER NORMALEN \_ \_ PRIORITÄTSKLASSE | \_ \_ THREADPRIORITÄT ÜBER \_ NORMAL  |
| 4             | NORMAL \_ \_ PRIORITY-KLASSE        | \_THREADPRIORITÄT \_ NORMAL         |
| 5             | NORMAL \_ \_ PRIORITY-KLASSE        | \_THREADPRIORITÄT \_ NORMAL         |
| 6             | NORMAL \_ \_ PRIORITY-KLASSE        | \_THREADPRIORITÄT \_ NORMAL         |
| 7             | BELOW \_ NORMAL \_ PRIORITY \_ CLASS | \_THREADPRIORITÄT \_ UNTER \_ NORMAL  |
| 8             | BELOW \_ NORMAL \_ PRIORITY \_ CLASS | \_THREADPRIORITÄT \_ UNTER \_ NORMAL  |
| 9             | IDLE \_ \_ PRIORITY-KLASSE          | \_ \_ THREADPRIORITÄT NIEDRIGSTE         |
| 10            | IDLE \_ \_ PRIORITY-KLASSE          | \_ \_ THREADPRIORITÄT IM LEERLAUF           |



 

Informationen zur C++-Entwicklung finden Sie unter [**Priority Property of ITaskSettings (Prioritätseigenschaft von ITaskSettings).**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority)

Informationen zur Skriptentwicklung finden Sie unter [**TaskSettings.Priority**](tasksettings-priority.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

