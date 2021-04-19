---
description: Die getprinterdata-Funktion ruft Konfigurationsdaten für den angegebenen Drucker oder Druckserver ab.
ms.assetid: b5a44b27-a4aa-4e58-9a64-05be87d12ab5
title: Getprinterdata-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterData
- GetPrinterDataA
- GetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: cb18936d6d3c1d82f4a52a874883cdcdfaae4815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362350"
---
# <a name="getprinterdata-function"></a><span data-ttu-id="03aa2-103">Getprinterdata-Funktion</span><span class="sxs-lookup"><span data-stu-id="03aa2-103">GetPrinterData function</span></span>

<span data-ttu-id="03aa2-104">Die **getprinterdata** -Funktion ruft Konfigurationsdaten für den angegebenen Drucker oder Druckserver ab.</span><span class="sxs-lookup"><span data-stu-id="03aa2-104">The **GetPrinterData** function retrieves configuration data for the specified printer or print server.</span></span>

<span data-ttu-id="03aa2-105">In Windows 2000 und neueren Versionen von Windows entspricht das Aufrufen von **getprinterdata** dem Aufrufen von [**getprinterdataex**](/windows/desktop/printdocs/getprinterdataex) , wobei der *pkeyname* -Parameter auf "printerdriverdata" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="03aa2-105">In Windows 2000 and later versions of Windows, calling **GetPrinterData** is equivalent to calling [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="03aa2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="03aa2-106">Syntax</span></span>


```C++
DWORD GetPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="03aa2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="03aa2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03aa2-108">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03aa2-108">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03aa2-109">Ein Handle für den Drucker oder Druckserver, für das die Funktion Konfigurationsdaten abruft.</span><span class="sxs-lookup"><span data-stu-id="03aa2-109">A handle to the printer or print server for which the function retrieves configuration data.</span></span> <span data-ttu-id="03aa2-110">Verwenden Sie die Funktion " [**OpenPrinter**](openprinter.md)", " [**OpenPrinter2**](openprinter2.md)" oder " [**addprinter**](addprinter.md) ", um ein Drucker Handle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="03aa2-110">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="03aa2-111">*pvaluename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03aa2-111">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03aa2-112">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die abzurufenden Daten identifiziert.</span><span class="sxs-lookup"><span data-stu-id="03aa2-112">A pointer to a null-terminated string that identifies the data to retrieve.</span></span>

<span data-ttu-id="03aa2-113">Bei Druckern ist diese Zeichenfolge der Name eines Registrierungs Werts unter dem Schlüssel "printerdriverdata" des Druckers in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="03aa2-113">For printers, this string is the name of a registry value under the printer's "PrinterDriverData" key in the registry.</span></span>

<span data-ttu-id="03aa2-114">Bei Druckservern handelt es sich bei dieser Zeichenfolge um eine der vordefinierten Zeichen folgen, die im folgenden Abschnitt mit Hinweisen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="03aa2-114">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="03aa2-115">*pType* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="03aa2-115">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03aa2-116">Ein Zeiger auf eine Variable, die einen Wert empfängt, der den Typ der in *pData* abgerufenen Daten angibt.</span><span class="sxs-lookup"><span data-stu-id="03aa2-116">A pointer to a variable that receives a value that indicates the type of data retrieved in *pData*.</span></span> <span data-ttu-id="03aa2-117">Die-Funktion gibt den Typ zurück, der im [**setprinterdata**](setprinterdata.md) -oder [**setprinterdataex**](setprinterdataex.md) -aufrufen angegeben ist, der die Daten gespeichert hat.</span><span class="sxs-lookup"><span data-stu-id="03aa2-117">The function returns the type specified in the [**SetPrinterData**](setprinterdata.md) or [**SetPrinterDataEx**](setprinterdataex.md) call that stored the data.</span></span> <span data-ttu-id="03aa2-118">Legen Sie diesen Parameter auf **null** fest, wenn Sie den-Datentyp nicht benötigen.</span><span class="sxs-lookup"><span data-stu-id="03aa2-118">Set this parameter to **NULL** if you don't need the data type.</span></span>

</dd> <dt>

<span data-ttu-id="03aa2-119">*pData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="03aa2-119">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03aa2-120">Ein Zeiger auf einen Puffer, der die Konfigurationsdaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="03aa2-120">A pointer to a buffer that receives the configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="03aa2-121">*nSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03aa2-121">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03aa2-122">Die Größe (in Bytes) des Puffers, auf den *pData* verweist.</span><span class="sxs-lookup"><span data-stu-id="03aa2-122">The size, in bytes, of the buffer that *pData* points to.</span></span>

</dd> <dt>

<span data-ttu-id="03aa2-123">*pcbbenötigte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="03aa2-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03aa2-124">Ein Zeiger auf eine Variable, die die Größe der Konfigurationsdaten in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="03aa2-124">A pointer to a variable that receives the size, in bytes, of the configuration data.</span></span> <span data-ttu-id="03aa2-125">Wenn die von *nSize* angegebene Puffergröße zu klein ist, gibt die Funktion **Fehler \_ Weitere \_ Daten** zurück, und *pcbrequired* gibt die erforderliche Puffergröße an.</span><span class="sxs-lookup"><span data-stu-id="03aa2-125">If the buffer size specified by *nSize* is too small, the function returns **ERROR\_MORE\_DATA**, and *pcbNeeded* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03aa2-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03aa2-126">Return value</span></span>

<span data-ttu-id="03aa2-127">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **Fehler \_ erfolgreich**.</span><span class="sxs-lookup"><span data-stu-id="03aa2-127">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="03aa2-128">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="03aa2-128">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="03aa2-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03aa2-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="03aa2-130">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="03aa2-130">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="03aa2-131">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="03aa2-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="03aa2-132">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="03aa2-132">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="03aa2-133">**Getprinterdata** ruft Drucker Konfigurationsdaten ab, die von der [**setprinterdataex**](setprinterdataex.md) -Funktion oder der [**setprinterdata**](setprinterdata.md) -Funktion festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="03aa2-133">**GetPrinterData** retrieves printer configuration data that was set by the [**SetPrinterDataEx**](setprinterdataex.md) or [**SetPrinterData**](setprinterdata.md) function.</span></span>

<span data-ttu-id="03aa2-134">**Getprinterdata** löst möglicherweise einen Windows-Befehl an [**getprinterdatafromport**](/previous-versions//ff550506(v=vs.85))aus, der in die Registrierung schreiben könnte.</span><span class="sxs-lookup"><span data-stu-id="03aa2-134">**GetPrinterData** might trigger a Windows call to [**GetPrinterDataFromPort**](/previous-versions//ff550506(v=vs.85)), which might write to the registry.</span></span> <span data-ttu-id="03aa2-135">Wenn dies der Fall ist, können Nebeneffekte auftreten, z. b. das Auslösen einer Update-oder upgradedrucker-Ereignis-ID 20 im Client, wenn der Drucker in einem Netzwerk freigegeben ist.</span><span class="sxs-lookup"><span data-stu-id="03aa2-135">If it does, side effects can occur, such as triggering an update or upgrade printer event ID 20 in the client, if the printer is shared in a network.</span></span>

<span data-ttu-id="03aa2-136">Wenn *hprinter* ein Handle für einen Druckserver ist, kann *pvaluename* einen der folgenden vordefinierten Werte angeben.</span><span class="sxs-lookup"><span data-stu-id="03aa2-136">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="03aa2-137">Wert</span><span class="sxs-lookup"><span data-stu-id="03aa2-137">Value</span></span>                                                               | <span data-ttu-id="03aa2-138">Kommentare</span><span class="sxs-lookup"><span data-stu-id="03aa2-138">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03aa2-139">**splreg \_ Allow \_ User \_ manageforms**</span><span class="sxs-lookup"><span data-stu-id="03aa2-139">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="03aa2-140">Windows XP mit Service Pack 2 (SP2) und höher</span><span class="sxs-lookup"><span data-stu-id="03aa2-140">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="03aa2-141">Windows Server 2003 mit Service Pack 1 (SP1) und höher</span><span class="sxs-lookup"><span data-stu-id="03aa2-141">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="03aa2-142">**splreg- \_ Architektur**</span><span class="sxs-lookup"><span data-stu-id="03aa2-142">**SPLREG\_ARCHITECTURE**</span></span>                                            |                                                                                                                                                                                                                                 |
| <span data-ttu-id="03aa2-143">**splreg \_ Beep \_ aktiviert**</span><span class="sxs-lookup"><span data-stu-id="03aa2-143">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="03aa2-144">**splreg \_ - \_ Standard \_ Spoolverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="03aa2-144">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="03aa2-145">**Name der splreg \_ DNS- \_ Maschine \_**</span><span class="sxs-lookup"><span data-stu-id="03aa2-145">**SPLREG\_DNS\_MACHINE\_NAME**</span></span>                                      |                                                                                                                                                                                                                                 |
| <span data-ttu-id="03aa2-146">**splreg \_ DS \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="03aa2-146">**SPLREG\_DS\_PRESENT**</span></span>                                             | <span data-ttu-id="03aa2-147">Bei erfolgreicher Rückgabe enthält *pData* 0x0001, wenn sich der Computer in einer DS-Domäne befindet, andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="03aa2-147">On successful return, *pData* contains 0x0001 if the machine is on a DS domain, 0 otherwise.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="03aa2-148">**splreg \_ DS \_ \_ für \_ Benutzer vorhanden**</span><span class="sxs-lookup"><span data-stu-id="03aa2-148">**SPLREG\_DS\_PRESENT\_FOR\_USER**</span></span>                                  | <span data-ttu-id="03aa2-149">Bei erfolgreicher Rückgabe enthält *pData* 0x0001, wenn der Benutzer bei einer DS-Domäne angemeldet ist, andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="03aa2-149">On successful return, *pData* contains 0x0001 if the user is logged onto a DS domain, 0 otherwise.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="03aa2-150">**splreg- \_ Ereignis \_ Protokoll**</span><span class="sxs-lookup"><span data-stu-id="03aa2-150">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="03aa2-151">**splreg- \_ Haupt \_ Version**</span><span class="sxs-lookup"><span data-stu-id="03aa2-151">**SPLREG\_MAJOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="03aa2-152">**splreg- \_ neben \_ Version**</span><span class="sxs-lookup"><span data-stu-id="03aa2-152">**SPLREG\_MINOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="03aa2-153">**splreg \_ net- \_ Popup**</span><span class="sxs-lookup"><span data-stu-id="03aa2-153">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="03aa2-154">Wird in Windows Server 2003 und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03aa2-154">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="03aa2-155">**splreg \_ net- \_ Popup \_ auf \_ Computer**</span><span class="sxs-lookup"><span data-stu-id="03aa2-155">**SPLREG\_NET\_POPUP\_TO\_COMPUTER**</span></span>                                | <span data-ttu-id="03aa2-156">Bei erfolgreicher Rückgabe enthält *pData* 1, wenn Auftrags Benachrichtigungen an den Client Computer gesendet werden sollen, oder 0, wenn Auftrags Benachrichtigungen an den Benutzer gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="03aa2-156">On successful return, *pData* contains 1 if job notifications should be sent to the client computer, or 0 if job notifications are to be sent to the user.</span></span><br/> <span data-ttu-id="03aa2-157">Wird in Windows Server 2003 und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03aa2-157">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="03aa2-158">**splreg \_ OS- \_ Version**</span><span class="sxs-lookup"><span data-stu-id="03aa2-158">**SPLREG\_OS\_VERSION**</span></span>                                             | <span data-ttu-id="03aa2-159">Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="03aa2-159">Windows XP and later</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="03aa2-160">**splreg \_ OS \_ versionex**</span><span class="sxs-lookup"><span data-stu-id="03aa2-160">**SPLREG\_OS\_VERSIONEX**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="03aa2-161">**standardmäßige \_ \_ Thread \_ Priorität \_ für den splreg-Port**</span><span class="sxs-lookup"><span data-stu-id="03aa2-161">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="03aa2-162">**\_ \_ Thread \_ Priorität des splreg-Ports**</span><span class="sxs-lookup"><span data-stu-id="03aa2-162">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="03aa2-163">**splreg \_ - \_ drucktreiberisolations- \_ \_ Gruppen**</span><span class="sxs-lookup"><span data-stu-id="03aa2-163">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="03aa2-164">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="03aa2-164">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="03aa2-165">**Dauer der \_ Druck \_ Treiber \_ Isolation \_ \_ vor \_ der Wiederverwendung**</span><span class="sxs-lookup"><span data-stu-id="03aa2-165">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="03aa2-166">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="03aa2-166">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="03aa2-167">**maximale Anzahl von Objekten für die \_ Druck \_ Treiber \_ Isolation \_ \_ \_ vor \_ der Wiederverwendung**</span><span class="sxs-lookup"><span data-stu-id="03aa2-167">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="03aa2-168">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="03aa2-168">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="03aa2-169">**Leerlauf Timeout der splreg- \_ Druck \_ Treiber \_ Isolation \_ \_**</span><span class="sxs-lookup"><span data-stu-id="03aa2-169">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="03aa2-170">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="03aa2-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="03aa2-171">**Ausführungs Richtlinie der splreg- \_ Druck \_ Treiber \_ Isolation \_ \_**</span><span class="sxs-lookup"><span data-stu-id="03aa2-171">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="03aa2-172">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="03aa2-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="03aa2-173">**Außerkraftsetzungs Richtlinie für die splreg- \_ Druck \_ Treiber \_ Isolation \_ \_**</span><span class="sxs-lookup"><span data-stu-id="03aa2-173">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="03aa2-174">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="03aa2-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="03aa2-175">**splreg- \_ Remote \_ Fax**</span><span class="sxs-lookup"><span data-stu-id="03aa2-175">**SPLREG\_REMOTE\_FAX**</span></span>                                             | <span data-ttu-id="03aa2-176">Bei erfolgreicher Rückgabe enthält *pData* 0x0001, wenn der Faxdienst Remote Clients unterstützt, andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="03aa2-176">On successful return, *pData* contains 0x0001 if the FAX service supports remote clients, 0 otherwise.</span></span><br/>                                                                                                               |
| <span data-ttu-id="03aa2-177">**splreg- \_ Wiederholungs- \_ Popup**</span><span class="sxs-lookup"><span data-stu-id="03aa2-177">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="03aa2-178">Bei erfolgreicher Rückgabe enthält *pData* 1, wenn der Server für die Wiederherstellung von Popup Fenstern für alle Aufträge festgelegt ist, oder 0, wenn der Server keine Popup Fenster für alle Aufträge erneut versucht.</span><span class="sxs-lookup"><span data-stu-id="03aa2-178">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="03aa2-179">Wird in Windows Server 2003 und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03aa2-179">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="03aa2-180">**splreg \_ Scheduler \_ Thread \_ Priorität**</span><span class="sxs-lookup"><span data-stu-id="03aa2-180">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="03aa2-181">**standardmäßige \_ \_ Thread \_ Priorität \_ für den splreg-Scheduler**</span><span class="sxs-lookup"><span data-stu-id="03aa2-181">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="03aa2-182">**splreg \_ websharemgmt**</span><span class="sxs-lookup"><span data-stu-id="03aa2-182">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="03aa2-183">Windows Server 2003 und höher</span><span class="sxs-lookup"><span data-stu-id="03aa2-183">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="03aa2-184">Die folgenden Werte von *pvaluename* geben das Druck Verhalten des Pools an, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="03aa2-184">The following values of *pValueName* indicate the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="03aa2-185">Wert</span><span class="sxs-lookup"><span data-stu-id="03aa2-185">Value</span></span>                                       | <span data-ttu-id="03aa2-186">Kommentare</span><span class="sxs-lookup"><span data-stu-id="03aa2-186">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03aa2-187">**\_Fehler beim Fehler "splreg Restart \_ Job \_ on \_ Pool \_ ".**</span><span class="sxs-lookup"><span data-stu-id="03aa2-187">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="03aa2-188">Der Wert von *pData* gibt die Zeit in Sekunden an, nach der ein Auftrag an einem anderen Port neu gestartet wird, nachdem ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="03aa2-188">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="03aa2-189">Diese Einstellung wird mit dem **Auftrag "splreg \_ Restart" \_ \_ bei \_ \_ aktiviertem Pool** verwendet.</span><span class="sxs-lookup"><span data-stu-id="03aa2-189">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="03aa2-190">**splreg- \_ Neustart \_ Auftrag \_ für \_ Pool \_ aktiviert**</span><span class="sxs-lookup"><span data-stu-id="03aa2-190">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="03aa2-191">Ein Wert ungleich 0 (null) in *pData* gibt an, dass der **Fehler "splreg \_ Restart \_ Job \_ on \_ Pool \_** " aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="03aa2-191">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="03aa2-192">Die im Fehler des **Auftrags "splreg \_ Restart \_ Job \_ on \_ Pool \_** " angegebene Zeit ist eine minimale Zeit.</span><span class="sxs-lookup"><span data-stu-id="03aa2-192">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="03aa2-193">Die tatsächliche Zeit kann je nach den folgenden Port Monitoreinstellungen, bei denen es sich um Registrierungs Werte unter diesem Registrierungsschlüssel handelt, länger sein:</span><span class="sxs-lookup"><span data-stu-id="03aa2-193">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="03aa2-194">**HKLM \\ System \\ CurrentControlSet \\ Control \\ Print \\ Monitors \\ < *Monitorname* > \\ Ports**</span><span class="sxs-lookup"><span data-stu-id="03aa2-194">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="03aa2-195">Aufrufen der [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) -Funktion, um diese Werte abzufragen.</span><span class="sxs-lookup"><span data-stu-id="03aa2-195">Call the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to query these values.</span></span>



| <span data-ttu-id="03aa2-196">Port Monitor Einstellung</span><span class="sxs-lookup"><span data-stu-id="03aa2-196">Port monitor setting</span></span>     | <span data-ttu-id="03aa2-197">Datentyp</span><span class="sxs-lookup"><span data-stu-id="03aa2-197">Data type</span></span>      | <span data-ttu-id="03aa2-198">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="03aa2-198">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03aa2-199">**Statusupdateaktivierte**</span><span class="sxs-lookup"><span data-stu-id="03aa2-199">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="03aa2-200">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="03aa2-200">**REG\_DWORD**</span></span> | <span data-ttu-id="03aa2-201">Wenn ein Wert ungleich NULL ist, wird es dem Port Monitor ermöglicht, den Spooler mit dem Port Status zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="03aa2-201">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="03aa2-202">**Statusupdateinterval**</span><span class="sxs-lookup"><span data-stu-id="03aa2-202">**StatusUpdateInterval**</span></span> | <span data-ttu-id="03aa2-203">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="03aa2-203">**REG\_DWORD**</span></span> | <span data-ttu-id="03aa2-204">Gibt das Intervall (in Minuten) an, in dem der Port Monitor den Spooler mit dem Port Status aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="03aa2-204">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="03aa2-205">In Windows 7 und höheren Versionen von Windows werden Druckaufträge, die an einen Druckserver gesendet werden, standardmäßig auf dem Client gerendert.</span><span class="sxs-lookup"><span data-stu-id="03aa2-205">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="03aa2-206">Die folgenden Werte konfigurieren das Client seitige Rendering von Druckaufträgen und können gelesen werden, wenn Sie die folgenden Werte in " *pvaluename*" festlegen.</span><span class="sxs-lookup"><span data-stu-id="03aa2-206">The following values configure client-side rendering of a print jobs and can be read if you set the following values in *pValueName*.</span></span>



| <span data-ttu-id="03aa2-207">Einstellung</span><span class="sxs-lookup"><span data-stu-id="03aa2-207">Setting</span></span>                      | <span data-ttu-id="03aa2-208">Datentyp</span><span class="sxs-lookup"><span data-stu-id="03aa2-208">Data type</span></span>      | <span data-ttu-id="03aa2-209">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03aa2-209">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03aa2-210">**EMF despoolingsetting**</span><span class="sxs-lookup"><span data-stu-id="03aa2-210">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="03aa2-211">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="03aa2-211">**REG\_DWORD**</span></span> | <span data-ttu-id="03aa2-212">Der Wert 0 (null), oder wenn dieser Wert nicht in der Registrierung vorhanden ist, aktiviert das Client seitige Standard Rendering von Druckaufträgen.</span><span class="sxs-lookup"><span data-stu-id="03aa2-212">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="03aa2-213">Der Wert 1 deaktiviert das Client seitige Rendering von Druckaufträgen.</span><span class="sxs-lookup"><span data-stu-id="03aa2-213">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="03aa2-214">**Forceclientsiderderdering**</span><span class="sxs-lookup"><span data-stu-id="03aa2-214">**ForceClientSideRendering**</span></span> | <span data-ttu-id="03aa2-215">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="03aa2-215">**REG\_DWORD**</span></span> | <span data-ttu-id="03aa2-216">Der Wert 0 oder, wenn dieser Wert nicht in der Registrierung vorhanden ist, bewirkt, dass die Druckaufträge auf dem Client gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="03aa2-216">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="03aa2-217">Wenn ein Druckauftrag nicht auf dem Client gerendert werden kann, wird er auf dem Server gerendert.</span><span class="sxs-lookup"><span data-stu-id="03aa2-217">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="03aa2-218">Wenn ein Druckauftrag nicht auf dem Server gerendert werden kann, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="03aa2-218">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="03aa2-219">Bei einem Wert von 1 werden Druckaufträge auf dem Client ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="03aa2-219">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="03aa2-220">Wenn ein Druckauftrag nicht auf dem Client gerendert werden kann, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="03aa2-220">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="03aa2-221">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03aa2-221">Requirements</span></span>



| <span data-ttu-id="03aa2-222">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03aa2-222">Requirement</span></span> | <span data-ttu-id="03aa2-223">Wert</span><span class="sxs-lookup"><span data-stu-id="03aa2-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03aa2-224">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03aa2-224">Minimum supported client</span></span><br/> | <span data-ttu-id="03aa2-225">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03aa2-225">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="03aa2-226">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03aa2-226">Minimum supported server</span></span><br/> | <span data-ttu-id="03aa2-227">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03aa2-227">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="03aa2-228">Header</span><span class="sxs-lookup"><span data-stu-id="03aa2-228">Header</span></span><br/>                   | <dl> <span data-ttu-id="03aa2-229"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03aa2-229"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="03aa2-230">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="03aa2-230">Library</span></span><br/>                  | <dl> <span data-ttu-id="03aa2-231"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03aa2-231"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="03aa2-232">DLL</span><span class="sxs-lookup"><span data-stu-id="03aa2-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03aa2-233"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="03aa2-233"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="03aa2-234">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="03aa2-234">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="03aa2-235">**Getprinterdataw** (Unicode) und **getprinterdataa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="03aa2-235">**GetPrinterDataW** (Unicode) and **GetPrinterDataA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="03aa2-236">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03aa2-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03aa2-237">Drucken</span><span class="sxs-lookup"><span data-stu-id="03aa2-237">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="03aa2-238">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="03aa2-238">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="03aa2-239">**Getprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="03aa2-239">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="03aa2-240">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="03aa2-240">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="03aa2-241">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="03aa2-241">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="03aa2-242">**Setprinterdata**</span><span class="sxs-lookup"><span data-stu-id="03aa2-242">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> <dt>

[<span data-ttu-id="03aa2-243">**Setprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="03aa2-243">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="03aa2-244">**PrintProcessor-Ober \_ Grenzen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="03aa2-244">**PRINTPROCESSOR\_CAPS\_1**</span></span>](printprocessor-caps-1.md)
</dt> </dl>

 

