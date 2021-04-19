---
title: Restartondle (idlesettingstype)-Element
description: Gibt an, ob der Task neu gestartet wird, wenn der Computer mehrmals in eine Leerlauf Bedingung wechselt.
ms.assetid: 7a7a388c-8dc9-4106-82c1-3435d9f89866
keywords:
- Restartondle-Element Taskplaner
topic_type:
- apiref
api_name:
- RestartOnIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec1d20798b7ceb6ad6ebe2c3a92896600e36eec1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346539"
---
# <a name="restartonidle-idlesettingstype-element"></a>Restartondle (idlesettingstype)-Element

Gibt an, ob der Task neu gestartet wird, wenn der Computer mehrmals in eine Leerlauf Bedingung wechselt.

``` syntax
<xs:element name="RestartOnIdle"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

Das **restartondle** -Element wird durch den komplexen [**idlesettingstype**](taskschedulerschema-idlesettingstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                       | Abgeleitet von                                                                 | BESCHREIBUNG                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**Idlesettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idlesettingstype**](taskschedulerschema-idlesettingstype-complextype.md) | Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.<br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Element wird nur verwendet, wenn das [**terminateonidleend**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) -Element auf true festgelegt ist.

Bei der Skript Entwicklung werden diese Aufgaben Einstellungen mithilfe der [**idlesettings. restartondle**](idlesettings-restartonidle.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung werden diese Aufgaben Einstellungen mithilfe der [**iidlesettings:: restartondle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert eine Leerlauf Einstellung, die angibt, dass die Aufgabe nicht neu gestartet werden soll, wenn die Leerlauf Bedingung nicht erfüllt ist.


```XML
<IdleSettings>
     <TerminateOnIdleEnd>true</TerminateOnIdleEnd>
     <RestartOnIdle>true</RestartOnIdle>
</IdleSettings>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





