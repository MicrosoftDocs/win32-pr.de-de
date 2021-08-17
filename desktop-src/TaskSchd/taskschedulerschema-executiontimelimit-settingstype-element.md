---
title: ExecutionTimeLimit (settingsType)-Element
description: Zulässige Zeit zum Abschließen der Aufgabe.
ms.assetid: c42d0f42-4571-44ab-90b1-948fd7ea991b
keywords:
- ExecutionTimeLimit-Taskplaner
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f6519495cc16cdff6a30c65f75468bd676ca1f2750faedb5c632972c1affb996
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356416"
---
# <a name="executiontimelimit-settingstype-element"></a>ExecutionTimeLimit (settingsType)-Element

Zulässige Zeit zum Abschließen der Aufgabe. Das Format für diese Zeichenfolge ist PnYnMnDTnHnMnS, Dabei steht nY für die Anzahl von Jahren, nM für die Anzahl der Monate, nD für die Anzahl von Tagen, "T" für das Datums-/Uhrzeittrennzeichen, nH für die Anzahl von Stunden, nM für die Anzahl von Minuten und nS für die Anzahl von Sekunden (pt5M gibt beispielsweise 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an). Weitere Informationen zum Dauertyp finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> . Mit dem Wert PT0S kann die Aufgabe unbegrenzt ausgeführt werden.

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
    minOccurs="0"
 />
```

Das **ExecutionTimeLimit-Element** wird durch den komplexen [**settingsType-Typ**](taskschedulerschema-settingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**ExecutionTimeLimit-Eigenschaft von ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit).

Informationen zur Skriptentwicklung finden Sie unter [**TaskSettings.ExecutionTimeLimit**](tasksettings-executiontimelimit.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





