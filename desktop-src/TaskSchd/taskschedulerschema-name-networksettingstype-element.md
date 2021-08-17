---
title: Name-Element (networkSettingsType)
description: Enthält den Namen eines Netzwerkprofils. Der Name wird zu Anzeigezwecken verwendet.
ms.assetid: 86e4e68d-3c36-41eb-8563-d7d5125a5957
keywords:
- Name-Element Taskplaner
topic_type:
- apiref
api_name:
- Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41b92c7e63a820c2a2a34378b041bec3a49f432b52887a732c3f3bfd360b10f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758500"
---
# <a name="name-networksettingstype-element"></a>Name-Element (networkSettingsType)

Enthält den Namen eines Netzwerkprofils. Der Name wird zu Anzeigezwecken verwendet.

``` syntax
<xs:element name="Name"
    type="nonEmptyString"
    minOccurs="0"
 />
```

Das **Name-Element** wird durch den komplexen [**NetworkSettingsType-Typ**](taskschedulerschema-networksettingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                            | Abgeleitet von                                                                       | Beschreibung                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingsType)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner verwendet, um ein Netzwerkprofil zu erhalten. Der Taskplaner überprüft die Verfügbarkeit dieses Netzwerks, wenn das [**RunOnlyIfNetworkAvailable-Element**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) auf **True festgelegt ist.**<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie [**unter Name-Eigenschaft von INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).

Informationen zur Skriptentwicklung finden Sie [**unter NetworkSettings.Name**](networksettings-name.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





