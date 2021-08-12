---
title: ShowMessage (actionGroup)-Element
description: Stellt eine Aktion dar, die ein Meldungsfeld zeigt.
ms.assetid: 33c6e437-b993-4b5e-b75a-fb3fda9b24df
keywords:
- ShowMessage-Taskplaner
topic_type:
- apiref
api_name:
- ShowMessage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 474bc44550408591616d3a8d2c6c3c69a5a0d073c90297c60b4a831627c996e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611298"
---
# <a name="showmessage-actiongroup-element"></a>ShowMessage (actionGroup)-Element

Stellt eine Aktion dar, die ein Meldungsfeld zeigt.

``` syntax
<xs:element name="ShowMessage"
    type="showMessageType"
 />
```

Das **ShowMessage-Element** wird durch die [**actionGroup definiert.**](taskschedulerschema-actiongroup-group.md)

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                    | Abgeleitet von                                                       | Beschreibung                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Aktionen (taskType)**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Enthält die aktionen, die von der Aufgabe ausgeführt werden.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                            | type           | Beschreibung                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [**Körper**](taskschedulerschema-body-showmessagetype-element.md)   | nonEmptyString | Gibt den Text an, der im Text des Meldungsfelds angezeigt werden soll. <br/> |
| [**Titel**](taskschedulerschema-title-showmessagetype-element.md) | nonEmptyString | Gibt den Titel des Meldungsfelds an. <br/>                       |



## <a name="remarks"></a>Hinweise

Für die Skripterstellung wird eine Meldungsfeldaktion mithilfe des [**ShowMessageAction-Objekts**](showmessageaction.md) angegeben.

Für die C++-Entwicklung wird eine Meldungsfeldaktion mithilfe der [**IShowMessageAction-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) angegeben.

**Windows 8 und Windows Server 2012:** Dieses Element wurde entfernt. Sie können IExecAction mit der [**MsgBox Windows-Skriptfunktion**](/previous-versions/sfw6660x(v=vs.80)) verwenden, um eine Nachricht in der Benutzersitzung zu zeigen.

## <a name="examples"></a>Beispiele

Ein vollständiges Beispiel für den XML-Code für einen Task, der eine Meldungsfeldaktion verwendet, finden Sie unter [Message Box Example (XML)](/previous-versions//aa381917(v=vs.85)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                 |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                    |



 

