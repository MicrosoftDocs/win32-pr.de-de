---
title: Actions(taskType)-Element
description: Enthält die aktionen, die von der Aufgabe ausgeführt werden.
ms.assetid: 0a48fbd6-8a6f-4bad-9b28-0631dce15748
keywords:
- Actions-Element (taskType) Taskplaner
- Aktionen Taskplaner , XML
- Actions-Taskplaner
topic_type:
- apiref
api_name:
- Actions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79fb5fe36b6fcff3622e0d12f0571e7f06c5f00d1ae930abc2bca805315f7dd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357098"
---
# <a name="actions-tasktype-element"></a>Actions(taskType)-Element

Enthält die aktionen, die von der Aufgabe ausgeführt werden.

``` syntax
<xs:element name="Actions"
    type="actionsType"
 />
```

Das **Actions-Element** wird durch den [**komplexen taskType-Typ**](taskschedulerschema-tasktype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                          | Abgeleitet von                                                 | Beschreibung                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Aufgabe**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Beschreibt die Aufgabe, die vom Dienst Taskplaner wird.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                    | Typ                                                                       | Beschreibung                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md)   | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md)   | Gibt eine Aktion an, die einen Handler ausgibt.<br/>                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | [**execType**](taskschedulerschema-exectype-complextype.md)               | Gibt eine Aktion an, die einen Befehlszeilenvorgang ausgibt.<br/> |
| [**Sendemail**](taskschedulerschema-sendemail-actiongroup-element.md)     | [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)     | Gibt eine Aktion an, die eine E-Mail sendet.<br/>            |
| [**Showmessage**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Gibt eine Aktion an, die ein Meldungsfeld zeigt.<br/>               |



## <a name="attributes"></a>Attributes



| Name    | Typ | BESCHREIBUNG                                                                                          |
|---------|------|------------------------------------------------------------------------------------------------------|
| Kontext |      | Prinzipalbezeichner des Benutzers, der der Sicherheitskontext für die Aktionen der Aufgabe ist.<br/> |



## <a name="remarks"></a>Hinweise

Die zuvor aufgeführten untergeordneten Elemente (maximal 32) werden von der [**ActionGroup-Gruppe**](taskschedulerschema-actiongroup-group.md) definiert. Diese Elemente können in beliebiger Reihenfolge hinzugefügt werden.

Für die C++-Entwicklung werden die Aktionen einer Aufgabe in der [**IActionCollection-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) definiert.

Für die Skriptentwicklung werden die Aktionen einer Aufgabe im [**ActionCollection-Objekt**](actioncollection.md) definiert.

## <a name="examples"></a>Beispiele

Weitere Informationen und ein vollständiges Beispiel des XML-Codes für eine Aufgabe, die eine einzelne Ausführungsaktion enthält, finden Sie unter [Time Trigger Example (XML) .](time-trigger-example--xml-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**taskType**](taskschedulerschema-tasktype-complextype.md)
</dt> <dt>

[**Actiongroup**](taskschedulerschema-actiongroup-group.md)
</dt> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





