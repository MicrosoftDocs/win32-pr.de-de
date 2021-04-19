---
title: Week (weekstype)-Element
description: Gibt eine bestimmte Woche des Monats an.
ms.assetid: 0cec07da-e9e7-43ef-9f54-48d00114ba1f
keywords:
- Week-Element Taskplaner
topic_type:
- apiref
api_name:
- Week
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0487aa07e1f1132c998b6cb2ba0f518a9db57ce2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342659"
---
# <a name="week-weekstype-element"></a>Week (weekstype)-Element

Gibt eine bestimmte Woche des Monats an.

``` syntax
<xs:element name="Week"
    type="weekType"
 />
```

Das **Week** -Element wird durch den komplexen [**weekstype**](taskschedulerschema-weekstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                        | Abgeleitet von                                                   | BESCHREIBUNG                                                           |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------------------|
| [**Wochen (monthlydayosweekscheduletype)**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) | [**weekstype**](taskschedulerschema-weekstype-complextype.md) | Gibt die Wochen des Monats an, in denen der Task ausgeführt wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Wenn Sie die Wochen des Monats angeben, verwenden Sie die Zahlen 1-4 für die ersten vier Wochen des Monats, oder verwenden Sie die Zeichenfolge "Last", um die letzte Woche des Monats anzugeben.

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

 

 





