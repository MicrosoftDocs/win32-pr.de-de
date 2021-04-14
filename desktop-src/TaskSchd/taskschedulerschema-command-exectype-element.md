---
title: Command (exectype)-Element
description: Gibt die ausführbare Datei oder das Dokument an, das ausgeführt werden soll.
ms.assetid: dedf8627-926c-43c6-8add-21ff298d697a
keywords:
- Command-Element Taskplaner
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9d27eb5b40d652035882efc311d9735bcbdd23e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392121"
---
# <a name="command-exectype-element"></a>Command (exectype)-Element

Gibt die ausführbare Datei oder das Dokument an, das ausgeführt werden soll.

``` syntax
<xs:element name="Command"
    type="pathType"
 />
```

Das **Command** -Element wird durch den komplexen [**exectype**](taskschedulerschema-exectype-complextype.md) -Typ definiert.

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

 

 





