---
description: Bricht alle ausstehenden Eingabe-und Ausgabe Vorgänge (e/a-Vorgänge) ab, die vom aufrufenden Thread für die angegebene Datei ausgegeben werden.
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
title: CancelIo-Funktion (ioapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: adb1ab95b30b31670a6ff5a4cc0e0205943f7683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367878"
---
# <a name="cancelio-function"></a><span data-ttu-id="29911-103">CancelIo-Funktion</span><span class="sxs-lookup"><span data-stu-id="29911-103">CancelIo function</span></span>

<span data-ttu-id="29911-104">Bricht alle ausstehenden Eingabe-und Ausgabe Vorgänge (e/a-Vorgänge) ab, die vom aufrufenden Thread für die angegebene Datei ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="29911-104">Cancels all pending input and output (I/O) operations that are issued by the calling thread for the specified file.</span></span> <span data-ttu-id="29911-105">Mit der-Funktion werden keine e/a-Vorgänge abgebrochen, die von anderen Threads für ein Datei Handle ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="29911-105">The function does not cancel I/O operations that other threads issue for a file handle.</span></span>

<span data-ttu-id="29911-106">Zum Abbrechen von e/a-Vorgängen von einem anderen Thread verwenden Sie die Funktion [**CancelIoEx**](cancelioex-func.md) .</span><span class="sxs-lookup"><span data-stu-id="29911-106">To cancel I/O operations from another thread, use the [**CancelIoEx**](cancelioex-func.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="29911-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="29911-107">Syntax</span></span>


```C++
BOOL WINAPI CancelIo(
  _In_ HANDLE hFile
);
```



## <a name="parameters"></a><span data-ttu-id="29911-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="29911-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29911-109">*hFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29911-109">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29911-110">Ein Handle für die Datei.</span><span class="sxs-lookup"><span data-stu-id="29911-110">A handle to the file.</span></span>

<span data-ttu-id="29911-111">Die-Funktion bricht alle ausstehenden e/a-Vorgänge für dieses Datei Handle ab.</span><span class="sxs-lookup"><span data-stu-id="29911-111">The function cancels all pending I/O operations for this file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29911-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29911-112">Return value</span></span>

<span data-ttu-id="29911-113">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.</span><span class="sxs-lookup"><span data-stu-id="29911-113">If the function succeeds, the return value is nonzero.</span></span> <span data-ttu-id="29911-114">Der Abbruch Vorgang für alle ausstehenden e/a-Vorgänge, die vom aufrufenden Thread für das angegebene Datei Handle ausgegeben wurden, wurde erfolgreich angefordert.</span><span class="sxs-lookup"><span data-stu-id="29911-114">The cancel operation for all pending I/O operations issued by the calling thread for the specified file handle was successfully requested.</span></span> <span data-ttu-id="29911-115">Der Thread kann die [**gedeverlappedresult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) -Funktion verwenden, um zu bestimmen, wann die e/a-Vorgänge selbst abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="29911-115">The thread can use the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function to determine when the I/O operations themselves have been completed.</span></span>

<span data-ttu-id="29911-116">Wenn die Funktion fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="29911-116">If the function fails, the return value is zero (0).</span></span> <span data-ttu-id="29911-117">Um erweiterte Fehlerinformationen abzurufen, müssen Sie die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="29911-117">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="29911-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29911-118">Remarks</span></span>

<span data-ttu-id="29911-119">Wenn für das angegebene Datei Handle ausstehende e/a-Vorgänge ausgeführt werden und diese vom aufrufenden Thread ausgegeben werden, werden diese von der **CancelIo** -Funktion abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="29911-119">If there are any pending I/O operations in progress for the specified file handle, and they are issued by the calling thread, the **CancelIo** function cancels them.</span></span> <span data-ttu-id="29911-120">**CancelIo** bricht nur ausstehende e/a-Vorgänge für das Handle ab, ändert den Zustand des Handles nicht. Dies bedeutet, dass Sie sich nicht auf den Zustand des Handles verlassen können, weil Sie nicht wissen, ob der Vorgang erfolgreich abgeschlossen wurde oder abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="29911-120">**CancelIo** cancels only outstanding I/O on the handle, it does not change the state of the handle; this means that you cannot rely on the state of the handle because you cannot know whether the operation was completed successfully or canceled.</span></span>

<span data-ttu-id="29911-121">Die e/a-Vorgänge müssen als überlappende e/a-Vorgänge ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="29911-121">The I/O operations must be issued as overlapped I/O.</span></span> <span data-ttu-id="29911-122">Wenn dies nicht der Fall ist, werden die e/a-Vorgänge nicht zurückgegeben, damit der Thread die **CancelIo** -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="29911-122">If they are not, the I/O operations do not return to allow the thread to call the **CancelIo** function.</span></span> <span data-ttu-id="29911-123">Das Aufrufen der **CancelIo** -Funktion mit einem Datei Handle, das nicht mit einem überlappenden **\_ Dateiflag \_** geöffnet wurde, bewirkt nichts.</span><span class="sxs-lookup"><span data-stu-id="29911-123">Calling the **CancelIo** function with a file handle that is not opened with **FILE\_FLAG\_OVERLAPPED** does nothing.</span></span>

<span data-ttu-id="29911-124">Alle e/a-Vorgänge, die abgebrochen werden, werden mit dem Fehler **\_ Vorgang \_ abgebrochen**, und alle Abschluss Benachrichtigungen für die e/a-Vorgänge treten in der Regel auf.</span><span class="sxs-lookup"><span data-stu-id="29911-124">All I/O operations that are canceled complete with the error **ERROR\_OPERATION\_ABORTED**, and all completion notifications for the I/O operations occur normally.</span></span>

<span data-ttu-id="29911-125">In Windows 8 und Windows Server 2012 wird diese Funktion von den folgenden Technologien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="29911-125">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="29911-126">Technologie</span><span class="sxs-lookup"><span data-stu-id="29911-126">Technology</span></span>                                           | <span data-ttu-id="29911-127">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="29911-127">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="29911-128">Server Message Block-Protokoll (SMB) 3,0</span><span class="sxs-lookup"><span data-stu-id="29911-128">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="29911-129">Ja</span><span class="sxs-lookup"><span data-stu-id="29911-129">Yes</span></span><br/> |
| <span data-ttu-id="29911-130">SMB 3,0 transparent Failover (TFO)</span><span class="sxs-lookup"><span data-stu-id="29911-130">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="29911-131">Ja</span><span class="sxs-lookup"><span data-stu-id="29911-131">Yes</span></span><br/> |
| <span data-ttu-id="29911-132">SMB 3,0 mit Dateifreigaben mit horizontaler Skalierung (also)</span><span class="sxs-lookup"><span data-stu-id="29911-132">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="29911-133">Ja</span><span class="sxs-lookup"><span data-stu-id="29911-133">Yes</span></span><br/> |
| <span data-ttu-id="29911-134">Freigegebenes Clustervolume Datei System (csvfs)</span><span class="sxs-lookup"><span data-stu-id="29911-134">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="29911-135">Ja</span><span class="sxs-lookup"><span data-stu-id="29911-135">Yes</span></span><br/> |
| <span data-ttu-id="29911-136">Robustes Dateisystem (Resilient File System, ReFS)</span><span class="sxs-lookup"><span data-stu-id="29911-136">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="29911-137">Ja</span><span class="sxs-lookup"><span data-stu-id="29911-137">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="29911-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29911-138">Requirements</span></span>



| <span data-ttu-id="29911-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29911-139">Requirement</span></span> | <span data-ttu-id="29911-140">Wert</span><span class="sxs-lookup"><span data-stu-id="29911-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29911-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29911-141">Minimum supported client</span></span><br/> | <span data-ttu-id="29911-142">\[UWP-Apps für Windows XP-Desktop-Apps \|\]</span><span class="sxs-lookup"><span data-stu-id="29911-142">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="29911-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29911-143">Minimum supported server</span></span><br/> | <span data-ttu-id="29911-144">Windows Server 2003 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="29911-144">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="29911-145">Header</span><span class="sxs-lookup"><span data-stu-id="29911-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="29911-146"><dt>Ioapi. h (Include Windows. h); </dt> <dt>Winbase. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29911-146"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="29911-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="29911-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="29911-148"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="29911-148"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="29911-149">DLL</span><span class="sxs-lookup"><span data-stu-id="29911-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29911-150"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29911-150"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="29911-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29911-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29911-152">**CancelIoEx**</span><span class="sxs-lookup"><span data-stu-id="29911-152">**CancelIoEx**</span></span>](cancelioex-func.md)
</dt> <dt>

[<span data-ttu-id="29911-153">**CancelSynchronousIo**</span><span class="sxs-lookup"><span data-stu-id="29911-153">**CancelSynchronousIo**</span></span>](cancelsynchronousio-func.md)
</dt> <dt>

[<span data-ttu-id="29911-154">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="29911-154">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="29911-155">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="29911-155">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="29911-156">Dateiverwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="29911-156">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="29911-157">**Lockfileex**</span><span class="sxs-lookup"><span data-stu-id="29911-157">**LockFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[<span data-ttu-id="29911-158">**"Read directoriychangesw"**</span><span class="sxs-lookup"><span data-stu-id="29911-158">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
</dt> <dt>

[<span data-ttu-id="29911-159">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="29911-159">**ReadFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[<span data-ttu-id="29911-160">**ReadFileEx**</span><span class="sxs-lookup"><span data-stu-id="29911-160">**ReadFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[<span data-ttu-id="29911-161">Synchrone und asynchrone e/a</span><span class="sxs-lookup"><span data-stu-id="29911-161">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> <dt>

[<span data-ttu-id="29911-162">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="29911-162">**WriteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> <dt>

[<span data-ttu-id="29911-163">**WriteFileEx**</span><span class="sxs-lookup"><span data-stu-id="29911-163">**WriteFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

