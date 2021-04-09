---
description: Legt verschiedene Akku Informationen fest.
ms.assetid: b827983d-5fb8-43f2-b732-541d16b3eb7b
title: IOCTL_BATTERY_SET_INFORMATION Steuerungs Code (poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: f540037486f16e920b3346620ff934b279652e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865080"
---
# <a name="ioctl_battery_set_information-control-code"></a><span data-ttu-id="37062-103">Code der IOCTL- \_ Akku \_ Satz- \_ Informations Steuerung</span><span class="sxs-lookup"><span data-stu-id="37062-103">IOCTL\_BATTERY\_SET\_INFORMATION control code</span></span>

<span data-ttu-id="37062-104">Legt verschiedene Akku Informationen fest.</span><span class="sxs-lookup"><span data-stu-id="37062-104">Sets various battery information.</span></span> <span data-ttu-id="37062-105">Die Eingabeparameter Struktur, [**Batterie \_ Satz \_ Informationen**](battery-set-information-str.md), gibt an, welche Akku Statusinformationen festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="37062-105">The input parameter structure, [**BATTERY\_SET\_INFORMATION**](battery-set-information-str.md), indicates which battery status information is to be set.</span></span>

<span data-ttu-id="37062-106">Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.</span><span class="sxs-lookup"><span data-stu-id="37062-106">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to battery
  IOCTL_BATTERY_SET_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,           // input buffer
  (DWORD) nInBufferSize,         // size of input buffer
  NULL,                          // lpOutBuffer
  0,                             // nOutBufferSize
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="37062-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="37062-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37062-108">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="37062-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="37062-109">Ein Handle für den Akku, auf dem die Informationen festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="37062-109">A handle to the battery on which the information is to be set.</span></span> <span data-ttu-id="37062-110">Rufen Sie zum Abrufen eines Geräte [**Handles die Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.</span><span class="sxs-lookup"><span data-stu-id="37062-110">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="37062-111">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="37062-111">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="37062-112">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="37062-112">The control code for the operation.</span></span> <span data-ttu-id="37062-113">Dieser Wert identifiziert den spezifischen Vorgang, der ausgeführt werden soll, und den Typ des Geräts, auf dem es ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="37062-113">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="37062-114">Verwenden Sie die **IOCTL- \_ Akku \_ Satz \_ Informationen** für diesen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="37062-114">Use **IOCTL\_BATTERY\_SET\_INFORMATION** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="37062-115">*lpinbuffer*</span><span class="sxs-lookup"><span data-stu-id="37062-115">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="37062-116">Ein Zeiger auf eine [**Batterie \_ Satz \_ Informations**](battery-set-information-str.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="37062-116">A pointer to a [**BATTERY\_SET\_INFORMATION**](battery-set-information-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="37062-117">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="37062-117">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="37062-118">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="37062-118">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="37062-119">*lpoutbuffer*</span><span class="sxs-lookup"><span data-stu-id="37062-119">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="37062-120">Wird bei diesem Vorgang nicht verwendet. auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="37062-120">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="37062-121">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="37062-121">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="37062-122">Wird bei diesem Vorgang nicht verwendet. auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="37062-122">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="37062-123">*lpbyteszurück gegeben*</span><span class="sxs-lookup"><span data-stu-id="37062-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="37062-124">Ein Zeiger auf eine Variable, die die Größe der im *lpoutbuffer* -Puffer zurückgegebenen Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="37062-124">A pointer to a variable that receives the size of data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="37062-125">Wenn der Ausgabepuffer zu klein ist, um Daten zurückzugeben, schlägt der-Befehl fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode Fehler \_ unzureichend zurück \_ , und die zurückgegebene Byte Anzahl ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="37062-125">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="37062-126">Wenn *lpoverllapp* den Wert **null** hat (nicht überlappende e/a), kann *lpbytesgab* nicht **null** sein, auch wenn *lpoutbuffer* **null** ist.</span><span class="sxs-lookup"><span data-stu-id="37062-126">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**, even if *lpOutBuffer* is **NULL**.</span></span>

<span data-ttu-id="37062-127">Wenn *lpoverllapp* nicht **null** (überlappende e/a) ist, kann *lpbytesgab* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="37062-127">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="37062-128">Wenn dies ein überlappende Vorgang ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetOverLappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="37062-128">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="37062-129">Wenn *hdevice* einem e/a-Abschlussport zugeordnet ist, können Sie die Anzahl der Bytes abrufen, die durch Aufrufen der [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="37062-129">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="37062-130">*lpoverlgetauscht*</span><span class="sxs-lookup"><span data-stu-id="37062-130">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="37062-131">Ein Zeiger auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.</span><span class="sxs-lookup"><span data-stu-id="37062-131">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="37062-132">Wenn *hdevice* mit dem überlappenden \_ Flag für das Dateiflag geöffnet wurde \_ , muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="37062-132">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="37062-133">In diesem Fall wird [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37062-133">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="37062-134">Wenn das Gerät mit dem überlappenden \_ Flag für das Dateiflag geöffnet wurde \_ und *lpoverlgetauscht* den Wert **null** hat, schlägt die Funktion auf unvorhersehbare Weise fehl.</span><span class="sxs-lookup"><span data-stu-id="37062-134">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="37062-135">Wenn *hdevice* ohne Angabe des überlappenden \_ Flag für das Dateiflag geöffnet wurde \_ , wird *lpoverlgetauscht* ignoriert, und die [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) -Funktion gibt nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="37062-135">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37062-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37062-136">Return value</span></span>

<span data-ttu-id="37062-137">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="37062-137">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="37062-138">Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="37062-138">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="37062-139">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="37062-139">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="37062-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37062-140">Remarks</span></span>

<span data-ttu-id="37062-141">Alle Anforderungen zum Festlegen der Akku Informationen werden mit dem Status "Fehler \_ Datei \_ nicht \_ gefunden", wenn das Akku-Tag der Anforderung nicht mit der des aktuellen Akku-Tags identisch ist, vervollständigt.</span><span class="sxs-lookup"><span data-stu-id="37062-141">All requests to set battery information will complete with the status of ERROR\_FILE\_NOT\_FOUND if the battery tag of the request does not match that of the current battery tag.</span></span>

<span data-ttu-id="37062-142">Informationen zu den Auswirkungen von überlappenden e/a-Vorgängen für diesen Vorgang finden Sie im Abschnitt "Hinweise" des Themas " [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ".</span><span class="sxs-lookup"><span data-stu-id="37062-142">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="37062-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37062-143">Requirements</span></span>



| <span data-ttu-id="37062-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37062-144">Requirement</span></span> | <span data-ttu-id="37062-145">Wert</span><span class="sxs-lookup"><span data-stu-id="37062-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37062-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37062-146">Minimum supported client</span></span><br/> | <span data-ttu-id="37062-147">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37062-147">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="37062-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37062-148">Minimum supported server</span></span><br/> | <span data-ttu-id="37062-149">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37062-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="37062-150">Header</span><span class="sxs-lookup"><span data-stu-id="37062-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="37062-151"><dt>Poclass. h; </dt> <dt>Batclass. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="37062-151"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37062-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37062-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37062-153">Akku Informationen</span><span class="sxs-lookup"><span data-stu-id="37062-153">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="37062-154">Steuerungs Codes der Energie Verwaltung</span><span class="sxs-lookup"><span data-stu-id="37062-154">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="37062-155">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="37062-155">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="37062-156">**Informationen zum Akku \_ Satz \_**</span><span class="sxs-lookup"><span data-stu-id="37062-156">**BATTERY\_SET\_INFORMATION**</span></span>](battery-set-information-str.md)
</dt> <dt>

[<span data-ttu-id="37062-157">**IOCTL- \_ Akku \_ Abfrage \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="37062-157">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="37062-158">**IOCTL \_ Akku \_ Query- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="37062-158">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="37062-159">**IOCTL \_ Akku \_ - \_ abfragetag**</span><span class="sxs-lookup"><span data-stu-id="37062-159">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> </dl>

 

