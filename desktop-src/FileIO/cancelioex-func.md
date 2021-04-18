---
description: Markiert alle ausstehenden e/a-Vorgänge für das angegebene Datei handle. Die-Funktion bricht nur e/a-Vorgänge im aktuellen Prozess ab, unabhängig davon, welcher Thread den e/a-Vorgang erstellt hat.
ms.assetid: a2ce13b8-7da6-4848-848d-901d9667c2e3
title: CancelIoEx-Funktion (ioapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIoEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3de44762ad9a230a9d8cc410c4ba3ae7c2d9964e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358398"
---
# <a name="cancelioex-function"></a><span data-ttu-id="7ccf3-104">CancelIoEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="7ccf3-104">CancelIoEx function</span></span>

<span data-ttu-id="7ccf3-105">Markiert alle ausstehenden e/a-Vorgänge für das angegebene Datei handle.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-105">Marks any outstanding I/O operations for the specified file handle.</span></span> <span data-ttu-id="7ccf3-106">Die-Funktion bricht nur e/a-Vorgänge im aktuellen Prozess ab, unabhängig davon, welcher Thread den e/a-Vorgang erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-106">The function only cancels I/O operations in the current process, regardless of which thread created the I/O operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ccf3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ccf3-107">Syntax</span></span>


```C++
BOOL WINAPI CancelIoEx(
  _In_     HANDLE       hFile,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a><span data-ttu-id="7ccf3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ccf3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ccf3-109">*hFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ccf3-109">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ccf3-110">Ein Handle für die Datei.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-110">A handle to the file.</span></span>

</dd> <dt>

<span data-ttu-id="7ccf3-111">*lpoverlgetauscht* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="7ccf3-111">*lpOverlapped* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7ccf3-112">Ein Zeiger auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Datenstruktur, die die Daten enthält, die für asynchrone e/a verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-112">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) data structure that contains the data used for asynchronous I/O.</span></span>

<span data-ttu-id="7ccf3-113">Wenn dieser Parameter **null** ist, werden alle e/a-Anforderungen für den *hFile* -Parameter abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-113">If this parameter is **NULL**, all I/O requests for the *hFile* parameter are canceled.</span></span>

<span data-ttu-id="7ccf3-114">Wenn dieser Parameter nicht **null** ist, werden nur die spezifischen e/a-Anforderungen, die für die Datei mit der *angegebenen über* Lapp enden überlappenden Struktur ausgegeben wurden, als abgebrochen markiert. Dies bedeutet, dass Sie eine oder mehrere Anforderungen abbrechen können, während die [**CancelIo**](cancelio.md) -Funktion alle ausstehenden Anforderungen eines Datei Handles abbricht.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-114">If this parameter is not **NULL**, only those specific I/O requests that were issued for the file with the specified *lpOverlapped* overlapped structure are marked as canceled, meaning that you can cancel one or more requests, while the [**CancelIo**](cancelio.md) function cancels all outstanding requests on a file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ccf3-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ccf3-115">Return value</span></span>

<span data-ttu-id="7ccf3-116">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-116">If the function succeeds, the return value is nonzero.</span></span> <span data-ttu-id="7ccf3-117">Der Abbruch Vorgang für alle ausstehenden e/a-Vorgänge, die vom aufrufenden Prozess für das angegebene Datei Handle ausgegeben wurden, wurde erfolgreich angefordert.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-117">The cancel operation for all pending I/O operations issued by the calling process for the specified file handle was successfully requested.</span></span> <span data-ttu-id="7ccf3-118">Die Anwendung darf die [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur, die den abgebrochenen e/a-Vorgängen zugeordnet ist, nicht freigeben oder wieder verwenden, bis Sie abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-118">The application must not free or reuse the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure associated with the canceled I/O operations until they have completed.</span></span> <span data-ttu-id="7ccf3-119">Der Thread kann die [**gedeverlappedresult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) -Funktion verwenden, um zu bestimmen, wann die e/a-Vorgänge selbst abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-119">The thread can use the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function to determine when the I/O operations themselves have been completed.</span></span>

<span data-ttu-id="7ccf3-120">Wenn die Funktion fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="7ccf3-120">If the function fails, the return value is 0 (zero).</span></span> <span data-ttu-id="7ccf3-121">Um erweiterte Fehlerinformationen abzurufen, müssen Sie die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-121">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="7ccf3-122">Wenn diese Funktion eine abzubrechende Anforderung nicht finden kann, ist der Rückgabewert 0 (null), und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den **Fehler " \_ nicht \_ gefunden**" zurück.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-122">If this function cannot find a request to cancel, the return value is 0 (zero), and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ccf3-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ccf3-123">Remarks</span></span>

<span data-ttu-id="7ccf3-124">Die **CancelIoEx** -Funktion ermöglicht es Ihnen, Anforderungen in anderen Threads als dem aufrufenden Thread abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-124">The **CancelIoEx** function allows you to cancel requests in threads other than the calling thread.</span></span> <span data-ttu-id="7ccf3-125">Die [**CancelIo**](cancelio.md) -Funktion bricht nur Anforderungen im gleichen Thread ab, der die **CancelIo** -Funktion aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-125">The [**CancelIo**](cancelio.md) function only cancels requests in the same thread that called the **CancelIo** function.</span></span> <span data-ttu-id="7ccf3-126">**CancelIoEx** bricht nur ausstehende e/a-Vorgänge für das Handle ab, ändert den Zustand des Handles nicht. Dies bedeutet, dass Sie sich nicht auf den Zustand des Handles verlassen können, weil Sie nicht wissen, ob der Vorgang erfolgreich abgeschlossen wurde oder abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-126">**CancelIoEx** cancels only outstanding I/O on the handle, it does not change the state of the handle; this means that you cannot rely on the state of the handle because you cannot know whether the operation was completed successfully or canceled.</span></span>

<span data-ttu-id="7ccf3-127">Wenn für das angegebene Datei Handle ausstehende e/a-Vorgänge ausgeführt werden, markiert die Funktion **CancelIoEx** Sie für den Abbruch.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-127">If there are any pending I/O operations in progress for the specified file handle, the **CancelIoEx** function marks them for cancellation.</span></span> <span data-ttu-id="7ccf3-128">Die meisten Vorgänge können sofort abgebrochen werden. andere Vorgänge können fortgesetzt werden, bevor Sie tatsächlich abgebrochen werden, und der Aufrufer wird benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-128">Most types of operations can be canceled immediately; other operations can continue toward completion before they are actually canceled and the caller is notified.</span></span> <span data-ttu-id="7ccf3-129">Die **CancelIoEx** -Funktion wartet nicht, bis alle abgebrochenen Vorgänge beendet sind.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-129">The **CancelIoEx** function does not wait for all canceled operations to complete.</span></span>

<span data-ttu-id="7ccf3-130">Wenn das Datei Handle einem Abschlussport zugeordnet ist, wird ein e/a-abschlusspaket nicht in die Warteschlange des Ports eingereiht, wenn ein synchroner Vorgang erfolgreich abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-130">If the file handle is associated with a completion port, an I/O completion packet is not queued to the port if a synchronous operation is successfully canceled.</span></span> <span data-ttu-id="7ccf3-131">Für asynchrone Vorgänge, die noch ausstehen, fügt der Abbruch Vorgang ein e/a-abschlusspaket in die Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-131">For asynchronous operations still pending, the cancel operation will queue an I/O completion packet.</span></span>

<span data-ttu-id="7ccf3-132">Der Vorgang, der abgebrochen wird, wird mit einem von drei Status abgeschlossen. Sie müssen den Abschluss Status überprüfen, um den Abschluss Status zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-132">The operation being canceled is completed with one of three statuses; you must check the completion status to determine the completion state.</span></span> <span data-ttu-id="7ccf3-133">Die drei Status lauten:</span><span class="sxs-lookup"><span data-stu-id="7ccf3-133">The three statuses are:</span></span>

-   <span data-ttu-id="7ccf3-134">Der Vorgang wurde normal abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-134">The operation completed normally.</span></span> <span data-ttu-id="7ccf3-135">Dies kann auch auftreten, wenn der Vorgang abgebrochen wurde, da die Abbruch Anforderung möglicherweise nicht rechtzeitig übermittelt wurde, um den Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-135">This can occur even if the operation was canceled, because the cancel request might not have been submitted in time to cancel the operation.</span></span>
-   <span data-ttu-id="7ccf3-136">Der Vorgang wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-136">The operation was canceled.</span></span> <span data-ttu-id="7ccf3-137">Die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt einen **\_ \_ abgebrochenen Fehler Vorgang** zurück.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-137">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_OPERATION\_ABORTED**.</span></span>
-   <span data-ttu-id="7ccf3-138">Der Vorgang ist mit einem weiteren Fehler fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-138">The operation failed with another error.</span></span> <span data-ttu-id="7ccf3-139">Die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt den relevanten Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-139">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns the relevant error code.</span></span>

<span data-ttu-id="7ccf3-140">In Windows 8 und Windows Server 2012 wird diese Funktion von den folgenden Technologien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7ccf3-140">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="7ccf3-141">Technologie</span><span class="sxs-lookup"><span data-stu-id="7ccf3-141">Technology</span></span>                                           | <span data-ttu-id="7ccf3-142">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="7ccf3-142">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="7ccf3-143">Server Message Block-Protokoll (SMB) 3,0</span><span class="sxs-lookup"><span data-stu-id="7ccf3-143">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="7ccf3-144">Ja</span><span class="sxs-lookup"><span data-stu-id="7ccf3-144">Yes</span></span><br/> |
| <span data-ttu-id="7ccf3-145">SMB 3,0 transparent Failover (TFO)</span><span class="sxs-lookup"><span data-stu-id="7ccf3-145">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="7ccf3-146">Ja</span><span class="sxs-lookup"><span data-stu-id="7ccf3-146">Yes</span></span><br/> |
| <span data-ttu-id="7ccf3-147">SMB 3,0 mit Dateifreigaben mit horizontaler Skalierung (also)</span><span class="sxs-lookup"><span data-stu-id="7ccf3-147">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="7ccf3-148">Ja</span><span class="sxs-lookup"><span data-stu-id="7ccf3-148">Yes</span></span><br/> |
| <span data-ttu-id="7ccf3-149">Freigegebenes Clustervolume Datei System (csvfs)</span><span class="sxs-lookup"><span data-stu-id="7ccf3-149">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="7ccf3-150">Ja</span><span class="sxs-lookup"><span data-stu-id="7ccf3-150">Yes</span></span><br/> |
| <span data-ttu-id="7ccf3-151">Robustes Dateisystem (Resilient File System, ReFS)</span><span class="sxs-lookup"><span data-stu-id="7ccf3-151">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="7ccf3-152">Ja</span><span class="sxs-lookup"><span data-stu-id="7ccf3-152">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7ccf3-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ccf3-153">Requirements</span></span>



| <span data-ttu-id="7ccf3-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ccf3-154">Requirement</span></span> | <span data-ttu-id="7ccf3-155">Wert</span><span class="sxs-lookup"><span data-stu-id="7ccf3-155">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ccf3-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ccf3-156">Minimum supported client</span></span><br/> | <span data-ttu-id="7ccf3-157">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7ccf3-157">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="7ccf3-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ccf3-158">Minimum supported server</span></span><br/> | <span data-ttu-id="7ccf3-159">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7ccf3-159">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="7ccf3-160">Header</span><span class="sxs-lookup"><span data-stu-id="7ccf3-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ccf3-161"><dt>Ioapi. h (Include Windows. h); </dt> <dt>Winbase. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ccf3-161"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7ccf3-162">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7ccf3-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ccf3-163"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ccf3-163"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="7ccf3-164">DLL</span><span class="sxs-lookup"><span data-stu-id="7ccf3-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ccf3-165"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ccf3-165"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="7ccf3-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ccf3-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ccf3-167">**CancelIo**</span><span class="sxs-lookup"><span data-stu-id="7ccf3-167">**CancelIo**</span></span>](cancelio.md)
</dt> <dt>

[<span data-ttu-id="7ccf3-168">**CancelSynchronousIo**</span><span class="sxs-lookup"><span data-stu-id="7ccf3-168">**CancelSynchronousIo**</span></span>](cancelsynchronousio-func.md)
</dt> <dt>

[<span data-ttu-id="7ccf3-169">Abbrechen von ausstehenden e/a-Vorgängen</span><span class="sxs-lookup"><span data-stu-id="7ccf3-169">Canceling Pending I/O Operations</span></span>](canceling-pending-i-o-operations.md)
</dt> <dt>

[<span data-ttu-id="7ccf3-170">Dateiverwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="7ccf3-170">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="7ccf3-171">Synchrone und asynchrone e/a</span><span class="sxs-lookup"><span data-stu-id="7ccf3-171">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

