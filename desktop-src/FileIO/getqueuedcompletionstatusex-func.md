---
description: Ruft mehrere Vervollständigungs Port Einträge gleichzeitig ab.
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
title: GetQueuedCompletionStatus usex-Funktion (ioapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetQueuedCompletionStatusEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: d45471cc066e6de7cb388036e06e727fe828a532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353937"
---
# <a name="getqueuedcompletionstatusex-function"></a><span data-ttu-id="e039f-103">GetQueuedCompletionStatus usex-Funktion</span><span class="sxs-lookup"><span data-stu-id="e039f-103">GetQueuedCompletionStatusEx function</span></span>

<span data-ttu-id="e039f-104">Ruft mehrere Vervollständigungs Port Einträge gleichzeitig ab.</span><span class="sxs-lookup"><span data-stu-id="e039f-104">Retrieves multiple completion port entries simultaneously.</span></span> <span data-ttu-id="e039f-105">Er wartet auf den Abschluss ausstehender e/a-Vorgänge, die dem angegebenen Abschlussport zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e039f-105">It waits for pending I/O operations that are associated with the specified completion port to complete.</span></span>

<span data-ttu-id="e039f-106">Um die e/a-Abschluss Pakete einzeln aus der Warteschlange zu entfernen, verwenden Sie die [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e039f-106">To dequeue I/O completion packets one at a time, use the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e039f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e039f-107">Syntax</span></span>


```C++
BOOL WINAPI GetQueuedCompletionStatusEx(
  _In_  HANDLE             CompletionPort,
  _Out_ LPOVERLAPPED_ENTRY lpCompletionPortEntries,
  _In_  ULONG              ulCount,
  _Out_ PULONG             ulNumEntriesRemoved,
  _In_  DWORD              dwMilliseconds,
  _In_  BOOL               fAlertable
);
```



## <a name="parameters"></a><span data-ttu-id="e039f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e039f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e039f-109">*Completionport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e039f-109">*CompletionPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e039f-110">Ein Handle für den Abschlussport.</span><span class="sxs-lookup"><span data-stu-id="e039f-110">A handle to the completion port.</span></span> <span data-ttu-id="e039f-111">Um einen Abschlussport zu erstellen, verwenden Sie die Funktion " [**kreateiocompletionport**](createiocompletionport.md) ".</span><span class="sxs-lookup"><span data-stu-id="e039f-111">To create a completion port, use the [**CreateIoCompletionPort**](createiocompletionport.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e039f-112">*lpcompletionportentries* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e039f-112">*lpCompletionPortEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e039f-113">Bei der Eingabe verweist auf ein vorab zugeordneter Array von überlappenden [**\_ Eintrags**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="e039f-113">On input, points to a pre-allocated array of [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) structures.</span></span>

<span data-ttu-id="e039f-114">Bei der Ausgabe empfängt ein Array von [**überlappenden \_ Eintrags**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) Strukturen, die die Einträge enthalten.</span><span class="sxs-lookup"><span data-stu-id="e039f-114">On output, receives an array of [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) structures that hold the entries.</span></span> <span data-ttu-id="e039f-115">Die Anzahl der Array Elemente wird von *ulnumentriesremoved* bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e039f-115">The number of array elements is provided by *ulNumEntriesRemoved*.</span></span>

<span data-ttu-id="e039f-116">Die Anzahl von Bytes, die während der einzelnen e/a-Vorgänge übertragen werden, der Abschluss Schlüssel, der angibt, für welche Datei die einzelnen e/As aufgetreten sind, und die überlappende Struktur Adresse, die in den einzelnen ursprünglichen e/a-Vorgängen verwendet wird, werden im *lpcompletionportentries*</span><span class="sxs-lookup"><span data-stu-id="e039f-116">The number of bytes transferred during each I/O, the completion key that indicates on which file each I/O occurred, and the overlapped structure address used in each original I/O are all returned in the *lpCompletionPortEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="e039f-117">*ulcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e039f-117">*ulCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e039f-118">Die maximale Anzahl der zu entfernenden Einträge.</span><span class="sxs-lookup"><span data-stu-id="e039f-118">The maximum number of entries to remove.</span></span>

</dd> <dt>

<span data-ttu-id="e039f-119">*ulnumentriesentfernt* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e039f-119">*ulNumEntriesRemoved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e039f-120">Ein Zeiger auf eine Variable, die die Anzahl der tatsächlich entfernten Einträge empfängt.</span><span class="sxs-lookup"><span data-stu-id="e039f-120">A pointer to a variable that receives the number of entries actually removed.</span></span>

</dd> <dt>

<span data-ttu-id="e039f-121">*dwmillisekunden* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e039f-121">*dwMilliseconds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e039f-122">Die Anzahl der Millisekunden, die der Aufrufer warten soll, bis ein abschlusspaket am Abschlussport angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e039f-122">The number of milliseconds that the caller is willing to wait for a completion packet to appear at the completion port.</span></span> <span data-ttu-id="e039f-123">Wenn ein Vervollständigungs Paket nicht innerhalb der angegebenen Zeit angezeigt wird, tritt bei der Funktion ein Timeout auf, und es wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e039f-123">If a completion packet does not appear within the specified time, the function times out and returns **FALSE**.</span></span>

<span data-ttu-id="e039f-124">Wenn *dwMilliseconds* **unendlich** (0xFFFFFFFF) ist, tritt für die Funktion kein Timeout auf. Wenn *dwMilliseconds* gleich 0 (null) ist und kein e/a-Vorgang zum Entfernen der Warteschlange vorhanden ist, tritt für die Funktion sofort ein Timeout ein.</span><span class="sxs-lookup"><span data-stu-id="e039f-124">If *dwMilliseconds* is **INFINITE** (0xFFFFFFFF), the function will never time out. If *dwMilliseconds* is zero and there is no I/O operation to dequeue, the function will time out immediately.</span></span>

</dd> <dt>

<span data-ttu-id="e039f-125">*falertable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e039f-125">*fAlertable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e039f-126">Wenn dieser Parameter **false** ist, wird die Funktion erst zurückgegeben, wenn der Timeout Zeitraum abgelaufen ist oder ein Eintrag abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e039f-126">If this parameter is **FALSE**, the function does not return until the time-out period has elapsed or an entry is retrieved.</span></span>

<span data-ttu-id="e039f-127">Wenn der-Parameter den Wert **true** hat und keine Einträge verfügbar sind, führt die Funktion eine warterattabellenwartezeit aus.</span><span class="sxs-lookup"><span data-stu-id="e039f-127">If the parameter is **TRUE** and there are no available entries, the function performs an alertable wait.</span></span> <span data-ttu-id="e039f-128">Der Thread gibt zurück, wenn das System eine e/a-Abschluss Routine oder APC in die Warteschlange für den Thread fügt und der Thread die Funktion ausführt.</span><span class="sxs-lookup"><span data-stu-id="e039f-128">The thread returns when the system queues an I/O completion routine or APC to the thread and the thread executes the function.</span></span>

<span data-ttu-id="e039f-129">Eine Vervollständigungs Routine wird in die Warteschlange eingereiht, wenn die Funktion "read [**fileex**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) " oder " [**schreitefileex**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) ", in der Sie angegeben wurde, abgeschlossen wurde und der aufrufende Thread der Thread ist, der den Vorgang initiiert</span><span class="sxs-lookup"><span data-stu-id="e039f-129">A completion routine is queued when the [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) or [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) function in which it was specified has completed, and the calling thread is the thread that initiated the operation.</span></span> <span data-ttu-id="e039f-130">Ein APC wird in die Warteschlange eingereiht, wenn [**queueuserapc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e039f-130">An APC is queued when you call [**QueueUserAPC**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e039f-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e039f-131">Return value</span></span>

<span data-ttu-id="e039f-132">Gibt einen Wert ungleich 0 (**true**) zurück, wenn erfolgreich, andernfalls 0 (**false**).</span><span class="sxs-lookup"><span data-stu-id="e039f-132">Returns nonzero (**TRUE**) if successful or zero (**FALSE**) otherwise.</span></span>

<span data-ttu-id="e039f-133">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="e039f-133">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="e039f-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e039f-134">Remarks</span></span>

<span data-ttu-id="e039f-135">Diese Funktion ordnet einen Thread dem angegebenen Abschlussport zu.</span><span class="sxs-lookup"><span data-stu-id="e039f-135">This function associates a thread with the specified completion port.</span></span> <span data-ttu-id="e039f-136">Einem Thread kann höchstens ein Abschlussport zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="e039f-136">A thread can be associated with at most one completion port.</span></span>

<span data-ttu-id="e039f-137">Diese Funktion gibt **true** zurück, wenn mindestens ein ausstehender e/a-Vorgang abgeschlossen ist. es ist jedoch möglich, dass bei mindestens einem e/a-Vorgang ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e039f-137">This function returns **TRUE** when at least one pending I/O is completed, but it is possible that one or more I/O operations failed.</span></span> <span data-ttu-id="e039f-138">Beachten Sie, dass es für den Benutzer dieser Funktion ist, die Liste der zurückgegebenen Einträge im *lpcompletionportentries* -Parameter zu überprüfen, um zu bestimmen, welche von Ihnen mögliche fehlgeschlagene e/a-Vorgänge entsprechen, indem Sie den Status des **lpoverllapp** -Elements in jedem überlappenden [**\_ Eintrag**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry)betrachten.</span><span class="sxs-lookup"><span data-stu-id="e039f-138">Note that it is up to the user of this function to check the list of returned entries in the *lpCompletionPortEntries* parameter to determine which of them correspond to any possible failed I/O operations by looking at the status contained in the **lpOverlapped** member in each [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry).</span></span>

<span data-ttu-id="e039f-139">Diese Funktion gibt **false** zurück, wenn kein e/a-Vorgang aus der Warteschlange entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="e039f-139">This function returns **FALSE** when no I/O operation was dequeued.</span></span> <span data-ttu-id="e039f-140">Dies bedeutet in der Regel, dass bei der Verarbeitung der Parameter für diesen Befehl ein Fehler aufgetreten ist oder dass der *completionport* -Handle geschlossen oder anderweitig ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="e039f-140">This typically means that an error occurred while processing the parameters to this call, or that the *CompletionPort* handle was closed or is otherwise invalid.</span></span> <span data-ttu-id="e039f-141">Die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion stellt erweiterte Fehlerinformationen bereit.</span><span class="sxs-lookup"><span data-stu-id="e039f-141">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function provides extended error information.</span></span>

<span data-ttu-id="e039f-142">Wenn beim Aufrufen von " [**GetQueuedCompletionStatus usex**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) " ein Fehler auftritt, weil das zugeordnete Handle geschlossen ist, gibt die Funktion " **false** " zurück, und " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " gibt einen Fehler zurück, der **\_ abgebrochen \_ \_** wurde</span><span class="sxs-lookup"><span data-stu-id="e039f-142">If a call to [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) fails because the handle associated with it is closed, the function returns **FALSE** and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return **ERROR\_ABANDONED\_WAIT\_0**.</span></span>

<span data-ttu-id="e039f-143">Server Anwendungen können mehrere Threads aufweisen, die die Funktion **GetQueuedCompletionStatus usex** für denselben Abschlussport aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e039f-143">Server applications may have several threads calling the **GetQueuedCompletionStatusEx** function for the same completion port.</span></span> <span data-ttu-id="e039f-144">Wenn e/a-Vorgänge durchgeführt werden, werden Sie in der Reihenfolge für die erstmaligen Ausführung in die Warteschlange dieses Ports eingereiht.</span><span class="sxs-lookup"><span data-stu-id="e039f-144">As I/O operations complete, they are queued to this port in first-in-first-out order.</span></span> <span data-ttu-id="e039f-145">Wenn ein Thread aktiv auf diesen-Befehl wartet, schließt mindestens eine in der Warteschlange befindliche Anforderung den-Befehl nur für diesen Thread aus.</span><span class="sxs-lookup"><span data-stu-id="e039f-145">If a thread is actively waiting on this call, one or more queued requests complete the call for that thread only.</span></span>

<span data-ttu-id="e039f-146">Weitere Informationen zu e/a-Abschluss Port Theorie, Verwendung und zugehörigen Funktionen finden Sie unter e [/](i-o-completion-ports.md)a-Abschlussports.</span><span class="sxs-lookup"><span data-stu-id="e039f-146">For more information on I/O completion port theory, usage, and associated functions, see [I/O Completion Ports](i-o-completion-ports.md).</span></span>

<span data-ttu-id="e039f-147">In Windows 8 und Windows Server 2012 wird diese Funktion von den folgenden Technologien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e039f-147">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="e039f-148">Technologie</span><span class="sxs-lookup"><span data-stu-id="e039f-148">Technology</span></span>                                           | <span data-ttu-id="e039f-149">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="e039f-149">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="e039f-150">Server Message Block-Protokoll (SMB) 3,0</span><span class="sxs-lookup"><span data-stu-id="e039f-150">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="e039f-151">Ja</span><span class="sxs-lookup"><span data-stu-id="e039f-151">Yes</span></span><br/> |
| <span data-ttu-id="e039f-152">SMB 3,0 transparent Failover (TFO)</span><span class="sxs-lookup"><span data-stu-id="e039f-152">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="e039f-153">Ja</span><span class="sxs-lookup"><span data-stu-id="e039f-153">Yes</span></span><br/> |
| <span data-ttu-id="e039f-154">SMB 3,0 mit Dateifreigaben mit horizontaler Skalierung (also)</span><span class="sxs-lookup"><span data-stu-id="e039f-154">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="e039f-155">Ja</span><span class="sxs-lookup"><span data-stu-id="e039f-155">Yes</span></span><br/> |
| <span data-ttu-id="e039f-156">Freigegebenes Clustervolume Datei System (csvfs)</span><span class="sxs-lookup"><span data-stu-id="e039f-156">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="e039f-157">Ja</span><span class="sxs-lookup"><span data-stu-id="e039f-157">Yes</span></span><br/> |
| <span data-ttu-id="e039f-158">Robustes Dateisystem (Resilient File System, ReFS)</span><span class="sxs-lookup"><span data-stu-id="e039f-158">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="e039f-159">Ja</span><span class="sxs-lookup"><span data-stu-id="e039f-159">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e039f-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e039f-160">Requirements</span></span>



| <span data-ttu-id="e039f-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e039f-161">Requirement</span></span> | <span data-ttu-id="e039f-162">Wert</span><span class="sxs-lookup"><span data-stu-id="e039f-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e039f-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e039f-163">Minimum supported client</span></span><br/> | <span data-ttu-id="e039f-164">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e039f-164">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="e039f-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e039f-165">Minimum supported server</span></span><br/> | <span data-ttu-id="e039f-166">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e039f-166">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="e039f-167">Header</span><span class="sxs-lookup"><span data-stu-id="e039f-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="e039f-168"><dt>Ioapi. h (Include Windows. h); </dt> <dt>Winbase. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e039f-168"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e039f-169">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e039f-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="e039f-170"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e039f-170"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="e039f-171">DLL</span><span class="sxs-lookup"><span data-stu-id="e039f-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e039f-172"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e039f-172"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="e039f-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e039f-173">See also</span></span>

<dl> <dt>

<span data-ttu-id="e039f-174">**Übersichts Themen**</span><span class="sxs-lookup"><span data-stu-id="e039f-174">**Overview Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="e039f-175">Dateiverwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="e039f-175">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="e039f-176">E/a-Abschlussports</span><span class="sxs-lookup"><span data-stu-id="e039f-176">I/O Completion Ports</span></span>](i-o-completion-ports.md)
</dt> <dt>

[<span data-ttu-id="e039f-177">Verwenden der Windows-Header</span><span class="sxs-lookup"><span data-stu-id="e039f-177">Using the Windows Headers</span></span>](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

<span data-ttu-id="e039f-178">**Funktionen**</span><span class="sxs-lookup"><span data-stu-id="e039f-178">**Functions**</span></span>
</dt> <dt>

[<span data-ttu-id="e039f-179">**Connectnamedpipe**</span><span class="sxs-lookup"><span data-stu-id="e039f-179">**ConnectNamedPipe**</span></span>](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
</dt> <dt>

[<span data-ttu-id="e039f-180">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="e039f-180">**CreateIoCompletionPort**</span></span>](createiocompletionport.md)
</dt> <dt>

[<span data-ttu-id="e039f-181">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="e039f-181">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="e039f-182">**GetQueuedCompletionStatus usex**</span><span class="sxs-lookup"><span data-stu-id="e039f-182">**GetQueuedCompletionStatusEx**</span></span>](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[<span data-ttu-id="e039f-183">**Lockfileex**</span><span class="sxs-lookup"><span data-stu-id="e039f-183">**LockFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[<span data-ttu-id="e039f-184">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="e039f-184">**ReadFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[<span data-ttu-id="e039f-185">**' PostQueuedCompletionStatus '**</span><span class="sxs-lookup"><span data-stu-id="e039f-185">**PostQueuedCompletionStatus**</span></span>](postqueuedcompletionstatus.md)
</dt> <dt>

[<span data-ttu-id="e039f-186">**Transactnamedpipe**</span><span class="sxs-lookup"><span data-stu-id="e039f-186">**TransactNamedPipe**</span></span>](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
</dt> <dt>

[<span data-ttu-id="e039f-187">**WaitCommEvent**</span><span class="sxs-lookup"><span data-stu-id="e039f-187">**WaitCommEvent**</span></span>](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
</dt> <dt>

[<span data-ttu-id="e039f-188">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="e039f-188">**WriteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> </dl>

 

