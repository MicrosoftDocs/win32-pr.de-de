---
title: StopIfGoingOnStopps -Element (settingsType)
description: Gibt an, dass der Task beendet wird, wenn der Computer in Akkus gerät.
ms.assetid: 0d772dbb-a552-45ed-9dc0-7159f6ef12ed
keywords:
- StopIfGoingOnStopps-Taskplaner
topic_type:
- apiref
api_name:
- StopIfGoingOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50b92be11400d1dbb223115f11334e2a596e94e9df1fd018ce16e4a646c84825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516099"
---
# <a name="stopifgoingonbatteries-settingstype-element"></a>StopIfGoingOnStopps -Element (settingsType)

Gibt an, dass der Task beendet wird, wenn der Computer in Akkus gerät.

``` syntax
<xs:element name="StopIfGoingOnBatteries"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

Das **StopIfGoingOnStopps-Element** wird durch den komplexen [**settingsType-Typ**](taskschedulerschema-settingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | Beschreibung                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="remarks"></a>Hinweise

Die Standardeinstellung für dieses Element ist False. Beachten Sie, dass sich der Standardwert gegenüber früheren Versionen von Taskplaner.

Für die Skriptentwicklung wird diese Einstellung mithilfe der [**TaskSettings.StopIfGoingOnStopps-Eigenschaft**](tasksettings-stopifgoingonbatteries.md) angegeben.

Für die C++-Entwicklung wird diese Einstellung mithilfe der [**ITaskSettings::StopIfGoingOnStopps-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Einstellungselement, das eine harte Beendigung des Task ermöglicht.


```XML
<Settings>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
</Settings>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





