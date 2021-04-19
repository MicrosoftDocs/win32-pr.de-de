---
description: Die Funktion SetPrinter legt die Daten für einen angegebenen Drucker fest oder legt den Zustand des angegebenen Druckers fest, indem der Druckvorgang angehalten, der Druck fortgesetzt oder alle Druckaufträge gelöscht werden.
ms.assetid: ade367c5-20d6-4da9-bb52-ce6768cf7537
title: SetPrinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinter
- SetPrinterA
- SetPrinterW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-printer-WinSpool-l1-1-0.dll
- Ext-MS-Win-printer-WinSpool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 5f2c58d97315ff108c8f12bd029849993a307025
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349978"
---
# <a name="setprinter-function"></a><span data-ttu-id="0e046-103">SetPrinter-Funktion</span><span class="sxs-lookup"><span data-stu-id="0e046-103">SetPrinter function</span></span>

<span data-ttu-id="0e046-104">Die Funktion **SetPrinter** legt die Daten für einen angegebenen Drucker fest oder legt den Zustand des angegebenen Druckers fest, indem der Druckvorgang angehalten, der Druck fortgesetzt oder alle Druckaufträge gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="0e046-104">The **SetPrinter** function sets the data for a specified printer or sets the state of the specified printer by pausing printing, resuming printing, or clearing all print jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e046-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e046-105">Syntax</span></span>


```C++
BOOL SetPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a><span data-ttu-id="0e046-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e046-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e046-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e046-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e046-108">Ein Handle für den Drucker.</span><span class="sxs-lookup"><span data-stu-id="0e046-108">A handle to the printer.</span></span> <span data-ttu-id="0e046-109">Verwenden Sie die Funktion " [**OpenPrinter**](openprinter.md)", " [**OpenPrinter2**](openprinter2.md)" oder " [**addprinter**](addprinter.md) ", um ein Drucker Handle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0e046-109">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="0e046-110">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e046-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e046-111">Der Typ der Daten, die die Funktion in dem Puffer speichert, auf den *pprinter* zeigt.</span><span class="sxs-lookup"><span data-stu-id="0e046-111">The type of data that the function stores into the buffer pointed to by *pPrinter*.</span></span> <span data-ttu-id="0e046-112">Wenn der *Befehls* Parameter ungleich 0 (null) ist, muss der *ebeneinameter* gleich 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="0e046-112">If the *Command* parameter is not equal to zero, the *Level* parameter must be zero.</span></span>

<span data-ttu-id="0e046-113">Dieser Wert kann 0, 2, 3, 4, 5, 6, 7, 8 oder 9 sein.</span><span class="sxs-lookup"><span data-stu-id="0e046-113">This value can be 0, 2, 3, 4, 5, 6, 7, 8, or 9.</span></span>

</dd> <dt>

<span data-ttu-id="0e046-114">*pprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e046-114">*pPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e046-115">Ein Zeiger auf einen Puffer, der Daten enthält, die für den Drucker festgelegt werden sollen, oder die Informationen für den Befehl enthält, der vom *Befehls* Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e046-115">A pointer to a buffer containing data to set for the printer, or containing information for the command specified by the *Command* parameter.</span></span> <span data-ttu-id="0e046-116">Der Typ der Daten im Puffer wird durch den Wert der *Ebene* bestimmt.</span><span class="sxs-lookup"><span data-stu-id="0e046-116">The type of data in the buffer is determined by the value of *Level*.</span></span>



| <span data-ttu-id="0e046-117">Ebene</span><span class="sxs-lookup"><span data-stu-id="0e046-117">Level</span></span>                                                                                                | <span data-ttu-id="0e046-118">Struktur</span><span class="sxs-lookup"><span data-stu-id="0e046-118">Structure</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="0e046-119"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="0e046-119"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="0e046-120">Wenn der *Befehls* Parameter der **\_ druckersteuerungsestatusstatus \_ \_** ist, muss *pprinter* einen **DWORD** -Wert enthalten, der den festzulegenden neuen Drucker Status angibt.</span><span class="sxs-lookup"><span data-stu-id="0e046-120">If the *Command* parameter is **PRINTER\_CONTROL\_SET\_STATUS**, *pPrinter* must contain a **DWORD** value that specifies the new printer status to set.</span></span> <span data-ttu-id="0e046-121">Eine Liste der möglichen Statuswerte finden Sie unter dem **statusmember** der Struktur " [**Printer \_ Info \_ 2**](printer-info-2.md) ".</span><span class="sxs-lookup"><span data-stu-id="0e046-121">For a list of the possible status values, see the **Status** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span> <span data-ttu-id="0e046-122">Beachten Sie, dass der **Drucker \_ Status \_ angeh** alten wurde und der **Drucker \_ Status \_ ausstehende \_ Löschung** keine gültigen Status Werte ist.</span><span class="sxs-lookup"><span data-stu-id="0e046-122">Note that **PRINTER\_STATUS\_PAUSED** and **PRINTER\_STATUS\_PENDING\_DELETION** are not valid status values to set.</span></span><br/> <span data-ttu-id="0e046-123">Wenn die *Ebene* 0 ist, der *Befehls* Parameter jedoch nicht der **Status der Drucker \_ Steuerungs \_ Sätze \_** ist, muss *pprinter* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="0e046-123">If *Level* is 0, but the *Command* parameter is not **PRINTER\_CONTROL\_SET\_STATUS**, *pPrinter* must be **NULL**.</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="0e046-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="0e046-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="0e046-125">Eine " [**Printer \_ Info \_ 2**](printer-info-2.md) "-Struktur, die ausführliche Informationen über den Drucker enthält.</span><span class="sxs-lookup"><span data-stu-id="0e046-125">A [**PRINTER\_INFO\_2**](printer-info-2.md) structure containing detailed information about the printer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="3"></span><dl> <span data-ttu-id="0e046-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="0e046-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="0e046-127">Eine [**Drucker \_ Info \_ 3**](printer-info-3.md) -Struktur, die die Sicherheitsinformationen des Druckers enthält.</span><span class="sxs-lookup"><span data-stu-id="0e046-127">A [**PRINTER\_INFO\_3**](printer-info-3.md) structure containing the printer's security information.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="4"></span><dl> <span data-ttu-id="0e046-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="0e046-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="0e046-129">Eine [**Drucker \_ Info \_ 4**](printer-info-4.md) -Struktur, die die minimalen Drucker Informationen enthält, einschließlich des Drucker namens, des Server namens und der Angabe, ob der Drucker Remote oder lokal ist.</span><span class="sxs-lookup"><span data-stu-id="0e046-129">A [**PRINTER\_INFO\_4**](printer-info-4.md) structure containing minimal printer information, including the name of the printer, the name of the server, and whether the printer is remote or local.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <span id="5"></span><dl> <span data-ttu-id="0e046-130"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="0e046-130"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="0e046-131">Eine [**Drucker \_ Info \_ 5**](printer-info-5.md) -Struktur, die Drucker Informationen enthält, wie z. b. Drucker Attribute und Timeout Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="0e046-131">A [**PRINTER\_INFO\_5**](printer-info-5.md) structure containing printer information such as printer attributes and time-out settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="6"></span><dl> <span data-ttu-id="0e046-132"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="0e046-132"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="0e046-133">Eine [**Drucker \_ Info \_ 6**](printer-info-6.md) -Struktur, die den Statuswert eines Druckers angibt.</span><span class="sxs-lookup"><span data-stu-id="0e046-133">A [**PRINTER\_INFO\_6**](printer-info-6.md) structure specifying the status value of a printer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="7"></span><dl> <span data-ttu-id="0e046-134"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="0e046-134"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="0e046-135">Eine [**Drucker \_ Info \_ 7**](printer-info-7.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0e046-135">A [**PRINTER\_INFO\_7**](printer-info-7.md) structure.</span></span> <span data-ttu-id="0e046-136">Der *dwAction* -Member dieser Struktur gibt an, ob **SetPrinter** die Daten des Druckers im Verzeichnisdienst veröffentlichen, erneut veröffentlichen, erneut veröffentlichen oder aktualisieren soll.</span><span class="sxs-lookup"><span data-stu-id="0e046-136">The *dwAction* member of this structure indicates whether **SetPrinter** should publish, unpublish, re-publish, or update the printer's data in the directory service.</span></span><br/>                                                                                                                                                                                                                                                                                                                |
| <span id="8"></span><dl> <span data-ttu-id="0e046-137"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="0e046-137"><dt>**8**</dt></span></span> </dl> | <span data-ttu-id="0e046-138">Eine [**Drucker \_ Info \_ 8**](printer-info-8.md) -Struktur, die die globalen Standarddrucker Einstellungen angibt.</span><span class="sxs-lookup"><span data-stu-id="0e046-138">A [**PRINTER\_INFO\_8**](printer-info-8.md) structure specifying the global default printer settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="9"></span><dl> <span data-ttu-id="0e046-139"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="0e046-139"><dt>**9**</dt></span></span> </dl> | <span data-ttu-id="0e046-140">Eine [**Drucker \_ Info \_ 9**](printer-info-9.md) -Struktur, die die Standarddrucker Einstellungen pro Benutzer angibt.</span><span class="sxs-lookup"><span data-stu-id="0e046-140">A [**PRINTER\_INFO\_9**](printer-info-9.md) structure specifying the per-user default printer settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="0e046-141">*Befehl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e046-141">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e046-142">Die auszuführende Aktion.</span><span class="sxs-lookup"><span data-stu-id="0e046-142">The action to perform.</span></span>

<span data-ttu-id="0e046-143">Wenn der *Level* -Parameter ungleich NULL ist, legen Sie den Wert dieses Parameters auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="0e046-143">If the *Level* parameter is nonzero, set the value of this parameter to zero.</span></span> <span data-ttu-id="0e046-144">In diesem Fall behält der Drucker seinen aktuellen Zustand bei, und die Funktion konfiguriert die Druckerdaten gemäß den Parametern " *Level* " und " *pprinter* " neu.</span><span class="sxs-lookup"><span data-stu-id="0e046-144">In this case, the printer retains its current state and the function reconfigures the printer data as specified by the *Level* and *pPrinter* parameters.</span></span>

<span data-ttu-id="0e046-145">Wenn der *Level* -Parameter 0 (null) ist, legen Sie den Wert dieses Parameters auf einen der folgenden Werte fest.</span><span class="sxs-lookup"><span data-stu-id="0e046-145">If the *Level* parameter is zero, set the value of this parameter to one of the following values.</span></span>



| <span data-ttu-id="0e046-146">Wert</span><span class="sxs-lookup"><span data-stu-id="0e046-146">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="0e046-147">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0e046-147">Meaning</span></span>                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CONTROL_PAUSE"></span><span id="printer_control_pause"></span><dl> <span data-ttu-id="0e046-148"><dt>**Drucker \_ Steuerelement anhalten \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0e046-148"><dt>**PRINTER\_CONTROL\_PAUSE**</dt></span></span> </dl>                 | <span data-ttu-id="0e046-149">Halten Sie den Drucker an.</span><span class="sxs-lookup"><span data-stu-id="0e046-149">Pause the printer.</span></span><br/>                                                                                                                       |
| <span id="PRINTER_CONTROL_PURGE"></span><span id="printer_control_purge"></span><dl> <span data-ttu-id="0e046-150"><dt>**Löschen von Drucker \_ Steuerelementen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0e046-150"><dt>**PRINTER\_CONTROL\_PURGE**</dt></span></span> </dl>                 | <span data-ttu-id="0e046-151">Löschen Sie alle Druckaufträge im Drucker.</span><span class="sxs-lookup"><span data-stu-id="0e046-151">Delete all print jobs in the printer.</span></span><br/>                                                                                                    |
| <span id="PRINTER_CONTROL_RESUME"></span><span id="printer_control_resume"></span><dl> <span data-ttu-id="0e046-152"><dt>**Drucker Steuerelement fortsetzen \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0e046-152"><dt>**PRINTER\_CONTROL\_RESUME**</dt></span></span> </dl>              | <span data-ttu-id="0e046-153">Setzen Sie einen angehaltenen Drucker fort.</span><span class="sxs-lookup"><span data-stu-id="0e046-153">Resume a paused printer.</span></span><br/>                                                                                                                 |
| <span id="PRINTER_CONTROL_SET_STATUS"></span><span id="printer_control_set_status"></span><dl> <span data-ttu-id="0e046-154"><dt>**\_Status des druckersteuerungsets \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0e046-154"><dt>**PRINTER\_CONTROL\_SET\_STATUS**</dt></span></span> </dl> | <span data-ttu-id="0e046-155">Legen Sie den Druckerstatus fest.</span><span class="sxs-lookup"><span data-stu-id="0e046-155">Set the printer status.</span></span><br/> <span data-ttu-id="0e046-156">Legen Sie den Parameter " *pprinter* " auf einen Zeiger auf einen **DWORD** -Wert fest, der den neuen Druckerstatus angibt.</span><span class="sxs-lookup"><span data-stu-id="0e046-156">Set the *pPrinter* parameter to a pointer to a **DWORD** value that specifies the new printer status.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e046-157">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e046-157">Return value</span></span>

<span data-ttu-id="0e046-158">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="0e046-158">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="0e046-159">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="0e046-159">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="0e046-160">Wenn *Level* 7 ist und bei der Veröffentlichungs Aktion ein Fehler aufgetreten ist, gibt **SetPrinter** eine **\_ \_ ausstehende Fehler** -e/a zurück und versucht, die Aktion im Hintergrund abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="0e046-160">If *Level* is 7 and the publish action failed, **SetPrinter** returns **ERROR\_IO\_PENDING** and attempts to complete the action in the background.</span></span> <span data-ttu-id="0e046-161">Wenn *Level* 7 ist und die Aktualisierungs Aktion fehlgeschlagen ist, gibt **SetPrinter** die **Fehler \_ Datei \_ nicht \_ gefunden** zurück.</span><span class="sxs-lookup"><span data-stu-id="0e046-161">If *Level* is 7 and the update action failed, **SetPrinter** returns **ERROR\_FILE\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e046-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e046-162">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0e046-163">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e046-163">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="0e046-164">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="0e046-164">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="0e046-165">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="0e046-165">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="0e046-166">Sie können **SetPrinter** nicht verwenden, um den Standarddrucker zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0e046-166">You cannot use **SetPrinter** to change the default printer.</span></span>

<span data-ttu-id="0e046-167">Um die aktuellen Druckereinstellungen zu ändern, rufen Sie die [**GetPrinter**](getprinter.md) -Funktion auf, um die aktuellen Einstellungen in eine [**Drucker \_ Info \_ 2**](printer-info-2.md) -Struktur abzurufen, die Elemente dieser Struktur nach Bedarf zu ändern und dann **SetPrinter** aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="0e046-167">To modify the current printer settings, call the [**GetPrinter**](getprinter.md) function to retrieve the current settings into a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, modify the members of that structure as necessary, and then call **SetPrinter**.</span></span>

<span data-ttu-id="0e046-168">Die Funktion " **SetPrinter** " ignoriert die Member " **pservername**", " **AveragePPM**", " **Status**" und " **cjobs** " einer [**Drucker \_ Info \_ 2**](printer-info-2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0e046-168">The **SetPrinter** function ignores the **pServerName**, **AveragePPM**, **Status**, and **cJobs** members of a [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>

<span data-ttu-id="0e046-169">Durch das Anhalten eines Druckers wird die Planung aller Druckaufträge für diesen Drucker angehalten, mit Ausnahme eines Druckauftrags, der möglicherweise gerade gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="0e046-169">Pausing a printer suspends scheduling of all print jobs for that printer, except for the one print job that may be currently printing.</span></span> <span data-ttu-id="0e046-170">Druckaufträge können an einen angehaltenen Drucker übermittelt werden, aber es ist nicht geplant, Aufträge auf diesem Drucker zu drucken, bis der Druckvorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="0e046-170">Print jobs can be submitted to a paused printer, but no jobs will be scheduled to print on that printer until printing is resumed.</span></span> <span data-ttu-id="0e046-171">Wenn ein Drucker gelöscht wird, werden alle Druckaufträge für diesen Drucker gelöscht, mit Ausnahme des aktuellen Druckauftrags.</span><span class="sxs-lookup"><span data-stu-id="0e046-171">If a printer is cleared, all print jobs for that printer are deleted, except for the current print job.</span></span>

<span data-ttu-id="0e046-172">Wenn Sie **SetPrinter** verwenden, um die Standardstruktur [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) für einen Drucker zu ändern (Global Festlegen der Drucker Standardwerte), müssen Sie zuerst die [**DocumentProperties**](documentproperties.md) -Funktion aufrufen, um die **DEVMODE** -Struktur zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0e046-172">If you use **SetPrinter** to modify the default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure for a printer (globally setting the printer defaults), you must first call the [**DocumentProperties**](documentproperties.md) function to validate the **DEVMODE** structure.</span></span>

<span data-ttu-id="0e046-173">Für die [**Drucker \_ Info \_ 2**](printer-info-2.md) -und [**Printer \_ Info \_ 3**](printer-info-3.md) -Strukturen, die einen Zeiger auf eine Sicherheits Beschreibung enthalten, kann die Funktion nur die Komponenten der Sicherheits Beschreibung festlegen, für die der Aufrufer über die Berechtigung zum Ändern verfügt.</span><span class="sxs-lookup"><span data-stu-id="0e046-173">For the [**PRINTER\_INFO\_2**](printer-info-2.md) and [**PRINTER\_INFO\_3**](printer-info-3.md) structures that contain a pointer to a security descriptor, the function can set only those components of the security descriptor that the caller has permission to modify.</span></span> <span data-ttu-id="0e046-174">Um bestimmte sicherheitsbeschreibungkomponenten festzulegen, müssen Sie die erforderlichen Zugriffsrechte angeben, wenn Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**OpenPrinter2**](openprinter2.md) aufrufen, um ein Handle für den Drucker abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0e046-174">To set particular security descriptor components, you must specify the necessary access rights when you call the [**OpenPrinter**](openprinter.md) or [**OpenPrinter2**](openprinter2.md) function to retrieve a handle to the printer.</span></span> <span data-ttu-id="0e046-175">In der folgenden Tabelle sind die zum Ändern der verschiedenen sicherheitsbeschreibungkomponenten erforderlichen Zugriffsrechte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e046-175">The following table shows the access rights required to modify the various security descriptor components.</span></span>



| <span data-ttu-id="0e046-176">Zugriffsberechtigung</span><span class="sxs-lookup"><span data-stu-id="0e046-176">Access permission</span></span>            | <span data-ttu-id="0e046-177">Sicherheitsbeschreibungerkomponente</span><span class="sxs-lookup"><span data-stu-id="0e046-177">Security descriptor component</span></span>             |
|------------------------------|-------------------------------------------|
| <span data-ttu-id="0e046-178">**\_Besitzer schreiben**</span><span class="sxs-lookup"><span data-stu-id="0e046-178">**WRITE\_OWNER**</span></span>             | <span data-ttu-id="0e046-179">Besitzer</span><span class="sxs-lookup"><span data-stu-id="0e046-179">Owner</span></span><br/> <span data-ttu-id="0e046-180">Primäre Gruppe</span><span class="sxs-lookup"><span data-stu-id="0e046-180">Primary group</span></span><br/> |
| <span data-ttu-id="0e046-181">**\_DAC schreiben**</span><span class="sxs-lookup"><span data-stu-id="0e046-181">**WRITE\_DAC**</span></span>               | <span data-ttu-id="0e046-182">Freigegebene Zugriffs Steuerungs Liste (DACL)</span><span class="sxs-lookup"><span data-stu-id="0e046-182">Discretionary access-control list (DACL)</span></span>  |
| <span data-ttu-id="0e046-183">**Zugreifen auf die \_ System \_ Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="0e046-183">**ACCESS\_SYSTEM\_SECURITY**</span></span> | <span data-ttu-id="0e046-184">System Zugriffs Steuerungs Liste (SACL)</span><span class="sxs-lookup"><span data-stu-id="0e046-184">System access-control list (SACL)</span></span>         |



 

<span data-ttu-id="0e046-185">Wenn die Sicherheits Beschreibung eine Komponente enthält, für die der Aufrufer nicht über das zu ändernde Zugriffsrecht verfügt, kann **SetPrinter** nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0e046-185">If the security descriptor contains a component that the caller does not have the access right to modify, **SetPrinter** fails.</span></span> <span data-ttu-id="0e046-186">Die Komponenten einer Sicherheits Beschreibung, die Sie nicht ändern möchten, sollten nach Bedarf **null** sein oder nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="0e046-186">Those components of a security descriptor that you don't want to modify should be **NULL** or not be present, as appropriate.</span></span> <span data-ttu-id="0e046-187">Wenn Sie die Sicherheits Beschreibung nicht ändern möchten und **SetPrinter** mit einer [**\_ Druckerinfo- \_ 2**](printer-info-2.md) -Struktur aufrufen, legen Sie den **psecuritydescriptor** -Member dieser Struktur auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="0e046-187">If you do not want to modify the security descriptor, and are calling **SetPrinter** with a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, set the **pSecurityDescriptor** member of that structure to **NULL**.</span></span>

<span data-ttu-id="0e046-188">Die Internetverbindungs Firewall (ICF) blockiert standardmäßig Drucker Anschlüsse, eine Ausnahme für die Datei-und Druckfreigabe kann jedoch aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="0e046-188">The Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing can be enabled.</span></span> <span data-ttu-id="0e046-189">Wenn **SetPrinter** von einem Computer Administrator aufgerufen wird, wird die Ausnahme aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0e046-189">If **SetPrinter** is called by a machine admin, it enables the exception.</span></span> <span data-ttu-id="0e046-190">Wenn Sie von einem nicht-Administrator aufgerufen wird und die Ausnahme nicht bereits aktiviert wurde, schlägt der Aufruf fehl.</span><span class="sxs-lookup"><span data-stu-id="0e046-190">If it is called by a non-admin and the exception has not already been enabled, the call fails.</span></span>

<span data-ttu-id="0e046-191">Sie können Ebene 7 mit der [**Drucker \_ Info \_ 7**](printer-info-7.md) -Struktur verwenden, um Verzeichnisdienst Daten für den Drucker zu veröffentlichen, zu veröffentlichen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0e046-191">You can use level 7 with the [**PRINTER\_INFO\_7**](printer-info-7.md) structure to publish, unpublish, or update directory service data for the printer.</span></span> <span data-ttu-id="0e046-192">Die Verzeichnisdienst Daten für einen Drucker enthalten alle Daten, die unter den splds-Schlüsseln gespeichert sind \_ \* , durch Aufrufe der [**setprinterdataex**](setprinterdataex.md) -Funktion für den Drucker.</span><span class="sxs-lookup"><span data-stu-id="0e046-192">The directory service data for a printer includes all the data stored under the SPLDS\_\* keys by calls to the [**SetPrinterDataEx**](setprinterdataex.md) function for the printer.</span></span> <span data-ttu-id="0e046-193">Legen Sie vor dem Aufrufen von **SetPrinter** den **pszobjectguid** -Member der **Drucker \_ Info \_ 7** auf **null** fest, und legen Sie den *dwAction* -Member auf einen der folgenden Werte fest.</span><span class="sxs-lookup"><span data-stu-id="0e046-193">Before calling **SetPrinter**, set the **pszObjectGUID** member of **PRINTER\_INFO\_7** to **NULL** and set the *dwAction* member to one of the following values.</span></span>



| <span data-ttu-id="0e046-194">Wert</span><span class="sxs-lookup"><span data-stu-id="0e046-194">Value</span></span>                             | <span data-ttu-id="0e046-195">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e046-195">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e046-196">**dsprint- \_ Veröffentlichung**</span><span class="sxs-lookup"><span data-stu-id="0e046-196">**DSPRINT\_PUBLISH**</span></span><br/>   | <span data-ttu-id="0e046-197">Veröffentlicht die Verzeichnisdienst Daten.</span><span class="sxs-lookup"><span data-stu-id="0e046-197">Publishes the directory service data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="0e046-198">**dsprint \_ erneut veröffentlichen**</span><span class="sxs-lookup"><span data-stu-id="0e046-198">**DSPRINT\_REPUBLISH**</span></span><br/> | <span data-ttu-id="0e046-199">Die Verzeichnisdienst Daten für den Drucker werden nicht veröffentlicht und dann erneut veröffentlicht, sodass alle Eigenschaften im veröffentlichten Drucker aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0e046-199">The directory service data for the printer is unpublished and then published again, refreshing all properties in the published printer.</span></span> <span data-ttu-id="0e046-200">Bei der erneuten Veröffentlichung wird auch die GUID des veröffentlichten Druckers geändert.</span><span class="sxs-lookup"><span data-stu-id="0e046-200">Re-publishing also changes the GUID of the published printer.</span></span> <span data-ttu-id="0e046-201">Verwenden Sie diesen Wert, wenn Sie vermuten, dass die veröffentlichten Daten des Druckers beschädigt wurden.</span><span class="sxs-lookup"><span data-stu-id="0e046-201">Use this value if you suspect the printer's published data has been corrupted.</span></span><br/>                                                                                         |
| <span data-ttu-id="0e046-202">**dsprint- \_ Veröffentlichung aufheben**</span><span class="sxs-lookup"><span data-stu-id="0e046-202">**DSPRINT\_UNPUBLISH**</span></span><br/> | <span data-ttu-id="0e046-203">Veröffentlicht die Veröffentlichung der Verzeichnisdienst Daten.</span><span class="sxs-lookup"><span data-stu-id="0e046-203">Unpublishes the directory service data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="0e046-204">**dsprint- \_ Update**</span><span class="sxs-lookup"><span data-stu-id="0e046-204">**DSPRINT\_UPDATE**</span></span><br/>    | <span data-ttu-id="0e046-205">Aktualisiert die Verzeichnisdienst Daten.</span><span class="sxs-lookup"><span data-stu-id="0e046-205">Updates the directory service data.</span></span> <span data-ttu-id="0e046-206">Dies entspricht der **dsprint- \_ Veröffentlichung**, mit dem Unterschied, dass **SetPrinter** fehlschlägt, wenn die **Fehler \_ Datei \_ nicht \_ gefunden** wurde, wenn der Drucker nicht bereits veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="0e046-206">This is the same as **DSPRINT\_PUBLISH**, except that **SetPrinter** fails with **ERROR\_FILE\_NOT\_FOUND** if the printer is not already published.</span></span><br/> <span data-ttu-id="0e046-207">Verwenden Sie das **dsprint- \_ Update** zum Aktualisieren veröffentlichter Eigenschaften, aber nicht das veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="0e046-207">Use **DSPRINT\_UPDATE** to update published properties but not force publishing.</span></span> <span data-ttu-id="0e046-208">Druckertreiber sollten immer das **dsprint- \_ Update** anstelle der **dsprint- \_ Veröffentlichung** verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e046-208">Printer drivers should always use **DSPRINT\_UPDATE** rather than **DSPRINT\_PUBLISH**.</span></span><br/> |



 

<span data-ttu-id="0e046-209">**Dsprint \_ Pending** ist kein gültiger *dwAction* -Wert für **SetPrinter**.</span><span class="sxs-lookup"><span data-stu-id="0e046-209">**DSPRINT\_PENDING** is not a valid *dwAction* value for **SetPrinter**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e046-210">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e046-210">Requirements</span></span>



| <span data-ttu-id="0e046-211">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e046-211">Requirement</span></span> | <span data-ttu-id="0e046-212">Wert</span><span class="sxs-lookup"><span data-stu-id="0e046-212">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e046-213">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0e046-213">Minimum supported client</span></span><br/> | <span data-ttu-id="0e046-214">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e046-214">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0e046-215">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0e046-215">Minimum supported server</span></span><br/> | <span data-ttu-id="0e046-216">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e046-216">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0e046-217">Header</span><span class="sxs-lookup"><span data-stu-id="0e046-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e046-218"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e046-218"><dt>WinSpool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0e046-219">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0e046-219">Library</span></span><br/>                  | <dl> <span data-ttu-id="0e046-220"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e046-220"><dt>WinSpool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="0e046-221">DLL</span><span class="sxs-lookup"><span data-stu-id="0e046-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e046-222"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="0e046-222"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="0e046-223">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="0e046-223">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0e046-224">**Setprinterw** (Unicode) und **setprintera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0e046-224">**SetPrinterW** (Unicode) and **SetPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="0e046-225">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e046-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e046-226">Drucken</span><span class="sxs-lookup"><span data-stu-id="0e046-226">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0e046-227">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="0e046-227">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="0e046-228">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="0e046-228">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="0e046-229">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="0e046-229">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="0e046-230">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="0e046-230">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="0e046-231">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="0e046-231">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="0e046-232">**Drucker \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="0e046-232">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="0e046-233">**Drucker \_ Informationen \_ 3**</span><span class="sxs-lookup"><span data-stu-id="0e046-233">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="0e046-234">**Drucker \_ Info \_ 4**</span><span class="sxs-lookup"><span data-stu-id="0e046-234">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="0e046-235">**Drucker \_ Informationen \_ 5**</span><span class="sxs-lookup"><span data-stu-id="0e046-235">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="0e046-236">**Drucker \_ Info \_ 6**</span><span class="sxs-lookup"><span data-stu-id="0e046-236">**PRINTER\_INFO\_6**</span></span>](printer-info-6.md)
</dt> <dt>

[<span data-ttu-id="0e046-237">**Drucker \_ Info \_ 7**</span><span class="sxs-lookup"><span data-stu-id="0e046-237">**PRINTER\_INFO\_7**</span></span>](printer-info-7.md)
</dt> <dt>

[<span data-ttu-id="0e046-238">**Drucker \_ Informationen \_ 8**</span><span class="sxs-lookup"><span data-stu-id="0e046-238">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> <dt>

[<span data-ttu-id="0e046-239">**Drucker \_ Informationen \_ 9**</span><span class="sxs-lookup"><span data-stu-id="0e046-239">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> <dt>

[<span data-ttu-id="0e046-240">**Setprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="0e046-240">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




