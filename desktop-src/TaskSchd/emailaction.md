---
title: EmailAction-Objekt
description: Skript Objekt, das eine Aktion darstellt, die eine e-Mail-Nachricht sendet.
ms.assetid: edc0dc4d-eda0-47e0-981f-8521ac4678eb
keywords:
- Emailaction-Objekt Taskplaner
- Emailaction-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- EmailAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a339a1549b76f61499b7192a48edc7c1b86a6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859186"
---
# <a name="emailaction-object"></a>EmailAction-Objekt

\[Dieses Objekt wird nicht mehr unterstützt. Verwenden Sie "IExecAction" mit dem PowerShell-Cmdlet " [**Send-Mail Message**](/powershell/module/microsoft.powershell.utility/send-mailmessage) " als Problem Umgehung.\]

Skript Objekt, das eine Aktion darstellt, die eine e-Mail-Nachricht sendet.

## <a name="members"></a>Member

Das **emailaction** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **emailaction** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                    | Zugriffstyp           | BESCHREIBUNG                                                                                               |
|:------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Attachments**](emailaction-attachments.md)<br/>   | Lesen/Schreiben<br/> | Ruft ein Array von Anlagen ab, das mit der e-Mail gesendet wird, oder legt dieses fest.<br/>                      |
| [**Bcc**](emailaction-bcc.md)<br/>                   | Lesen/Schreiben<br/> | Dient zum Abrufen oder Festlegen der e-Mail-Adressen, die Sie in der e-Mail-Nachricht für Bcc angeben möchten<br/>         |
| [**Text**](emailaction-body.md)<br/>                 | Lesen/Schreiben<br/> | Ruft den Textkörper der e-Mail ab, der die e-Mail enthält, oder legt diesen fest.<br/>                            |
| [**125**](emailaction-cc.md)<br/>                     | Lesen/Schreiben<br/> | Dient zum Abrufen oder Festlegen der e-Mail-Adressen, die Sie in der e-Mail-Nachricht CC CC angeben möchten<br/>          |
| [**From**](emailaction-from.md)<br/>                 | Lesen/Schreiben<br/> | Ruft die e-Mail-Adresse ab, von der Sie die e-Mail senden möchten, oder legt Sie fest.<br/>                           |
| [**Headerfields**](emailaction-headerfields.md)<br/> | Lesen/Schreiben<br/> | Ruft die Header Informationen in der e-Mail ab, die Sie senden möchten, oder legt diese fest.<br/>                        |
| [**Name**](action-id.md)<br/>                          | Lesen/Schreiben<br/> | Wird vom [**Action**](action.md) -Objekt geerbt. Ruft den Bezeichner der Aktion ab oder legt ihn fest.<br/> |
| [**ReplyTo**](emailaction-replyto.md)<br/>           | Lesen/Schreiben<br/> | Ruft die e-Mail-Adresse ab, der Sie antworten möchten, oder legt Sie fest.<br/>                                      |
| [**Servers**](emailaction-server.md)<br/>             | Lesen/Schreiben<br/> | Ruft den Namen des Servers ab, der zum Senden von e-Mails verwendet wird, oder legt ihn fest.<br/>                           |
| [**Subject**](emailaction-subject.md)<br/>           | Lesen/Schreiben<br/> | Ruft den Betreff der e-Mail-Nachricht ab oder legt diesen fest.<br/>                                                 |
| [**An**](emailaction-to.md)<br/>                     | Lesen/Schreiben<br/> | Ruft die e-Mail-Adresse oder Adressen ab, an die die e-Mail gesendet werden soll, oder legt diese fest.<br/>                |
| [**type**](/windows/win32/api/taskschd/nf-taskschd-iaction-get_type)<br/>                     | Schreibgeschützt<br/>  | Wird vom [**Aktions**](action.md) Objekt geerbt. Ruft den Typ der Aktion ab.<br/>                   |



 

## <a name="remarks"></a>Bemerkungen

Die e-Mail-Aktion muss einen gültigen Wert für die Eigenschaften " [**Server**](emailaction-server.md)", " [**from**](emailaction-from.md)" und " [**to**](emailaction-to.md) " und " [**CC**](emailaction-cc.md) " aufweisen, damit die Aufgabe ordnungsgemäß registriert und ausgeführt

Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird eine e-Mail-Aktion mithilfe des [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) -Elements des Taskplaner-Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [Event-auslöserbeispiel (Skripterstellung)](/previous-versions//aa446887(v=vs.85)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                    |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                                                       |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

