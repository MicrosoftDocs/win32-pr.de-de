---
description: Mit der setprinterdata-Funktion werden die Konfigurationsdaten für einen Drucker oder Druckserver festgelegt.
ms.assetid: 16072de9-98fb-4ada-8216-180b64cf44c8
title: Setprinterdata-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterData
- SetPrinterDataA
- SetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 36af84fe665d68fd7996a0b81fbbf291314cc69e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864751"
---
# <a name="setprinterdata-function"></a><span data-ttu-id="e4f66-103">Setprinterdata-Funktion</span><span class="sxs-lookup"><span data-stu-id="e4f66-103">SetPrinterData function</span></span>

<span data-ttu-id="e4f66-104">Mit der **setprinterdata** -Funktion werden die Konfigurationsdaten für einen Drucker oder Druckserver festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e4f66-104">The **SetPrinterData** function sets the configuration data for a printer or print server.</span></span>

<span data-ttu-id="e4f66-105">Um den Registrierungsschlüssel anzugeben, unter dem die Daten gespeichert werden sollen, müssen Sie die Funktion [**setprinterdataex**](setprinterdataex.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e4f66-105">To specify the registry key under which to store the data, call the [**SetPrinterDataEx**](setprinterdataex.md) function.</span></span> <span data-ttu-id="e4f66-106">Das Aufrufen von **setprinterdata** entspricht dem Aufrufen der **setprinterdataex** -Funktion, wobei der *pkeyname* -Parameter auf "printerdriverdata" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e4f66-106">Calling **SetPrinterData** is equivalent to calling the **SetPrinterDataEx** function with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="e4f66-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4f66-107">Syntax</span></span>


```C++
DWORD SetPrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName,
  _In_ DWORD  Type,
  _In_ LPBYTE pData,
  _In_ DWORD  cbData
);
```



## <a name="parameters"></a><span data-ttu-id="e4f66-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4f66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4f66-109">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4f66-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4f66-110">Ein Handle für den Drucker oder Druckserver, für das die Funktion Konfigurationsdaten festlegt.</span><span class="sxs-lookup"><span data-stu-id="e4f66-110">A handle to the printer or print server for which the function sets configuration data.</span></span> <span data-ttu-id="e4f66-111">Verwenden Sie die Funktion " [**OpenPrinter**](openprinter.md)", " [**OpenPrinter2**](openprinter2.md)" oder " [**addprinter**](addprinter.md) ", um ein Drucker Handle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e4f66-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="e4f66-112">*pvaluename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4f66-112">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4f66-113">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die festzulegenden Daten identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e4f66-113">A pointer to a null-terminated string that identifies the data to set.</span></span>

<span data-ttu-id="e4f66-114">Bei Druckern ist diese Zeichenfolge der Name eines Registrierungs Werts unter dem Schlüssel "printerdriverdata" des Druckers in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="e4f66-114">For printers, this string is the name of a registry value under the printer's "PrinterDriverData" key in the registry.</span></span>

<span data-ttu-id="e4f66-115">Bei Druckservern handelt es sich bei dieser Zeichenfolge um eine der vordefinierten Zeichen folgen, die im folgenden Abschnitt mit Hinweisen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e4f66-115">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="e4f66-116">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4f66-116">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4f66-117">Ein Code, der den Datentyp angibt, auf den der *pData* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="e4f66-117">A code that indicates the type of data that the *pData* parameter points to.</span></span> <span data-ttu-id="e4f66-118">Eine Liste der möglichen Typcodes finden Sie unter [Registrierungs Werttypen](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="e4f66-118">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

</dd> <dt>

<span data-ttu-id="e4f66-119">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4f66-119">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4f66-120">Ein Zeiger auf ein Bytearray, das die Drucker Konfigurationsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="e4f66-120">A pointer to an array of bytes that contains the printer configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="e4f66-121">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4f66-121">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4f66-122">Die Größe des Arrays in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e4f66-122">The size, in bytes, of the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4f66-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4f66-123">Return value</span></span>

<span data-ttu-id="e4f66-124">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **Fehler \_ erfolgreich**.</span><span class="sxs-lookup"><span data-stu-id="e4f66-124">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="e4f66-125">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="e4f66-125">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4f66-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4f66-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e4f66-127">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e4f66-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e4f66-128">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="e4f66-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e4f66-129">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="e4f66-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e4f66-130">Um vorhandene Konfigurationsdaten für einen Drucker abzurufen, rufen Sie die Funktion [**getprinterdataex**](getprinterdataex.md) oder [**getprinterdata**](getprinterdata.md) auf.</span><span class="sxs-lookup"><span data-stu-id="e4f66-130">To retrieve existing configuration data for a printer, call the [**GetPrinterDataEx**](getprinterdataex.md) or [**GetPrinterData**](getprinterdata.md) function.</span></span>

<span data-ttu-id="e4f66-131">Wenn *hprinter* ein Handle für einen Druckserver ist, kann *pvaluename* einen der folgenden vordefinierten Werte angeben.</span><span class="sxs-lookup"><span data-stu-id="e4f66-131">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="e4f66-132">Wert</span><span class="sxs-lookup"><span data-stu-id="e4f66-132">Value</span></span>                                                               | <span data-ttu-id="e4f66-133">Kommentare</span><span class="sxs-lookup"><span data-stu-id="e4f66-133">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f66-134">**splreg \_ Allow \_ User \_ manageforms**</span><span class="sxs-lookup"><span data-stu-id="e4f66-134">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="e4f66-135">Windows XP mit Service Pack 2 (SP2) und höher</span><span class="sxs-lookup"><span data-stu-id="e4f66-135">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="e4f66-136">Windows Server 2003 mit Service Pack 1 (SP1) und höher</span><span class="sxs-lookup"><span data-stu-id="e4f66-136">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="e4f66-137">**splreg \_ Beep \_ aktiviert**</span><span class="sxs-lookup"><span data-stu-id="e4f66-137">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="e4f66-138">**splreg \_ - \_ Standard \_ Spoolverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="e4f66-138">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="e4f66-139">**splreg- \_ Ereignis \_ Protokoll**</span><span class="sxs-lookup"><span data-stu-id="e4f66-139">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="e4f66-140">**splreg \_ net- \_ Popup**</span><span class="sxs-lookup"><span data-stu-id="e4f66-140">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="e4f66-141">Wird in Windows Server 2003 und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e4f66-141">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="e4f66-142">**standardmäßige \_ \_ Thread \_ Priorität \_ für den splreg-Port**</span><span class="sxs-lookup"><span data-stu-id="e4f66-142">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="e4f66-143">**\_ \_ Thread \_ Priorität des splreg-Ports**</span><span class="sxs-lookup"><span data-stu-id="e4f66-143">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="e4f66-144">**splreg \_ - \_ drucktreiberisolations- \_ \_ Gruppen**</span><span class="sxs-lookup"><span data-stu-id="e4f66-144">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="e4f66-145">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="e4f66-145">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="e4f66-146">**Dauer der \_ Druck \_ Treiber \_ Isolation \_ \_ vor \_ der Wiederverwendung**</span><span class="sxs-lookup"><span data-stu-id="e4f66-146">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="e4f66-147">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="e4f66-147">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="e4f66-148">**maximale Anzahl von Objekten für die \_ Druck \_ Treiber \_ Isolation \_ \_ \_ vor \_ der Wiederverwendung**</span><span class="sxs-lookup"><span data-stu-id="e4f66-148">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="e4f66-149">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="e4f66-149">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="e4f66-150">**Leerlauf Timeout der splreg- \_ Druck \_ Treiber \_ Isolation \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e4f66-150">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="e4f66-151">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="e4f66-151">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="e4f66-152">**Ausführungs Richtlinie der splreg- \_ Druck \_ Treiber \_ Isolation \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e4f66-152">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="e4f66-153">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="e4f66-153">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="e4f66-154">**Außerkraftsetzungs Richtlinie für die splreg- \_ Druck \_ Treiber \_ Isolation \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e4f66-154">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="e4f66-155">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="e4f66-155">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="e4f66-156">**splreg- \_ Wiederholungs- \_ Popup**</span><span class="sxs-lookup"><span data-stu-id="e4f66-156">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="e4f66-157">Bei erfolgreicher Rückgabe enthält *pData* 1, wenn der Server für die Wiederherstellung von Popup Fenstern für alle Aufträge festgelegt ist, oder 0, wenn der Server keine Popup Fenster für alle Aufträge erneut versucht.</span><span class="sxs-lookup"><span data-stu-id="e4f66-157">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="e4f66-158">Wird in Windows Server 2003 und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e4f66-158">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="e4f66-159">**splreg \_ Scheduler \_ Thread \_ Priorität**</span><span class="sxs-lookup"><span data-stu-id="e4f66-159">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="e4f66-160">**standardmäßige \_ \_ Thread \_ Priorität \_ für den splreg-Scheduler**</span><span class="sxs-lookup"><span data-stu-id="e4f66-160">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="e4f66-161">**splreg \_ websharemgmt**</span><span class="sxs-lookup"><span data-stu-id="e4f66-161">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="e4f66-162">Windows Server 2003 und höher</span><span class="sxs-lookup"><span data-stu-id="e4f66-162">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="e4f66-163">Die folgenden Werte von *pvaluename* bestimmen das Druck Verhalten beim Pool, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="e4f66-163">The following values of *pValueName* determine the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="e4f66-164">Wert</span><span class="sxs-lookup"><span data-stu-id="e4f66-164">Value</span></span>                                       | <span data-ttu-id="e4f66-165">Kommentare</span><span class="sxs-lookup"><span data-stu-id="e4f66-165">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f66-166">**\_Fehler beim Fehler "splreg Restart \_ Job \_ on \_ Pool \_ ".**</span><span class="sxs-lookup"><span data-stu-id="e4f66-166">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="e4f66-167">Der Wert von *pData* gibt die Zeit in Sekunden an, nach der ein Auftrag an einem anderen Port neu gestartet wird, nachdem ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e4f66-167">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="e4f66-168">Diese Einstellung wird mit dem **Auftrag "splreg \_ Restart" \_ \_ bei \_ \_ aktiviertem Pool** verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4f66-168">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="e4f66-169">**splreg- \_ Neustart \_ Auftrag \_ für \_ Pool \_ aktiviert**</span><span class="sxs-lookup"><span data-stu-id="e4f66-169">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="e4f66-170">Ein Wert ungleich 0 (null) in *pData* gibt an, dass der **Fehler "splreg \_ Restart \_ Job \_ on \_ Pool \_** " aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e4f66-170">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="e4f66-171">Die im Fehler des **Auftrags "splreg \_ Restart \_ Job \_ on \_ Pool \_** " angegebene Zeit ist eine minimale Zeit.</span><span class="sxs-lookup"><span data-stu-id="e4f66-171">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="e4f66-172">Die tatsächliche Zeit kann je nach den folgenden Port Monitoreinstellungen, bei denen es sich um Registrierungs Werte unter diesem Registrierungsschlüssel handelt, länger sein:</span><span class="sxs-lookup"><span data-stu-id="e4f66-172">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="e4f66-173">**HKLM \\ System \\ CurrentControlSet \\ Control \\ Print \\ Monitors \\ < *Monitorname* > \\ Ports**</span><span class="sxs-lookup"><span data-stu-id="e4f66-173">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="e4f66-174">Um diese Werte festzulegen, können Sie die [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e4f66-174">Call the [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) function to set these values.</span></span>



| <span data-ttu-id="e4f66-175">Port Monitor Einstellung</span><span class="sxs-lookup"><span data-stu-id="e4f66-175">Port monitor setting</span></span>     | <span data-ttu-id="e4f66-176">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e4f66-176">Data type</span></span>      | <span data-ttu-id="e4f66-177">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e4f66-177">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f66-178">**Statusupdateaktivierte**</span><span class="sxs-lookup"><span data-stu-id="e4f66-178">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="e4f66-179">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e4f66-179">**REG\_DWORD**</span></span> | <span data-ttu-id="e4f66-180">Wenn ein Wert ungleich NULL ist, wird es dem Port Monitor ermöglicht, den Spooler mit dem Port Status zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e4f66-180">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="e4f66-181">**Statusupdateinterval**</span><span class="sxs-lookup"><span data-stu-id="e4f66-181">**StatusUpdateInterval**</span></span> | <span data-ttu-id="e4f66-182">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e4f66-182">**REG\_DWORD**</span></span> | <span data-ttu-id="e4f66-183">Gibt das Intervall (in Minuten) an, in dem der Port Monitor den Spooler mit dem Port Status aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e4f66-183">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="e4f66-184">In Windows 7 und höheren Versionen von Windows werden Druckaufträge, die an einen Druckserver gesendet werden, standardmäßig auf dem Client gerendert.</span><span class="sxs-lookup"><span data-stu-id="e4f66-184">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="e4f66-185">Das Client seitige Rendering von Druckaufträgen kann für jeden Drucker konfiguriert werden, indem die folgenden Werte in " *pvaluename*" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e4f66-185">Client-side rendering of a print jobs can be configured for each printer by setting the following values in *pValueName*.</span></span>



| <span data-ttu-id="e4f66-186">Einstellung</span><span class="sxs-lookup"><span data-stu-id="e4f66-186">Setting</span></span>                      | <span data-ttu-id="e4f66-187">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e4f66-187">Data type</span></span>      | <span data-ttu-id="e4f66-188">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4f66-188">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f66-189">**EMF despoolingsetting**</span><span class="sxs-lookup"><span data-stu-id="e4f66-189">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="e4f66-190">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e4f66-190">**REG\_DWORD**</span></span> | <span data-ttu-id="e4f66-191">Der Wert 0 (null), oder wenn dieser Wert nicht in der Registrierung vorhanden ist, aktiviert das Client seitige Standard Rendering von Druckaufträgen.</span><span class="sxs-lookup"><span data-stu-id="e4f66-191">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="e4f66-192">Der Wert 1 deaktiviert das Client seitige Rendering von Druckaufträgen.</span><span class="sxs-lookup"><span data-stu-id="e4f66-192">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                      |
| <span data-ttu-id="e4f66-193">**Forceclientsiderderdering**</span><span class="sxs-lookup"><span data-stu-id="e4f66-193">**ForceClientSideRendering**</span></span> | <span data-ttu-id="e4f66-194">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e4f66-194">**REG\_DWORD**</span></span> | <span data-ttu-id="e4f66-195">Der Wert 0 oder, wenn dieser Wert nicht in der Registrierung vorhanden ist, bewirkt, dass die Druckaufträge auf dem Client gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="e4f66-195">A value of 0, or if this value is not present in the registry, causes the print jobs to be rendered on the client.</span></span> <span data-ttu-id="e4f66-196">Wenn ein Druckauftrag nicht auf dem Client gerendert werden kann, wird er auf dem Server gerendert.</span><span class="sxs-lookup"><span data-stu-id="e4f66-196">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="e4f66-197">Wenn ein Druckauftrag nicht auf dem Server gerendert werden kann, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="e4f66-197">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="e4f66-198">Bei einem Wert von 1 werden Druckaufträge auf dem Client ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="e4f66-198">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="e4f66-199">Wenn ein Druckauftrag nicht auf dem Client gerendert werden kann, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="e4f66-199">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e4f66-200">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4f66-200">Requirements</span></span>



| <span data-ttu-id="e4f66-201">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4f66-201">Requirement</span></span> | <span data-ttu-id="e4f66-202">Wert</span><span class="sxs-lookup"><span data-stu-id="e4f66-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f66-203">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4f66-203">Minimum supported client</span></span><br/> | <span data-ttu-id="e4f66-204">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4f66-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e4f66-205">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4f66-205">Minimum supported server</span></span><br/> | <span data-ttu-id="e4f66-206">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4f66-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e4f66-207">Header</span><span class="sxs-lookup"><span data-stu-id="e4f66-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4f66-208"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4f66-208"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e4f66-209">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e4f66-209">Library</span></span><br/>                  | <dl> <span data-ttu-id="e4f66-210"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4f66-210"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e4f66-211">DLL</span><span class="sxs-lookup"><span data-stu-id="e4f66-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4f66-212"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="e4f66-212"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e4f66-213">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="e4f66-213">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e4f66-214">**Setprinterdataw** (Unicode) und **setprinterdataa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e4f66-214">**SetPrinterDataW** (Unicode) and **SetPrinterDataA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="e4f66-215">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4f66-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4f66-216">Drucken</span><span class="sxs-lookup"><span data-stu-id="e4f66-216">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e4f66-217">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e4f66-217">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e4f66-218">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="e4f66-218">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="e4f66-219">**Getprinterdata**</span><span class="sxs-lookup"><span data-stu-id="e4f66-219">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="e4f66-220">**Getprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="e4f66-220">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="e4f66-221">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="e4f66-221">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="e4f66-222">**Setprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="e4f66-222">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

