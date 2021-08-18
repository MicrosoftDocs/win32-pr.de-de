---
description: Die LogFileEventConsumer-Klasse schreibt benutzerdefinierte Zeichenfolgen in eine Textdatei, wenn Ereignisse an sie übermittelt werden.
ms.assetid: 8934b60e-3763-4b85-89fd-58fe6136dff6
ms.tgt_platform: multiple
title: LogFileEventConsumer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogFileEventConsumer
- LogFileEventConsumer.CreatorSID
- LogFileEventConsumer.MachineName
- LogFileEventConsumer.MaximumQueueSize
- LogFileEventConsumer.Filename
- LogFileEventConsumer.IsUnicode
- LogFileEventConsumer.MaximumFileSize
- LogFileEventConsumer.Name
- LogFileEventConsumer.Text
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: dbcf0f90a8bca0cf1f648f74d1b58d7037b79fa8bc9d2d13c4fe2c6dc8306eba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996520"
---
# <a name="logfileeventconsumer-class"></a>LogFileEventConsumer-Klasse

Die **LogFileEventConsumer-Klasse** schreibt benutzerdefinierte Zeichenfolgen in eine Textdatei, wenn Ereignisse an sie übermittelt werden. Die Zeichenfolgen werden durch Zeilenendesequenzen getrennt. Diese Klasse ist einer der Standardereignis-Consumers, die WMI bietet. Weitere Informationen finden Sie unter [Überwachen und Reagieren auf Ereignisse mit Standardverbrauchern.](monitoring-and-responding-to-events-with-standard-consumers.md)

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class LogFileEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  Filename;
  boolean IsUnicode;
  uint64  MaximumFileSize = 65535;
  string  Name;
  string  Text;
};
```

## <a name="members"></a>Member

Die **LogFileEventConsumer-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **LogFileEventConsumer-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Sicherheits-ID (SID), die den Benutzer, der einen Filter erstellt, eindeutig identifiziert. WMI speichert je nach Betriebssystem die SID des Benutzers, der eine Instanz von [**\_ \_ EventConsumer**](--eventconsumer.md) oder die Administrator-SID erstellt. Weitere Informationen finden Sie unter [Binden eines Ereignisfilters](binding-an-event-filter-with-a-logical-consumer.md) mit einem logischen Consumer und Überwachen und Reagieren auf [Ereignisse mit Standardverbrauchern.](monitoring-and-responding-to-events-with-standard-consumers.md)

Diese Eigenschaft wird von [**\_ \_ EventConsumer geerbt.**](--eventconsumer.md)

</dd> <dt>

**Filename**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name einer Datei, die den Pfad enthält, an den die Protokolleinträge angefügt werden. Wenn die Datei nicht vorhanden ist, **versucht LogFileEventConsumer,** sie zu erstellen. Der Consumer schlägt fehl, wenn der Pfad nicht vorhanden ist oder wenn der Benutzer, der den Consumer erstellt, nicht über Schreibberechtigungen für die Datei oder den Pfad verfügt.

</dd> <dt>

**IsUnicode**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt an,** dass die Protokolldatei eine Unicode-Textdatei ist. False **gibt an,** dass die Protokolldatei eine Multibyte-Codetextdatei ist. Wenn die Datei vorhanden ist, wird diese Eigenschaft ignoriert, und die aktuelle Dateieinstellung wird verwendet. Wenn **IsUnicode** beispielsweise **FALSE** ist, die vorhandene Datei jedoch eine Unicode-Datei ist, wird Unicode verwendet. Wenn **IsUnicode** **TRUE ist,** die Datei jedoch Multibytecode ist, wird Multibytecode verwendet.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name des Computers, an den die Windows Management Instrumentation (WMI) Ereignisse sendet.

Diese Eigenschaft wird von [**\_ \_ EventConsumer geerbt.**](--eventconsumer.md)

</dd> <dt>

**MaximumFileSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale Größe einer Protokolldatei in Bytes. Wenn die primäre Datei ihre maximale Größe überschreitet, wird der Inhalt in eine andere Datei verschoben und die primäre Datei geleert. Der Wert 0 (null) bedeutet, dass keine Größenbeschränkung besteht. Der Standardwert ist 65.535 Bytes. Die Größe der Datei wird vor einem Schreibvorgang überprüft. Daher können Sie über eine Datei verfügen, die etwas größer als die angegebene Größenbeschränkung ist. Der nächste Schreibvorgang fängt es ab und startet eine neue Datei.

In der folgenden Liste ist die Namensstruktur für die Sicherungsdatei aufgeführt:

-   Wenn der ursprüngliche Dateiname 8.3 ist, wird die Erweiterung durch eine Zeichenfolge im Format "001", "002" und so weiter durch die kleinste Zahl ersetzt, die größer als alle zuvor verwendeten und ausgewählten Zahlen ist. Wenn "999" verwendet wird, ist die ausgewählte Zahl die kleinste nicht verwendete Zahl.
-   Wenn der ursprüngliche Dateiname nicht 8.3 ist, wird eine Zeichenfolge im Format "001", "002" und so weiter an den Dateinamen angefügt.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

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

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](key-qualifier.md)
</dt> </dl>

Eindeutiger Name für diesen Consumer.

</dd> <dt>

**Text**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

[Standardzeichenfolgenvorlage](using-standard-string-templates.md) für den Text eines Protokolleintrags.

</dd> </dl>

## <a name="remarks"></a>Hinweise

> [!Note]  
> **LogFileEventConsumer** sichert die Protokolldatei nicht. Daher ist es beim Konfigurieren von **LogFileEventConsumer** wichtig, ein Verzeichnis anzugeben, das auf der von Ihnen benötigten Ebene geschützt ist.

 

Die **LogFileEventConsumer-Klasse** wird von der abstrakten [**\_ \_ EventConsumer-Klasse**](--eventconsumer.md) abgeleitet.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung **von LogFileEventConsumer** zum Erstellen eines Consumers finden Sie unter Schreiben in eine Protokolldatei [basierend auf einem Ereignis.](writing-to-a-log-file-based-on-an-event.md)

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

[Schreiben in eine Protokolldatei basierend auf einem Ereignis](writing-to-a-log-file-based-on-an-event.md)
</dt> <dt>

[Erstellen eines logischen Consumers](creating-a-logical-consumer.md)
</dt> <dt>

[Jederzeites Empfangen von Ereignissen](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

