---
description: Legt die aktuellen AC-und DC-Timeout-Ebenen fest.
ms.assetid: baa77811-046d-4a07-b3df-2a31fba2d9a7
title: IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS Steuerungs Code (ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a0c679f352012eea66b80335bc3ad1547501dd92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959742"
---
# <a name="ioctl_video_set_display_brightness-control-code"></a><span data-ttu-id="45711-103">IOCTL- \_ Video \_ Satz Anzeige des \_ \_ Helligkeits Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="45711-103">IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS control code</span></span>

<span data-ttu-id="45711-104">Legt die aktuellen AC-und DC-Timeout-Ebenen fest.</span><span class="sxs-lookup"><span data-stu-id="45711-104">Sets the current AC and DC backlight levels.</span></span>

<span data-ttu-id="45711-105">Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.</span><span class="sxs-lookup"><span data-stu-id="45711-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS, // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of the input buffer
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize 
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="45711-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="45711-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45711-107">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="45711-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="45711-108">Ein Handle für den \\ \\ . \\ LCD-Gerät.</span><span class="sxs-lookup"><span data-stu-id="45711-108">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="45711-109">Rufen Sie zum Abrufen eines Geräte [**Handles die Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.</span><span class="sxs-lookup"><span data-stu-id="45711-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="45711-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="45711-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="45711-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="45711-111">The control code for the operation.</span></span> <span data-ttu-id="45711-112">Dieser Wert identifiziert den spezifischen Vorgang, der ausgeführt werden soll, und den Typ des Geräts, auf dem es ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="45711-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="45711-113">Verwenden Sie die **IOCTL- \_ Video \_ Satz \_ Anzeige \_ Helligkeit** für diesen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="45711-113">Use **IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="45711-114">*lpinbuffer*</span><span class="sxs-lookup"><span data-stu-id="45711-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="45711-115">Ein Zeiger auf eine [**Anzeige \_ Helligkeits**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) Struktur.</span><span class="sxs-lookup"><span data-stu-id="45711-115">A pointer to a [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="45711-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="45711-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="45711-117">Die Größe des Puffers, auf den *lpoutbuffer* zeigt (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="45711-117">The size of the buffer pointed to by *lpOutBuffer*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="45711-118">*lpoutbuffer*</span><span class="sxs-lookup"><span data-stu-id="45711-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="45711-119">Wird bei diesem Vorgang nicht verwendet. auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="45711-119">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="45711-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="45711-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="45711-121">Wird bei diesem Vorgang nicht verwendet. auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="45711-121">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="45711-122">*lpbyteszurück gegeben*</span><span class="sxs-lookup"><span data-stu-id="45711-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="45711-123">Ein Zeiger auf eine Variable, die die tatsächliche Anzahl von Bytes empfängt, die von der Funktion im Ausgabepuffer zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="45711-123">A pointer to a variable that receives the actual count of bytes returned by the function in the output buffer.</span></span>

<span data-ttu-id="45711-124">Wenn " *lpoverlused* " **null** (nicht überlappende e/a) ist, wird " *lpbytesused* " intern verwendet und kann nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="45711-124">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* is used internally and cannot be **NULL**.</span></span>

<span data-ttu-id="45711-125">Wenn *lpoverllapp* nicht **null** (überlappende e/a) ist, kann *lpbytesgab* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="45711-125">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="45711-126">*lpoverlgetauscht*</span><span class="sxs-lookup"><span data-stu-id="45711-126">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="45711-127">Ein Zeiger auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.</span><span class="sxs-lookup"><span data-stu-id="45711-127">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="45711-128">Wenn *hdevice* mit dem überlappenden \_ Flag für das Dateiflag geöffnet wurde \_ , muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="45711-128">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="45711-129">In diesem Fall wird der Vorgang als überlappende (asynchrone) Vorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="45711-129">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="45711-130">Wenn das Gerät mit dem überlappenden \_ Flag für das Dateiflag geöffnet wurde \_ und *lpoverlgetauscht* den Wert **null** hat, schlägt die Funktion auf unvorhersehbare Weise fehl.</span><span class="sxs-lookup"><span data-stu-id="45711-130">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="45711-131">Wenn *hdevice* ohne Angabe des überlappenden \_ Flags für das Dateiflag geöffnet wurde \_ , wird *lpoverllapp* ignoriert, und [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) wird nicht zurückgegeben, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="45711-131">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45711-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="45711-132">Return value</span></span>

<span data-ttu-id="45711-133">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="45711-133">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="45711-134">Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="45711-134">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="45711-135">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="45711-135">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="45711-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45711-136">Remarks</span></span>

<span data-ttu-id="45711-137">Die Werte, die in den Elementen **ucachelligkeit** und **ucdchelligkeit** der [**Anzeige \_ Helligkeits**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) Struktur angegeben sind, müssen zuvor von der [**\_ \_ \_ unterstützten \_ Helligkeit von IOCTL-Video Abfragen**](ioctl-video-query-supported-brightness.md)zurückgegeben worden sein.</span><span class="sxs-lookup"><span data-stu-id="45711-137">The values specified in the **ucACBrightness** and **ucDCBrightness** members of the [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure must have been previously returned by [**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**](ioctl-video-query-supported-brightness.md).</span></span> <span data-ttu-id="45711-138">Wenn die unterstützten Werte beispielsweise 10, 20, 30, 40, 50, 60, 70, 80, 90 und 100 sind, ist die Verwendung des Werts 33 ein Fehler.</span><span class="sxs-lookup"><span data-stu-id="45711-138">For example, if the supported values are 10, 20, 30, 40, 50, 60, 70, 80, 90, and 100, then using a value of 33 would be an error.</span></span>

<span data-ttu-id="45711-139">Die Header Datei, die zum Erstellen von Anwendungen verwendet wird, die diese Funktion (ntddvdeo. h) enthalten, ist im Microsoft Windows Driver Development Kit (DDK) enthalten.</span><span class="sxs-lookup"><span data-stu-id="45711-139">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="45711-140">Weitere Informationen zum Abrufen des DDK finden Sie unter [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .</span><span class="sxs-lookup"><span data-stu-id="45711-140">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="45711-141">Alternativ können Sie diesen Steuerelement Code wie folgt definieren:</span><span class="sxs-lookup"><span data-stu-id="45711-141">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x127, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="45711-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45711-142">Requirements</span></span>



| <span data-ttu-id="45711-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45711-143">Requirement</span></span> | <span data-ttu-id="45711-144">Wert</span><span class="sxs-lookup"><span data-stu-id="45711-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45711-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45711-145">Minimum supported client</span></span><br/> | <span data-ttu-id="45711-146">Windows Vista, Windows XP mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="45711-146">Windows Vista, Windows XP with SP1 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="45711-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45711-147">Minimum supported server</span></span><br/> | <span data-ttu-id="45711-148">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="45711-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="45711-149">Header</span><span class="sxs-lookup"><span data-stu-id="45711-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="45711-150"><dt>Ntddvdeo. h</dt></span><span class="sxs-lookup"><span data-stu-id="45711-150"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45711-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45711-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45711-152">Backlight-Steuerungs Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="45711-152">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="45711-153">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="45711-153">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

<span data-ttu-id="45711-154">[**\_Helligkeit anzeigen**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="45711-154">[**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="45711-155">**Bildschirmhelligkeit der IOCTL- \_ Video \_ Abfrage \_ \_**</span><span class="sxs-lookup"><span data-stu-id="45711-155">**IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS**</span></span>](ioctl-video-query-display-brightness.md)
</dt> <dt>

[<span data-ttu-id="45711-156">**\_ \_ \_ unterstützte \_ Helligkeit der IOCTL-Video Abfrage**</span><span class="sxs-lookup"><span data-stu-id="45711-156">**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**</span></span>](ioctl-video-query-supported-brightness.md)
</dt> </dl>

 

