---
title: Name (networksettingstype)-Element
description: Enthält den Namen eines Netzwerk Profils. Der Name wird zu Anzeige Zwecken verwendet.
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
ms.openlocfilehash: ed877b731b64ee8f2d807067b59399decc0eefe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518071"
---
# <a name="name-networksettingstype-element"></a>Name (networksettingstype)-Element

Enthält den Namen eines Netzwerk Profils. Der Name wird zu Anzeige Zwecken verwendet.

``` syntax
<xs:element name="Name"
    type="nonEmptyString"
    minOccurs="0"
 />
```

Das **Name** -Element wird durch den komplexen Typ [**networksettingstype**](taskschedulerschema-networksettingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                            | Abgeleitet von                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Network Settings (settingstype)**](taskschedulerschema-networksettings-settingstype-element.md) | [**Network settingstype**](taskschedulerschema-networksettingstype-complextype.md) | Enthält die Einstellungen, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden. Der Taskplaner Dienst prüft die Verfügbarkeit dieses Netzwerks, wenn das [**runonlyifnetworkavailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) -Element auf " **true**" festgelegt ist.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**Name-Eigenschaft von inetworksettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).

Informationen zur Skript Entwicklung finden Sie unter [**NetworkSettings.Name**](networksettings-name.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





