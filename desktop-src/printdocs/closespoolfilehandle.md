---
description: Die closespoolfilehandle-Funktion schließt ein Handle für eine Spooldatei, die dem gerade von der Anwendung übermittelten Druckauftrag zugeordnet ist.
ms.assetid: e2c0e68f-b72e-4a97-ba18-8943bc5789c1
title: Closespoolfilehandle-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CloseSpoolFileHandle
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: c808bddde5b9b4e4a87a8608c1efb3999ce1f391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349387"
---
# <a name="closespoolfilehandle-function"></a><span data-ttu-id="fd0fd-103">Closespoolfilehandle-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd0fd-103">CloseSpoolFileHandle function</span></span>

<span data-ttu-id="fd0fd-104">Die **closespoolfilehandle** -Funktion schließt ein Handle für eine Spooldatei, die dem gerade von der Anwendung übermittelten Druckauftrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fd0fd-104">The **CloseSpoolFileHandle** function closes a handle to a spool file associated with the print job currently submitted by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd0fd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd0fd-105">Syntax</span></span>


```C++
BOOL CloseSpoolFileHandle(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile
);
```



## <a name="parameters"></a><span data-ttu-id="fd0fd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd0fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd0fd-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd0fd-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd0fd-108">Ein Handle für den Drucker, an den der Auftrag übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="fd0fd-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="fd0fd-109">Dabei sollte es sich um das gleiche Handle handeln, das zum Abrufen von *hspoolfile* mit [**getspoolfilehandle**](getspoolfilehandle.md)verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="fd0fd-109">This should be the same handle that was used to obtain *hSpoolFile* with [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd0fd-110">*hspoolfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd0fd-110">*hSpoolFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd0fd-111">Ein Handle für die Spooldatei, die geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="fd0fd-111">A handle to the spool file being closed.</span></span> <span data-ttu-id="fd0fd-112">Wenn [**commitspooldata**](commitspooldata.md) seit dem Aufruf von [**getspoolfilehandle**](getspoolfilehandle.md) nicht aufgerufen wurde, sollte dies das gleiche Handle sein, das von **getspoolfilehandle** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="fd0fd-112">If [**CommitSpoolData**](commitspooldata.md) has not been called since [**GetSpoolFileHandle**](getspoolfilehandle.md) was called, then this should be the same handle that was returned by **GetSpoolFileHandle**.</span></span> <span data-ttu-id="fd0fd-113">Andernfalls sollte es sich um das Handle handeln, das durch den letzten **Commit von commitspooldata** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="fd0fd-113">Otherwise, it should be the handle that was returned by the most recent call to **CommitSpoolData**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd0fd-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd0fd-114">Return value</span></span>

<span data-ttu-id="fd0fd-115">**True**, wenn der Vorgang erfolgreich ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="fd0fd-115">**TRUE**, if it succeeds, **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd0fd-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd0fd-116">Remarks</span></span>

<span data-ttu-id="fd0fd-117">Die Anwendung darf " [**closeprinter**](closeprinter.md) " nicht auf dem *hprinter* aufrufen, bis Sie zum letzten Mal auf die Spooldatei zugegriffen hat.</span><span class="sxs-lookup"><span data-stu-id="fd0fd-117">Your application must not call [**ClosePrinter**](closeprinter.md) on *hPrinter* until after it has accessed the spool file for the last time.</span></span> <span data-ttu-id="fd0fd-118">Dann sollte es **closespoolfilehandle** gefolgt von **closeprinter** aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fd0fd-118">Then it should call **CloseSpoolFileHandle** followed by **ClosePrinter**.</span></span> <span data-ttu-id="fd0fd-119">Wenn Sie versuchen, auf das spooldateihandle zuzugreifen, nachdem der ursprüngliche *hprinter* geschlossen wurde, tritt ein Fehler auf, auch wenn das Datei Handle selbst nicht geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="fd0fd-119">Attempts to access the spool file handle after the original *hPrinter* has been closed will fail even if the file handle itself has not been closed.</span></span> <span data-ttu-id="fd0fd-120">**Closespoolfilehandle** schlägt fehl, wenn **closeprinter** zuerst aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fd0fd-120">**CloseSpoolFileHandle** will fail if **ClosePrinter** is called first.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd0fd-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd0fd-121">Requirements</span></span>



| <span data-ttu-id="fd0fd-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd0fd-122">Requirement</span></span> | <span data-ttu-id="fd0fd-123">Wert</span><span class="sxs-lookup"><span data-stu-id="fd0fd-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd0fd-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd0fd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fd0fd-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd0fd-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="fd0fd-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd0fd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fd0fd-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd0fd-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fd0fd-128">Header</span><span class="sxs-lookup"><span data-stu-id="fd0fd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd0fd-129"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd0fd-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fd0fd-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fd0fd-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd0fd-131"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd0fd-131"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="fd0fd-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fd0fd-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd0fd-133"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="fd0fd-133"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="fd0fd-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd0fd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd0fd-135">Drucken</span><span class="sxs-lookup"><span data-stu-id="fd0fd-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fd0fd-136">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="fd0fd-136">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="fd0fd-137">**Closeprinter**</span><span class="sxs-lookup"><span data-stu-id="fd0fd-137">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="fd0fd-138">**Getspoolfilehandle**</span><span class="sxs-lookup"><span data-stu-id="fd0fd-138">**GetSpoolFileHandle**</span></span>](getspoolfilehandle.md)
</dt> </dl>

 

 




