---
title: Multipleinstancespolicy-Element (settingstype)
description: Gibt die Richtlinie an, mit der definiert wird, wie die Taskplaner mehrere Instanzen der Aufgabe behandelt.
ms.assetid: ec82d396-f83c-4684-98ab-f70e15ada075
keywords:
- Multipleinstancespolicy-Element Taskplaner
topic_type:
- apiref
api_name:
- MultipleInstancesPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5bcbbd26880f1ccced3e71b44dc93993d20f4a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339165"
---
# <a name="multipleinstancespolicy-settingstype-element"></a>Multipleinstancespolicy-Element (settingstype)

Gibt die Richtlinie an, mit der definiert wird, wie die Taskplaner mehrere Instanzen der Aufgabe behandelt.

``` syntax
<xs:element name="MultipleInstancesPolicy"
    type="multipleInstancesPolicyType"
 />
```

Das **multipleinstancespolicy** -Element wird vom einfachen Typ " [**multipleinstancespolicytype**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) " definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**multipleinhaltungen-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).

Informationen zur Skript Entwicklung finden Sie unter [**Task Settings. multipleinhaltungen**](tasksettings-multipleinstances.md).

### <a name="restricted-values"></a>Eingeschränkte Werte

Dieses Element ist auf die folgenden Werte beschränkt.

-   Parallel: startet eine neue-Instanz, während eine vorhandene-Instanz ausgeführt wird.
-   Queue: startet eine neue Instanz der Aufgabe, nachdem alle anderen Instanzen der Aufgabe vollständig sind.
-   Ignorumew: Standardwert. Startet keine neue Instanz, wenn eine vorhandene Instanz der Aufgabe ausgeführt wird.
-   StopAll: beendet eine vorhandene Instanz der Aufgabe, bevor eine neue Instanz gestartet wird.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein settings-Element, das es ermöglicht, mehrere Instanzen der Aufgabe parallel auszuführen.


```XML
<Settings>
    <MultipleInstancesPolicy>Parallel</MultipleInstancesPolicy>
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

 

 





