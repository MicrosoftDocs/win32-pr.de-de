---
description: Bricht einen registrierten warte Vorgang ab, der von der RegisterWaitForSingleObject-Funktion ausgegeben wurde.
ms.assetid: ea700e55-fce7-46cd-bb96-0c129b429d46
title: Unregisterwaitex-Funktion (threadpoollegacyapiset. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnregisterWaitEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-threadpool-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-threadpool-legacy-l1-1-0.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
ms.openlocfilehash: 30f5ad5f88bec9eb7eebff5a73d8f84f633cb249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865404"
---
# <a name="unregisterwaitex-function"></a><span data-ttu-id="e1626-103">Unregisterwaitex-Funktion</span><span class="sxs-lookup"><span data-stu-id="e1626-103">UnregisterWaitEx function</span></span>

<span data-ttu-id="e1626-104">Bricht einen registrierten warte Vorgang ab, der von der [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) -Funktion ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e1626-104">Cancels a registered wait operation issued by the [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1626-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1626-105">Syntax</span></span>


```C++
BOOL WINAPI UnregisterWaitEx(
  _In_     HANDLE WaitHandle,
  _In_opt_ HANDLE CompletionEvent
);
```



## <a name="parameters"></a><span data-ttu-id="e1626-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1626-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1626-107">*WaitHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1626-107">*WaitHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1626-108">Das Wait-Handle.</span><span class="sxs-lookup"><span data-stu-id="e1626-108">The wait handle.</span></span> <span data-ttu-id="e1626-109">Dieses Handle wird von der [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e1626-109">This handle is returned by the [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) function.</span></span>

</dd> <dt>

<span data-ttu-id="e1626-110">*CompletionEvent* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="e1626-110">*CompletionEvent* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e1626-111">Ein Handle für das Ereignis Objekt, das signalisiert werden soll, wenn die Registrierung des warte Vorgangs aufgehoben wurde.</span><span class="sxs-lookup"><span data-stu-id="e1626-111">A handle to the event object to be signaled when the wait operation has been unregistered.</span></span> <span data-ttu-id="e1626-112">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="e1626-112">This parameter can be **NULL**.</span></span>

<span data-ttu-id="e1626-113">Wenn dieser Parameter ein **ungültiger \_ handle- \_ Wert** ist, wartet die Funktion auf den Abschluss aller Rückruf Funktionen, bevor Sie zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e1626-113">If this parameter is **INVALID\_HANDLE\_VALUE**, the function waits for all callback functions to complete before returning.</span></span>

<span data-ttu-id="e1626-114">Wenn dieser Parameter **null** ist, markiert die Funktion den Timer zum Löschen und wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e1626-114">If this parameter is **NULL**, the function marks the timer for deletion and returns immediately.</span></span> <span data-ttu-id="e1626-115">Die meisten Aufrufer sollten jedoch warten, bis die Rückruffunktion vollständig ist, damit Sie alle benötigten Bereinigungs Vorgänge ausführen können.</span><span class="sxs-lookup"><span data-stu-id="e1626-115">However, most callers should wait for the callback function to complete so they can perform any needed cleanup.</span></span>

<span data-ttu-id="e1626-116">Wenn der Aufrufer dieses Ereignis bereitstellt und die Funktion erfolgreich ist oder die Funktion mit der Fehler-e/a **\_ \_ Ausstehend** ausfällt, schließen Sie das Ereignis erst, wenn es signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e1626-116">If the caller provides this event and the function succeeds or the function fails with **ERROR\_IO\_PENDING**, do not close the event until it is signaled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1626-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e1626-117">Return value</span></span>

<span data-ttu-id="e1626-118">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.</span><span class="sxs-lookup"><span data-stu-id="e1626-118">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="e1626-119">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="e1626-119">If the function fails, the return value is zero.</span></span> <span data-ttu-id="e1626-120">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="e1626-120">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="e1626-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1626-121">Remarks</span></span>

<span data-ttu-id="e1626-122">Es ist nicht möglich, einen blockierenden Aufrufs von **unregisterwaitex** innerhalb einer Rückruffunktion für denselben warte Vorgang durchführen.</span><span class="sxs-lookup"><span data-stu-id="e1626-122">You cannot make a blocking call to **UnregisterWaitEx** from within a callback function for the same wait operation.</span></span> <span data-ttu-id="e1626-123">Andernfalls wartet der Rückruf darauf, dass er abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="e1626-123">Otherwise, the callback will be waiting for itself to finish.</span></span> <span data-ttu-id="e1626-124">Im Allgemeinen wird durch einen blockierenden Aufrufs von **unregisterwaitex** eine Abhängigkeit zwischen dem aktuellen Thread und dem Rückruf erstellt. Wenn Sie also einen blockierenden aufheben-Aufrufs bei einem anderen warte Vorgang ausführen möchten, müssen Sie sicherstellen, dass die Rückruf Funktionen nicht voneinander abhängen und dass der zweite warte Vorgang nicht auch einen blockierenden aufheben-Aufrufs für den ersten Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="e1626-124">In general, a blocking call to **UnregisterWaitEx** creates a dependency between the current thread and the callback, so to make a blocking unregister call on another wait operation, you must ensure that the callback functions do not depend on one another and that the second wait operation does not also perform a blocking unregister call on the first operation.</span></span>

<span data-ttu-id="e1626-125">Gehen Sie beim Erstellen eines **unregisterwaitex** -Aufrufs für einen persistenten Thread vorsichtig vor.</span><span class="sxs-lookup"><span data-stu-id="e1626-125">Be careful when making a blocking **UnregisterWaitEx** call on a persistent thread.</span></span> <span data-ttu-id="e1626-126">Wenn der Warte Vorgang, dessen Registrierung aufgehoben wurde, mit dem **WT \_ executeinpersistentthread** erstellt wurde, kann ein Deadlock auftreten.</span><span class="sxs-lookup"><span data-stu-id="e1626-126">If the wait operation being unregistered was created with **WT\_EXECUTEINPERSISTENTTHREAD**, a deadlock may occur.</span></span>

<span data-ttu-id="e1626-127">Nach dem nicht blockierenden Aufrufen von **unregisterwaitex** können keine neuen Rückruf Funktionen in eine Warteschlange eingereiht werden, die mit *WaitHandle* verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="e1626-127">After making non-blocking call to **UnregisterWaitEx**, no new callback functions associated with *WaitHandle* can be queued.</span></span> <span data-ttu-id="e1626-128">Möglicherweise gibt es jedoch ausstehende Rückruf Funktionen, die bereits in die Warteschlange eingereiht wurden.</span><span class="sxs-lookup"><span data-stu-id="e1626-128">However, there may be pending callback functions already queued to worker threads.</span></span>

<span data-ttu-id="e1626-129">Unter bestimmten Bedingungen tritt bei der Funktion ein **Fehler auf \_ , \_** Wenn *CompletionEvent* **null** ist.</span><span class="sxs-lookup"><span data-stu-id="e1626-129">Under some conditions, the function will fail with **ERROR\_IO\_PENDING** if *CompletionEvent* is **NULL**.</span></span> <span data-ttu-id="e1626-130">Dies weist darauf hin, dass ausstehende Rückruf Funktionen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e1626-130">This indicates that there are outstanding callback functions.</span></span> <span data-ttu-id="e1626-131">Diese Rückrufe werden entweder ausgeführt oder befinden sich in der Mitte der Ausführung.</span><span class="sxs-lookup"><span data-stu-id="e1626-131">Those callbacks either will execute or are in the middle of executing.</span></span>

<span data-ttu-id="e1626-132">Wenn *CompletionEvent* ein Handle für ein Ereignis ist, das vom Aufrufer bereitgestellt wird, ist es möglich, dass die Funktion erfolgreich ausgeführt wird, dass die Fehler-e/a **\_ \_ Ausstehend** ist oder mit einem anderen Fehlercode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="e1626-132">If *CompletionEvent* is a handle to an event provided by the caller, it is possible for the function to succeed, fail with **ERROR\_IO\_PENDING**, or fail with a different error code.</span></span> <span data-ttu-id="e1626-133">Wenn die Funktion erfolgreich ausgeführt wird oder wenn die Funktion fehlschlägt, wenn die Fehler-e/a aussteht, sollte der Aufrufer immer warten, bis das Ereignis signalisiert wird, um das Ereignis **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="e1626-133">If the function succeeds, or if the function fails with **ERROR\_IO\_PENDING**, the caller should always wait until the event is signaled to close the event.</span></span> <span data-ttu-id="e1626-134">Wenn die Funktion mit einem anderen Fehlercode fehlschlägt, müssen Sie nicht warten, bis das Ereignis signalisiert wird, um das Ereignis zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e1626-134">If the function fails with a different error code, it is not necessary to wait until the event is signaled to close the event.</span></span>

<span data-ttu-id="e1626-135">**Windows XP:** Wenn *CompletionEvent* ein Handle für ein Ereignis ist, das vom Aufrufer bereitgestellt wird, und die Funktion mit dem **\_ \_ ausstehenden Fehler**-e/a-Vorgang fehlschlägt, sollte der Aufrufer warten, bis das Ereignis signalisiert wird,</span><span class="sxs-lookup"><span data-stu-id="e1626-135">**Windows XP:** If *CompletionEvent* is a handle to an event provided by the caller and the function fails with **ERROR\_IO\_PENDING**, the caller should wait until the event is signaled to close the event.</span></span> <span data-ttu-id="e1626-136">Dieses Verhalten hat sich seit Windows Vista geändert.</span><span class="sxs-lookup"><span data-stu-id="e1626-136">This behavior changed starting with Windows Vista.</span></span>

<span data-ttu-id="e1626-137">Um eine Anwendung zu kompilieren, die diese Funktion verwendet, definieren Sie **\_ Win32 \_ Winnt** als 0x0500 sein oder höher.</span><span class="sxs-lookup"><span data-stu-id="e1626-137">To compile an application that uses this function, define **\_WIN32\_WINNT** as 0x0500 or later.</span></span> <span data-ttu-id="e1626-138">Weitere Informationen finden Sie unter [Verwenden der Windows-Header](../winprog/using-the-windows-headers.md).</span><span class="sxs-lookup"><span data-stu-id="e1626-138">For more information, see [Using the Windows Headers](../winprog/using-the-windows-headers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1626-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1626-139">Requirements</span></span>



| <span data-ttu-id="e1626-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1626-140">Requirement</span></span> | <span data-ttu-id="e1626-141">Wert</span><span class="sxs-lookup"><span data-stu-id="e1626-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1626-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e1626-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e1626-143">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e1626-143">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="e1626-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e1626-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e1626-145">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e1626-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="e1626-146">Header</span><span class="sxs-lookup"><span data-stu-id="e1626-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1626-147"><dt>Threadpoollegacyapiset. h unter Windows 8 und Windows Server 2012 (Include Windows. h); </dt> <dt>Winbase. h unter Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP und Windows Server 2003 (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1626-147"><dt>Threadpoollegacyapiset.h on Windows 8 and Windows Server 2012 (include Windows.h); </dt> <dt>WinBase.h on Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003 (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e1626-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e1626-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="e1626-149"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1626-149"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="e1626-150">DLL</span><span class="sxs-lookup"><span data-stu-id="e1626-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1626-151"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1626-151"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a><span data-ttu-id="e1626-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1626-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1626-153">**Von RegisterWaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="e1626-153">**RegisterWaitForSingleObject**</span></span>](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)
</dt> <dt>

[<span data-ttu-id="e1626-154">Synchronisierungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="e1626-154">Synchronization Functions</span></span>](synchronization-functions.md)
</dt> <dt>

[<span data-ttu-id="e1626-155">Pooling von Threads</span><span class="sxs-lookup"><span data-stu-id="e1626-155">Thread Pooling</span></span>](../procthread/thread-pooling.md)
</dt> </dl>

 

 
