---
description: Die deleteprinter-Funktion löscht das angegebene Drucker Objekt.
ms.assetid: 04d9c073-b795-4307-ba89-d4984bc5b354
title: Deleteprinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 16d82a263b09c87f5c9b9725db48dd6634404ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349834"
---
# <a name="deleteprinter-function"></a><span data-ttu-id="5705c-103">Deleteprinter-Funktion</span><span class="sxs-lookup"><span data-stu-id="5705c-103">DeletePrinter function</span></span>

<span data-ttu-id="5705c-104">Die **deleteprinter** -Funktion löscht das angegebene Drucker Objekt.</span><span class="sxs-lookup"><span data-stu-id="5705c-104">The **DeletePrinter** function deletes the specified printer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5705c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5705c-105">Syntax</span></span>


```C++
BOOL DeletePrinter(
  _Inout_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="5705c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5705c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5705c-107">*hprinter* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5705c-107">*hPrinter* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5705c-108">Handle für ein Drucker Objekt, das gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="5705c-108">Handle to a printer object that will be deleted.</span></span> <span data-ttu-id="5705c-109">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="5705c-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5705c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5705c-110">Return value</span></span>

<span data-ttu-id="5705c-111">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="5705c-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="5705c-112">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="5705c-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5705c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5705c-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5705c-114">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5705c-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="5705c-115">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="5705c-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="5705c-116">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="5705c-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="5705c-117">Wenn noch Druckaufträge für den angegebenen Drucker verarbeitet werden, markiert **deleteprinter** den Drucker für das ausstehende löschen und löscht ihn dann, wenn alle Druckaufträge gedruckt wurden.</span><span class="sxs-lookup"><span data-stu-id="5705c-117">If there are print jobs remaining to be processed for the specified printer, **DeletePrinter** marks the printer for pending deletion, and then deletes it when all the print jobs have been printed.</span></span> <span data-ttu-id="5705c-118">Einem Drucker, der zum ausstehenden Löschen markiert ist, können keine Druckaufträge hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5705c-118">No print jobs can be added to a printer that is marked for pending deletion.</span></span>

<span data-ttu-id="5705c-119">Ein Drucker, der zum Löschen ausstehend markiert ist, kann nicht gespeichert werden, seine Druckaufträge können jedoch gehalten, fortgesetzt und neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="5705c-119">A printer marked for pending deletion cannot be held, but its print jobs can be held, resumed, and restarted.</span></span> <span data-ttu-id="5705c-120">Wenn der Drucker angehalten wird und Aufträge für den Drucker vorhanden sind, schlägt **deleteprinter** mit Fehler \_ Zugriff \_ verweigert fehl.</span><span class="sxs-lookup"><span data-stu-id="5705c-120">If the printer is held and there are jobs for the printer, **DeletePrinter** fails with ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="5705c-121">Beachten Sie, dass **deleteprinter** das an ihn übertragende Handle nicht schließt.</span><span class="sxs-lookup"><span data-stu-id="5705c-121">Note that **DeletePrinter** does not close the handle that is passed to it.</span></span> <span data-ttu-id="5705c-122">Daher muss die Anwendung [**closeprinter**](closeprinter.md)weiterhin aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="5705c-122">Thus, the application must still call [**ClosePrinter**](closeprinter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5705c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5705c-123">Requirements</span></span>



| <span data-ttu-id="5705c-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5705c-124">Requirement</span></span> | <span data-ttu-id="5705c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5705c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5705c-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5705c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5705c-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5705c-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5705c-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5705c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5705c-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5705c-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5705c-130">Header</span><span class="sxs-lookup"><span data-stu-id="5705c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5705c-131"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5705c-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5705c-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5705c-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="5705c-133"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5705c-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="5705c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5705c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5705c-135"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5705c-135"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="5705c-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5705c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5705c-137">Drucken</span><span class="sxs-lookup"><span data-stu-id="5705c-137">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5705c-138">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="5705c-138">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="5705c-139">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="5705c-139">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="5705c-140">**Enumdrucker**</span><span class="sxs-lookup"><span data-stu-id="5705c-140">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="5705c-141">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="5705c-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




