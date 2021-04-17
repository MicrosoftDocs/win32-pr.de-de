---
description: Liest Daten aus einer geöffneten Datei.
ms.assetid: 7EA2FE38-20DA-43E1-A764-66A81725D1EA
title: Ntreadfile-Funktion (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtReadFile
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: be1a73c6451012dfd97d7d4c55c23f0842cf1551
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523176"
---
# <a name="ntreadfile-function"></a><span data-ttu-id="7af73-103">Ntreadfile-Funktion</span><span class="sxs-lookup"><span data-stu-id="7af73-103">NtReadFile function</span></span>

<span data-ttu-id="7af73-104">Liest Daten aus einer geöffneten Datei.</span><span class="sxs-lookup"><span data-stu-id="7af73-104">Reads data from an open file.</span></span>

<span data-ttu-id="7af73-105">Diese Funktion ist der Benutzermodus, der der im Windows-Treiberkit (WDK) dokumentierten [**zwlesefile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) -Funktion entspricht.</span><span class="sxs-lookup"><span data-stu-id="7af73-105">This function is the user-mode equivalent to the [**ZwReadFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) function documented in the Windows Driver Kit (WDK).</span></span>

## <a name="syntax"></a><span data-ttu-id="7af73-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7af73-106">Syntax</span></span>


```C++
NTSTATUS NtReadFile(
  _In_     HANDLE           FileHandle,
  _In_opt_ HANDLE           Event,
  _In_opt_ PIO_APC_ROUTINE  ApcRoutine,
  _In_opt_ PVOID            ApcContext,
  _Out_    PIO_STATUS_BLOCK IoStatusBlock,
  _Out_    PVOID            Buffer,
  _In_     ULONG            Length,
  _In_opt_ PLARGE_INTEGER   ByteOffset,
  _In_opt_ PULONG           Key
);
```



## <a name="parameters"></a><span data-ttu-id="7af73-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7af73-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7af73-108">*FILEHANDLE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7af73-108">*FileHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7af73-109">Handle für das Datei Objekt.</span><span class="sxs-lookup"><span data-stu-id="7af73-109">Handle to the file object.</span></span> <span data-ttu-id="7af73-110">Dieses Handle wird durch einen erfolgreichen Aufrufen von [**ntkreatefile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) oder [**ntopenfile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile)erstellt.</span><span class="sxs-lookup"><span data-stu-id="7af73-110">This handle is created by a successful call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) or [**NtOpenFile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile).</span></span>

</dd> <dt>

<span data-ttu-id="7af73-111">*Ereignis* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="7af73-111">*Event* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7af73-112">Ein Handle für ein Ereignis Objekt, das auf den signalisierten Zustand festgelegt werden soll, nachdem der Lesevorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="7af73-112">Optionally, a handle to an event object to set to the signaled state after the read operation completes.</span></span> <span data-ttu-id="7af73-113">Für Geräte-und zwischen Treiber sollte dieser Parameter auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7af73-113">Device and intermediate drivers should set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7af73-114">*Apcroutine* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="7af73-114">*ApcRoutine* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7af73-115">Dieser Parameter ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="7af73-115">This parameter is reserved.</span></span> <span data-ttu-id="7af73-116">Für Geräte-und zwischen Treiber sollte dieser Zeiger auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7af73-116">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7af73-117">*Apccontext* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="7af73-117">*ApcContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7af73-118">Dieser Parameter ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="7af73-118">This parameter is reserved.</span></span> <span data-ttu-id="7af73-119">Für Geräte-und zwischen Treiber sollte dieser Zeiger auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7af73-119">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7af73-120">*Iostatus Block* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7af73-120">*IoStatusBlock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7af73-121">Zeiger auf eine [**IO- \_ Status \_ Block**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) Struktur, die den endgültigen Abschluss Status und Informationen zum angeforderten Lesevorgang empfängt.</span><span class="sxs-lookup"><span data-stu-id="7af73-121">Pointer to an [**IO\_STATUS\_BLOCK**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) structure that receives the final completion status and information about the requested read operation.</span></span> <span data-ttu-id="7af73-122">Der **informationsmember** erhält die Anzahl der tatsächlich aus der Datei gelesenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="7af73-122">The **Information** member receives the number of bytes actually read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="7af73-123">*Puffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7af73-123">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7af73-124">Zeiger auf einen vom Aufrufer zugewiesenen Puffer, der die aus der Datei gelesenen Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="7af73-124">Pointer to a caller-allocated buffer that receives the data read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="7af73-125">*Länge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7af73-125">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7af73-126">Die Größe des Puffers in Byte, auf den durch den *Puffer* gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7af73-126">The size, in bytes, of the buffer pointed to by *Buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="7af73-127">*Byteoffset* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="7af73-127">*ByteOffset* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7af73-128">Ein Zeiger auf eine Variable, die den Start Byte Offset in der Datei angibt, in der der Lesevorgang beginnt.</span><span class="sxs-lookup"><span data-stu-id="7af73-128">Pointer to a variable that specifies the starting byte offset in the file where the read operation will begin.</span></span> <span data-ttu-id="7af73-129">Wenn versucht wird, über das Dateiende hinaus zu lesen, gibt **ntreadfile** einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="7af73-129">If an attempt is made to read beyond the end of the file, **NtReadFile** returns an error.</span></span>

<span data-ttu-id="7af73-130">Wenn für den Aufrufen von [**ntkreatefile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) *eine der Dateien für die* synchrone e/a-Benachrichtigung oder eine synchrone e/a-Datei für e/a-Vorgänge festgelegt \_ \_ \_ \_ \_ \_ ist, behält der e/a-Manager die aktuelle Datei</span><span class="sxs-lookup"><span data-stu-id="7af73-130">If the call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) set either of the *CreateOptions* flags FILE\_SYNCHRONOUS\_IO\_ALERT or FILE\_SYNCHRONOUS\_IO\_NONALERT, the I/O Manager maintains the current file position.</span></span> <span data-ttu-id="7af73-131">Wenn dies der Fall ist, kann der Aufrufer von **ntreadfile** angeben, dass der aktuelle Offset der Dateiposition anstelle eines expliziten *Byteoffset* -Werts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7af73-131">If so, the caller of **NtReadFile** can specify that the current file position offset be used instead of an explicit *ByteOffset* value.</span></span> <span data-ttu-id="7af73-132">Diese Angabe kann mithilfe einer der folgenden Methoden erfolgen:</span><span class="sxs-lookup"><span data-stu-id="7af73-132">This specification can be made by using one of the following methods:</span></span>

-   <span data-ttu-id="7af73-133">Geben Sie einen Zeiger auf einen **großen \_ ganzzahligen** Wert an, bei dem das **highpart** -Element auf-1 festgelegt ist und das **LowPart** -Element, das auf die System definierte Wert Datei festgelegt ist, \_ \_ Datei \_ Zeiger \_</span><span class="sxs-lookup"><span data-stu-id="7af73-133">Specify a pointer to a **LARGE\_INTEGER** value with the **HighPart** member set to -1 and the **LowPart** member set to the system-defined value FILE\_USE\_FILE\_POINTER\_POSITION.</span></span>

-   <span data-ttu-id="7af73-134">Übergeben Sie einen **null** -Zeiger für *Byteoffset*.</span><span class="sxs-lookup"><span data-stu-id="7af73-134">Pass a **NULL** pointer for *ByteOffset*.</span></span>

<span data-ttu-id="7af73-135">**Ntreadfile** aktualisiert die aktuelle Dateiposition durch Hinzufügen der Anzahl der gelesenen Bytes, wenn der Lesevorgang abgeschlossen wird, wenn die aktuelle Dateiposition verwendet wird, die vom e/a-Manager verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="7af73-135">**NtReadFile** updates the current file position by adding the number of bytes read when it completes the read operation, if it is using the current file position maintained by the I/O Manager.</span></span>

<span data-ttu-id="7af73-136">Auch wenn der e/a-Manager die aktuelle Dateiposition beibehält, kann der Aufrufer diese Position zurücksetzen, indem er einen expliziten *Byteoffset* -Wert an **ntreadfile** übergibt.</span><span class="sxs-lookup"><span data-stu-id="7af73-136">Even when the I/O Manager is maintaining the current file position, the caller can reset this position by passing an explicit *ByteOffset* value to **NtReadFile**.</span></span> <span data-ttu-id="7af73-137">Dadurch wird die aktuelle Dateiposition automatisch in diesen *Byteoffset* -Wert geändert, der Lesevorgang ausgeführt und die Position entsprechend der Anzahl der tatsächlich gelesenen Bytes aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7af73-137">Doing this automatically changes the current file position to that *ByteOffset* value, performs the read operation, and then updates the position according to the number of bytes actually read.</span></span> <span data-ttu-id="7af73-138">Diese Technik bietet dem Aufrufer den atomarischen Seek-und Lesedienst.</span><span class="sxs-lookup"><span data-stu-id="7af73-138">This technique gives the caller atomic seek-and-read service.</span></span>

</dd> <dt>

<span data-ttu-id="7af73-139">*Schlüssel* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="7af73-139">*Key* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7af73-140">Für Geräte-und zwischen Treiber sollte dieser Zeiger auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7af73-140">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7af73-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7af73-141">Return value</span></span>

<span data-ttu-id="7af73-142">**Ntreadfile** gibt entweder \_ den Status Erfolg oder den entsprechenden NTSTATUS-Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="7af73-142">**NtReadFile** returns either STATUS\_SUCCESS or the appropriate NTSTATUS error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7af73-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7af73-143">Remarks</span></span>

<span data-ttu-id="7af73-144">Aufrufer von **ntreadfile** müssen bereits [**ntkreatefile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) mit der Datei \_ Read \_ Data oder dem \_ Wert für einen generischen Lesevorgang im *desiredAccess* -Parameter aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="7af73-144">Callers of **NtReadFile** must have already called [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) with the FILE\_READ\_DATA or GENERIC\_READ value set in the *DesiredAccess* parameter.</span></span>

<span data-ttu-id="7af73-145">Wenn der vorherige Befehl von [**ntkreatefile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) das Flag " \_ keine \_ zwischen \_ Pufferung für Datei" im Parameter " *kreateoptions* " auf " **ntkreatefile**" festgelegt hat, müssen die Parameter " *length* " und " *Byteoffset* " in " **ntreadfile** " Vielfachen der Sektorgröße sein</span><span class="sxs-lookup"><span data-stu-id="7af73-145">If the preceding call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) set the FILE\_NO\_INTERMEDIATE\_BUFFERING flag in the *CreateOptions* parameter to **NtCreateFile**, the *Length* and *ByteOffset* parameters to **NtReadFile** must be multiples of the sector size.</span></span> <span data-ttu-id="7af73-146">Weitere Informationen finden Sie unter **ntkreatefile**.</span><span class="sxs-lookup"><span data-stu-id="7af73-146">For more information, see **NtCreateFile**.</span></span>

<span data-ttu-id="7af73-147">**Ntreadfile** beginnt mit dem Lesen aus dem angegebenen *Byteoffset* oder der aktuellen Dateiposition in den angegebenen *Puffer*.</span><span class="sxs-lookup"><span data-stu-id="7af73-147">**NtReadFile** begins reading from the given *ByteOffset* or the current file position into the given *Buffer*.</span></span> <span data-ttu-id="7af73-148">Der Lesevorgang wird unter einer der folgenden Bedingungen beendet:</span><span class="sxs-lookup"><span data-stu-id="7af73-148">It terminates the read operation under one of the following conditions:</span></span>

-   <span data-ttu-id="7af73-149">Der Puffer ist voll, weil die vom *length* -Parameter angegebene Anzahl von Bytes gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="7af73-149">The buffer is full because the number of bytes specified by the *Length* parameter has been read.</span></span> <span data-ttu-id="7af73-150">Daher können keine weiteren Daten ohne Überlauf in den Puffer eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7af73-150">Therefore, no more data can be placed into the buffer without an overflow.</span></span>

-   <span data-ttu-id="7af73-151">Das Dateiende wird während des Lesevorgangs erreicht, sodass keine weiteren Daten in der Datei vorhanden sind, die in den Puffer übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="7af73-151">The end of file is reached during the read operation, so there is no more data in the file to be transferred into the buffer.</span></span>

<span data-ttu-id="7af73-152">Wenn der Aufrufer die Datei mit dem in *desiredAccess* festgelegten synchronisierungsflag geöffnet hat, kann der aufrufende Thread mit dem Abschluss des Lesevorgangs synchronisiert werden, indem auf das Datei Handle, *FILEHANDLE*, gewartet wird.</span><span class="sxs-lookup"><span data-stu-id="7af73-152">If the caller opened the file with the SYNCHRONIZE flag set in *DesiredAccess*, the calling thread can synchronize to the completion of the read operation by waiting on the file handle, *FileHandle*.</span></span> <span data-ttu-id="7af73-153">Das Handle wird jedes Mal signalisiert, wenn ein e/a-Vorgang, der für das Handle ausgegeben wurde, abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="7af73-153">The handle is signaled each time that an I/O operation that was issued on the handle completes.</span></span> <span data-ttu-id="7af73-154">Der Aufrufer darf jedoch nicht auf ein Handle warten, das für den synchronen Dateizugriff geöffnet wurde (Datei synchrone e/a-Warnung oder synchrone e/a- \_ \_ \_ \_ \_ \_ Warnung).</span><span class="sxs-lookup"><span data-stu-id="7af73-154">However, the caller must not wait on a handle that was opened for synchronous file access (FILE\_SYNCHRONOUS\_IO\_NONALERT or FILE\_SYNCHRONOUS\_IO\_ALERT).</span></span> <span data-ttu-id="7af73-155">In diesem Fall wartet **ntreadfile** im Auftrag des Aufrufers und gibt erst dann zurück, wenn der Lesevorgang beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7af73-155">In this case, **NtReadFile** waits on behalf of the caller and does not return until the read operation is complete.</span></span> <span data-ttu-id="7af73-156">Der Aufrufer kann auf das Datei Handle nur dann sicher warten, wenn alle drei der folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="7af73-156">The caller can safely wait on the file handle only if all three of the following conditions are met:</span></span>

-   <span data-ttu-id="7af73-157">Das Handle wurde für den asynchronen Zugriff geöffnet (d. h., es wurde kein synchrones e/a- \_ Flag " \_ \_ *xxx* " angegeben)</span><span class="sxs-lookup"><span data-stu-id="7af73-157">The handle was opened for asynchronous access (that is, neither FILE\_SYNCHRONOUS\_IO\_*XXX* flag was specified).</span></span>

-   <span data-ttu-id="7af73-158">Das Handle wird nur für einen e/a-Vorgang gleichzeitig verwendet.</span><span class="sxs-lookup"><span data-stu-id="7af73-158">The handle is being used for only one I/O operation at a time.</span></span>

-   <span data-ttu-id="7af73-159">**Ntreadfile** hat Status \_ Ausstehend zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7af73-159">**NtReadFile** returned STATUS\_PENDING.</span></span>

<span data-ttu-id="7af73-160">Ein Treiber sollte **ntreadfile** im Kontext des System Prozesses abrufen, wenn eine der folgenden Bedingungen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7af73-160">A driver should call **NtReadFile** in the context of the system process if any of the following conditions exist:</span></span>

-   <span data-ttu-id="7af73-161">Der Treiber hat das Datei Handle erstellt, das an **ntreadfile** weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="7af73-161">The driver created the file handle that it passes to **NtReadFile**.</span></span>

-   <span data-ttu-id="7af73-162">**Ntreadfile** benachrichtigt den Treiber über den e/a-Abschluss mithilfe eines Ereignisses, das der Treiber erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="7af73-162">**NtReadFile** will notify the driver of I/O completion by means of an event that the driver created.</span></span>

-   <span data-ttu-id="7af73-163">**Ntreadfile** benachrichtigt den Treiber über den e/a-Abschluss mithilfe einer APC-Rückruf Routine, die der Treiber an **ntreadfile** übergibt.</span><span class="sxs-lookup"><span data-stu-id="7af73-163">**NtReadFile** will notify the driver of I/O completion by means of an APC callback routine that the driver passes to **NtReadFile**.</span></span>

<span data-ttu-id="7af73-164">Datei-und Ereignis Handles sind nur im Prozess Kontext gültig, in dem die Handles erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7af73-164">File and event handles are valid only in the process context where the handles are created.</span></span> <span data-ttu-id="7af73-165">Um Sicherheitslücken zu vermeiden, sollte der Treiber daher jedes beliebige Datei-oder Ereignis handle, das er im Kontext des System Prozesses an **ntreadfile** übergibt, und nicht den Kontext des Prozesses, in dem sich der Treiber befindet, erstellen.</span><span class="sxs-lookup"><span data-stu-id="7af73-165">Therefore, to avoid security holes, the driver should create any file or event handle that it passes to **NtReadFile** in the context of the system process rather than the context of the process that the driver is in.</span></span>

<span data-ttu-id="7af73-166">Ebenso sollte **ntreadfile** im Kontext des System Prozesses aufgerufen werden, wenn der Treiber über einen e/a-Abschluss mithilfe eines APC benachrichtigt wird, da APCs immer im Kontext des Threads ausgelöst werden, der die e/a-Anforderung ausgibt.</span><span class="sxs-lookup"><span data-stu-id="7af73-166">Likewise, **NtReadFile** should be called in the context of the system process if it notifies the driver of I/O completion by means of an APC, because APCs are always fired in the context of the thread that issues the I/O request.</span></span> <span data-ttu-id="7af73-167">Wenn der Treiber **ntreadfile** im Kontext eines anderen Prozesses als dem System aufruft, kann das APC unbegrenzt verzögert oder überhaupt nicht ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="7af73-167">If the driver calls **NtReadFile** in the context of a process other than the system one, the APC could be delayed indefinitely, or it might not fire at all.</span></span>

<span data-ttu-id="7af73-168">Weitere Informationen zum Arbeiten mit Dateien finden Sie unter [Verwenden von Dateien in einem Treiber](/windows-hardware/drivers/kernel/using-files-in-a-driver).</span><span class="sxs-lookup"><span data-stu-id="7af73-168">For more information about working with files, see [Using Files in a Driver](/windows-hardware/drivers/kernel/using-files-in-a-driver).</span></span>

<span data-ttu-id="7af73-169">Aufrufer von **ntreadfile** müssen auf der Ebene "iriql = passiv" \_ und [mit aktivierten speziellen Kernel-APCs](/windows-hardware/drivers/kernel/disabling-apcs)ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7af73-169">Callers of **NtReadFile** must be running at IRQL = PASSIVE\_LEVEL and [with special kernel APCs enabled](/windows-hardware/drivers/kernel/disabling-apcs).</span></span>

## <a name="requirements"></a><span data-ttu-id="7af73-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7af73-170">Requirements</span></span>



| <span data-ttu-id="7af73-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7af73-171">Requirement</span></span> | <span data-ttu-id="7af73-172">Wert</span><span class="sxs-lookup"><span data-stu-id="7af73-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7af73-173">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7af73-173">Minimum supported client</span></span><br/> | <span data-ttu-id="7af73-174">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7af73-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="7af73-175">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7af73-175">Minimum supported server</span></span><br/> | <span data-ttu-id="7af73-176">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7af73-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="7af73-177">Zielplattform</span><span class="sxs-lookup"><span data-stu-id="7af73-177">Target platform</span></span><br/>          | <dl> <span data-ttu-id="7af73-178"><dt>[Universell](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="7af73-178"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="7af73-179">Header</span><span class="sxs-lookup"><span data-stu-id="7af73-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="7af73-180"><dt>WDM. h (Include WDM. h, ntddk. h oder ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7af73-180"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="7af73-181">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7af73-181">Library</span></span><br/>                  | <dl> <span data-ttu-id="7af73-182"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7af73-182"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7af73-183">DLL</span><span class="sxs-lookup"><span data-stu-id="7af73-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7af73-184"><dt>Ntdll.dll (Benutzermodus)</dt></span><span class="sxs-lookup"><span data-stu-id="7af73-184"><dt>Ntdll.dll (user mode)</dt></span></span> </dl>                                        |



## <a name="see-also"></a><span data-ttu-id="7af73-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7af73-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7af73-186">**Keinitializeevent**</span><span class="sxs-lookup"><span data-stu-id="7af73-186">**KeInitializeEvent**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-keinitializeevent)
</dt> <dt>

[<span data-ttu-id="7af73-187">**NtCreateFile**</span><span class="sxs-lookup"><span data-stu-id="7af73-187">**NtCreateFile**</span></span>](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile)
</dt> <dt>

[<span data-ttu-id="7af73-188">**Ntqueryinformationfile**</span><span class="sxs-lookup"><span data-stu-id="7af73-188">**NtQueryInformationFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntqueryinformationfile)
</dt> <dt>

[<span data-ttu-id="7af73-189">**Ntsetinformationfile**</span><span class="sxs-lookup"><span data-stu-id="7af73-189">**NtSetInformationFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntsetinformationfile)
</dt> <dt>

[<span data-ttu-id="7af73-190">**Ntwrite-Datei**</span><span class="sxs-lookup"><span data-stu-id="7af73-190">**NtWriteFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntwritefile)
</dt> </dl>

 

 
