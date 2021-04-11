---
title: SendEmail (actionGroup)-Element
description: Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.
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
ms.openlocfilehash: 81f6f3437521dea2c5cf6e157ad7997718632081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956920"
---
# <a name="sendemail-actiongroup-element"></a>SendEmail (actionGroup)-Element

Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.

``` syntax
<xs:element name="SendEmail"
    type="sendEmailType"
 />
```

Das **SendEmail** -Element wird von der [**Aktionsgruppe**](taskschedulerschema-actiongroup-group.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                         | Abgeleitet von                                                       | BESCHREIBUNG                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Aktionen**](taskschedulerschema-actions-tasktype-element.md) | [**Aktions sType**](taskschedulerschema-actionstype-complextype.md) | Enthält die Aktionen, die vom Task ausgeführt werden.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                        | type                                                                         | BESCHREIBUNG                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Attachments**](taskschedulerschema-attachments-sendemailtype-element.md)   | [**attachmentstype**](taskschedulerschema-attachmentstype-complextype.md)   | Gibt eine Liste der Anlagen in der e-Mail-Nachricht an.<br/>                                 |
| [**Bcc**](taskschedulerschema-bcc-sendemailtype-element.md)                   | **string**                                                                   | Gibt die e-Mail-Adressen an, die in der Bcc-Zeile einer e-Mail verwendet werden.<br/>               |
| [**Text**](taskschedulerschema-body-sendemailtype-element.md)                 | **string**                                                                   | Gibt den Text im Textkörper der e-Mail-Nachricht an.<br/>                                  |
| [**125**](taskschedulerschema-cc-sendemailtype-element.md)                     | **string**                                                                   | Gibt die e-Mail-Adressen an, die in der CC-Zeile einer e-Mail verwendet werden.<br/>                |
| [**From**](taskschedulerschema-from-sendemailtype-element.md)                 | **string**                                                                   | Gibt die e-Mail-Adresse des Absenders an.<br/>                                            |
| [**Headerfields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerfieldstype**](taskschedulerschema-headerfieldstype-complextype.md) | Gibt die Header Felder und deren Werte an, die im Header der e-Mail-Nachricht verwendet werden.<br/> |
| [**ReplyTo**](taskschedulerschema-replyto-sendemailtype-element.md)           | **string**                                                                   | Gibt die e-Mail-Adressen an, auf die in der e-Mail geantwortet wird.<br/>               |
| [**Servers**](taskschedulerschema-server-sendemailtype-element.md)             | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)      | Gibt den e-Mail-Server an, mit dem die e-Mail gesendet wird. <br/>                           |
| [**Subject**](taskschedulerschema-subject-sendemailtype-element.md)           | **string**                                                                   | Gibt den Betreff der e-Mail-Nachricht an.<br/>                                           |
| [**An**](taskschedulerschema-to-sendemailtype-element.md)                     | **string**                                                                   | Gibt die e-Mail-Adressen an, an die die e-Mail gesendet wird.<br/>                        |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter der [**iemailaction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) -Schnittstelle.

Informationen zur Skript Entwicklung finden Sie unter dem [**emailaction**](emailaction.md) -Objekt.

**Windows 8 und Windows Server 2012:** Dieses Element wurde entfernt. Verwenden Sie "IExecAction" mit dem PowerShell-Cmdlet " [**Send-Mail Message**](/powershell/module/microsoft.powershell.utility/send-mailmessage) " als Problem Umgehung.

## <a name="examples"></a>Beispiele

Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die eine e-Mail-Aktion angibt, finden Sie unter [Event triggerbeispiel (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                 |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                    |



 

