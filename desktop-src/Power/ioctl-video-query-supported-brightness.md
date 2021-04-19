---
description: Ruft die unterstützten Timeout-Ebenen ab.
ms.assetid: b4c1ee3f-af75-477e-b7ed-53be905374d7
title: IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS Steuerungs Code (ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a5618ec29fd47ba690106b5f826e6fb145eac208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349216"
---
# <a name="ioctl_video_query_supported_brightness-control-code"></a><span data-ttu-id="c1c64-103">\_ \_ \_ Unterstützte \_ Helligkeit-Steuerungs Code durch ioctl-Video Abfrage</span><span class="sxs-lookup"><span data-stu-id="c1c64-103">IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS control code</span></span>

<span data-ttu-id="c1c64-104">Ruft die unterstützten Timeout-Ebenen ab.</span><span class="sxs-lookup"><span data-stu-id="c1c64-104">Retrieves the supported backlight levels.</span></span>

<span data-ttu-id="c1c64-105">Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.</span><span class="sxs-lookup"><span data-stu-id="c1c64-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="c1c64-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1c64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1c64-107">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="c1c64-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="c1c64-108">Ein Handle für den \\ \\ . \\ LCD-Gerät.</span><span class="sxs-lookup"><span data-stu-id="c1c64-108">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="c1c64-109">Rufen Sie zum Abrufen eines Geräte [**Handles die Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.</span><span class="sxs-lookup"><span data-stu-id="c1c64-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="c1c64-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="c1c64-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="c1c64-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c1c64-111">The control code for the operation.</span></span> <span data-ttu-id="c1c64-112">Dieser Wert identifiziert den spezifischen Vorgang, der ausgeführt werden soll, und den Typ des Geräts, auf dem es ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1c64-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="c1c64-113">Verwenden Sie die **IOCTL- \_ Video \_ Abfrage \_ unterstützte \_ Helligkeit** für diesen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c1c64-113">Use **IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="c1c64-114">*lpinbuffer*</span><span class="sxs-lookup"><span data-stu-id="c1c64-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="c1c64-115">Wird bei diesem Vorgang nicht verwendet. auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c1c64-115">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c1c64-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="c1c64-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="c1c64-117">Wird bei diesem Vorgang nicht verwendet. auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c1c64-117">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="c1c64-118">*lpoutbuffer*</span><span class="sxs-lookup"><span data-stu-id="c1c64-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="c1c64-119">Ein Zeiger auf einen Puffer, der ein Array der verfügbaren Energie Stufen empfängt.</span><span class="sxs-lookup"><span data-stu-id="c1c64-119">A pointer to a buffer that receives an array of the available power levels.</span></span> <span data-ttu-id="c1c64-120">Dieser Puffer sollte 256 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="c1c64-120">This buffer should be 256 bytes long.</span></span>

</dd> <dt>

<span data-ttu-id="c1c64-121">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="c1c64-121">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="c1c64-122">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="c1c64-122">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c1c64-123">*lpbyteszurück gegeben*</span><span class="sxs-lookup"><span data-stu-id="c1c64-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="c1c64-124">Ein Zeiger auf eine Variable, die die Größe der zurückgegebenen Ausgabedaten in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="c1c64-124">A pointer to a variable that receives the size, in bytes, of output data returned.</span></span>

<span data-ttu-id="c1c64-125">Wenn der Ausgabepuffer zu klein ist, um Daten zurückzugeben, schlägt der-Befehl fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode Fehler \_ unzureichend zurück \_ , und die zurückgegebene Byte Anzahl ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c1c64-125">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="c1c64-126">Wenn der Ausgabepuffer zu klein ist, um alle Daten aufzunehmen, aber einige Einträge enthalten kann, gibt das Betriebssystem die gleichen Anforderungen zurück, der Rückruf schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode für \_ Weitere \_ Daten zurück, und *lpbytesreturns* gibt die Menge der zurückgegebenen Daten an.</span><span class="sxs-lookup"><span data-stu-id="c1c64-126">If the output buffer is too small to hold all of the data but can hold some entries, then the operating system returns as much as fits, the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_MORE\_DATA, and *lpBytesReturned* indicates the amount of data returned.</span></span> <span data-ttu-id="c1c64-127">Die Anwendung sollte [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit dem gleichen Vorgang erneut aufzurufen, wobei ein neuer Startpunkt angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c1c64-127">Your application should call [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) again with the same operation, specifying a new starting point.</span></span>

<span data-ttu-id="c1c64-128">Wenn *lpoverllapp* den Wert **null** hat (nicht überlappende e/a), kann *lpbytesgab* nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c1c64-128">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="c1c64-129">Wenn *lpoverllapp* nicht **null** (überlappende e/a) ist, kann *lpbytesgab* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c1c64-129">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="c1c64-130">Wenn dies ein überlappende Vorgang ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetOverLappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c1c64-130">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="c1c64-131">Wenn *hdevice* einem e/a-Abschlussport zugeordnet ist, können Sie die Anzahl der Bytes abrufen, die durch Aufrufen der [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c1c64-131">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="c1c64-132">*lpoverlgetauscht*</span><span class="sxs-lookup"><span data-stu-id="c1c64-132">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="c1c64-133">Ein Zeiger auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.</span><span class="sxs-lookup"><span data-stu-id="c1c64-133">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="c1c64-134">Wenn *hdevice* mit dem überlappenden \_ Flag für das Dateiflag geöffnet wurde \_ , muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="c1c64-134">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="c1c64-135">In diesem Fall wird der Vorgang als überlappende (asynchrone) Vorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1c64-135">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="c1c64-136">Wenn das Gerät mit dem überlappenden \_ Flag für das Dateiflag geöffnet wurde \_ und *lpoverlgetauscht* den Wert **null** hat, schlägt die Funktion auf unvorhersehbare Weise fehl.</span><span class="sxs-lookup"><span data-stu-id="c1c64-136">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="c1c64-137">Wenn *hdevice* ohne Angabe des überlappenden \_ Flags für das Dateiflag geöffnet wurde \_ , wird *lpoverllapp* ignoriert, und [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) wird nicht zurückgegeben, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="c1c64-137">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1c64-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1c64-138">Return value</span></span>

<span data-ttu-id="c1c64-139">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c1c64-139">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="c1c64-140">Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c1c64-140">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="c1c64-141">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="c1c64-141">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="c1c64-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1c64-142">Remarks</span></span>

<span data-ttu-id="c1c64-143">Jedes Element im *lpoutbuffer* -Array ist ein Byte lang.</span><span class="sxs-lookup"><span data-stu-id="c1c64-143">Each element in the *lpOutBuffer* array is one byte in length.</span></span> <span data-ttu-id="c1c64-144">Daher gibt der *lpbytesreturn* -Parameter bei der Rückgabe die Anzahl der unterstützten Ebenen an.</span><span class="sxs-lookup"><span data-stu-id="c1c64-144">Therefore, upon return, the *lpBytesReturned* parameter indicates the number of supported levels.</span></span> <span data-ttu-id="c1c64-145">Jede Ebene ist ein Wert zwischen 0 und 100.</span><span class="sxs-lookup"><span data-stu-id="c1c64-145">Each level is a value from 0 to 100.</span></span> <span data-ttu-id="c1c64-146">Je größer der Wert, desto heller ist das Backlight.</span><span class="sxs-lookup"><span data-stu-id="c1c64-146">The larger the value, the brighter the backlight.</span></span> <span data-ttu-id="c1c64-147">Alle Ebenen werden unterstützt, unabhängig davon, ob es sich um eine Stromversorgung der Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="c1c64-147">All levels are supported whether the power source is AC or DC.</span></span>

<span data-ttu-id="c1c64-148">Die Header Datei, die zum Erstellen von Anwendungen verwendet wird, die diese Funktion (ntddvdeo. h) enthalten, ist im Microsoft Windows Driver Development Kit (DDK) enthalten.</span><span class="sxs-lookup"><span data-stu-id="c1c64-148">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="c1c64-149">Weitere Informationen zum Abrufen des DDK finden Sie unter [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .</span><span class="sxs-lookup"><span data-stu-id="c1c64-149">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="c1c64-150">Alternativ können Sie diesen Steuerelement Code wie folgt definieren:</span><span class="sxs-lookup"><span data-stu-id="c1c64-150">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x125, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="c1c64-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1c64-151">Requirements</span></span>



| <span data-ttu-id="c1c64-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1c64-152">Requirement</span></span> | <span data-ttu-id="c1c64-153">Wert</span><span class="sxs-lookup"><span data-stu-id="c1c64-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1c64-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1c64-154">Minimum supported client</span></span><br/> | <span data-ttu-id="c1c64-155">Windows Vista, Windows XP mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1c64-155">Windows Vista, Windows XP with SP1 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="c1c64-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1c64-156">Minimum supported server</span></span><br/> | <span data-ttu-id="c1c64-157">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1c64-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c1c64-158">Header</span><span class="sxs-lookup"><span data-stu-id="c1c64-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1c64-159"><dt>Ntddvdeo. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1c64-159"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1c64-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1c64-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c64-161">Backlight-Steuerungs Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c1c64-161">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="c1c64-162">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="c1c64-162">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

