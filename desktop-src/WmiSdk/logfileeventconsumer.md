---
description: Die logfileeventconsumer-Klasse schreibt angepasste Zeichen folgen in eine Text Protokolldatei, wenn Ereignisse an Sie übermittelt werden.
ms.assetid: 8934b60e-3763-4b85-89fd-58fe6136dff6
ms.tgt_platform: multiple
title: Logfileeventconsumer-Klasse
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
ms.openlocfilehash: 462989b740aaf6a6bd78968c951b7c676038cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348915"
---
# <a name="logfileeventconsumer-class"></a>Logfileeventconsumer-Klasse

Die **logfileeventconsumer** -Klasse schreibt angepasste Zeichen folgen in eine Text Protokolldatei, wenn Ereignisse an Sie übermittelt werden. Die Zeichen folgen werden durch zeilige Zeilen voneinander getrennt. Diese Klasse ist einer der standardereignisconsumer, die von WMI bereitstellt werden. Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.

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

Die **logfileeventconsumer** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **logfileeventconsumer** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**"Kreatorsid"**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Sicherheits-ID (SID), die den Benutzer, der einen Filter erstellt, eindeutig identifiziert. WMI speichert die SID des Benutzers, der eine Instanz von [**\_ \_ eventconsumer**](--eventconsumer.md) oder die Administrator-SID erstellt, je nach Betriebssystem. Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md) und über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.

Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.

</dd> <dt>

**Filename**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name einer Datei, die den Pfad enthält, an den die Protokolleinträge angehängt werden. Wenn die Datei nicht vorhanden ist, versucht **logfileeventconsumer** , Sie zu erstellen. Der Consumer schlägt fehl, wenn der Pfad nicht vorhanden ist oder wenn der Benutzer, der den Consumer erstellt, nicht über Schreibberechtigungen für die Datei oder den Pfad verfügt.

</dd> <dt>

**Isunicode**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass die Protokolldatei eine Unicode-Textdatei ist. Wenn der Wert **false** ist, ist die Protokolldatei eine Multibytezeichen-Code Textdatei. Wenn die Datei vorhanden ist, wird diese Eigenschaft ignoriert, und die aktuelle Datei Einstellung wird verwendet. Wenn **isunicode** beispielsweise **false** ist, die vorhandene Datei jedoch eine Unicode-Datei ist, wird Unicode verwendet. Wenn **isunicode** **true** ist, aber die Datei multibytecode ist, wird multibytecode verwendet.

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

**MaximumFileSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale Größe einer Protokolldatei in Bytes. Wenn die primäre Datei die maximale Größe überschreitet, wird der Inhalt in eine andere Datei verschoben, und die primäre Datei wird geleert. Der Wert 0 (null) bedeutet, dass es keine Größenbeschränkung gibt. Der Standardwert ist 65.535 bytes. Die Größe der Datei wird vor einem Schreibvorgang geprüft. Daher können Sie eine Datei haben, die etwas größer als die angegebene Größenbeschränkung ist. Beim nächsten Schreibvorgang wird die Datei abgefangen und eine neue Datei gestartet.

In der folgenden Liste ist die Benennungs Struktur für die Sicherungsdatei angegeben:

-   Wenn der ursprüngliche Dateiname 8,3 ist, wird die Erweiterung durch eine Zeichenfolge im Format "001", "002" usw. ersetzt, wobei die kleinste Zahl größer als alle zuvor verwendeten und ausgewählten Zahlen ist. Wenn "999" verwendet wird, ist die ausgewählte Zahl die kleinste nicht verwendete Zahl.
-   Wenn der ursprüngliche Dateiname nicht 8,3 ist, wird eine Zeichenfolge im Format "001", "002" usw. an den Dateinamen angehängt.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

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

Eindeutiger Name für diesen Consumer.

</dd> <dt>

**Text**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Standard Zeichen folgen [Vorlage](using-standard-string-templates.md) für den Text eines Protokoll Eintrags.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Protokolldatei wird von **logfileeventconsumer** nicht gesichert. Wenn Sie **logfileeventconsumer** konfigurieren, ist es daher wichtig, ein Verzeichnis anzugeben, das auf der gewünschten Ebene gesichert ist.

 

Die **logfileeventconsumer** -Klasse wird von der [**\_ \_ eventconsumer**](--eventconsumer.md) abstract-Klasse abgeleitet.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung von **logfileeventconsumer** , um einen Consumer zu erstellen, finden Sie unter [Schreiben in eine Protokolldatei auf Grundlage eines Ereignisses](writing-to-a-log-file-based-on-an-event.md).

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

[Schreiben in eine Protokolldatei auf Grundlage eines Ereignisses](writing-to-a-log-file-based-on-an-event.md)
</dt> <dt>

[Erstellen eines logischen Consumers](creating-a-logical-consumer.md)
</dt> <dt>

[Empfangen von Ereignissen zu allen Zeitpunkten](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_Eventconsumer**](--eventconsumer.md)
</dt> </dl>

 

