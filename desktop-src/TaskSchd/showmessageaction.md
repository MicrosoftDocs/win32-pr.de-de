---
title: Showmessageaction-Objekt
description: Stellt bei der Skripterstellung eine Aktion dar, die ein Meldungs Feld anzeigt, wenn eine Aufgabe aktiviert wird.
ms.assetid: fdd22eef-965c-4a81-954c-66011c435ab9
keywords:
- Showmessageaction-Objekt Taskplaner
- Showmessageaction-Objekt Taskplaner, beschrieben
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
ms.openlocfilehash: ef1e500f0492ad010e88719a467fda38f85e184c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391698"
---
# <a name="showmessageaction-object"></a>Showmessageaction-Objekt

\[Dieses Objekt wird nicht mehr unterstützt. Sie können IExecAction mit der Windows Scripting [**MsgBox-Funktion**](/previous-versions/sfw6660x(v=vs.80)) verwenden, um eine Meldung in der Benutzersitzung anzuzeigen.\]

Stellt bei der Skripterstellung eine Aktion dar, die ein Meldungs Feld anzeigt, wenn eine Aufgabe aktiviert wird.

## <a name="members"></a>Member

Das **showmessageaction** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **showmessageaction** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                        | Zugriffstyp           | BESCHREIBUNG                                                                                               |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Name**](action-id.md)<br/>                              | Lesen/Schreiben<br/> | Wird vom [**Action**](action.md) -Objekt geerbt. Ruft den Bezeichner der Aktion ab oder legt ihn fest.<br/> |
| [**MessageBody**](showmessageaction-messagebody.md)<br/> | Lesen/Schreiben<br/> | Ruft den Meldungs Text ab, der im Textkörper des Meldungs Felds angezeigt wird, oder legt diesen fest.<br/>                |
| [**Titel**](showmessageaction-title.md)<br/>             | Lesen/Schreiben<br/> | Ruft den Titel des Meldungs Felds ab oder legt diesen fest.<br/>                                                     |
| [**type**](action-type.md)<br/>                          | Schreibgeschützt<br/>  | Wird vom [**Action**](action.md) -Objekt geerbt. Ruft den Typ der Aktion ab.<br/>               |



 

## <a name="remarks"></a>Bemerkungen

Für einen Task, der eine MessageBox-Aktion enthält, wird das Meldungs Feld angezeigt, wenn die Aufgabe aktiviert ist und der Task einen interaktiven Anmeldetyp aufweist. Wenn Sie den Anmeldetyp für die Aufgabe interaktiv festlegen möchten, geben Sie in der [**logontype**](principal-logontype.md) -Eigenschaft des Task Prinzipals oder im *logontype* -Parameter von [**taskfolder. RegisterTask**](taskfolder-registertask.md) oder [**taskfolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)den Wert 3 an.**\_ \_ \_****\_ \_**

Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird eine Meldungs Feld Aktion mit dem [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter Beispiel für Meldungs Felder [(Skripterstellung)](/previous-versions//aa381916(v=vs.85)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                    |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                                                       |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

