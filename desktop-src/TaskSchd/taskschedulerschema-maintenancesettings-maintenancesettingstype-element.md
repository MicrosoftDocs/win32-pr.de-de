---
title: MaintenanceSettings(maintenanceSettingsType)-Element
description: Gibt an, wie die Taskplaner während der automatischen Wartung Aufgaben ausführt.
ms.assetid: 6A204980-851D-4487-A6CC-01BE262A517A
keywords:
- MaintenanceSettings-Element Taskplaner
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
# <a name="maintenancesettings-maintenancesettingstype-element"></a>MaintenanceSettings(maintenanceSettingsType)-Element

Gibt an, wie die Taskplaner während der automatischen Wartung Aufgaben ausführt.

``` syntax
<xs:element name="MaintenanceSettings"
    type="maintenanceSettingsType"
    minOccurs="0"
 />
```

Das **MaintenanceSettings-Element** wird vom komplexen [**MaintenanceSettingsType-Typ**](taskschedulerschema-maintenancesettingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | Beschreibung                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                    | type    | Beschreibung                                                                                                                                                                                     |
|------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Stichtag**](taskschedulerschema-deadline-element.md)   |         | Gibt die Zeitspanne an, nach der der Taskplaner versucht, den Task während der automatischen Notfallwartung zu starten, wenn er während der regulären Wartung nicht abgeschlossen werden konnte. <br/> |
| [**Exklusiv**](taskschedulerschema-exclusive-element.md) | boolean | Wenn diese Einstellung auf TRUE festgelegt ist, wird der Task ausschließlich mit anderen Wartungstasks gestartet. <br/>                                                                                                 |
| [**Zeitraum**](taskschedulerschema-period-element.md)       |         | Gibt an, wie oft der Task während der automatischen Wartung gestartet werden muss. <br/>                                                                                                      |



## <a name="remarks"></a>Hinweise

Für die C++-Programmierung wird diese Leerlaufeinstellung mithilfe der [**ITaskSettings3::MaintenanceSettings-Eigenschaft**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Einstellungselement, das Taskplaner anweist, den Task während der regulären automatischen Wartung innerhalb von fünf Tagen auszuführen. Wenn 15 Tage lang ein Fehler aufgetreten ist, starten Sie den Task während der automatischen Notfallwartung.


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

 

 





