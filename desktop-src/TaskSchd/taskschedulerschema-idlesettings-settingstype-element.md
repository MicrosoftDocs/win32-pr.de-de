---
title: IdleSettings(settingsType)-Element
description: Gibt an, wie der Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.
ms.assetid: 23d57417-95a9-42e3-904c-7f0859fcda7c
keywords:
- IdleSettings-Element Taskplaner
topic_type:
- apiref
api_name:
- IdleSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc0a4c3fc978c93d13be8faa62012d3928d47da5b5a214ce50f5506992f1fc8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991219"
---
# <a name="idlesettings-settingstype-element"></a>IdleSettings(settingsType)-Element

Gibt an, wie der Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet. Informationen zu Leerlaufbedingungen finden Sie unter [Leerlaufbedingungen für Aufgaben.](task-idle-conditions.md)

``` syntax
<xs:element name="IdleSettings"
    type="idleSettingsType"
    minOccurs="0"
 />
```

Das **IdleSettings-Element** wird durch den komplexen [**SettingsType-Typ**](taskschedulerschema-settingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element

| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |

## <a name="child-elements"></a>Untergeordnete Elemente

> [!NOTE]
> Die Einstellungen *Dauer* und *WaitTimeout* sind veraltet. Sie sind weiterhin in der Taskplaner Benutzeroberfläche vorhanden, und ihre Schnittstellenmethoden geben möglicherweise weiterhin gültige Werte zurück, werden jedoch nicht mehr verwendet.

| Element                                                                                  | type     | BESCHREIBUNG                                                                                                              |
|------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | boolean  | Gibt an, ob der Task neu gestartet wird, wenn der Computer mehr als einmal in eine Leerlaufbedingung eintritt.<br/>       |
| [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | boolean  | Gibt an, dass die Taskplaner die Aufgabe beendet, wenn die Leerlaufbedingung beendet wird, bevor der Task abgeschlossen wird.<br/> |
| **Veraltet:** [ **Dauer**](taskschedulerschema-duration-idlesettingstype-element.md)                | duration | Gibt an, wie lange sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird.<br/>                              |
| **Veraltet:** [ **WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)          | duration | Gibt die Zeitspanne an, die der Taskplaner auf das Auftreten einer Leerlaufbedingung wartet.<br/>                |

## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung werden Leerlaufeinstellungen mithilfe der [**TaskSettings.IdleSettings-Eigenschaft**](tasksettings-idlesettings.md) angegeben.

Für die C++-Entwicklung werden Leerlaufeinstellungen mithilfe der [**ITaskSettings::IdleSettings-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Einstellungselement, das es Taskplaner ermöglicht, 24 Stunden auf eine Leerlaufbedingung zu warten und dann nur 10 Minuten {IdleDuration) zu erlauben, um den Task zu initiieren.

```XML
<Settings>
    <IdleSettings>
        <StopOnIdleEnd>false</StopOnIdleEnd>
        <RestartOnIdle>false</RestartOnIdle> 
        <!-- WaitTimeout and Duration have been deprecated -->
        <Duration>PT5M</Duration>
        <WaitTimeout>PT24H</WaitTimeout>
    </IdleSettings>       
</Settings>
```

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |

## <a name="see-also"></a>Siehe auch

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)

[Aufgabenplanung](task-scheduler-start-page.md)
