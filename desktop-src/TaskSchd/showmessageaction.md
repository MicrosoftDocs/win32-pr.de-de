---
title: ShowMessageAction-Objekt
description: Stellt für die Skripterstellung eine Aktion dar, die ein Meldungsfeld anzeigt, wenn eine Aufgabe aktiviert wird.
ms.assetid: fdd22eef-965c-4a81-954c-66011c435ab9
keywords:
- ShowMessageAction-Objekt Taskplaner
- ShowMessageAction-Objekt Taskplaner beschrieben
topic_type:
- apiref
api_name:
- ShowMessageAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2daec97e66c160cc9da1369e44970f5d9e9ee7c5dcbbcea14cee1e4847a9df0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132366"
---
# <a name="showmessageaction-object"></a>ShowMessageAction-Objekt

\[Dieses Objekt wird nicht mehr unterstützt. Sie können IExecAction mit der [**msgBox-Skriptfunktion**](/previous-versions/sfw6660x(v=vs.80)) Windows verwenden, um eine Nachricht in der Benutzersitzung anzuzeigen.\]

Stellt für die Skripterstellung eine Aktion dar, die ein Meldungsfeld anzeigt, wenn eine Aufgabe aktiviert wird.

## <a name="members"></a>Member

Das **ShowMessageAction-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **ShowMessageAction-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                        | Zugriffstyp           | Beschreibung                                                                                               |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Id**](action-id.md)<br/>                              | Lesen/Schreiben<br/> | Geerbt vom [**Action-Objekt.**](action.md) Ruft den Bezeichner der Aktion ab oder legt den Bezeichner fest.<br/> |
| [**MessageBody**](showmessageaction-messagebody.md)<br/> | Lesen/Schreiben<br/> | Ruft den Meldungstext ab, der im Text des Meldungsfelds angezeigt wird, oder legt diesen fest.<br/>                |
| [**Titel**](showmessageaction-title.md)<br/>             | Lesen/Schreiben<br/> | Ruft den Titel des Meldungsfelds ab oder legt den Titel fest.<br/>                                                     |
| [**Typ**](action-type.md)<br/>                          | Schreibgeschützt<br/>  | Geerbt vom [**Action-Objekt.**](action.md) Ruft den Typ der Aktion ab.<br/>               |



 

## <a name="remarks"></a>Hinweise

Für eine Aufgabe, die eine Meldungsfeldaktion enthält, wird das Meldungsfeld angezeigt, wenn der Task aktiviert ist und der Task einen interaktiven Anmeldetyp auf hat. Um den Taskanmeldungstyp auf interactive festzulegen, geben Sie 3 (**TASK \_ LOGON \_ INTERACTIVE \_ TOKEN**) oder 4 (**TASK \_ LOGON \_ GROUP**) in der [**LogonType-Eigenschaft**](principal-logontype.md) des Aufgabenprinzipals oder im *logonType-Parameter* von [**TaskFolder.RegisterTask**](taskfolder-registertask.md) oder [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)an.

Beim Lesen oder Schreiben eigener XML-Daten für eine Aufgabe wird eine Meldungsfeldaktion mithilfe des [**ShowMessage-Elements**](taskschedulerschema-showmessage-actiongroup-element.md) des Taskplaner Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skriptobjekt finden Sie unter [Message Box Example (Scripting) (Message Box-Beispiel (Skripterstellung)).](/previous-versions//aa381916(v=vs.85))

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                    |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                                                       |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

