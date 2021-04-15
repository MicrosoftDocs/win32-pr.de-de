---
title: komplexer TaskType-Typ (Taskplaner)
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das Task-Element.
ms.assetid: 622b2bf4-c7e0-403c-bd6c-99b687c1d439
keywords:
- komplexer TaskType-Typ Taskplaner
topic_type:
- apiref
api_name:
- taskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e86174920c28614f6c871e3f0bb0bc322243009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477775"
---
# <a name="tasktype-complex-type"></a>komplexer TaskType-Typ

Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**Task**](taskschedulerschema-task-element.md) -Element.

``` syntax
<xs:complexType name="taskType">
    <xs:all>
        <xs:element name="RegistrationInfo"
            type="registrationInfoType"
            minOccurs="0"
         />
        <xs:element name="Triggers"
            type="triggersType"
            minOccurs="0"
         />
        <xs:element name="Settings"
            type="settingsType"
            minOccurs="0"
         />
        <xs:element name="Data"
            type="dataType"
            minOccurs="0"
         />
        <xs:element name="Principals"
            type="principalsType"
            minOccurs="0"
         />
        <xs:element name="Actions"
            type="actionsType"
         />
    </xs:all>
    <xs:attribute name="version"
        type="versionType"
        use="optional"
        fixed="1.3"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                           | type                                                                                 | BESCHREIBUNG                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktionen**](taskschedulerschema-actions-tasktype-element.md)                   | [**Aktions sType**](taskschedulerschema-actionstype-complextype.md)                   | Gibt die Aktionen an, die vom Task ausgeführt werden.<br/>                                                                             |
| [**Daten**](taskschedulerschema-data-tasktype-element.md)                         | [**Datentyp**](taskschedulerschema-datatype-complextype.md)                         | Gibt zusätzliche Daten an, die dem Task zugeordnet sind, wird aber vom Taskplaner-Dienst anderweitig nicht verwendet.<br/>         |
| [**Principals**](taskschedulerschema-principals-tasktype-element.md)             | [**principalstype**](taskschedulerschema-principalstype-complextype.md)             | Gibt die Sicherheits Kontexte an, die verwendet werden können, um den Task auszuführen.<br/>                                                        |
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) | Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.<br/> |
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md)                 | [**settingstype**](taskschedulerschema-settingstype-complextype.md)                 | Gibt die Einstellungen an, die vom Taskplaner zum Ausführen der Aufgabe verwendet werden.<br/>                                                 |
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md)                 | [**triggerstype**](taskschedulerschema-triggerstype-complextype.md)                 | Gibt die Trigger an, die den Task starten.<br/>                                                                              |



## <a name="attributes"></a>Attributes



| Name    | type                                                              | BESCHREIBUNG                                   |
|---------|-------------------------------------------------------------------|-----------------------------------------------|
| version | [**versiontype**](taskschedulerschema-versiontype-simpletype.md) | Gibt die Version der Aufgabe an.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Komplexe Typen von Taskplaner Schemas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





