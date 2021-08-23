---
description: Die NTEventLogEventConsumer-Klasse protokolliert eine bestimmte Meldung im Betriebssystemereignisprotokoll, wenn ein Ereignis an das Ereignis übermittelt wird.
ms.assetid: cf986812-f09a-4f32-ba76-db76a23e2e4c
ms.tgt_platform: multiple
title: NTEventLogEventConsumer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NTEventLogEventConsumer
- NTEventLogEventConsumer.CreatorSID
- NTEventLogEventConsumer.MachineName
- NTEventLogEventConsumer.MaximumQueueSize
- NTEventLogEventConsumer.Category
- NTEventLogEventConsumer.NameOfRawDataProperty
- NTEventLogEventConsumer.EventID
- NTEventLogEventConsumer.EventType
- NTEventLogEventConsumer.InsertionStringTemplates
- NTEventLogEventConsumer.Name
- NTEventLogEventConsumer.NumberOfInsertionStrings
- NTEventLogEventConsumer.NameOfUserSidProperty
- NTEventLogEventConsumer.SourceName
- NTEventLogEventConsumer.UNCServerName
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: dfa2a1dcf15b65808af758820604df6aa62d7bc59d4e1c69e8d4d6e06b1d93a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555170"
---
# <a name="nteventlogeventconsumer-class"></a>NTEventLogEventConsumer-Klasse

Die **NTEventLogEventConsumer-Klasse** protokolliert eine bestimmte Meldung im Betriebssystemereignisprotokoll, wenn ein Ereignis an das Ereignis übermittelt wird. Diese Klasse ist einer der Standardereignis-Consumer, die WMI bereitstellt. Weitere Informationen finden Sie unter [Überwachen und Reagieren auf Ereignisse mit Standard-Consumern.](monitoring-and-responding-to-events-with-standard-consumers.md)

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class NTEventLogEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  uint16 Category;
  string NameOfRawDataProperty;
  uint32 EventID;
  uint32 EventType = 1;
  string InsertionStringTemplates[] = {""};
  string Name;
  uint32 NumberOfInsertionStrings = 0;
  string NameOfUserSidProperty;
  string SourceName;
  string UNCServerName;
};
```

## <a name="members"></a>Member

Die **NTEventLogEventConsumer-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **NTEventLogEventConsumer-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Kategorie**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ereigniskategorie. Dies sind quellspezifische Informationen, die einen beliebigen Wert aufweisen können.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Sicherheits-ID (SID), die den Benutzer eindeutig identifiziert, der einen Filter erstellt. WMI speichert die SID des Benutzers, der je nach Betriebssystem eine Instanz von [**\_ \_ EventConsumer**](--eventconsumer.md) erstellt, oder die Administrator-SID. Weitere Informationen finden Sie unter [Binden eines Ereignisfilters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md) und Überwachen und Reagieren auf Ereignisse mit [Standard-Consumern.](monitoring-and-responding-to-events-with-standard-consumers.md)

Diese Eigenschaft wird von [**\_ \_ EventConsumer**](--eventconsumer.md)geerbt.

</dd> <dt>

**EventID**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ereignismeldung in der Nachrichten-DLL. Diese Eigenschaft darf nicht **NULL** sein.

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ereignistyp. Dieser Parameter kann einen der in der folgenden Liste aufgeführten Werte enthalten, die in Winnt.h definiert sind.

<dt>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**EVENTLOG \_ SUCCESS** (0 (0x0))


</dt> <dd>

Erfolgreiches Ereignis

</dd> <dt>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**EVENTLOG \_ FEHLER \_ TPYE** (1 (0x1))


</dt> <dd>

Fehlerereignis

</dd> <dt>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**EVENTLOG \_ \_WARNUNGSTYP** (2 (0x2))


</dt> <dd>

Warnungsereignis

</dd> <dt>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**EVENTLOG \_ \_INFORMATIONSTYP** (4 (0x4))


</dt> <dd>

Informationsereignis

</dd> <dt>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**EVENTLOG \_ AUDIT \_ SUCCESS** (8 (0x8))


</dt> <dd>

Erfolgsüberwachungstyp

</dd> <dt>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**EVENTLOG \_ AUDIT \_ FAILURE** (16 (0x10))


</dt> <dd>

Fehlerüberwachungstyp

</dd> </dl>

</dd> <dt>

**InsertionStringTemplates**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array von Standardzeichenfolgenvorlagen, die als Einfügezeichenfolge für einen Ereignisprotokolldatensatz verwendet werden.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name des Computers, an den Windows Management Instrumentation (WMI) Ereignisse sendet.

Diese Eigenschaft wird von [**\_ \_ EventConsumer**](--eventconsumer.md)geerbt.

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale Warteschlange für einen bestimmten Consumer in Bytes.

Diese Eigenschaft wird von [**\_ \_ EventConsumer**](--eventconsumer.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](key-qualifier.md)
</dt> </dl>

Eindeutiger Name eines Consumers.

</dd> <dt>

**NameOfRawDataProperty**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name der Ereigniseigenschaft, die Daten enthält, die an den *LpRawData-Parameter* der [**ReportEvent-Funktion**](/windows/desktop/api/winbase/nf-winbase-reporteventa) übergeben werden sollen.

</dd> <dt>

**NameOfUserSidProperty**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name der Ereigniseigenschaft, die eine Sicherheits-ID (SID) enthält, die an den *LpUserSid-Parameter* der [**ReportEvent-Funktion**](/windows/desktop/api/winbase/nf-winbase-reporteventa) übergeben werden soll. Die -Eigenschaft muss entweder ein Bytearray (**uint8**) oder eine Zeichenfolge sein. Wenn es sich um ein Bytearray handelt, wird davon ausgegangen, dass es sich um eine SID handelt. Wenn es sich um eine Zeichenfolge handelt, handelt es sich um eine Zeichenfolgen-SID, die in eine SID konvertiert wird.

</dd> <dt>

**NumberOfInsertionStrings**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Elemente im **InsertionStringTemplates-Array.**

</dd> <dt>

**SourceName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Quellname, in dem sich eine Nachricht befindet. Es wird davon ausgegangen, dass der Kunde eine DLL mit den erforderlichen Nachrichten registriert hat.

> [!Note]  
> Der Wert dieses Parameters darf keinen Doppelpunkt enthalten (:) Charakter.

 

</dd> <dt>

**UNCServerName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Computers, auf dem ein Ereignis protokolliert werden soll, oder **NULL,** wenn das Ereignis auf einem lokalen Server protokolliert werden soll.

Authentifizierte Benutzer können standardmäßig keine Ereignisse im Anwendungsprotokoll auf einem Remotecomputer protokollieren. Daher funktioniert die Verwendung dieser Eigenschaft zum Angeben eines Remotecomputers nicht. Informationen zum Ändern der Sicherheit von Ereignisprotokollen finden Sie in diesem [KB-Artikel.](https://support.microsoft.com/kb/323076)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **NTEventLogEventConsumer-Klasse** wird von der [**\_ \_ abstrakten EventConsumer-Klasse**](--eventconsumer.md) abgeleitet.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung von **NTEventLogEventConsumer** zum Erstellen eines Consumers finden Sie unter [Protokollierung im NT-Ereignisprotokoll basierend auf einem Ereignis.](logging-to-nt-event-log-based-on-an-event.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stammabonnement<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Standard-Consumerklassen](standard-consumer-classes.md)
</dt> <dt>

[Erstellen eines logischen Consumers](creating-a-logical-consumer.md)
</dt> <dt>

[Jederzeites Empfangen von Ereignissen](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

