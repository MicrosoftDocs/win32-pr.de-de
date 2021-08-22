---
title: AllowStartOnDemand (settingsType)-Element
description: Gibt an, dass die Aufgabe mit dem Befehl Ausführen oder dem Kontextmenü gestartet werden kann.
ms.assetid: 5a0f0842-9f09-4d52-bed2-45740945d9a5
keywords:
- AllowStartOnDemand-Taskplaner
topic_type:
- apiref
api_name:
- AllowStartOnDemand
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be89197c4ae88188fc1d2a746c40d69e385edc7ba08aaf2d3bf29067ee5f4a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516990"
---
# <a name="allowstartondemand-settingstype-element"></a>AllowStartOnDemand (settingsType)-Element

Gibt an, dass die Aufgabe mit dem Befehl Ausführen oder dem Kontextmenü gestartet werden kann.

``` syntax
<xs:element name="AllowStartOnDemand"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

Das **AllowStartOnDemand-Element** wird durch den komplexen [**settingsType-Typ**](taskschedulerschema-settingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | Beschreibung                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="remarks"></a>Hinweise

Wenn dieses Element auf True festgelegt ist, kann die Aufgabe unabhängig davon gestartet werden, wenn ein Trigger die Aufgabe startet.

Informationen zur C++-Entwicklung finden Sie unter [**der AllowDemandStart-Eigenschaft von ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).

Informationen zur Skriptentwicklung finden Sie [**unter TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md).

## <a name="examples"></a>Beispiele

Ein vollständiges Beispiel für den XML-Code für eine Aufgabe, die den Bedarfsstart zulässt, finden Sie unter [Time Trigger Example (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





