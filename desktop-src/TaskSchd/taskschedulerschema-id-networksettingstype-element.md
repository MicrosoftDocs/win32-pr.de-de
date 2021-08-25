---
title: Id-Element (networkSettingsType)
description: Enthält einen GUID-Wert, der ein Netzwerkprofil identifiziert.
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- Id-Element Taskplaner
topic_type:
- apiref
api_name:
- Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06196710b9db9d39d45a24b78bccabf479ef210a97f3cea1fd19286b76f2fc42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125840"
---
# <a name="id-networksettingstype-element"></a>Id-Element (networkSettingsType)

Enthält einen GUID-Wert, der ein Netzwerkprofil identifiziert.

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

Das **Id-Element** wird durch den [**komplexen NetworkSettingsType-Typ**](taskschedulerschema-networksettingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                            | Abgeleitet von                                                                       | Beschreibung                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingsType)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner verwendet, um ein Netzwerkprofil zu erhalten. Der Taskplaner überprüft die Verfügbarkeit dieses Netzwerks, wenn das [**RunOnlyIfNetworkAvailable-Element**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) auf **True festgelegt ist.**<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**Id-Eigenschaft von INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).

Informationen zur Skriptentwicklung finden Sie [**unter NetworkSettings.Id**](networksettings-id.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





