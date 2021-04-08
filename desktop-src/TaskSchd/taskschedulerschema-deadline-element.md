---
title: Stichtag-Element
description: Gibt an, wann der Taskplaner den Task während der automatischen Notfallwartung starten muss, wenn er während der regulären automatischen Wartung nicht fertiggestellt werden konnte.
ms.assetid: 34E33FAE-888E-4E82-83B8-059FB4A64B52
keywords:
- Stichtag Element Taskplaner
topic_type:
- apiref
api_name:
- Deadline
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e12524971e8b713d4d17817a8a7c7602017bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740832"
---
# <a name="deadline-element"></a>Stichtag-Element

Gibt an, wann der Taskplaner den Task während der automatischen Notfallwartung starten muss, wenn er während der regulären automatischen Wartung nicht fertiggestellt werden konnte.

Das Format dieser Zeichenfolge ist " *pnynmndtnhnmns*", wobei " *NY* " die Anzahl von Jahren ist. "nm" ist die Anzahl von Monaten, " *ND* " die Anzahl von Tagen, " *T* " das Trennzeichen für Datum/Uhrzeit, " *NH* " die Anzahl von Stunden, " *nm* " die Anzahl der Minuten und " *NS* " die Anzahl von Sekunden (z. b. "PT5M" gibt 5 Minuten an und "P1M4DT2H5M" einen Monat, vier Tage, zwei Stunden und fünf Minuten) Der Mindestwert ist eine Minute. Weitere Informationen zum Duration-Typ finden Sie unter [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration). Der minimale Stichtag, den ein Task verwenden kann, ist 1 Tag. Der Wert des stichtelementes muss größer als der Wert des [**Period**](taskschedulerschema-period-element.md) **-Elements sein** . Wenn der Stichtag nicht angegeben wird, wird der Task während der automatischen Notfallwartung nicht gestartet.

``` syntax
<xs:element name="Deadline"
    maxOccurs="1"
    minOccurs="0"
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

Das **Stichtag** -Element wird durch den komplexen Typ [**maintenancesettingstype**](taskschedulerschema-maintenancesettingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                                          | Abgeleitet von                                                                               | BESCHREIBUNG                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**Maintenancesettings (maintenancesettingstype)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenancesettingstype**](taskschedulerschema-maintenancesettingstype-complextype.md) | Gibt die Task Einstellungen an, mit denen der Taskplaner während der automatischen Wartung gestartet wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der C++-Programmierung wird diese Einstellung für den Leerlauf mithilfe der [**imaintenancesettings::D eadline**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Im folgenden XML-Code wird ein Monatskalender definiert, in dem die Aufgabe im März ausgeführt wird.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
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

 

 





