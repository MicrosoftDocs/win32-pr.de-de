---
title: Maintenancesettings-Element (maintenancesettingstype)
description: Gibt an, wie das Taskplaner während der automatischen Wartung Tasks ausführt.
ms.assetid: 6A204980-851D-4487-A6CC-01BE262A517A
keywords:
- Maintenancesettings-Element Taskplaner
topic_type:
- apiref
api_name:
- MaintenanceSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca68876d8742ea04faa972d2ea7fd5f4b2071ffc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105218"
---
# <a name="maintenancesettings-maintenancesettingstype-element"></a>Maintenancesettings-Element (maintenancesettingstype)

Gibt an, wie das Taskplaner während der automatischen Wartung Tasks ausführt.

``` syntax
<xs:element name="MaintenanceSettings"
    type="maintenanceSettingsType"
    minOccurs="0"
 />
```

Das **maintenancesettings** -Element wird durch den komplexen Typ [**maintenancesettingstype**](taskschedulerschema-maintenancesettingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                    | type    | BESCHREIBUNG                                                                                                                                                                                     |
|------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Stichtag**](taskschedulerschema-deadline-element.md)   |         | Gibt die Zeitspanne an, nach der der Taskplaner versucht, die Aufgabe während der automatischen Notfallwartung zu starten, wenn dieser während der regulären Wartung nicht fertiggestellt werden konnte. <br/> |
| [**Exklusiv**](taskschedulerschema-exclusive-element.md) | boolean | Wenn diese Einstellung auf "true" festgelegt ist, wird die Aufgabe ausschließlich unter anderen Wartungs Tasks gestartet. <br/>                                                                                                 |
| [**Zeitraum**](taskschedulerschema-period-element.md)       |         | Gibt an, wie oft der Task während der automatischen Wartung gestartet werden muss. <br/>                                                                                                      |



## <a name="remarks"></a>Bemerkungen

Bei der C++-Programmierung wird diese Einstellung für den Leerlauf mithilfe der [**ITaskSettings3:: maintenancesettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Einstellungs Element, das Taskplaner anweist, die Aufgabe einmal in 5 Tagen während der regulären automatischen Wartung auszuführen. wenn 15 Tage lang ein Fehler aufgetreten ist, sollte der Task während der automatischen Notfallwartung gestartet werden.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





