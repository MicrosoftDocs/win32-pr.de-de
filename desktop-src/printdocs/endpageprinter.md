---
description: Die endpageprinter-Funktion benachrichtigt den Druck Spooler, dass sich die Anwendung am Ende einer Seite in einem Druckauftrag befindet.
ms.assetid: aceb88b9-375b-4cd2-996a-c369f590154e
title: Endpageprinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndPagePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 45e8ce005953e07f10ec621660ed38e68d50c62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131597"
---
# <a name="endpageprinter-function"></a><span data-ttu-id="4aeec-103">Endpageprinter-Funktion</span><span class="sxs-lookup"><span data-stu-id="4aeec-103">EndPagePrinter function</span></span>

<span data-ttu-id="4aeec-104">Die **endpageprinter** -Funktion benachrichtigt den Druck Spooler, dass sich die Anwendung am Ende einer Seite in einem Druckauftrag befindet.</span><span class="sxs-lookup"><span data-stu-id="4aeec-104">The **EndPagePrinter** function notifies the print spooler that the application is at the end of a page in a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aeec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4aeec-105">Syntax</span></span>


```C++
BOOL EndPagePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="4aeec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4aeec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aeec-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4aeec-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4aeec-108">Handle für den Drucker, für den die Seite geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="4aeec-108">Handle to the printer for which the page will be concluded.</span></span> <span data-ttu-id="4aeec-109">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="4aeec-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aeec-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4aeec-110">Return value</span></span>

<span data-ttu-id="4aeec-111">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="4aeec-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="4aeec-112">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="4aeec-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4aeec-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4aeec-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4aeec-114">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4aeec-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4aeec-115">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="4aeec-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4aeec-116">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="4aeec-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4aeec-117">Die Reihenfolge für einen Druckauftrag lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4aeec-117">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="4aeec-118">Zum Starten eines Druckauftrags aufrufen Sie [**StartDocPrinter**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="4aeec-118">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="4aeec-119">Um jede Seite zu starten, aufrufen Sie [**startpageprinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="4aeec-119">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="4aeec-120">Um Daten auf eine Seite zu schreiben, müssen Sie " [**Write-Printer**](writeprinter.md)" anrufen.</span><span class="sxs-lookup"><span data-stu-id="4aeec-120">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="4aeec-121">Um jede Seite zu beenden, nennen Sie **endpageprinter**.</span><span class="sxs-lookup"><span data-stu-id="4aeec-121">To end each page, call **EndPagePrinter**.</span></span>
5.  <span data-ttu-id="4aeec-122">Wiederholen Sie den Vorgang 2, 3 und 4 für beliebig viele Seiten.</span><span class="sxs-lookup"><span data-stu-id="4aeec-122">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="4aeec-123">Um den Druckauftrag zu beenden, nennen Sie [**enddocprinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="4aeec-123">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="4aeec-124">Wenn eine Seite in einer Spooldatei ungefähr 350 MB überschreitet, kann Sie nicht gedruckt werden, und es wird keine Fehlermeldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="4aeec-124">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="4aeec-125">Dies kann z. b. vorkommen, wenn große EMF-Dateien gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="4aeec-125">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="4aeec-126">Der Grenzwert für die Seitengröße hängt von vielen Faktoren ab, z. b. von der Menge des verfügbaren virtuellen Speichers, von der durch den Aufruf von Prozessen belegten Arbeitsspeicher Menge und von der Fragmentierung im Prozess Heap.</span><span class="sxs-lookup"><span data-stu-id="4aeec-126">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aeec-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4aeec-127">Requirements</span></span>



| <span data-ttu-id="4aeec-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4aeec-128">Requirement</span></span> | <span data-ttu-id="4aeec-129">Wert</span><span class="sxs-lookup"><span data-stu-id="4aeec-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aeec-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4aeec-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4aeec-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4aeec-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4aeec-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4aeec-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4aeec-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4aeec-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4aeec-134">Header</span><span class="sxs-lookup"><span data-stu-id="4aeec-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4aeec-135"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4aeec-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4aeec-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4aeec-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="4aeec-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4aeec-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4aeec-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4aeec-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4aeec-139"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4aeec-139"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="4aeec-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4aeec-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aeec-141">Drucken</span><span class="sxs-lookup"><span data-stu-id="4aeec-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4aeec-142">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="4aeec-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4aeec-143">**Enddocprinter**</span><span class="sxs-lookup"><span data-stu-id="4aeec-143">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="4aeec-144">**Endpageprinter**</span><span class="sxs-lookup"><span data-stu-id="4aeec-144">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="4aeec-145">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="4aeec-145">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="4aeec-146">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="4aeec-146">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="4aeec-147">**Startpageprinter**</span><span class="sxs-lookup"><span data-stu-id="4aeec-147">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="4aeec-148">**"Write Printer"**</span><span class="sxs-lookup"><span data-stu-id="4aeec-148">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




