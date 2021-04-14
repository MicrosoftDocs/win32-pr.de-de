---
description: Die Struktur der Auftrags \_ Informationen \_ 1 gibt Druckauftrags Informationen an, z. b. den Wert des Auftrags Bezeichners, den Namen des Druckers, für den der Auftrag gespoolte ist, den Namen des Computers, der den Druckauftrag erstellt hat, den Namen des Benutzers, der den Druckauftrag besitzt, usw.
ms.assetid: d42ada89-6bc7-4006-81d9-dbcc0347edd3
title: JOB_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_1
- _JOB_INFO_1A
- _JOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d56d4d6bce15a661ce141d8e22d27a15837a9f6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349079"
---
# <a name="job_info_1-structure"></a><span data-ttu-id="2178f-103">Struktur von Auftrags \_ Informationen \_ 1</span><span class="sxs-lookup"><span data-stu-id="2178f-103">JOB\_INFO\_1 structure</span></span>

<span data-ttu-id="2178f-104">Die Struktur der **Auftrags \_ Informationen \_ 1** gibt Druckauftrags Informationen an, z. b. den Wert des Auftrags Bezeichners, den Namen des Druckers, für den der Auftrag gespoolte ist, den Namen des Computers, der den Druckauftrag erstellt hat, den Namen des Benutzers, der den Druckauftrag besitzt, usw.</span><span class="sxs-lookup"><span data-stu-id="2178f-104">The **JOB\_INFO\_1** structure specifies print-job information such as the job-identifier value, the name of the printer for which the job is spooled, the name of the machine that created the print job, the name of the user that owns the print job, and so on.</span></span>

## <a name="syntax"></a><span data-ttu-id="2178f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2178f-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_1 {
  DWORD      JobId;
  LPTSTR     pPrinterName;
  LPTSTR     pMachineName;
  LPTSTR     pUserName;
  LPTSTR     pDocument;
  LPTSTR     pDatatype;
  LPTSTR     pStatus;
  DWORD      Status;
  DWORD      Priority;
  DWORD      Position;
  DWORD      TotalPages;
  DWORD      PagesPrinted;
  SYSTEMTIME Submitted;
} JOB_INFO_1, *PJOB_INFO_1;
```



## <a name="members"></a><span data-ttu-id="2178f-106">Member</span><span class="sxs-lookup"><span data-stu-id="2178f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2178f-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="2178f-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="2178f-108">Ein Auftrags Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="2178f-108">A job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="2178f-109">**pprintername**</span><span class="sxs-lookup"><span data-stu-id="2178f-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="2178f-110">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckers angibt, für den der Auftrag gespoolkt ist.</span><span class="sxs-lookup"><span data-stu-id="2178f-110">A pointer to a null-terminated string that specifies the name of the printer for which the job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="2178f-111">**pmachinename**</span><span class="sxs-lookup"><span data-stu-id="2178f-111">**pMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="2178f-112">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Computers angibt, der den Druckauftrag erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="2178f-112">A pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>

</dd> <dt>

<span data-ttu-id="2178f-113">**pusername**</span><span class="sxs-lookup"><span data-stu-id="2178f-113">**pUserName**</span></span>
</dt> <dd>

<span data-ttu-id="2178f-114">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Benutzers angibt, der Besitzer des Druckauftrags ist.</span><span class="sxs-lookup"><span data-stu-id="2178f-114">A pointer to a null-terminated string that specifies the name of the user that owns the print job.</span></span>

</dd> <dt>

<span data-ttu-id="2178f-115">**pdocument**</span><span class="sxs-lookup"><span data-stu-id="2178f-115">**pDocument**</span></span>
</dt> <dd>

<span data-ttu-id="2178f-116">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckauftrags angibt (z. b. "MS-Word: Review.doc").</span><span class="sxs-lookup"><span data-stu-id="2178f-116">A pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>

</dd> <dt>

<span data-ttu-id="2178f-117">**pdatatype**</span><span class="sxs-lookup"><span data-stu-id="2178f-117">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="2178f-118">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp angibt, der zum Aufzeichnen des Druckauftrags verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2178f-118">A pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>

</dd> <dt>

<span data-ttu-id="2178f-119">**pstatus**</span><span class="sxs-lookup"><span data-stu-id="2178f-119">**pStatus**</span></span>
</dt> <dd>

<span data-ttu-id="2178f-120">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Status des Druckauftrags angibt.</span><span class="sxs-lookup"><span data-stu-id="2178f-120">A pointer to a null-terminated string that specifies the status of the print job.</span></span> <span data-ttu-id="2178f-121">Dieser Member sollte vor dem *Status* geprüft werden, und wenn *pstatus* den Wert **null** hat, wird der Status durch den Inhalt des statusmembers definiert.</span><span class="sxs-lookup"><span data-stu-id="2178f-121">This member should be checked prior to *Status* and, if *pStatus* is **NULL**, the status is defined by the contents of the Status member.</span></span>

</dd> <dt>

<span data-ttu-id="2178f-122">**Status**</span><span class="sxs-lookup"><span data-stu-id="2178f-122">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="2178f-123">Der Status des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="2178f-123">The job status.</span></span> <span data-ttu-id="2178f-124">Der Wert dieses Members kann 0 (null) oder eine Kombination aus einem oder mehreren der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="2178f-124">The value of this member can be zero or a combination of one or more of the following values.</span></span> <span data-ttu-id="2178f-125">Der Wert 0 (null) gibt an, dass die Druck Warteschlange angehalten wurde, nachdem das Spoolvorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="2178f-125">A value of zero indicates that the print queue was paused after the document finished spooling.</span></span>



| <span data-ttu-id="2178f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2178f-126">Value</span></span>                           | <span data-ttu-id="2178f-127">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2178f-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2178f-128">der Auftrags \_ Status ist \_ blockiert \_ devq.</span><span class="sxs-lookup"><span data-stu-id="2178f-128">JOB\_STATUS\_BLOCKED\_DEVQ</span></span>      | <span data-ttu-id="2178f-129">Der Treiber kann den Auftrag nicht drucken.</span><span class="sxs-lookup"><span data-stu-id="2178f-129">The driver cannot print the job.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="2178f-130">Auftrags \_ Status ist \_ fertiggestellt</span><span class="sxs-lookup"><span data-stu-id="2178f-130">JOB\_STATUS\_COMPLETE</span></span>           | <span data-ttu-id="2178f-131">**Windows XP und höher:** Der Auftrag wird an den Drucker gesendet, aber der Auftrag wurde möglicherweise noch nicht gedruckt.</span><span class="sxs-lookup"><span data-stu-id="2178f-131">**Windows XP and later:** Job is sent to the printer, but the job may not be printed yet.</span></span><br/> <span data-ttu-id="2178f-132">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="2178f-132">See Remarks for more information.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="2178f-133">Auftrags \_ Status \_ gelöscht</span><span class="sxs-lookup"><span data-stu-id="2178f-133">JOB\_STATUS\_DELETED</span></span>            | <span data-ttu-id="2178f-134">Der Auftrag wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2178f-134">Job has been deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="2178f-135">Auftrags \_ Status wird \_ gelöscht</span><span class="sxs-lookup"><span data-stu-id="2178f-135">JOB\_STATUS\_DELETING</span></span>           | <span data-ttu-id="2178f-136">Der Auftrag wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2178f-136">Job is being deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="2178f-137">Auftrags \_ Status \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="2178f-137">JOB\_STATUS\_ERROR</span></span>              | <span data-ttu-id="2178f-138">Dem Auftrag ist ein Fehler zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2178f-138">An error is associated with the job.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="2178f-139">Auftrags \_ Status \_ Offline</span><span class="sxs-lookup"><span data-stu-id="2178f-139">JOB\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="2178f-140">Der Drucker ist offline.</span><span class="sxs-lookup"><span data-stu-id="2178f-140">Printer is offline.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="2178f-141">Ausgabe des Auftrags \_ Status \_</span><span class="sxs-lookup"><span data-stu-id="2178f-141">JOB\_STATUS\_PAPEROUT</span></span>           | <span data-ttu-id="2178f-142">Der Drucker ist nicht mehr im Papier.</span><span class="sxs-lookup"><span data-stu-id="2178f-142">Printer is out of paper.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="2178f-143">Auftrags \_ Status \_ angehalten</span><span class="sxs-lookup"><span data-stu-id="2178f-143">JOB\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="2178f-144">Der Auftrag wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="2178f-144">Job is paused.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="2178f-145">Auftrags \_ Status \_ gedruckt</span><span class="sxs-lookup"><span data-stu-id="2178f-145">JOB\_STATUS\_PRINTED</span></span>            | <span data-ttu-id="2178f-146">Der Auftrag hat gedruckt.</span><span class="sxs-lookup"><span data-stu-id="2178f-146">Job has printed.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="2178f-147">Drucken von Auftrags \_ Status \_</span><span class="sxs-lookup"><span data-stu-id="2178f-147">JOB\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="2178f-148">Der Auftrag wird gedruckt.</span><span class="sxs-lookup"><span data-stu-id="2178f-148">Job is printing.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="2178f-149">Auftrags \_ Status \_ neu starten</span><span class="sxs-lookup"><span data-stu-id="2178f-149">JOB\_STATUS\_RESTART</span></span>            | <span data-ttu-id="2178f-150">Der Auftrag wurde neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="2178f-150">Job has been restarted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="2178f-151">Auftrags \_ Status \_ beibehalten</span><span class="sxs-lookup"><span data-stu-id="2178f-151">JOB\_STATUS\_RETAINED</span></span>           | <span data-ttu-id="2178f-152">**Windows Vista und höher:** Der Auftrag wurde in der Druck Warteschlange beibehalten und kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="2178f-152">**Windows Vista and later:** Job has been retained in the print queue and cannot be deleted.</span></span> <span data-ttu-id="2178f-153">Dies kann folgende Ursachen haben:</span><span class="sxs-lookup"><span data-stu-id="2178f-153">This can be caused by the following:</span></span><br/> <span data-ttu-id="2178f-154">1) der Auftrag wurde manuell durch einen Aufrufen von setjob aufbewahrt, und der Spooler wartet auf die Freigabe des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="2178f-154">1) The job was manually retained by a call to SetJob and the spooler is waiting for the job to be released.</span></span><br/> <span data-ttu-id="2178f-155">2) der Auftrag wurde nicht beendet, und das Drucken muss abgeschlossen sein, bevor er automatisch gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="2178f-155">2) The job has not finished printing and must finish printing before it can be automatically deleted.</span></span><br/> <span data-ttu-id="2178f-156">Weitere Informationen zu Druckauftrags Befehlen finden Sie unter [**setjob**](setjob.md) .</span><span class="sxs-lookup"><span data-stu-id="2178f-156">See [**SetJob**](setjob.md) for more information about print job commands.</span></span><br/> |
| <span data-ttu-id="2178f-157">Auftrags \_ Status \_ Spoolvorgang</span><span class="sxs-lookup"><span data-stu-id="2178f-157">JOB\_STATUS\_SPOOLING</span></span>           | <span data-ttu-id="2178f-158">Auftrag ist Spoolvorgang.</span><span class="sxs-lookup"><span data-stu-id="2178f-158">Job is spooling.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="2178f-159">Auftrags \_ Status \_ Benutzer \_ Eingriff</span><span class="sxs-lookup"><span data-stu-id="2178f-159">JOB\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="2178f-160">Der Drucker weist einen Fehler auf, der erfordert, dass der Benutzer etwas tut.</span><span class="sxs-lookup"><span data-stu-id="2178f-160">Printer has an error that requires the user to do something.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="2178f-161">**Priority**</span><span class="sxs-lookup"><span data-stu-id="2178f-161">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="2178f-162">Die Auftrags Priorität.</span><span class="sxs-lookup"><span data-stu-id="2178f-162">The job priority.</span></span> <span data-ttu-id="2178f-163">Bei diesem Element kann es sich um einen der folgenden Werte oder im Bereich zwischen 1 und 99 (minimale \_ Priorität bis Max \_ . Priorität) handeln.</span><span class="sxs-lookup"><span data-stu-id="2178f-163">This member can be one of the following values or in the range between 1 through 99 (MIN\_PRIORITY through MAX\_PRIORITY).</span></span>



| <span data-ttu-id="2178f-164">Wert</span><span class="sxs-lookup"><span data-stu-id="2178f-164">Value</span></span>         | <span data-ttu-id="2178f-165">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2178f-165">Meaning</span></span>           |
|---------------|-------------------|
| <span data-ttu-id="2178f-166">minimale \_ Priorität</span><span class="sxs-lookup"><span data-stu-id="2178f-166">MIN\_PRIORITY</span></span> | <span data-ttu-id="2178f-167">Minimale Priorität.</span><span class="sxs-lookup"><span data-stu-id="2178f-167">Minimum priority.</span></span> |
| <span data-ttu-id="2178f-168">maximale \_ Priorität</span><span class="sxs-lookup"><span data-stu-id="2178f-168">MAX\_PRIORITY</span></span> | <span data-ttu-id="2178f-169">Maximale Priorität.</span><span class="sxs-lookup"><span data-stu-id="2178f-169">Maximum priority.</span></span> |
| <span data-ttu-id="2178f-170">DEF- \_ Priorität</span><span class="sxs-lookup"><span data-stu-id="2178f-170">DEF\_PRIORITY</span></span> | <span data-ttu-id="2178f-171">Standardpriorität.</span><span class="sxs-lookup"><span data-stu-id="2178f-171">Default priority.</span></span> |



 

</dd> <dt>

<span data-ttu-id="2178f-172">**Position**</span><span class="sxs-lookup"><span data-stu-id="2178f-172">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="2178f-173">Die Position des Auftrags in der Druck Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="2178f-173">The job's position in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="2178f-174">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="2178f-174">**TotalPages**</span></span>
</dt> <dd>

<span data-ttu-id="2178f-175">Die Gesamtanzahl der Seiten, die im Dokument enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="2178f-175">The total number of pages that the document contains.</span></span> <span data-ttu-id="2178f-176">Dieser Wert kann NULL sein, wenn der Druckauftrag keine Seiten Begrenzungs Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="2178f-176">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="2178f-177">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="2178f-177">**PagesPrinted**</span></span>
</dt> <dd>

<span data-ttu-id="2178f-178">Die Anzahl der Seiten, die gedruckt wurden.</span><span class="sxs-lookup"><span data-stu-id="2178f-178">The number of pages that have printed.</span></span> <span data-ttu-id="2178f-179">Dieser Wert kann NULL sein, wenn der Druckauftrag keine Seiten Begrenzungs Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="2178f-179">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="2178f-180">**Gesendet**</span><span class="sxs-lookup"><span data-stu-id="2178f-180">**Submitted**</span></span>
</dt> <dd>

<span data-ttu-id="2178f-181">Eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die die Uhrzeit angibt, zu der dieses Dokument spoolte.</span><span class="sxs-lookup"><span data-stu-id="2178f-181">A [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time that this document was spooled.</span></span>

<span data-ttu-id="2178f-182">Dieser Zeitwert liegt im UTC-Format (Universal Time Koordinate) vor.</span><span class="sxs-lookup"><span data-stu-id="2178f-182">This time value is in Universal Time Coordinate (UTC) format.</span></span> <span data-ttu-id="2178f-183">Sie sollten Sie in einen lokalen Uhrzeitwert konvertieren, bevor Sie Sie anzeigen.</span><span class="sxs-lookup"><span data-stu-id="2178f-183">You should convert it to a local time value before displaying it.</span></span> <span data-ttu-id="2178f-184">Sie können die [**filetimetolocalfiletime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) -Funktion verwenden, um die Konvertierung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2178f-184">You can use the [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) function to perform the conversion.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2178f-185">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2178f-185">Remarks</span></span>

<span data-ttu-id="2178f-186">Port Monitore, die trueendofjob nicht unterstützen, legen den Auftrag als Auftrags Status fest, \_ \_ nachdem der Auftrag an den Drucker gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="2178f-186">Port monitors that do not support TrueEndOfJob will set the job as JOB\_STATUS\_PRINTED right after the job is submitted to the printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2178f-187">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2178f-187">Requirements</span></span>



| <span data-ttu-id="2178f-188">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2178f-188">Requirement</span></span> | <span data-ttu-id="2178f-189">Wert</span><span class="sxs-lookup"><span data-stu-id="2178f-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2178f-190">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2178f-190">Minimum supported client</span></span><br/> | <span data-ttu-id="2178f-191">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2178f-191">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2178f-192">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2178f-192">Minimum supported server</span></span><br/> | <span data-ttu-id="2178f-193">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2178f-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2178f-194">Header</span><span class="sxs-lookup"><span data-stu-id="2178f-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="2178f-195"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2178f-195"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2178f-196">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="2178f-196">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2178f-197">**\_ Auftrags \_ Informationen \_ 1W** (Unicode) und **\_ Auftrags \_ Informationen \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2178f-197">**\_JOB\_INFO\_1W** (Unicode) and **\_JOB\_INFO\_1A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="2178f-198">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2178f-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2178f-199">Drucken</span><span class="sxs-lookup"><span data-stu-id="2178f-199">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2178f-200">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="2178f-200">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="2178f-201">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="2178f-201">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="2178f-202">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="2178f-202">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="2178f-203">**Setjob**</span><span class="sxs-lookup"><span data-stu-id="2178f-203">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

