---
title: Task-Element
description: Definiert den Task, der vom Taskplaner-Dienst ausgeführt wird.
ms.assetid: 103a332a-8620-4e0c-81b5-4782d85fc391
keywords:
- Task-Element Taskplaner
topic_type:
- apiref
api_name:
- Task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38bac482f8546028d21db913e31dc4152f19f599
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858736"
---
# <a name="task-element"></a>Task-Element

Definiert den Task, der vom Taskplaner-Dienst ausgeführt wird.

``` syntax
<xs:element name="Task"
    type="taskType"
>
    <xs:key name="PrincipalKey">
        <xs:selector
            xpath="td:Principals/td:Principal"
         />
        <xs:field
            xpath="@id"
         />
    </xs:key>
    <xs:keyref name="ContextKeyRef">
        <xs:selector
            xpath="td:Actions"
         />
        <xs:field
            xpath="@Context"
         />
    </xs:keyref>
    <xs:unique name="UniqueId">
        <xs:selector
            xpath="td:Principals/td:Principal|td:Triggers/td:BootTrigger|td:Triggers/td:RegistrationTrigger|td:Triggers/td:IdleTrigger|td:Triggers/td:TimeTrigger|td:Triggers/td:EventTrigger|td:Triggers/td:LogonTrigger|td:Triggers/td:SessionStateChangeTrigger|td:Triggers/td:CalendarTrigger|td:Actions/td:Exec|td:Actions/td:ComHandler|td:Actions/td:SendEmail"
         />
        <xs:field
            xpath="@id"
         />
    </xs:unique>
</xs:element>
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



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).

Informationen zur Skript Entwicklung finden Sie unter [**Task Definition**](taskdefinition.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





