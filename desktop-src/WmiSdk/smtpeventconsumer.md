---
description: Die Klasse smtpeer-Consumer sendet eine e-Mail-Nachricht mit Simple Mail Transfer Protocol (SMTP), wenn ein Ereignis an Sie übermittelt wird.
ms.assetid: 42178360-9e22-4cd1-9b72-5f6b0d7e6c9c
ms.tgt_platform: multiple
title: Smtpventconsumer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMTPEventConsumer
- SMTPEventConsumer.CreatorSID
- SMTPEventConsumer.MachineName
- SMTPEventConsumer.MaximumQueueSize
- SMTPEventConsumer.BccLine
- SMTPEventConsumer.CcLine
- SMTPEventConsumer.FromLine
- SMTPEventConsumer.HeaderFields
- SMTPEventConsumer.Message
- SMTPEventConsumer.Name
- SMTPEventConsumer.ReplyToLine
- SMTPEventConsumer.SMTPServer
- SMTPEventConsumer.Subject
- SMTPEventConsumer.ToLine
api_type:
- DllExport
api_location:
- Smtpcons.dll
ms.openlocfilehash: 76c7fad3b5cb4bbf6c3c0c03689607ba64fbcc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218306"
---
# <a name="smtpeventconsumer-class"></a>Smtpventconsumer-Klasse

Die Klasse **smtpeer-Consumer** sendet eine e-Mail-Nachricht mit Simple Mail Transfer Protocol (SMTP), wenn ein Ereignis an Sie übermittelt wird. Ein SMTP-Server muss im Netzwerk vorhanden sein. Die Klasse smtpventconsumer unterstützt keine Anlagen. Die Codierung der e-Mail-Nachricht muss "US-ASCII" lauten.

Diese Klasse ist einer der standardereignisconsumer, die von WMI bereitstellt werden. Ein Beispiel für die Verwendung von **smtpeer-Consumer** , um einen Consumer zu erstellen, finden Sie unter [Senden von e-Mails auf der Grundlage eines Ereignisses](sending-e-mail-based-on-an-event.md). Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class SMTPEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  string BccLine;
  string CcLine;
  string FromLine;
  string HeaderFields[];
  string Message;
  string Name;
  string ReplyToLine;
  string SMTPServer;
  string Subject;
  string ToLine;
};
```

## <a name="members"></a>Member

Die Klasse **smtpventconsumer** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Klasse **smtpventconsumer** verfügt über diese Eigenschaften.

<dl> <dt>

**Bccline**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Liste von Adressen, getrennt durch ein Komma oder Semikolon, im Format einer standardmäßigen Zeichen folgen Vorlage, an die die Nachricht als Blind Kopie gesendet wird. Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.

</dd> <dt>

**Ccline**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Liste von Adressen, getrennt durch ein Komma oder Semikolon, im Format einer standardmäßigen Zeichen folgen Vorlage, an die die Nachricht als Kopie der Nachricht gesendet wird. Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.

</dd> <dt>

**"Kreatorsid"**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Sicherheits-ID (SID), die den Benutzer, der einen Filter erstellt, eindeutig identifiziert. WMI speichert die SID des Benutzers, der eine Instanz von [**\_ \_ eventconsumer**](--eventconsumer.md) oder die Administrator-SID erstellt, je nach Betriebssystem. Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md) und über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.

Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.

</dd> <dt>

**Fromline**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aus Zeile einer e-Mail-Nachricht im Format einer Standard Zeichenfolgen-Vorlage. Wenn der Wert **null** ist, wird eine from-Zeile in der Form "Winmgmt@*MachineName*" erstellt.

</dd> <dt>

**Headerfields**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Header Feldern, die ohne Interpretation in eine e-Mail-Nachricht eingefügt werden.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Computers, an den Windows-Verwaltungsinstrumentation (WMI) Ereignisse sendet.

Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale Warteschlange für einen bestimmten Consumer in Bytes.

Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.

</dd> <dt>

**Meldung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Standard mäßige Zeichen folgen Vorlage, die den Textkörper einer e-Mail-Nachricht enthält.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](key-qualifier.md)
</dt> </dl>

Eindeutiger Bezeichner für den Ereignisconsumer.

</dd> <dt>

**Replytoline**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Antwort an Zeile einer e-Mail-Nachricht im Format einer Standard Zeichenfolgen-Vorlage. Wenn der Wert **null** ist, wird keine Antwort an Zeile verwendet.

</dd> <dt>

**SMTPServer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des SMTP-Servers, über den eine e-Mail gesendet wird. Zulässige Namen sind eine IP-Adresse oder ein DNS-oder NetBIOS-Name. Diese Eigenschaft darf nicht **null** sein.

</dd> <dt>

**Subject**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Standard Zeichen folgen Vorlage, die den Betreff einer e-Mail-Nachricht enthält.

</dd> <dt>

**Unter Toline**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Liste von Adressen, getrennt durch ein Komma oder Semikolon, im Format einer standardmäßigen Zeichen folgen Vorlage, die angibt, wohin die Nachricht gesendet werden soll. Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Klasse smtpeer-Consumer wird von der [**\_ \_ eventconsumer**](--eventconsumer.md) abstract-Klasse abgeleitet.

Einige der Eigenschaften **Toline**, **ccline** oder **bccline** können **null** sein, Sie können jedoch nicht alle **null** sein.

Der Empfang eines Fehlerrückgabe Codes vom SMTP-Dienst wird als Fehler betrachtet.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung von **smtpeer-Consumer** , um einen Consumer zu erstellen, finden Sie unter [Senden von e-Mails auf der Grundlage eines Ereignisses](sending-e-mail-based-on-an-event.md). Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Stamm \\ Abonnement<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Smtpcons. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Smtpcons.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Eventconsumer**](--eventconsumer.md)
</dt> <dt>

[Standard Consumer-Klassen](standard-consumer-classes.md)
</dt> <dt>

[Senden von e-Mails auf der Grundlage eines Ereignisses](sending-e-mail-based-on-an-event.md)
</dt> <dt>

[Erstellen eines logischen Consumers](creating-a-logical-consumer.md)
</dt> <dt>

[Empfangen von Ereignissen zu allen Zeitpunkten](receiving-events-at-all-times.md)
</dt> </dl>

 

 




