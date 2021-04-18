---
title: Exklusives Element
description: Gibt an, ob der Taskplaner die Aufgabe während der automatischen Wartung im exklusiven Modus starten muss.
ms.assetid: F690FD8F-BCCB-456D-92E3-25A262D6DCF1
keywords:
- Exklusives Element Taskplaner
topic_type:
- apiref
api_name:
- Exclusive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e0cd7cf5b2a5ce3aa68f92834aa45563000945d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339941"
---
# <a name="exclusive-element"></a>Exklusives Element

Gibt an, ob der Taskplaner die Aufgabe während der automatischen Wartung im exklusiven Modus starten muss.

Die Exklusivität wird nur zwischen anderen Wartungs Tasks garantiert und erteilt keine Reihenfolge Priorität der Aufgabe. Wenn die Exklusivität nicht angegeben wird, wird die Aufgabe parallel mit anderen Wartungs Tasks gestartet.

``` syntax
<xs:element name="Exclusive"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
 />
```

Das **exklusive** Element wird durch den komplexen Typ [**maintenancesettingstype**](taskschedulerschema-maintenancesettingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                                          | Abgeleitet von                                                                               | BESCHREIBUNG                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**Maintenancesettings (maintenancesettingstype)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenancesettingstype**](taskschedulerschema-maintenancesettingstype-complextype.md) | Gibt die Task Einstellungen an, mit denen der Taskplaner während der automatischen Wartung gestartet wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der C++-Programmierung wird diese Einstellung für den Leerlauf mithilfe der [**imaintenancesettings:: Exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert den Wartungs Task mit der Stichtag Anforderung auf 15 Tage.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





