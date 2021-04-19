---
description: Die schedulejob-Funktion fordert an, dass der Druck Spooler einen angegebenen Druckauftrag zum Drucken plant.
ms.assetid: a103a29c-be4d-491e-9b04-84571fe969a5
title: Schedulejob-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScheduleJob
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 1ef938cc2a9b1893a4825255325457d5c210842a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363231"
---
# <a name="schedulejob-function"></a><span data-ttu-id="dec7c-103">Schedulejob-Funktion</span><span class="sxs-lookup"><span data-stu-id="dec7c-103">ScheduleJob function</span></span>

<span data-ttu-id="dec7c-104">Die **schedulejob** -Funktion fordert an, dass der Druck Spooler einen angegebenen Druckauftrag zum Drucken plant.</span><span class="sxs-lookup"><span data-stu-id="dec7c-104">The **ScheduleJob** function requests that the print spooler schedule a specified print job for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="dec7c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dec7c-105">Syntax</span></span>


```C++
BOOL ScheduleJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  dwJobID
);
```



## <a name="parameters"></a><span data-ttu-id="dec7c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dec7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dec7c-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dec7c-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dec7c-108">Ein Handle für den Drucker für den Druckauftrag.</span><span class="sxs-lookup"><span data-stu-id="dec7c-108">A handle to the printer for the print job.</span></span> <span data-ttu-id="dec7c-109">Dabei muss es sich um einen lokalen Drucker handeln, der als Druck Drucker konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="dec7c-109">This must be a local printer that is configured as a spooled printer.</span></span> <span data-ttu-id="dec7c-110">Wenn *hprinter* ein Handle für eine Remote Druckerverbindung ist oder wenn der Drucker für den direkten Druck konfiguriert ist, tritt bei der **schedulejob** -Funktion ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="dec7c-110">If *hPrinter* is a handle to a remote printer connection, or if the printer is configured for direct printing, the **ScheduleJob** function fails.</span></span> <span data-ttu-id="dec7c-111">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="dec7c-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

<span data-ttu-id="dec7c-112">*hprinter* muss das gleiche Drucker Handle sein, das im [**AddJob**](addjob.md) -Rückruf angegeben wurde, der den *dwjobid* -Druckauftrags Bezeichner abgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="dec7c-112">*hPrinter* must be the same printer handle specified in the call to [**AddJob**](addjob.md) that obtained the *dwJobID* print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-113">*dwjobid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dec7c-113">*dwJobID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dec7c-114">Der Druckauftrag, der geplant werden soll.</span><span class="sxs-lookup"><span data-stu-id="dec7c-114">The print job to be scheduled.</span></span> <span data-ttu-id="dec7c-115">Sie erhalten diese Druckauftrags Kennung durch Aufrufen der [**AddJob**](addjob.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="dec7c-115">You obtain this print job identifier by calling the [**AddJob**](addjob.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dec7c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dec7c-116">Return value</span></span>

<span data-ttu-id="dec7c-117">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="dec7c-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="dec7c-118">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="dec7c-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="dec7c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dec7c-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dec7c-120">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dec7c-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="dec7c-121">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="dec7c-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="dec7c-122">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="dec7c-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="dec7c-123">Sie müssen die [**AddJob**](addjob.md) -Funktion erfolgreich aufrufen, bevor Sie die **schedulejob** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dec7c-123">You must successfully call the [**AddJob**](addjob.md) function before calling the **ScheduleJob** function.</span></span> <span data-ttu-id="dec7c-124">**AddJob** erhält den Druckauftrags Bezeichner, den Sie als *dwjobid* an **schedulejob** übergeben.</span><span class="sxs-lookup"><span data-stu-id="dec7c-124">**AddJob** obtains the print job identifier that you pass to **ScheduleJob** as *dwJobID*.</span></span> <span data-ttu-id="dec7c-125">Beide Aufrufe müssen den gleichen Wert für *hprinter* verwenden.</span><span class="sxs-lookup"><span data-stu-id="dec7c-125">Both calls must use the same value for *hPrinter*.</span></span>

<span data-ttu-id="dec7c-126">Die **schedulejob** -Funktion prüft auf eine gültige Spooldatei.</span><span class="sxs-lookup"><span data-stu-id="dec7c-126">The **ScheduleJob** function checks for a valid spool file.</span></span> <span data-ttu-id="dec7c-127">Wenn eine Spooldatei ungültig ist oder leer ist, löscht **schedulejob** sowohl die Spooldatei als auch den entsprechenden Druckauftrags Eintrag im Druck Spooler.</span><span class="sxs-lookup"><span data-stu-id="dec7c-127">If there is an invalid spool file, or if it is empty, **ScheduleJob** deletes both the spool file and the corresponding print job entry in the print spooler.</span></span>

## <a name="requirements"></a><span data-ttu-id="dec7c-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dec7c-128">Requirements</span></span>



| <span data-ttu-id="dec7c-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dec7c-129">Requirement</span></span> | <span data-ttu-id="dec7c-130">Wert</span><span class="sxs-lookup"><span data-stu-id="dec7c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec7c-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dec7c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dec7c-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dec7c-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dec7c-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dec7c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dec7c-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dec7c-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dec7c-135">Header</span><span class="sxs-lookup"><span data-stu-id="dec7c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="dec7c-136"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dec7c-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="dec7c-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dec7c-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="dec7c-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dec7c-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="dec7c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="dec7c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dec7c-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dec7c-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="dec7c-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dec7c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dec7c-142">Drucken</span><span class="sxs-lookup"><span data-stu-id="dec7c-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="dec7c-143">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="dec7c-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="dec7c-144">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="dec7c-144">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="dec7c-145">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="dec7c-145">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




