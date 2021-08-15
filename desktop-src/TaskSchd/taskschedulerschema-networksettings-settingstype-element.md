---
title: NetworkSettings -Element (settingsType)
description: Enthält die Einstellungen, die der Taskplaner verwendet, um ein Netzwerkprofil zu erhalten. Der Taskplaner überprüft die Verfügbarkeit dieses Netzwerks, wenn das RunOnlyIfNetworkAvailable-Element auf True festgelegt ist.
ms.assetid: 7452b788-a170-4afe-abc5-ebcd3722da0d
keywords:
- NetworkSettings-Taskplaner
topic_type:
- apiref
api_name:
- NetworkSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b81e1ff2a9f03646d124f5fd2d3aae27f18069f4b32631f9f8d9e66a193ac3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758480"
---
# <a name="networksettings-settingstype-element"></a>NetworkSettings -Element (settingsType)

Enthält die Einstellungen, die der Taskplaner verwendet, um ein Netzwerkprofil zu erhalten. Der Taskplaner überprüft die Verfügbarkeit dieses Netzwerks, wenn das [**RunOnlyIfNetworkAvailable-Element**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) auf **True festgelegt ist.**

``` syntax
<xs:element name="NetworkSettings"
    type="networkSettingsType"
    minOccurs="0"
 />
```

Das **NetworkSettings-Element** wird durch den komplexen [**settingsType-Typ**](taskschedulerschema-settingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                      | Abgeleitet von                                                         | BESCHREIBUNG                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Einstellungen (taskType)**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Gibt die Einstellungen an, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**NetworkSettings-Eigenschaft von ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).

Informationen zur Skriptentwicklung finden Sie [**unter TaskSettings.NetworkSettings**](tasksettings-networksettings.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





