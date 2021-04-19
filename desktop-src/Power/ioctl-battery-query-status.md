---
description: Ruft den aktuellen Status des Akkus ab.
ms.assetid: 7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df
title: IOCTL_BATTERY_QUERY_STATUS Steuerungs Code (poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: e2de9d3ab48aec13a9a5c1957a5f98aefbe6a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348609"
---
# <a name="ioctl_battery_query_status-control-code"></a><span data-ttu-id="a61be-103">IOCTL \_ Akku \_ Query- \_ Status Steuerungs Code</span><span class="sxs-lookup"><span data-stu-id="a61be-103">IOCTL\_BATTERY\_QUERY\_STATUS control code</span></span>

<span data-ttu-id="a61be-104">Ruft den aktuellen Status des Akkus ab.</span><span class="sxs-lookup"><span data-stu-id="a61be-104">Retrieves the current status of the battery.</span></span>

<span data-ttu-id="a61be-105">Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.</span><span class="sxs-lookup"><span data-stu-id="a61be-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to battery
  IOCTL_BATTERY_QUERY_STATUS, // dwIoControlCode
  (LPVOID) lpInBuffer,        // input buffer
  (DWORD) nInBufferSize,      // size of input buffer
  (LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,  // number of bytes returned
  (LPOVERLAPPED) lpOverlapped // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="a61be-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a61be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a61be-107">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="a61be-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="a61be-108">Ein Handle für den Akku, von dem Informationen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a61be-108">A handle to the battery from which information is to be returned.</span></span> <span data-ttu-id="a61be-109">Rufen Sie zum Abrufen eines Geräte [**Handles die Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.</span><span class="sxs-lookup"><span data-stu-id="a61be-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="a61be-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="a61be-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="a61be-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="a61be-111">The control code for the operation.</span></span> <span data-ttu-id="a61be-112">Dieser Wert identifiziert den spezifischen Vorgang, der ausgeführt werden soll, und den Typ des Geräts, auf dem es ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a61be-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="a61be-113">Verwenden Sie den **IOCTL- \_ Akku \_ Abfrage \_ Status** für diesen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="a61be-113">Use **IOCTL\_BATTERY\_QUERY\_STATUS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="a61be-114">*lpinbuffer*</span><span class="sxs-lookup"><span data-stu-id="a61be-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="a61be-115">Ein Zeiger auf die [**\_ \_ Status Struktur der Akku Wartezeit**](battery-wait-status-str.md) .</span><span class="sxs-lookup"><span data-stu-id="a61be-115">A pointer to a [**BATTERY\_WAIT\_STATUS**](battery-wait-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a61be-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="a61be-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a61be-117">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a61be-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a61be-118">*lpoutbuffer*</span><span class="sxs-lookup"><span data-stu-id="a61be-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="a61be-119">Ein Zeiger auf eine [**Akku \_ Status**](battery-status-str.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="a61be-119">A pointer to a [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a61be-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="a61be-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a61be-121">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a61be-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a61be-122">*lpbyteszurück gegeben*</span><span class="sxs-lookup"><span data-stu-id="a61be-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="a61be-123">Ein Zeiger auf eine Variable, die die Größe der im *lpoutbuffer* -Puffer zurückgegebenen Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="a61be-123">A pointer to a variable that receives the size of the data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="a61be-124">Wenn der Ausgabepuffer zu klein ist, um Daten zurückzugeben, dann schlägt der-Befehl fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode **Fehler \_ unzureichend \_** zurück, und die zurückgegebene Byte Anzahl ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a61be-124">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="a61be-125">Wenn *lpoverllapp* den Wert **null** hat (nicht überlappende e/a), kann *lpbytesgab* nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="a61be-125">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="a61be-126">Wenn *lpoverllapp* nicht **null** (überlappende e/a) ist, kann *lpbytesgab* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="a61be-126">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="a61be-127">Wenn dies ein überlappende Vorgang ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetOverLappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a61be-127">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="a61be-128">Wenn *hdevice* einem e/a-Abschlussport zugeordnet ist, können Sie die Anzahl der Bytes abrufen, die durch Aufrufen der [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a61be-128">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="a61be-129">*lpoverlgetauscht*</span><span class="sxs-lookup"><span data-stu-id="a61be-129">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="a61be-130">Ein Zeiger auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.</span><span class="sxs-lookup"><span data-stu-id="a61be-130">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="a61be-131">Wenn *hdevice* mit dem überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="a61be-131">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="a61be-132">In diesem Fall wird [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a61be-132">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="a61be-133">Wenn das Gerät mit dem überlappenden Flag für das **\_ Dateiflag \_** geöffnet wurde und *lpoverlgetauscht* den Wert **null** hat, schlägt die Funktion auf unvorhersehbare Weise fehl.</span><span class="sxs-lookup"><span data-stu-id="a61be-133">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="a61be-134">Wenn *hdevice* ohne Angabe des überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, wird *lpoverlgetauscht* ignoriert, und die [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) -Funktion gibt nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="a61be-134">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a61be-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a61be-135">Return value</span></span>

<span data-ttu-id="a61be-136">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="a61be-136">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="a61be-137">Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="a61be-137">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="a61be-138">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="a61be-138">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="a61be-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a61be-139">Remarks</span></span>

<span data-ttu-id="a61be-140">Diese Akku-ioctl Ruft den Status des Akkus zu dem Zeitpunkt ab, an dem der Vorgang zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a61be-140">This battery IOCTL retrieves the status of the battery at the time the operation returns.</span></span> <span data-ttu-id="a61be-141">Die Eingabeparameter Struktur, [**der \_ \_ Status der Akku Wartezeit**](battery-wait-status-str.md), gibt an, wann der Akku Status verarbeitet und zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="a61be-141">The input parameter structure, [**BATTERY\_WAIT\_STATUS**](battery-wait-status-str.md), indicates when the battery status is to be processed and returned.</span></span>

<span data-ttu-id="a61be-142">Anforderungen für den Akku Status können für die sofortige Rückgabe oder für das warten auf eine bestimmte Bedingung vor dem Abschlussfest gelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a61be-142">Requests for battery status can be for immediate return or can be set to wait for a particular condition before completing.</span></span> <span data-ttu-id="a61be-143">Beispielsweise kann eine Anforderung für Akku Informationen erfolgen, die warten, bis die Akkukapazität einen bestimmten Punkt erreicht oder sich der Akku Zustand ändert.</span><span class="sxs-lookup"><span data-stu-id="a61be-143">For example, a request for battery information can be made that waits until the battery capacity reaches a specified point or the battery state changes.</span></span>

<span data-ttu-id="a61be-144">Alle Anforderungen für Akku Informationen werden mit dem Status der **Fehler \_ Datei \_ nicht \_ gefunden** , wenn das Element " **batterytag** " der Anforderung nicht mit der des aktuellen Akku Tags identisch ist.</span><span class="sxs-lookup"><span data-stu-id="a61be-144">All requests for battery information will complete with the status of **ERROR\_FILE\_NOT\_FOUND** whenever the **BatteryTag** element of the request does not match that of the current battery tag.</span></span> <span data-ttu-id="a61be-145">(Weitere Informationen finden Sie unter [Akku-Tags](battery-information.md) .) Hiermit wird sichergestellt, dass die zurückgegebenen Akku Informationen mit denen des angeforderten Akkus übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a61be-145">(See [Battery Tags](battery-information.md) for more information.) This is used to ensure that the returned battery information matches that of the requested battery.</span></span>

<span data-ttu-id="a61be-146">Informationen zu den Auswirkungen von überlappenden e/a-Vorgängen für diesen Vorgang finden Sie im Abschnitt "Hinweise" des Themas " [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ".</span><span class="sxs-lookup"><span data-stu-id="a61be-146">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="a61be-147">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a61be-147">Examples</span></span>

<span data-ttu-id="a61be-148">Ein Beispiel finden Sie unter Auflisten von [Akku Geräten](enumerating-battery-devices.md).</span><span class="sxs-lookup"><span data-stu-id="a61be-148">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a61be-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a61be-149">Requirements</span></span>



| <span data-ttu-id="a61be-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a61be-150">Requirement</span></span> | <span data-ttu-id="a61be-151">Wert</span><span class="sxs-lookup"><span data-stu-id="a61be-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a61be-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a61be-152">Minimum supported client</span></span><br/> | <span data-ttu-id="a61be-153">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a61be-153">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="a61be-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a61be-154">Minimum supported server</span></span><br/> | <span data-ttu-id="a61be-155">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a61be-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="a61be-156">Header</span><span class="sxs-lookup"><span data-stu-id="a61be-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="a61be-157"><dt>Poclass. h; </dt> <dt>Batclass. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="a61be-157"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a61be-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a61be-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a61be-159">Akku Informationen</span><span class="sxs-lookup"><span data-stu-id="a61be-159">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="a61be-160">Steuerungs Codes der Energie Verwaltung</span><span class="sxs-lookup"><span data-stu-id="a61be-160">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="a61be-161">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="a61be-161">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="a61be-162">**Akku \_ Status**</span><span class="sxs-lookup"><span data-stu-id="a61be-162">**BATTERY\_STATUS**</span></span>](battery-status-str.md)
</dt> <dt>

[<span data-ttu-id="a61be-163">**Status der Akku \_ Wartezeit \_**</span><span class="sxs-lookup"><span data-stu-id="a61be-163">**BATTERY\_WAIT\_STATUS**</span></span>](battery-wait-status-str.md)
</dt> <dt>

[<span data-ttu-id="a61be-164">**IOCTL- \_ Akku \_ Abfrage \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="a61be-164">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="a61be-165">**IOCTL \_ Akku \_ - \_ abfragetag**</span><span class="sxs-lookup"><span data-stu-id="a61be-165">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> <dt>

[<span data-ttu-id="a61be-166">**IOCTL- \_ Akku \_ Satz \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="a61be-166">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

