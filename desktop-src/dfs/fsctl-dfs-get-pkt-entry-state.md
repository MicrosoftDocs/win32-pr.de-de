---
title: FSCTL_DFS_GET_PKT_ENTRY_STATE-Steuerungscode (LmDfs.h)
description: Der FSCTL_DFS_GET_PKT_ENTRY_STATE Steuerungs Code kann die gleichen Informationen wie die netdfsgetclientinfo-Funktion erhalten, kann jedoch bei manchen Konfigurationen mit hohen Wartezeiten für die DFS-Server eine bessere Leistung erzielen.
ms.assetid: d4eec104-128b-43b5-9fae-08ab0b977dec
topic_type:
- apiref
api_name:
- FSCTL_DFS_GET_PKT_ENTRY_STATE
api_location:
- LmDfs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a57fb448934908ebc1530e95a298715324aaee6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524032"
---
# <a name="fsctl_dfs_get_pkt_entry_state-control-code"></a><span data-ttu-id="7abdd-103">FSCTL_DFS_GET_PKT_ENTRY_STATE Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="7abdd-103">FSCTL_DFS_GET_PKT_ENTRY_STATE control code</span></span>

<span data-ttu-id="7abdd-104">Der **FSCTL_DFS_GET_PKT_ENTRY_STATE** Steuerungs Code kann die gleichen Informationen wie die [**netdfsgetclientinfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) -Funktion erhalten, kann jedoch bei manchen Konfigurationen mit hohen Wartezeiten für die DFS-Server eine bessere Leistung erzielen.</span><span class="sxs-lookup"><span data-stu-id="7abdd-104">The **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code can get the same information as the [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) function but can provide better performance in some configurations with high latencies to the DFS servers.</span></span> <span data-ttu-id="7abdd-105">Es wird nicht empfohlen, den **FSCTL_DFS_GET_PKT_ENTRY_STATE** Control-Code zu verwenden, es sei denn, es treten Leistungsprobleme auf.</span><span class="sxs-lookup"><span data-stu-id="7abdd-105">It is not recommended to use the **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code unless there are performance issues.</span></span>

<span data-ttu-id="7abdd-106">Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.</span><span class="sxs-lookup"><span data-stu-id="7abdd-106">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>

```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,            // handle to device
                    (DWORD)        FSCTL_DFS_GET_PKT_ENTRY_STATE, // dwIoControlCode(LPDWORD)      lpInBuffer,         // input buffer
                    (DWORD)        nInBufferSize,      // size of input buffer
                    (LPDWORD)      lpOutBuffer,        // output buffer
                    (DWORD)        nOutBufferSize,     // size of output buffer
                    (LPDWORD)      lpBytesReturned,    // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );     // OVERLAPPED structure
```

## <a name="parameters"></a><span data-ttu-id="7abdd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7abdd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7abdd-108">*hdevice* [in]</span><span class="sxs-lookup"><span data-stu-id="7abdd-108">*hDevice* [in]</span></span>
</dt> <dd>

<span data-ttu-id="7abdd-109">Ein Handle für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="7abdd-109">A handle to the device.</span></span> <span data-ttu-id="7abdd-110">Rufen Sie zum Abrufen eines Geräte [**Handles die Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.</span><span class="sxs-lookup"><span data-stu-id="7abdd-110">To obtain a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="7abdd-111">*dwIoControlCode* [in]</span><span class="sxs-lookup"><span data-stu-id="7abdd-111">*dwIoControlCode* [in]</span></span>
</dt> <dd>

<span data-ttu-id="7abdd-112">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7abdd-112">The control code for the operation.</span></span> <span data-ttu-id="7abdd-113">Verwenden Sie **FSCTL_DFS_GET_PKT_ENTRY_STATE** für diesen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7abdd-113">Use **FSCTL_DFS_GET_PKT_ENTRY_STATE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="7abdd-114">*lpinbuffer*</span><span class="sxs-lookup"><span data-stu-id="7abdd-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="7abdd-115">Adresse einer [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) Struktur und der folgenden 1-3-Unicode-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="7abdd-115">Address of a [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) structure and the 1-3 Unicode strings that follow.</span></span>

</dd> <dt>

<span data-ttu-id="7abdd-116">*nInBufferSize* [in]</span><span class="sxs-lookup"><span data-stu-id="7abdd-116">*nInBufferSize* [in]</span></span>
</dt> <dd>

<span data-ttu-id="7abdd-117">Größe (in Bytes) des Puffers, auf den der *lpinbuffer* -Parameter zeigt.</span><span class="sxs-lookup"><span data-stu-id="7abdd-117">Size, in bytes, of the buffer pointed to by the *lpInBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7abdd-118">*lpoutbuffer* [out]</span><span class="sxs-lookup"><span data-stu-id="7abdd-118">*lpOutBuffer* [out]</span></span>
</dt> <dd>

<span data-ttu-id="7abdd-119">Die Adresse einer **DFS_INFO_ \#** Struktur und alle Zeichen folgen und Strukturen, auf die von der **DFS_INFO_ \#** Struktur verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7abdd-119">Address of a **DFS_INFO_\#** structure and any strings and structures pointed to by the **DFS_INFO_\#** structure.</span></span> <span data-ttu-id="7abdd-120">Die angegebene Struktur ist abhängig vom **ebenenmember** in der [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) Struktur, die im Eingabepuffer weitergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7abdd-120">The specific structure returned depends on the **Level** member in the [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) structure passed in the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7abdd-121">*nOutBufferSize* [in]</span><span class="sxs-lookup"><span data-stu-id="7abdd-121">*nOutBufferSize* [in]</span></span>
</dt> <dd>

<span data-ttu-id="7abdd-122">Größe (in Bytes) des Puffers, auf den der *lpoutbuffer* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="7abdd-122">Size, in bytes, of the buffer pointed to by the *lpOutBuffer* parameter.</span></span> <span data-ttu-id="7abdd-123">Aufgrund der Zeichen folgen und Strukturen, auf die die zurückgegebene **DFS_INFO_ \#** -Struktur verweist, die sich ebenfalls im Ausgabepuffer befinden, sollte dieser Puffer größer als die angegebene **DFS_INFO_ \#** Struktur sein.</span><span class="sxs-lookup"><span data-stu-id="7abdd-123">Due to the strings and structures referenced by the returned **DFS_INFO_\#** structure that are also in the output buffer, this buffer should be larger than the **DFS_INFO_\#** structure specified.</span></span>

</dd> <dt>

<span data-ttu-id="7abdd-124">*lpbyteszurück gegeben* [out]</span><span class="sxs-lookup"><span data-stu-id="7abdd-124">*lpBytesReturned* [out]</span></span>
</dt> <dd>

<span data-ttu-id="7abdd-125">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="7abdd-125">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="7abdd-126">Wenn der Ausgabepuffer zu klein ist, aber mindestens groß genug ist, um ein **DWORD** zu speichern, schlägt der-Befehl fehl, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt **ERROR_MORE_DATA** zurück, und das erste **DWORD** des Ausgabepuffers enthält die benötigte Größe.</span><span class="sxs-lookup"><span data-stu-id="7abdd-126">If the output buffer is too small, but at least large enough to hold a **DWORD**, the call fails, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR_MORE_DATA**, and the first **DWORD** of the output buffer contains the size that would have been required.</span></span> <span data-ttu-id="7abdd-127">Wenn der Ausgabepuffer kein **DWORD** enthalten kann, schlägt der-Vorgang mit **ERROR_INSUFFICIENT_BUFFER** fehl, und *lpbyteshat* den Wert 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7abdd-127">If the output buffer cannot hold a **DWORD** then the call fails with **ERROR_INSUFFICIENT_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="7abdd-128">Wenn *lpoverllapp* den **Wert NULL** hat, kann *lpbytes-Rückgabe* Wert nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="7abdd-128">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="7abdd-129">Selbst wenn ein Vorgang keine Ausgabedaten zurückgibt und *lpoutbuffer* den Wert **null** hat, verwendet [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) *lpbytesreturn*.</span><span class="sxs-lookup"><span data-stu-id="7abdd-129">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="7abdd-130">Nach einem solchen Vorgang ist der Wert von *lpbytesno* bedeutungslos.</span><span class="sxs-lookup"><span data-stu-id="7abdd-130">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="7abdd-131">Wenn *lpoverllapp* nicht **null** ist, kann *lpbytesgab* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="7abdd-131">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="7abdd-132">Wenn dieser Parameter nicht **null** ist und der Vorgang Daten zurückgibt, ist *lpbytesreturns* bedeutungslos, bis der überlappende Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="7abdd-132">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="7abdd-133">Um die Anzahl der zurückgegebenen Bytes abzurufen, rufen Sie [**gezu verlappedresult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult)auf.</span><span class="sxs-lookup"><span data-stu-id="7abdd-133">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="7abdd-134">Wenn der *hdevice* -Parameter einem e/a-Abschlussport zugeordnet ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7abdd-134">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="7abdd-135">*lpoverlgetauscht* [in]</span><span class="sxs-lookup"><span data-stu-id="7abdd-135">*lpOverlapped* [in]</span></span>
</dt> <dd>

<span data-ttu-id="7abdd-136">Ein Zeiger auf eine [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.</span><span class="sxs-lookup"><span data-stu-id="7abdd-136">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="7abdd-137">Wenn *hdevice* geöffnet wurde, ohne **FILE_FLAG_OVERLAPPED** anzugeben, wird *lpoverlgetauscht* ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7abdd-137">If *hDevice* was opened without specifying **FILE_FLAG_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="7abdd-138">Wenn *hdevice* mit dem **FILE_FLAG_OVERLAPPED** -Flag geöffnet wurde, wird der Vorgang als überlappende (asynchrone) Vorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7abdd-138">If *hDevice* was opened with the **FILE_FLAG_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="7abdd-139">In diesem Fall muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur verweisen, die ein Handle für ein Ereignis Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="7abdd-139">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="7abdd-140">Andernfalls schlägt die Funktion auf unvorhersehbare Weise fehl.</span><span class="sxs-lookup"><span data-stu-id="7abdd-140">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="7abdd-141">Bei überlappenden Vorgängen gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) sofort zurück, und das Ereignis Objekt wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="7abdd-141">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="7abdd-142">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="7abdd-142">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7abdd-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7abdd-143">Return value</span></span>

<span data-ttu-id="7abdd-144">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="7abdd-144">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="7abdd-145">Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="7abdd-145">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="7abdd-146">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="7abdd-146">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="7abdd-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7abdd-147">Requirements</span></span>

| <span data-ttu-id="7abdd-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7abdd-148">Requirement</span></span> | <span data-ttu-id="7abdd-149">Wert</span><span class="sxs-lookup"><span data-stu-id="7abdd-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7abdd-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7abdd-150">Minimum supported client</span></span><br/> | <span data-ttu-id="7abdd-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7abdd-151">Windows Vista</span></span><br/>                                                                             |
| <span data-ttu-id="7abdd-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7abdd-152">Minimum supported server</span></span><br/> | <span data-ttu-id="7abdd-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7abdd-153">Windows Server 2008</span></span><br/>                                                                       |
| <span data-ttu-id="7abdd-154">Header</span><span class="sxs-lookup"><span data-stu-id="7abdd-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="7abdd-155"><dt>Lmdfs. h (Include lmdfs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7abdd-155"><dt>LmDfs.h (include LmDfs.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="7abdd-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7abdd-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7abdd-157">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="7abdd-157">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="7abdd-158">**Netdfsgetclientinfo**</span><span class="sxs-lookup"><span data-stu-id="7abdd-158">**NetDfsGetClientInfo**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> </dl>
