---
description: Die flushprinter-Funktion sendet einen Puffer an den Drucker, um ihn aus einem vorübergehenden Zustand zu löschen.
ms.assetid: 08e54175-da68-4ebd-91ec-8f4525f49d30
title: Flushprinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FlushPrinter
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d46a4a8d7143e10fc13722d278ca21a0602b7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528997"
---
# <a name="flushprinter-function"></a><span data-ttu-id="cba54-103">Flushprinter-Funktion</span><span class="sxs-lookup"><span data-stu-id="cba54-103">FlushPrinter function</span></span>

<span data-ttu-id="cba54-104">Die **flushprinter** -Funktion sendet einen Puffer an den Drucker, um ihn aus einem vorübergehenden Zustand zu löschen.</span><span class="sxs-lookup"><span data-stu-id="cba54-104">The **FlushPrinter** function sends a buffer to the printer in order to clear it from a transient state.</span></span>

## <a name="syntax"></a><span data-ttu-id="cba54-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cba54-105">Syntax</span></span>


```C++
BOOL FlushPrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten,
  _In_  DWORD   cSleep
);
```



## <a name="parameters"></a><span data-ttu-id="cba54-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cba54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cba54-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cba54-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cba54-108">Ein Handle für das Drucker Objekt.</span><span class="sxs-lookup"><span data-stu-id="cba54-108">A handle to the printer object.</span></span> <span data-ttu-id="cba54-109">Dabei sollte es sich um das gleiche Handle handeln, das in einem vorherigen [**Write-Printer**](writeprinter.md) -Befehl vom Druckertreiber verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="cba54-109">This should be the same handle that was used, in a prior [**WritePrinter**](writeprinter.md) call, by the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="cba54-110">*PBUF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cba54-110">*pBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cba54-111">Ein Zeiger auf ein Bytearray, das die Daten enthält, die in den Drucker geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cba54-111">A pointer to an array of bytes that contains the data to be written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="cba54-112">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cba54-112">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cba54-113">Die Größe (in Bytes) des Arrays, auf das von *PBUF* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cba54-113">The size, in bytes, of the array pointed to by *pBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="cba54-114">*pcwritten* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cba54-114">*pcWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cba54-115">Ein Zeiger auf einen Wert, der die Anzahl der Daten Bytes empfängt, die an den Drucker geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="cba54-115">A pointer to a value that receives the number of bytes of data that were written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="cba54-116">*csleep* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cba54-116">*cSleep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cba54-117">Die Zeit (in Millisekunden), für die die e/a-Linie zum Druckerport im Leerlauf bleiben soll.</span><span class="sxs-lookup"><span data-stu-id="cba54-117">The time, in milliseconds, for which the I/O line to the printer port should be kept idle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cba54-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cba54-118">Return value</span></span>

<span data-ttu-id="cba54-119">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.</span><span class="sxs-lookup"><span data-stu-id="cba54-119">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="cba54-120">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="cba54-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cba54-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cba54-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cba54-122">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cba54-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="cba54-123">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="cba54-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="cba54-124">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="cba54-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="cba54-125">**Flushprinter** sollte nur aufgerufen werden, wenn bei " [**Write-Printer**](writeprinter.md) " ein Fehler aufgetreten ist, sodass der Drucker in einem vorübergehenden Zustand ist.</span><span class="sxs-lookup"><span data-stu-id="cba54-125">**FlushPrinter** should be called only if [**WritePrinter**](writeprinter.md) failed, leaving the printer in a transient state.</span></span> <span data-ttu-id="cba54-126">Beispielsweise könnte der Drucker in einen vorübergehenden Zustand geraten, wenn der Auftrag abgebrochen wird, und der Druckertreiber hat einige Rohdaten teilweise an den Drucker gesendet.</span><span class="sxs-lookup"><span data-stu-id="cba54-126">For example, the printer could get into a transient state when the job gets aborted and the printer driver has partially sent some raw data to the printer.</span></span>

<span data-ttu-id="cba54-127">**Flushprinter** kann auch einen Leerlauf Zeitraum angeben, in dem der Druck Spooler keine Aufträge für den entsprechenden Druckerport plant.</span><span class="sxs-lookup"><span data-stu-id="cba54-127">**FlushPrinter** also can specify an idle period during which the print spooler does not schedule any jobs to the corresponding printer port.</span></span>

## <a name="requirements"></a><span data-ttu-id="cba54-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cba54-128">Requirements</span></span>



| <span data-ttu-id="cba54-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cba54-129">Requirement</span></span> | <span data-ttu-id="cba54-130">Wert</span><span class="sxs-lookup"><span data-stu-id="cba54-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cba54-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cba54-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cba54-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cba54-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cba54-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cba54-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cba54-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cba54-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cba54-135">Header</span><span class="sxs-lookup"><span data-stu-id="cba54-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="cba54-136"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cba54-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="cba54-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cba54-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="cba54-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cba54-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="cba54-139">DLL</span><span class="sxs-lookup"><span data-stu-id="cba54-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cba54-140"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="cba54-140"><dt>Winspool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="cba54-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cba54-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cba54-142">Drucken</span><span class="sxs-lookup"><span data-stu-id="cba54-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="cba54-143">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="cba54-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="cba54-144">**"Write Printer"**</span><span class="sxs-lookup"><span data-stu-id="cba54-144">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




