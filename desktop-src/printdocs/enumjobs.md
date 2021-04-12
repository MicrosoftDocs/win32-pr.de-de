---
description: Die EnumJobs-Funktion Ruft Informationen zu einem angegebenen Satz von Druckaufträgen für einen angegebenen Drucker ab.
ms.assetid: 1cf429ea-b40e-4063-b6de-c43b7b87f3d3
title: EnumJobs-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumJobs
- EnumJobsA
- EnumJobsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 174f58ba3fb1012e6ff46612fe312579969e6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217019"
---
# <a name="enumjobs-function"></a><span data-ttu-id="dcc75-103">EnumJobs-Funktion</span><span class="sxs-lookup"><span data-stu-id="dcc75-103">EnumJobs function</span></span>

<span data-ttu-id="dcc75-104">Die **EnumJobs** -Funktion Ruft Informationen zu einem angegebenen Satz von Druckaufträgen für einen angegebenen Drucker ab.</span><span class="sxs-lookup"><span data-stu-id="dcc75-104">The **EnumJobs** function retrieves information about a specified set of print jobs for a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcc75-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dcc75-105">Syntax</span></span>


```C++
BOOL EnumJobs(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   FirstJob,
  _In_  DWORD   NoJobs,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="dcc75-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dcc75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcc75-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcc75-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc75-108">Ein Handle für das Drucker Objekt, dessen Druckaufträge die Funktion auflistet.</span><span class="sxs-lookup"><span data-stu-id="dcc75-108">A handle to the printer object whose print jobs the function enumerates.</span></span> <span data-ttu-id="dcc75-109">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="dcc75-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="dcc75-110">*Firstjob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcc75-110">*FirstJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc75-111">Die null basierte Position innerhalb der Druck Warteschlange des ersten aufzuzählenden Druckauftrags.</span><span class="sxs-lookup"><span data-stu-id="dcc75-111">The zero-based position within the print queue of the first print job to enumerate.</span></span> <span data-ttu-id="dcc75-112">Der Wert 0 gibt beispielsweise an, dass die Enumeration beim ersten Druckauftrag in der Druck Warteschlange beginnen soll. der Wert 9 gibt an, dass die Enumeration mit dem zehnten Druckauftrag in der Druck Warteschlange beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="dcc75-112">For example, a value of 0 specifies that enumeration should begin at the first print job in the print queue; a value of 9 specifies that enumeration should begin at the tenth print job in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="dcc75-113">*Nojobs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcc75-113">*NoJobs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc75-114">Die Gesamtanzahl der aufzuzählenden Druckaufträge.</span><span class="sxs-lookup"><span data-stu-id="dcc75-114">The total number of print jobs to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="dcc75-115">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcc75-115">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc75-116">Der Typ der Informationen, die im *pjob* -Puffer zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dcc75-116">The type of information returned in the *pJob* buffer.</span></span>



| <span data-ttu-id="dcc75-117">Wert</span><span class="sxs-lookup"><span data-stu-id="dcc75-117">Value</span></span>                                                                                                | <span data-ttu-id="dcc75-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="dcc75-118">Meaning</span></span>                                                                              |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="dcc75-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="dcc75-119"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="dcc75-120">*pjob* empfängt ein Array von [**Auftrags \_ Informationen \_ 1**](job-info-1.md) -Strukturen</span><span class="sxs-lookup"><span data-stu-id="dcc75-120">*pJob* receives an array of [**JOB\_INFO\_1**](job-info-1.md) structures</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="dcc75-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="dcc75-121"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="dcc75-122">*pjob* empfängt ein Array von [**Auftrags \_ Informationen \_ 2**](job-info-2.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="dcc75-122">*pJob* receives an array of [**JOB\_INFO\_2**](job-info-2.md) structures</span></span><br/> |
| <span id="3"></span><dl> <span data-ttu-id="dcc75-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="dcc75-123"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="dcc75-124">*pjob* empfängt ein Array von [**Auftrags \_ Informationen \_ 3**](job-info-3.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="dcc75-124">*pJob* receives an array of [**JOB\_INFO\_3**](job-info-3.md) structures</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dcc75-125">*pjob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dcc75-125">*pJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc75-126">Ein Zeiger auf einen Puffer, der ein Array mit den Strukturen Job [**\_ Info \_ 1**](job-info-1.md), [**Job \_ Info \_ 2**](job-info-2.md)oder [**Job \_ Info \_ 3**](job-info-3.md) empfängt.</span><span class="sxs-lookup"><span data-stu-id="dcc75-126">A pointer to a buffer that receives an array of [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_3**](job-info-3.md) structures.</span></span> <span data-ttu-id="dcc75-127">Der Puffer muss groß genug sein, um das Array von Strukturen und Zeichen folgen oder andere Daten zu erhalten, auf die die Strukturmember zeigen.</span><span class="sxs-lookup"><span data-stu-id="dcc75-127">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="dcc75-128">Um die erforderliche Puffergröße zu ermitteln, muss **EnumJobs** aufgerufen werden, wobei *cbbuf* auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dcc75-128">To determine the required buffer size, call **EnumJobs** with *cbBuf* set to zero.</span></span> <span data-ttu-id="dcc75-129">**EnumJobs** schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt fehlerhaften \_ Puffer zurück \_ , und der *pcbrequired* -Parameter gibt die Größe (in Bytes) des Puffers zurück, der für das Array von Strukturen und deren Daten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="dcc75-129">**EnumJobs** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="dcc75-130">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcc75-130">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc75-131">Die Größe des *pjob* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="dcc75-131">The size, in bytes, of the *pJob* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="dcc75-132">*pcbbenötigte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dcc75-132">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc75-133">Ein Zeiger auf eine Variable, die die Anzahl der kopierten Bytes empfängt, wenn die Funktion erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dcc75-133">A pointer to a variable that receives the number of bytes copied if the function succeeds.</span></span> <span data-ttu-id="dcc75-134">Wenn die Funktion fehlschlägt, erhält die Variable die erforderliche Anzahl von Bytes.</span><span class="sxs-lookup"><span data-stu-id="dcc75-134">If the function fails, the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="dcc75-135">*pkreturned* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dcc75-135">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc75-136">Ein Zeiger auf eine Variable, die die Anzahl der im *pjob* -Puffer zurückgegebenen Struktur von [**Auftrags \_ Informationen \_ 1**](job-info-1.md), [**Auftrags \_ Informationen \_ 2**](job-info-2.md)oder [**Auftrags \_ Informationen \_ 3**](job-info-3.md) empfängt.</span><span class="sxs-lookup"><span data-stu-id="dcc75-136">A pointer to a variable that receives the number of [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_3**](job-info-3.md) structures returned in the *pJob* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcc75-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dcc75-137">Return value</span></span>

<span data-ttu-id="dcc75-138">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="dcc75-138">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="dcc75-139">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="dcc75-139">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcc75-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dcc75-140">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dcc75-141">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dcc75-141">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="dcc75-142">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="dcc75-142">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="dcc75-143">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="dcc75-143">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="dcc75-144">Die Struktur der [**Auftrags \_ Informationen \_ 1**](job-info-1.md) enthält allgemeine Druckauftrags Informationen. die Struktur der [**Auftrags \_ Informationen \_ 2**](job-info-2.md) enthält wesentlich ausführlichere Informationen.</span><span class="sxs-lookup"><span data-stu-id="dcc75-144">The [**JOB\_INFO\_1**](job-info-1.md) structure contains general print-job information; the [**JOB\_INFO\_2**](job-info-2.md) structure has much more detailed information.</span></span> <span data-ttu-id="dcc75-145">Die [**Auftrags \_ Info \_ 3**](job-info-3.md) -Struktur enthält Informationen darüber, wie Aufträge verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="dcc75-145">The [**JOB\_INFO\_3**](job-info-3.md) structure contains information about how jobs are linked.</span></span>

<span data-ttu-id="dcc75-146">Um die Anzahl der Druckaufträge in der Drucker Warteschlange zu ermitteln, müssen Sie die [**GetPrinter**](getprinter.md) -Funktion mit dem auf 2 festgelegten *Level* -Parameter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dcc75-146">To determine the number of print jobs in the printer queue, call the [**GetPrinter**](getprinter.md) function with the *Level* parameter set to 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcc75-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dcc75-147">Requirements</span></span>



| <span data-ttu-id="dcc75-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dcc75-148">Requirement</span></span> | <span data-ttu-id="dcc75-149">Wert</span><span class="sxs-lookup"><span data-stu-id="dcc75-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcc75-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dcc75-150">Minimum supported client</span></span><br/> | <span data-ttu-id="dcc75-151">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dcc75-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dcc75-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dcc75-152">Minimum supported server</span></span><br/> | <span data-ttu-id="dcc75-153">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dcc75-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dcc75-154">Header</span><span class="sxs-lookup"><span data-stu-id="dcc75-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcc75-155"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dcc75-155"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="dcc75-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dcc75-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="dcc75-157"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcc75-157"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="dcc75-158">DLL</span><span class="sxs-lookup"><span data-stu-id="dcc75-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcc75-159"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="dcc75-159"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="dcc75-160">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="dcc75-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="dcc75-161">**Enumjobsw** (Unicode) und **enumjobsa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="dcc75-161">**EnumJobsW** (Unicode) and **EnumJobsA** (ANSI)</span></span><br/>                                               |



## <a name="see-also"></a><span data-ttu-id="dcc75-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcc75-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcc75-163">Drucken</span><span class="sxs-lookup"><span data-stu-id="dcc75-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="dcc75-164">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="dcc75-164">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="dcc75-165">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="dcc75-165">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="dcc75-166">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="dcc75-166">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="dcc75-167">**Auftrags \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="dcc75-167">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="dcc75-168">**Auftrags \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="dcc75-168">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="dcc75-169">**Auftrags \_ Informationen \_ 3**</span><span class="sxs-lookup"><span data-stu-id="dcc75-169">**JOB\_INFO\_3**</span></span>](job-info-3.md)
</dt> <dt>

[<span data-ttu-id="dcc75-170">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="dcc75-170">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="dcc75-171">**Setjob**</span><span class="sxs-lookup"><span data-stu-id="dcc75-171">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

