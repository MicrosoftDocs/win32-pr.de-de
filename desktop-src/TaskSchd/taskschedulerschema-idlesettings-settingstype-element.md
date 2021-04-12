---
title: Idlesettings (settingstype)-Element
description: Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.
ms.assetid: 23d57417-95a9-42e3-904c-7f0859fcda7c
keywords:
- Idlesettings-Element Taskplaner
topic_type:
- apiref
api_name:
- IdleSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ae8b7953f31d7e9c6f01387d3136f01d8ab697a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105219"
---
# <a name="idlesettings-settingstype-element"></a>Idlesettings (settingstype)-Element

Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet. Informationen zu Bedingungen im Leerlauf finden Sie unter [Aufgaben im Leerlauf](task-idle-conditions.md).

``` syntax
<xs:element name="IdleSettings"
    type="idleSettingsType"
    minOccurs="0"
 />
```

Das **idlesettings** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element

| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.<br/> |

## <a name="child-elements"></a>Untergeordnete Elemente

> [!NOTE]
> Die Einstellungen für *Dauer* und *WaitTimeout* sind veraltet. Sie sind weiterhin in der Taskplaner-Benutzeroberfläche vorhanden, und ihre Schnittstellen Methoden geben möglicherweise weiterhin gültige Werte zurück, aber Sie werden nicht mehr verwendet.

| Element                                                                                  | type     | BESCHREIBUNG                                                                                                              |
|------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [**Neustartondle**](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | boolean  | Gibt an, ob der Task neu gestartet wird, wenn der Computer mehrmals in eine Leerlauf Bedingung wechselt.<br/>       |
| [**Stoponidleend**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | boolean  | Gibt an, dass der Taskplaner den Task beendet, wenn die Leerlauf Bedingung vor dem Abschluss der Aufgabe endet.<br/> |
| **Veraltet**: [ **Dauer**](taskschedulerschema-duration-idlesettingstype-element.md)                | duration | Gibt an, wie lange sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird.<br/>                              |
| **Veraltet**: [ **WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)          | duration | Gibt die Zeitspanne an, die der Taskplaner auf das Eintreten einer Leerlauf Bedingung wartet.<br/>                |

## <a name="remarks"></a>Bemerkungen

Bei der Skript Entwicklung werden im Leerlauf Einstellungen mithilfe der [**tasksettings. idlesettings**](tasksettings-idlesettings.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung werden Leerlauf Einstellungen mithilfe der [**itasksettings:: idlesettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein settings-Element, das es Taskplaner ermöglicht, 24 Stunden auf eine Leerlauf Bedingung zu warten, und dann nur 10 Minuten {idleduration) zum Initiieren der Aufgabe zulässt.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |

## <a name="see-also"></a>Siehe auch

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)

[Aufgabenplanung](task-scheduler-start-page.md)
