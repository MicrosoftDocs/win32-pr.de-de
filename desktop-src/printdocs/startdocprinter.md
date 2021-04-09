---
description: Die Funktion StartDocPrinter benachrichtigt den Druck Spooler, dass ein Dokument zum Drucken gespoolt werden soll.
ms.assetid: caa2bd80-4af3-4968-a5b9-d12f16cac6fc
title: StartDocPrinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartDocPrinter
- StartDocPrinterA
- StartDocPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: f8bdb0ae08c88e553dad3a91f0f1a578bed4ad39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868024"
---
# <a name="startdocprinter-function"></a><span data-ttu-id="fe3bd-103">StartDocPrinter-Funktion</span><span class="sxs-lookup"><span data-stu-id="fe3bd-103">StartDocPrinter function</span></span>

<span data-ttu-id="fe3bd-104">Die Funktion **StartDocPrinter** benachrichtigt den Druck Spooler, dass ein Dokument zum Drucken gespoolt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-104">The **StartDocPrinter** function notifies the print spooler that a document is to be spooled for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe3bd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe3bd-105">Syntax</span></span>


```C++
DWORD StartDocPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pDocInfo
);
```



## <a name="parameters"></a><span data-ttu-id="fe3bd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe3bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe3bd-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe3bd-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe3bd-108">Ein Handle für den Drucker.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-108">A handle to the printer.</span></span> <span data-ttu-id="fe3bd-109">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="fe3bd-110">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe3bd-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe3bd-111">Die Version der-Struktur, auf die *pdocinfo* verweist.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-111">The version of the structure to which *pDocInfo* points.</span></span> <span data-ttu-id="fe3bd-112">Dieser Wert muss 1 sein.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-112">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="fe3bd-113">*pdocinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe3bd-113">*pDocInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe3bd-114">Ein Zeiger auf eine [**doc \_ Info \_ 1**](doc-info-1.md) -Struktur, die das zu druckende Dokument beschreibt.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-114">A pointer to a [**DOC\_INFO\_1**](doc-info-1.md) structure that describes the document to print.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe3bd-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe3bd-115">Return value</span></span>

<span data-ttu-id="fe3bd-116">Wenn die Funktion erfolgreich ausgeführt wird, identifiziert der Rückgabewert den Druckauftrag.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-116">If the function succeeds, the return value identifies the print job.</span></span>

<span data-ttu-id="fe3bd-117">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe3bd-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe3bd-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fe3bd-119">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="fe3bd-120">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="fe3bd-121">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="fe3bd-122">Die typische Reihenfolge für einen Druckauftrag lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fe3bd-122">The typical sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="fe3bd-123">Zum Starten eines Druckauftrags aufrufen Sie **StartDocPrinter**.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-123">To begin a print job, call **StartDocPrinter**.</span></span>
2.  <span data-ttu-id="fe3bd-124">Um jede Seite zu starten, aufrufen Sie [**startpageprinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="fe3bd-124">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="fe3bd-125">Um Daten auf eine Seite zu schreiben, müssen Sie " [**Write-Printer**](writeprinter.md)" anrufen.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-125">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="fe3bd-126">Um jede Seite zu beenden, nennen Sie [**endpageprinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="fe3bd-126">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="fe3bd-127">Wiederholen Sie den Vorgang 2, 3 und 4 für beliebig viele Seiten.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-127">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="fe3bd-128">Um den Druckauftrag zu beenden, nennen Sie [**enddocprinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="fe3bd-128">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="fe3bd-129">Beachten Sie, dass das Aufrufen von [**startpageprinter**](startpageprinter.md) und [**endpageprinter**](endpageprinter.md) möglicherweise nicht erforderlich ist, z. b. wenn der Print-Datentyp die Seiten Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-129">Note that calling [**StartPagePrinter**](startpageprinter.md) and [**EndPagePrinter**](endpageprinter.md) may not be necessary, such as if the print data type includes the page information.</span></span>

<span data-ttu-id="fe3bd-130">Wenn eine Seite in einer Spooldatei ungefähr 350 MB überschreitet, kann Sie nicht gedruckt werden, und es wird keine Fehlermeldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-130">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="fe3bd-131">Dies kann z. b. vorkommen, wenn große EMF-Dateien gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-131">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="fe3bd-132">Der Grenzwert für die Seitengröße hängt von vielen Faktoren ab, z. b. von der Menge des verfügbaren virtuellen Speichers, von der durch den Aufruf von Prozessen belegten Arbeitsspeicher Menge und von der Fragmentierung im Prozess Heap.</span><span class="sxs-lookup"><span data-stu-id="fe3bd-132">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="examples"></a><span data-ttu-id="fe3bd-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe3bd-133">Examples</span></span>

<span data-ttu-id="fe3bd-134">Ein Beispielprogramm, das diese Funktion verwendet, finden [Sie unter Gewusst wie: Drucken mit der GDI-Druck-API](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="fe3bd-134">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe3bd-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe3bd-135">Requirements</span></span>



| <span data-ttu-id="fe3bd-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe3bd-136">Requirement</span></span> | <span data-ttu-id="fe3bd-137">Wert</span><span class="sxs-lookup"><span data-stu-id="fe3bd-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe3bd-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe3bd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fe3bd-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe3bd-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fe3bd-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe3bd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fe3bd-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe3bd-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fe3bd-142">Header</span><span class="sxs-lookup"><span data-stu-id="fe3bd-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe3bd-143"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe3bd-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fe3bd-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fe3bd-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="fe3bd-145"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe3bd-145"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="fe3bd-146">DLL</span><span class="sxs-lookup"><span data-stu-id="fe3bd-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe3bd-147"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="fe3bd-147"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="fe3bd-148">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="fe3bd-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fe3bd-149">**Startdocprinterw** (Unicode) und **startdocprintera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fe3bd-149">**StartDocPrinterW** (Unicode) and **StartDocPrinterA** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="fe3bd-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe3bd-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe3bd-151">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="fe3bd-151">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="fe3bd-152">**DOC \_ Info \_ 1**</span><span class="sxs-lookup"><span data-stu-id="fe3bd-152">**DOC\_INFO\_1**</span></span>](doc-info-1.md)
</dt> <dt>

[<span data-ttu-id="fe3bd-153">**DOC \_ Info \_ 2**</span><span class="sxs-lookup"><span data-stu-id="fe3bd-153">**DOC\_INFO\_2**</span></span>](doc-info-2.md)
</dt> <dt>

[<span data-ttu-id="fe3bd-154">**Enddocprinter**</span><span class="sxs-lookup"><span data-stu-id="fe3bd-154">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="fe3bd-155">**Endpageprinter**</span><span class="sxs-lookup"><span data-stu-id="fe3bd-155">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="fe3bd-156">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="fe3bd-156">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="fe3bd-157">Drucken</span><span class="sxs-lookup"><span data-stu-id="fe3bd-157">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fe3bd-158">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="fe3bd-158">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="fe3bd-159">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="fe3bd-159">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="fe3bd-160">**Startpageprinter**</span><span class="sxs-lookup"><span data-stu-id="fe3bd-160">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="fe3bd-161">**"Write Printer"**</span><span class="sxs-lookup"><span data-stu-id="fe3bd-161">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




