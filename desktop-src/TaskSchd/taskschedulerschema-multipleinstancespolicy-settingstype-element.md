---
title: MultipleInstancesPolicy -Element (settingsType)
description: Gibt die Richtlinie an, die definiert, wie die Taskplaner mit mehreren Instanzen der Aufgabe umgeht.
ms.assetid: ec82d396-f83c-4684-98ab-f70e15ada075
keywords:
- MultipleInstancesPolicy-Element Taskplaner
topic_type:
- apiref
api_name:
- MultipleInstancesPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d7728d2b39fbcbed060fce409f4d721b59ef5ca324cd141d7777a5ffed110a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072450"
---
# <a name="multipleinstancespolicy-settingstype-element"></a>MultipleInstancesPolicy -Element (settingsType)

Gibt die Richtlinie an, die definiert, wie die Taskplaner mit mehreren Instanzen der Aufgabe umgeht.

``` syntax
<xs:element name="MultipleInstancesPolicy"
    type="multipleInstancesPolicyType"
 />
```

Das **MultipleInstancesPolicy-Element** wird durch den [**einfachen MultipleInstancesPolicyType-Typ**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**MultipleInstances-Eigenschaft von ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances)

Informationen zur Skriptentwicklung finden Sie unter [**TaskSettings.MultipleInstances.**](tasksettings-multipleinstances.md)

### <a name="restricted-values"></a>Eingeschränkte Werte

Dieses Element ist auf die folgenden Werte beschränkt.

-   Parallel: Startet eine neue Instanz, während eine vorhandene Instanz ausgeführt wird.
-   Warteschlange: Startet eine neue Instanz des Tasks, nachdem alle anderen Instanzen des Tasks abgeschlossen sind.
-   IgnoreNew: Standard. Startet keine neue Instanz, wenn eine vorhandene Instanz des Tasks ausgeführt wird.
-   StopExisting: Beendet eine vorhandene Instanz des Tasks, bevor eine neue Instanz gestartet wird.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Einstellungselement, mit dem mehrere Instanzen des Tasks parallel ausgeführt werden können.


```XML
<Settings>
    <MultipleInstancesPolicy>Parallel</MultipleInstancesPolicy>
</Settings>
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





