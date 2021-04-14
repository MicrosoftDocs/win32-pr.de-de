---
title: Actions (TaskType)-Element
description: Enthält die Aktionen, die vom Task ausgeführt werden.
ms.assetid: 0a48fbd6-8a6f-4bad-9b28-0631dce15748
keywords:
- Aktionen (TaskType)-Element Taskplaner
- Aktionen Taskplaner, XML
- Actions-Element Taskplaner
topic_type:
- apiref
api_name:
- Actions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 21af0f8a06faa9cdc61917dcb3b3b0672c47e0e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391695"
---
# <a name="actions-tasktype-element"></a>Actions (TaskType)-Element

Enthält die Aktionen, die vom Task ausgeführt werden.

``` syntax
<xs:element name="Actions"
    type="actionsType"
 />
```

Das **Actions** -Element wird durch den komplexen [**TaskType**](taskschedulerschema-tasktype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                          | Abgeleitet von                                                 | BESCHREIBUNG                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Aufgabe**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Beschreibt den Task, der vom Taskplaner-Dienst ausgeführt wird.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                    | type                                                                       | BESCHREIBUNG                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Comhandler**](taskschedulerschema-comhandler-actiongroup-element.md)   | [**comhandlertype**](taskschedulerschema-comhandlertype-complextype.md)   | Gibt eine Aktion an, die einen Handler auslöst.<br/>                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | [**exectype**](taskschedulerschema-exectype-complextype.md)               | Gibt eine Aktion an, die einen Befehlszeilen Vorgang ausführt.<br/> |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md)     | Gibt eine Aktion an, die eine e-Mail-Nachricht sendet.<br/>            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showmessagetype**](taskschedulerschema-showmessagetype-complextype.md) | Gibt eine Aktion an, die ein Meldungs Feld anzeigt.<br/>               |



## <a name="attributes"></a>Attributes



| Name    | type | BESCHREIBUNG                                                                                          |
|---------|------|------------------------------------------------------------------------------------------------------|
| Kontext |      | Prinzipal Bezeichner des Benutzers, der der Sicherheitskontext für die Aktionen der Aufgabe ist.<br/> |



## <a name="remarks"></a>Bemerkungen

Die zuvor aufgelisteten untergeordneten Elemente (Maximum 32) werden von der Gruppe " [**Aktionsgruppe**](taskschedulerschema-actiongroup-group.md) " definiert. Diese Elemente können in beliebiger Reihenfolge hinzugefügt werden.

Bei der C++-Entwicklung werden die Aktionen einer Aufgabe in der [**iaktioncollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) -Schnittstelle definiert.

Bei der Skript Entwicklung werden die Aktionen einer Aufgabe im [**Aktions Sammlungs**](actioncollection.md) Objekt definiert.

## <a name="examples"></a>Beispiele

Weitere Informationen und ein vollständiges Beispiel für den XML-Code für eine Aufgabe, die eine einzelne Ausführungs Aktion enthält, finden Sie unter [time-triggerbeispiel (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**taskType**](taskschedulerschema-tasktype-complextype.md)
</dt> <dt>

[**Action Group**](taskschedulerschema-actiongroup-group.md)
</dt> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





