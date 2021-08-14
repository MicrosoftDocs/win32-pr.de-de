---
title: MaintenanceSettings-Element (maintenanceSettingsType)
description: Gibt an, wie die Taskplaner während der automatischen Wartung Aufgaben ausführt.
ms.assetid: 6A204980-851D-4487-A6CC-01BE262A517A
keywords:
- MaintenanceSettings-Taskplaner
topic_type:
- apiref
api_name:
- MaintenanceSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5724a5dff942377af783970e5d011e8f8a1ce9123039112917a3f652372495d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309340"
---
# <a name="maintenancesettings-maintenancesettingstype-element"></a>MaintenanceSettings-Element (maintenanceSettingsType)

Gibt an, wie die Taskplaner während der automatischen Wartung Aufgaben ausführt.

``` syntax
<xs:element name="MaintenanceSettings"
    type="maintenanceSettingsType"
    minOccurs="0"
 />
```

Das **MaintenanceSettings-Element** wird durch den komplexen [**MaintenanceSettingsType-Typ**](taskschedulerschema-maintenancesettingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                    | type    | BESCHREIBUNG                                                                                                                                                                                     |
|------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Stichtag**](taskschedulerschema-deadline-element.md)   |         | Gibt die Zeit an, nach der der Taskplaner versucht, den Task während der automatischen Notfallwartung zu starten, wenn er während der regulären Wartung nicht abgeschlossen werden konnte. <br/> |
| [**Exklusiv**](taskschedulerschema-exclusive-element.md) | boolean | Wenn auf TRUE festgelegt, wird der Task ausschließlich unter anderen Wartungsaufgaben gestartet. <br/>                                                                                                 |
| [**Zeitraum**](taskschedulerschema-period-element.md)       |         | Gibt an, wie oft der Task während der automatischen Wartung gestartet werden muss. <br/>                                                                                                      |



## <a name="remarks"></a>Hinweise

Für die C++-Programmierung wird diese Leerlaufeinstellung mithilfe der [**ITaskSettings3::MaintenanceSettings-Eigenschaft**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Einstellungselement, das Taskplaner anweisen soll, den Task während der regelmäßigen automatischen Wartung einmal in 5 Tagen auszuführen, und bei einem Fehler von 15 Tagen den Task während der automatischen Notfallwartung zu starten.


```XML
<Settings>
    <MaintenanceSettings>
        <Period>P5D</Period>
        <Deadline>P15D</Deadline>
    </MaintenanceSettings>       
</Settings>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>           |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





