---
title: Network Settings (settingstype)-Element
description: Enthält die Einstellungen, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden. Der Taskplaner Dienst prüft die Verfügbarkeit dieses Netzwerks, wenn das runonlyifnetworkavailable-Element auf "true" festgelegt ist.
ms.assetid: 7452b788-a170-4afe-abc5-ebcd3722da0d
keywords:
- Network settings-Element Taskplaner
topic_type:
- apiref
api_name:
- NetworkSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c7861d91cbc2647d241bc41753efbebcc346759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477463"
---
# <a name="networksettings-settingstype-element"></a>Network Settings (settingstype)-Element

Enthält die Einstellungen, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden. Der Taskplaner Dienst prüft die Verfügbarkeit dieses Netzwerks, wenn das [**runonlyifnetworkavailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) -Element auf " **true**" festgelegt ist.

``` syntax
<xs:element name="NetworkSettings"
    type="networkSettingsType"
    minOccurs="0"
 />
```

Das **networksettings** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                      | Abgeleitet von                                                         | BESCHREIBUNG                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Einstellungen (TaskType)**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Gibt die Einstellungen an, die vom Taskplaner zum Ausführen der Aufgabe verwendet werden.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**networksettings-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).

Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. networksettings**](tasksettings-networksettings.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





