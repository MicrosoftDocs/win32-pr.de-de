---
description: Ruft die Attribute des angegebenen Datenträger Geräts ab.
ms.assetid: 2FF81F67-9E70-43C6-A504-0D60382E0945
title: IOCTL_DISK_GET_CLUSTER_INFO Steuerungs Code (ntdddisk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_GET_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: 613c73c2fd82e76768b0fc692b63b0761938a342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352531"
---
# <a name="ioctl_disk_get_cluster_info-control-code"></a><span data-ttu-id="4677a-103">IOCTL \_ Disk \_ get \_ Cluster \_ Info-Steuerungs Code</span><span class="sxs-lookup"><span data-stu-id="4677a-103">IOCTL\_DISK\_GET\_CLUSTER\_INFO control code</span></span>

<span data-ttu-id="4677a-104">Ruft die Attribute des angegebenen Datenträger Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="4677a-104">Retrieves the attributes of the specified disk device.</span></span>

<span data-ttu-id="4677a-105">Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.</span><span class="sxs-lookup"><span data-stu-id="4677a-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_GET_CLUSTER_INFO,    // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       lpOutBuffer,     // output buffer:GET_DISK_ATTRIBUTES
                 (DWORD)        nOutBufferSize,  // size of output buffer
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="4677a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4677a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4677a-107">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="4677a-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="4677a-108">Ein Handle für den Datenträger.</span><span class="sxs-lookup"><span data-stu-id="4677a-108">A handle to the disk.</span></span>

<span data-ttu-id="4677a-109">Rufen Sie zum Abrufen eines Geräte [**Handles die Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) "-Funktion" auf.</span><span class="sxs-lookup"><span data-stu-id="4677a-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="4677a-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="4677a-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="4677a-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="4677a-111">The control code for the operation.</span></span>

<span data-ttu-id="4677a-112">Verwenden **Sie IOCTL \_ Disk \_ get \_ Cluster \_ Info** für diesen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="4677a-112">Use **IOCTL\_DISK\_GET\_CLUSTER\_INFO** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="4677a-113">*lpinbuffer*</span><span class="sxs-lookup"><span data-stu-id="4677a-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="4677a-114">Wird bei diesem Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4677a-114">Not used with this operation.</span></span> <span data-ttu-id="4677a-115">Auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4677a-115">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4677a-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="4677a-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="4677a-117">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="4677a-117">The size of the input buffer, in bytes.</span></span> <span data-ttu-id="4677a-118">Legen Sie den Wert auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="4677a-118">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="4677a-119">*lpoutbuffer*</span><span class="sxs-lookup"><span data-stu-id="4677a-119">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="4677a-120">Ein Zeiger auf einen Puffer, der eine Datenträger [**\_ Cluster \_ Info**](disk-cluster-info.md) -Datenstruktur empfängt.</span><span class="sxs-lookup"><span data-stu-id="4677a-120">A pointer to a buffer that receives a [**DISK\_CLUSTER\_INFO**](disk-cluster-info.md) data structure.</span></span>

</dd> <dt>

<span data-ttu-id="4677a-121">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="4677a-121">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="4677a-122">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="4677a-122">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4677a-123">*lpbyteszurück gegeben*</span><span class="sxs-lookup"><span data-stu-id="4677a-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="4677a-124">Wird bei diesem Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4677a-124">Not used with this operation.</span></span> <span data-ttu-id="4677a-125">Auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4677a-125">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4677a-126">*lpoverlgetauscht*</span><span class="sxs-lookup"><span data-stu-id="4677a-126">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="4677a-127">Ein Zeiger auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.</span><span class="sxs-lookup"><span data-stu-id="4677a-127">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="4677a-128">Wenn *hdevice* ohne Angabe eines überlappenden **\_ Dateiflags \_** geöffnet wurde, wird *lpoverlgetauscht* ignoriert.</span><span class="sxs-lookup"><span data-stu-id="4677a-128">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="4677a-129">Wenn *hdevice* mit dem überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, wird der Vorgang als überlappende (asynchrone) Vorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4677a-129">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="4677a-130">In diesem Fall muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur verweisen, die ein Handle für ein Ereignis Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="4677a-130">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="4677a-131">Andernfalls schlägt die Funktion auf unvorhersehbare Weise fehl.</span><span class="sxs-lookup"><span data-stu-id="4677a-131">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="4677a-132">Bei überlappenden Vorgängen gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) sofort zurück, und das Ereignis Objekt wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="4677a-132">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="4677a-133">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="4677a-133">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4677a-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4677a-134">Return value</span></span>

<span data-ttu-id="4677a-135">Wenn der Vorgang erfolgreich abgeschlossen wurde, was darauf hinweist, dass alle Volumes auf dem Datenträger einsatzbereit sind, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="4677a-135">If the operation completes successfully, indicating that all volumes on the disk are ready for use, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="4677a-136">Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="4677a-136">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="4677a-137">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="4677a-137">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="4677a-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4677a-138">Requirements</span></span>



| <span data-ttu-id="4677a-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4677a-139">Requirement</span></span> | <span data-ttu-id="4677a-140">Wert</span><span class="sxs-lookup"><span data-stu-id="4677a-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4677a-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4677a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4677a-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4677a-142">None supported</span></span><br/>                                                             |
| <span data-ttu-id="4677a-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4677a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4677a-144">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4677a-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4677a-145">Header</span><span class="sxs-lookup"><span data-stu-id="4677a-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="4677a-146"><dt>Ntdddisk. h</dt></span><span class="sxs-lookup"><span data-stu-id="4677a-146"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4677a-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4677a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4677a-148">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="4677a-148">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="4677a-149">Steuerungs Codes für die Datenträgerverwaltung</span><span class="sxs-lookup"><span data-stu-id="4677a-149">Disk Management Control Codes</span></span>](disk-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="4677a-150">**Informationen zum Datenträger \_ Cluster \_**</span><span class="sxs-lookup"><span data-stu-id="4677a-150">**DISK\_CLUSTER\_INFO**</span></span>](disk-cluster-info.md)
</dt> <dt>

[<span data-ttu-id="4677a-151">**ioctl-Datenträger \_ \_ Satz- \_ Cluster \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="4677a-151">**IOCTL\_DISK\_SET\_CLUSTER\_INFO**</span></span>](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

