---
description: Wartet, bis alle Volumes auf dem angegebenen Datenträger zur Verwendung bereit sind.
ms.assetid: 6cf619bb-7ff5-485e-b533-0f7f6503c6e0
title: IOCTL_DISK_ARE_VOLUMES_READY Steuerungs Code (ntdddisk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_ARE_VOLUMES_READY
api_type:
- HeaderDef
api_location:
- ntdddisk.h
ms.openlocfilehash: dc4457af2ce6e7759ef879900803504933a09978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369019"
---
# <a name="ioctl_disk_are_volumes_ready-control-code"></a><span data-ttu-id="b41f2-103">Ioctl-Datenträger \_ \_ sind für die \_ \_ Bereitstellung von Volumes</span><span class="sxs-lookup"><span data-stu-id="b41f2-103">IOCTL\_DISK\_ARE\_VOLUMES\_READY control code</span></span>

<span data-ttu-id="b41f2-104">Wartet, bis alle Volumes auf dem angegebenen Datenträger zur Verwendung bereit sind.</span><span class="sxs-lookup"><span data-stu-id="b41f2-104">Waits for all volumes on the specified disk to be ready for use.</span></span>

<span data-ttu-id="b41f2-105">Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.</span><span class="sxs-lookup"><span data-stu-id="b41f2-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_ARE_VOLUMES_READY,   // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       NULL,            // lpOutBuffer 
                 (DWORD)        0,               // nOutBufferSize
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="b41f2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b41f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b41f2-107">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="b41f2-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="b41f2-108">Ein Handle für den Datenträger.</span><span class="sxs-lookup"><span data-stu-id="b41f2-108">A handle to the disk.</span></span>

<span data-ttu-id="b41f2-109">Rufen Sie zum Abrufen eines Geräte [**Handles die Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) "-Funktion" auf.</span><span class="sxs-lookup"><span data-stu-id="b41f2-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="b41f2-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="b41f2-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="b41f2-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="b41f2-111">The control code for the operation.</span></span>

<span data-ttu-id="b41f2-112">Ioctl-Datenträger verwenden sind Volumes, die für diesen Vorgang **\_ \_ \_ \_ bereit sind** .</span><span class="sxs-lookup"><span data-stu-id="b41f2-112">Use **IOCTL\_DISK\_ARE\_VOLUMES\_READY** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="b41f2-113">*lpinbuffer*</span><span class="sxs-lookup"><span data-stu-id="b41f2-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="b41f2-114">Wird bei diesem Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b41f2-114">Not used with this operation.</span></span> <span data-ttu-id="b41f2-115">Auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b41f2-115">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b41f2-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="b41f2-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="b41f2-117">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="b41f2-117">The size of the input buffer, in bytes.</span></span> <span data-ttu-id="b41f2-118">Legen Sie den Wert auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="b41f2-118">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="b41f2-119">*lpoutbuffer*</span><span class="sxs-lookup"><span data-stu-id="b41f2-119">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="b41f2-120">Wird bei diesem Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b41f2-120">Not used with this operation.</span></span> <span data-ttu-id="b41f2-121">Auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b41f2-121">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b41f2-122">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="b41f2-122">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="b41f2-123">Wird bei diesem Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b41f2-123">Not used with this operation.</span></span> <span data-ttu-id="b41f2-124">Legen Sie den Wert auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="b41f2-124">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="b41f2-125">*lpbyteszurück gegeben*</span><span class="sxs-lookup"><span data-stu-id="b41f2-125">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="b41f2-126">Wird bei diesem Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b41f2-126">Not used with this operation.</span></span> <span data-ttu-id="b41f2-127">Auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b41f2-127">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b41f2-128">*lpoverlgetauscht*</span><span class="sxs-lookup"><span data-stu-id="b41f2-128">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="b41f2-129">Ein Zeiger auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.</span><span class="sxs-lookup"><span data-stu-id="b41f2-129">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="b41f2-130">Wenn *hdevice* ohne Angabe eines überlappenden **\_ Dateiflags \_** geöffnet wurde, wird *lpoverlgetauscht* ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b41f2-130">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="b41f2-131">Wenn *hdevice* mit dem überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, wird der Vorgang als überlappende (asynchrone) Vorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b41f2-131">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="b41f2-132">In diesem Fall muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur verweisen, die ein Handle für ein Ereignis Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="b41f2-132">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="b41f2-133">Andernfalls schlägt die Funktion auf unvorhersehbare Weise fehl.</span><span class="sxs-lookup"><span data-stu-id="b41f2-133">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="b41f2-134">Bei überlappenden Vorgängen gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) sofort zurück, und das Ereignis Objekt wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="b41f2-134">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="b41f2-135">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="b41f2-135">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b41f2-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b41f2-136">Return value</span></span>

<span data-ttu-id="b41f2-137">Wenn der Vorgang erfolgreich abgeschlossen wurde, was darauf hinweist, dass alle Volumes auf dem Datenträger einsatzbereit sind, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="b41f2-137">If the operation completes successfully, indicating that all volumes on the disk are ready for use, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="b41f2-138">Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="b41f2-138">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="b41f2-139">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="b41f2-139">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="b41f2-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b41f2-140">Requirements</span></span>



| <span data-ttu-id="b41f2-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b41f2-141">Requirement</span></span> | <span data-ttu-id="b41f2-142">Wert</span><span class="sxs-lookup"><span data-stu-id="b41f2-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b41f2-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b41f2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b41f2-144">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b41f2-144">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b41f2-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b41f2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b41f2-146">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b41f2-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b41f2-147">Header</span><span class="sxs-lookup"><span data-stu-id="b41f2-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="b41f2-148"><dt>Ntdddisk. h</dt></span><span class="sxs-lookup"><span data-stu-id="b41f2-148"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b41f2-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b41f2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b41f2-150">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="b41f2-150">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="b41f2-151">Steuerungs Codes für die Datenträgerverwaltung</span><span class="sxs-lookup"><span data-stu-id="b41f2-151">Disk Management Control Codes</span></span>](disk-management-control-codes.md)
</dt> </dl>

 

