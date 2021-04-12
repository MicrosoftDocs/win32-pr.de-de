---
description: Die GetJob-Funktion Ruft Informationen zu einem angegebenen Druckauftrag ab.
ms.assetid: 57e59f84-d2a0-4722-b0fc-6673f7bb5c57
title: GetJob-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetJob
- GetJobA
- GetJobW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 73ae36ebab4530bf21eb86918fdbbbe941ed0741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215973"
---
# <a name="getjob-function"></a><span data-ttu-id="f710b-103">GetJob-Funktion</span><span class="sxs-lookup"><span data-stu-id="f710b-103">GetJob function</span></span>

<span data-ttu-id="f710b-104">Die **GetJob** -Funktion Ruft Informationen zu einem angegebenen Druckauftrag ab.</span><span class="sxs-lookup"><span data-stu-id="f710b-104">The **GetJob** function retrieves information about a specified print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="f710b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f710b-105">Syntax</span></span>


```C++
BOOL GetJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   JobId,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="f710b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f710b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f710b-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f710b-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f710b-108">Ein Handle für den Drucker, für den die Druckauftrags Daten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f710b-108">A handle to the printer for which the print-job data is retrieved.</span></span> <span data-ttu-id="f710b-109">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="f710b-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="f710b-110">*JobID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f710b-110">*JobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f710b-111">Identifiziert den Druckauftrag, für den Daten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f710b-111">Identifies the print job for which to retrieve data.</span></span> <span data-ttu-id="f710b-112">Verwenden Sie die [**AddJob**](addjob.md) -Funktion oder die [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) -Funktion, um einen Druckauftrags Bezeichner zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f710b-112">Use the [**AddJob**](addjob.md) function or [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function to get a print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f710b-113">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f710b-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f710b-114">Der Typ der Informationen, die im *pjob* -Puffer zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f710b-114">The type of information returned in the *pJob* buffer.</span></span> <span data-ttu-id="f710b-115">Wenn *Level den Wert* 1 hat, empfängt *pjob* die Struktur [**Job \_ Info \_ 1**](job-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="f710b-115">If *Level* is 1, *pJob* receives a [**JOB\_INFO\_1**](job-info-1.md) structure.</span></span> <span data-ttu-id="f710b-116">Wenn *Level* 2 ist, empfängt *pjob* eine Struktur mit [**Auftrags \_ Informationen \_ 2**](job-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="f710b-116">If *Level* is 2, *pJob* receives a [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f710b-117">*pjob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f710b-117">*pJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f710b-118">Ein Zeiger auf einen Puffer, der eine [**Auftrags \_ Info \_ 1**](job-info-1.md) oder eine [**Auftrags \_ Info \_ 2**](job-info-2.md) -Struktur mit Informationen über den Auftrag empfängt.</span><span class="sxs-lookup"><span data-stu-id="f710b-118">A pointer to a buffer that receives a [**JOB\_INFO\_1**](job-info-1.md) or a [**JOB\_INFO\_2**](job-info-2.md) structure containing information about the job.</span></span> <span data-ttu-id="f710b-119">Der Puffer muss groß genug sein, um die Zeichen folgen zu speichern, auf die von den Strukturmembern verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f710b-119">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="f710b-120">Um die erforderliche Puffergröße zu ermitteln, nennen Sie **GetJob** , bei dem *cbbuf* auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f710b-120">To determine the required buffer size, call **GetJob** with *cbBuf* set to zero.</span></span> <span data-ttu-id="f710b-121">**GetJob** schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt fehlerhaften \_ Puffer zurück \_ , und der *pcbrequired* -Parameter gibt die Größe (in Bytes) des Puffers zurück, der für das Array von Strukturen und deren Daten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f710b-121">**GetJob** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="f710b-122">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f710b-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f710b-123">Die Größe des Arrays in Bytes.</span><span class="sxs-lookup"><span data-stu-id="f710b-123">The size, in bytes, of the array.</span></span>

</dd> <dt>

<span data-ttu-id="f710b-124">*pcbbenötigte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f710b-124">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f710b-125">Ein Zeiger auf einen-Wert, der die Anzahl der kopierten Bytes angibt, wenn die Funktion erfolgreich ist, oder die Anzahl der Bytes, die erforderlich sind, wenn *cbbuf* zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="f710b-125">A pointer to a value that specifies the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f710b-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f710b-126">Return value</span></span>

<span data-ttu-id="f710b-127">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f710b-127">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="f710b-128">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="f710b-128">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f710b-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f710b-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f710b-130">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f710b-130">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f710b-131">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="f710b-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f710b-132">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="f710b-132">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f710b-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f710b-133">Requirements</span></span>



| <span data-ttu-id="f710b-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f710b-134">Requirement</span></span> | <span data-ttu-id="f710b-135">Wert</span><span class="sxs-lookup"><span data-stu-id="f710b-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f710b-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f710b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f710b-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f710b-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f710b-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f710b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f710b-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f710b-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f710b-140">Header</span><span class="sxs-lookup"><span data-stu-id="f710b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f710b-141"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f710b-141"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f710b-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f710b-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="f710b-143"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f710b-143"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f710b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f710b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f710b-145"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="f710b-145"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="f710b-146">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="f710b-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f710b-147">**Getjobw** (Unicode) und **getjoba** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f710b-147">**GetJobW** (Unicode) and **GetJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="f710b-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f710b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f710b-149">Drucken</span><span class="sxs-lookup"><span data-stu-id="f710b-149">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f710b-150">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="f710b-150">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f710b-151">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="f710b-151">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="f710b-152">**Auftrags \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="f710b-152">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="f710b-153">**Auftrags \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f710b-153">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="f710b-154">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="f710b-154">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="f710b-155">**Setjob**</span><span class="sxs-lookup"><span data-stu-id="f710b-155">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

