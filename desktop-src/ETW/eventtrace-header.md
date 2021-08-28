---
description: Die Ereignistypklasse für das Protokolldateiheaderereignis. Diese Klasse enthält Informationen zur Ereignisablaufverfolgungssitzung.
ms.assetid: 3d0c4044-da06-4850-95c4-99b4ea28fcd9
title: EventTrace_Header-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace_Header
- EventTrace_Header.BufferSize
- EventTrace_Header.Version
- EventTrace_Header.ProviderVersion
- EventTrace_Header.NumberOfProcessors
- EventTrace_Header.EndTime
- EventTrace_Header.TimerResolution
- EventTrace_Header.MaxFileSize
- EventTrace_Header.LogFileMode
- EventTrace_Header.BuffersWritten
- EventTrace_Header.StartBuffers
- EventTrace_Header.PointerSize
- EventTrace_Header.EventsLost
- EventTrace_Header.CPUSpeed
- EventTrace_Header.LoggerName
- EventTrace_Header.LogFileName
- EventTrace_Header.TimeZoneInformation
- EventTrace_Header.BootTime
- EventTrace_Header.PerfFreq
- EventTrace_Header.StartTime
- EventTrace_Header.ReservedFlags
- EventTrace_Header.BuffersLost
api_type:
- NA
api_location: ''
ms.openlocfilehash: a5d0515b9d7d720409e0a72aec7aad5dc54561637563976a35d03b3e0dec79f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829990"
---
# <a name="eventtrace_header-class"></a>EventTrace \_ Header-Klasse

Die Ereignistypklasse für das Protokolldateiheaderereignis. Diese Klasse enthält Informationen zur Ereignisablaufverfolgungssitzung.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(0)]
class EventTrace_Header : EventTraceEvent
{
  uint32 BufferSize;
  uint32 Version;
  uint32 ProviderVersion;
  uint32 NumberOfProcessors;
  uint64 EndTime;
  uint32 TimerResolution;
  uint32 MaxFileSize;
  uint32 LogFileMode;
  uint32 BuffersWritten;
  uint32 StartBuffers;
  uint32 PointerSize;
  uint32 EventsLost;
  uint32 CPUSpeed;
  uint32 LoggerName;
  uint32 LogFileName;
  uint8  TimeZoneInformation[];
  uint64 BootTime;
  uint64 PerfFreq;
  uint64 StartTime;
  uint32 ReservedFlags;
  uint32 BuffersLost;
};
```

## <a name="members"></a>Member

Die **EventTrace \_ Header-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **EventTrace \_ Header-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BootTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (17)
</dt> </dl>

Zeitpunkt des Systemstarts in Intervallen von 100 Nanosekunden seit Mitternacht, 1. Januar 1601.

</dd> <dt>

**BufferSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (1)
</dt> </dl>

Größe der Puffer der Ereignisablaufverfolgungssitzung in Kilobyte.

</dd> <dt>

**BuffersLost**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (21)
</dt> </dl>

Gesamtanzahl der verloren gegangenen Puffer.

</dd> <dt>

**BuffersWritten**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (9)
</dt> </dl>

Gesamtanzahl von Puffern, die von der Ereignisablaufverfolgungssitzung geschrieben wurden.

</dd> <dt>

**CPUSpeed**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (13)
</dt> </dl>

CPU-Geschwindigkeit in Megahertz.

**Windows 2000:** Wird nicht unterstützt.

</dd> <dt>

**EndTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (5)
</dt> </dl>

Zeitpunkt, zu dem die Ereignisablaufverfolgungssitzung beendet wurde, in Intervallen von 100 Nanosekunden seit Mitternacht, 1. Januar 1601. Dieser Wert kann 0 sein, wenn Sie Ereignisse in Echtzeit oder aus einer Protokolldatei nutzen, in der die Bereitstellung weiterhin Ereignisse protokolliert.

</dd> <dt>

**EventsLost**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (12)
</dt> </dl>

Anzahl der während der Ereignisablaufverfolgungssitzung verloren gegangenen Ereignisse.

</dd> <dt>

**LogFileMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (8), **Format("x")**
</dt> </dl>

Aktueller Protokollierungsmodus für die Ereignisablaufverfolgungssitzung. Eine Liste der Werte finden Sie unter Protokollierungsmoduskonstanten.

</dd> <dt>

**LogFileName**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (15), **Zeiger**
</dt> </dl>

Name der Protokolldatei für die Ereignisablaufverfolgung, die die Ereignisse enthält.

</dd> <dt>

**LoggerName**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (14), **Zeiger**
</dt> </dl>

Name der Ereignisablaufverfolgungssitzung.

</dd> <dt>

**MaxFileSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (7)
</dt> </dl>

Maximale Größe der Protokolldatei in Megabyte.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (4)
</dt> </dl>

Anzahl der Prozessoren im System.

</dd> <dt>

**PerfFreq**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (18)
</dt> </dl>

Häufigkeit des Leistungsindikators mit hoher Auflösung, sofern vorhanden.

</dd> <dt>

**PointerSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (11)
</dt> </dl>

Größe eines Zeigerdatentyps in Bytes.

</dd> <dt>

**ProviderVersion**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (3)
</dt> </dl>

Buildnummer des Betriebssystems.

</dd> <dt>

**ReservedFlags**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (20)
</dt> </dl>

Reserviert.

</dd> <dt>

**StartBuffers**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (10)
</dt> </dl>

Reserviert.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (19)
</dt> </dl>

Zeitpunkt, zu dem die Ereignisablaufverfolgungssitzung gestartet wurde, in Intervallen von 100 Nanosekunden seit Mitternacht, 1. Januar 1601.

</dd> <dt>

**TimerResolution**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (6)
</dt> </dl>

Auflösung des Hardwarezeiters in Einheiten von 100 Nanosekunden.

</dd> <dt>

**TimeZoneInformation**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (16), **Extension("NoPrint")**, **Max** (176)
</dt> </dl>

Eine [**TIME \_ ZONE \_ INFORMATION-Struktur,**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) die die Zeitzone für die **Elemente BootTime,** **EndTime** und **StartTime** enthält.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (2)
</dt> </dl>

Versionsnummer des Betriebssystems. Beginnend mit den niedrigen Bytes enthalten die ersten beiden Bytes die Hauptversion, die nächsten zwei Bytes eine Nebenversion, die nächsten zwei Bytes enthalten die Service Pack-Hauptversion und die letzten beiden Bytes die Service Pack-Nebenversion.

</dd> </dl>

## <a name="remarks"></a>Hinweise

In der Regel möchten Sie die Werte für die folgenden Eigenschaften zur späteren Verwendung bei der Verarbeitung von Ereignissen aus der Protokolldatei speichern.

-   **TimerResolution :** Verwenden Sie mit den **KernelTime-** und **UserTime-Membern** der [**EVENT TRACE \_ \_ HEADER-Struktur,**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) um die CPU-Kosten für eine Reihe von Anweisungen zu bestimmen. Weitere Informationen finden Sie im Abschnitt "Hinweise" von [**EVENT \_ TRACE \_ HEADER.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)
-   **PointerSize :** Verwenden Sie diesen Wert für Eigenschaften, die den **Zeigerqualifizierer** enthalten, um die Größe des Zeigers zu bestimmen. Beachten Sie, dass dieser Wert möglicherweise nicht genau ist. Beispielsweise protokolliert eine 32-Bit-Anwendung auf einem 64-Bit-Computer 4-Byte-Zeiger. Die Sitzung setzt jedoch **PointerSize auf** 8.
-   **LogFileMode :** Verwenden Sie , um zu bestimmen, ob es sich bei dieser Sitzung um eine private Protokollierungssitzung handelt. Es gibt einige Eigenschaften, die keine Daten für private Protokollierungssitzungen enthalten. Beispielsweise die **KernelTime- und** **UserTime-Member** der [**EVENT TRACE \_ \_ HEADER-Struktur.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EventTraceEvent**](eventtraceevent.md)
</dt> <dt>

[**TRACE \_ LOGFILE \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header)
</dt> </dl>

 

 
