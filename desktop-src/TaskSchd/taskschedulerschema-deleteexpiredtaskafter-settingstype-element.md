---
title: Deleteexpiredtaskafter (settingstype)-Element
description: Gibt die Zeitspanne an, die der Taskplaner wartet, bevor der Task nach Ablauf gelöscht wird.
ms.assetid: 947a2fec-ceda-4726-aa1a-26fd1b258c1f
keywords:
- Deleteexpiredtaskafter-Element Taskplaner
topic_type:
- apiref
api_name:
- DeleteExpiredTaskAfter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cee7cfc48f62b58caf63125404fb07209b399fc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340576"
---
# <a name="deleteexpiredtaskafter-settingstype-element"></a>Deleteexpiredtaskafter (settingstype)-Element

Gibt die Zeitspanne an, die der Taskplaner wartet, bevor der Task nach Ablauf gelöscht wird. Wenn für dieses Element kein Wert angegeben wird, wird der Task vom Taskplaner-Dienst nicht gelöscht. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="DeleteExpiredTaskAfter"
    type="duration"
    minOccurs="0"
    default="PT0S"
 />
```

Das **deleteexpiredtaskafter** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**deleteexpiredtaskafter-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter).

Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. deleteexpiredtaskafter**](tasksettings-deleteexpiredtaskafter.md).

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Einstellungs Element, das eine abgelaufene Aufgabe nach einer Woche löscht.


```XML
<Settings>
    <DeleteExpiredTaskAfter>PT7D</DeleteExpiredTaskAfter>
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

 

 





