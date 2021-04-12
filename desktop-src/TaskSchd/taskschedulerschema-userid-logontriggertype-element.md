---
title: UserID-Element (logontriggertype)
description: Der Bezeichner des Benutzers. Der Task wird gestartet, wenn sich der Benutzer am Computer anmeldet.
ms.assetid: 52568899-e351-4ee1-b613-d7c42d7b983d
keywords:
- UserID-Element Taskplaner
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69d6534122b4b5e11a18a64ffa9bbb5e29e2a68a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519108"
---
# <a name="userid-logontriggertype-element"></a>UserID-Element (logontriggertype)

Der Bezeichner des Benutzers. Der Task wird gestartet, wenn sich der Benutzer am Computer anmeldet.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

Das **UserID** -Element wird durch den komplexen [**logontriggertype**](taskschedulerschema-logontriggertype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                       | Abgeleitet von                                                                 | BESCHREIBUNG                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Logonauslöst**](taskschedulerschema-logontrigger-triggergroup-element.md) | [**logontriggertype**](taskschedulerschema-logontriggertype-complextype.md) | Gibt einen-Vorgang an, der einen Task startet, wenn sich ein Benutzer anmeldet.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skripterstellung wird die Benutzer-ID für den Logon-Auslösers mithilfe der [**logonauslöst. UserID**](logontrigger-userid.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird die Benutzer-ID für den Logon-Auslösers mithilfe der [**iLogon-Eigenschaft:: UserID**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen Logon-Vorgang angibt, finden Sie unter [Logon-auslöserbeispiel (XML)](logon-trigger-example--xml-.md).

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

 

 





