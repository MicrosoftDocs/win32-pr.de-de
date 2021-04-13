---
title: Arguments (exectype)-Element
description: Gibt die Argumente an, die dem Befehlszeilen Vorgang zugeordnet sind.
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
ms.openlocfilehash: ff35465fbad1de82d096b583499ea6cdafe93ca7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518194"
---
# <a name="arguments-exectype-element"></a>Arguments (exectype)-Element

Gibt die Argumente an, die dem Befehlszeilen Vorgang zugeordnet sind.

``` syntax
<xs:element name="Arguments"
    type="string"
 />
```

Das **Arguments** -Element wird durch den komplexen [**exectype**](taskschedulerschema-exectype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                      | Abgeleitet von                                                 | BESCHREIBUNG                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**exectype**](taskschedulerschema-exectype-complextype.md) | Gibt eine Aktion an, die einen Befehlszeilen Vorgang ausführt.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter der [**Arguments-Eigenschaft von IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).

Informationen zur Skript Entwicklung finden Sie unter [**execaction. Arguments**](execaction-arguments.md).

## <a name="examples"></a>Beispiele

Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die eine ausführbare Aktion verwendet, finden Sie unter [time-triggerbeispiel (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





