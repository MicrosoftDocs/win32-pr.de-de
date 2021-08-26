---
title: Exclusive-Element
description: Gibt an, ob der Taskplaner den Task während der automatischen Wartung im exklusiven Modus starten muss.
ms.assetid: F690FD8F-BCCB-456D-92E3-25A262D6DCF1
keywords:
- Exklusive Taskplaner
topic_type:
- apiref
api_name:
- Exclusive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aab796abfdcad67a348b6d42186732d402bbe8eeeb359ac772588fe809dbf73c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991330"
---
# <a name="exclusive-element"></a>Exclusive-Element

Gibt an, ob der Taskplaner den Task während der automatischen Wartung im exklusiven Modus starten muss.

Die Reihenfolge wird nur zwischen anderen Wartungsaufgaben garantiert und gewährt keine Reihenfolgenpriorität der Aufgabe. Wenn keine Intervalle angegeben werden, wird der Task parallel zu anderen Wartungsaufgaben gestartet.

``` syntax
<xs:element name="Exclusive"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
 />
```

Das **Exclusive-Element** wird durch den komplexen [**MaintenanceSettingsType-Typ**](taskschedulerschema-maintenancesettingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                                          | Abgeleitet von                                                                               | Beschreibung                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Gibt die Aufgabeneinstellungen an, die der Taskplaner verwendet, um den Task während der automatischen Wartung zu starten.<br/> |



## <a name="remarks"></a>Hinweise

Bei der C++-Programmierung wird diese Leerlaufeinstellung mithilfe der [**IMaintenanceSettings::Exclusive-Eigenschaft**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert den Wartungs task, für den die Stichtaganforderung auf 15 Tage festgelegt ist.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
    <Exclusive>true</Exclusive>
</MaintenanceSettings>
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

 

 





