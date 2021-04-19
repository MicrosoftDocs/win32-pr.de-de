---
description: Der IOCTL \_ copychunk-Steuerungs Code initiiert eine serverseitige Kopie eines Datenbereichs, auch als Block bezeichnet.
ms.assetid: 36f68840-bd5c-4cfc-a8ad-0cfbbdc5a2a9
title: IOCTL_COPYCHUNK Steuerungs Codes
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
ms.openlocfilehash: c425fc53563e6dfc16d2040fb575f47f0f8fdf35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344804"
---
# <a name="ioctl_copychunk-control-code"></a><span data-ttu-id="88d1a-103">IOCTL \_ copychunk-Steuerungs Code</span><span class="sxs-lookup"><span data-stu-id="88d1a-103">IOCTL\_COPYCHUNK control code</span></span>

<span data-ttu-id="88d1a-104">Der **IOCTL \_ copychunk** -Steuerungs Code initiiert eine serverseitige Kopie eines Datenbereichs, auch als Block bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="88d1a-104">The **IOCTL\_COPYCHUNK** control code initiates a server-side copy of a range of data, also called a chunk.</span></span>

<span data-ttu-id="88d1a-105">Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.</span><span class="sxs-lookup"><span data-stu-id="88d1a-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_COPYCHUNK,              // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="88d1a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="88d1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88d1a-107">*hdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88d1a-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88d1a-108">Ein Handle für die Datei, die das Ziel des serverseitigen Kopiervorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="88d1a-108">A handle to the file that is the target of the server-side copy operation.</span></span> <span data-ttu-id="88d1a-109">Um dieses Handle zu erhalten, rufen [**Sie die Funktion**](/windows/win32/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.</span><span class="sxs-lookup"><span data-stu-id="88d1a-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="88d1a-110">*dwIoControlCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88d1a-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88d1a-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="88d1a-111">The control code for the operation.</span></span> <span data-ttu-id="88d1a-112">Verwenden Sie **IOCTL \_ copychunk** für diesen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="88d1a-112">Use **IOCTL\_COPYCHUNK** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="88d1a-113">*lpinbuffer*</span><span class="sxs-lookup"><span data-stu-id="88d1a-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="88d1a-114">Ein Zeiger auf den Eingabepuffer, eine **SRV \_ copychunk- \_ Kopier** Struktur.</span><span class="sxs-lookup"><span data-stu-id="88d1a-114">A pointer to the input buffer, a **SRV\_COPYCHUNK\_COPY** structure.</span></span> <span data-ttu-id="88d1a-115">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="88d1a-115">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="88d1a-116">*nInBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88d1a-116">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88d1a-117">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="88d1a-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="88d1a-118">*lpoutbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="88d1a-118">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88d1a-119">Ein Zeiger auf den Ausgabepuffer, eine **SRV- \_ copychunk- \_ Antwort** Struktur.</span><span class="sxs-lookup"><span data-stu-id="88d1a-119">A pointer to the output buffer, a **SRV\_COPYCHUNK\_RESPONSE** structure.</span></span> <span data-ttu-id="88d1a-120">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="88d1a-120">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="88d1a-121">*nOutBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88d1a-121">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88d1a-122">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="88d1a-122">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="88d1a-123">*lpbyteszurück gegeben* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="88d1a-123">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88d1a-124">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="88d1a-124">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="88d1a-125">Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, die [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt einen **fehlerhaften \_ \_ Puffer** zurück, und *lpbytesreturns* ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="88d1a-125">If the output buffer is too small, the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="88d1a-126">Wenn der *lpoverllapp* -Parameter **null** ist, kann *lpbytes-Rückgabe* Wert nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="88d1a-126">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="88d1a-127">Selbst wenn ein Vorgang keine Ausgabedaten zurückgibt und der *lpoutbuffer* -Parameter den Wert **null** hat, verwendet [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) *lpbytesreturn*.</span><span class="sxs-lookup"><span data-stu-id="88d1a-127">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="88d1a-128">Nach einem solchen Vorgang ist der Wert von *lpbytesno* bedeutungslos.</span><span class="sxs-lookup"><span data-stu-id="88d1a-128">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="88d1a-129">Wenn *lpoverllapp* nicht **null** ist, kann *lpbytesgab* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="88d1a-129">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="88d1a-130">Wenn *lpoverlgetauscht* nicht **null** ist und der Vorgang Daten zurückgibt, ist *lpbytesreturns* bedeutungslos, bis der überlappende Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="88d1a-130">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="88d1a-131">Um die Anzahl der zurückgegebenen Bytes abzurufen, rufen Sie die Funktion [**ge-verlappedresult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) auf.</span><span class="sxs-lookup"><span data-stu-id="88d1a-131">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="88d1a-132">Wenn der *hdevice* -Parameter einem e/a-Abschlussport zugeordnet ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="88d1a-132">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="88d1a-133">*lpoverlgetauscht* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88d1a-133">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88d1a-134">Ein Zeiger auf eine [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.</span><span class="sxs-lookup"><span data-stu-id="88d1a-134">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="88d1a-135">Wenn der *hdevice* -Parameter ohne Angabe eines **überlappenden \_ Dateiflags \_** geöffnet wurde, wird *lpoverlgetauscht* ignoriert.</span><span class="sxs-lookup"><span data-stu-id="88d1a-135">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="88d1a-136">Wenn *hdevice* mit dem überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, wird der Vorgang als überlappende (asynchrone) Vorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88d1a-136">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="88d1a-137">In diesem Fall muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur verweisen, die ein Handle für ein Ereignis Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="88d1a-137">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="88d1a-138">Andernfalls schlägt die Funktion auf unvorhersehbare Weise fehl.</span><span class="sxs-lookup"><span data-stu-id="88d1a-138">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="88d1a-139">Bei überlappenden Vorgängen gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) sofort zurück, und das Ereignis Objekt wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="88d1a-139">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="88d1a-140">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="88d1a-140">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88d1a-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88d1a-141">Return value</span></span>

<span data-ttu-id="88d1a-142">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="88d1a-142">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="88d1a-143">Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="88d1a-143">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="88d1a-144">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="88d1a-144">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="88d1a-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88d1a-145">Remarks</span></span>

<span data-ttu-id="88d1a-146">Diesem Steuerungs Code ist keine Header Datei zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="88d1a-146">This control code has no associated header file.</span></span> <span data-ttu-id="88d1a-147">Sie müssen den Steuerungs Code und die Datenstrukturen wie folgt definieren.</span><span class="sxs-lookup"><span data-stu-id="88d1a-147">You must define the control code and data structures as follows.</span></span>

``` syntax
#define IOCTL_COPYCHUNK CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 262, METHOD_BUFFERED,  FILE_READ_ACCESS)

typedef struct _SRV_COPYCHUNK {
    LARGE_INTEGER SourceOffset;
    LARGE_INTEGER DestinationOffset;
    ULONG  Length;
} SRV_COPYCHUNK, *PSRV_COPYCHUNK;

typedef struct _SRV_COPYCHUNK_COPY {
    SRV_RESUME_KEY SourceFile;
    ULONG          ChunkCount;
    ULONG          Reserved;
    SRV_COPYCHUNK  Chunk[1];    // Array
} SRV_COPYCHUNK_COPY, *PSRV_COPYCHUNK_COPY;

typedef struct _SRV_COPYCHUNK_RESPONSE {
    ULONG          ChunksWritten;
    ULONG          ChunkBytesWritten;
    ULONG          TotalBytesWritten;
} SRV_COPYCHUNK_RESPONSE, *PSRV_COPYCHUNK_RESPONSE;
```

<span data-ttu-id="88d1a-148">Diese Member können wie folgt beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="88d1a-148">These members can be described as follows.</span></span>



| <span data-ttu-id="88d1a-149">Member</span><span class="sxs-lookup"><span data-stu-id="88d1a-149">Member</span></span>                                                                                                                                       | <span data-ttu-id="88d1a-150">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88d1a-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88d1a-151"><span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**</span><span class="sxs-lookup"><span data-stu-id="88d1a-151"><span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**</span></span><br/>                     | <span data-ttu-id="88d1a-152">Der Offset in Bytes vom Anfang der Quelldatei bis zum zu kopierenden Block.</span><span class="sxs-lookup"><span data-stu-id="88d1a-152">The offset, in bytes, from the beginning of the source file to the chunk to be copied.</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="88d1a-153"><span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**</span><span class="sxs-lookup"><span data-stu-id="88d1a-153"><span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**</span></span><br/> | <span data-ttu-id="88d1a-154">Der Offset in Bytes vom Anfang der Zieldatei bis zum Speicherort, an den der Block kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="88d1a-154">The offset, in bytes, from the beginning of the target file to the location where the chunk is to be copied.</span></span><br/>                                                                                                                                                                                                                                               |
| <span data-ttu-id="88d1a-155"><span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Füll**</span><span class="sxs-lookup"><span data-stu-id="88d1a-155"><span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Length**</span></span><br/>                                             | <span data-ttu-id="88d1a-156">Die Anzahl der Daten Bytes im Block, die kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="88d1a-156">The number of bytes of data in the chunk to be copied.</span></span> <span data-ttu-id="88d1a-157">Muss größer als 0 (null) und kleiner oder gleich 1 MB sein.</span><span class="sxs-lookup"><span data-stu-id="88d1a-157">Must be greater than zero and less than or equal to 1 MB.</span></span> <span data-ttu-id="88d1a-158">**Länge** \* " **Chunkcount** " muss kleiner oder gleich 16 MB sein.</span><span class="sxs-lookup"><span data-stu-id="88d1a-158">**Length** \* **ChunkCount** must be less than or equal to 16 MB.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="88d1a-159"><span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**</span><span class="sxs-lookup"><span data-stu-id="88d1a-159"><span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**</span></span><br/>                             | <span data-ttu-id="88d1a-160">Ein Schlüssel, der die Quelldatei mit den zu kopierenden Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="88d1a-160">A key that represents the source file with the data to be copied.</span></span> <span data-ttu-id="88d1a-161">Dieser Schlüssel wird über den Schlüssel zum Fortsetzen der [**fisctl- \_ SRV- \_ Anforderung \_ \_**](fsctl-srv-request-resume-key.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="88d1a-161">This key is obtained through [**FSCTL\_SRV\_REQUEST\_RESUME\_KEY**](fsctl-srv-request-resume-key.md).</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="88d1a-162"><span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**Anzahl von Blöcken**</span><span class="sxs-lookup"><span data-stu-id="88d1a-162"><span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**</span></span><br/>                             | <span data-ttu-id="88d1a-163">Die Anzahl der Blöcke, die kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="88d1a-163">The number of chunks to be copied.</span></span> <span data-ttu-id="88d1a-164">Muss größer als 0 (null) und kleiner oder gleich 256 sein.</span><span class="sxs-lookup"><span data-stu-id="88d1a-164">Must be greater than zero and less than or equal to 256.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="88d1a-165"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Bleiben**</span><span class="sxs-lookup"><span data-stu-id="88d1a-165"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved**</span></span><br/>                                     | <span data-ttu-id="88d1a-166">Dieses Mitglied ist für die Verwendung durch das System reserviert. Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="88d1a-166">This member is reserved for system use; do not use.</span></span><br/>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="88d1a-167"><span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Block**</span><span class="sxs-lookup"><span data-stu-id="88d1a-167"><span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Chunk**</span></span><br/>                                                 | <span data-ttu-id="88d1a-168">Ein Array von Block **count** - **SRV- \_ copychunk** -Strukturen, eines für jeden zu kopierenden Block.</span><span class="sxs-lookup"><span data-stu-id="88d1a-168">An array of **ChunkCount** **SRV\_COPYCHUNK** structures, one for each chunk to be copied.</span></span> <span data-ttu-id="88d1a-169">Die Länge dieses Arrays in Bytes muss " **chunkcount** \* sizeof (**SRV \_ copyblock**)" lauten.</span><span class="sxs-lookup"><span data-stu-id="88d1a-169">The length, in bytes, of this array must be **ChunkCount** \* sizeof(**SRV\_COPYCHUNK**).</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="88d1a-170"><span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**Chunksgeschrieben**</span><span class="sxs-lookup"><span data-stu-id="88d1a-170"><span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**</span></span><br/>                 | <span data-ttu-id="88d1a-171">Wenn bei dem Vorgang ein **Fehler aufgrund eines \_ ungültigen \_ Parameters aufgetreten** ist, gibt dieser Wert die maximale Anzahl von Blöcken an, die der Server in einer einzelnen Anforderung akzeptiert, d. h. 256.</span><span class="sxs-lookup"><span data-stu-id="88d1a-171">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of chunks the server will accept in a single request, which is 256.</span></span> <span data-ttu-id="88d1a-172">Andernfalls gibt dieser Wert die Anzahl von Blöcken an, die erfolgreich geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="88d1a-172">Otherwise, this value indicates the number of chunks that were successfully written.</span></span><br/>                                                                                               |
| <span data-ttu-id="88d1a-173"><span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**Chunkbyteswritten**</span><span class="sxs-lookup"><span data-stu-id="88d1a-173"><span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**</span></span><br/> | <span data-ttu-id="88d1a-174">Wenn bei dem Vorgang ein **Fehler aufgrund eines \_ ungültigen \_ Parameters aufgetreten** ist, gibt dieser Wert die maximale Anzahl von Bytes an, die der Server in einem einzelnen Block schreiben darf (1 MB).</span><span class="sxs-lookup"><span data-stu-id="88d1a-174">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of bytes the server will allow to be written in a single chunk, which is 1 MB.</span></span> <span data-ttu-id="88d1a-175">Andernfalls gibt dieser Wert die Anzahl von Bytes an, die erfolgreich in das letzte Segment geschrieben wurden, das nicht erfolgreich verarbeitet wurde (bei einem partiellen Schreibvorgang).</span><span class="sxs-lookup"><span data-stu-id="88d1a-175">Otherwise, this value indicates the number of bytes that were successfully written in the last chunk that was not successfully processed (if a partial write occurred).</span></span><br/> |
| <span data-ttu-id="88d1a-176"><span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**Total byteswritten**</span><span class="sxs-lookup"><span data-stu-id="88d1a-176"><span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**</span></span><br/> | <span data-ttu-id="88d1a-177">Wenn bei dem Vorgang ein **Fehler aufgrund eines \_ ungültigen \_ Parameters aufgetreten** ist, gibt dieser Wert die maximale Anzahl von Bytes an, die der Server in einer einzelnen Anforderung kopiert, d. h. 16 MB.</span><span class="sxs-lookup"><span data-stu-id="88d1a-177">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of bytes the server will copy in a single request, which is 16 MB.</span></span> <span data-ttu-id="88d1a-178">Andernfalls gibt dieser Wert die Anzahl der Bytes an, die erfolgreich geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="88d1a-178">Otherwise, this value indicates the number of bytes that were successfully written.</span></span><br/>                                                                                                 |



 

## <a name="see-also"></a><span data-ttu-id="88d1a-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88d1a-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88d1a-180">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="88d1a-180">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="88d1a-181">**Fortsetzen des Schlüssels der ssctl \_ SRV- \_ Anforderung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="88d1a-181">**FSCTL\_SRV\_REQUEST\_RESUME\_KEY**</span></span>](fsctl-srv-request-resume-key.md)
</dt> </dl>

 

 
