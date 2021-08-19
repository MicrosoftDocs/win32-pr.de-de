---
description: Die WNODE \_ HEADER-Struktur ist ein Member der EVENT \_ TRACE \_ PROPERTIES-Struktur.
ms.assetid: 862a8f46-a326-48c6-92b7-8bb667837bb7
title: WNODE_HEADER -Struktur (Wmistr.h)
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

Gesamtgröße des zugeordneten Arbeitsspeichers für die Sitzungseigenschaften der Ereignisablaufverfolgung in Bytes. Die Größe des Arbeitsspeichers muss den Raum für die [**EVENT \_ TRACE \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) sowie die Zeichenfolge für den Sitzungsnamen und den Namen der Protokolldatei enthalten, die der Struktur im Arbeitsspeicher folgen.

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

Die Zeit, zu der die Informationen in dieser Struktur aktualisiert wurden, in Intervallen von 100 Nanosekunden seit Mitternacht, dem 1. Januar 1601.

</dd> <dt>

**Guid**
</dt> <dd>

Die GUID, die Sie für die Sitzung definieren.

Legen Sie für eine NT-Kernelprotokollierungssitzung diesen Member auf **SystemTraceControlGuid fest.**

Wenn dieser Member auf **SystemTraceControlGuid** oder **GlobalLoggerGuid** festgelegt ist, ist die Protokollierung eine Systemprotokollierung.

Legen Sie für eine private Protokollierungssitzung dieses Mitglied auf die GUID des Anbieters fest, die Sie für die Sitzung aktivieren möchten.

Wenn Sie eine Sitzung starten, die keine Kernelprotokollierungs- oder private Protokollierungssitzung ist, müssen Sie keine Sitzungs-GUID angeben. Wenn Sie keine GUID angeben, erstellt ETW eine GUID für Sie. Sie müssen nur dann eine Sitzungs-GUID angeben, wenn Sie die einer bestimmten Sitzung zugeordneten Standardberechtigungen ändern möchten. Weitere Informationen finden Sie in der EventAccessControl-Funktion.

Sie können nicht mehr als eine Sitzung mit derselben Sitzungs-GUID starten.

**Vor der Windows Vista:** Sie können mehrere Sitzungen mit derselben Sitzungs-GUID starten.

</dd> <dt>

**ClientContext**
</dt> <dd>

Uhrauflösung, die beim Protokollieren des Zeitstempels für jedes Ereignis verwendet werden soll. Der Standardwert ist Der Abfrageleistungsindikator (Query Performance Counter, QPC).

**Vor der Windows Vista:** Der Standardwert ist die Systemzeit.

**Vor Windows 10 Version 1703:** Alle Systemprotokollierungstypen können nicht mehr als zwei unterschiedliche Uhrtypen gleichzeitig verwenden.

**Ab Windows 10 Version 1703:** Die Einschränkung des Uhrtyps wurde entfernt. Alle drei Uhrtypen können jetzt gleichzeitig von Systemprotokollen verwendet werden.

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
<td>Abfrageleistungsindikator (Query Performance Counter, QPC). Der QPC-Indikator stellt einen zeitstempel mit hoher Auflösung zur Verfügung, der nicht von Anpassungen der Systemuhr betroffen ist. Der im Ereignis gespeicherte Zeitstempel entspricht dem Wert, der von der QueryPerformanceCounter-API zurückgegeben wird. Weitere Informationen zu den Merkmalen dieses Zeitstempels finden Sie unter Abrufen von zeitstempeln <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">mit hoher Auflösung.</a><br/> Sie sollten diese Auflösung verwenden, wenn Sie über hohe Ereignisraten verfügen oder wenn der Consumer Ereignisse aus unterschiedlichen Puffern zusammenführungen. In diesen Fällen ermöglicht die Genauigkeit und Stabilität des QPC-Zeitstempels eine bessere Genauigkeit bei der Sortierung der Ereignisse aus verschiedenen Puffern. Der QPC-Zeitstempel spiegelt jedoch keine Aktualisierungen der Systemuhr wider, z. B. wenn die Systemuhr aufgrund der Synchronisierung mit einem NTP-Server während der Ablaufverfolgung nach vorn angepasst wird, spiegeln die QPC-Zeitstempel in der Ablaufverfolgung weiterhin die Zeit wider, als ob kein Update erfolgt wäre.<br/> Um die Auflösung zu bestimmen, verwenden Sie das <strong>PerfFreq-TRACE_LOGFILE_HEADER</strong> <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>bei</strong></a> der Nutzung des Ereignisses.<br/> Verwenden Sie die folgende Konvertierungsformel, um den Zeitstempel eines Ereignisses in 100-ns-Einheiten zu konvertieren: <br/> scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart * 10000000.0 / logfileHeader.PerfFreq.QuadPart<br/> Beachten Sie, dass der Zeitstempel auf älteren Computern möglicherweise nicht genau ist, da der Zähler manchmal aufgrund von Hardwarefehlern übersprungen wird.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>2</dt> </dl></td>
<td>Systemzeit. Die Systemzeit stellt einen Zeitstempel zur Verfügung, mit dem Änderungen an der Systemuhr nachverfolgt werden, z. B. wenn die Systemuhr aufgrund der Synchronisierung mit einem NTP-Server während der Ablaufverfolgung nach vorn angepasst wird, springen die Zeitstempel der Systemzeit in der Ablaufverfolgung ebenfalls vorwärts, um der neuen Einstellung der Systemuhr zu folgen. <br/>
<ul>
<li>Auf Systemen vor Windows 10 entspricht der im Ereignis gespeicherte Zeitstempel dem Wert, der von der GetSystemTimeAsFileTime-API zurückgegeben wird.</li>
<li>Bei Windows 10 oder höher entspricht der im Ereignis gespeicherte Zeitstempel dem Wert, der von der GetSystemTimePreciseAsFileTime-API zurückgegeben wird.</li>
</ul>
Vor Windows 10 war die Auflösung dieses Zeitstempels die Auflösung eines Systemtakttakts, wie durch den TimerResolution-Member des TRACE_LOGFILE_HEADER. Ab Windows 10 ist die Auflösung dieses Zeitstempels die Auflösung des Leistungsindikators, wie vom PerfFreq-Member des TRACE_LOGFILE_HEADER.<br/> Verwenden Sie die folgende Konvertierungsformel, um den Zeitstempel eines Ereignisses in 100-ns-Einheiten zu konvertieren: <br/> scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart<br/> Beachten Sie Folgendes: Wenn Ereignisse auf einem System erfasst werden, auf dem ein Betriebssystem vor Windows 10 ausgeführt wird und die Menge der Ereignisse hoch ist, ist die Auflösung für die Systemzeit möglicherweise nicht ausreichend, um die Abfolge der Ereignisse zu bestimmen. In diesem Fall hat ein Satz von Ereignissen den gleichen Zeitstempel, aber die Reihenfolge, in der ETW die Ereignisse liefert, ist möglicherweise nicht richtig. Ab Windows 10 wird der Zeitstempel mit zusätzlicher Genauigkeit erfasst, aber in Fällen, in denen die Systemuhr während der Erfassung der Ablaufverfolgung angepasst wurde, kann es trotzdem zu Instabilität kommen.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>3</dt> </dl></td>
<td>CPU-Zykluszähler. Der CPU-Leistungsindikator stellt den zeitstempel der höchsten Auflösung und ist der am wenigsten ressourcenintensiv abzurufende. Der CPU-Indikator ist jedoch unzuverlässig und sollte nicht in der Produktion verwendet werden. Auf einigen Computern ändern sich die Timer beispielsweise aufgrund von Wärme- und Stromänderungen und werden nicht nur in einigen Zuzuständen beendet.<br/> Um die Auflösung zu bestimmen, verwenden Sie den <strong>CpuSpeedInMHz-Member</strong> von <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> bei der Nutzung des Ereignisses.<br/> Wenn Ihre Hardware diesen Uhrtyp nicht unterstützt, verwendet ETW die Systemzeit.<br/> <strong>Windows Server 2003, Windows XP mit SP1 und Windows XP:</strong> Dieser Wert wird nicht unterstützt. Er wurde in Windows Server 2003 mit SP1 und Windows XP mit SP2 eingeführt.<br/></td>
</tr>
</tbody>
</table>



 

**Windows 2000:** Der **ClientContext-Member** wird nicht unterstützt.

</dd> <dt>

**Flags**
</dt> <dd>

Muss **WNODE \_ FLAG \_ TRACED \_ GUID enthalten,** um anzugeben, dass die Struktur Informationen zur Ereignisablaufverfolgung enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Stellen Sie sicher, dass Sie den Arbeitsspeicher für diese Struktur auf 0 (null) initialisieren, bevor Sie Member festlegen.

Um einen ETW-Zeitstempel in filetime zu konvertieren, verwenden Sie das folgende Verfahren:

<dl> 1. Überprüfen Sie für jede verarbeitete Sitzung oder Protokolldatei (d. h. für jede EVENT TRACE LOGFILE) das Feld \_ \_ logFile.ProcessTraceMode, um zu bestimmen, ob das PROCESS \_ TRACE MODE RAW \_ TIMESTAMP-Flag festgelegt \_ \_ ist. Standardmäßig ist dieses Flag nicht festgelegt. Wenn dieses Flag nicht festgelegt ist, konvertiert die ETW-Runtime den Zeitstempel jedes EVENT RECORD automatisch in eine FILETIME-Datei, bevor der EVENT RECORD an Ihre \_ EventRecordCallback-Funktion sendet, sodass keine zusätzliche Verarbeitung erforderlich \_ ist. Die folgenden Schritte sollten nur verwendet werden, wenn die Ablaufverfolgung mit dem festgelegten PROCESS \_ TRACE \_ MODE RAW \_ \_ TIMESTAMP-Flag verarbeitet wird.  
2. Überprüfen Sie für jede verarbeitete Sitzung oder Protokolldatei (d. h. für jede EVENT TRACE LOGFILE) das Feld \_ logFile.LogfileHeader.ReservedFlags, um die Zeitstempelskala für die Protokolldatei \_ zu bestimmen. Führen Sie basierend auf dem Wert von ReservedFlags einen der folgenden Schritte aus, um den Wert zu bestimmen, der in den verbleibenden Schritten für timeStampScale verwendet werden soll: <dl> a. Wenn ReservedFlags == 1 (QPC): DOUBLE timeStampScale = 10000000.0 / logFile.LogfileHeader.PerfFreq.QuadPart;  
b. Wenn ReservedFlags == 2 (Systemzeit): DOUBLE timeStampScale = 1.0;  
Beachten Sie, dass die verbleibenden Schritte für Ereignisse mit Systemzeit nicht erforderlich sind, da die Ereignisse bereits ihre Zeitstempel in FILETIME-Einheiten bereitstellen. Die verbleibenden Schritte funktionieren, sind aber nicht erforderlich und führen zu einem kleinen Rundungsfehler.  
c. Wenn ReservedFlags == 3 (CPU-Zykluszähler): DOUBLE timeStampScale = 10.0 / logFile.LogfileHeader.CpuSpeedInMHz;  
</dl> </dd> 3. On the FIRST call to your EventRecordCallback function for a particular log file, use data from the logFile (EVENT\_TRACE\_LOGFILE) and from the eventRecord (EVENT\_RECORD) to compute the timeStampBase that will be used for the remaining events in the log file: INT64 timeStampBase = logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
4. For each eventRecord (EVENT\_RECORD), convert the event’s timestamp into FILETIME as follows, using the timeStampScale and timeStampBase values calculated in steps 2 and 3: INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
</dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                         |
| Header<br/>                   | <dl> <dt>Wmistr.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[*ControlCallback*](/windows/win32/api/evntrace/nc-evntrace-wmidprequest)
</dt> <dt>

[**EIGENSCHAFTEN \_ DER \_ EREIGNISVERFOLGUNG**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle)
</dt> <dt>

[**GROßE \_ GANZE ZAHL**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)
</dt> </dl>

 

 
