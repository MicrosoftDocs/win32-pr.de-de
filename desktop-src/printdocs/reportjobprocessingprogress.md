---
description: Meldet an den Druckspoolerdienst, ob sich ein XPS-Druckauftrag in der spoolingphase oder der Renderingphase befindet und welcher Teil der Verarbeitung derzeit ausgeführt wird.
ms.assetid: 66f7483d-be98-410d-b0c7-430743397de2
title: Reportjobprocessingprogress-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportJobProcessingProgress
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 327d2f7cffe2f90a5719de38cef4cd3fde17e086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960189"
---
# <a name="reportjobprocessingprogress-function"></a><span data-ttu-id="90bf4-103">Reportjobprocessingprogress-Funktion</span><span class="sxs-lookup"><span data-stu-id="90bf4-103">ReportJobProcessingProgress function</span></span>

<span data-ttu-id="90bf4-104">Meldet an den Druckspoolerdienst, ob sich ein XPS-Druckauftrag in der spoolingphase oder der Renderingphase befindet und welcher Teil der Verarbeitung derzeit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90bf4-104">Reports to the Print Spooler service whether an XPS print job is in the spooling or the rendering phase and what part of the processing is currently underway.</span></span>

## <a name="syntax"></a><span data-ttu-id="90bf4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="90bf4-105">Syntax</span></span>


```C++
HRESULT ReportJobProcessingProgress(
  _In_ HANDLE                printerHandle,
  _In_ ULONG                 jobId,
       EPrintXPSJobOperation jobOperation,
       EPrintXPSJobProgress  jobProgress
);
```



## <a name="parameters"></a><span data-ttu-id="90bf4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="90bf4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90bf4-107">*printerhandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90bf4-107">*printerHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90bf4-108">Ein Drucker handle, für das die Funktion Informationen abrufen soll.</span><span class="sxs-lookup"><span data-stu-id="90bf4-108">A printer handle for which the function is to retrieve information.</span></span> <span data-ttu-id="90bf4-109">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="90bf4-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="90bf4-110">*jobId* \[in\]</span><span class="sxs-lookup"><span data-stu-id="90bf4-110">*jobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90bf4-111">Identifiziert den Druckauftrag, für den Daten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="90bf4-111">Identifies the print job for which to retrieve data.</span></span> <span data-ttu-id="90bf4-112">Verwenden Sie die [**AddJob**](addjob.md) -Funktion oder die [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) -Funktion, um einen Druckauftrags Bezeichner zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="90bf4-112">Use the [**AddJob**](addjob.md) function or [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function to get a print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="90bf4-113">*joboperation*</span><span class="sxs-lookup"><span data-stu-id="90bf4-113">*jobOperation*</span></span> 
</dt> <dd>

<span data-ttu-id="90bf4-114">Gibt an, ob sich der Auftrag in der spoolingphase oder der Renderingphase befindet.</span><span class="sxs-lookup"><span data-stu-id="90bf4-114">Specifies whether the job is in the spooling phase or the rendering phase.</span></span>

</dd> <dt>

<span data-ttu-id="90bf4-115">*jobprogress*</span><span class="sxs-lookup"><span data-stu-id="90bf4-115">*jobProgress*</span></span> 
</dt> <dd>

<span data-ttu-id="90bf4-116">Gibt an, welcher Teil der Verarbeitung derzeit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90bf4-116">Specifies what part of the processing is currently underway.</span></span> <span data-ttu-id="90bf4-117">Dieser Wert bezieht sich abhängig vom Wert von *joboperation* auf Ereignisse in der spoolingphase oder der Renderingphase.</span><span class="sxs-lookup"><span data-stu-id="90bf4-117">This value refers to events in either the spooling or rendering phase depending on the value of *jobOperation*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90bf4-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90bf4-118">Return value</span></span>

<span data-ttu-id="90bf4-119">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert S \_ OK; andernfalls enthält das **HRESULT** einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="90bf4-119">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="90bf4-120">Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="90bf4-120">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="90bf4-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90bf4-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="90bf4-122">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="90bf4-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="90bf4-123">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="90bf4-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="90bf4-124">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="90bf4-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

> [!Note]  
> <span data-ttu-id="90bf4-125">**Reportjobprocessingprogress** meldet nur den Fortschritt des XPS-Druckauftrags, wenn sich der Druckauftrag in der spoolingphase oder der Renderingphase befindet.</span><span class="sxs-lookup"><span data-stu-id="90bf4-125">**ReportJobProcessingProgress** will only report the progress of the XPS print job if the print job is in the spooling or rendering phase.</span></span> <span data-ttu-id="90bf4-126">**Reportjobprocessingprogress** schlägt fehl, wenn Sie aufgerufen wird, wenn sich der XPS-Druckauftrag nicht in der spoolingphase oder der Renderingphase befindet.</span><span class="sxs-lookup"><span data-stu-id="90bf4-126">**ReportJobProcessingProgress** will fail if it is called when the XPS print job is not in the spooling or rendering phase.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="90bf4-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90bf4-127">Requirements</span></span>



| <span data-ttu-id="90bf4-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90bf4-128">Requirement</span></span> | <span data-ttu-id="90bf4-129">Wert</span><span class="sxs-lookup"><span data-stu-id="90bf4-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90bf4-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90bf4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="90bf4-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90bf4-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="90bf4-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90bf4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="90bf4-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90bf4-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="90bf4-134">Header</span><span class="sxs-lookup"><span data-stu-id="90bf4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="90bf4-135"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90bf4-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="90bf4-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="90bf4-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="90bf4-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90bf4-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="90bf4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="90bf4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90bf4-139"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90bf4-139"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="90bf4-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90bf4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90bf4-141">Drucken</span><span class="sxs-lookup"><span data-stu-id="90bf4-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="90bf4-142">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="90bf4-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="90bf4-143">**Eprintxpsjoboperation**</span><span class="sxs-lookup"><span data-stu-id="90bf4-143">**EPrintXPSJobOperation**</span></span>](eprintxpsjoboperation.md)
</dt> <dt>

[<span data-ttu-id="90bf4-144">**Eprintxpsjobprogress**</span><span class="sxs-lookup"><span data-stu-id="90bf4-144">**EPrintXPSJobProgress**</span></span>](eprintxpsjobprogress.md)
</dt> </dl>

 

