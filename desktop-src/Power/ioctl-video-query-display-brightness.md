---
description: Ruft die aktuellen AC-und DC-Timeout-Ebenen und den aktuellen Energiezustand ab.
ms.assetid: c7b7c302-6e92-46a7-b9a6-e3f2a3e44d1b
title: IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS Steuerungs Code (ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: 547501a28492aecfe06f63f95b0e007fc80d3d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358891"
---
# <a name="ioctl_video_query_display_brightness-control-code"></a><span data-ttu-id="da9fb-103">IOCTL- \_ Video \_ Abfrage \_ Anzeige \_ Helligkeits Steuerungs Code</span><span class="sxs-lookup"><span data-stu-id="da9fb-103">IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS control code</span></span>

<span data-ttu-id="da9fb-104">\[Dieser Steuerungs Code ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="da9fb-104">\[This control code is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="da9fb-105">Die Unterstützung für diesen Steuerungs Code wurde in Windows Server 2008 und Windows Vista entfernt.</span><span class="sxs-lookup"><span data-stu-id="da9fb-105">Support for this control code was removed in Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="da9fb-106">Verwenden Sie stattdessen die [**wmimonitorbrightness**](/windows/desktop/WmiCoreProv/wmimonitorbrightness) -Klasse.\]</span><span class="sxs-lookup"><span data-stu-id="da9fb-106">Use the [**WmiMonitorBrightness**](/windows/desktop/WmiCoreProv/wmimonitorbrightness) class instead.\]</span></span>

<span data-ttu-id="da9fb-107">Ruft die aktuellen AC-und DC-Timeout-Ebenen und den aktuellen Energiezustand ab.</span><span class="sxs-lookup"><span data-stu-id="da9fb-107">Retrieves the current AC and DC backlight levels and the current power state.</span></span>

<span data-ttu-id="da9fb-108">Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.</span><span class="sxs-lookup"><span data-stu-id="da9fb-108">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="da9fb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="da9fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da9fb-110">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="da9fb-110">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="da9fb-111">Ein Handle für den \\ \\ . \\ LCD-Gerät.</span><span class="sxs-lookup"><span data-stu-id="da9fb-111">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="da9fb-112">Rufen Sie zum Abrufen eines Geräte [**Handles die Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.</span><span class="sxs-lookup"><span data-stu-id="da9fb-112">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="da9fb-113">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="da9fb-113">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="da9fb-114">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="da9fb-114">The control code for the operation.</span></span> <span data-ttu-id="da9fb-115">Dieser Wert identifiziert den spezifischen Vorgang, der ausgeführt werden soll, und den Typ des Geräts, auf dem es ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="da9fb-115">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="da9fb-116">Verwenden Sie die **IOCTL- \_ Video \_ Abfrage \_ Anzeige \_ Helligkeit** für diesen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="da9fb-116">Use **IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="da9fb-117">*lpinbuffer*</span><span class="sxs-lookup"><span data-stu-id="da9fb-117">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="da9fb-118">Wird bei diesem Vorgang nicht verwendet. auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da9fb-118">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="da9fb-119">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="da9fb-119">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="da9fb-120">Wird bei diesem Vorgang nicht verwendet. auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da9fb-120">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="da9fb-121">*lpoutbuffer*</span><span class="sxs-lookup"><span data-stu-id="da9fb-121">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="da9fb-122">Ein Zeiger auf einen Puffer, der eine [**Anzeige \_ Helligkeit**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) -Struktur empfängt.</span><span class="sxs-lookup"><span data-stu-id="da9fb-122">A pointer to a buffer that will receive a [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="da9fb-123">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="da9fb-123">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="da9fb-124">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="da9fb-124">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="da9fb-125">*lpbyteszurück gegeben*</span><span class="sxs-lookup"><span data-stu-id="da9fb-125">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="da9fb-126">Ein Zeiger auf eine Variable, die die Größe der zurückgegebenen Ausgabedaten in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="da9fb-126">A pointer to a variable that receives the size, in bytes, of output data returned.</span></span>

<span data-ttu-id="da9fb-127">Wenn der Ausgabepuffer zu klein ist, um Daten zurückzugeben, schlägt der-Befehl fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode Fehler \_ unzureichend zurück \_ , und die zurückgegebene Byte Anzahl ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="da9fb-127">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="da9fb-128">Wenn der Ausgabepuffer zu klein ist, um alle Daten aufzunehmen, aber einige Einträge enthalten kann, gibt das Betriebssystem die gleichen Anforderungen zurück, der Rückruf schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode für \_ Weitere \_ Daten zurück, und *lpbytesreturns* gibt die Menge der zurückgegebenen Daten an.</span><span class="sxs-lookup"><span data-stu-id="da9fb-128">If the output buffer is too small to hold all of the data but can hold some entries, then the operating system returns as much as fits, the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_MORE\_DATA, and *lpBytesReturned* indicates the amount of data returned.</span></span> <span data-ttu-id="da9fb-129">Die Anwendung sollte [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit dem gleichen Vorgang erneut aufzurufen, wobei ein neuer Startpunkt angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="da9fb-129">Your application should call [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) again with the same operation, specifying a new starting point.</span></span>

<span data-ttu-id="da9fb-130">Wenn *lpoverllapp* den Wert **null** hat (nicht überlappende e/a), kann *lpbytesgab* nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="da9fb-130">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="da9fb-131">Wenn *lpoverllapp* nicht **null** (überlappende e/a) ist, kann *lpbytesgab* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="da9fb-131">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="da9fb-132">Wenn dies ein überlappende Vorgang ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetOverLappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="da9fb-132">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="da9fb-133">Wenn *hdevice* einem e/a-Abschlussport zugeordnet ist, können Sie die Anzahl der Bytes abrufen, die durch Aufrufen der [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="da9fb-133">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="da9fb-134">*lpoverlgetauscht*</span><span class="sxs-lookup"><span data-stu-id="da9fb-134">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="da9fb-135">Ein Zeiger auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.</span><span class="sxs-lookup"><span data-stu-id="da9fb-135">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="da9fb-136">Wenn *hdevice* mit dem überlappenden \_ Flag für das Dateiflag geöffnet wurde \_ , muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="da9fb-136">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="da9fb-137">In diesem Fall wird der Vorgang als überlappende (asynchrone) Vorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da9fb-137">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="da9fb-138">Wenn das Gerät mit dem überlappenden \_ Flag für das Dateiflag geöffnet wurde \_ und *lpoverlgetauscht* den Wert **null** hat, schlägt die Funktion auf unvorhersehbare Weise fehl.</span><span class="sxs-lookup"><span data-stu-id="da9fb-138">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="da9fb-139">Wenn *hdevice* ohne Angabe des überlappenden \_ Flags für das Dateiflag geöffnet wurde \_ , wird *lpoverllapp* ignoriert, und [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) wird nicht zurückgegeben, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="da9fb-139">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da9fb-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da9fb-140">Return value</span></span>

<span data-ttu-id="da9fb-141">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="da9fb-141">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="da9fb-142">Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="da9fb-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="da9fb-143">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="da9fb-143">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="da9fb-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da9fb-144">Remarks</span></span>

<span data-ttu-id="da9fb-145">Die Header Datei, die zum Erstellen von Anwendungen verwendet wird, die diese Funktion (ntddvdeo. h) enthalten, ist im Microsoft Windows Driver Development Kit (DDK) enthalten.</span><span class="sxs-lookup"><span data-stu-id="da9fb-145">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="da9fb-146">Weitere Informationen zum Abrufen des DDK finden Sie unter [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .</span><span class="sxs-lookup"><span data-stu-id="da9fb-146">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="da9fb-147">Alternativ können Sie diesen Steuerelement Code wie folgt definieren:</span><span class="sxs-lookup"><span data-stu-id="da9fb-147">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x126, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="da9fb-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da9fb-148">Requirements</span></span>



| <span data-ttu-id="da9fb-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da9fb-149">Requirement</span></span> | <span data-ttu-id="da9fb-150">Wert</span><span class="sxs-lookup"><span data-stu-id="da9fb-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da9fb-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da9fb-151">Minimum supported client</span></span><br/> | <span data-ttu-id="da9fb-152">Nur Windows XP mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da9fb-152">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da9fb-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da9fb-153">Minimum supported server</span></span><br/> | <span data-ttu-id="da9fb-154">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da9fb-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da9fb-155">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="da9fb-155">End of client support</span></span><br/>    | <span data-ttu-id="da9fb-156">Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="da9fb-156">Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="da9fb-157">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="da9fb-157">End of server support</span></span><br/>    | <span data-ttu-id="da9fb-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="da9fb-158">Windows Server 2003 R2</span></span><br/>                                                     |
| <span data-ttu-id="da9fb-159">Header</span><span class="sxs-lookup"><span data-stu-id="da9fb-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="da9fb-160"><dt>Ntddvdeo. h</dt></span><span class="sxs-lookup"><span data-stu-id="da9fb-160"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da9fb-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da9fb-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da9fb-162">Backlight-Steuerungs Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="da9fb-162">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="da9fb-163">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="da9fb-163">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

<span data-ttu-id="da9fb-164">[**\_Helligkeit anzeigen**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="da9fb-164">[**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="da9fb-165">**Anzeige Helligkeit für IOCTL- \_ Video \_ Satz \_ \_**</span><span class="sxs-lookup"><span data-stu-id="da9fb-165">**IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS**</span></span>](ioctl-video-set-display-brightness.md)
</dt> </dl>

 

