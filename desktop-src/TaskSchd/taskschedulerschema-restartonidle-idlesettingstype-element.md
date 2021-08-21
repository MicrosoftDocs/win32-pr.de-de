---
title: RestartOnIdle (idleSettingsType)-Element
description: Gibt an, ob der Task neu gestartet wird, wenn der Computer mehr als einmal in eine Leerlaufbedingung eintritt.
ms.assetid: 7a7a388c-8dc9-4106-82c1-3435d9f89866
keywords:
- RestartOnIdle-Element Taskplaner
topic_type:
- apiref
api_name:
- RestartOnIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16a636ebc052bb04a150390659909f0b73cae78871acaacfb4ba529ea2d8e917
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575140"
---
# <a name="restartonidle-idlesettingstype-element"></a>RestartOnIdle (idleSettingsType)-Element

Gibt an, ob der Task neu gestartet wird, wenn der Computer mehr als einmal in eine Leerlaufbedingung eintritt.

``` syntax
<xs:element name="RestartOnIdle"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

Das **RestartOnIdle-Element** wird durch den komplexen Typ [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                       | Abgeleitet von                                                                 | Beschreibung                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Gibt an, wie der Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.<br/> |



## <a name="remarks"></a>Hinweise

Dieses Element wird nur verwendet, wenn das [**TerminateOnIdleEnd-Element**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) auf True festgelegt ist.

Für die Skriptentwicklung werden diese Taskeinstellungen mithilfe der [**IdleSettings.RestartOnIdle-Eigenschaft**](idlesettings-restartonidle.md) angegeben.

Für die C++-Entwicklung werden diese Taskeinstellungen mithilfe der [**IIdleSettings::RestartOnIdle-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert eine Leerlaufeinstellung, die angibt, dass der Task nicht neu gestartet werden soll, wenn die Leerlaufbedingung zyklen.


```XML
<IdleSettings>
     <TerminateOnIdleEnd>true</TerminateOnIdleEnd>
     <RestartOnIdle>true</RestartOnIdle>
</IdleSettings>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





