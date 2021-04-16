---
title: Period-Element
description: Gibt an, wie oft der Task während der automatischen Wartung gestartet werden muss.
ms.assetid: E4BE2466-3119-41F8-8238-4627C28B26E5
keywords:
- Period-Element Taskplaner
topic_type:
- apiref
api_name:
- Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a507a9b0a8f97d1ae4e6c8df654a45d67b77767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479230"
---
# <a name="period-element"></a>Period-Element

Gibt an, wie oft der Task während der automatischen Wartung gestartet werden muss.

Das Format dieser Zeichenfolge ist " *pnynmndtnhnmns*", wobei " *NY* " die Anzahl von Jahren ist. "nm" ist die Anzahl von Monaten, " *ND* " die Anzahl von Tagen, " *T* " das Trennzeichen für Datum/Uhrzeit, " *NH* " die Anzahl von Stunden, " *nm* " die Anzahl der Minuten und " *NS* " die Anzahl von Sekunden (z. b. "PT5M" gibt 5 Minuten an und "P1M4DT2H5M" einen Monat, vier Tage, zwei Stunden und fünf Minuten) Der Mindestwert ist eine Minute. Weitere Informationen zum Duration-Typ finden Sie unter [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).

``` syntax
<xs:element name="Period"
    maxOccurs="1"
    minOccurs="1"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="P1D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das **Period** -Element wird durch den komplexen Typ [**maintenancesettingstype**](taskschedulerschema-maintenancesettingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                                          | Abgeleitet von                                                                               | BESCHREIBUNG                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**Maintenancesettings (maintenancesettingstype)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenancesettingstype**](taskschedulerschema-maintenancesettingstype-complextype.md) | Gibt die Task Einstellungen an, mit denen der Taskplaner während der automatischen Wartung gestartet wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der C++-Programmierung wird diese Einstellung für den Leerlauf mithilfe der [**imaintenancesettings::P eriod**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen Wartungs Task, bei dem periodizitäts Anforderungen auf 5 Tage festgelegt sind.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
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

 

 





