---
title: EmailAction-Objekt
description: Skripterstellungsobjekt, das eine Aktion darstellt, die eine E-Mail sendet.
ms.assetid: edc0dc4d-eda0-47e0-981f-8521ac4678eb
keywords:
- EmailAction-Taskplaner
- EmailAction-Taskplaner , beschrieben
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
ms.openlocfilehash: c918065515322696a33114d2d9b09b7b72d12eb6b74e120a7963835a23321fe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002478"
---
# <a name="emailaction-object"></a>EmailAction-Objekt

\[Dieses Objekt wird nicht mehr unterstützt. Verwenden Sie IExecAction mit dem [**PowerShell-Cmdlet Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) als Problemumgehung.\]

Skripterstellungsobjekt, das eine Aktion darstellt, die eine E-Mail sendet.

## <a name="members"></a>Member

Das **EmailAction-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **EmailAction-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                    | Zugriffstyp           | BESCHREIBUNG                                                                                               |
|:------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Attachments**](emailaction-attachments.md)<br/>   | Lesen/Schreiben<br/> | Ruft ein Array von Anlagen ab, die mit der E-Mail gesendet werden, oder legt dieses fest.<br/>                      |
| [**Bcc**](emailaction-bcc.md)<br/>                   | Lesen/Schreiben<br/> | Ruft die E-Mail-Adresse oder die Adressen ab, die in der E-Mail-Nachricht Bcc enthalten sein soll, oder legt diese fest.<br/>         |
| [**Text**](emailaction-body.md)<br/>                 | Lesen/Schreiben<br/> | Ruft den Text der E-Mail ab, die die E-Mail enthält, oder legt diesen fest.<br/>                            |
| [**Cc**](emailaction-cc.md)<br/>                     | Lesen/Schreiben<br/> | Ruft die E-Mail-Adresse oder die Adressen ab, die in der E-Mail-Nachricht cc enthalten sein soll, oder legt diese fest.<br/>          |
| [**Von**](emailaction-from.md)<br/>                 | Lesen/Schreiben<br/> | Ruft die E-Mail-Adresse ab, von der Sie die E-Mail senden möchten, oder legt sie fest.<br/>                           |
| [**HeaderFields**](emailaction-headerfields.md)<br/> | Lesen/Schreiben<br/> | Ruft die Headerinformationen in der E-Mail ab, die Sie senden möchten, oder legt sie fest.<br/>                        |
| [**Id**](action-id.md)<br/>                          | Lesen/Schreiben<br/> | Geerbt vom [**Action-Objekt.**](action.md) Ruft den Bezeichner der Aktion ab oder legt den Bezeichner fest.<br/> |
| [**ReplyTo**](emailaction-replyto.md)<br/>           | Lesen/Schreiben<br/> | Ruft die E-Mail-Adresse ab, auf die Sie antworten möchten, oder legt sie fest.<br/>                                      |
| [**Server**](emailaction-server.md)<br/>             | Lesen/Schreiben<br/> | Ruft den Namen des Servers ab, von dem Sie E-Mails senden, oder legt ihn fest.<br/>                           |
| [**Betreff**](emailaction-subject.md)<br/>           | Lesen/Schreiben<br/> | Ruft den Betreff der E-Mail ab oder legt den Betreff fest.<br/>                                                 |
| [**An**](emailaction-to.md)<br/>                     | Lesen/Schreiben<br/> | Ruft die E-Mail-Adresse oder die E-Mail-Adressen ab, an die Sie die E-Mail senden möchten, oder legt sie fest.<br/>                |
| [**type**](/windows/win32/api/taskschd/nf-taskschd-iaction-get_type)<br/>                     | Schreibgeschützt<br/>  | Geerbt vom [**Action-Objekt.**](action.md) Ruft den Typ der Aktion ab.<br/>                   |



 

## <a name="remarks"></a>Hinweise

Die E-Mail-Aktion muss einen gültigen Wert für die [**Eigenschaften Server**](emailaction-server.md), [**From**](emailaction-from.md)und [**To**](emailaction-to.md) oder [**Cc**](emailaction-cc.md) aufweisen, damit der Task ordnungsgemäß registriert und ausgeführt werden kann.

Beim Lesen oder Schreiben eigener XML-Daten für eine Aufgabe wird eine E-Mail-Aktion mithilfe des [**SendEmail-Elements**](taskschedulerschema-sendemail-actiongroup-element.md) des Taskplaner angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skriptobjekt finden Sie unter [Ereignistriggerbeispiel (Skripterstellung).](/previous-versions//aa446887(v=vs.85))

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                    |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                                                       |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

