---
description: Beschreibt einen vollständigen Satz von Werten, die einem Auftrag zugeordnet sind, und unterstützt große Spooldateien mit Größen, ausgedrückt mit 64 Bits.
ms.assetid: 90932ae2-ea9e-43bc-9a1d-c68223f6d0ee
title: JOB_INFO_4 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_4
- _JOB_INFO_4A
- _JOB_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 5a6ccd7bf589ed341c9aceab86205cd9852c0896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351547"
---
# <a name="job_info_4-structure"></a><span data-ttu-id="099f6-103">Auftrags \_ Info \_ 4-Struktur</span><span class="sxs-lookup"><span data-stu-id="099f6-103">JOB\_INFO\_4 structure</span></span>

<span data-ttu-id="099f6-104">Beschreibt einen vollständigen Satz von Werten, die einem Auftrag zugeordnet sind, und unterstützt große Spooldateien mit Größen, ausgedrückt mit 64 Bits.</span><span class="sxs-lookup"><span data-stu-id="099f6-104">Describes a full set of values associated with a job and supports large spool files with sizes expressed with 64 bits.</span></span>

## <a name="syntax"></a><span data-ttu-id="099f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="099f6-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_4 {
  DWORD                JobId;
  LPTSTR               pPrinterName;
  LPTSTR               pMachineName;
  LPTSTR               pUserName;
  LPTSTR               pDocument;
  LPTSTR               pNotifyName;
  LPTSTR               pDatatype;
  LPTSTR               pPrintProcessor;
  LPTSTR               pParameters;
  LPTSTR               pDriverName;
  LPDEVMODE            pDevMode;
  LPTSTR               pStatus;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Status;
  DWORD                Priority;
  DWORD                Position;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                TotalPages;
  DWORD                Size;
  SYSTEMTIME           Submitted;
  DWORD                Time;
  DWORD                PagesPrinted;
  LONG                 SizeHigh;
} JOB_INFO_4, *PJOB_INFO_4;
```



## <a name="members"></a><span data-ttu-id="099f6-106">Member</span><span class="sxs-lookup"><span data-stu-id="099f6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="099f6-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="099f6-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-108">Ein Auftrags Bezeichnerwert.</span><span class="sxs-lookup"><span data-stu-id="099f6-108">A job identifier value.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-109">**pprintername**</span><span class="sxs-lookup"><span data-stu-id="099f6-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-110">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckers angibt, für den der Auftrag gespoolkt ist.</span><span class="sxs-lookup"><span data-stu-id="099f6-110">A pointer to a null-terminated string that specifies the name of the printer for which the job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-111">**pmachinename**</span><span class="sxs-lookup"><span data-stu-id="099f6-111">**pMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-112">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Computers angibt, der den Druckauftrag erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="099f6-112">A pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-113">**pusername**</span><span class="sxs-lookup"><span data-stu-id="099f6-113">**pUserName**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-114">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Benutzers angibt, der den Druckauftrag besitzt.</span><span class="sxs-lookup"><span data-stu-id="099f6-114">A pointer to a null-terminated string that specifies the name of the user who owns the print job.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-115">**pdocument**</span><span class="sxs-lookup"><span data-stu-id="099f6-115">**pDocument**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-116">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckauftrags angibt (z. b. "MS-Word: Review.doc").</span><span class="sxs-lookup"><span data-stu-id="099f6-116">A pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>

</dd> <dt>

<span data-ttu-id="099f6-117">**pnotifyname**</span><span class="sxs-lookup"><span data-stu-id="099f6-117">**pNotifyName**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-118">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Benutzers angibt, der benachrichtigt werden soll, wenn der Auftrag gedruckt wurde, oder wenn beim Drucken des Auftrags ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="099f6-118">A pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed, or when an error occurs while printing the job.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-119">**pdatatype**</span><span class="sxs-lookup"><span data-stu-id="099f6-119">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-120">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp angibt, der zum Aufzeichnen des Druckauftrags verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="099f6-120">A pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-121">**pprintprocessor**</span><span class="sxs-lookup"><span data-stu-id="099f6-121">**pPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-122">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Druck Prozessors angibt, der zum Drucken des Auftrags verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="099f6-122">A pointer to a null-terminated string that specifies the name of the print processor that should be used to print the job.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-123">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="099f6-123">**pParameters**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-124">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die Druck Prozessor Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="099f6-124">A pointer to a null-terminated string that specifies print-processor parameters.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-125">**pdrivername**</span><span class="sxs-lookup"><span data-stu-id="099f6-125">**pDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-126">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Druckertreibers angibt, der zum Verarbeiten des Druckauftrags verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="099f6-126">A pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-127">**pdevmode**</span><span class="sxs-lookup"><span data-stu-id="099f6-127">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-128">Ein Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die die Geräte Initialisierungs-und Umgebungs Daten für den Druckertreiber enthält.</span><span class="sxs-lookup"><span data-stu-id="099f6-128">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains device-initialization and environment data for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-129">**pstatus**</span><span class="sxs-lookup"><span data-stu-id="099f6-129">**pStatus**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-130">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Status des Druckauftrags angibt.</span><span class="sxs-lookup"><span data-stu-id="099f6-130">A pointer to a null-terminated string that specifies the status of the print job.</span></span> <span data-ttu-id="099f6-131">Dieser Member sollte vor dem **Status** geprüft werden, und wenn **pstatus** den Wert **null** hat, wird der Status durch den Inhalt des statusmembers definiert.</span><span class="sxs-lookup"><span data-stu-id="099f6-131">This member should be checked prior to **Status** and, if **pStatus** is **NULL**, the status is defined by the contents of the Status member.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-132">**psecuritydescriptor**</span><span class="sxs-lookup"><span data-stu-id="099f6-132">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-133">Der Wert dieses Members ist **null**.</span><span class="sxs-lookup"><span data-stu-id="099f6-133">The value of this member is **NULL**.</span></span> <span data-ttu-id="099f6-134">Das Abrufen und Festlegen von Dokument Sicherheits Deskriptoren wird in dieser Version nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="099f6-134">Retrieval and setting of document security descriptors is not supported in this release.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-135">**Status**</span><span class="sxs-lookup"><span data-stu-id="099f6-135">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-136">Der Status des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="099f6-136">The job status.</span></span> <span data-ttu-id="099f6-137">Dieser Member kann einen oder mehrere der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="099f6-137">This member can be one or more of the following values:</span></span>

| <span data-ttu-id="099f6-138">Wert</span><span class="sxs-lookup"><span data-stu-id="099f6-138">Value</span></span>                           | <span data-ttu-id="099f6-139">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="099f6-139">Meaning</span></span>                                                      |
|---------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="099f6-140">der Auftrags \_ Status ist \_ blockiert \_ devq.</span><span class="sxs-lookup"><span data-stu-id="099f6-140">JOB\_STATUS\_BLOCKED\_DEVQ</span></span>      | <span data-ttu-id="099f6-141">Der Treiber kann den Auftrag nicht drucken.</span><span class="sxs-lookup"><span data-stu-id="099f6-141">The driver cannot print the job.</span></span>                             |
| <span data-ttu-id="099f6-142">Auftrags \_ Status \_ gelöscht</span><span class="sxs-lookup"><span data-stu-id="099f6-142">JOB\_STATUS\_DELETED</span></span>            | <span data-ttu-id="099f6-143">Der Auftrag wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="099f6-143">Job has been deleted.</span></span>                                        |
| <span data-ttu-id="099f6-144">Auftrags \_ Status wird \_ gelöscht</span><span class="sxs-lookup"><span data-stu-id="099f6-144">JOB\_STATUS\_DELETING</span></span>           | <span data-ttu-id="099f6-145">Der Auftrag wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="099f6-145">Job is being deleted.</span></span>                                        |
| <span data-ttu-id="099f6-146">Auftrags \_ Status \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="099f6-146">JOB\_STATUS\_ERROR</span></span>              | <span data-ttu-id="099f6-147">Dem Auftrag ist ein Fehler zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="099f6-147">An error is associated with the job.</span></span>                         |
| <span data-ttu-id="099f6-148">Auftrags \_ Status \_ Offline</span><span class="sxs-lookup"><span data-stu-id="099f6-148">JOB\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="099f6-149">Der Drucker ist offline.</span><span class="sxs-lookup"><span data-stu-id="099f6-149">Printer is offline.</span></span>                                          |
| <span data-ttu-id="099f6-150">Ausgabe des Auftrags \_ Status \_</span><span class="sxs-lookup"><span data-stu-id="099f6-150">JOB\_STATUS\_PAPEROUT</span></span>           | <span data-ttu-id="099f6-151">Der Drucker ist nicht mehr im Papier.</span><span class="sxs-lookup"><span data-stu-id="099f6-151">Printer is out of paper.</span></span>                                     |
| <span data-ttu-id="099f6-152">Auftrags \_ Status \_ angehalten</span><span class="sxs-lookup"><span data-stu-id="099f6-152">JOB\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="099f6-153">Der Auftrag wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="099f6-153">Job is paused.</span></span>                                               |
| <span data-ttu-id="099f6-154">Auftrags \_ Status \_ gedruckt</span><span class="sxs-lookup"><span data-stu-id="099f6-154">JOB\_STATUS\_PRINTED</span></span>            | <span data-ttu-id="099f6-155">Der Auftrag hat gedruckt.</span><span class="sxs-lookup"><span data-stu-id="099f6-155">Job has printed.</span></span>                                             |
| <span data-ttu-id="099f6-156">Drucken von Auftrags \_ Status \_</span><span class="sxs-lookup"><span data-stu-id="099f6-156">JOB\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="099f6-157">Der Auftrag wird gedruckt.</span><span class="sxs-lookup"><span data-stu-id="099f6-157">Job is printing.</span></span>                                             |
| <span data-ttu-id="099f6-158">Auftrags \_ Status \_ neu starten</span><span class="sxs-lookup"><span data-stu-id="099f6-158">JOB\_STATUS\_RESTART</span></span>            | <span data-ttu-id="099f6-159">Der Auftrag wurde neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="099f6-159">Job has been restarted.</span></span>                                      |
| <span data-ttu-id="099f6-160">Auftrags \_ Status \_ Spoolvorgang</span><span class="sxs-lookup"><span data-stu-id="099f6-160">JOB\_STATUS\_SPOOLING</span></span>           | <span data-ttu-id="099f6-161">Auftrag ist Spoolvorgang.</span><span class="sxs-lookup"><span data-stu-id="099f6-161">Job is spooling.</span></span>                                             |
| <span data-ttu-id="099f6-162">Auftrags \_ Status \_ Benutzer \_ Eingriff</span><span class="sxs-lookup"><span data-stu-id="099f6-162">JOB\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="099f6-163">Der Drucker weist einen Fehler auf, der erfordert, dass der Benutzer etwas tut.</span><span class="sxs-lookup"><span data-stu-id="099f6-163">Printer has an error that requires the user to do something.</span></span> |



 

<span data-ttu-id="099f6-164">In Windows XP und höheren Versionen von Windows können auch die folgenden Werte verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="099f6-164">In Windows XP and later versions of Windows, the following values can also be used:</span></span>

| <span data-ttu-id="099f6-165">Wert</span><span class="sxs-lookup"><span data-stu-id="099f6-165">Value</span></span>                 | <span data-ttu-id="099f6-166">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="099f6-166">Meaning</span></span>                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="099f6-167">Auftrags \_ Status ist \_ fertiggestellt</span><span class="sxs-lookup"><span data-stu-id="099f6-167">JOB\_STATUS\_COMPLETE</span></span> | <span data-ttu-id="099f6-168">Der Auftrag wird an den Drucker gesendet, aber möglicherweise noch nicht gedruckt.</span><span class="sxs-lookup"><span data-stu-id="099f6-168">The job is sent to the printer, but may not be printed yet.</span></span> <span data-ttu-id="099f6-169">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="099f6-169">See Remarks for more information.</span></span> |
| <span data-ttu-id="099f6-170">Auftrags \_ Status \_ beibehalten</span><span class="sxs-lookup"><span data-stu-id="099f6-170">JOB\_STATUS\_RETAINED</span></span> | <span data-ttu-id="099f6-171">Der Auftrag wurde nach dem Drucken in der Druck Warteschlange beibehalten.</span><span class="sxs-lookup"><span data-stu-id="099f6-171">The job has been retained in the print queue following printing.</span></span>                              |



 

</dd> <dt>

<span data-ttu-id="099f6-172">**Priority**</span><span class="sxs-lookup"><span data-stu-id="099f6-172">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-173">Die Auftrags Priorität.</span><span class="sxs-lookup"><span data-stu-id="099f6-173">The job priority.</span></span> <span data-ttu-id="099f6-174">Bei diesem Element kann es sich um einen der folgenden Werte oder um einen Bereich zwischen 1 und 99 (minimale \_ Priorität bis Max \_ . Priorität) handeln.</span><span class="sxs-lookup"><span data-stu-id="099f6-174">This member can be one of the following values, or in the range between 1 through 99 (MIN\_PRIORITY through MAX\_PRIORITY).</span></span>



| <span data-ttu-id="099f6-175">Wert</span><span class="sxs-lookup"><span data-stu-id="099f6-175">Value</span></span>         | <span data-ttu-id="099f6-176">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="099f6-176">Meaning</span></span>           |
|---------------|-------------------|
| <span data-ttu-id="099f6-177">minimale \_ Priorität</span><span class="sxs-lookup"><span data-stu-id="099f6-177">MIN\_PRIORITY</span></span> | <span data-ttu-id="099f6-178">Minimale Priorität.</span><span class="sxs-lookup"><span data-stu-id="099f6-178">Minimum priority.</span></span> |
| <span data-ttu-id="099f6-179">maximale \_ Priorität</span><span class="sxs-lookup"><span data-stu-id="099f6-179">MAX\_PRIORITY</span></span> | <span data-ttu-id="099f6-180">Maximale Priorität.</span><span class="sxs-lookup"><span data-stu-id="099f6-180">Maximum priority.</span></span> |
| <span data-ttu-id="099f6-181">DEF- \_ Priorität</span><span class="sxs-lookup"><span data-stu-id="099f6-181">DEF\_PRIORITY</span></span> | <span data-ttu-id="099f6-182">Standardpriorität.</span><span class="sxs-lookup"><span data-stu-id="099f6-182">Default priority.</span></span> |



 

</dd> <dt>

<span data-ttu-id="099f6-183">**Position**</span><span class="sxs-lookup"><span data-stu-id="099f6-183">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-184">Die Position des Auftrags in der Druck Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="099f6-184">The job's position in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-185">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="099f6-185">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-186">Der früheste Zeitpunkt, an dem der Auftrag gedruckt werden kann.</span><span class="sxs-lookup"><span data-stu-id="099f6-186">The earliest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-187">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="099f6-187">**UntilTime**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-188">Der letzte Zeitpunkt, zu dem der Auftrag gedruckt werden kann.</span><span class="sxs-lookup"><span data-stu-id="099f6-188">The latest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-189">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="099f6-189">**TotalPages**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-190">Die Anzahl der Seiten, die für den Auftrag benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="099f6-190">The number of pages required for the job.</span></span> <span data-ttu-id="099f6-191">Dieser Wert kann NULL sein, wenn der Druckauftrag keine Seiten Begrenzungs Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="099f6-191">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-192">**Größe**</span><span class="sxs-lookup"><span data-stu-id="099f6-192">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-193">Die unteren vier Bytes der Größe (in Bytes) des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="099f6-193">The lower four bytes of the size, in bytes, of the job.</span></span> <span data-ttu-id="099f6-194">Siehe auch das **sizehigh** -Member weiter unten.</span><span class="sxs-lookup"><span data-stu-id="099f6-194">See also the **SizeHigh** member below.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-195">**Gesendet**</span><span class="sxs-lookup"><span data-stu-id="099f6-195">**Submitted**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-196">Eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die die Uhrzeit angibt, zu der der Auftrag übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="099f6-196">A [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time when the job was submitted.</span></span>

<span data-ttu-id="099f6-197">Dieser Zeitwert liegt im UTC-Format (Universal Time Koordinate) vor.</span><span class="sxs-lookup"><span data-stu-id="099f6-197">This time value is in Universal Time Coordinate (UTC) format.</span></span> <span data-ttu-id="099f6-198">Sie sollten Sie in einen lokalen Uhrzeitwert konvertieren, bevor Sie Sie anzeigen.</span><span class="sxs-lookup"><span data-stu-id="099f6-198">You should convert it to a local time value before displaying it.</span></span> <span data-ttu-id="099f6-199">Sie können die [**filetimetolocalfiletime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) -Funktion verwenden, um die Konvertierung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="099f6-199">You can use the [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) function to perform the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-200">**Time**</span><span class="sxs-lookup"><span data-stu-id="099f6-200">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-201">Die Gesamtzeit in Millisekunden, die seit dem Drucken des Auftrags verstrichen ist.</span><span class="sxs-lookup"><span data-stu-id="099f6-201">The total time, in milliseconds, that has elapsed since the job began printing.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-202">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="099f6-202">**PagesPrinted**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-203">Die Anzahl der Seiten, die gedruckt wurden.</span><span class="sxs-lookup"><span data-stu-id="099f6-203">The number of pages that have printed.</span></span> <span data-ttu-id="099f6-204">Dieser Wert kann NULL sein, wenn der Druckauftrag keine Seiten Begrenzungs Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="099f6-204">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="099f6-205">**Sizehigh**</span><span class="sxs-lookup"><span data-stu-id="099f6-205">**SizeHigh**</span></span>
</dt> <dd>

<span data-ttu-id="099f6-206">Die höheren vier Bytes der Größe (in Bytes) des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="099f6-206">The higher four bytes of the size, in bytes, of the job.</span></span> <span data-ttu-id="099f6-207">Siehe auch das **Größen** Element oben.</span><span class="sxs-lookup"><span data-stu-id="099f6-207">See also the **Size** member above.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="099f6-208">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="099f6-208">Remarks</span></span>

<span data-ttu-id="099f6-209">Port Monitore, die trueendofjob nicht unterstützen, legen den Auftrag als Auftrags Status fest, wenn \_ \_ der Auftrag an den Drucker gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="099f6-209">Port monitors that do not support TrueEndOfJob will set the job as JOB\_STATUS\_PRINTED immediately after the job is submitted to the printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="099f6-210">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="099f6-210">Requirements</span></span>



| <span data-ttu-id="099f6-211">Anforderung</span><span class="sxs-lookup"><span data-stu-id="099f6-211">Requirement</span></span> | <span data-ttu-id="099f6-212">Wert</span><span class="sxs-lookup"><span data-stu-id="099f6-212">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="099f6-213">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="099f6-213">Minimum supported client</span></span><br/> | <span data-ttu-id="099f6-214">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="099f6-214">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="099f6-215">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="099f6-215">Minimum supported server</span></span><br/> | <span data-ttu-id="099f6-216">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="099f6-216">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="099f6-217">Header</span><span class="sxs-lookup"><span data-stu-id="099f6-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="099f6-218"><dt>Winspool. h</dt></span><span class="sxs-lookup"><span data-stu-id="099f6-218"><dt>Winspool.h</dt></span></span> </dl> |
| <span data-ttu-id="099f6-219">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="099f6-219">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="099f6-220">**\_ Auftrags \_ Info \_ 4W** (Unicode) und **\_ Auftrags \_ Info \_ 4a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="099f6-220">**\_JOB\_INFO\_4W** (Unicode) and **\_JOB\_INFO\_4A** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="099f6-221">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="099f6-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="099f6-222">Drucken</span><span class="sxs-lookup"><span data-stu-id="099f6-222">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="099f6-223">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="099f6-223">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="099f6-224">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="099f6-224">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="099f6-225">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="099f6-225">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="099f6-226">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="099f6-226">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="099f6-227">**Setjob**</span><span class="sxs-lookup"><span data-stu-id="099f6-227">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

