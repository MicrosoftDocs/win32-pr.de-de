---
description: Die startpageprinter-Funktion benachrichtigt den Spooler, dass eine Seite auf dem angegebenen Drucker gedruckt werden soll.
ms.assetid: 8ac7c47b-b3a7-4642-bfb7-54e014139fbf
title: Startpageprinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartPagePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f8d1c5cc296fae1b166b891fc881a6abcdb6b2af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959623"
---
# <a name="startpageprinter-function"></a><span data-ttu-id="02421-103">Startpageprinter-Funktion</span><span class="sxs-lookup"><span data-stu-id="02421-103">StartPagePrinter function</span></span>

<span data-ttu-id="02421-104">Die **startpageprinter** -Funktion benachrichtigt den Spooler, dass eine Seite auf dem angegebenen Drucker gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="02421-104">The **StartPagePrinter** function notifies the spooler that a page is about to be printed on the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="02421-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="02421-105">Syntax</span></span>


```C++
BOOL StartPagePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="02421-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="02421-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02421-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02421-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02421-108">Handle für einen Drucker.</span><span class="sxs-lookup"><span data-stu-id="02421-108">Handle to a printer.</span></span> <span data-ttu-id="02421-109">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="02421-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02421-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02421-110">Return value</span></span>

<span data-ttu-id="02421-111">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="02421-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="02421-112">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="02421-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="02421-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02421-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="02421-114">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="02421-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="02421-115">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="02421-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="02421-116">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="02421-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="02421-117">Die Reihenfolge für einen Druckauftrag lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="02421-117">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="02421-118">Zum Starten eines Druckauftrags aufrufen Sie [**StartDocPrinter**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="02421-118">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="02421-119">Um jede Seite zu starten, aufrufen Sie **startpageprinter**.</span><span class="sxs-lookup"><span data-stu-id="02421-119">To begin each page, call **StartPagePrinter**.</span></span>
3.  <span data-ttu-id="02421-120">Um Daten auf eine Seite zu schreiben, müssen Sie " [**Write-Printer**](writeprinter.md)" anrufen.</span><span class="sxs-lookup"><span data-stu-id="02421-120">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="02421-121">Um jede Seite zu beenden, nennen Sie [**endpageprinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="02421-121">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="02421-122">Wiederholen Sie den Vorgang 2, 3 und 4 für beliebig viele Seiten.</span><span class="sxs-lookup"><span data-stu-id="02421-122">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="02421-123">Um den Druckauftrag zu beenden, nennen Sie [**enddocprinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="02421-123">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="02421-124">Wenn eine Seite in einer Spooldatei ungefähr 350 MB überschreitet, kann Sie nicht gedruckt werden, und es wird keine Fehlermeldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="02421-124">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="02421-125">Dies kann z. b. vorkommen, wenn große EMF-Dateien gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="02421-125">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="02421-126">Der Grenzwert für die Seitengröße hängt von vielen Faktoren ab, z. b. von der Menge des verfügbaren virtuellen Speichers, von der durch den Aufruf von Prozessen belegten Arbeitsspeicher Menge und von der Fragmentierung im Prozess Heap.</span><span class="sxs-lookup"><span data-stu-id="02421-126">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="examples"></a><span data-ttu-id="02421-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02421-127">Examples</span></span>

<span data-ttu-id="02421-128">Ein Beispielprogramm, das diese Funktion verwendet, finden [Sie unter Gewusst wie: Drucken mit der GDI-Druck-API](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="02421-128">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02421-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02421-129">Requirements</span></span>



| <span data-ttu-id="02421-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02421-130">Requirement</span></span> | <span data-ttu-id="02421-131">Wert</span><span class="sxs-lookup"><span data-stu-id="02421-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02421-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02421-132">Minimum supported client</span></span><br/> | <span data-ttu-id="02421-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02421-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="02421-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02421-134">Minimum supported server</span></span><br/> | <span data-ttu-id="02421-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02421-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="02421-136">Header</span><span class="sxs-lookup"><span data-stu-id="02421-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="02421-137"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02421-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="02421-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="02421-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="02421-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02421-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="02421-140">DLL</span><span class="sxs-lookup"><span data-stu-id="02421-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02421-141"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02421-141"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="02421-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02421-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02421-143">Drucken</span><span class="sxs-lookup"><span data-stu-id="02421-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="02421-144">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="02421-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="02421-145">**Enddocprinter**</span><span class="sxs-lookup"><span data-stu-id="02421-145">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="02421-146">**Endpageprinter**</span><span class="sxs-lookup"><span data-stu-id="02421-146">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="02421-147">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="02421-147">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="02421-148">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="02421-148">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="02421-149">**Startpageprinter**</span><span class="sxs-lookup"><span data-stu-id="02421-149">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="02421-150">**"Write Printer"**</span><span class="sxs-lookup"><span data-stu-id="02421-150">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




