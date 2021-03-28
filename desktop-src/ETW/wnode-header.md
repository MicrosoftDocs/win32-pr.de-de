---
description: Die wnode- \_ Header Struktur ist ein Member der Eigenschaften Struktur der Ereignis Ablauf \_ Verfolgung \_ .
ms.assetid: 862a8f46-a326-48c6-92b7-8bb667837bb7
title: WNODE_HEADER Struktur (wmistr. h)
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
ms.openlocfilehash: 6a2ed615d2b67cbd47a817234a14b7cf1221f601
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "104982836"
---
# <a name="wnode_header-structure"></a>Wnode- \_ Header Struktur

Die **wnode- \_ Header** Struktur ist ein Member der [**\_ \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) Struktur der Ereignis Ablauf Verfolgung.

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

Gesamtgröße des zugeordneten Arbeitsspeichers in Bytes für die Eigenschaften der Ereignis Ablauf Verfolgungs Sitzung. Die Größe des Arbeitsspeichers muss den Raum für die [**Eigenschaften der Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) sowie die Zeichenfolge für den Sitzungs Namen und die Protokolldatei namens Zeichenfolge enthalten, die der Struktur im Arbeitsspeicher entsprechen

</dd> <dt>

**ProviderID**
</dt> <dd>

Für die interne Verwendung reserviert.

</dd> <dt>

**Historicalcontext**
</dt> <dd>

Bei der Ausgabe das Handle für die Ereignis Ablauf Verfolgungs Sitzung.

</dd> <dt>

**Version**
</dt> <dd>

Für die interne Verwendung reserviert.

</dd> <dt>

**Verknüpfung**
</dt> <dd>

Für die interne Verwendung reserviert.

</dd> <dt>

**KERNELHANDLE**
</dt> <dd>

Für die interne Verwendung reserviert.

</dd> <dt>

**Zeitstempel**
</dt> <dd>

Der Zeitpunkt, zu dem die Informationen in dieser Struktur in 100-Nanosekunden-Intervallen seit Mitternacht, 1. Januar 1601, aktualisiert wurden.

</dd> <dt>

**GUID**
</dt> <dd>

Die GUID, die Sie für die Sitzung definieren.

Legen Sie für eine NT-Kernel Protokollierungs Sitzung diesen Member auf **systemtracecontrolguid** fest.

Wenn dieser Member auf **systemtracecontrolguid** oder **globalloggerguid** festgelegt ist, ist die Protokollierung eine Systemprotokollierung.

Legen Sie für eine private Protokollierungs Sitzung diesen Member auf die GUID des Anbieters fest, den Sie für die Sitzung aktivieren werden.

Wenn Sie eine Sitzung starten, bei der es sich nicht um eine Kernel Protokollierung oder eine private Protokollierungs Sitzung handelt, müssen Sie keine Sitzungs-GUID angeben. Wenn Sie keine GUID angeben, wird von etw eine für Sie erstellt. Sie müssen eine Sitzungs-GUID nur angeben, wenn Sie die Standard Berechtigungen ändern möchten, die einer bestimmten Sitzung zugeordnet sind. Weitere Informationen finden Sie in der eventaccesscontrol-Funktion.

Sie können nicht mehr als eine Sitzung mit derselben Sitzungs-GUID starten.

**Vor Windows Vista:** Sie können mehr als eine Sitzung mit derselben Sitzungs-GUID starten.

</dd> <dt>

**ClientContext**
</dt> <dd>

Die Uhrzeit Auflösung, die beim Protokollieren des Zeitstempels für jedes Ereignis verwendet werden soll. Der Standardwert ist "Query Performance Counter" (QPC).

**Vor Windows Vista:** Der Standardwert ist die Systemzeit.

**Vor Windows 10, Version 1703:** Es können nicht mehr als zwei unterschiedliche uhrtypen gleichzeitig von beliebigen systemloggern verwendet werden.

**Ab Windows 10, Version 1703:** Die Uhrtyp Einschränkung wurde entfernt. Alle drei uhrtypen können nun gleichzeitig von systemloggern verwendet werden.

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
<td>Query Performance Counter (QPC). Der QPC-Leistungs-Counter bietet einen Zeitstempel mit hoher Auflösung, der von Anpassungen der Systemuhr nicht betroffen ist. Der im Ereignis gespeicherte Zeitstempel entspricht dem Wert, der von der QueryPerformanceCounter-API zurückgegeben wird. Weitere Informationen zu den Merkmalen dieses Zeitstempels finden Sie unter <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">erwerben von Zeitstempeln mit hoher Auflösung</a>.<br/> Sie sollten diese Lösung verwenden, wenn Sie über hohe Ereignis Raten verfügen oder wenn der Consumer Ereignisse aus verschiedenen Puffern zusammenfasst. In diesen Fällen ermöglicht die Genauigkeit und Stabilität des QPC-Zeitstempels eine bessere Genauigkeit bei der Anordnung von Ereignissen aus unterschiedlichen Puffern. Der QPC-Zeitstempel spiegelt jedoch keine Updates für die Systemuhr wider, z. b. wenn die Systemuhr aufgrund der Synchronisierung mit einem NTP-Server, während die Ablauf Verfolgung ausgeführt wird, vorwärts angepasst wird, spiegeln die QPC-Zeitstempel in der Ablauf Verfolgung weiterhin die Zeit wider, als wäre kein Update aufgetreten.<br/> Verwenden Sie zum Bestimmen der Auflösung den <strong>PerfFreq</strong> -Member von <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> , wenn Sie das Ereignis verarbeiten.<br/> Um den Zeitstempel eines Ereignisses in 100-ns-Einheiten zu konvertieren, verwenden Sie die folgende Konvertierungs Formel: <br/> scaledtimestamp = EventRecord. evenderader. timestamp. quadpart * 10000000,0/logfileheader. PerfFreq. quadpart<br/> Beachten Sie, dass der Zeitstempel auf älteren Computern möglicherweise nicht korrekt ist, da der-Wert manchmal aufgrund von Hardwarefehlern weiter geht.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>2</dt> </dl></td>
<td>System Zeit. Die Systemzeit bietet einen Zeitstempel, der Änderungen an der Systemuhr des Systems nachverfolgt, z. b. wenn die Systemuhr aufgrund der Synchronisierung mit einem NTP-Server, während die Ablauf Verfolgung ausgeführt wird, vorwärts angepasst wird, werden die Zeitstempel der Systemzeit in der Ablauf Verfolgung ebenfalls entsprechend der neuen Einstellung der Systemuhr fortgesetzt. <br/>
<ul>
<li>Auf Systemen vor Windows 10 entspricht der im Ereignis gespeicherte Zeitstempel dem Wert, der von der GetSystemTimeAsFileTime-API zurückgegeben wird.</li>
<li>Unter Windows 10 oder höher entspricht der im Ereignis gespeicherte Zeitstempel dem Wert, der von der getsystemtimepreciseasfiletime-API zurückgegeben wird.</li>
</ul>
Vor Windows 10 war die Auflösung dieses Zeitstempels die Auflösung eines Systemtakt Takts, wie vom timerresolution-Member von TRACE_LOGFILE_HEADER angegeben. Ab Windows 10 ist die Auflösung dieses Zeitstempels die Auflösung des Leistungs Zählers, wie vom PerfFreq-Mitglied von TRACE_LOGFILE_HEADER angegeben.<br/> Um den Zeitstempel eines Ereignisses in 100-ns-Einheiten zu konvertieren, verwenden Sie die folgende Konvertierungs Formel: <br/> scaledtimestamp = EventRecord. evenderader. timestamp. quadpart<br/> Beachten Sie Folgendes: Wenn Ereignisse auf einem System aufgezeichnet werden, auf dem ein Betriebssystem vor Windows 10 ausgeführt wird, ist die Auflösung der Systemzeit möglicherweise nicht ausreichend, um die Reihenfolge der Ereignisse zu bestimmen, wenn die Anzahl der Ereignisse hoch ist. In diesem Fall weist ein Satz von Ereignissen denselben Zeitstempel auf, aber die Reihenfolge, in der die Ereignisse von etw übermittelt werden, ist möglicherweise nicht richtig. Ab Windows 10 wird der Zeitstempel mit zusätzlicher Genauigkeit aufgezeichnet, obwohl eine gewisse Instabilität in Fällen auftreten kann, in denen die Systemuhr während der Erfassung der Ablauf Verfolgung angepasst wurde.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>€</dt> </dl></td>
<td>CPU-Zyklen-Counter. Der CPU-Leistungs Bewert bietet den höchsten Zeitstempel für die Auflösung und ist der am wenigsten ressourcenintensive Abruf. Der CPU-Counter ist jedoch unzuverlässig und sollte nicht in der Produktionsumgebung verwendet werden. Auf einigen Computern ändern sich z. b. die Häufigkeit aufgrund von Änderungen an der Stromversorgung und der Stromversorgung, zusätzlich zum Beenden in einigen Zuständen.<br/> Verwenden Sie zum Bestimmen der Auflösung das <strong>cpuspeedinmhz</strong> -Element von <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> , wenn Sie das Ereignis verarbeiten.<br/> Wenn die Hardware diesen Uhrentyp nicht unterstützt, verwendet ETW die Systemzeit.<br/> <strong>Windows Server 2003, Windows XP mit SP1 und Windows XP:</strong> Dieser Wert wird nicht unterstützt und wurde in Windows Server 2003 mit SP1 und Windows XP mit SP2 eingeführt.<br/></td>
</tr>
</tbody>
</table>



 

**Windows 2000:** Der **clientcontext** -Member wird nicht unterstützt.

</dd> <dt>

**Flags**
</dt> <dd>

Muss die **\_ \_ \_ GUID des wnode-Flags** enthalten, um anzugeben, dass die Strukturinformationen zur Ereignis Ablauf Verfolgung enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Stellen Sie sicher, dass Sie den Arbeitsspeicher für diese Struktur auf Null initialisieren, bevor Sie Elemente festlegen.

Verwenden Sie das folgende Verfahren, um einen etw-Zeitstempel in eine FILETIME zu konvertieren:

<dl> 1. Aktivieren Sie für jede zu verarbeitende Sitzung oder Protokolldatei (d. h. für jede Ereignis \_ Ablauf Verfolgungs Protokoll \_ Datei) das Feld Logfile. processtracemode, um zu bestimmen, ob das Flag für das unformatierte Zeitstempel des Prozessablauf \_ Verfolgungs \_ Modus \_ \_ festgelegt ist. Standardmäßig ist dieses Flag nicht festgelegt. Wenn dieses Flag nicht festgelegt ist, konvertiert die ETW-Laufzeit den Zeitstempel jedes Ereignis \_ Datensatzes automatisch in eine FILETIME, bevor der Ereignis \_ Daten Satz an die eventrecordcallback-Funktion gesendet wird, sodass keine zusätzliche Verarbeitung erforderlich ist. Die folgenden Schritte sollten nur verwendet werden, wenn die Ablauf Verfolgung mit dem unformatierten Timestamp-Flag für den Prozessablauf \_ Verfolgungs Modus verarbeitet wird \_ \_ \_ .  
2. Überprüfen Sie für jede zu verarbeitende Sitzung oder Protokolldatei (d. h. für jede Ereignis Ablauf \_ Verfolgungs Protokoll \_ Datei) das Feld Logfile. logfileheader. reservedflags, um die Zeitstempel Skala für die Protokolldatei zu bestimmen. Führen Sie basierend auf dem Wert von reservedflags einen der folgenden Schritte aus, um den Wert zu bestimmen, der für timestampscale in den verbleibenden Schritten verwendet wird: <dl> a. Wenn reservedflags = = 1 (QPC): Double timestampscale = 10000000,0/Logfile. logfileheader. PerfFreq. quadpart;  
b. Wenn reservedflags = = 2 (System Zeit): Double timestampscale = 1,0;  
Beachten Sie, dass die verbleibenden Schritte für Ereignisse, die die Systemzeit verwenden, unnötig sind, da die Ereignisse ihre Zeitstempel bereits in FILETIME-Einheiten bereitstellen. Die verbleibenden Schritte funktionieren zwar, sind aber unnötig und führen zu einem kleinen Rundungsfehler.  
c. Wenn reservedflags = = 3 (CPU-Zyklen-Counter): Double timestampscale = 10,0/Logfile. logfileheader. cpuspeedinmhz;  
</dl> </dd> 3. On the FIRST call to your EventRecordCallback function for a particular log file, use data from the logFile (EVENT\_TRACE\_LOGFILE) and from the eventRecord (EVENT\_RECORD) to compute the timeStampBase that will be used for the remaining events in the log file: INT64 timeStampBase = logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
4. For each eventRecord (EVENT\_RECORD), convert the event’s timestamp into FILETIME as follows, using the timeStampScale and timeStampBase values calculated in steps 2 and 3: INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
</dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[ Desktop Apps \| UWP-apps\]<br/>                         |
| Header<br/>                   | <dl> <dt>Wmistr. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[*Controlcallback*](/windows/win32/api/evntrace/nc-evntrace-wmidprequest)
</dt> <dt>

[**Eigenschaften der Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**Gettraceloggerhandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle)
</dt> <dt>

[**große \_ ganze Zahl**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)
</dt> </dl>

 

 
