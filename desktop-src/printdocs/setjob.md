---
description: Mit der setjob-Funktion wird ein Druckauftrag auf einem angegebenen Drucker angehalten, fortgesetzt, abgebrochen oder neu gestartet. Sie können auch die setjob-Funktion verwenden, um Druckauftrags Parameter festzulegen, z. b. die Druckauftrags Priorität und den Dokumentnamen.
ms.assetid: 21947c69-c517-4962-8eb7-b45ed4211d9a
title: Setjob-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetJob
- SetJobA
- SetJobW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 34dfc8c0239a10d7e7f036beed457d57329f4c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349541"
---
# <a name="setjob-function"></a><span data-ttu-id="2d941-104">Setjob-Funktion</span><span class="sxs-lookup"><span data-stu-id="2d941-104">SetJob function</span></span>

<span data-ttu-id="2d941-105">Mit der **setjob** -Funktion wird ein Druckauftrag auf einem angegebenen Drucker angehalten, fortgesetzt, abgebrochen oder neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="2d941-105">The **SetJob** function pauses, resumes, cancels, or restarts a print job on a specified printer.</span></span> <span data-ttu-id="2d941-106">Sie können auch die **setjob** -Funktion verwenden, um Druckauftrags Parameter festzulegen, z. b. die Druckauftrags Priorität und den Dokumentnamen.</span><span class="sxs-lookup"><span data-stu-id="2d941-106">You can also use the **SetJob** function to set print job parameters, such as the print job priority and the document name.</span></span>

<span data-ttu-id="2d941-107">Mit der **setjob** -Funktion können Sie einem Druckauftrag einen Befehl übergeben, Druckauftrags Parameter festlegen oder beide im gleichen-Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d941-107">You can use the **SetJob** function to give a command to a print job, or to set print job parameters, or to do both in the same call.</span></span> <span data-ttu-id="2d941-108">Der Wert des *Command* -Parameters wirkt sich nicht darauf aus, wie die Funktion die Parameter " *Level* " und " *pjob* " verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d941-108">The value of the *Command* parameter does not affect how the function uses the *Level* and *pJob* parameters.</span></span> <span data-ttu-id="2d941-109">Außerdem können Sie **setjob** mit [**Auftrags \_ Info \_ 3**](job-info-3.md) verwenden, um einen Satz von Druckaufträgen miteinander zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="2d941-109">Also, you can use **SetJob** with [**JOB\_INFO\_3**](job-info-3.md) to link together a set of print jobs.</span></span> <span data-ttu-id="2d941-110">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="2d941-110">See Remarks for more information.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d941-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d941-111">Syntax</span></span>


```C++
BOOL SetJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  JobId,
  _In_ DWORD  Level,
  _In_ LPBYTE pJob,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a><span data-ttu-id="2d941-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d941-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d941-113">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d941-113">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d941-114">Ein Handle für das gewünschte Drucker Objekt.</span><span class="sxs-lookup"><span data-stu-id="2d941-114">A handle to the printer object of interest.</span></span> <span data-ttu-id="2d941-115">Verwenden Sie die Funktion " [**OpenPrinter**](openprinter.md)", " [**OpenPrinter2**](openprinter2.md)" oder " [**addprinter**](addprinter.md) ", um ein Drucker Handle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2d941-115">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="2d941-116">*JobID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d941-116">*JobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d941-117">Bezeichner, der den Druckauftrag angibt.</span><span class="sxs-lookup"><span data-stu-id="2d941-117">Identifier that specifies the print job.</span></span> <span data-ttu-id="2d941-118">Sie erhalten einen Druckauftrags Bezeichner, indem Sie die [**AddJob**](addjob.md) -Funktion oder die [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2d941-118">You obtain a print job identifier by calling the [**AddJob**](addjob.md) function or the [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function.</span></span>

<span data-ttu-id="2d941-119">Wenn der *Ebenenparameter* auf 3 festgelegt ist, muss der *JobID* -Parameter mit dem **JobID** -Member der [**Auftrags \_ Info \_ 3**](job-info-3.md) -Struktur, auf die von *pjob* verwiesen wird, stimmen.</span><span class="sxs-lookup"><span data-stu-id="2d941-119">If the *Level* parameter is set to 3, the *JobId* parameter must match the **JobId** member of the [**JOB\_INFO\_3**](job-info-3.md) structure pointed to by *pJob*</span></span>

</dd> <dt>

<span data-ttu-id="2d941-120">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d941-120">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d941-121">Der Typ der Auftrags Informationsstruktur, auf die durch den *pjob* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2d941-121">The type of job information structure pointed to by the *pJob* parameter.</span></span>

<span data-ttu-id="2d941-122">**Alle Versionen von Windows**: Sie können den *Level* -Parameter auf 0, 1 oder 2 festlegen.</span><span class="sxs-lookup"><span data-stu-id="2d941-122">**All versions of Windows**: You can set the *Level* parameter to 0, 1, or 2.</span></span> <span data-ttu-id="2d941-123">Wenn Sie die *Ebene* auf 0 festlegen, sollte *pjob* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="2d941-123">When you set *Level* to 0, *pJob* should be **NULL**.</span></span> <span data-ttu-id="2d941-124">Verwenden Sie diese Werte, wenn Sie keine Druckauftrags Parameter festlegen.</span><span class="sxs-lookup"><span data-stu-id="2d941-124">Use these values when you are not setting any print job parameters.</span></span>

<span data-ttu-id="2d941-125">Sie können auch den *Level* -Parameter auf 3 festlegen.</span><span class="sxs-lookup"><span data-stu-id="2d941-125">You can also set the *Level* parameter to 3.</span></span>

<span data-ttu-id="2d941-126">Ab **Windows Vista**: Sie können den *Level* -Parameter auch auf 4 festlegen.</span><span class="sxs-lookup"><span data-stu-id="2d941-126">Starting with **Windows Vista**: You can also set the *Level* parameter to 4.</span></span>

</dd> <dt>

<span data-ttu-id="2d941-127">*pjob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d941-127">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d941-128">Ein Zeiger auf eine-Struktur, die die Druckauftrags Parameter festlegt.</span><span class="sxs-lookup"><span data-stu-id="2d941-128">A pointer to a structure that sets the print job parameters.</span></span>

<span data-ttu-id="2d941-129">**Alle Versionen von Windows**: *pjob* können auf eine [**Auftrags \_ Info \_ 1**](job-info-1.md) oder eine [**Auftrags \_ Info \_ 2**](job-info-2.md) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="2d941-129">**All versions of Windows**: *pJob* can point to a [**JOB\_INFO\_1**](job-info-1.md) or [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>

<span data-ttu-id="2d941-130">*pjob* kann auch auf eine [**Auftrags \_ Info \_ 3**](job-info-3.md) -Struktur verweisen.</span><span class="sxs-lookup"><span data-stu-id="2d941-130">*pJob* can also point to a [**JOB\_INFO\_3**](job-info-3.md) structure.</span></span> <span data-ttu-id="2d941-131">Sie müssen über die Berechtigung Zugriffsberechtigung **\_ \_ Verwalten** für die Aufträge verfügen, die von den Membern **JobID** und **nextjobid** der Struktur **Job \_ Info \_ 3** angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2d941-131">You must have **JOB\_ACCESS\_ADMINISTER** access permission for the jobs specified by the **JobId** and **NextJobId** members of the **JOB\_INFO\_3** structure.</span></span>

<span data-ttu-id="2d941-132">Ab **Windows Vista**: *pjob* kann auch auf eine [**Auftrags \_ Info \_ 4**](job-info-4.md) -Struktur verweisen.</span><span class="sxs-lookup"><span data-stu-id="2d941-132">Starting with **Windows Vista**: *pJob* can also point to a [**JOB\_INFO\_4**](job-info-4.md) structure.</span></span>

<span data-ttu-id="2d941-133">Wenn der *Level* -Parameter 0 ist, sollte *pjob* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="2d941-133">If the *Level* parameter is 0, *pJob* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2d941-134">*Befehl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d941-134">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d941-135">Der auszuführende Druckauftrags Vorgang.</span><span class="sxs-lookup"><span data-stu-id="2d941-135">The print job operation to perform.</span></span> <span data-ttu-id="2d941-136">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="2d941-136">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="2d941-137">Wert</span><span class="sxs-lookup"><span data-stu-id="2d941-137">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="2d941-138">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2d941-138">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="JOB_CONTROL_CANCEL"></span><span id="job_control_cancel"></span><dl> <span data-ttu-id="2d941-139"><dt>**Abbrechen der Auftrags \_ Steuerung \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2d941-139"><dt>**JOB\_CONTROL\_CANCEL**</dt></span></span> </dl>                                    | <span data-ttu-id="2d941-140">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d941-140">Do not use.</span></span> <span data-ttu-id="2d941-141">Verwenden Sie zum Löschen eines Druckauftrags **das \_ \_ Löschen von Auftrags Steuer** Elementen.</span><span class="sxs-lookup"><span data-stu-id="2d941-141">To delete a print job, use **JOB\_CONTROL\_DELETE**.</span></span><br/>        |
| <span id="JOB_CONTROL_PAUSE"></span><span id="job_control_pause"></span><dl> <span data-ttu-id="2d941-142"><dt>**Anhalten der Auftrags \_ Steuerung \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2d941-142"><dt>**JOB\_CONTROL\_PAUSE**</dt></span></span> </dl>                                       | <span data-ttu-id="2d941-143">Halten Sie den Druckauftrag an.</span><span class="sxs-lookup"><span data-stu-id="2d941-143">Pause the print job.</span></span><br/>                                                    |
| <span id="JOB_CONTROL_RESTART"></span><span id="job_control_restart"></span><dl> <span data-ttu-id="2d941-144"><dt>**Neustarten der Auftrags \_ Steuerung \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2d941-144"><dt>**JOB\_CONTROL\_RESTART**</dt></span></span> </dl>                                 | <span data-ttu-id="2d941-145">Starten Sie den Druckauftrag neu.</span><span class="sxs-lookup"><span data-stu-id="2d941-145">Restart the print job.</span></span> <span data-ttu-id="2d941-146">Ein Auftrag kann nur neu gestartet werden, wenn er gedruckt wurde.</span><span class="sxs-lookup"><span data-stu-id="2d941-146">A job can only be restarted if it was printing.</span></span><br/>  |
| <span id="JOB_CONTROL_RESUME"></span><span id="job_control_resume"></span><dl> <span data-ttu-id="2d941-147"><dt>**Fortsetzen der Auftrags \_ Steuerung \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2d941-147"><dt>**JOB\_CONTROL\_RESUME**</dt></span></span> </dl>                                    | <span data-ttu-id="2d941-148">Fortsetzen eines angehaltenen Druckauftrags</span><span class="sxs-lookup"><span data-stu-id="2d941-148">Resume a paused print job.</span></span><br/>                                              |
| <span id="JOB_CONTROL_DELETE"></span><span id="job_control_delete"></span><dl> <span data-ttu-id="2d941-149"><dt>**Löschen von Auftrags \_ Steuerelementen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2d941-149"><dt>**JOB\_CONTROL\_DELETE**</dt></span></span> </dl>                                    | <span data-ttu-id="2d941-150">Löschen Sie den Druckauftrag.</span><span class="sxs-lookup"><span data-stu-id="2d941-150">Delete the print job.</span></span><br/>                                                   |
| <span id="JOB_CONTROL_SENT_TO_PRINTER"></span><span id="job_control_sent_to_printer"></span><dl> <span data-ttu-id="2d941-151"><dt>**\_ \_ \_ an den Drucker gesendete Auftragssteuerung \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2d941-151"><dt>**JOB\_CONTROL\_SENT\_TO\_PRINTER**</dt></span></span> </dl>       | <span data-ttu-id="2d941-152">Wird von Port Monitoren zum Beenden des Druckauftrags verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d941-152">Used by port monitors to end the print job.</span></span><br/>                             |
| <span id="JOB_CONTROL_LAST_PAGE_EJECTED"></span><span id="job_control_last_page_ejected"></span><dl> <span data-ttu-id="2d941-153"><dt>**\_ \_ Letzte \_ Seite \_ der Auftragssteuerung**</dt></span><span class="sxs-lookup"><span data-stu-id="2d941-153"><dt>**JOB\_CONTROL\_LAST\_PAGE\_EJECTED**</dt></span></span> </dl> | <span data-ttu-id="2d941-154">Wird von sprach Monitoren zum Beenden des Druckauftrags verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d941-154">Used by language monitors to end the print job.</span></span><br/>                         |
| <span id="JOB_CONTROL_RETAIN"></span><span id="job_control_retain"></span><dl> <span data-ttu-id="2d941-155"><dt>**beibehalten der Auftrags \_ Kontrolle \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2d941-155"><dt>**JOB\_CONTROL\_RETAIN**</dt></span></span> </dl>                                    | <span data-ttu-id="2d941-156">**Windows Vista und** höher: behalten Sie den Auftrag in der Warteschlange, nachdem er gedruckt wurde.</span><span class="sxs-lookup"><span data-stu-id="2d941-156">**Windows Vista and later**: Keep the job in the queue after it prints.</span></span><br/> |
| <span id="JOB_CONTROL_RELEASE"></span><span id="job_control_release"></span><dl> <span data-ttu-id="2d941-157"><dt>**Freigabe der Auftrags \_ Kontrolle \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2d941-157"><dt>**JOB\_CONTROL\_RELEASE**</dt></span></span> </dl>                                 | <span data-ttu-id="2d941-158">**Windows Vista und** höher: Geben Sie den Druckauftrag frei.</span><span class="sxs-lookup"><span data-stu-id="2d941-158">**Windows Vista and later**: Release the print job.</span></span><br/>                     |



 

<span data-ttu-id="2d941-159">Sie können den gleichen **calljob** -Befehl verwenden, um Druckauftrags Parameter festzulegen und einem Druckauftrag einen Befehl zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="2d941-159">You can use the same call to the **SetJob** function to set print job parameters and to give a command to a print job.</span></span> <span data-ttu-id="2d941-160">Folglich muss der *Befehl* nicht 0 sein, wenn Sie Druckauftrags Parameter festlegen, obwohl dies der Fall sein kann.</span><span class="sxs-lookup"><span data-stu-id="2d941-160">Thus, *Command* does not need to be 0 if you are setting print job parameters, although it can be.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d941-161">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d941-161">Return value</span></span>

<span data-ttu-id="2d941-162">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2d941-162">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="2d941-163">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="2d941-163">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d941-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d941-164">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2d941-165">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2d941-165">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="2d941-166">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="2d941-166">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="2d941-167">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="2d941-167">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="2d941-168">Mit der **setjob** -Funktion können Sie verschiedene Druckauftrags Parameter festlegen, indem Sie einen Zeiger auf die Struktur " [**Job \_ Info \_ 1**](job-info-1.md)", " [**Job \_ Info \_ 2**](job-info-2.md)", " [**Job \_ Info \_ 3**](job-info-3.md)" oder " [**Job \_ Info \_ 4**](job-info-4.md) " bereitstellen, die die erforderlichen Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="2d941-168">You can use the **SetJob** function to set various print job parameters by supplying a pointer to a [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), [**JOB\_INFO\_3**](job-info-3.md), or [**JOB\_INFO\_4**](job-info-4.md) structure that contains the necessary data.</span></span>

<span data-ttu-id="2d941-169">Wenn Sie alle Druckaufträge für einen bestimmten Drucker entfernen oder löschen möchten, müssen Sie die Funktion [**SetPrinter**](setprinter.md) aufrufen, wobei der *Befehls* Parameter auf Löschung der **Drucker \_ Steuerung \_** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2d941-169">To remove or delete all of the print jobs for a particular printer, call the [**SetPrinter**](setprinter.md) function with its *Command* parameter set to **PRINTER\_CONTROL\_PURGE**.</span></span>

<span data-ttu-id="2d941-170">Die folgenden Member der Struktur [**Auftrags \_ Informationen \_ 1**](job-info-1.md), [**Job \_ Info \_ 2**](job-info-2.md)oder [**Job \_ Info \_ 4**](job-info-4.md) werden bei einem Aufruf von **setjob** ignoriert: **JobID**, **pprintername**, **pmachinename**, **pusername**, **pdrivername**, **size**, **Submitted**, **time** und **TotalPages**.</span><span class="sxs-lookup"><span data-stu-id="2d941-170">The following members of a [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_4**](job-info-4.md) structure are ignored on a call to **SetJob**: **JobId**, **pPrinterName**, **pMachineName**, **pUserName**, **pDrivername**, **Size**, **Submitted**, **Time**, and **TotalPages**.</span></span>

<span data-ttu-id="2d941-171">Um die Position eines Druckauftrags in der Druck Warteschlange zu ändern, müssen Sie über die Zugriffsberechtigung " **Drucker \_ Zugriff \_ Verwalten** " verfügen.</span><span class="sxs-lookup"><span data-stu-id="2d941-171">You must have **PRINTER\_ACCESS\_ADMINISTER** access permission for a printer in order to change a print job's position in the print queue.</span></span>

<span data-ttu-id="2d941-172">Wenn Sie die Position eines Druckauftrags nicht in der Druck Warteschlange festlegen möchten, sollten Sie das **Positions** Element der Struktur [**Auftrags \_ Informationen \_ 1**](job-info-1.md), [**Auftrags \_ Informationen \_ 2**](job-info-2.md)oder [**Auftrags \_ Info \_ 4**](job-info-4.md) auf die **Auftrags Position nicht \_ \_ angegeben** festlegen.</span><span class="sxs-lookup"><span data-stu-id="2d941-172">If you do not want to set a print job's position in the print queue, you should set the **Position** member of the [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_4**](job-info-4.md) structure to **JOB\_POSITION\_UNSPECIFIED**.</span></span>

<span data-ttu-id="2d941-173">Verwenden Sie die **setjob** -Funktion mit der [**Auftrags \_ Info \_ 3**](job-info-3.md) -Struktur, um einen Satz von Druckaufträgen (auch als Kette bezeichnet) zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="2d941-173">Use the **SetJob** function with the [**JOB\_INFO\_3**](job-info-3.md) structure to link together a set of print jobs (also known as a chain).</span></span> <span data-ttu-id="2d941-174">Dies ist in Situationen nützlich, in denen ein einzelnes Dokument aus mehreren Teilen besteht, die Sie separat Rendering möchten.</span><span class="sxs-lookup"><span data-stu-id="2d941-174">This is useful in situations where a single document consists of several parts that you want to render separately.</span></span> <span data-ttu-id="2d941-175">Um die Aufträge A, b, c und D in der richtigen Reihenfolge zu drucken, nennen Sie **setjob** mit [**Auftrags \_ Info \_ 4**](job-info-4.md) , um A mit b, b mit c und c bis D zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="2d941-175">To print jobs A, B, C, and D in order, call **SetJob** with [**JOB\_INFO\_4**](job-info-4.md) to link A to B, B to C, and C to D.</span></span>

<span data-ttu-id="2d941-176">Beachten Sie beim Verknüpfen von Druckaufträgen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2d941-176">If you link print jobs, note the following:</span></span>

-   <span data-ttu-id="2d941-177">Aufträge können am Anfang oder Ende einer Kette hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2d941-177">Jobs can be added to the beginning or end of a chain.</span></span>
-   <span data-ttu-id="2d941-178">Alle Aufträge in der Kette müssen denselben Datentyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2d941-178">All jobs in the chain must have the same data type.</span></span>
-   <span data-ttu-id="2d941-179">Die Kette muss vollständig verknüpft sein, bevor der Spoolvorgang beginnt. andernfalls kann der Spooler Spoolaufträge drucken und löschen, bevor Sie alle verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="2d941-179">The chain must be completely linked before spooling begins, otherwise the spooler may print and delete spooled jobs before you link them all.</span></span> <span data-ttu-id="2d941-180">Es gibt zwei Möglichkeiten, den Druck von der Kette vorzeitig zu halten:</span><span class="sxs-lookup"><span data-stu-id="2d941-180">There are two ways to keep the chain from printing prematurely:</span></span>

    -   <span data-ttu-id="2d941-181">Hält den ersten Auftrag in der Kette an, bis die Kette vollständig verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="2d941-181">Pause the first job in the chain until the chain is completely linked.</span></span> <span data-ttu-id="2d941-182">Der angehaltene Status des ersten Auftrags steuert den Status aller Aufträge in der Kette.</span><span class="sxs-lookup"><span data-stu-id="2d941-182">The paused state of the first job governs the state of all jobs in the chain.</span></span>
    -   <span data-ttu-id="2d941-183">Lassen Sie den ersten Auftrag unvollständig, d. h., Sie dürfen [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) oder [**schedulejob**](schedulejob.md) nicht für den ersten Auftrag aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="2d941-183">Keep the first job incomplete, that is, do not call [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) or [**ScheduleJob**](schedulejob.md) for the first job.</span></span> <span data-ttu-id="2d941-184">Wenn jedoch ' Drucken beim Spoolvorgang ' aktiviert ist (Standardeinstellung), blockiert diese Methode den Port, während die Kette erstellt wird. Dadurch wird auch das Drucken nicht verknüpfter Aufträge verhindert.</span><span class="sxs-lookup"><span data-stu-id="2d941-184">However, if 'print while spooling' is enabled (the default), this method blocks the port while the chain is built, which also prevents the printing of non-related jobs.</span></span>

-   <span data-ttu-id="2d941-185">Die Anwendung muss den Fall behandeln, in dem der Benutzer einen Auftrag in der Kette löscht, bevor der Druck der Kette abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2d941-185">The application must handle the case where the user deletes a job in the chain before the chain finishes printing.</span></span> <span data-ttu-id="2d941-186">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen **ungültigen \_ Parameter** zurück, wenn keine JobID vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2d941-186">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **INVALID\_PARAMETER** when a JobID does not exist.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d941-187">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d941-187">Requirements</span></span>



| <span data-ttu-id="2d941-188">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d941-188">Requirement</span></span> | <span data-ttu-id="2d941-189">Wert</span><span class="sxs-lookup"><span data-stu-id="2d941-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d941-190">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d941-190">Minimum supported client</span></span><br/> | <span data-ttu-id="2d941-191">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d941-191">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2d941-192">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d941-192">Minimum supported server</span></span><br/> | <span data-ttu-id="2d941-193">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d941-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2d941-194">Header</span><span class="sxs-lookup"><span data-stu-id="2d941-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d941-195"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d941-195"><dt>WinSpool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2d941-196">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2d941-196">Library</span></span><br/>                  | <dl> <span data-ttu-id="2d941-197"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d941-197"><dt>WinSpool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="2d941-198">DLL</span><span class="sxs-lookup"><span data-stu-id="2d941-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d941-199"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="2d941-199"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="2d941-200">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="2d941-200">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2d941-201">**Setjobw** (Unicode) und **setjoba** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2d941-201">**SetJobW** (Unicode) and **SetJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="2d941-202">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d941-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d941-203">Drucken</span><span class="sxs-lookup"><span data-stu-id="2d941-203">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2d941-204">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="2d941-204">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="2d941-205">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="2d941-205">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="2d941-206">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="2d941-206">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="2d941-207">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="2d941-207">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="2d941-208">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="2d941-208">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="2d941-209">**Auftrags \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="2d941-209">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="2d941-210">**Auftrags \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="2d941-210">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="2d941-211">**Auftrags \_ Informationen \_ 3**</span><span class="sxs-lookup"><span data-stu-id="2d941-211">**JOB\_INFO\_3**</span></span>](job-info-3.md)
</dt> <dt>

[<span data-ttu-id="2d941-212">**Auftrags \_ Informationen \_ 4**</span><span class="sxs-lookup"><span data-stu-id="2d941-212">**JOB\_INFO\_4**</span></span>](job-info-4.md)
</dt> </dl>

 

