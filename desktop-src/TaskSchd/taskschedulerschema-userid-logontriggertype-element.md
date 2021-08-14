---
title: UserId (logonTriggerType)-Element
description: Bezeichner des Benutzers. Die Aufgabe wird gestartet, wenn sich dieser Benutzer beim Computer anmeldet.
ms.assetid: 52568899-e351-4ee1-b613-d7c42d7b983d
keywords:
- UserId-Element Taskplaner
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33a1e0f82a3005bfec8e689d088a8d8e28ebbf0a949e4288338d27e68c3a0314
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355566"
---
# <a name="userid-logontriggertype-element"></a>UserId (logonTriggerType)-Element

Bezeichner des Benutzers. Die Aufgabe wird gestartet, wenn sich dieser Benutzer beim Computer anmeldet.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

Das **UserId-Element** wird durch den [**komplexen LogonTriggerType-Typ**](taskschedulerschema-logontriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                       | Abgeleitet von                                                                 | BESCHREIBUNG                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) | Gibt einen Trigger an, der eine Aufgabe startet, wenn sich ein Benutzer anmeldet.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird der Benutzerbezeichner für den Anmeldetrigger mithilfe der [**LogonTrigger.UserId-Eigenschaft**](logontrigger-userid.md) angegeben.

Für die C++-Entwicklung wird der Benutzerbezeichner für den Anmeldetrigger mithilfe der [**ILogonTrigger::UserId-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) angegeben.

## <a name="examples"></a>Beispiele

Ein vollständiges Beispiel für den XML-Code für eine Aufgabe, die einen Anmeldetrigger angibt, finden Sie unter [Logon Trigger Example (XML) (Beispiel für Logon-Trigger (XML)).](logon-trigger-example--xml-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





