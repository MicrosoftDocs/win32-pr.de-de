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
# <a name="wnode_header-structure"></a><span data-ttu-id="6d7c8-103">Wnode- \_ Header Struktur</span><span class="sxs-lookup"><span data-stu-id="6d7c8-103">WNODE\_HEADER structure</span></span>

<span data-ttu-id="6d7c8-104">Die **wnode- \_ Header** Struktur ist ein Member der [**\_ \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) Struktur der Ereignis Ablauf Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-104">The **WNODE\_HEADER** structure is a member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d7c8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d7c8-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="6d7c8-106">Member</span><span class="sxs-lookup"><span data-stu-id="6d7c8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6d7c8-107">**BufferSize**</span><span class="sxs-lookup"><span data-stu-id="6d7c8-107">**BufferSize**</span></span>
</dt> <dd>

<span data-ttu-id="6d7c8-108">Gesamtgröße des zugeordneten Arbeitsspeichers in Bytes für die Eigenschaften der Ereignis Ablauf Verfolgungs Sitzung.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-108">Total size of memory allocated, in bytes, for the event tracing session properties.</span></span> <span data-ttu-id="6d7c8-109">Die Größe des Arbeitsspeichers muss den Raum für die [**Eigenschaften der Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) sowie die Zeichenfolge für den Sitzungs Namen und die Protokolldatei namens Zeichenfolge enthalten, die der Struktur im Arbeitsspeicher entsprechen</span><span class="sxs-lookup"><span data-stu-id="6d7c8-109">The size of memory must include the room for the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure plus the session name string and log file name string that follow the structure in memory.</span></span>

</dd> <dt>

<span data-ttu-id="6d7c8-110">**ProviderID**</span><span class="sxs-lookup"><span data-stu-id="6d7c8-110">**ProviderId**</span></span>
</dt> <dd>

<span data-ttu-id="6d7c8-111">Für die interne Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-111">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="6d7c8-112">**Historicalcontext**</span><span class="sxs-lookup"><span data-stu-id="6d7c8-112">**HistoricalContext**</span></span>
</dt> <dd>

<span data-ttu-id="6d7c8-113">Bei der Ausgabe das Handle für die Ereignis Ablauf Verfolgungs Sitzung.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-113">On output, the handle to the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="6d7c8-114">**Version**</span><span class="sxs-lookup"><span data-stu-id="6d7c8-114">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="6d7c8-115">Für die interne Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-115">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="6d7c8-116">**Verknüpfung**</span><span class="sxs-lookup"><span data-stu-id="6d7c8-116">**Linkage**</span></span>
</dt> <dd>

<span data-ttu-id="6d7c8-117">Für die interne Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-117">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="6d7c8-118">**KERNELHANDLE**</span><span class="sxs-lookup"><span data-stu-id="6d7c8-118">**KernelHandle**</span></span>
</dt> <dd>

<span data-ttu-id="6d7c8-119">Für die interne Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-119">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="6d7c8-120">**Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="6d7c8-120">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="6d7c8-121">Der Zeitpunkt, zu dem die Informationen in dieser Struktur in 100-Nanosekunden-Intervallen seit Mitternacht, 1. Januar 1601, aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-121">Time at which the information in this structure was updated, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="6d7c8-122">**GUID**</span><span class="sxs-lookup"><span data-stu-id="6d7c8-122">**Guid**</span></span>
</dt> <dd>

<span data-ttu-id="6d7c8-123">Die GUID, die Sie für die Sitzung definieren.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-123">The GUID that you define for the session.</span></span>

<span data-ttu-id="6d7c8-124">Legen Sie für eine NT-Kernel Protokollierungs Sitzung diesen Member auf **systemtracecontrolguid** fest.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-124">For an NT Kernel Logger session, set this member to **SystemTraceControlGuid**.</span></span>

<span data-ttu-id="6d7c8-125">Wenn dieser Member auf **systemtracecontrolguid** oder **globalloggerguid** festgelegt ist, ist die Protokollierung eine Systemprotokollierung.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-125">If this member is set to **SystemTraceControlGuid** or **GlobalLoggerGuid**, the logger will be a system logger.</span></span>

<span data-ttu-id="6d7c8-126">Legen Sie für eine private Protokollierungs Sitzung diesen Member auf die GUID des Anbieters fest, den Sie für die Sitzung aktivieren werden.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-126">For a private logger session, set this member to the provider's GUID that you are going to enable for the session.</span></span>

<span data-ttu-id="6d7c8-127">Wenn Sie eine Sitzung starten, bei der es sich nicht um eine Kernel Protokollierung oder eine private Protokollierungs Sitzung handelt, müssen Sie keine Sitzungs-GUID angeben.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-127">If you start a session that is not a kernel logger or private logger session, you do not have to specify a session GUID.</span></span> <span data-ttu-id="6d7c8-128">Wenn Sie keine GUID angeben, wird von etw eine für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-128">If you do not specify a GUID, ETW creates one for you.</span></span> <span data-ttu-id="6d7c8-129">Sie müssen eine Sitzungs-GUID nur angeben, wenn Sie die Standard Berechtigungen ändern möchten, die einer bestimmten Sitzung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-129">You need to specify a session GUID only if you want to change the default permissions associated with a specific session.</span></span> <span data-ttu-id="6d7c8-130">Weitere Informationen finden Sie in der eventaccesscontrol-Funktion.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-130">For details, see the EventAccessControl function.</span></span>

<span data-ttu-id="6d7c8-131">Sie können nicht mehr als eine Sitzung mit derselben Sitzungs-GUID starten.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-131">You cannot start more than one session with the same session GUID.</span></span>

<span data-ttu-id="6d7c8-132">**Vor Windows Vista:** Sie können mehr als eine Sitzung mit derselben Sitzungs-GUID starten.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-132">**Prior to Windows Vista:** You can start more than one session with the same session GUID.</span></span>

</dd> <dt>

<span data-ttu-id="6d7c8-133">**ClientContext**</span><span class="sxs-lookup"><span data-stu-id="6d7c8-133">**ClientContext**</span></span>
</dt> <dd>

<span data-ttu-id="6d7c8-134">Die Uhrzeit Auflösung, die beim Protokollieren des Zeitstempels für jedes Ereignis verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-134">Clock resolution to use when logging the time stamp for each event.</span></span> <span data-ttu-id="6d7c8-135">Der Standardwert ist "Query Performance Counter" (QPC).</span><span class="sxs-lookup"><span data-stu-id="6d7c8-135">The default is Query performance counter (QPC).</span></span>

<span data-ttu-id="6d7c8-136">**Vor Windows Vista:** Der Standardwert ist die Systemzeit.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-136">**Prior to Windows Vista:** The default is system time.</span></span>

<span data-ttu-id="6d7c8-137">**Vor Windows 10, Version 1703:** Es können nicht mehr als zwei unterschiedliche uhrtypen gleichzeitig von beliebigen systemloggern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-137">**Prior to Windows 10, version 1703:** No more than 2 distinct clock types can be used simultaneously by any system loggers.</span></span>

<span data-ttu-id="6d7c8-138">**Ab Windows 10, Version 1703:** Die Uhrtyp Einschränkung wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-138">**Starting with Windows 10, version 1703:** The clock type restriction has been removed.</span></span> <span data-ttu-id="6d7c8-139">Alle drei uhrtypen können nun gleichzeitig von systemloggern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-139">All three clock types can now be used simultaneously by system loggers.</span></span>

<span data-ttu-id="6d7c8-140">Sie können einen der folgenden Werte angeben.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-140">You can specify one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6d7c8-141">Wert</span><span class="sxs-lookup"><span data-stu-id="6d7c8-141">Value</span></span></th>
<th><span data-ttu-id="6d7c8-142">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6d7c8-142">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="6d7c8-143"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="6d7c8-143"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="6d7c8-144">Query Performance Counter (QPC).</span><span class="sxs-lookup"><span data-stu-id="6d7c8-144">Query performance counter (QPC).</span></span> <span data-ttu-id="6d7c8-145">Der QPC-Leistungs-Counter bietet einen Zeitstempel mit hoher Auflösung, der von Anpassungen der Systemuhr nicht betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-145">The QPC counter provides a high-resolution time stamp that is not affected by adjustments to the system clock.</span></span> <span data-ttu-id="6d7c8-146">Der im Ereignis gespeicherte Zeitstempel entspricht dem Wert, der von der QueryPerformanceCounter-API zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-146">The time stamp stored in the event is equivalent to the value returned from the QueryPerformanceCounter API.</span></span> <span data-ttu-id="6d7c8-147">Weitere Informationen zu den Merkmalen dieses Zeitstempels finden Sie unter <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">erwerben von Zeitstempeln mit hoher Auflösung</a>.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-147">For more information on the characteristics of this time stamp, see <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">Acquiring high-resolution time stamps</a>.</span></span><br/> <span data-ttu-id="6d7c8-148">Sie sollten diese Lösung verwenden, wenn Sie über hohe Ereignis Raten verfügen oder wenn der Consumer Ereignisse aus verschiedenen Puffern zusammenfasst.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-148">You should use this resolution if you have high event rates or if the consumer merges events from different buffers.</span></span> <span data-ttu-id="6d7c8-149">In diesen Fällen ermöglicht die Genauigkeit und Stabilität des QPC-Zeitstempels eine bessere Genauigkeit bei der Anordnung von Ereignissen aus unterschiedlichen Puffern.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-149">In these cases, the precision and stability of the QPC time stamp allows for better accuracy in ordering the events from different buffers.</span></span> <span data-ttu-id="6d7c8-150">Der QPC-Zeitstempel spiegelt jedoch keine Updates für die Systemuhr wider, z. b. wenn die Systemuhr aufgrund der Synchronisierung mit einem NTP-Server, während die Ablauf Verfolgung ausgeführt wird, vorwärts angepasst wird, spiegeln die QPC-Zeitstempel in der Ablauf Verfolgung weiterhin die Zeit wider, als wäre kein Update aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-150">However, the QPC time stamp will not reflect updates to the system clock, e.g. if the system clock is adjusted forward due to synchronization with an NTP server while the trace is in progress, the QPC time stamps in the trace will continue to reflect time as if no update had occurred.</span></span><br/> <span data-ttu-id="6d7c8-151">Verwenden Sie zum Bestimmen der Auflösung den <strong>PerfFreq</strong> -Member von <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> , wenn Sie das Ereignis verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-151">To determine the resolution, use the <strong>PerfFreq</strong> member of <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> when consuming the event.</span></span><br/> <span data-ttu-id="6d7c8-152">Um den Zeitstempel eines Ereignisses in 100-ns-Einheiten zu konvertieren, verwenden Sie die folgende Konvertierungs Formel:</span><span class="sxs-lookup"><span data-stu-id="6d7c8-152">To convert an event’s time stamp into 100-ns units, use the following conversion formula:</span></span> <br/> <span data-ttu-id="6d7c8-153">scaledtimestamp = EventRecord. evenderader. timestamp. quadpart \* 10000000,0/logfileheader. PerfFreq. quadpart</span><span class="sxs-lookup"><span data-stu-id="6d7c8-153">scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart \* 10000000.0 / logfileHeader.PerfFreq.QuadPart</span></span><br/> <span data-ttu-id="6d7c8-154">Beachten Sie, dass der Zeitstempel auf älteren Computern möglicherweise nicht korrekt ist, da der-Wert manchmal aufgrund von Hardwarefehlern weiter geht.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-154">Note that on older computers, the time stamp may not be accurate because the counter sometimes skips forward due to hardware errors.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6d7c8-155"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="6d7c8-155"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="6d7c8-156">System Zeit.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-156">System time.</span></span> <span data-ttu-id="6d7c8-157">Die Systemzeit bietet einen Zeitstempel, der Änderungen an der Systemuhr des Systems nachverfolgt, z. b. wenn die Systemuhr aufgrund der Synchronisierung mit einem NTP-Server, während die Ablauf Verfolgung ausgeführt wird, vorwärts angepasst wird, werden die Zeitstempel der Systemzeit in der Ablauf Verfolgung ebenfalls entsprechend der neuen Einstellung der Systemuhr fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-157">The system time provides a time stamp that tracks changes to the system’s clock, e.g. if the system clock is adjusted forward due to synchronization with an NTP server while the trace is in progress, the System Time time stamps in the trace will also jump forward to match the new setting of the system clock.</span></span> <br/>
<ul>
<li><span data-ttu-id="6d7c8-158">Auf Systemen vor Windows 10 entspricht der im Ereignis gespeicherte Zeitstempel dem Wert, der von der GetSystemTimeAsFileTime-API zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-158">On systems prior to Windows 10, the time stamp stored in the event is equivalent to the value returned from the GetSystemTimeAsFileTime API.</span></span></li>
<li><span data-ttu-id="6d7c8-159">Unter Windows 10 oder höher entspricht der im Ereignis gespeicherte Zeitstempel dem Wert, der von der getsystemtimepreciseasfiletime-API zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-159">On Windows 10 or later, the time stamp stored in the event is equivalent to the value returned from the GetSystemTimePreciseAsFileTime API.</span></span></li>
</ul>
<span data-ttu-id="6d7c8-160">Vor Windows 10 war die Auflösung dieses Zeitstempels die Auflösung eines Systemtakt Takts, wie vom timerresolution-Member von TRACE_LOGFILE_HEADER angegeben.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-160">Prior to Windows 10, the resolution of this time stamp was the resolution of a system clock tick, as indicated by the TimerResolution member of TRACE_LOGFILE_HEADER.</span></span> <span data-ttu-id="6d7c8-161">Ab Windows 10 ist die Auflösung dieses Zeitstempels die Auflösung des Leistungs Zählers, wie vom PerfFreq-Mitglied von TRACE_LOGFILE_HEADER angegeben.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-161">Starting with Windows 10, the resolution of this time stamp is the performance counter resolution, as indicated by the PerfFreq member of TRACE_LOGFILE_HEADER.</span></span><br/> <span data-ttu-id="6d7c8-162">Um den Zeitstempel eines Ereignisses in 100-ns-Einheiten zu konvertieren, verwenden Sie die folgende Konvertierungs Formel:</span><span class="sxs-lookup"><span data-stu-id="6d7c8-162">To convert an event’s time stamp into 100-ns units, use the following conversion formula:</span></span> <br/> <span data-ttu-id="6d7c8-163">scaledtimestamp = EventRecord. evenderader. timestamp. quadpart</span><span class="sxs-lookup"><span data-stu-id="6d7c8-163">scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart</span></span><br/> <span data-ttu-id="6d7c8-164">Beachten Sie Folgendes: Wenn Ereignisse auf einem System aufgezeichnet werden, auf dem ein Betriebssystem vor Windows 10 ausgeführt wird, ist die Auflösung der Systemzeit möglicherweise nicht ausreichend, um die Reihenfolge der Ereignisse zu bestimmen, wenn die Anzahl der Ereignisse hoch ist.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-164">Note that when events are captured on a system running an OS prior to Windows 10, if the volume of events is high, the resolution for system time may not be fine enough to determine the sequence of events.</span></span> <span data-ttu-id="6d7c8-165">In diesem Fall weist ein Satz von Ereignissen denselben Zeitstempel auf, aber die Reihenfolge, in der die Ereignisse von etw übermittelt werden, ist möglicherweise nicht richtig.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-165">In this case, a set of events will have the same time stamp, but the order in which ETW delivers the events may not be correct.</span></span> <span data-ttu-id="6d7c8-166">Ab Windows 10 wird der Zeitstempel mit zusätzlicher Genauigkeit aufgezeichnet, obwohl eine gewisse Instabilität in Fällen auftreten kann, in denen die Systemuhr während der Erfassung der Ablauf Verfolgung angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-166">Starting with Windows 10, the time stamp is captured with additional precision, though some instability may still occur in cases where the system clock was adjusted while the trace was being captured.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6d7c8-167"><dt>€</dt> </span><span class="sxs-lookup"><span data-stu-id="6d7c8-167"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="6d7c8-168">CPU-Zyklen-Counter.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-168">CPU cycle counter.</span></span> <span data-ttu-id="6d7c8-169">Der CPU-Leistungs Bewert bietet den höchsten Zeitstempel für die Auflösung und ist der am wenigsten ressourcenintensive Abruf.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-169">The CPU counter provides the highest resolution time stamp and is the least resource-intensive to retrieve.</span></span> <span data-ttu-id="6d7c8-170">Der CPU-Counter ist jedoch unzuverlässig und sollte nicht in der Produktionsumgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-170">However, the CPU counter is unreliable and should not be used in production.</span></span> <span data-ttu-id="6d7c8-171">Auf einigen Computern ändern sich z. b. die Häufigkeit aufgrund von Änderungen an der Stromversorgung und der Stromversorgung, zusätzlich zum Beenden in einigen Zuständen.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-171">For example, on some computers, the timers will change frequency due to thermal and power changes, in addition to stopping in some states.</span></span><br/> <span data-ttu-id="6d7c8-172">Verwenden Sie zum Bestimmen der Auflösung das <strong>cpuspeedinmhz</strong> -Element von <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> , wenn Sie das Ereignis verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-172">To determine the resolution, use the <strong>CpuSpeedInMHz</strong> member of <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> when consuming the event.</span></span><br/> <span data-ttu-id="6d7c8-173">Wenn die Hardware diesen Uhrentyp nicht unterstützt, verwendet ETW die Systemzeit.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-173">If your hardware does not support this clock type, ETW uses system time.</span></span><br/> <span data-ttu-id="6d7c8-174"><strong>Windows Server 2003, Windows XP mit SP1 und Windows XP:</strong> Dieser Wert wird nicht unterstützt und wurde in Windows Server 2003 mit SP1 und Windows XP mit SP2 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-174"><strong>Windows Server 2003, Windows XP with SP1 and Windows XP:</strong> This value is not supported, it was introduced in Windows Server 2003 with SP1 and Windows XP with SP2.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6d7c8-175">**Windows 2000:** Der **clientcontext** -Member wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-175">**Windows 2000:** The **ClientContext** member is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6d7c8-176">**Flags**</span><span class="sxs-lookup"><span data-stu-id="6d7c8-176">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="6d7c8-177">Muss die **\_ \_ \_ GUID des wnode-Flags** enthalten, um anzugeben, dass die Strukturinformationen zur Ereignis Ablauf Verfolgung enthält.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-177">Must contain **WNODE\_FLAG\_TRACED\_GUID** to indicate that the structure contains event tracing information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d7c8-178">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d7c8-178">Remarks</span></span>

<span data-ttu-id="6d7c8-179">Stellen Sie sicher, dass Sie den Arbeitsspeicher für diese Struktur auf Null initialisieren, bevor Sie Elemente festlegen.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-179">Be sure to initialize the memory for this structure to zero before setting any members.</span></span>

<span data-ttu-id="6d7c8-180">Verwenden Sie das folgende Verfahren, um einen etw-Zeitstempel in eine FILETIME zu konvertieren:</span><span class="sxs-lookup"><span data-stu-id="6d7c8-180">To convert an ETW timestamp into a FILETIME, use the following procedure:</span></span>

<dl> 1. <span data-ttu-id="6d7c8-181">Aktivieren Sie für jede zu verarbeitende Sitzung oder Protokolldatei (d. h. für jede Ereignis \_ Ablauf Verfolgungs Protokoll \_ Datei) das Feld Logfile. processtracemode, um zu bestimmen, ob das Flag für das unformatierte Zeitstempel des Prozessablauf \_ Verfolgungs \_ Modus \_ \_ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-181">For each session or log file being processed (i.e. for each EVENT\_TRACE\_LOGFILE), check the logFile.ProcessTraceMode field to determine whether the PROCESS\_TRACE\_MODE\_RAW\_TIMESTAMP flag is set.</span></span> <span data-ttu-id="6d7c8-182">Standardmäßig ist dieses Flag nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-182">By default, this flag is not set.</span></span> <span data-ttu-id="6d7c8-183">Wenn dieses Flag nicht festgelegt ist, konvertiert die ETW-Laufzeit den Zeitstempel jedes Ereignis \_ Datensatzes automatisch in eine FILETIME, bevor der Ereignis \_ Daten Satz an die eventrecordcallback-Funktion gesendet wird, sodass keine zusätzliche Verarbeitung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-183">If this flag is not set, the ETW runtime will automatically convert the timestamp of each EVENT\_RECORD into a FILETIME before sending the EVENT\_RECORD to your EventRecordCallback function, so no additional processing is needed.</span></span> <span data-ttu-id="6d7c8-184">Die folgenden Schritte sollten nur verwendet werden, wenn die Ablauf Verfolgung mit dem unformatierten Timestamp-Flag für den Prozessablauf \_ Verfolgungs Modus verarbeitet wird \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6d7c8-184">The following steps should only be used if the trace is being processed with the PROCESS\_TRACE\_MODE\_RAW\_TIMESTAMP flag set.</span></span>  
2. <span data-ttu-id="6d7c8-185">Überprüfen Sie für jede zu verarbeitende Sitzung oder Protokolldatei (d. h. für jede Ereignis Ablauf \_ Verfolgungs Protokoll \_ Datei) das Feld Logfile. logfileheader. reservedflags, um die Zeitstempel Skala für die Protokolldatei zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-185">For each session or log file being processed (i.e. for each EVENT\_TRACE\_LOGFILE), check the logFile.LogfileHeader.ReservedFlags field to determine the time stamp scale for the log file.</span></span> <span data-ttu-id="6d7c8-186">Führen Sie basierend auf dem Wert von reservedflags einen der folgenden Schritte aus, um den Wert zu bestimmen, der für timestampscale in den verbleibenden Schritten verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="6d7c8-186">Based on the value of ReservedFlags, follow one of these steps to determine the value to use for timeStampScale in the remaining steps:</span></span> <dl> <span data-ttu-id="6d7c8-187">a.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-187">a.</span></span> <span data-ttu-id="6d7c8-188">Wenn reservedflags = = 1 (QPC): Double timestampscale = 10000000,0/Logfile. logfileheader. PerfFreq. quadpart;</span><span class="sxs-lookup"><span data-stu-id="6d7c8-188">If ReservedFlags == 1 (QPC): DOUBLE timeStampScale = 10000000.0 / logFile.LogfileHeader.PerfFreq.QuadPart;</span></span>  
<span data-ttu-id="6d7c8-189">b.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-189">b.</span></span> <span data-ttu-id="6d7c8-190">Wenn reservedflags = = 2 (System Zeit): Double timestampscale = 1,0;</span><span class="sxs-lookup"><span data-stu-id="6d7c8-190">If ReservedFlags == 2 (System time): DOUBLE timeStampScale = 1.0;</span></span>  
<span data-ttu-id="6d7c8-191">Beachten Sie, dass die verbleibenden Schritte für Ereignisse, die die Systemzeit verwenden, unnötig sind, da die Ereignisse ihre Zeitstempel bereits in FILETIME-Einheiten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-191">Note that the remaining steps are unnecessary for events using system time, since the events already provide their time stamps in FILETIME units.</span></span> <span data-ttu-id="6d7c8-192">Die verbleibenden Schritte funktionieren zwar, sind aber unnötig und führen zu einem kleinen Rundungsfehler.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-192">The remaining steps will work but are unnecessary and will introduce a small rounding error.</span></span>  
<span data-ttu-id="6d7c8-193">c.</span><span class="sxs-lookup"><span data-stu-id="6d7c8-193">c.</span></span> <span data-ttu-id="6d7c8-194">Wenn reservedflags = = 3 (CPU-Zyklen-Counter): Double timestampscale = 10,0/Logfile. logfileheader. cpuspeedinmhz;</span><span class="sxs-lookup"><span data-stu-id="6d7c8-194">If ReservedFlags == 3 (CPU cycle counter): DOUBLE timeStampScale = 10.0 / logFile.LogfileHeader.CpuSpeedInMHz;</span></span>  
</dl> </dd> 3. On the FIRST call to your EventRecordCallback function for a particular log file, use data from the logFile (EVENT\_TRACE\_LOGFILE) and from the eventRecord (EVENT\_RECORD) to compute the timeStampBase that will be used for the remaining events in the log file: INT64 timeStampBase = logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
4. For each eventRecord (EVENT\_RECORD), convert the event’s timestamp into FILETIME as follows, using the timeStampScale and timeStampBase values calculated in steps 2 and 3: INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
</dl>

## <a name="requirements"></a><span data-ttu-id="6d7c8-195">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6d7c8-195">Requirements</span></span>



| <span data-ttu-id="6d7c8-196">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d7c8-196">Requirement</span></span> | <span data-ttu-id="6d7c8-197">Wert</span><span class="sxs-lookup"><span data-stu-id="6d7c8-197">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6d7c8-198">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d7c8-198">Minimum supported client</span></span><br/> | <span data-ttu-id="6d7c8-199">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6d7c8-199">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                   |
| <span data-ttu-id="6d7c8-200">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d7c8-200">Minimum supported server</span></span><br/> | <span data-ttu-id="6d7c8-201">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6d7c8-201">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                         |
| <span data-ttu-id="6d7c8-202">Header</span><span class="sxs-lookup"><span data-stu-id="6d7c8-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d7c8-203"><dt>Wmistr. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d7c8-203"><dt>Wmistr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d7c8-204">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6d7c8-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d7c8-205">*Controlcallback*</span><span class="sxs-lookup"><span data-stu-id="6d7c8-205">*ControlCallback*</span></span>](/windows/win32/api/evntrace/nc-evntrace-wmidprequest)
</dt> <dt>

[<span data-ttu-id="6d7c8-206">**Eigenschaften der Ereignis Ablauf \_ Verfolgung \_**</span><span class="sxs-lookup"><span data-stu-id="6d7c8-206">**EVENT\_TRACE\_PROPERTIES**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[<span data-ttu-id="6d7c8-207">**Gettraceloggerhandle**</span><span class="sxs-lookup"><span data-stu-id="6d7c8-207">**GetTraceLoggerHandle**</span></span>](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle)
</dt> <dt>

[<span data-ttu-id="6d7c8-208">**große \_ ganze Zahl**</span><span class="sxs-lookup"><span data-stu-id="6d7c8-208">**LARGE\_INTEGER**</span></span>](/windows/win32/api/winnt/ns-winnt-large_integer-r1)
</dt> </dl>

 

 
