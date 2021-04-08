---
description: Die getspoolfilehandle-Funktion Ruft ein Handle für die Spooldatei ab, die dem derzeit von der Anwendung übermittelten Auftrag zugeordnet ist.
ms.assetid: df6f28b3-66a6-4fb7-bdde-40cd7d934c5f
title: Getspoolfilehandle-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSpoolFileHandle
- GetSpoolFileHandleA
- GetSpoolFileHandleW
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9ac4dd4b0db9a59cc0140872ff04f89adaf8b6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050492"
---
# <a name="getspoolfilehandle-function"></a><span data-ttu-id="c803a-103">Getspoolfilehandle-Funktion</span><span class="sxs-lookup"><span data-stu-id="c803a-103">GetSpoolFileHandle function</span></span>

<span data-ttu-id="c803a-104">Die **getspoolfilehandle** -Funktion Ruft ein Handle für die Spooldatei ab, die dem derzeit von der Anwendung übermittelten Auftrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c803a-104">The **GetSpoolFileHandle** function retrieves a handle for the spool file associated with the job currently submitted by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="c803a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c803a-105">Syntax</span></span>


```C++
HANDLE GetSpoolFileHandle(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="c803a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c803a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c803a-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c803a-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c803a-108">Ein Handle für den Drucker, an den der Auftrag übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="c803a-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="c803a-109">Dies sollte das gleiche Handle sein, das verwendet wurde, um den Auftrag zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="c803a-109">This should be the same handle that was used to submit the job.</span></span> <span data-ttu-id="c803a-110">(Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.)</span><span class="sxs-lookup"><span data-stu-id="c803a-110">(Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c803a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c803a-111">Return value</span></span>

<span data-ttu-id="c803a-112">Wenn die Funktion erfolgreich ausgeführt wird, wird ein Handle für die Spooldatei zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c803a-112">If the function succeeds, it returns a handle to the spool file.</span></span>

<span data-ttu-id="c803a-113">Wenn die Funktion fehlschlägt, wird ein **ungültiger \_ handle- \_ Wert** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c803a-113">If the function fails, it returns **INVALID\_HANDLE\_VALUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c803a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c803a-114">Remarks</span></span>

<span data-ttu-id="c803a-115">Mit dem Handle für die Spooldatei kann die Anwendung mit Aufrufen von "Write [**File**](/windows/desktop/api/fileapi/nf-fileapi-writefile) " in die Spooldatei schreiben, gefolgt von " [**commitspooldata**](commitspooldata.md)".</span><span class="sxs-lookup"><span data-stu-id="c803a-115">With the handle to the spool file, your application can write to the spool file with calls to [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) followed by [**CommitSpoolData**](commitspooldata.md).</span></span>

<span data-ttu-id="c803a-116">Die Anwendung darf " [**closeprinter**](closeprinter.md) " nicht auf dem *hprinter* aufrufen, bis Sie zum letzten Mal auf die Spooldatei zugegriffen hat.</span><span class="sxs-lookup"><span data-stu-id="c803a-116">Your application must not call [**ClosePrinter**](closeprinter.md) on *hPrinter* until after it has accessed the spool file for the last time.</span></span> <span data-ttu-id="c803a-117">Dann sollte es [**closespoolfilehandle**](closespoolfilehandle.md) gefolgt von **closeprinter** aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c803a-117">Then it should call [**CloseSpoolFileHandle**](closespoolfilehandle.md) followed by **ClosePrinter**.</span></span> <span data-ttu-id="c803a-118">Wenn Sie versuchen, auf das spooldateihandle zuzugreifen, nachdem der ursprüngliche *hprinter* geschlossen wurde, tritt ein Fehler auf, auch wenn das Datei Handle selbst nicht geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="c803a-118">Attempts to access the spool file handle after the original *hPrinter* has been closed will fail even if the file handle itself has not been closed.</span></span> <span data-ttu-id="c803a-119">**Closespoolfilehandle** schlägt selbst fehl, wenn **closeprinter** zuerst aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c803a-119">**CloseSpoolFileHandle** will itself fail if **ClosePrinter** is called first.</span></span>

<span data-ttu-id="c803a-120">Diese Funktion schlägt fehl, wenn Sie aufgerufen wird, bevor der Druckauftrag das Spoolvorgang abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="c803a-120">This function will fail if it is called before the print job has finished spooling.</span></span>

## <a name="requirements"></a><span data-ttu-id="c803a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c803a-121">Requirements</span></span>



| <span data-ttu-id="c803a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c803a-122">Requirement</span></span> | <span data-ttu-id="c803a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c803a-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c803a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c803a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c803a-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c803a-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c803a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c803a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c803a-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c803a-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c803a-128">Header</span><span class="sxs-lookup"><span data-stu-id="c803a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c803a-129"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c803a-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c803a-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c803a-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="c803a-131"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c803a-131"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="c803a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c803a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c803a-133"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="c803a-133"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="c803a-134">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="c803a-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c803a-135">**Getspoolfilelenker** (Unicode) und **getspoolfilehandlea** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c803a-135">**GetSpoolFileHandleW** (Unicode) and **GetSpoolFileHandleA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="c803a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c803a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c803a-137">Drucken</span><span class="sxs-lookup"><span data-stu-id="c803a-137">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c803a-138">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="c803a-138">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="c803a-139">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="c803a-139">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="c803a-140">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="c803a-140">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="c803a-141">**Closeprinter**</span><span class="sxs-lookup"><span data-stu-id="c803a-141">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="c803a-142">**Closespoolfilehandle**</span><span class="sxs-lookup"><span data-stu-id="c803a-142">**CloseSpoolFileHandle**</span></span>](closespoolfilehandle.md)
</dt> <dt>

[<span data-ttu-id="c803a-143">**Commitspooldata**</span><span class="sxs-lookup"><span data-stu-id="c803a-143">**CommitSpoolData**</span></span>](commitspooldata.md)
</dt> </dl>

 

