---
description: Markiert ausstehende synchrone e/a-Vorgänge, die vom angegebenen Thread ausgegeben werden, als abgebrochen.
ms.assetid: f362c8b2-2193-443e-bb69-78f8b4147117
title: CancelSynchronousIo-Funktion (ioapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelSynchronousIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3e0c1596603ef7c0d13362c2608cc59b88d366fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530005"
---
# <a name="cancelsynchronousio-function"></a><span data-ttu-id="1bf1e-103">CancelSynchronousIo-Funktion</span><span class="sxs-lookup"><span data-stu-id="1bf1e-103">CancelSynchronousIo function</span></span>

<span data-ttu-id="1bf1e-104">Markiert ausstehende synchrone e/a-Vorgänge, die vom angegebenen Thread ausgegeben werden, als abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="1bf1e-104">Marks pending synchronous I/O operations that are issued by the specified thread as canceled.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bf1e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bf1e-105">Syntax</span></span>


```C++
BOOL WINAPI CancelSynchronousIo(
  _In_ HANDLE hThread
);
```



## <a name="parameters"></a><span data-ttu-id="1bf1e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bf1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bf1e-107">*hThread* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1bf1e-107">*hThread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bf1e-108">Ein Handle für den Thread.</span><span class="sxs-lookup"><span data-stu-id="1bf1e-108">A handle to the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bf1e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1bf1e-109">Return value</span></span>

<span data-ttu-id="1bf1e-110">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.</span><span class="sxs-lookup"><span data-stu-id="1bf1e-110">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="1bf1e-111">Wenn die Funktion fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1bf1e-111">If the function fails, the return value is 0 (zero).</span></span> <span data-ttu-id="1bf1e-112">Um erweiterte Fehlerinformationen abzurufen, müssen Sie die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1bf1e-112">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="1bf1e-113">Wenn diese Funktion eine abzubrechende Anforderung nicht finden kann, ist der Rückgabewert 0 (null), und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den **Fehler " \_ nicht \_ gefunden**" zurück.</span><span class="sxs-lookup"><span data-stu-id="1bf1e-113">If this function cannot find a request to cancel, the return value is 0 (zero), and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bf1e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1bf1e-114">Remarks</span></span>

<span data-ttu-id="1bf1e-115">Der Aufrufer muss über das Zugriffsrecht " [Thread \_ Beenden](/windows/desktop/ProcThread/thread-security-and-access-rights) " verfügen.</span><span class="sxs-lookup"><span data-stu-id="1bf1e-115">The caller must have the [THREAD\_TERMINATE](/windows/desktop/ProcThread/thread-security-and-access-rights) access right.</span></span>

<span data-ttu-id="1bf1e-116">Wenn für den angegebenen Thread ausstehende e/a-Vorgänge ausgeführt werden, markiert die Funktion " **CancelSynchronousIo** " Sie für den Abbruch.</span><span class="sxs-lookup"><span data-stu-id="1bf1e-116">If there are any pending I/O operations in progress for the specified thread, the **CancelSynchronousIo** function marks them for cancellation.</span></span> <span data-ttu-id="1bf1e-117">Die meisten Vorgänge können sofort abgebrochen werden. andere Vorgänge können fortgesetzt werden, bevor Sie tatsächlich abgebrochen werden, und der Aufrufer wird benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="1bf1e-117">Most types of operations can be canceled immediately; other operations can continue toward completion before they are actually canceled and the caller is notified.</span></span> <span data-ttu-id="1bf1e-118">Die **CancelSynchronousIo** -Funktion wartet nicht, bis alle abgebrochenen Vorgänge beendet sind.</span><span class="sxs-lookup"><span data-stu-id="1bf1e-118">The **CancelSynchronousIo** function does not wait for all canceled operations to complete.</span></span> <span data-ttu-id="1bf1e-119">Weitere Informationen finden Sie unter e [/a-Abschluss-/Abbruch Richtlinien](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span><span class="sxs-lookup"><span data-stu-id="1bf1e-119">For more information, see [I/O Completion/Cancellation Guidelines](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span></span>

<span data-ttu-id="1bf1e-120">Der Vorgang, der abgebrochen wird, wird mit einem von drei Status abgeschlossen. Sie müssen den Abschluss Status überprüfen, um den Abschluss Status zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="1bf1e-120">The operation being canceled is completed with one of three statuses; you must check the completion status to determine the completion state.</span></span> <span data-ttu-id="1bf1e-121">Die drei Status lauten:</span><span class="sxs-lookup"><span data-stu-id="1bf1e-121">The three statuses are:</span></span>

-   <span data-ttu-id="1bf1e-122">**Der Vorgang wurde normal abgeschlossen.**</span><span class="sxs-lookup"><span data-stu-id="1bf1e-122">**The operation completed normally.**</span></span> <span data-ttu-id="1bf1e-123">Dies kann auch auftreten, wenn der Vorgang abgebrochen wurde, da die Abbruch Anforderung möglicherweise nicht rechtzeitig übermittelt wurde, um den Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="1bf1e-123">This can occur even if the operation was canceled, because the cancel request might not have been submitted in time to cancel the operation.</span></span>
-   <span data-ttu-id="1bf1e-124">**Der Vorgang wurde abgebrochen.**</span><span class="sxs-lookup"><span data-stu-id="1bf1e-124">**The operation was canceled.**</span></span> <span data-ttu-id="1bf1e-125">Die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt einen **\_ \_ abgebrochenen Fehler Vorgang** zurück.</span><span class="sxs-lookup"><span data-stu-id="1bf1e-125">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_OPERATION\_ABORTED**.</span></span>
-   <span data-ttu-id="1bf1e-126">**Der Vorgang ist mit einem weiteren Fehler fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="1bf1e-126">**The operation failed with another error.**</span></span> <span data-ttu-id="1bf1e-127">Die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt den relevanten Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="1bf1e-127">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns the relevant error code.</span></span>

<span data-ttu-id="1bf1e-128">In Windows 8 und Windows Server 2012 wird diese Funktion von den folgenden Technologien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1bf1e-128">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="1bf1e-129">Technologie</span><span class="sxs-lookup"><span data-stu-id="1bf1e-129">Technology</span></span>                                           | <span data-ttu-id="1bf1e-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="1bf1e-130">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="1bf1e-131">Server Message Block-Protokoll (SMB) 3,0</span><span class="sxs-lookup"><span data-stu-id="1bf1e-131">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="1bf1e-132">Ja</span><span class="sxs-lookup"><span data-stu-id="1bf1e-132">Yes</span></span><br/> |
| <span data-ttu-id="1bf1e-133">SMB 3,0 transparent Failover (TFO)</span><span class="sxs-lookup"><span data-stu-id="1bf1e-133">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="1bf1e-134">Ja</span><span class="sxs-lookup"><span data-stu-id="1bf1e-134">Yes</span></span><br/> |
| <span data-ttu-id="1bf1e-135">SMB 3,0 mit Dateifreigaben mit horizontaler Skalierung (also)</span><span class="sxs-lookup"><span data-stu-id="1bf1e-135">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="1bf1e-136">Ja</span><span class="sxs-lookup"><span data-stu-id="1bf1e-136">Yes</span></span><br/> |
| <span data-ttu-id="1bf1e-137">Freigegebenes Clustervolume Datei System (csvfs)</span><span class="sxs-lookup"><span data-stu-id="1bf1e-137">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="1bf1e-138">Ja</span><span class="sxs-lookup"><span data-stu-id="1bf1e-138">Yes</span></span><br/> |
| <span data-ttu-id="1bf1e-139">Robustes Dateisystem (Resilient File System, ReFS)</span><span class="sxs-lookup"><span data-stu-id="1bf1e-139">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="1bf1e-140">Ja</span><span class="sxs-lookup"><span data-stu-id="1bf1e-140">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1bf1e-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1bf1e-141">Requirements</span></span>



| <span data-ttu-id="1bf1e-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1bf1e-142">Requirement</span></span> | <span data-ttu-id="1bf1e-143">Wert</span><span class="sxs-lookup"><span data-stu-id="1bf1e-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bf1e-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1bf1e-144">Minimum supported client</span></span><br/> | <span data-ttu-id="1bf1e-145">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1bf1e-145">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                          |
| <span data-ttu-id="1bf1e-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1bf1e-146">Minimum supported server</span></span><br/> | <span data-ttu-id="1bf1e-147">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1bf1e-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="1bf1e-148">Header</span><span class="sxs-lookup"><span data-stu-id="1bf1e-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bf1e-149"><dt>Ioapi. h (Include Windows. h); </dt> <dt>Winbase. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1bf1e-149"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1bf1e-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1bf1e-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="1bf1e-151"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bf1e-151"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="1bf1e-152">DLL</span><span class="sxs-lookup"><span data-stu-id="1bf1e-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bf1e-153"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bf1e-153"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="1bf1e-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1bf1e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bf1e-155">**CancelIo**</span><span class="sxs-lookup"><span data-stu-id="1bf1e-155">**CancelIo**</span></span>](cancelio.md)
</dt> <dt>

[<span data-ttu-id="1bf1e-156">**CancelIoEx**</span><span class="sxs-lookup"><span data-stu-id="1bf1e-156">**CancelIoEx**</span></span>](cancelioex-func.md)
</dt> <dt>

[<span data-ttu-id="1bf1e-157">Dateiverwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="1bf1e-157">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="1bf1e-158">Synchrone und asynchrone e/a</span><span class="sxs-lookup"><span data-stu-id="1bf1e-158">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

