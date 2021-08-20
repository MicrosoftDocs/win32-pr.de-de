---
description: Die SMTPEventConsumer-Klasse sendet eine E-Mail mithilfe Simple Mail Transfer Protocol (SMTP) jedes Mal, wenn ein Ereignis an sie übermittelt wird.
ms.assetid: 42178360-9e22-4cd1-9b72-5f6b0d7e6c9c
ms.tgt_platform: multiple
title: SMTPEventConsumer-Klasse
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
ms.openlocfilehash: 4f216647f7ac6796c4b94157a261e535d9e2eb9cd98e02fd1f9cec5ac3dee95d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117922941"
---
# <a name="smtpeventconsumer-class"></a>SMTPEventConsumer-Klasse

Die **SMTPEventConsumer-Klasse** sendet eine E-Mail mithilfe Simple Mail Transfer Protocol (SMTP) jedes Mal, wenn ein Ereignis an sie übermittelt wird. Im Netzwerk muss ein SMTP-Server vorhanden sein. Die SMTPEventConsumer-Klasse unterstützt keine Anlagen. Die Codierung der E-Mail-Nachricht muss US-ASCII sein.

Diese Klasse ist einer der Standardereignis-Consumers, die WMI bietet. Ein Beispiel für die Verwendung von **SMTPEventConsumer** zum Erstellen eines Consumers finden Sie unter Senden von [E-Mails basierend auf einem Ereignis.](sending-e-mail-based-on-an-event.md) Weitere Informationen finden Sie unter [Überwachen und Reagieren auf Ereignisse mit Standardverbrauchern.](monitoring-and-responding-to-events-with-standard-consumers.md)

Die folgende Syntax wird durch Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

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

Die **SMTPEventConsumer-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SMTPEventConsumer-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BccLine**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine durch ein Komma oder Semikolon getrennte Liste von Adressen im Format einer Standardzeichenfolgenvorlage, an die die Nachricht als blinde Kopie gesendet wird. Weitere Informationen finden Sie im Abschnitt "Hinweise" dieses Themas.

</dd> <dt>

**CcLine**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Liste von Adressen, getrennt durch ein Komma oder Semikolon, im Format einer Standardzeichenfolgenvorlage, an die die Nachricht als Co-Kopie gesendet wird. Weitere Informationen finden Sie im Abschnitt "Hinweise" dieses Themas.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Sicherheits-ID (SID), die den Benutzer, der einen Filter erstellt, eindeutig identifiziert. WMI speichert je nach Betriebssystem die SID des Benutzers, der eine Instanz von [**\_ \_ EventConsumer**](--eventconsumer.md) oder die Administrator-SID erstellt. Weitere Informationen finden Sie unter [Binden eines Ereignisfilters](binding-an-event-filter-with-a-logical-consumer.md) mit einem logischen Consumer und Überwachen und Reagieren auf [Ereignisse mit Standardverbrauchern.](monitoring-and-responding-to-events-with-standard-consumers.md)

Diese Eigenschaft wird von [**\_ \_ EventConsumer geerbt.**](--eventconsumer.md)

</dd> <dt>

**FromLine**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aus der Zeile einer E-Mail im Format einer Standardzeichenfolgenvorlage. Wenn **NULL,** wird eine From-Zeile in Form von "WinMgmt@*MachineName"* erstellt.

</dd> <dt>

**HeaderFields**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array von Headerfeldern, die ohne Interpretation in eine E-Mail-Nachricht eingefügt werden.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name des Computers, an den die Windows Management Instrumentation (WMI) Ereignisse sendet.

Diese Eigenschaft wird von [**\_ \_ EventConsumer geerbt.**](--eventconsumer.md)

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale Warteschlange für einen bestimmten Consumer in Bytes.

Diese Eigenschaft wird von [**\_ \_ EventConsumer geerbt.**](--eventconsumer.md)

</dd> <dt>

**Meldung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Standardzeichenfolgenvorlage, die den Text einer E-Mail-Nachricht enthält.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](key-qualifier.md)
</dt> </dl>

Eindeutiger Bezeichner für den Ereignisverbraucher.

</dd> <dt>

**ReplyToLine**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Antwortzeile einer E-Mail-Nachricht im Format einer Standardzeichenfolgenvorlage. Wenn **NULL,** wird keine Antwortzeile verwendet.

</dd> <dt>

**SMTPServer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name des SMTP-Servers, über den eine E-Mail gesendet wird. Zulässige Namen sind eine IP-Adresse oder ein DNS- oder NetBIOS-Name. Diese Eigenschaft darf nicht **NULL sein.**

</dd> <dt>

**Subject**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Standardzeichenfolgenvorlage, die den Betreff einer E-Mail enthält.

</dd> <dt>

**ToLine**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine durch ein Komma oder Semikolon getrennte Liste von Adressen im Format einer Standardzeichenfolgenvorlage, die angibt, wohin die Nachricht gesendet werden soll. Weitere Informationen finden Sie im Abschnitt "Hinweise" dieses Themas.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die SMTPEventConsumer-Klasse wird von der abstrakten [**\_ \_ EventConsumer-Klasse**](--eventconsumer.md) abgeleitet.

Einige der **ToLine-,** **CcLine-** oder **BccLine-Eigenschaften** können **NULL** sein, aber sie können nicht alle **NULL sein.**

Das Empfangen eines Fehler-Rückgabecodes vom SMTP-Dienst wird als Fehler betrachtet.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung von **SMTPEventConsumer** zum Erstellen eines Consumers finden Sie unter Senden von [E-Mails basierend auf einem Ereignis.](sending-e-mail-based-on-an-event.md) Weitere Informationen finden Sie unter [Überwachen und Reagieren auf Ereignisse mit Standardverbrauchern.](monitoring-and-responding-to-events-with-standard-consumers.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stammabonnement<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Smtpcons.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Smtpcons.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> <dt>

[Standard-Consumerklassen](standard-consumer-classes.md)
</dt> <dt>

[Senden von E-Mails basierend auf einem Ereignis](sending-e-mail-based-on-an-event.md)
</dt> <dt>

[Erstellen eines logischen Consumers](creating-a-logical-consumer.md)
</dt> <dt>

[Empfangen von Ereignissen zu jedem Zeitpunkt](receiving-events-at-all-times.md)
</dt> </dl>

 

 




