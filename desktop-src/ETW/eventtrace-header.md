---
description: Die Ereignistyp Klasse für das Header Ereignis der Protokolldatei. Diese Klasse enthält Informationen über die Ereignis Ablauf Verfolgungs Sitzung.
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
ms.openlocfilehash: dea803849d6aa15c2a3a14deb850d85ade569116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526864"
---
# <a name="eventtrace_header-class"></a>EventTrace- \_ Header Klasse

Die Ereignistyp Klasse für das Header Ereignis der Protokolldatei. Diese Klasse enthält Informationen über die Ereignis Ablauf Verfolgungs Sitzung.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **EventTrace- \_ Header** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **EventTrace- \_ Header** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**BootTime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (17)
</dt> </dl>

Der Zeitpunkt, zu dem das System gestartet wurde, in 100-Nanosekunden-Intervallen seit Mitternacht, 1. Januar 1601.

</dd> <dt>

**BufferSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (1)
</dt> </dl>

Größe der Puffer der Ereignis Ablauf Verfolgungs Sitzung in Kilobyte.

</dd> <dt>

**Bufferslost**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (21)
</dt> </dl>

Gesamtanzahl verlorener Puffer.

</dd> <dt>

**Bufferswritten**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (9)
</dt> </dl>

Die Gesamtanzahl der Puffer, die von der Ereignis Ablauf Verfolgungs Sitzung geschrieben wurden.

</dd> <dt>

**Cpuspeed**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (13)
</dt> </dl>

CPU-Geschwindigkeit in Megahertz.

**Windows 2000:** Nicht unterstützt.

</dd> <dt>

**EndTime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (5)
</dt> </dl>

Der Zeitpunkt, zu dem die Ereignis Ablauf Verfolgungs Sitzung beendet wurde (in 100-Nanosekunden-Intervallen seit Mitternacht, 1. Januar 1601). Dieser Wert kann 0 sein, wenn Sie Ereignisse in Echtzeit oder über eine Protokolldatei, für die die Bereitstellung weiterhin Ereignisse protokolliert, verbrauchen.

</dd> <dt>

**Eventslost**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (12)
</dt> </dl>

Anzahl von Ereignissen, die während der Ereignis Ablauf Verfolgungs Sitzung verloren gehen.

</dd> <dt>

**Logfilemode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (8), **Format ("x")**
</dt> </dl>

Aktueller Protokollierungs Modus für die Ereignis Ablauf Verfolgungs Sitzung. Eine Liste der Werte finden Sie unter Protokollierungs Modus-Konstanten.

</dd> <dt>

**Protokoll Dateiname**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (15), **Zeiger**
</dt> </dl>

Der Name der Ereignis Ablauf Verfolgungs Protokoll-Datei, die die Ereignisse enthält.

</dd> <dt>

**Loggername**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (14), **Zeiger**
</dt> </dl>

Name der Ereignis Ablauf Verfolgungs Sitzung.

</dd> <dt>

**MaxFileSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (7)
</dt> </dl>

Maximale Größe der Protokolldatei in Megabytes.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (4)
</dt> </dl>

Anzahl der Prozessoren im System.

</dd> <dt>

**PerfFreq**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (18)
</dt> </dl>

Häufigkeit des hochauflösenden Leistungs Zählers, falls vorhanden.

</dd> <dt>

**Pointersize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (11)
</dt> </dl>

Größe eines Zeiger Datentyps in Bytes.

</dd> <dt>

**ProviderVersion**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (3)
</dt> </dl>

Buildnummer des Betriebssystems.

</dd> <dt>

**Reservedflags**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (20)
</dt> </dl>

Reserviert.

</dd> <dt>

**Startbuffers**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (10)
</dt> </dl>

Reserviert.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (19)
</dt> </dl>

Der Zeitpunkt, zu dem die Ereignis Ablauf Verfolgungs Sitzung in 100-Nanosekunden-Intervallen seit Mitternacht, 1. Januar 1601, gestartet wurde.

</dd> <dt>

**TimerResolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (6)
</dt> </dl>

Auflösung des Hardware Zeit Gebers in Einheiten von 100 Nanosekunden.

</dd> <dt>

**TimeZoneInformation**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (16), **Extension ("noprint")**, **Max** (176)
</dt> </dl>

Eine [**Zeit \_ Zonen \_ Informations**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) Struktur, die die Zeitzone für die Member " **Boottime**", " **EndTime** " und " **StartTime** " enthält.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (2)
</dt> </dl>

Versionsnummer des Betriebssystems. Beginnend mit den nieder wertigen Bytes enthalten die ersten zwei Bytes die Hauptversion, die nächsten zwei Bytes enthalten eine neben Version, die nächsten zwei Bytes enthalten Service Pack Hauptversion, und die letzten zwei Bytes enthalten Service Pack neben Version.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Normalerweise möchten Sie die Werte für die folgenden Eigenschaften speichern, damit Sie später bei der Verarbeitung von Ereignissen aus der Protokolldatei verwendet werden können.

-   **Timerresolution**– verwenden Sie diese mit den **kerneltime** -und **usertime** -Membern der [**Ereignis Ablauf \_ Verfolgungs \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) -Struktur, um die CPU-Kosten für eine Reihe von Anweisungen zu ermitteln. Weitere Informationen finden Sie im Abschnitt "Hinweise" im [**Ereignis Ablauf \_ Verfolgungs \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).
-   **Pointersize**– verwenden Sie diesen Wert für Eigenschaften, die den **Zeiger** Qualifizierer enthalten, um die Größe des Zeigers zu bestimmen. Beachten Sie, dass dieser Wert möglicherweise nicht korrekt ist. Auf einem 64-Bit-Computer protokolliert z. b. eine 32-Bit-Anwendung 4-Byte-Zeiger. in der Sitzung wird jedoch " **pointersize** " auf 8 festgelegt.
-   **Logfilemode**– verwenden Sie, um zu bestimmen, ob diese Sitzung eine private Protokollierungs Sitzung ist. Es gibt einige Eigenschaften, die keine Daten für private Protokollierungs Sitzungen enthalten. Beispielsweise die **kerneltime** -und **usertime** -Member der [**Ereignis-Ablauf \_ Verfolgungs \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) -Struktur.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Eventtraceevent**](eventtraceevent.md)
</dt> <dt>

[**\_logfile-Header der Ablauf Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header)
</dt> </dl>

 

 
