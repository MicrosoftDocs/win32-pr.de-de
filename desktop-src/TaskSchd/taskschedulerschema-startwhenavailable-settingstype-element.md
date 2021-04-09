---
title: Starteinavailable (settingstype)-Element
description: Gibt an, dass die Taskplaner die Aufgabe jederzeit starten kann, nachdem die geplante Zeit abgelaufen ist.
ms.assetid: 1d65fd51-3a94-4083-8e38-2a652383656a
keywords:
- Startstartbare Element Taskplaner
topic_type:
- apiref
api_name:
- StartWhenAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d86f6f6e75457d08e10ef40d728eaf3e3b00aa7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949572"
---
# <a name="startwhenavailable-settingstype-element"></a>Starteinavailable (settingstype)-Element

Gibt an, dass die Taskplaner die Aufgabe jederzeit starten kann, nachdem die geplante Zeit abgelaufen ist.

``` syntax
<xs:element name="StartWhenAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

Das **starteinavailable** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.<br/> |



## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gilt nur für zeitgesteuerte Tasks.

Informationen zur C++-Entwicklung finden Sie unter [**Start-verfügbare Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).

Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. start\available**](tasksettings-startwhenavailable.md).

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein settings-Element, das dem Taskplaner ermöglicht, die Aufgabe zu starten, wenn Sie verfügbar ist.


```XML
<Settings>
    <StartWhenAvailable>true</StartWhenAvailable>
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

 

 





