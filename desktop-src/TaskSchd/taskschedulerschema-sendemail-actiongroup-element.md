---
title: SendEmail (actionGroup)-Element
description: Stellt eine Aktion dar, die eine E-Mail sendet.
ms.assetid: 83416b02-8327-47b3-9dfc-1bf5b9365728
keywords:
- SendEmail-Element Taskplaner
topic_type:
- apiref
api_name:
- SendEmail
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b42a8e63f3b64ef2a66a74300036bbf8ade24a7e0ee5c68b3d1d599f00a04b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099850"
---
# <a name="sendemail-actiongroup-element"></a>SendEmail (actionGroup)-Element

Stellt eine Aktion dar, die eine E-Mail sendet.

``` syntax
<xs:element name="SendEmail"
    type="sendEmailType"
 />
```

Das **SendEmail-Element** wird durch die [**actionGroup definiert.**](taskschedulerschema-actiongroup-group.md)

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                         | Abgeleitet von                                                       | BESCHREIBUNG                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Aktionen**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Enthält die aktionen, die von der Aufgabe ausgeführt werden.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                        | type                                                                         | BESCHREIBUNG                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Attachments**](taskschedulerschema-attachments-sendemailtype-element.md)   | [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md)   | Gibt eine Liste der Anlagen in der E-Mail an.<br/>                                 |
| [**Bcc**](taskschedulerschema-bcc-sendemailtype-element.md)                   | **string**                                                                   | Gibt die E-Mail-Adressen an, die in der Bcc-Zeile einer E-Mail-Nachricht verwendet werden.<br/>               |
| [**Text**](taskschedulerschema-body-sendemailtype-element.md)                 | **string**                                                                   | Gibt den Text im Text der E-Mail an.<br/>                                  |
| [**Cc**](taskschedulerschema-cc-sendemailtype-element.md)                     | **string**                                                                   | Gibt die E-Mail-Adressen an, die in der Cc-Zeile einer E-Mail-Nachricht verwendet werden.<br/>                |
| [**Von**](taskschedulerschema-from-sendemailtype-element.md)                 | **string**                                                                   | Gibt die E-Mail-Adresse des Absenders an.<br/>                                            |
| [**HeaderFields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) | Gibt die Headerfelder und deren Werte an, die im Header der E-Mail-Nachricht verwendet werden.<br/> |
| [**ReplyTo**](taskschedulerschema-replyto-sendemailtype-element.md)           | **string**                                                                   | Gibt die E-Mail-Adressen an, auf die in der E-Mail-Nachricht geantwortet wird.<br/>               |
| [**Server**](taskschedulerschema-server-sendemailtype-element.md)             | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)      | Gibt den E-Mail-Server an, der zum Senden der E-Mail-Nachricht verwendet wird. <br/>                           |
| [**Betreff**](taskschedulerschema-subject-sendemailtype-element.md)           | **string**                                                                   | Gibt den Betreff der E-Mail an.<br/>                                           |
| [**An**](taskschedulerschema-to-sendemailtype-element.md)                     | **string**                                                                   | Gibt die E-Mail-Adressen an, an die die E-Mail gesendet wird.<br/>                        |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**IEmailAction-Schnittstelle.**](/windows/win32/api/taskschd/nn-taskschd-iemailaction)

Informationen zur Skriptentwicklung finden Sie im [**EmailAction-Objekt.**](emailaction.md)

**Windows 8 und Windows Server 2012:** Dieses Element wurde entfernt. Verwenden Sie IExecAction mit dem [**PowerShell-Cmdlet Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) als Problemumgehung.

## <a name="examples"></a>Beispiele

Ein vollständiges Beispiel für den XML-Code für eine Aufgabe, die eine E-Mail-Aktion angibt, finden Sie unter [Ereignistriggerbeispiel (XML).](/previous-versions//aa446889(v=vs.85))

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                 |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                    |



 

