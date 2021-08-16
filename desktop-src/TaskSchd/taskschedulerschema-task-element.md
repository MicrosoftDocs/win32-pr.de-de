---
title: Task-Element
description: Definiert die Aufgabe, die vom Taskplaner Dienst ausgeführt wird.
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
ms.openlocfilehash: 3be36d0799e98b99a6d5ebe6430220b29fe2192935f67e9df5e189bc0f970a58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356233"
---
# <a name="task-element"></a>Task-Element

Definiert die Aufgabe, die vom Taskplaner Dienst ausgeführt wird.

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
| [**Aktionen**](taskschedulerschema-actions-tasktype-element.md)                   | [**actionsType**](taskschedulerschema-actionstype-complextype.md)                   | Gibt die aktionen an, die von der Aufgabe ausgeführt werden.<br/>                                                                             |
| [**Daten**](taskschedulerschema-data-tasktype-element.md)                         | [**Datatype**](taskschedulerschema-datatype-complextype.md)                         | Gibt Additionsdaten an, die dem Task zugeordnet sind, aber andernfalls vom Taskplaner Dienst nicht verwendet werden.<br/>         |
| [**Principals**](taskschedulerschema-principals-tasktype-element.md)             | [**principalsType**](taskschedulerschema-principalstype-complextype.md)             | Gibt die Sicherheitskontexte an, die zum Ausführen der Aufgabe verwendet werden können.<br/>                                                        |
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Gibt administrative Informationen über den Task an, z. B. den Ersteller der Aufgabe und das Datum, an dem der Task registriert ist.<br/> |
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md)                 | [**settingsType**](taskschedulerschema-settingstype-complextype.md)                 | Gibt die Einstellungen an, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/>                                                 |
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md)                 | [**triggersType**](taskschedulerschema-triggerstype-complextype.md)                 | Gibt die Trigger an, die den Task starten.<br/>                                                                              |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).

Informationen zur Skriptentwicklung finden Sie unter [**TaskDefinition**](taskdefinition.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





