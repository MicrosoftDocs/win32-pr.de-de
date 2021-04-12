---
description: Der "da \_ Get NFS-Attribute"- \_ \_ Steuerungs Code fragt zusätzliche Informationen über eine NFS-Freigabe ab.
ms.assetid: BC9E0E19-7D78-4AE7-A3E6-9FD9212B2B83
title: DA_GET_NFS_ATTRIBUTES Steuerungs Codes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DA_GET_NFS_ATTRIBUTES
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4427dd48190bd12f7837c4841a98e15f7ddaff5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523371"
---
# <a name="da_get_nfs_attributes-control-code"></a><span data-ttu-id="94002-103">Steuerelement Code für da \_ Get NFS- \_ \_ Attribute</span><span class="sxs-lookup"><span data-stu-id="94002-103">DA\_GET\_NFS\_ATTRIBUTES control code</span></span>

<span data-ttu-id="94002-104">Der " **da \_ Get NFS- \_ \_ Attribute** "-Steuerungs Code fragt zusätzliche Informationen über eine NFS-Freigabe ab.</span><span class="sxs-lookup"><span data-stu-id="94002-104">The **DA\_GET\_NFS\_ATTRIBUTES** control code queries additional information about an NFS share.</span></span>

<span data-ttu-id="94002-105">Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.</span><span class="sxs-lookup"><span data-stu-id="94002-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,               // handle to device
                    (DWORD)        DA_GET_NFS_ATTRIBUTES, // dwIoControlCode
                                   NULL,                  // lpInBuffer
                                   0,                     // nInBufferSize
                    (LPDWORD)      lpOutBuffer,           // output buffer
                    (DWORD)        nOutBufferSize,        // size of output buffer
                    (LPDWORD)      lpBytesReturned,       // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );        // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="94002-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="94002-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94002-107">*hdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94002-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94002-108">Ein Handle für eine Datei auf der NFS-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="94002-108">A handle to a file on the NFS share.</span></span> <span data-ttu-id="94002-109">Um dieses Handle zu erhalten, rufen [**Sie die Funktion**](/windows/win32/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.</span><span class="sxs-lookup"><span data-stu-id="94002-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="94002-110">*dwIoControlCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94002-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94002-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="94002-111">The control code for the operation.</span></span> <span data-ttu-id="94002-112">Verwenden Sie für diesen Vorgang " **da \_ get \_ NFS \_** "-Attribute.</span><span class="sxs-lookup"><span data-stu-id="94002-112">Use **DA\_GET\_NFS\_ATTRIBUTES** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="94002-113">*lpinbuffer*</span><span class="sxs-lookup"><span data-stu-id="94002-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="94002-114">Wird bei diesem Vorgang nicht verwendet. auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="94002-114">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="94002-115">*nInBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94002-115">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94002-116">Wird bei diesem Vorgang nicht verwendet. auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="94002-116">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="94002-117">*lpoutbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="94002-117">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94002-118">Ein Zeiger auf den Ausgabepuffer, der eine **NFS- \_ Datei \_ Attribute** -Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="94002-118">A pointer to the output buffer, which contains an **NFS\_FILE\_ATTRIBUTES** structure.</span></span> <span data-ttu-id="94002-119">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="94002-119">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="94002-120">*nOutBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94002-120">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94002-121">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="94002-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="94002-122">*lpbyteszurück gegeben* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="94002-122">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94002-123">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="94002-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="94002-124">Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen **fehlerhaften \_ \_ Puffer** zurück, und *lpbytesreturns* ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="94002-124">If the output buffer is too small, the call fails, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="94002-125">Wenn *lpoverllapp* den **Wert NULL** hat, kann *lpbytes-Rückgabe* Wert nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="94002-125">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="94002-126">Selbst wenn ein Vorgang keine Ausgabedaten zurückgibt und *lpoutbuffer* den Wert **null** hat, verwendet [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) *lpbytesreturn*.</span><span class="sxs-lookup"><span data-stu-id="94002-126">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="94002-127">Nach einem solchen Vorgang ist der Wert von *lpbytesno* bedeutungslos.</span><span class="sxs-lookup"><span data-stu-id="94002-127">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="94002-128">Wenn *lpoverllapp* nicht **null** ist, kann *lpbytesgab* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="94002-128">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="94002-129">Wenn dieser Parameter nicht **null** ist und der Vorgang Daten zurückgibt, ist *lpbytesreturns* bedeutungslos, bis der überlappende Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="94002-129">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="94002-130">Um die Anzahl der zurückgegebenen Bytes abzurufen, rufen Sie [**gezu verlappedresult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult)auf.</span><span class="sxs-lookup"><span data-stu-id="94002-130">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="94002-131">Wenn der *hdevice* -Parameter einem e/a-Abschlussport zugeordnet ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="94002-131">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="94002-132">*lpoverlgetauscht* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94002-132">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94002-133">Ein Zeiger auf eine [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.</span><span class="sxs-lookup"><span data-stu-id="94002-133">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="94002-134">Wenn *hdevice* ohne Angabe eines überlappenden **\_ Dateiflags \_** geöffnet wurde, wird *lpoverlgetauscht* ignoriert.</span><span class="sxs-lookup"><span data-stu-id="94002-134">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="94002-135">Wenn *hdevice* mit dem überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, wird der Vorgang als überlappende (asynchrone) Vorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94002-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="94002-136">In diesem Fall muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur verweisen, die ein Handle für ein Ereignis Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="94002-136">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="94002-137">Andernfalls schlägt die Funktion auf unvorhersehbare Weise fehl.</span><span class="sxs-lookup"><span data-stu-id="94002-137">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="94002-138">Bei überlappenden Vorgängen gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) sofort zurück, und das Ereignis Objekt wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="94002-138">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="94002-139">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="94002-139">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94002-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94002-140">Return value</span></span>

<span data-ttu-id="94002-141">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="94002-141">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="94002-142">Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="94002-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="94002-143">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="94002-143">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="94002-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94002-144">Remarks</span></span>

<span data-ttu-id="94002-145">Diesem Steuerungs Code ist keine Header Datei zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="94002-145">This control code has no associated header file.</span></span> <span data-ttu-id="94002-146">Sie müssen den Steuerungs Code und die Datenstrukturen wie folgt definieren.</span><span class="sxs-lookup"><span data-stu-id="94002-146">You must define the control code and data structures as follows.</span></span>

``` syntax
#define DEVICE_DA_RDR 0x80000  
 
#define DA_GET_NFS_ATTRIBUTES CTL_CODE(DEVICE_DA_RDR, 0x804, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _NFS_SPEC_DATA {  
    ULONG               SpecData1;
    ULONG               SpecData2;
} NFS_SPEC_DATA, *PNFS_SPEC_DATA;

typedef struct _NFS_TIME {
    ULONG        Seconds;
    ULONG        nSeconds;
} NFS_TIME, *PNFS_TIME;

#define NFS_TYPE_REG         1
#define NFS_TYPE_DIR         2
#define NFS_TYPE_BLK         3
#define NFS_TYPE_CHR         4
#define NFS_TYPE_LNK         5
#define NFS_TYPE_SOCK        6
#define NFS_TYPE_FIFO        7

typedef struct _NFS_FILE_ATTRIBUTES {  
    ULONG               FileType;  
    ULONG               Mode;  
    ULONG               NLink;  
    ULONG               Uid;  
    ULONG               Gid;  
    ULONGLONG           Size;  
    ULONGLONG           Used;
    NFS_SPEC_DATA       Rdev;
    ULONGLONG           Fsid;  
    ULONGLONG           FileId;  
    NFS_TIME            AccessTime;  
    NFS_TIME            ModifyTime;  
    NFS_TIME            ChangeTime;  
} NFS_FILE_ATTRIBUTES, *PNFS_FILE_ATTRIBUTES;

typedef struct _DA_FILE_ATTRIBUTES {  
    NFS_FILE_ATTRIBUTES FileAttributes;  
    ULONG               Version;  
} DA_FILE_ATTRIBUTES, *PDA_FILE_ATTRIBUTES;
```

<span data-ttu-id="94002-147">Die Strukturmember können wie folgt beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="94002-147">The structure members can be described as follows.</span></span>

<dl> <dt>

<span data-ttu-id="94002-148"><span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**</span><span class="sxs-lookup"><span data-stu-id="94002-148"><span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**</span></span>
</dt> <dd>

<span data-ttu-id="94002-149">Ein nicht transparenter Wert, der für spezielle Dateitypen wie z. b. Block-Special-, Character-Special-und FIFO-Dateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="94002-149">An opaque value that is used for special file types such as block-special, character-special and FIFO files.</span></span>

</dd> <dt>

<span data-ttu-id="94002-150"><span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**</span><span class="sxs-lookup"><span data-stu-id="94002-150"><span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**</span></span>
</dt> <dd>

<span data-ttu-id="94002-151">Ein nicht transparenter Wert, der für spezielle Dateitypen wie z. b. Block-Special-, Character-Special-und FIFO-Dateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="94002-151">An opaque value that is used for special file types such as block-special, character-special and FIFO files.</span></span>

</dd> <dt>

<span data-ttu-id="94002-152"><span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Vorsprung**</span><span class="sxs-lookup"><span data-stu-id="94002-152"><span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Seconds**</span></span>
</dt> <dd>

<span data-ttu-id="94002-153">Ein 64-Bit-Wert, der die Sekunden seit dem 1. Januar 1970 (UTC) darstellt.</span><span class="sxs-lookup"><span data-stu-id="94002-153">A 64-bit value representing the seconds since January 1, 1970 (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="94002-154"><span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSekunden**</span><span class="sxs-lookup"><span data-stu-id="94002-154"><span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**</span></span>
</dt> <dd>

<span data-ttu-id="94002-155">Die Anzahl der Nanosekunden, die dem **Sekunden** -Element hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="94002-155">The number of nanoseconds to be added to the **Seconds** member.</span></span>

</dd> <dt>

<span data-ttu-id="94002-156"><span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**</span><span class="sxs-lookup"><span data-stu-id="94002-156"><span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**</span></span>
</dt> <dd>

<span data-ttu-id="94002-157">Der NFS-Dateityp der Freigabe.</span><span class="sxs-lookup"><span data-stu-id="94002-157">The NFS file type of the share.</span></span>



| <span data-ttu-id="94002-158">NFS-Dateityp</span><span class="sxs-lookup"><span data-stu-id="94002-158">NFS File Type</span></span>                                                                              | <span data-ttu-id="94002-159">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94002-159">Description</span></span>                          |
|--------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="94002-160"><span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>NFS- \_ Typ- \_ reg</span><span class="sxs-lookup"><span data-stu-id="94002-160"><span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>NFS\_TYPE\_REG</span></span><br/>    | <span data-ttu-id="94002-161">Eine reguläre Datei.</span><span class="sxs-lookup"><span data-stu-id="94002-161">A regular file.</span></span><br/>           |
| <span data-ttu-id="94002-162"><span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>NFS- \_ typverzeichnis \_</span><span class="sxs-lookup"><span data-stu-id="94002-162"><span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>NFS\_TYPE\_DIR</span></span><br/>    | <span data-ttu-id="94002-163">Ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="94002-163">A directory.</span></span><br/>              |
| <span data-ttu-id="94002-164"><span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>NFS- \_ Typ \_ BLK</span><span class="sxs-lookup"><span data-stu-id="94002-164"><span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>NFS\_TYPE\_BLK</span></span><br/>    | <span data-ttu-id="94002-165">Eine Block spezifische Datei.</span><span class="sxs-lookup"><span data-stu-id="94002-165">A block-special file.</span></span><br/>     |
| <span data-ttu-id="94002-166"><span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>NFS- \_ Typ \_ Chr</span><span class="sxs-lookup"><span data-stu-id="94002-166"><span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>NFS\_TYPE\_CHR</span></span><br/>    | <span data-ttu-id="94002-167">Eine Zeichen spezifische Datei.</span><span class="sxs-lookup"><span data-stu-id="94002-167">A character-special file.</span></span><br/> |
| <span data-ttu-id="94002-168"><span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>NFS- \_ Typ \_ lnk</span><span class="sxs-lookup"><span data-stu-id="94002-168"><span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>NFS\_TYPE\_LNK</span></span><br/>    | <span data-ttu-id="94002-169">Eine symbolische Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="94002-169">A symbolic link.</span></span><br/>          |
| <span data-ttu-id="94002-170"><span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>NFS- \_ Typ- \_ Sock</span><span class="sxs-lookup"><span data-stu-id="94002-170"><span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>NFS\_TYPE\_SOCK</span></span><br/> | <span data-ttu-id="94002-171">Ein Windows-Socket.</span><span class="sxs-lookup"><span data-stu-id="94002-171">A Windows socket.</span></span><br/>         |
| <span data-ttu-id="94002-172"><span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>NFS- \_ Typ \_ FIFO</span><span class="sxs-lookup"><span data-stu-id="94002-172"><span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>NFS\_TYPE\_FIFO</span></span><br/> | <span data-ttu-id="94002-173">Eine FIFO-Datei.</span><span class="sxs-lookup"><span data-stu-id="94002-173">A FIFO file.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="94002-174"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Spar**</span><span class="sxs-lookup"><span data-stu-id="94002-174"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode**</span></span>
</dt> <dd>

<span data-ttu-id="94002-175">Der Dateimodus.</span><span class="sxs-lookup"><span data-stu-id="94002-175">The file mode.</span></span>

</dd> <dt>

<span data-ttu-id="94002-176"><span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**Nlink**</span><span class="sxs-lookup"><span data-stu-id="94002-176"><span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**</span></span>
</dt> <dd>

<span data-ttu-id="94002-177">Die Anzahl der Links zur Freigabe.</span><span class="sxs-lookup"><span data-stu-id="94002-177">The number of links to the share.</span></span>

</dd> <dt>

<span data-ttu-id="94002-178"><span id="Uid"></span><span id="uid"></span><span id="UID"></span>**UID**</span><span class="sxs-lookup"><span data-stu-id="94002-178"><span id="Uid"></span><span id="uid"></span><span id="UID"></span>**Uid**</span></span>
</dt> <dd>

<span data-ttu-id="94002-179">Die UNIX-Benutzer-ID (UID).</span><span class="sxs-lookup"><span data-stu-id="94002-179">The UNIX user identifier (UID).</span></span>

</dd> <dt>

<span data-ttu-id="94002-180"><span id="Gid"></span><span id="gid"></span><span id="GID"></span>**Ü**</span><span class="sxs-lookup"><span data-stu-id="94002-180"><span id="Gid"></span><span id="gid"></span><span id="GID"></span>**Gid**</span></span>
</dt> <dd>

<span data-ttu-id="94002-181">Der UNIX-Gruppen Bezeichner (GID).</span><span class="sxs-lookup"><span data-stu-id="94002-181">The UNIX group identifier (GID).</span></span>

</dd> <dt>

<span data-ttu-id="94002-182"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Größe**</span><span class="sxs-lookup"><span data-stu-id="94002-182"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Size**</span></span>
</dt> <dd>

<span data-ttu-id="94002-183">Die Dateigröße in Bytes.</span><span class="sxs-lookup"><span data-stu-id="94002-183">The file size, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="94002-184"><span id="Used"></span><span id="used"></span><span id="USED"></span>**Daran**</span><span class="sxs-lookup"><span data-stu-id="94002-184"><span id="Used"></span><span id="used"></span><span id="USED"></span>**Used**</span></span>
</dt> <dd>

<span data-ttu-id="94002-185">Die verwendete Dateigröße in Bytes.</span><span class="sxs-lookup"><span data-stu-id="94002-185">The file size used, in bytes.</span></span> <span data-ttu-id="94002-186">Dies entspricht der Dateigröße.</span><span class="sxs-lookup"><span data-stu-id="94002-186">This is the same as the file size.</span></span>

</dd> <dt>

<span data-ttu-id="94002-187"><span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**</span><span class="sxs-lookup"><span data-stu-id="94002-187"><span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**</span></span>
</dt> <dd>

<span data-ttu-id="94002-188">Der Geräte Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="94002-188">The device identifier.</span></span>

</dd> <dt>

<span data-ttu-id="94002-189"><span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**-Sid**</span><span class="sxs-lookup"><span data-stu-id="94002-189"><span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**</span></span>
</dt> <dd>

<span data-ttu-id="94002-190">Der Bezeichner des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="94002-190">The file system identifier.</span></span>

</dd> <dt>

<span data-ttu-id="94002-191"><span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**FileID**</span><span class="sxs-lookup"><span data-stu-id="94002-191"><span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**FileId**</span></span>
</dt> <dd>

<span data-ttu-id="94002-192">Der Dateibezeichner.</span><span class="sxs-lookup"><span data-stu-id="94002-192">The file identifier.</span></span>

</dd> <dt>

<span data-ttu-id="94002-193"><span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**ACCESSTIME**</span><span class="sxs-lookup"><span data-stu-id="94002-193"><span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**AccessTime**</span></span>
</dt> <dd>

<span data-ttu-id="94002-194">Der Zeitpunkt des letzten Zugriffs.</span><span class="sxs-lookup"><span data-stu-id="94002-194">The last access time.</span></span>

</dd> <dt>

<span data-ttu-id="94002-195"><span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**Modifytime**</span><span class="sxs-lookup"><span data-stu-id="94002-195"><span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**ModifyTime**</span></span>
</dt> <dd>

<span data-ttu-id="94002-196">Der Zeitpunkt der letzten Änderung.</span><span class="sxs-lookup"><span data-stu-id="94002-196">The last modification time.</span></span>

</dd> <dt>

<span data-ttu-id="94002-197"><span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**Changetime**</span><span class="sxs-lookup"><span data-stu-id="94002-197"><span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**</span></span>
</dt> <dd>

<span data-ttu-id="94002-198">Der Zeitpunkt der letzten Änderung.</span><span class="sxs-lookup"><span data-stu-id="94002-198">The last change time.</span></span>

</dd> <dt>

<span data-ttu-id="94002-199"><span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**File Attributes**</span><span class="sxs-lookup"><span data-stu-id="94002-199"><span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="94002-200">Eine **NFS- \_ Datei \_ Attribute** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="94002-200">An **NFS\_FILE\_ATTRIBUTES** structure.</span></span>

> [!Note]  
> <span data-ttu-id="94002-201">Ausführlichere Beschreibungen der Member dieser Struktur finden Sie in der **fattr3** -Struktur in der Version 3 des NFS-Protokolls (wie in [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)definiert).</span><span class="sxs-lookup"><span data-stu-id="94002-201">For more detailed descriptions of the members of this structure, see the **fattr3** structure in the NFS Version 3 Protocol Specification (as defined in [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)).</span></span>

 

</dd> <dt>

<span data-ttu-id="94002-202"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**</span><span class="sxs-lookup"><span data-stu-id="94002-202"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**</span></span>
</dt> <dd>

<span data-ttu-id="94002-203">Gibt an, ob die Verbindung, auf der das Handle für die NFS-Freigabe erstellt wurde, über NFS Version 2 oder das NFS-Protokoll (Version 3) erfolgt.</span><span class="sxs-lookup"><span data-stu-id="94002-203">Specifies whether the connection on which the handle to the NFS share was created is over NFS Version 2 or NFS Version 3 protocol.</span></span>



| <span data-ttu-id="94002-204">Wert</span><span class="sxs-lookup"><span data-stu-id="94002-204">Value</span></span>                            | <span data-ttu-id="94002-205">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94002-205">Description</span></span>              |
|----------------------------------|--------------------------|
| <span data-ttu-id="94002-206"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="94002-206"><span id="2"></span>2</span></span><br/> | <span data-ttu-id="94002-207">NFS Version 2</span><span class="sxs-lookup"><span data-stu-id="94002-207">NFS Version 2</span></span><br/> |
| <span data-ttu-id="94002-208"><span id="3"></span>€</span><span class="sxs-lookup"><span data-stu-id="94002-208"><span id="3"></span>3</span></span><br/> | <span data-ttu-id="94002-209">NFS Version 3</span><span class="sxs-lookup"><span data-stu-id="94002-209">NFS Version 3</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94002-210">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94002-210">Requirements</span></span>



| <span data-ttu-id="94002-211">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94002-211">Requirement</span></span> | <span data-ttu-id="94002-212">Wert</span><span class="sxs-lookup"><span data-stu-id="94002-212">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="94002-213">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94002-213">Minimum supported client</span></span><br/> | <span data-ttu-id="94002-214">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="94002-214">None supported</span></span><br/>         |
| <span data-ttu-id="94002-215">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94002-215">Minimum supported server</span></span><br/> | <span data-ttu-id="94002-216">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94002-216">Windows Server 2008</span></span><br/>    |
| <span data-ttu-id="94002-217">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="94002-217">End of client support</span></span><br/>    | <span data-ttu-id="94002-218">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="94002-218">None supported</span></span><br/>         |
| <span data-ttu-id="94002-219">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="94002-219">End of server support</span></span><br/>    | <span data-ttu-id="94002-220">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="94002-220">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94002-221">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94002-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94002-222">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="94002-222">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
