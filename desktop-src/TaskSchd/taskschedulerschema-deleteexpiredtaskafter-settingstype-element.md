---
title: DeleteExpiredTaskAfter (settingsType)-Element
description: Gibt die Zeit an, die der Taskplaner, bevor der Task nach ablaufen gelöscht wird.
ms.assetid: 947a2fec-ceda-4726-aa1a-26fd1b258c1f
keywords:
- DeleteExpiredTaskAfter-Taskplaner
topic_type:
- apiref
api_name:
- DeleteExpiredTaskAfter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e4f491d857eb4ca0fde629b780f22a7795b79f593f94332fb923003520cec706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357209"
---
# <a name="deleteexpiredtaskafter-settingstype-element"></a>DeleteExpiredTaskAfter (settingsType)-Element

Gibt die Zeit an, die der Taskplaner, bevor der Task nach ablaufen gelöscht wird. Wenn für dieses Element kein Wert angegeben wird, löscht der Taskplaner den Task nicht. Das Format für diese Zeichenfolge ist PnYnMnDTnHnMnS, Dabei steht nY für die Anzahl von Jahren, nM für die Anzahl der Monate, nD für die Anzahl von Tagen, "T" für das Datums-/Uhrzeittrennzeichen, nH für die Anzahl von Stunden, nM für die Anzahl von Minuten und nS für die Anzahl von Sekunden (pt5M gibt beispielsweise 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an). Weitere Informationen zum Dauertyp finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="DeleteExpiredTaskAfter"
    type="duration"
    minOccurs="0"
    default="PT0S"
 />
```

Das **DeleteExpiredTaskAfter-Element** wird durch den komplexen [**settingsType-Typ**](taskschedulerschema-settingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**DeleteExpiredTaskAfter-Eigenschaft von ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter)

Informationen zur Skriptentwicklung finden Sie [**unter TaskSettings.DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md).

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Einstellungselement, das eine abgelaufene Aufgabe nach einer Woche löscht.


```XML
<Settings>
    <DeleteExpiredTaskAfter>PT7D</DeleteExpiredTaskAfter>
</Settings>
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

 

 





