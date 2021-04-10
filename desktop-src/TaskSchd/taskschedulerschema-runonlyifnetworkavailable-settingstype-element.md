---
title: Runonlyifnetworkavailable (settingstype)-Element
description: Gibt an, dass der Taskplaner die Aufgabe nur dann ausgeführt wird, wenn ein Netzwerk verfügbar ist.
ms.assetid: b7b804d3-b31a-4d70-9ba5-805a285e278e
keywords:
- Runonlyifnetworkavailable-Element Taskplaner
topic_type:
- apiref
api_name:
- RunOnlyIfNetworkAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ff1e7c838c142e30b75eb4abb935c0de352d9f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956959"
---
# <a name="runonlyifnetworkavailable-settingstype-element"></a>Runonlyifnetworkavailable (settingstype)-Element

Gibt an, dass der Taskplaner die Aufgabe nur dann ausgeführt wird, wenn ein Netzwerk verfügbar ist.

``` syntax
<xs:element name="RunOnlyIfNetworkAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

Das **runonlyifnetworkavailable** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**der runonlyifnetworkavailable-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable).

Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. runonlyifnetworkavailable**](tasksettings-runonlyifnetworkavailable.md).

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein settings-Element, das es ermöglicht, dass der Task nur gestartet wird, wenn ein Netzwerk verfügbar ist.


```XML
<Settings>
    <RunOnlyIfNetworkAvailable>true</RunOnlyIfNetworkAvailable>
</Settings>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





