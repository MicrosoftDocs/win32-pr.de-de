---
description: Ruft das aktuelle Akku-Tag ab.
ms.assetid: 0bbe59ba-e037-47ce-a54a-6500ea7c9bc5
title: IOCTL_BATTERY_QUERY_TAG Steuerungs Code (poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_TAG
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: 1d8435e62c4f061ac13b3e18e5bcd64afcb399c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349411"
---
# <a name="ioctl_battery_query_tag-control-code"></a><span data-ttu-id="288c1-103">IOCTL \_ Akku \_ Query \_ Tag Control Code</span><span class="sxs-lookup"><span data-stu-id="288c1-103">IOCTL\_BATTERY\_QUERY\_TAG control code</span></span>

<span data-ttu-id="288c1-104">Ruft das aktuelle Tag des Akkus ab.</span><span class="sxs-lookup"><span data-stu-id="288c1-104">Retrieves the battery's current tag.</span></span>

<span data-ttu-id="288c1-105">Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.</span><span class="sxs-lookup"><span data-stu-id="288c1-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to battery
  IOCTL_BATTERY_QUERY_TAG,     // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  (LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped);// OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="288c1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="288c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="288c1-107">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="288c1-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="288c1-108">Ein Handle für den Akku, von dem das Tag abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="288c1-108">A handle to the battery from which the tag is to be retrieved.</span></span> <span data-ttu-id="288c1-109">Rufen Sie zum Abrufen eines Geräte [**Handles die Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.</span><span class="sxs-lookup"><span data-stu-id="288c1-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="288c1-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="288c1-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="288c1-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="288c1-111">The control code for the operation.</span></span> <span data-ttu-id="288c1-112">Dieser Wert identifiziert den spezifischen Vorgang, der ausgeführt werden soll, und den Typ des Geräts, auf dem es ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="288c1-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="288c1-113">Verwenden Sie für diesen Vorgang das **IOCTL \_ Akku- \_ abfragetag \_** .</span><span class="sxs-lookup"><span data-stu-id="288c1-113">Use **IOCTL\_BATTERY\_QUERY\_TAG** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="288c1-114">*lpinbuffer*</span><span class="sxs-lookup"><span data-stu-id="288c1-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="288c1-115">Ein Zeiger auf einen **ulong** -Eingabepuffer.</span><span class="sxs-lookup"><span data-stu-id="288c1-115">A pointer to a **ULONG** input buffer.</span></span> <span data-ttu-id="288c1-116">Der Wert gibt an, wie viele Millisekunden gewartet werden soll, wenn kein Akku vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="288c1-116">The value indicates the number of milliseconds to wait if there is no battery.</span></span> <span data-ttu-id="288c1-117">Der Wert-1 gibt an, dass die Anforderung unbegrenzt wartet (oder von einem anderen Ereignis abgebrochen wird).</span><span class="sxs-lookup"><span data-stu-id="288c1-117">A value of -1 indicates the request will wait indefinitely (or until canceled by some other event).</span></span>

</dd> <dt>

<span data-ttu-id="288c1-118">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="288c1-118">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="288c1-119">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="288c1-119">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="288c1-120">*lpoutbuffer*</span><span class="sxs-lookup"><span data-stu-id="288c1-120">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="288c1-121">Ein Zeiger auf einen **ulong** -Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="288c1-121">A pointer to a **ULONG** output buffer.</span></span> <span data-ttu-id="288c1-122">Bei Erfolg enthält dieser Puffer das aktuelle Akku Kennzeichen, bei dem es sich um einen beliebigen Wert mit Ausnahme eines \_ ungültigen Akku Tags handelt \_ .</span><span class="sxs-lookup"><span data-stu-id="288c1-122">On success this buffer contains the current battery tag, which can be any value except BATTERY\_TAG\_INVALID.</span></span> <span data-ttu-id="288c1-123">Wenn [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) bei einem Fehler die Fehlercode- **Fehler \_ Datei \_ nicht \_ gefunden** zurückgibt, enthält dieser Puffer den Wert des **Akku \_ Tags \_ ungültig**.</span><span class="sxs-lookup"><span data-stu-id="288c1-123">On failure, if [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_FILE\_NOT\_FOUND**, this buffer contains the value **BATTERY\_TAG\_INVALID**.</span></span>

</dd> <dt>

<span data-ttu-id="288c1-124">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="288c1-124">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="288c1-125">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="288c1-125">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="288c1-126">*lpbyteszurück gegeben*</span><span class="sxs-lookup"><span data-stu-id="288c1-126">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="288c1-127">Ein Zeiger auf eine Variable, die die Größe der im *lpoutbuffer* -Puffer gespeicherten Daten in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="288c1-127">A pointer to a variable that receives the size of the data stored in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="288c1-128">Wenn der Ausgabepuffer zu klein ist, um Daten zurückzugeben, dann schlägt der-Befehl fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode **Fehler \_ unzureichend \_** zurück, und die zurückgegebene Byte Anzahl ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="288c1-128">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="288c1-129">Wenn *lpoverllapp* den Wert **null** hat (nicht überlappende e/a), kann *lpbytesgab* nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="288c1-129">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="288c1-130">Wenn *lpoverllapp* nicht **null** (überlappende e/a) ist, kann *lpbytesgab* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="288c1-130">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="288c1-131">Wenn dies ein überlappende Vorgang ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetOverLappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="288c1-131">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="288c1-132">Wenn *hdevice* einem e/a-Abschlussport zugeordnet ist, können Sie die Anzahl der Bytes abrufen, die durch Aufrufen der [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="288c1-132">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="288c1-133">*lpoverlgetauscht*</span><span class="sxs-lookup"><span data-stu-id="288c1-133">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="288c1-134">Ein Zeiger auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.</span><span class="sxs-lookup"><span data-stu-id="288c1-134">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="288c1-135">Wenn *hdevice* mit dem überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="288c1-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="288c1-136">In diesem Fall wird [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="288c1-136">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="288c1-137">Wenn das Gerät mit dem überlappenden Flag für das **\_ Dateiflag \_** geöffnet wurde und *lpoverlgetauscht* den Wert **null** hat, schlägt die Funktion auf unvorhersehbare Weise fehl.</span><span class="sxs-lookup"><span data-stu-id="288c1-137">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="288c1-138">Wenn *hdevice* ohne Angabe des überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, wird *lpoverlgetauscht* ignoriert, und die [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) -Funktion gibt nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="288c1-138">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="288c1-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="288c1-139">Return value</span></span>

<span data-ttu-id="288c1-140">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="288c1-140">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="288c1-141">Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="288c1-141">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="288c1-142">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="288c1-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="288c1-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="288c1-143">Remarks</span></span>

<span data-ttu-id="288c1-144">Mit diesem Akku-IOCTL wird das aktuelle Tag des Akkus abgerufen.</span><span class="sxs-lookup"><span data-stu-id="288c1-144">This battery IOCTL retrieves the battery's current tag.</span></span> <span data-ttu-id="288c1-145">Das Akku-Tag ist ein eindeutiger Wert ungleich 0 (null), der sich ändert, wenn die physische Batterie wieder hergestellt, ersetzt oder geändert wird.</span><span class="sxs-lookup"><span data-stu-id="288c1-145">The battery tag is a unique nonzero value that changes when the physical battery is reinserted, replaced, or undergoes any characteristic changes.</span></span> <span data-ttu-id="288c1-146">Weitere Informationen zum Zeitpunkt der Änderung eines Akku Tags, zum Erkennen der Änderung und zum Fortsetzen einer Anwendung nach der Änderung eines Akku Tags finden Sie im Abschnitt "Akku-Tags" im Thema "Übersicht über [Akku Informationen](battery-information.md) ".</span><span class="sxs-lookup"><span data-stu-id="288c1-146">See the Battery Tags section in the [Battery Information](battery-information.md) overview topic for more detail on when a battery tag changes, how to detect the change, and how an application should proceed after a battery tag change.</span></span> <span data-ttu-id="288c1-147">Wenn kein Akku vorhanden ist, wartet diese Anforderung die festgelegte Zeit, und wenn noch kein Akku vorhanden ist, wird die **Fehler \_ Datei \_ nicht \_ gefunden** , und das Akku-Tag wird auf **\_ \_ ungültig** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="288c1-147">When a battery is not present, this request will wait the indicated time, and if there is still no battery present, then it will return **ERROR\_FILE\_NOT\_FOUND** and set the battery tag to **BATTERY\_TAG\_INVALID**.</span></span> <span data-ttu-id="288c1-148">(Weitere Informationen finden Sie in den Akku Informationen.)</span><span class="sxs-lookup"><span data-stu-id="288c1-148">(See Battery Information for more information.)</span></span>

<span data-ttu-id="288c1-149">Alle Anforderungen für andere Akku Informationen erfordern, dass der Aufrufer das passende Akku Kennzeichen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="288c1-149">All requests for other battery information require the caller to supply the matching battery tag.</span></span> <span data-ttu-id="288c1-150">Dadurch wird sichergestellt, dass der Aufrufer für jede Anforderung Informationen für den gleichen Akku empfängt und sicherstellt, dass der Aufrufer die Akku Änderungen ohne konstantenabruf kennt.</span><span class="sxs-lookup"><span data-stu-id="288c1-150">This ensures that the caller is receiving information for the same battery for every request and ensures that the caller is aware of battery changes without constant polling.</span></span>

<span data-ttu-id="288c1-151">Informationen zu den Auswirkungen von überlappenden e/a-Vorgängen für diesen Vorgang finden Sie im Abschnitt "Hinweise" des Themas " [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ".</span><span class="sxs-lookup"><span data-stu-id="288c1-151">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="288c1-152">Beispiele</span><span class="sxs-lookup"><span data-stu-id="288c1-152">Examples</span></span>

<span data-ttu-id="288c1-153">Ein Beispiel finden Sie unter Auflisten von [Akku Geräten](enumerating-battery-devices.md).</span><span class="sxs-lookup"><span data-stu-id="288c1-153">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="288c1-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="288c1-154">Requirements</span></span>



| <span data-ttu-id="288c1-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="288c1-155">Requirement</span></span> | <span data-ttu-id="288c1-156">Wert</span><span class="sxs-lookup"><span data-stu-id="288c1-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="288c1-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="288c1-157">Minimum supported client</span></span><br/> | <span data-ttu-id="288c1-158">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="288c1-158">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="288c1-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="288c1-159">Minimum supported server</span></span><br/> | <span data-ttu-id="288c1-160">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="288c1-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="288c1-161">Header</span><span class="sxs-lookup"><span data-stu-id="288c1-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="288c1-162"><dt>Poclass. h; </dt> <dt>Batclass. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="288c1-162"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="288c1-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="288c1-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="288c1-164">Akku Informationen</span><span class="sxs-lookup"><span data-stu-id="288c1-164">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="288c1-165">Steuerungs Codes der Energie Verwaltung</span><span class="sxs-lookup"><span data-stu-id="288c1-165">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="288c1-166">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="288c1-166">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="288c1-167">**IOCTL- \_ Akku \_ Abfrage \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="288c1-167">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="288c1-168">**IOCTL \_ Akku \_ Query- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="288c1-168">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="288c1-169">**IOCTL- \_ Akku \_ Satz \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="288c1-169">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

