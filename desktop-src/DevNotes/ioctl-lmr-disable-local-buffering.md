---
description: Der IOCTL \_ LMR \_ \_ \_ -Code zum Deaktivieren der lokalen Puffer Steuerung deaktiviert das lokale Zwischenspeichern von Daten beim Lesen von Daten aus oder Schreiben von Daten in eine Remote Datei. Dabei handelt es sich um einen intern definierten Steuerungs Code, der in einem öffentlichen Header nicht verfügbar ist.
ms.assetid: a464671b-253c-4f35-84a2-2619cb15b009
title: IOCTL_LMR_DISABLE_LOCAL_BUFFERING Steuerungs Codes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPY_CHUNK
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0d596402c489caee972e1305f2a32881312fd3e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342972"
---
# <a name="ioctl_lmr_disable_local_buffering-control-code"></a><span data-ttu-id="fd6d5-104">IOCTL \_ LMR \_ deaktiviert \_ den Code für die lokale \_ Puffer Steuerung.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-104">IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING control code</span></span>

<span data-ttu-id="fd6d5-105">Der **IOCTL \_ LMR-Code zum \_ Deaktivieren der \_ lokalen \_ Puffer** Steuerung deaktiviert das lokale Zwischenspeichern von Daten beim Lesen von Daten aus oder Schreiben von Daten in eine Remote Datei.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-105">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code disables local client-side in-memory caching of data when reading data from or writing data to a remote file.</span></span> <span data-ttu-id="fd6d5-106">Dabei handelt es sich um einen intern definierten Steuerungs Code, der in einem öffentlichen Header nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-106">This is an internally-defined control code not available in a public header.</span></span>

<span data-ttu-id="fd6d5-107">Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-107">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_LMR_DISABLE_LOCAL_BUFFERING, // dwIoControlCode
  (LPVOID) NULL,                // lpInBuffer
  (DWORD) 0,                    // nInBufferSize
  (LPVOID) NULL,                // lpOutBuffer
  (DWORD) 0,                    // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="fd6d5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd6d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd6d5-109">*hdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd6d5-109">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6d5-110">Ein Handle für die Remote Datei.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-110">A handle to the remote file.</span></span> <span data-ttu-id="fd6d5-111">Um dieses Handle zu erhalten, rufen [**Sie die Funktion**](/windows/win32/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-111">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="fd6d5-112">*dwIoControlCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd6d5-112">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6d5-113">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-113">The control code for the operation.</span></span> <span data-ttu-id="fd6d5-114">Verwenden Sie für diesen Vorgang den Wert 0x140390.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-114">Use the value 0x140390 for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="fd6d5-115">*lpinbuffer*</span><span class="sxs-lookup"><span data-stu-id="fd6d5-115">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="fd6d5-116">Nicht verwendet, muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-116">Not used, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fd6d5-117">*nInBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd6d5-117">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6d5-118">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-118">The size of the input buffer, in bytes.</span></span> <span data-ttu-id="fd6d5-119">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-119">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fd6d5-120">*lpoutbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fd6d5-120">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6d5-121">Nicht verwendet, muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-121">Not used, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fd6d5-122">*nOutBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd6d5-122">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6d5-123">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-123">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="fd6d5-124">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-124">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fd6d5-125">*lpbyteszurück gegeben* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fd6d5-125">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6d5-126">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-126">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="fd6d5-127">Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, die [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt einen **fehlerhaften \_ \_ Puffer** zurück, und *lpbytesreturns* ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="fd6d5-127">If the output buffer is too small, then the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="fd6d5-128">Wenn der *lpoverllapp* -Parameter **null** ist, kann *lpbytes-Rückgabe* Wert nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-128">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="fd6d5-129">Selbst wenn ein Vorgang keine Ausgabedaten zurückgibt und der *lpoutbuffer* -Parameter den Wert **null** hat, verwendet [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) *lpbytesreturn*.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-129">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="fd6d5-130">Nach einem solchen Vorgang ist der Wert von *lpbytesno* bedeutungslos.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-130">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="fd6d5-131">Wenn *lpoverllapp* nicht **null** ist, kann *lpbytesgab* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-131">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="fd6d5-132">Wenn *lpoverlgetauscht* nicht **null** ist und der Vorgang Daten zurückgibt, ist *lpbytesreturns* bedeutungslos, bis der überlappende Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-132">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="fd6d5-133">Um die Anzahl der zurückgegebenen Bytes abzurufen, rufen Sie die Funktion [**ge-verlappedresult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) auf.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-133">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="fd6d5-134">Wenn der *hdevice* -Parameter einem e/a-Abschlussport zugeordnet ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-134">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="fd6d5-135">*lpoverlgetauscht* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd6d5-135">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6d5-136">Ein Zeiger auf eine [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-136">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="fd6d5-137">Wenn der *hdevice* -Parameter ohne Angabe eines **überlappenden \_ Dateiflags \_** geöffnet wurde, wird *lpoverlgetauscht* ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-137">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="fd6d5-138">Wenn *hdevice* mit dem überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, wird der Vorgang als überlappende (asynchrone) Vorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-138">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="fd6d5-139">In diesem Fall muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur verweisen, die ein Handle für ein Ereignis Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-139">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="fd6d5-140">Andernfalls schlägt die Funktion auf unvorhersehbare Weise fehl.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-140">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="fd6d5-141">Bei überlappenden Vorgängen gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) sofort zurück, und das Ereignis Objekt wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-141">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="fd6d5-142">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-142">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd6d5-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd6d5-143">Return value</span></span>

<span data-ttu-id="fd6d5-144">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-144">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="fd6d5-145">Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-145">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="fd6d5-146">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-146">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="fd6d5-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd6d5-147">Remarks</span></span>

<span data-ttu-id="fd6d5-148">Der **ioctl LMR-Code für die \_ \_ \_ lokale \_ Puffer Aktivierung** wird intern vom System als 0x140390 und nicht in einer öffentlichen Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-148">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code is defined internally by the system as 0x140390 and not in a public header file.</span></span> <span data-ttu-id="fd6d5-149">Sie wird von Anwendungen für zweckgebundene Anwendungen verwendet, um das Client seitige Zwischenspeichern von Daten beim Lesen von Daten aus oder das Schreiben von Daten in eine Remote Datei zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-149">It is used by special-purpose applications to disable local client-side in-memory caching of data when reading data from or writing data to a remote file.</span></span> <span data-ttu-id="fd6d5-150">Nach der Deaktivierung der lokalen Pufferung bleibt die Einstellung wirksam, bis alle geöffneten Handles für die Datei geschlossen sind und der Redirector die internen Datenstrukturen bereinigt.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-150">After local buffering is disabled, the setting remains in effect until all open handles to the file are closed and the redirector cleans up its internal data structures.</span></span>

<span data-ttu-id="fd6d5-151">Anwendungen für allgemeine Zwecke sollten nicht **IOCTL \_ LMR \_ Deaktivieren \_ lokale \_ Pufferung** verwenden, da dies zu einem übermäßigen Netzwerkverkehr und einem zugehörigen Leistungsverlust führen kann.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-151">General-purpose applications should not use **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING**, because it can result in excessive network traffic and associated loss of performance.</span></span> <span data-ttu-id="fd6d5-152">Der **ioctl-LMR-Code für die \_ \_ \_ lokale \_ Puffer Aktivierung** sollte nur in spezialisierten Anwendungen verwendet werden, die große Datenmengen über das Netzwerk verschieben, während versucht wird, die Nutzung der Netzwerkbandbreite zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-152">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code should be used only in specialized applications moving large amounts of data over the network while attempting to maximize use of network bandwidth.</span></span> <span data-ttu-id="fd6d5-153">Die Funktionen [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) und [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) verwenden z. b. **IOCTL \_ LMR \_ \_ \_** , um die Leistung großer Datei Kopien zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-153">For example, the [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) and [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) functions use **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** to improve large file copy performance.</span></span>

<span data-ttu-id="fd6d5-154">**IOCTL \_ LMR- \_ Deaktivierung der \_ lokalen \_ Pufferung** wird nicht von lokalen Dateisystemen implementiert, und die Fehlermeldung " **\_ ungültige \_ Funktion**" schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-154">**IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** is not implemented by local file systems and will fail with the error **ERROR\_INVALID\_FUNCTION**.</span></span> <span data-ttu-id="fd6d5-155">Bei der Ausgabe von **ioctl LMR wird der Code für die \_ \_ \_ lokale \_ Puffer** Steuerung nicht auf Remote Verzeichnis Handles festgelegt, und die Fehlermeldung wird **\_ nicht \_ unterstützt**.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-155">Issuing the **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code on remote directory handles will fail with the error **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd6d5-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd6d5-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd6d5-157">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="fd6d5-157">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
