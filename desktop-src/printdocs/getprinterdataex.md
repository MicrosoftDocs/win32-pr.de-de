---
description: Die getprinterdataex-Funktion ruft Konfigurationsdaten für den angegebenen Drucker oder Druckserver ab.
ms.assetid: 5d9183a7-97cc-46de-848e-e37ce51396eb
title: Getprinterdataex-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDataEx
- GetPrinterDataExA
- GetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: bdadf2e1259445ca5285e5b12bc906140a137cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759661"
---
# <a name="getprinterdataex-function"></a><span data-ttu-id="37ada-103">Getprinterdataex-Funktion</span><span class="sxs-lookup"><span data-stu-id="37ada-103">GetPrinterDataEx function</span></span>

<span data-ttu-id="37ada-104">Die **getprinterdataex** -Funktion ruft Konfigurationsdaten für den angegebenen Drucker oder Druckserver ab.</span><span class="sxs-lookup"><span data-stu-id="37ada-104">The **GetPrinterDataEx** function retrieves configuration data for the specified printer or print server.</span></span> <span data-ttu-id="37ada-105">**Getprinterdataex** kann Werte abrufen, die von der [**setprinterdata**](setprinterdata.md) -Funktion gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="37ada-105">**GetPrinterDataEx** can retrieve values that the [**SetPrinterData**](setprinterdata.md) function stored.</span></span> <span data-ttu-id="37ada-106">Außerdem kann **getprinterdataex** Werte abrufen, die von der [**setprinterdataex**](setprinterdataex.md) -Funktion unter einem angegebenen Schlüssel gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="37ada-106">In addition, **GetPrinterDataEx** can retrieve values that the [**SetPrinterDataEx**](setprinterdataex.md) function stored under a specified key.</span></span>

## <a name="syntax"></a><span data-ttu-id="37ada-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="37ada-107">Syntax</span></span>


```C++
DWORD GetPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _In_  LPCTSTR pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="37ada-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="37ada-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37ada-109">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37ada-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ada-110">Ein Handle für den Drucker oder Druckserver, für das die Funktion Konfigurationsdaten abruft.</span><span class="sxs-lookup"><span data-stu-id="37ada-110">A handle to the printer or print server for which the function retrieves configuration data.</span></span> <span data-ttu-id="37ada-111">Verwenden Sie die Funktion " [**OpenPrinter**](openprinter.md)", " [**OpenPrinter2**](openprinter2.md)" oder " [**addprinter**](addprinter.md) ", um ein Drucker Handle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="37ada-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="37ada-112">*pkeyname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37ada-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ada-113">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Schlüssel mit dem abzurufenden Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="37ada-113">A pointer to a null-terminated string that specifies the key containing the value to be retrieved.</span></span> <span data-ttu-id="37ada-114">Verwenden Sie den umgekehrten Schrägstrich ( \\ ) als Trennzeichen, um einen Pfad anzugeben, der über mindestens einen Unterschlüssel verfügt.</span><span class="sxs-lookup"><span data-stu-id="37ada-114">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="37ada-115">Wenn *hprinter* ein Handle für einen Drucker ist und *pkeyname* **null** oder eine leere Zeichenfolge ist, gibt **getprinterdataex** einen **\_ ungültigen \_ Parameter** zurück.</span><span class="sxs-lookup"><span data-stu-id="37ada-115">If *hPrinter* is a handle to a printer and *pKeyName* is **NULL** or an empty string, **GetPrinterDataEx** returns **ERROR\_INVALID\_PARAMETER**.</span></span>

<span data-ttu-id="37ada-116">Wenn *hprinter* ein Handle für einen Druckserver ist, wird *pkeyname* ignoriert.</span><span class="sxs-lookup"><span data-stu-id="37ada-116">If *hPrinter* is a handle to a print server, *pKeyName* is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="37ada-117">*pvaluename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37ada-117">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ada-118">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die abzurufenden Daten identifiziert.</span><span class="sxs-lookup"><span data-stu-id="37ada-118">A pointer to a null-terminated string that identifies the data to retrieve.</span></span>

<span data-ttu-id="37ada-119">Bei Druckern gibt diese Zeichenfolge den Namen eines Werts unter dem *pkeyname* -Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="37ada-119">For printers, this string specifies the name of a value under the *pKeyName* key.</span></span>

<span data-ttu-id="37ada-120">Bei Druckservern handelt es sich bei dieser Zeichenfolge um eine der vordefinierten Zeichen folgen, die im folgenden Abschnitt mit Hinweisen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="37ada-120">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="37ada-121">*pType* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="37ada-121">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37ada-122">Ein Zeiger auf eine Variable, die den Typ der im-Wert gespeicherten Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="37ada-122">A pointer to a variable that receives the type of data stored in the value.</span></span> <span data-ttu-id="37ada-123">Die-Funktion gibt den Typ zurück, der im [**setprinterdataex**](setprinterdataex.md) -Befehl angegeben wurde, als die Daten gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="37ada-123">The function returns the type specified in the [**SetPrinterDataEx**](setprinterdataex.md) call when the data was stored.</span></span> <span data-ttu-id="37ada-124">Dieser Parameter kann **null** sein, wenn Sie die Informationen nicht benötigen.</span><span class="sxs-lookup"><span data-stu-id="37ada-124">This parameter can be **NULL** if you don't need the information.</span></span> <span data-ttu-id="37ada-125">**Getprinterdataex** übergibt *pType* als den *lpdwtype* -Parameter eines [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) -Funktions Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="37ada-125">**GetPrinterDataEx** passes *pType* on as the *lpdwType* parameter of a [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function call.</span></span>

</dd> <dt>

<span data-ttu-id="37ada-126">*pData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="37ada-126">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37ada-127">Ein Zeiger auf einen Puffer, der die Konfigurationsdaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="37ada-127">A pointer to a buffer that receives the configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="37ada-128">*nSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37ada-128">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ada-129">Die Größe (in Bytes) des Puffers, auf den *pData* zeigt.</span><span class="sxs-lookup"><span data-stu-id="37ada-129">The size, in bytes, of the buffer pointed to by *pData*.</span></span>

</dd> <dt>

<span data-ttu-id="37ada-130">*pcbbenötigte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="37ada-130">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37ada-131">Ein Zeiger auf eine Variable, die die Größe der Konfigurationsdaten in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="37ada-131">A pointer to a variable that receives the size, in bytes, of the configuration data.</span></span> <span data-ttu-id="37ada-132">Wenn die von *nSize* angegebene Puffergröße zu klein ist, gibt die Funktion **Fehler \_ Weitere \_ Daten** zurück, und *pcbrequired* gibt die erforderliche Puffergröße an.</span><span class="sxs-lookup"><span data-stu-id="37ada-132">If the buffer size specified by *nSize* is too small, the function returns **ERROR\_MORE\_DATA**, and *pcbNeeded* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37ada-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37ada-133">Return value</span></span>

<span data-ttu-id="37ada-134">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **Fehler \_ erfolgreich**.</span><span class="sxs-lookup"><span data-stu-id="37ada-134">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="37ada-135">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="37ada-135">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37ada-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37ada-136">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="37ada-137">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="37ada-137">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="37ada-138">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="37ada-138">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="37ada-139">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="37ada-139">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="37ada-140">**Getprinterdataex** ruft Drucker Konfigurationsdaten ab, die von den Funktionen [**setprinterdataex**](setprinterdataex.md) und [**setprinterdata**](setprinterdata.md) festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="37ada-140">**GetPrinterDataEx** retrieves printer-configuration data that was set by the [**SetPrinterDataEx**](setprinterdataex.md) and [**SetPrinterData**](setprinterdata.md) functions.</span></span>

<span data-ttu-id="37ada-141">Der Aufruf von **getprinterdataex** mit dem *pkeyname* -Parameter, der auf "printerdriverdata" festgelegt ist, entspricht dem Aufrufen der [**getprinterdata**](getprinterdata.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="37ada-141">Calling **GetPrinterDataEx** with the *pKeyName* parameter set to "PrinterDriverData" is equivalent to calling the [**GetPrinterData**](getprinterdata.md) function.</span></span>

<span data-ttu-id="37ada-142">Wenn *hprinter* ein Handle für einen Druckserver ist, kann *pvaluename* einen der folgenden vordefinierten Werte angeben.</span><span class="sxs-lookup"><span data-stu-id="37ada-142">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="37ada-143">Wert</span><span class="sxs-lookup"><span data-stu-id="37ada-143">Value</span></span>                                                               | <span data-ttu-id="37ada-144">Kommentare</span><span class="sxs-lookup"><span data-stu-id="37ada-144">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37ada-145">**splreg \_ Allow \_ User \_ manageforms**</span><span class="sxs-lookup"><span data-stu-id="37ada-145">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="37ada-146">Windows XP mit Service Pack 2 (SP2) und höher</span><span class="sxs-lookup"><span data-stu-id="37ada-146">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="37ada-147">Windows Server 2003 mit Service Pack 1 (SP1) und höher</span><span class="sxs-lookup"><span data-stu-id="37ada-147">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="37ada-148">**splreg- \_ Architektur**</span><span class="sxs-lookup"><span data-stu-id="37ada-148">**SPLREG\_ARCHITECTURE**</span></span>                                            |                                                                                                                                                                                                                                 |
| <span data-ttu-id="37ada-149">**splreg \_ Beep \_ aktiviert**</span><span class="sxs-lookup"><span data-stu-id="37ada-149">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="37ada-150">**splreg \_ - \_ Standard \_ Spoolverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="37ada-150">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="37ada-151">**Name der splreg \_ DNS- \_ Maschine \_**</span><span class="sxs-lookup"><span data-stu-id="37ada-151">**SPLREG\_DNS\_MACHINE\_NAME**</span></span>                                      |                                                                                                                                                                                                                                 |
| <span data-ttu-id="37ada-152">**splreg \_ DS \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="37ada-152">**SPLREG\_DS\_PRESENT**</span></span>                                             | <span data-ttu-id="37ada-153">Bei erfolgreicher Rückgabe enthält *pData* 0x0001, wenn sich der Computer in einer DS-Domäne befindet, andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="37ada-153">On successful return, *pData* contains 0x0001 if the machine is on a DS domain, 0 otherwise.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="37ada-154">**splreg \_ DS \_ \_ für \_ Benutzer vorhanden**</span><span class="sxs-lookup"><span data-stu-id="37ada-154">**SPLREG\_DS\_PRESENT\_FOR\_USER**</span></span>                                  | <span data-ttu-id="37ada-155">Bei erfolgreicher Rückgabe enthält *pData* 0x0001, wenn der Benutzer bei einer DS-Domäne angemeldet ist, andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="37ada-155">On successful return, *pData* contains 0x0001 if the user is logged onto a DS domain, 0 otherwise.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="37ada-156">**splreg- \_ Ereignis \_ Protokoll**</span><span class="sxs-lookup"><span data-stu-id="37ada-156">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="37ada-157">**splreg- \_ Haupt \_ Version**</span><span class="sxs-lookup"><span data-stu-id="37ada-157">**SPLREG\_MAJOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="37ada-158">**splreg- \_ neben \_ Version**</span><span class="sxs-lookup"><span data-stu-id="37ada-158">**SPLREG\_MINOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="37ada-159">**splreg \_ net- \_ Popup**</span><span class="sxs-lookup"><span data-stu-id="37ada-159">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="37ada-160">Wird in Windows Server 2003 und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37ada-160">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="37ada-161">**splreg \_ net- \_ Popup \_ auf \_ Computer**</span><span class="sxs-lookup"><span data-stu-id="37ada-161">**SPLREG\_NET\_POPUP\_TO\_COMPUTER**</span></span>                                | <span data-ttu-id="37ada-162">Bei erfolgreicher Rückgabe enthält *pData* 1, wenn Auftrags Benachrichtigungen an den Client Computer gesendet werden sollen, oder 0, wenn Auftrags Benachrichtigungen an den Benutzer gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="37ada-162">On successful return, *pData* contains 1 if job notifications should be sent to the client computer, or 0 if job notifications are to be sent to the user.</span></span><br/> <span data-ttu-id="37ada-163">Wird in Windows Server 2003 und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37ada-163">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="37ada-164">**splreg \_ OS- \_ Version**</span><span class="sxs-lookup"><span data-stu-id="37ada-164">**SPLREG\_OS\_VERSION**</span></span>                                             | <span data-ttu-id="37ada-165">Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="37ada-165">Windows XP and later</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="37ada-166">**splreg \_ OS \_ versionex**</span><span class="sxs-lookup"><span data-stu-id="37ada-166">**SPLREG\_OS\_VERSIONEX**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="37ada-167">**standardmäßige \_ \_ Thread \_ Priorität \_ für den splreg-Port**</span><span class="sxs-lookup"><span data-stu-id="37ada-167">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="37ada-168">**\_ \_ Thread \_ Priorität des splreg-Ports**</span><span class="sxs-lookup"><span data-stu-id="37ada-168">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="37ada-169">**splreg \_ - \_ drucktreiberisolations- \_ \_ Gruppen**</span><span class="sxs-lookup"><span data-stu-id="37ada-169">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="37ada-170">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="37ada-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="37ada-171">**Dauer der \_ Druck \_ Treiber \_ Isolation \_ \_ vor \_ der Wiederverwendung**</span><span class="sxs-lookup"><span data-stu-id="37ada-171">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="37ada-172">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="37ada-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="37ada-173">**maximale Anzahl von Objekten für die \_ Druck \_ Treiber \_ Isolation \_ \_ \_ vor \_ der Wiederverwendung**</span><span class="sxs-lookup"><span data-stu-id="37ada-173">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="37ada-174">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="37ada-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="37ada-175">**Leerlauf Timeout der splreg- \_ Druck \_ Treiber \_ Isolation \_ \_**</span><span class="sxs-lookup"><span data-stu-id="37ada-175">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="37ada-176">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="37ada-176">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="37ada-177">**Ausführungs Richtlinie der splreg- \_ Druck \_ Treiber \_ Isolation \_ \_**</span><span class="sxs-lookup"><span data-stu-id="37ada-177">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="37ada-178">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="37ada-178">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="37ada-179">**Außerkraftsetzungs Richtlinie für die splreg- \_ Druck \_ Treiber \_ Isolation \_ \_**</span><span class="sxs-lookup"><span data-stu-id="37ada-179">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="37ada-180">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="37ada-180">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="37ada-181">**splreg- \_ Remote \_ Fax**</span><span class="sxs-lookup"><span data-stu-id="37ada-181">**SPLREG\_REMOTE\_FAX**</span></span>                                             | <span data-ttu-id="37ada-182">Bei erfolgreicher Rückgabe enthält *pData* 0x0001, wenn der Faxdienst Remote Clients unterstützt, andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="37ada-182">On successful return, *pData* contains 0x0001 if the FAX service supports remote clients, 0 otherwise.</span></span><br/>                                                                                                               |
| <span data-ttu-id="37ada-183">**splreg- \_ Wiederholungs- \_ Popup**</span><span class="sxs-lookup"><span data-stu-id="37ada-183">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="37ada-184">Bei erfolgreicher Rückgabe enthält *pData* 1, wenn der Server für die Wiederherstellung von Popup Fenstern für alle Aufträge festgelegt ist, oder 0, wenn der Server keine Popup Fenster für alle Aufträge erneut versucht.</span><span class="sxs-lookup"><span data-stu-id="37ada-184">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="37ada-185">Wird in Windows Server 2003 und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37ada-185">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="37ada-186">**splreg \_ Scheduler \_ Thread \_ Priorität**</span><span class="sxs-lookup"><span data-stu-id="37ada-186">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="37ada-187">**standardmäßige \_ \_ Thread \_ Priorität \_ für den splreg-Scheduler**</span><span class="sxs-lookup"><span data-stu-id="37ada-187">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="37ada-188">**splreg \_ websharemgmt**</span><span class="sxs-lookup"><span data-stu-id="37ada-188">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="37ada-189">Windows Server 2003 und höher</span><span class="sxs-lookup"><span data-stu-id="37ada-189">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="37ada-190">Die folgenden Werte von *pvaluename* geben das Druck Verhalten des Pools an, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="37ada-190">The following values of *pValueName* indicate the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="37ada-191">Wert</span><span class="sxs-lookup"><span data-stu-id="37ada-191">Value</span></span>                                       | <span data-ttu-id="37ada-192">Kommentare</span><span class="sxs-lookup"><span data-stu-id="37ada-192">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37ada-193">**\_Fehler beim Fehler "splreg Restart \_ Job \_ on \_ Pool \_ ".**</span><span class="sxs-lookup"><span data-stu-id="37ada-193">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="37ada-194">Der Wert von *pData* gibt die Zeit in Sekunden an, nach der ein Auftrag an einem anderen Port neu gestartet wird, nachdem ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="37ada-194">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="37ada-195">Diese Einstellung wird mit dem **Auftrag "splreg \_ Restart" \_ \_ bei \_ \_ aktiviertem Pool** verwendet.</span><span class="sxs-lookup"><span data-stu-id="37ada-195">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="37ada-196">**splreg- \_ Neustart \_ Auftrag \_ für \_ Pool \_ aktiviert**</span><span class="sxs-lookup"><span data-stu-id="37ada-196">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="37ada-197">Ein Wert ungleich 0 (null) in *pData* gibt an, dass der **Fehler "splreg \_ Restart \_ Job \_ on \_ Pool \_** " aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="37ada-197">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="37ada-198">Die im Fehler des **Auftrags "splreg \_ Restart \_ Job \_ on \_ Pool \_** " angegebene Zeit ist eine minimale Zeit.</span><span class="sxs-lookup"><span data-stu-id="37ada-198">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="37ada-199">Die tatsächliche Zeit kann je nach den folgenden Port Monitoreinstellungen, bei denen es sich um Registrierungs Werte unter diesem Registrierungsschlüssel handelt, länger sein:</span><span class="sxs-lookup"><span data-stu-id="37ada-199">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="37ada-200">**HKLM \\ System \\ CurrentControlSet \\ Control \\ Print \\ Monitors \\ < *Monitorname* > \\ Ports**</span><span class="sxs-lookup"><span data-stu-id="37ada-200">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="37ada-201">Aufrufen der [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) -Funktion, um diese Werte abzufragen.</span><span class="sxs-lookup"><span data-stu-id="37ada-201">Call the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to query these values.</span></span>



| <span data-ttu-id="37ada-202">Port Monitor Einstellung</span><span class="sxs-lookup"><span data-stu-id="37ada-202">Port monitor setting</span></span>     | <span data-ttu-id="37ada-203">Datentyp</span><span class="sxs-lookup"><span data-stu-id="37ada-203">Data type</span></span>      | <span data-ttu-id="37ada-204">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="37ada-204">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37ada-205">**Statusupdateaktivierte**</span><span class="sxs-lookup"><span data-stu-id="37ada-205">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="37ada-206">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="37ada-206">**REG\_DWORD**</span></span> | <span data-ttu-id="37ada-207">Wenn ein Wert ungleich NULL ist, wird es dem Port Monitor ermöglicht, den Spooler mit dem Port Status zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="37ada-207">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="37ada-208">**Statusupdateinterval**</span><span class="sxs-lookup"><span data-stu-id="37ada-208">**StatusUpdateInterval**</span></span> | <span data-ttu-id="37ada-209">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="37ada-209">**REG\_DWORD**</span></span> | <span data-ttu-id="37ada-210">Gibt das Intervall (in Minuten) an, in dem der Port Monitor den Spooler mit dem Port Status aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37ada-210">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="37ada-211">Wenn *pkeyname* einer der vordefinierten Verzeichnisdienst (DS)-Schlüssel ist (siehe [**SetPrinter**](setprinter.md)) und *pvaluename* ein Komma (",") enthält, ist der Teil von " *pvaluename* " vor dem Komma der Wertname, und der Teil von " *pvaluename* " rechts neben dem Komma ist die DS-Eigenschaften-OID.</span><span class="sxs-lookup"><span data-stu-id="37ada-211">If *pKeyName* is one of the predefined Directory Service (DS) keys (see [**SetPrinter**](setprinter.md)) and *pValueName* contains a comma (','), then the portion of *pValueName* before the comma is the value name and the portion of *pValueName* to the right of the comma is the DS Property OID.</span></span> <span data-ttu-id="37ada-212">Ein Unterschlüssel namens OID wird erstellt, und ein neuer Wert, der aus dem Wertnamen und der OID besteht, wird unter dem OID-Schlüssel eingegeben.</span><span class="sxs-lookup"><span data-stu-id="37ada-212">A subkey called OID is created and a new value that consists of the value name and OID is entered under the OID key.</span></span> <span data-ttu-id="37ada-213">[**Setprinterdataex**](setprinterdataex.md) fügt auch den Wertnamen und die Daten unter dem DS-Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="37ada-213">[**SetPrinterDataEx**](setprinterdataex.md) also adds the value name and data under the DS key.</span></span>

<span data-ttu-id="37ada-214">In Windows 7 und höheren Versionen von Windows werden Druckaufträge, die an einen Druckserver gesendet werden, standardmäßig auf dem Client gerendert.</span><span class="sxs-lookup"><span data-stu-id="37ada-214">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="37ada-215">Die Konfiguration des Client seitigen Renderings für einen Drucker kann gelesen werden, indem *pkeyname* auf "printerdriverdata" und *pvaluename* auf den Einstellungs Wert in der folgenden Tabelle festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="37ada-215">The configuration of client-side rendering for a printer can be read by setting *pKeyName* to "PrinterDriverData" and *pValueName* to the setting value in the following table.</span></span>



| <span data-ttu-id="37ada-216">Einstellung</span><span class="sxs-lookup"><span data-stu-id="37ada-216">Setting</span></span>                      | <span data-ttu-id="37ada-217">Datentyp</span><span class="sxs-lookup"><span data-stu-id="37ada-217">Data type</span></span>      | <span data-ttu-id="37ada-218">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37ada-218">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37ada-219">**EMF despoolingsetting**</span><span class="sxs-lookup"><span data-stu-id="37ada-219">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="37ada-220">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="37ada-220">**REG\_DWORD**</span></span> | <span data-ttu-id="37ada-221">Der Wert 0 (null), oder wenn dieser Wert nicht in der Registrierung vorhanden ist, aktiviert das Client seitige Standard Rendering von Druckaufträgen.</span><span class="sxs-lookup"><span data-stu-id="37ada-221">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="37ada-222">Der Wert 1 deaktiviert das Client seitige Rendering von Druckaufträgen.</span><span class="sxs-lookup"><span data-stu-id="37ada-222">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="37ada-223">**Forceclientsiderderdering**</span><span class="sxs-lookup"><span data-stu-id="37ada-223">**ForceClientSideRendering**</span></span> | <span data-ttu-id="37ada-224">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="37ada-224">**REG\_DWORD**</span></span> | <span data-ttu-id="37ada-225">Der Wert 0 oder, wenn dieser Wert nicht in der Registrierung vorhanden ist, bewirkt, dass die Druckaufträge auf dem Client gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="37ada-225">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="37ada-226">Wenn ein Druckauftrag nicht auf dem Client gerendert werden kann, wird er auf dem Server gerendert.</span><span class="sxs-lookup"><span data-stu-id="37ada-226">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="37ada-227">Wenn ein Druckauftrag nicht auf dem Server gerendert werden kann, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="37ada-227">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="37ada-228">Bei einem Wert von 1 werden Druckaufträge auf dem Client ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="37ada-228">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="37ada-229">Wenn ein Druckauftrag nicht auf dem Client gerendert werden kann, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="37ada-229">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="37ada-230">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37ada-230">Requirements</span></span>



| <span data-ttu-id="37ada-231">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37ada-231">Requirement</span></span> | <span data-ttu-id="37ada-232">Wert</span><span class="sxs-lookup"><span data-stu-id="37ada-232">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37ada-233">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37ada-233">Minimum supported client</span></span><br/> | <span data-ttu-id="37ada-234">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37ada-234">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="37ada-235">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37ada-235">Minimum supported server</span></span><br/> | <span data-ttu-id="37ada-236">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37ada-236">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="37ada-237">Header</span><span class="sxs-lookup"><span data-stu-id="37ada-237">Header</span></span><br/>                   | <dl> <span data-ttu-id="37ada-238"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37ada-238"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="37ada-239">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="37ada-239">Library</span></span><br/>                  | <dl> <span data-ttu-id="37ada-240"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37ada-240"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="37ada-241">DLL</span><span class="sxs-lookup"><span data-stu-id="37ada-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37ada-242"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="37ada-242"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="37ada-243">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="37ada-243">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="37ada-244">**Getprinterdataexw** (Unicode) und **getprinterdataexa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="37ada-244">**GetPrinterDataExW** (Unicode) and **GetPrinterDataExA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="37ada-245">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37ada-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37ada-246">Drucken</span><span class="sxs-lookup"><span data-stu-id="37ada-246">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="37ada-247">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="37ada-247">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="37ada-248">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="37ada-248">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="37ada-249">**Setprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="37ada-249">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

