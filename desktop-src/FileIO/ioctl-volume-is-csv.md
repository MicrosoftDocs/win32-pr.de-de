---
description: Bestimmt, ob ein Volume ein CSV-Volume ist.
ms.assetid: 6B09B519-1E2F-4757-AAD5-1E4C81023E14
title: IOCTL_VOLUME_IS_CSV Steuerungs Code (ntddvol. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VOLUME_IS_CSV
api_type:
- HeaderDef
api_location:
- Ntddvol.h
ms.openlocfilehash: 8121e1b89c88ad05a2c2be8537d7170bfabfc412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348539"
---
# <a name="ioctl_volume_is_csv-control-code"></a><span data-ttu-id="8d003-103">IOCTL- \_ Volume \_ ist CSV- \_ Steuerungs Code</span><span class="sxs-lookup"><span data-stu-id="8d003-103">IOCTL\_VOLUME\_IS\_CSV control code</span></span>

<span data-ttu-id="8d003-104">Bestimmt, ob ein Volume ein CSV-Volume ist.</span><span class="sxs-lookup"><span data-stu-id="8d003-104">Determines whether a volume is a CSV volume.</span></span>

<span data-ttu-id="8d003-105">Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.</span><span class="sxs-lookup"><span data-stu-id="8d003-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,              // handle to device
                 IOCTL_VOLUME_IS_CSV,           // dwIoControlCode
                 NULL,                          // input buffer
                 0,                             // size of input buffer
                 (LPVOID) lpOutBuffer,          // lpOutBuffer
                 (DWORD) nOutBufferSize,        // nOutBufferSize
                 (LPDWORD) lpBytesReturned,     // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="8d003-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d003-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d003-107">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="8d003-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="8d003-108">Ein Handle für das Volume.</span><span class="sxs-lookup"><span data-stu-id="8d003-108">A handle to the volume.</span></span> <span data-ttu-id="8d003-109">Rufen Sie zum Abrufen eines Volumehandles [**die Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) "-Funktion" auf.</span><span class="sxs-lookup"><span data-stu-id="8d003-109">To retrieve a volume handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="8d003-110">Nur Administratoren können Volumehandles öffnen.</span><span class="sxs-lookup"><span data-stu-id="8d003-110">Only administrators can open volume handles.</span></span>

</dd> <dt>

<span data-ttu-id="8d003-111">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="8d003-111">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="8d003-112">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="8d003-112">The control code for the operation.</span></span> <span data-ttu-id="8d003-113">Verwenden Sie das **IOCTL- \_ Volume \_ ist \_** für diesen Vorgang CSV.</span><span class="sxs-lookup"><span data-stu-id="8d003-113">Use **IOCTL\_VOLUME\_IS\_CSV** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="8d003-114">*lpinbuffer*</span><span class="sxs-lookup"><span data-stu-id="8d003-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="8d003-115">Wird bei diesem Vorgang nicht verwendet. auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8d003-115">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8d003-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="8d003-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="8d003-117">Wird bei diesem Vorgang nicht verwendet. auf NULL (0) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8d003-117">Not used with this operation; set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="8d003-118">*lpoutbuffer*</span><span class="sxs-lookup"><span data-stu-id="8d003-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="8d003-119">Ein Zeiger auf **true** , wenn das Volume ein CSV-Volume ist. Andernfalls schlägt der Funktionsaufrufe fehl.</span><span class="sxs-lookup"><span data-stu-id="8d003-119">A pointer to **TRUE** if the volume is a CSV volume; otherwise, the function call fails.</span></span>

</dd> <dt>

<span data-ttu-id="8d003-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="8d003-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="8d003-121">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="8d003-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8d003-122">*lpbyteszurück gegeben*</span><span class="sxs-lookup"><span data-stu-id="8d003-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="8d003-123">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="8d003-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="8d003-124">Wenn *lpoverllapp* den **Wert NULL** hat, kann *lpbytes-Rückgabe* Wert nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="8d003-124">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="8d003-125">Selbst wenn ein Vorgang keine Ausgabedaten zurückgibt und *lpoutbuffer* den Wert **null** hat, verwendet [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) *lpbytesreturn*.</span><span class="sxs-lookup"><span data-stu-id="8d003-125">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="8d003-126">Nach einem solchen Vorgang ist der Wert von *lpbytesno* bedeutungslos.</span><span class="sxs-lookup"><span data-stu-id="8d003-126">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="8d003-127">Wenn *lpoverllapp* nicht **null** ist, kann *lpbytesgab* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="8d003-127">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="8d003-128">Wenn dieser Parameter nicht **null** ist und der Vorgang Daten zurückgibt, ist *lpbytesreturns* bedeutungslos, bis der überlappende Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="8d003-128">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="8d003-129">Um die Anzahl der zurückgegebenen Bytes abzurufen, rufen Sie [**gezu verlappedresult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult)auf.</span><span class="sxs-lookup"><span data-stu-id="8d003-129">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="8d003-130">Wenn *hdevice* einem e/a-Abschlussport zugeordnet ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8d003-130">If *hDevice* is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="8d003-131">*lpoverlgetauscht*</span><span class="sxs-lookup"><span data-stu-id="8d003-131">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="8d003-132">Ein Zeiger auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.</span><span class="sxs-lookup"><span data-stu-id="8d003-132">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="8d003-133">Wenn *hdevice* ohne Angabe eines überlappenden **\_ Dateiflags \_** geöffnet wurde, wird *lpoverlgetauscht* ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8d003-133">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="8d003-134">Wenn *hdevice* mit dem überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, wird der Vorgang als überlappende (asynchrone) Vorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d003-134">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="8d003-135">In diesem Fall muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur verweisen, die ein Handle für ein Ereignis Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="8d003-135">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="8d003-136">Andernfalls schlägt die Funktion auf unvorhersehbare Weise fehl.</span><span class="sxs-lookup"><span data-stu-id="8d003-136">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="8d003-137">Bei überlappenden Vorgängen gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) sofort zurück, und das Ereignis Objekt wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="8d003-137">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="8d003-138">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="8d003-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d003-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d003-139">Return value</span></span>

<span data-ttu-id="8d003-140">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="8d003-140">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="8d003-141">Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert NULL (0) zurück.</span><span class="sxs-lookup"><span data-stu-id="8d003-141">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero (0).</span></span> <span data-ttu-id="8d003-142">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="8d003-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d003-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d003-143">Requirements</span></span>



| <span data-ttu-id="8d003-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d003-144">Requirement</span></span> | <span data-ttu-id="8d003-145">Wert</span><span class="sxs-lookup"><span data-stu-id="8d003-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8d003-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d003-146">Minimum supported client</span></span><br/> | <span data-ttu-id="8d003-147">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8d003-147">None supported</span></span><br/>                                                            |
| <span data-ttu-id="8d003-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d003-148">Minimum supported server</span></span><br/> | <span data-ttu-id="8d003-149">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d003-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8d003-150">Header</span><span class="sxs-lookup"><span data-stu-id="8d003-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d003-151"><dt>Ntddvol. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d003-151"><dt>Ntddvol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d003-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d003-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d003-153">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="8d003-153">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="8d003-154">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="8d003-154">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="8d003-155">Volumeverwaltungs-Steuerungscodes</span><span class="sxs-lookup"><span data-stu-id="8d003-155">Volume Management Control Codes</span></span>](volume-management-control-codes.md)
</dt> </dl>

 

