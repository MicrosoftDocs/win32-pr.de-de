---
description: Die WNODE \_ HEADER-Struktur ist ein Member der EVENT \_ TRACE \_ PROPERTIES-Struktur.
ms.assetid: 862a8f46-a326-48c6-92b7-8bb667837bb7
title: WNODE_HEADER-Struktur (Wmistr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WNODE_HEADER
api_type:
- HeaderDef
api_location:
- Wmistr.h
ms.openlocfilehash: e8ad8bd5e1fd4917fa031e7553ed0e7e460244b8ab7c7da347a62d7430036cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015238"
---
# <a name="wnode_header-structure"></a>WNODE \_ HEADER-Struktur

Die **WNODE \_ HEADER-Struktur** ist ein Member der [**EVENT TRACE \_ \_ PROPERTIES-Struktur.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)

## <a name="syntax"></a>Syntax


```C++
typedef struct _WNODE_HEADER {
  ULONG BufferSize;
  ULONG ProviderId;
  union {
    ULONG64 HistoricalContext;
    struct {
      ULONG Version;
      ULONG Linkage;
    };
  };
  union {
    HANDLE        KernelHandle;
    LARGE_INTEGER TimeStamp;
  };
  GUID  Guid;
  ULONG ClientContext;
  ULONG Flags;
} WNODE_HEADER, *PWNODE_HEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**BufferSize**
</dt> <dd>

Gesamtgröße des zugeordneten Arbeitsspeichers in Bytes für die Eigenschaften der Ereignisablaufverfolgungssitzung. Die Größe des Arbeitsspeichers muss den Raum für die [**EVENT \_ TRACE \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) sowie die Sitzungsnamenszeichenfolge und die Protokolldateinamenzeichenfolge enthalten, die der Struktur im Arbeitsspeicher folgen.

</dd> <dt>

**ProviderId**
</dt> <dd>

Für die interne Verwendung reserviert.

</dd> <dt>

**HistoricalContext**
</dt> <dd>

Bei der Ausgabe das Handle für die Ereignisablaufverfolgungssitzung.

</dd> <dt>

**Version**
</dt> <dd>

Für die interne Verwendung reserviert.

</dd> <dt>

**Verknüpfung**
</dt> <dd>

Für die interne Verwendung reserviert.

</dd> <dt>

**KernelHandle**
</dt> <dd>

Für die interne Verwendung reserviert.

</dd> <dt>

**Timestamp**
</dt> <dd>

Zeitpunkt der Aktualisierung der Informationen in dieser Struktur in Intervallen von 100 Nanosekunden seit Mitternacht, 1. Januar 1601.

</dd> <dt>

**Guid**
</dt> <dd>

Die GUID, die Sie für die Sitzung definieren.

Legen Sie für eine NT-Kernelprotokollierungssitzung diesen Member auf **SystemTraceControlGuid fest.**

Wenn dieser Member auf **SystemTraceControlGuid** oder **GlobalLoggerGuid** festgelegt ist, ist die Protokollierung eine Systemprotokollierung.

Legen Sie für eine private Protokollierungssitzung diesen Member auf die GUID des Anbieters fest, die Sie für die Sitzung aktivieren möchten.

Wenn Sie eine Sitzung starten, die keine Kernelprotokollierungs- oder private Protokollierungssitzung ist, müssen Sie keine Sitzungs-GUID angeben. Wenn Sie keine GUID angeben, erstellt ETW eine für Sie. Sie müssen eine Sitzungs-GUID nur angeben, wenn Sie die Einer bestimmten Sitzung zugeordneten Standardberechtigungen ändern möchten. Weitere Informationen finden Sie in der EventAccessControl-Funktion.

Sie können nicht mehr als eine Sitzung mit derselben Sitzungs-GUID starten.

**Vor Windows Vista:** Sie können mehrere Sitzungen mit der gleichen Sitzungs-GUID starten.

</dd> <dt>

**ClientContext**
</dt> <dd>

Die Uhrauflösung, die beim Protokollieren des Zeitstempels für jedes Ereignis verwendet werden soll. Der Standardwert ist Abfrageleistungsindikator (Query Performance Counter, QPC).

**Vor Windows Vista:** Der Standardwert ist die Systemzeit.

**Vor Windows 10 Version 1703:** Nicht mehr als zwei verschiedene Uhrtypen können gleichzeitig von allen Systemprotokollierungen verwendet werden.

**Ab Windows 10 Version 1703:** Die Einschränkung des Uhrtyps wurde entfernt. Alle drei Uhrtypen können jetzt gleichzeitig von Systemprotokollierungen verwendet werden.

Sie können einen der folgenden Werte angeben.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt>1</dt> </dl></td>
<td>Abfrageleistungsindikator (QPC). Der QPC-Indikator stellt einen zeitstempel mit hoher Auflösung bereit, der von Anpassungen der Systemuhr nicht betroffen ist. Der im Ereignis gespeicherte Zeitstempel entspricht dem Wert, der von der QueryPerformanceCounter-API zurückgegeben wird. Weitere Informationen zu den Merkmalen dieses Zeitstempels finden Sie unter Abrufen von <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">Zeitstempeln</a>mit hoher Auflösung.<br/> Sie sollten diese Auflösung verwenden, wenn Sie über hohe Ereignisraten verfügen oder wenn der Consumer Ereignisse aus verschiedenen Puffern zusammenführt. In diesen Fällen ermöglicht die Genauigkeit und Stabilität des QPC-Zeitstempels eine bessere Genauigkeit bei der Reihenfolge der Ereignisse aus verschiedenen Puffern. Der QPC-Zeitstempel spiegelt jedoch keine Aktualisierungen der Systemuhr wider, z. B. wenn die Systemuhr aufgrund der Synchronisierung mit einem NTP-Server während der Ablaufverfolgung vorwärts angepasst wird, spiegeln die QPC-Zeitstempel in der Ablaufverfolgung weiterhin die Zeit wider, als ob kein Update stattgefunden hätte.<br/> Um die Auflösung zu bestimmen, verwenden Sie das <strong>PerfFreq-Element</strong> von <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> beim Nutzen des Ereignisses.<br/> Verwenden Sie die folgende Konvertierungsformel, um den Zeitstempel eines Ereignisses in 100-ns-Einheiten zu konvertieren: <br/> scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart * 10000000.0 / logfileHeader.PerfFreq.QuadPart<br/> Beachten Sie, dass der Zeitstempel auf älteren Computern möglicherweise nicht genau ist, da der Leistungsindikator aufgrund von Hardwarefehlern manchmal übersprungen wird.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>2</dt> </dl></td>
<td>Systemzeit. Die Systemzeit stellt einen Zeitstempel bereit, der Änderungen an der Systemuhr nachverfolgt. Wenn die Systemuhr z. B. aufgrund der Synchronisierung mit einem NTP-Server vorwärts angepasst wird, während die Ablaufverfolgung ausgeführt wird, springen die Systemzeitstempel in der Ablaufverfolgung ebenfalls vorwärts, um der neuen Einstellung der Systemuhr zu entsprechen. <br/>
<ul>
<li>Auf Systemen vor Windows 10 entspricht der im Ereignis gespeicherte Zeitstempel dem Wert, der von der GetSystemTimeAsFileTime-API zurückgegeben wird.</li>
<li>Bei Windows 10 oder höher entspricht der im Ereignis gespeicherte Zeitstempel dem Wert, der von der GetSystemTimePreciseAsFileTime-API zurückgegeben wird.</li>
</ul>
Vor Windows 10 war die Auflösung dieses Zeitstempels die Auflösung eines Systemtakt-Ticks, wie durch den TimerResolution-Member von TRACE_LOGFILE_HEADER angegeben. Ab Windows 10 ist die Auflösung dieses Zeitstempels die Auflösung des Leistungsindikators, wie durch das PerfFreq-Element von TRACE_LOGFILE_HEADER angegeben.<br/> Verwenden Sie die folgende Konvertierungsformel, um den Zeitstempel eines Ereignisses in 100-ns-Einheiten zu konvertieren: <br/> scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart<br/> Beachten Sie Folgendes: Wenn Ereignisse auf einem System erfasst werden, auf dem ein Betriebssystem vor Windows 10 ausgeführt wird, ist die Auflösung für die Systemzeit bei hoher Ereignismenge möglicherweise nicht ausreichend, um die Reihenfolge der Ereignisse zu bestimmen. In diesem Fall hat eine Gruppe von Ereignissen den gleichen Zeitstempel, aber die Reihenfolge, in der ETW die Ereignisse übermittelt, ist möglicherweise nicht richtig. Ab Windows 10 wird der Zeitstempel mit zusätzlicher Genauigkeit erfasst, obwohl in Fällen, in denen die Systemuhr während der Erfassung der Ablaufverfolgung angepasst wurde, eine gewisse Instabilität auftreten kann.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>3</dt> </dl></td>
<td>CPU-Zykluszähler. Der CPU-Indikator bietet den höchsten Auflösungszeitstempel und ist der am wenigsten ressourcenintensive abzurufende. Der CPU-Indikator ist jedoch unzuverlässig und sollte nicht in der Produktion verwendet werden. Auf einigen Computern ändern sich die Zeitgeber z. B. aufgrund von Wärme- und Stromänderungen sowie aufgrund von Unterbrechungen in einigen Zuständen.<br/> Um die Auflösung zu bestimmen, verwenden Sie den <strong>CpuSpeedInMHz-Member</strong> von <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> beim Nutzen des Ereignisses.<br/> Wenn Ihre Hardware diesen Uhrtyp nicht unterstützt, verwendet ETW die Systemzeit.<br/> <strong>Windows Server 2003 Windows XP mit SP1 und Windows XP:</strong> Dieser Wert wird nicht unterstützt. Er wurde in Windows Server 2003 mit SP1 und Windows XP mit SP2 eingeführt.<br/></td>
</tr>
</tbody>
</table>



 

**Windows 2000:** Der **ClientContext-Member** wird nicht unterstützt.

</dd> <dt>

**Flags**
</dt> <dd>

Muss **WNODE \_ FLAG \_ TRACED \_ GUID** enthalten, um anzugeben, dass die Struktur Ereignisablaufverfolgungsinformationen enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Stellen Sie sicher, dass Sie den Arbeitsspeicher für diese Struktur auf 0 (null) initialisieren, bevor Sie Member festlegen.

Um einen ETW-Zeitstempel in filetime zu konvertieren, verwenden Sie das folgende Verfahren:

<dl> 1. Überprüfen Sie für jede Sitzung oder Protokolldatei, die verarbeitet wird (d. h. für jede EVENT \_ TRACE \_ LOGFILE), das Feld logFile.ProcessTraceMode, um zu bestimmen, ob das FLAG PROCESS \_ TRACE MODE RAW \_ \_ \_ TIMESTAMP festgelegt ist. Standardmäßig ist dieses Flag nicht festgelegt. Wenn dieses Flag nicht festgelegt ist, konvertiert die ETW-Runtime den Zeitstempel jedes \_ EREIGNISDATENSATZES automatisch in filetime, bevor der \_ EREIGNISDATENSATZ an Ihre EventRecordCallback-Funktion gesendet wird, sodass keine zusätzliche Verarbeitung erforderlich ist. Die folgenden Schritte sollten nur verwendet werden, wenn die Ablaufverfolgung mit festgelegtem \_ \_ \_ TIMESTAMP-Flag PROCESS TRACE MODE RAW verarbeitet \_ wird.  
2. Überprüfen Sie für jede Sitzung oder Protokolldatei, die verarbeitet wird (d. h. für jede EVENT \_ TRACE \_ LOGFILE), das Feld logFile.LogfileHeader.ReservedFlags, um die Zeitstempelskala für die Protokolldatei zu bestimmen. Führen Sie basierend auf dem Wert von ReservedFlags einen der folgenden Schritte aus, um den Für timeStampScale in den verbleibenden Schritten zu verwendenden Wert zu bestimmen: <dl> a. If ReservedFlags == 1 (QPC): DOUBLE timeStampScale = 10000000.0 / logFile.LogfileHeader.PerfFreq.QuadPart;  
b. If ReservedFlags == 2 (Systemzeit): DOUBLE timeStampScale = 1,0;  
Beachten Sie, dass die verbleibenden Schritte für Ereignisse, die Systemzeit verwenden, nicht erforderlich sind, da die Ereignisse bereits ihre Zeitstempel in FILETIME-Einheiten bereitstellen. Die verbleibenden Schritte funktionieren, sind jedoch unnötig und führen zu einem kleinen Rundungsfehler.  
c. If ReservedFlags == 3 (CPU Cycle Counter): DOUBLE timeStampScale = 10.0 / logFile.LogfileHeader.CpuSpeedInMHz;  
</dl> </dd> 3. On the FIRST call to your EventRecordCallback function for a particular log file, use data from the logFile (EVENT\_TRACE\_LOGFILE) and from the eventRecord (EVENT\_RECORD) to compute the timeStampBase that will be used for the remaining events in the log file: INT64 timeStampBase = logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
4. For each eventRecord (EVENT\_RECORD), convert the event’s timestamp into FILETIME as follows, using the timeStampScale and timeStampBase values calculated in steps 2 and 3: INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
</dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                         |
| Header<br/>                   | <dl> <dt>Wmistr.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[*ControlCallback*](/windows/win32/api/evntrace/nc-evntrace-wmidprequest)
</dt> <dt>

[**\_ \_ EREIGNISABLAUFVERFOLGUNGSEIGENSCHAFTEN**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle)
</dt> <dt>

[**GROßE \_ GANZE ZAHL**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)
</dt> </dl>

 

 
