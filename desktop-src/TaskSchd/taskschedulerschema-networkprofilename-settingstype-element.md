---
title: Networkprofilename (settingstype)-Element
description: Enthält den Namen eines Netzwerk Profils. Der Taskplaner Dienst prüft die Verfügbarkeit dieses Netzwerks, wenn das runonlyifnetworkavailable-Element auf "true" festgelegt ist. Der Name wird zu Anzeige Zwecken verwendet.
ms.assetid: f02dc75c-6c48-4a42-8263-13d9704b993c
keywords:
- Networkprofilename-Element Taskplaner
topic_type:
- apiref
api_name:
- NetworkProfileName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76a1e89b1d40a422f10512583563e9b1ac56c06f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742160"
---
# <a name="networkprofilename-settingstype-element"></a>Networkprofilename (settingstype)-Element

Enthält den Namen eines Netzwerk Profils. Der Taskplaner Dienst prüft die Verfügbarkeit dieses Netzwerks, wenn das [**runonlyifnetworkavailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) -Element auf " **true**" festgelegt ist. Der Name wird zu Anzeige Zwecken verwendet.

``` syntax
<xs:element name="NetworkProfileName"
    type="string"
    minOccurs="0"
 />
```

Das **networkprofilename** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                      | Abgeleitet von                                                         | BESCHREIBUNG                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Einstellungen (TaskType)**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Gibt die Einstellungen an, die vom Taskplaner zum Ausführen der Aufgabe verwendet werden.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





