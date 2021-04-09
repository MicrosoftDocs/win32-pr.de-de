---
description: Der FSCTL \_ SRV- \_ Anforderungs Code zum fort \_ setzen des \_ Schlüsselcodes wird verwendet, um einen nicht transparenten Datei Verweis für die Verwendung mit dem IOCTL \_ copychunk-Steuerungs Code abzurufen.
ms.assetid: a6e0d253-5beb-4de8-8c40-d004f5794d47
title: FSCTL_SRV_REQUEST_RESUME_KEY Steuerungs Codes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSCTL_SRV_REQUEST_RESUME_KEY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8f11b70f7b4bfd05cbd5f7c29323f1dca00083a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860660"
---
# <a name="fsctl_srv_request_resume_key-control-code"></a><span data-ttu-id="11d97-103">F/a-Anforderung zum Fortsetzen des \_ \_ \_ \_ Schlüsselcodes</span><span class="sxs-lookup"><span data-stu-id="11d97-103">FSCTL\_SRV\_REQUEST\_RESUME\_KEY control code</span></span>

<span data-ttu-id="11d97-104">Der **FSCTL \_ SRV \_ - \_ Anforderungs \_** Code zum Fortsetzen des Schlüsselcodes wird verwendet, um einen nicht transparenten Datei Verweis für die Verwendung mit dem [**IOCTL \_ copychunk**](ioctl-copychunk.md) -Steuerungs Code abzurufen.</span><span class="sxs-lookup"><span data-stu-id="11d97-104">The **FSCTL\_SRV\_REQUEST\_RESUME\_KEY** control code is used to retrieve an opaque file reference for use with the [**IOCTL\_COPYCHUNK**](ioctl-copychunk.md) control code.</span></span>

<span data-ttu-id="11d97-105">Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.</span><span class="sxs-lookup"><span data-stu-id="11d97-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_SRV_REQUEST_RESUME_KEY, // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="11d97-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="11d97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11d97-107">*hdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11d97-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11d97-108">Ein Handle für die Datei, für die der Quelldatei Schlüssel angefordert werden soll.</span><span class="sxs-lookup"><span data-stu-id="11d97-108">A handle to the file for which the source file key is to be requested.</span></span> <span data-ttu-id="11d97-109">Um dieses Handle zu erhalten, rufen [**Sie die Funktion**](/windows/win32/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.</span><span class="sxs-lookup"><span data-stu-id="11d97-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="11d97-110">*dwIoControlCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11d97-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11d97-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="11d97-111">The control code for the operation.</span></span> <span data-ttu-id="11d97-112">Verwenden Sie für diesen Vorgang den **\_ \_ \_ \_ Schlüssel** für die Fortsetzung des Befehls "f".</span><span class="sxs-lookup"><span data-stu-id="11d97-112">Use **FSCTL\_SRV\_REQUEST\_RESUME\_KEY** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="11d97-113">*lpinbuffer*</span><span class="sxs-lookup"><span data-stu-id="11d97-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="11d97-114">Wird bei diesem Vorgang nicht verwendet. auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="11d97-114">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="11d97-115">*nInBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11d97-115">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11d97-116">Wird bei diesem Vorgang nicht verwendet. auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="11d97-116">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="11d97-117">*lpoutbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="11d97-117">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11d97-118">Ein Zeiger auf den Ausgabepuffer, eine SRV-Anforderung zum Fortsetzen der **\_ \_ \_ Schlüssel** Struktur.</span><span class="sxs-lookup"><span data-stu-id="11d97-118">A pointer to the output buffer, a **SRV\_REQUEST\_RESUME\_KEY** structure.</span></span> <span data-ttu-id="11d97-119">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="11d97-119">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="11d97-120">*nOutBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11d97-120">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11d97-121">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="11d97-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="11d97-122">*lpbyteszurück gegeben* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="11d97-122">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11d97-123">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="11d97-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="11d97-124">Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, die [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt einen **fehlerhaften \_ \_ Puffer** zurück, und *lpbytesreturns* ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="11d97-124">If the output buffer is too small, the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="11d97-125">Wenn der *lpoverllapp* -Parameter **null** ist, kann *lpbytes-Rückgabe* Wert nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="11d97-125">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="11d97-126">Selbst wenn ein Vorgang keine Ausgabedaten zurückgibt und der *lpoutbuffer* -Parameter den Wert **null** hat, verwendet [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) *lpbytesreturn*.</span><span class="sxs-lookup"><span data-stu-id="11d97-126">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="11d97-127">Nach einem solchen Vorgang ist der Wert von *lpbytesno* bedeutungslos.</span><span class="sxs-lookup"><span data-stu-id="11d97-127">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="11d97-128">Wenn *lpoverllapp* nicht **null** ist, kann *lpbytesgab* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="11d97-128">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="11d97-129">Wenn *lpoverlgetauscht* nicht **null** ist und der Vorgang Daten zurückgibt, ist *lpbytesreturns* bedeutungslos, bis der überlappende Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="11d97-129">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="11d97-130">Um die Anzahl der zurückgegebenen Bytes abzurufen, rufen Sie die Funktion [**ge-verlappedresult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) auf.</span><span class="sxs-lookup"><span data-stu-id="11d97-130">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="11d97-131">Wenn der *hdevice* -Parameter einem e/a-Abschlussport zugeordnet ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="11d97-131">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="11d97-132">*lpoverlgetauscht* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11d97-132">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11d97-133">Ein Zeiger auf eine [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.</span><span class="sxs-lookup"><span data-stu-id="11d97-133">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="11d97-134">Wenn der *hdevice* -Parameter ohne Angabe eines **überlappenden \_ Dateiflags \_** geöffnet wurde, wird *lpoverlgetauscht* ignoriert.</span><span class="sxs-lookup"><span data-stu-id="11d97-134">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="11d97-135">Wenn *hdevice* mit dem überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, wird der Vorgang als überlappende (asynchrone) Vorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="11d97-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="11d97-136">In diesem Fall muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur verweisen, die ein Handle für ein Ereignis Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="11d97-136">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="11d97-137">Andernfalls schlägt die Funktion auf unvorhersehbare Weise fehl.</span><span class="sxs-lookup"><span data-stu-id="11d97-137">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="11d97-138">Bei überlappenden Vorgängen gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) sofort zurück, und das Ereignis Objekt wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="11d97-138">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="11d97-139">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="11d97-139">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11d97-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11d97-140">Return value</span></span>

<span data-ttu-id="11d97-141">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="11d97-141">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="11d97-142">Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="11d97-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="11d97-143">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="11d97-143">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="11d97-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11d97-144">Remarks</span></span>

<span data-ttu-id="11d97-145">Diesem Steuerungs Code ist keine Header Datei zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="11d97-145">This control code has no associated header file.</span></span> <span data-ttu-id="11d97-146">Sie müssen den Steuerungs Code und die Datenstrukturen wie folgt definieren.</span><span class="sxs-lookup"><span data-stu-id="11d97-146">You must define the control code and data structures as follows.</span></span>

``` syntax
#define FSCTL_SRV_REQUEST_RESUME_KEY CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 30, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _SRV_RESUME_KEY {
    UINT64 ResumeKey;
    UINT64 Timestamp;
    UINT64 Pid;
} SRV_RESUME_KEY, *PSRV_RESUME_KEY;

typedef struct _SRV_REQUEST_RESUME_KEY {
    SRV_RESUME_KEY Key;
    ULONG  ContextLength;
    BYTE   Context[1];
} SRV_REQUEST_RESUME_KEY, *PSRV_REQUEST_RESUME_KEY;
```

<span data-ttu-id="11d97-147">Diese Member können wie folgt beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="11d97-147">These members can be described as follows.</span></span>



| <span data-ttu-id="11d97-148">Member</span><span class="sxs-lookup"><span data-stu-id="11d97-148">Member</span></span>                                                                                                                       | <span data-ttu-id="11d97-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11d97-149">Description</span></span>                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11d97-150"><span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**Resumekey**</span><span class="sxs-lookup"><span data-stu-id="11d97-150"><span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**</span></span><br/>                 | <span data-ttu-id="11d97-151">Ein nicht transparenter Wert, der die Quelldatei für den Server identifiziert.</span><span class="sxs-lookup"><span data-stu-id="11d97-151">An opaque value that identifies the source file to the server.</span></span><br/>                                                                                                   |
| <span data-ttu-id="11d97-152"><span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="11d97-152"><span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Timestamp**</span></span><br/>                 | <span data-ttu-id="11d97-153">Ein nicht transparenter Wert, der die Uhrzeit angibt, zu der die Datei geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="11d97-153">An opaque value that identifies the time when the file was opened.</span></span><br/>                                                                                               |
| <span data-ttu-id="11d97-154"><span id="Pid"></span><span id="pid"></span><span id="PID"></span>**Lauer**</span><span class="sxs-lookup"><span data-stu-id="11d97-154"><span id="Pid"></span><span id="pid"></span><span id="PID"></span>**Pid**</span></span><br/>                                         | <span data-ttu-id="11d97-155">Ein nicht transparenter Wert, der den Prozess identifiziert, der die Datei geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="11d97-155">An opaque value that identifies the process that opened the file.</span></span><br/>                                                                                                |
| <span data-ttu-id="11d97-156"><span id="Key"></span><span id="key"></span><span id="KEY"></span>**Wichtigen**</span><span class="sxs-lookup"><span data-stu-id="11d97-156"><span id="Key"></span><span id="key"></span><span id="KEY"></span>**Key**</span></span><br/>                                         | <span data-ttu-id="11d97-157">Eine **SRV \_ Resume- \_ Schlüssel** Struktur.</span><span class="sxs-lookup"><span data-stu-id="11d97-157">A **SRV\_RESUME\_KEY** structure.</span></span> <span data-ttu-id="11d97-158">Um einen serverseitigen Kopiervorgang auszuführen, verwenden Sie diese Struktur mit dem [**IOCTL \_ copychunk**](ioctl-copychunk.md) -Steuerungs Code.</span><span class="sxs-lookup"><span data-stu-id="11d97-158">To perform a server-side copy operation, use this structure with the [**IOCTL\_COPYCHUNK**](ioctl-copychunk.md) control code.</span></span><br/> |
| <span data-ttu-id="11d97-159"><span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**Contextlength**</span><span class="sxs-lookup"><span data-stu-id="11d97-159"><span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**ContextLength**</span></span><br/> | <span data-ttu-id="11d97-160">Dieses Mitglied ist für die Verwendung durch das System reserviert. Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="11d97-160">This member is reserved for system use; do not use.</span></span><br/>                                                                                                              |
| <span data-ttu-id="11d97-161"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Kontext**</span><span class="sxs-lookup"><span data-stu-id="11d97-161"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Context**</span></span><br/>                         | <span data-ttu-id="11d97-162">Dieses Mitglied ist für die Verwendung durch das System reserviert. Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="11d97-162">This member is reserved for system use; do not use.</span></span><br/>                                                                                                              |



 

## <a name="see-also"></a><span data-ttu-id="11d97-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11d97-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11d97-164">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="11d97-164">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="11d97-165">**IOCTL- \_ copychunk**</span><span class="sxs-lookup"><span data-stu-id="11d97-165">**IOCTL\_COPYCHUNK**</span></span>](ioctl-copychunk.md)
</dt> </dl>

 

 
