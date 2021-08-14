---
title: Arguments (execType)-Element
description: Gibt die Argumente an, die dem Befehlszeilenvorgang zugeordnet sind.
ms.assetid: 37207c4f-941c-4cbf-9a81-5876b224a7c1
keywords:
- Arguments-Element Taskplaner
topic_type:
- apiref
api_name:
- Arguments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: edf76f7073e62aac10c85dc035d3b441a90a4e0ee1fae90b4decf5cffc4568df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132075"
---
# <a name="arguments-exectype-element"></a>Arguments (execType)-Element

Gibt die Argumente an, die dem Befehlszeilenvorgang zugeordnet sind.

``` syntax
<xs:element name="Arguments"
    type="string"
 />
```

Das **Arguments-Element** wird durch den komplexen [**execType-Typ**](taskschedulerschema-exectype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                      | Abgeleitet von                                                 | BESCHREIBUNG                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**execType**](taskschedulerschema-exectype-complextype.md) | Gibt eine Aktion an, die einen Befehlszeilenvorgang ausführt.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter der [**Arguments-Eigenschaft von IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).

Informationen zur Skriptentwicklung finden Sie unter [**ExecAction.Arguments**](execaction-arguments.md).

## <a name="examples"></a>Beispiele

Ein vollständiges Beispiel für den XML-Code für eine Aufgabe, die eine ausführbare Aktion verwendet, finden Sie unter [Time Trigger Example (XML) (Zeittriggerbeispiel (XML)).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





