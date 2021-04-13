---
title: ShowMessage-Element (Aktionsgruppe)
description: Stellt eine Aktion dar, die ein Meldungs Feld anzeigt.
ms.assetid: 33c6e437-b993-4b5e-b75a-fb3fda9b24df
keywords:
- ShowMessage-Element Taskplaner
topic_type:
- apiref
api_name:
- ShowMessage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1344aadfa5fe67e411048bac2a83330ea704c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340497"
---
# <a name="showmessage-actiongroup-element"></a>ShowMessage-Element (Aktionsgruppe)

Stellt eine Aktion dar, die ein Meldungs Feld anzeigt.

``` syntax
<xs:element name="ShowMessage"
    type="showMessageType"
 />
```

Das **ShowMessage** -Element wird von der [**Aktionsgruppe**](taskschedulerschema-actiongroup-group.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                    | Abgeleitet von                                                       | BESCHREIBUNG                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Aktionen (TaskType)**](taskschedulerschema-actions-tasktype-element.md) | [**Aktions sType**](taskschedulerschema-actionstype-complextype.md) | Enthält die Aktionen, die vom Task ausgeführt werden.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                            | type           | BESCHREIBUNG                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [**Text**](taskschedulerschema-body-showmessagetype-element.md)   | nonEmptyString | Gibt den Text an, der im Textkörper des Meldungs Felds angezeigt werden soll. <br/> |
| [**Titel**](taskschedulerschema-title-showmessagetype-element.md) | nonEmptyString | Gibt den Titel des Meldungs Felds an. <br/>                       |



## <a name="remarks"></a>Bemerkungen

Bei der Skripterstellung wird eine MessageBox-Aktion mithilfe des [**showmessageaction**](showmessageaction.md) -Objekts angegeben.

Bei der C++-Entwicklung wird eine MessageBox-Aktion mithilfe der [**ishowmessageaction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) -Schnittstelle angegeben.

**Windows 8 und Windows Server 2012:** Dieses Element wurde entfernt. Sie können IExecAction mit der Windows Scripting [**MsgBox-Funktion**](/previous-versions/sfw6660x(v=vs.80)) verwenden, um eine Meldung in der Benutzersitzung anzuzeigen.

## <a name="examples"></a>Beispiele

Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die eine Meldungs Feld Aktion verwendet, finden Sie unter [Message Box example (XML)](/previous-versions//aa381917(v=vs.85)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                 |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                    |



 

