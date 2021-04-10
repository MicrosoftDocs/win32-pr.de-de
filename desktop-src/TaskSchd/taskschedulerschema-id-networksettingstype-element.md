---
title: ID-Element (networksettingstype)
description: Enthält einen GUID-Wert, der ein Netzwerk Profil identifiziert.
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- ID-Element Taskplaner
topic_type:
- apiref
api_name:
- Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d14865d50e9c3418e3ef65cdbeaea747a98a4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106370"
---
# <a name="id-networksettingstype-element"></a>ID-Element (networksettingstype)

Enthält einen GUID-Wert, der ein Netzwerk Profil identifiziert.

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

Das **ID** -Element wird durch den komplexen Typ [**networksettingstype**](taskschedulerschema-networksettingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                            | Abgeleitet von                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Network Settings (settingstype)**](taskschedulerschema-networksettings-settingstype-element.md) | [**Network settingstype**](taskschedulerschema-networksettingstype-complextype.md) | Enthält die Einstellungen, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden. Der Taskplaner Dienst prüft die Verfügbarkeit dieses Netzwerks, wenn das [**runonlyifnetworkavailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) -Element auf " **true**" festgelegt ist.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**ID-Eigenschaft von inetworksettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).

Informationen zur Skript Entwicklung finden Sie unter [**NetworkSettings.ID**](networksettings-id.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





