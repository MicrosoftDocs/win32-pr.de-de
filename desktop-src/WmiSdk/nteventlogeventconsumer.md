---
description: Die nteventlogeventconsumer-Klasse protokolliert eine bestimmte Nachricht im Ereignisprotokoll des Betriebssystems, wenn ihr ein Ereignis zugestellt wird.
ms.assetid: cf986812-f09a-4f32-ba76-db76a23e2e4c
ms.tgt_platform: multiple
title: Nteventlogeventconsumer-Klasse
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
ms.openlocfilehash: e98948688b0fee37316102b2c37039de1c139310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863323"
---
# <a name="nteventlogeventconsumer-class"></a>Nteventlogeventconsumer-Klasse

Die **nteventlogeventconsumer** -Klasse protokolliert eine bestimmte Nachricht im Ereignisprotokoll des Betriebssystems, wenn ihr ein Ereignis zugestellt wird. Diese Klasse ist einer der standardereignisconsumer, die von WMI bereitstellt werden. Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.

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

Die **nteventlogeventconsumer** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **nteventlogeventconsumer** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Kategorie**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ereignis Kategorie. Dies sind Quell spezifische Informationen, die einen beliebigen Wert aufweisen können.

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

**EventID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ereignismeldung in der Nachrichten-dll. Diese Eigenschaft darf nicht **null** sein.

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ereignistyp. Dieser Parameter kann einen der in der folgenden Liste aufgeführten Werte aufweisen, die in "Winnt. h" definiert sind.

<dt>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**Ereignisprotokoll \_ Erfolg** (0 (0x0))


</dt> <dd>

Erfolgreiches Ereignis

</dd> <dt>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**Ereignisprotokoll \_ Fehler- \_ Tpye** (1 (0x1))


</dt> <dd>

Fehler Ereignis

</dd> <dt>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**Ereignisprotokoll \_ \_Warnungstyp** (2 (0x2))


</dt> <dd>

Warnungs Ereignis

</dd> <dt>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**Ereignisprotokoll \_ \_Informationstyp** (4 (0x4))


</dt> <dd>

Informations Ereignis

</dd> <dt>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**Ereignisprotokoll \_ Überwachen \_ erfolgreich** (8 (0x8))


</dt> <dd>

Erfolgreicher Überwachungstyp

</dd> <dt>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**Ereignisprotokoll \_ Überwachungs \_ Fehler** (16 (0x10))


</dt> <dd>

Fehler Überwachungstyp

</dd> </dl>

</dd> <dt>

**Insertionstringtemplates**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array von standardmäßigen Zeichen folgen Vorlagen, die als Einfügezeichenfolge für einen Ereignisprotokoll Daten Satz verwendet werden.

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

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](key-qualifier.md)
</dt> </dl>

Der eindeutige Name eines Consumers.

</dd> <dt>

**Nameofrawdataproperty**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Ereignis Eigenschaft, die Daten enthält, die an die Report [**Event**](/windows/desktop/api/winbase/nf-winbase-reporteventa) -Funktion des *lprawdata* -Parameters übergeben werden.

</dd> <dt>

**NameOfUserSIDProperty**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Ereignis Eigenschaft, die eine Sicherheits-ID (SID) enthält, die an den "Report [**Event**](/windows/desktop/api/winbase/nf-winbase-reporteventa) "-Funktion- *lpusersid* -Parameter übergeben werden soll. Die-Eigenschaft muss entweder ein Bytearray (**Uint8**) oder eine Zeichenfolge sein. Wenn es sich um ein Bytearray handelt, wird davon ausgegangen, dass es sich um eine SID handelt. Wenn es sich um eine Zeichenfolge handelt, ist es eine Zeichen folgen-sid, die in eine SID konvertiert wird.

</dd> <dt>

**"Numofinsertionstrings"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Elemente im **insertionstringtemplates** -Array.

</dd> <dt>

**SourceName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Quelle, in der sich eine Nachricht befindet. Es wird davon ausgegangen, dass der Kunde eine DLL mit den erforderlichen Nachrichten registriert hat.

> [!Note]  
> Der Wert dieses Parameters darf keinen Doppelpunkt enthalten (:) Art.

 

</dd> <dt>

**Uncservername**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Computers, auf dem ein Ereignis protokolliert werden soll, oder **null** , wenn das Ereignis auf einem lokalen Server protokolliert werden soll.

Authentifizierte Benutzer können Ereignisse standardmäßig nicht im Anwendungsprotokoll auf einem Remote Computer protokollieren. Daher funktioniert die Verwendung dieser Eigenschaft zum Angeben eines Remote Computers nicht. Weitere Informationen zum Ändern der Ereignisprotokoll Sicherheit finden Sie in diesem [KB-Artikel](https://support.microsoft.com/kb/323076).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **nteventlogeventconsumer** -Klasse wird von der [**\_ \_ eventconsumer**](--eventconsumer.md) abstract-Klasse abgeleitet.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung von **nteventlogeventconsumer** , um einen Consumer zu erstellen, finden Sie unter [Protokollieren in NT-Ereignisprotokoll basierend auf einem Ereignis](logging-to-nt-event-log-based-on-an-event.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Stamm \\ Abonnement<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Standard Consumer-Klassen](standard-consumer-classes.md)
</dt> <dt>

[Erstellen eines logischen Consumers](creating-a-logical-consumer.md)
</dt> <dt>

[Empfangen von Ereignissen zu allen Zeitpunkten](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_Eventconsumer**](--eventconsumer.md)
</dt> </dl>

 

