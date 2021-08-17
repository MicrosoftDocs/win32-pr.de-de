---
title: NetworkProfileName (settingsType)-Element
description: Enthält den Namen eines Netzwerkprofils. Der Taskplaner überprüft die Verfügbarkeit dieses Netzwerks, wenn das RunOnlyIfNetworkAvailable-Element auf True festgelegt ist. Der Name wird zu Anzeigezwecken verwendet.
ms.assetid: f02dc75c-6c48-4a42-8263-13d9704b993c
keywords:
- NetworkProfileName-element Taskplaner
topic_type:
- apiref
api_name:
- NetworkProfileName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 464c8b8f23dfeed6ea7c3412c3eeec07f20e5a8a7fcea662b4a16dfac7cb3fb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758490"
---
# <a name="networkprofilename-settingstype-element"></a>NetworkProfileName (settingsType)-Element

Enthält den Namen eines Netzwerkprofils. Der Taskplaner überprüft die Verfügbarkeit dieses Netzwerks, wenn das [**RunOnlyIfNetworkAvailable-Element**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) auf **True festgelegt ist.** Der Name wird zu Anzeigezwecken verwendet.

``` syntax
<xs:element name="NetworkProfileName"
    type="string"
    minOccurs="0"
 />
```

Das **NetworkProfileName-Element** wird durch den komplexen [**settingsType-Typ**](taskschedulerschema-settingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                      | Abgeleitet von                                                         | Beschreibung                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Einstellungen (taskType)**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Gibt die Einstellungen an, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





