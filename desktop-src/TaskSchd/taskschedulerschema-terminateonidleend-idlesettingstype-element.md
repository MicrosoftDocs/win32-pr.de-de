---
title: StopOnIdleEnd (idleSettingsType) -Element
description: Gibt an, dass Taskplaner die Aufgabe beendet, wenn die Leerlaufbedingung endet, bevor der Task abgeschlossen wird.
ms.assetid: 5e8e4fd9-bba1-4ede-a0b3-9f50feb1b6f3
keywords:
- StopOnIdleEnd-Taskplaner
topic_type:
- apiref
api_name:
- TerminateOnIdleEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e6497ca88d43b96096ee6a23ee81a322b0f397757466ed8cf09dd1b3cd45fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356058"
---
# <a name="stoponidleend-idlesettingstype-element"></a>StopOnIdleEnd (idleSettingsType) -Element

Gibt an, dass Taskplaner die Aufgabe beendet, wenn die Leerlaufbedingung endet, bevor der Task abgeschlossen wird.

``` syntax
<xs:element name="StopOnIdleEnd"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

Das **StopOnIdleEnd-Element** wird durch den komplexen [**Typ idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                       | Abgeleitet von                                                                 | BESCHREIBUNG                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**StopOnIdleEnd-Eigenschaft von IIdleSettings.**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend)

Informationen zur Skriptentwicklung finden Sie unter [**IdleSettings.StopOnIdleEnd**](idlesettings-stoponidleend.md).

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert eine Leerlaufeinstellung, die angibt, dass die Aufgabe nicht ausgeführt werden soll, wenn die Leerlaufbedingung endet.


```XML
<IdleSettings>
    <StopOnIdleEnd>false</StopOnIdleEnd>
</IdleSettings>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





