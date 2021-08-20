---
title: Enabled(settingsType)-Element
description: Gibt an, dass der Task aktiviert ist. Die Aufgabe kann nur ausgeführt werden, wenn diese Einstellung true ist.
ms.assetid: d28f0d54-1205-4b70-a178-72d809da9ce1
keywords:
- Aktivierte Taskplaner
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff198520e354147ff092b2374bb5a766e1ce1c6db6a4b8fc6302b92670bddcda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131869"
---
# <a name="enabled-settingstype-element"></a>Enabled(settingsType)-Element

Gibt an, dass der Task aktiviert ist. Die Aufgabe kann nur ausgeführt werden, wenn diese Einstellung true ist.

``` syntax
<xs:element name="Enabled"
    type="boolean"
    default="true"
    minOccurs="1"
 />
```

Das **Enabled-Element** wird durch den komplexen [**settingsType-Typ**](taskschedulerschema-settingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | Beschreibung                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**Enabled-Eigenschaft von ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).

Informationen zur Skriptentwicklung finden Sie [**unter TaskSettings.Enabled**](tasksettings-enabled.md).

## <a name="examples"></a>Beispiele

Ein vollständiges Beispiel für den XML-Code für eine aktivierte Aufgabe finden Sie unter [Beispiel für Zeittrigger (XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





