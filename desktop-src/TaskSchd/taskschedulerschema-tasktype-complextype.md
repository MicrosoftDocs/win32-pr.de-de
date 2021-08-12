---
title: taskType Complex Type (Taskplaner)
description: Definiert die untergeordneten Elemente und Sequenzierungsinformationen für das Task-Element.
ms.assetid: 622b2bf4-c7e0-403c-bd6c-99b687c1d439
keywords:
- komplexer taskType-Taskplaner
topic_type:
- apiref
api_name:
- taskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e2465773fb784c87fe560bdc8f6306771578cb22cf9aa26bf79b84867deb61b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611057"
---
# <a name="tasktype-complex-type"></a>komplexer taskType-Typ

Definiert die untergeordneten Elemente und Sequenzierungsinformationen für das [**Task-Element.**](taskschedulerschema-task-element.md)

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



| Element                                                                           | type                                                                                 | Beschreibung                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktionen**](taskschedulerschema-actions-tasktype-element.md)                   | [**actionsType**](taskschedulerschema-actionstype-complextype.md)                   | Gibt die aktionen an, die von der Aufgabe ausgeführt werden.<br/>                                                                             |
| [**Daten**](taskschedulerschema-data-tasktype-element.md)                         | [**Datatype**](taskschedulerschema-datatype-complextype.md)                         | Gibt Additionsdaten an, die der Aufgabe zugeordnet sind, aber andernfalls vom Taskplaner werden.<br/>         |
| [**Principals**](taskschedulerschema-principals-tasktype-element.md)             | [**principalsType**](taskschedulerschema-principalstype-complextype.md)             | Gibt die Sicherheitskontexte an, die zum Ausführen der Aufgabe verwendet werden können.<br/>                                                        |
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Gibt Administratorinformationen zum Task an, z. B. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert wird.<br/> |
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md)                 | [**settingsType**](taskschedulerschema-settingstype-complextype.md)                 | Gibt die Einstellungen an, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/>                                                 |
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md)                 | [**triggersType**](taskschedulerschema-triggerstype-complextype.md)                 | Gibt die Trigger an, die die Aufgabe starten.<br/>                                                                              |



## <a name="attributes"></a>Attributes



| Name    | type                                                              | BESCHREIBUNG                                   |
|---------|-------------------------------------------------------------------|-----------------------------------------------|
| version | [**versionType**](taskschedulerschema-versiontype-simpletype.md) | Gibt die Version der Aufgabe an.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Komplexe Schematypen](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





