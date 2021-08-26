---
title: RunOnlyIfNetworkAvailable -Element (settingsType)
description: Gibt an, dass die Taskplaner den Task nur dann ausführen, wenn ein Netzwerk verfügbar ist.
ms.assetid: b7b804d3-b31a-4d70-9ba5-805a285e278e
keywords:
- RunOnlyIfNetworkAvailable-Element Taskplaner
topic_type:
- apiref
api_name:
- RunOnlyIfNetworkAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3680ba3c29dc0d258a48aa16ae7923e3761eda30f198384fecfbf238e2933cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991030"
---
# <a name="runonlyifnetworkavailable-settingstype-element"></a>RunOnlyIfNetworkAvailable -Element (settingsType)

Gibt an, dass die Taskplaner den Task nur dann ausführen, wenn ein Netzwerk verfügbar ist.

``` syntax
<xs:element name="RunOnlyIfNetworkAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

Das **RunOnlyIfNetworkAvailable-Element** wird durch den komplexen [**SettingsType-Typ**](taskschedulerschema-settingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | Beschreibung                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**RunOnlyIfNetworkAvailable-Eigenschaft von ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable)

Informationen zur Skriptentwicklung finden Sie unter [**TaskSettings.RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md).

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Einstellungselement, mit dem der Task nur gestartet werden kann, wenn ein Netzwerk verfügbar ist.


```XML
<Settings>
    <RunOnlyIfNetworkAvailable>true</RunOnlyIfNetworkAvailable>
</Settings>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





