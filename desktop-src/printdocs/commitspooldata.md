---
description: Die commitspooldata-Funktion benachrichtigt den Druck Spooler, dass eine angegebene Datenmenge in eine angegebene Spooldatei geschrieben wurde und zum Rendern bereit ist.
ms.assetid: cb8899e0-2fdf-4928-adff-17ef5af39f63
title: Commitspooldata-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommitSpoolData
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: fa90cb1344e7c087a601a74991598e509daed226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864760"
---
# <a name="commitspooldata-function"></a><span data-ttu-id="2e83d-103">Commitspooldata-Funktion</span><span class="sxs-lookup"><span data-stu-id="2e83d-103">CommitSpoolData function</span></span>

<span data-ttu-id="2e83d-104">Die **commitspooldata** -Funktion benachrichtigt den Druck Spooler, dass eine angegebene Datenmenge in eine angegebene Spooldatei geschrieben wurde und zum Rendern bereit ist.</span><span class="sxs-lookup"><span data-stu-id="2e83d-104">The **CommitSpoolData** function notifies the print spooler that a specified amount of data has been written to a specified spool file and is ready to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e83d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e83d-105">Syntax</span></span>


```C++
HANDLE CommitSpoolData(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile,
       DWORD  cbCommit
);
```



## <a name="parameters"></a><span data-ttu-id="2e83d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e83d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e83d-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e83d-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e83d-108">Ein Handle für den Drucker, an den der Auftrag übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="2e83d-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="2e83d-109">Dabei sollte es sich um das gleiche Handle handeln, das zum Abrufen von *hspoolfile* mit [**getspoolfilehandle**](getspoolfilehandle.md)verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="2e83d-109">This should be the same handle that was used to obtain *hSpoolFile* with [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e83d-110">*hspoolfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e83d-110">*hSpoolFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e83d-111">Ein Handle für die Spooldatei, die geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2e83d-111">A handle to the spool file being changed.</span></span> <span data-ttu-id="2e83d-112">Beim ersten Aufrufen von **commitspooldata** sollte dies das gleiche Handle sein, das von [**getspoolfilehandle**](getspoolfilehandle.md)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2e83d-112">On the first call of **CommitSpoolData**, this should be the same handle that was returned by [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span> <span data-ttu-id="2e83d-113">Nachfolgende Aufrufe von **commitspooldata** sollten das vom vorhergehenden-Aufruf zurückgegebene Handle übergeben.</span><span class="sxs-lookup"><span data-stu-id="2e83d-113">Subsequent calls to **CommitSpoolData** should pass the handle returned by the preceding call.</span></span> <span data-ttu-id="2e83d-114">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="2e83d-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2e83d-115">*cbcommit*</span><span class="sxs-lookup"><span data-stu-id="2e83d-115">*cbCommit*</span></span> 
</dt> <dd>

<span data-ttu-id="2e83d-116">Die Anzahl der Bytes, die an den Druck Spooler übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="2e83d-116">The number of bytes committed to the print spooler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e83d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e83d-117">Return value</span></span>

<span data-ttu-id="2e83d-118">Wenn die Funktion erfolgreich ausgeführt wird, wird ein Handle für die Spooldatei zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2e83d-118">If the function succeeds, it returns a handle to the spool file.</span></span>

<span data-ttu-id="2e83d-119">Wenn die Funktion fehlschlägt, wird ein ungültiger handle-Wert zurückgegeben \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2e83d-119">If the function fails, it returns INVALID\_HANDLE\_VALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e83d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e83d-120">Remarks</span></span>

<span data-ttu-id="2e83d-121">Anwendungen, die einen spoolerdruckauftrag übermitteln, können [**getspoolfilehandle**](getspoolfilehandle.md) aufrufen und dann Daten direkt in das spooldateihandle schreiben, indem Sie " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2e83d-121">Applications submitting a spooler print job can call [**GetSpoolFileHandle**](getspoolfilehandle.md) and then directly write data to the spool file handle by calling [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile).</span></span> <span data-ttu-id="2e83d-122">Um den Druck Spooler zu benachrichtigen, dass die Datei Daten enthält, die zum Rendern bereit sind, muss die Anwendung **commitspooldata** aufzurufen und die Anzahl der verfügbaren Bytes angeben.</span><span class="sxs-lookup"><span data-stu-id="2e83d-122">To notify the print spooler that the file contains data which is ready to be rendered, the application must call **CommitSpoolData** and provide the number of available bytes.</span></span>

<span data-ttu-id="2e83d-123">Wenn **commitspooldata** mehrmals aufgerufen wird, muss jeder Aufruf das spooldateihandle verwenden, das vom vorherigen Aufruf zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2e83d-123">If **CommitSpoolData** is called multiple times, each call must use the spool file handle returned by the previous call.</span></span> <span data-ttu-id="2e83d-124">Wenn keine weiteren Daten in die Spooldatei geschrieben werden, sollte [**closespoolfilehandle**](closespoolfilehandle.md) für das Datei Handle aufgerufen werden, das durch den letzten Aufruf von **commitspooldata** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2e83d-124">When no more data will be written to the spool file, [**CloseSpoolFileHandle**](closespoolfilehandle.md) should be called for the file handle returned by the last call to **CommitSpoolData**.</span></span>

<span data-ttu-id="2e83d-125">Vor dem Aufrufen von **commitspooldata** müssen Anwendungen den Dateizeiger auf die Position festlegen, die vor dem Schreiben von Daten in die Datei aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2e83d-125">Before calling **CommitSpoolData**, applications must set the file pointer to the position it had before it wrote data to the file.</span></span> <span data-ttu-id="2e83d-126">Beim Rendern der Daten in der spoolerdatei verschiebt der Druck Spooler den spooldateizeiger *cbcommit* Bytes aus dem aktuellen Wert des Dateizeigers.</span><span class="sxs-lookup"><span data-stu-id="2e83d-126">In the process of rendering the data in the spooler file, the print spooler will move the spool file pointer *cbCommit* bytes from the current value of file pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e83d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e83d-127">Requirements</span></span>



| <span data-ttu-id="2e83d-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e83d-128">Requirement</span></span> | <span data-ttu-id="2e83d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="2e83d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e83d-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e83d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2e83d-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e83d-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2e83d-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e83d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2e83d-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e83d-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2e83d-134">Header</span><span class="sxs-lookup"><span data-stu-id="2e83d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e83d-135"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e83d-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2e83d-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2e83d-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="2e83d-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e83d-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="2e83d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2e83d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e83d-139"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="2e83d-139"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="2e83d-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e83d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e83d-141">Drucken</span><span class="sxs-lookup"><span data-stu-id="2e83d-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2e83d-142">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="2e83d-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="2e83d-143">**Getspoolfilehandle**</span><span class="sxs-lookup"><span data-stu-id="2e83d-143">**GetSpoolFileHandle**</span></span>](getspoolfilehandle.md)
</dt> <dt>

[<span data-ttu-id="2e83d-144">**Closespoolfilehandle**</span><span class="sxs-lookup"><span data-stu-id="2e83d-144">**CloseSpoolFileHandle**</span></span>](closespoolfilehandle.md)
</dt> </dl>

 

