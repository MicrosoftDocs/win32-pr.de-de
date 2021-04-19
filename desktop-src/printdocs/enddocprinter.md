---
description: Die enddocprinter-Funktion beendet einen Druckauftrag für den angegebenen Drucker.
ms.assetid: 13c713e8-cc24-4191-8b1e-967b9e20e541
title: Enddocprinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndDocPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 8d3e2bc110e5ee9412bb1edb89779f896edb015a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363513"
---
# <a name="enddocprinter-function"></a><span data-ttu-id="cf68b-103">Enddocprinter-Funktion</span><span class="sxs-lookup"><span data-stu-id="cf68b-103">EndDocPrinter function</span></span>

<span data-ttu-id="cf68b-104">Die **enddocprinter** -Funktion beendet einen Druckauftrag für den angegebenen Drucker.</span><span class="sxs-lookup"><span data-stu-id="cf68b-104">The **EndDocPrinter** function ends a print job for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf68b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf68b-105">Syntax</span></span>


```C++
BOOL EndDocPrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="cf68b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf68b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf68b-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf68b-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf68b-108">Handle für einen Drucker, für den der Druckauftrag beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf68b-108">Handle to a printer for which the print job should be ended.</span></span> <span data-ttu-id="cf68b-109">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="cf68b-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf68b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf68b-110">Return value</span></span>

<span data-ttu-id="cf68b-111">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="cf68b-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="cf68b-112">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="cf68b-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf68b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf68b-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cf68b-114">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cf68b-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="cf68b-115">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="cf68b-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="cf68b-116">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="cf68b-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="cf68b-117">Die **enddocprinter** -Funktion gibt einen Fehler zurück, wenn der Druckauftrag nicht durch Aufrufen der [**StartDocPrinter**](startdocprinter.md) -Funktion gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="cf68b-117">The **EndDocPrinter** function returns an error if the print job was not started by calling the [**StartDocPrinter**](startdocprinter.md) function.</span></span>

<span data-ttu-id="cf68b-118">Die Reihenfolge für einen Druckauftrag lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cf68b-118">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="cf68b-119">Zum Starten eines Druckauftrags aufrufen Sie [**StartDocPrinter**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="cf68b-119">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="cf68b-120">Um jede Seite zu starten, aufrufen Sie [**startpageprinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="cf68b-120">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="cf68b-121">Um Daten auf eine Seite zu schreiben, müssen Sie " [**Write-Printer**](writeprinter.md)" anrufen.</span><span class="sxs-lookup"><span data-stu-id="cf68b-121">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="cf68b-122">Um jede Seite zu beenden, nennen Sie [**endpageprinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="cf68b-122">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="cf68b-123">Wiederholen Sie den Vorgang 2, 3 und 4 für beliebig viele Seiten.</span><span class="sxs-lookup"><span data-stu-id="cf68b-123">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="cf68b-124">Um den Druckauftrag zu beenden, nennen Sie **enddocprinter**.</span><span class="sxs-lookup"><span data-stu-id="cf68b-124">To end the print job, call **EndDocPrinter**.</span></span>

<span data-ttu-id="cf68b-125">Wenn eine Seite in einer Spooldatei ungefähr 350 MB überschreitet, kann Sie nicht gedruckt werden, und es wird keine Fehlermeldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="cf68b-125">When a page in a spooled file exceeds approximately 350 MB, it may fail to print and not send an error message.</span></span> <span data-ttu-id="cf68b-126">Dies kann z. b. vorkommen, wenn große EMF-Dateien gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="cf68b-126">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="cf68b-127">Der Grenzwert für die Seitengröße hängt von vielen Faktoren ab, z. b. von der Menge des verfügbaren virtuellen Speichers, von der durch den Aufruf von Prozessen belegten Arbeitsspeicher Menge und von der Fragmentierung im Prozess Heap.</span><span class="sxs-lookup"><span data-stu-id="cf68b-127">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf68b-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf68b-128">Requirements</span></span>



| <span data-ttu-id="cf68b-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf68b-129">Requirement</span></span> | <span data-ttu-id="cf68b-130">Wert</span><span class="sxs-lookup"><span data-stu-id="cf68b-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf68b-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf68b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cf68b-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf68b-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cf68b-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf68b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cf68b-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf68b-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cf68b-135">Header</span><span class="sxs-lookup"><span data-stu-id="cf68b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf68b-136"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf68b-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="cf68b-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cf68b-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="cf68b-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf68b-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="cf68b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="cf68b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf68b-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf68b-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="cf68b-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf68b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf68b-142">Drucken</span><span class="sxs-lookup"><span data-stu-id="cf68b-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="cf68b-143">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="cf68b-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="cf68b-144">**Enddocprinter**</span><span class="sxs-lookup"><span data-stu-id="cf68b-144">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="cf68b-145">**Endpageprinter**</span><span class="sxs-lookup"><span data-stu-id="cf68b-145">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="cf68b-146">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="cf68b-146">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="cf68b-147">**Startpageprinter**</span><span class="sxs-lookup"><span data-stu-id="cf68b-147">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="cf68b-148">**"Write Printer"**</span><span class="sxs-lookup"><span data-stu-id="cf68b-148">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




