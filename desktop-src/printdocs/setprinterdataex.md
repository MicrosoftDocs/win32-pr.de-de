---
description: Die Funktion setprinterdataex legt die Konfigurationsdaten für einen Drucker oder Druckserver fest. Die-Funktion speichert die Konfigurationsdaten unter dem Drucker Registrierungsschlüssel.
ms.assetid: b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1
title: Setprinterdataex-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterDataEx
- SetPrinterDataExA
- SetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 9f384c9c9d6f0d956264b45ec8b52043ad20e897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217839"
---
# <a name="setprinterdataex-function"></a><span data-ttu-id="1fc37-104">Setprinterdataex-Funktion</span><span class="sxs-lookup"><span data-stu-id="1fc37-104">SetPrinterDataEx function</span></span>

<span data-ttu-id="1fc37-105">Die Funktion **setprinterdataex** legt die Konfigurationsdaten für einen Drucker oder Druckserver fest.</span><span class="sxs-lookup"><span data-stu-id="1fc37-105">The **SetPrinterDataEx** function sets the configuration data for a printer or print server.</span></span> <span data-ttu-id="1fc37-106">Die-Funktion speichert die Konfigurationsdaten unter dem-Registrierungsschlüssel des Druckers.</span><span class="sxs-lookup"><span data-stu-id="1fc37-106">The function stores the configuration data under the printer's registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc37-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fc37-107">Syntax</span></span>


```C++
DWORD SetPrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName,
  _In_ DWORD   Type,
  _In_ LPBYTE  pData,
  _In_ DWORD   cbData
);
```



## <a name="parameters"></a><span data-ttu-id="1fc37-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fc37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fc37-109">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1fc37-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc37-110">Ein Handle für den Drucker oder Druckserver, für das die Funktion Konfigurationsdaten festlegt.</span><span class="sxs-lookup"><span data-stu-id="1fc37-110">A handle to the printer or print server for which the function sets configuration data.</span></span> <span data-ttu-id="1fc37-111">Verwenden Sie die Funktion " [**OpenPrinter**](openprinter.md)", " [**OpenPrinter2**](openprinter2.md)" oder " [**addprinter**](addprinter.md) ", um ein Drucker Handle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1fc37-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="1fc37-112">*pkeyname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1fc37-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc37-113">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Schlüssel mit dem festzulegenden Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="1fc37-113">A pointer to a null-terminated string that specifies the key containing the value to set.</span></span> <span data-ttu-id="1fc37-114">Wenn die angegebenen Schlüssel oder Unterschlüssel nicht vorhanden sind, werden Sie von der Funktion erstellt.</span><span class="sxs-lookup"><span data-stu-id="1fc37-114">If the specified key or subkeys do not exist, the function creates them.</span></span>

<span data-ttu-id="1fc37-115">Zum Speichern von Konfigurationsdaten, die im Verzeichnisdienst (DS) veröffentlicht werden können, geben Sie einen der folgenden vordefinierten Registrierungsschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="1fc37-115">To store configuration data that can be published in the directory service (DS), specify one of the following predefined registry keys.</span></span>



| <span data-ttu-id="1fc37-116">Wert</span><span class="sxs-lookup"><span data-stu-id="1fc37-116">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="1fc37-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1fc37-117">Meaning</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="SPLDS_DRIVER_KEY"></span><span id="splds_driver_key"></span><dl> <span data-ttu-id="1fc37-118"><dt>**SPLDS_DRIVER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="1fc37-118"><dt>**SPLDS_DRIVER_KEY**</dt></span></span> </dl>    | <span data-ttu-id="1fc37-119">Druckertreiber verwenden diesen Schlüssel zum Speichern von Treiber Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1fc37-119">Printer drivers use this key to store driver properties.</span></span><br/>                             |
| <span id="SPLDS_SPOOLER_KEY"></span><span id="splds_spooler_key"></span><dl> <span data-ttu-id="1fc37-120"><dt>**SPLDS_SPOOLER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="1fc37-120"><dt>**SPLDS_SPOOLER_KEY**</dt></span></span> </dl> | <span data-ttu-id="1fc37-121">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="1fc37-121">Reserved.</span></span> <span data-ttu-id="1fc37-122">Wird nur vom Druck Spooler verwendet, um Eigenschaften interner Spooler zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1fc37-122">Used only by the print spooler to store internal spooler properties.</span></span><br/>       |
| <span id="SPLDS_USER_KEY"></span><span id="splds_user_key"></span><dl> <span data-ttu-id="1fc37-123"><dt>**SPLDS_USER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="1fc37-123"><dt>**SPLDS_USER_KEY**</dt></span></span> </dl>          | <span data-ttu-id="1fc37-124">Anwendungen verwenden diesen Schlüssel zum Speichern von Druckereigenschaften, z. b. Drucker Medienobjekt Nummern.</span><span class="sxs-lookup"><span data-stu-id="1fc37-124">Applications use this key to store printer properties such as printer asset numbers.</span></span><br/> |



 

<span data-ttu-id="1fc37-125">Werte, die unter dem SPLDS_USER_KEY Schlüssel gespeichert werden, werden nur im Verzeichnisdienst veröffentlicht, wenn im Schema eine entsprechende Eigenschaft vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1fc37-125">Values that are stored under the SPLDS_USER_KEY key are published in the directory service only if there is a corresponding property in the schema.</span></span> <span data-ttu-id="1fc37-126">Ein Domänen Administrator muss die-Eigenschaft erstellen, wenn er nicht bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1fc37-126">A domain administrator must create the property if it doesn't already exist.</span></span> <span data-ttu-id="1fc37-127">Um eine benutzerdefinierte Eigenschaft zu veröffentlichen, nachdem Sie **setprinterdataex** zum Hinzufügen oder Ändern eines Werts verwendet haben, nennen Sie [**SetPrinter**](setprinter.md) mit *Level* = 7, und der **dwAction** -Member von [**PRINTER_INFO_7**](printer-info-7.md) auf **DSPRINT_UPDATE** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1fc37-127">To publish a user-defined property after you use **SetPrinterDataEx** to add or change a value, call [**SetPrinter**](setprinter.md) with *Level* = 7 and with the **dwAction** member of [**PRINTER_INFO_7**](printer-info-7.md) set to **DSPRINT_UPDATE**.</span></span>

<span data-ttu-id="1fc37-128">Sie können andere Schlüssel angeben, um nicht-DS-Konfigurationsdaten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1fc37-128">You can specify other keys to store non-DS configuration data.</span></span> <span data-ttu-id="1fc37-129">Verwenden Sie den umgekehrten Schrägstrich ( \\ ) als Trennzeichen, um einen Pfad anzugeben, der über mindestens einen Unterschlüssel verfügt.</span><span class="sxs-lookup"><span data-stu-id="1fc37-129">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="1fc37-130">Wenn *hprinter* ein Handle für einen Drucker ist und *pkeyname* **null** oder eine leere Zeichenfolge ist, gibt **setprinterdataex** **ERROR_INVALID_PARAMETER** zurück.</span><span class="sxs-lookup"><span data-stu-id="1fc37-130">If *hPrinter* is a handle to a printer and *pKeyName* is **NULL** or an empty string, **SetPrinterDataEx** returns **ERROR_INVALID_PARAMETER**.</span></span>

<span data-ttu-id="1fc37-131">Wenn *hprinter* ein Handle für einen Druckserver ist, wird *pkeyname* ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1fc37-131">If *hPrinter* is a handle to a print server, *pKeyName* is ignored.</span></span>

<span data-ttu-id="1fc37-132">Verwenden Sie **SPLDS_SPOOLER_KEY** nicht.</span><span class="sxs-lookup"><span data-stu-id="1fc37-132">Do not use **SPLDS_SPOOLER_KEY**.</span></span> <span data-ttu-id="1fc37-133">Verwenden Sie [**SetPrinter**](setprinter.md) mit *Level* = 2, um die Eigenschaften des Spooler-Druckers zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1fc37-133">To change the spooler printer properties, use [**SetPrinter**](setprinter.md) with *Level* = 2.</span></span>

</dd> <dt>

<span data-ttu-id="1fc37-134">*pvaluename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1fc37-134">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc37-135">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die festzulegenden Daten identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1fc37-135">A pointer to a null-terminated string that identifies the data to set.</span></span>

<span data-ttu-id="1fc37-136">Bei Druckern gibt diese Zeichenfolge den Namen eines Werts unter dem *pkeyname* -Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="1fc37-136">For printers, this string specifies the name of a value under the *pKeyName* key.</span></span>

<span data-ttu-id="1fc37-137">Bei Druckservern handelt es sich bei dieser Zeichenfolge um eine der vordefinierten Zeichen folgen, die im folgenden Abschnitt mit Hinweisen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="1fc37-137">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="1fc37-138">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1fc37-138">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc37-139">Ein Code, der den Typ der Daten angibt, auf die der *pData* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="1fc37-139">A code indicating the type of data pointed to by the *pData* parameter.</span></span> <span data-ttu-id="1fc37-140">Eine Liste der möglichen Typcodes finden Sie unter [Registrierungs Werttypen](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="1fc37-140">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

<span data-ttu-id="1fc37-141">Wenn " *pkeyname* " einen der vordefinierten Verzeichnisdienst Schlüssel angibt, muss der *Typ* " **REG_SZ**", " **REG_MULTI_SZ**", " **REG_DWORD**" oder " **REG_BINARY**" lauten.</span><span class="sxs-lookup"><span data-stu-id="1fc37-141">If *pKeyName* specifies one of the predefined directory service keys, *Type* must be **REG_SZ**, **REG_MULTI_SZ**, **REG_DWORD**, or **REG_BINARY**.</span></span> <span data-ttu-id="1fc37-142">Wenn **REG_BINARY** verwendet wird, müssen *cbData* gleich 1 sein, und der Verzeichnisdienst behandelt die Daten als booleschen Wert.</span><span class="sxs-lookup"><span data-stu-id="1fc37-142">If **REG_BINARY** is used, *cbData* must be equal to 1, and the directory service treats the data as a Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="1fc37-143">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1fc37-143">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc37-144">Ein Zeiger auf einen Puffer, der die Drucker Konfigurationsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="1fc37-144">A pointer to a buffer that contains the printer configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="1fc37-145">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1fc37-145">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc37-146">Die Größe des Arrays in Bytes.</span><span class="sxs-lookup"><span data-stu-id="1fc37-146">The size, in bytes, of the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fc37-147">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1fc37-147">Return value</span></span>

<span data-ttu-id="1fc37-148">Wenn die Funktion erfolgreich ausgeführt wird, wird der Rückgabewert **ERROR_SUCCESS**.</span><span class="sxs-lookup"><span data-stu-id="1fc37-148">If the function succeeds, the return value is **ERROR_SUCCESS**.</span></span>

<span data-ttu-id="1fc37-149">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="1fc37-149">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fc37-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1fc37-150">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1fc37-151">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1fc37-151">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="1fc37-152">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="1fc37-152">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="1fc37-153">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="1fc37-153">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="1fc37-154">Um vorhandene Konfigurationsdaten für einen Drucker oder Druck Spooler abzurufen, rufen Sie die [**getprinterdataex**](getprinterdataex.md) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="1fc37-154">To retrieve existing configuration data for a printer or print spooler, call the [**GetPrinterDataEx**](getprinterdataex.md) function.</span></span>

<span data-ttu-id="1fc37-155">Das Aufrufen von **setprinterdataex** mit dem *pkeyname* -Parameter, der auf "printerdriverdata" festgelegt ist, entspricht dem Aufrufen der [**setprinterdata**](setprinterdata.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="1fc37-155">Calling **SetPrinterDataEx** with the *pKeyName* parameter set to "PrinterDriverData" is equivalent to calling the [**SetPrinterData**](setprinterdata.md) function.</span></span>

<span data-ttu-id="1fc37-156">Wenn *hprinter* ein Handle für einen Druckserver ist, kann *pvaluename* einen der folgenden vordefinierten Werte angeben.</span><span class="sxs-lookup"><span data-stu-id="1fc37-156">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="1fc37-157">Wert</span><span class="sxs-lookup"><span data-stu-id="1fc37-157">Value</span></span>                                                               | <span data-ttu-id="1fc37-158">Kommentare</span><span class="sxs-lookup"><span data-stu-id="1fc37-158">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc37-159">**SPLREG_ALLOW_USER_MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="1fc37-159">**SPLREG_ALLOW_USER_MANAGEFORMS**</span></span>                                | <span data-ttu-id="1fc37-160">Windows XP mit Service Pack 2 (SP2) und höher</span><span class="sxs-lookup"><span data-stu-id="1fc37-160">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="1fc37-161">Windows Server 2003 mit Service Pack 1 (SP1) und höher</span><span class="sxs-lookup"><span data-stu-id="1fc37-161">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="1fc37-162">**SPLREG_BEEP_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="1fc37-162">**SPLREG_BEEP_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="1fc37-163">**SPLREG_DEFAULT_SPOOL_DIRECTORY**</span><span class="sxs-lookup"><span data-stu-id="1fc37-163">**SPLREG_DEFAULT_SPOOL_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="1fc37-164">**SPLREG_EVENT_LOG**</span><span class="sxs-lookup"><span data-stu-id="1fc37-164">**SPLREG_EVENT_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="1fc37-165">**SPLREG_NET_POPUP**</span><span class="sxs-lookup"><span data-stu-id="1fc37-165">**SPLREG_NET_POPUP**</span></span>                                              | <span data-ttu-id="1fc37-166">Wird in Windows Server 2003 und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1fc37-166">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="1fc37-167">**SPLREG_PORT_THREAD_PRIORITY_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="1fc37-167">**SPLREG_PORT_THREAD_PRIORITY_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="1fc37-168">**SPLREG_PORT_THREAD_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="1fc37-168">**SPLREG_PORT_THREAD_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="1fc37-169">**SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**</span><span class="sxs-lookup"><span data-stu-id="1fc37-169">**SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**</span></span>                        | <span data-ttu-id="1fc37-170">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="1fc37-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="1fc37-171">**SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**</span><span class="sxs-lookup"><span data-stu-id="1fc37-171">**SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**</span></span>         | <span data-ttu-id="1fc37-172">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="1fc37-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="1fc37-173">**SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE**</span><span class="sxs-lookup"><span data-stu-id="1fc37-173">**SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE**</span></span> | <span data-ttu-id="1fc37-174">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="1fc37-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="1fc37-175">**SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="1fc37-175">**SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**</span></span>                 | <span data-ttu-id="1fc37-176">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="1fc37-176">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="1fc37-177">**SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**</span><span class="sxs-lookup"><span data-stu-id="1fc37-177">**SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**</span></span>             | <span data-ttu-id="1fc37-178">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="1fc37-178">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="1fc37-179">**SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**</span><span class="sxs-lookup"><span data-stu-id="1fc37-179">**SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**</span></span>              | <span data-ttu-id="1fc37-180">Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="1fc37-180">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="1fc37-181">**SPLREG_RETRY_POPUP**</span><span class="sxs-lookup"><span data-stu-id="1fc37-181">**SPLREG_RETRY_POPUP**</span></span>                                            | <span data-ttu-id="1fc37-182">Bei erfolgreicher Rückgabe enthält *pData* 1, wenn der Server für die Wiederherstellung von Popup Fenstern für alle Aufträge festgelegt ist, oder 0, wenn der Server keine Popup Fenster für alle Aufträge erneut versucht.</span><span class="sxs-lookup"><span data-stu-id="1fc37-182">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="1fc37-183">Wird in Windows Server 2003 und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1fc37-183">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="1fc37-184">**SPLREG_SCHEDULER_THREAD_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="1fc37-184">**SPLREG_SCHEDULER_THREAD_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="1fc37-185">**SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="1fc37-185">**SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="1fc37-186">**SPLREG_WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="1fc37-186">**SPLREG_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="1fc37-187">Windows Server 2003 und höher</span><span class="sxs-lookup"><span data-stu-id="1fc37-187">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="1fc37-188">Wenn Sie einen der folgenden vordefinierten Werte als *pvaluename* übergeben, wird das Druck Verhalten des Pools festgelegt, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="1fc37-188">Passing one of the following predefined values as *pValueName* sets the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="1fc37-189">Wert</span><span class="sxs-lookup"><span data-stu-id="1fc37-189">Value</span></span>                                       | <span data-ttu-id="1fc37-190">Kommentare</span><span class="sxs-lookup"><span data-stu-id="1fc37-190">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc37-191">**SPLREG_RESTART_JOB_ON_POOL_ERROR**</span><span class="sxs-lookup"><span data-stu-id="1fc37-191">**SPLREG_RESTART_JOB_ON_POOL_ERROR**</span></span>   | <span data-ttu-id="1fc37-192">Der Wert von *pData* gibt die Zeit in Sekunden an, nach der ein Auftrag an einem anderen Port neu gestartet wird, nachdem ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="1fc37-192">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="1fc37-193">Diese Einstellung wird mit **SPLREG_RESTART_JOB_ON_POOL_ENABLED** verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fc37-193">This setting is used with **SPLREG_RESTART_JOB_ON_POOL_ENABLED**.</span></span><br/> |
| <span data-ttu-id="1fc37-194">**SPLREG_RESTART_JOB_ON_POOL_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="1fc37-194">**SPLREG_RESTART_JOB_ON_POOL_ENABLED**</span></span> | <span data-ttu-id="1fc37-195">Ein Wert ungleich 0 (null) in *pData* gibt an, dass **SPLREG_RESTART_JOB_ON_POOL_ERROR** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1fc37-195">A nonzero value in *pData* indicates that **SPLREG_RESTART_JOB_ON_POOL_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="1fc37-196">Die in **SPLREG_RESTART_JOB_ON_POOL_ERROR** angegebene Zeit ist eine minimale Zeit.</span><span class="sxs-lookup"><span data-stu-id="1fc37-196">The time specified in **SPLREG_RESTART_JOB_ON_POOL_ERROR** is a minimum time.</span></span> <span data-ttu-id="1fc37-197">Die tatsächliche Zeit kann je nach den folgenden Port Monitoreinstellungen, bei denen es sich um Registrierungs Werte unter diesem Registrierungsschlüssel handelt, länger sein:</span><span class="sxs-lookup"><span data-stu-id="1fc37-197">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="1fc37-198">**HKLM \\ System \\ CurrentControlSet \\ Control \\ Print \\ Monitors \\ < *Monitorname* > \\ Ports**</span><span class="sxs-lookup"><span data-stu-id="1fc37-198">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="1fc37-199">Um diese Werte festzulegen, können Sie die [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1fc37-199">Call the [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) function to set these values.</span></span>



| <span data-ttu-id="1fc37-200">Port Monitor Einstellung</span><span class="sxs-lookup"><span data-stu-id="1fc37-200">Port monitor setting</span></span>     | <span data-ttu-id="1fc37-201">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1fc37-201">Data type</span></span>      | <span data-ttu-id="1fc37-202">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1fc37-202">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc37-203">**Statusupdateaktivierte**</span><span class="sxs-lookup"><span data-stu-id="1fc37-203">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="1fc37-204">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="1fc37-204">**REG_DWORD**</span></span> | <span data-ttu-id="1fc37-205">Wenn ein Wert ungleich NULL ist, wird es dem Port Monitor ermöglicht, den Spooler mit dem Port Status zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1fc37-205">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="1fc37-206">**Statusupdateinterval**</span><span class="sxs-lookup"><span data-stu-id="1fc37-206">**StatusUpdateInterval**</span></span> | <span data-ttu-id="1fc37-207">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="1fc37-207">**REG_DWORD**</span></span> | <span data-ttu-id="1fc37-208">Gibt das Intervall (in Minuten) an, in dem der Port Monitor den Spooler mit dem Port Status aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1fc37-208">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="1fc37-209">Um sicherzustellen, dass der Spooler Aufträge an den nächsten verfügbaren Drucker im Pool umleitet (wenn der Druckauftrag nicht innerhalb der festgelegten Zeit gedruckt wird), muss der Port Monitor SNMP unterstützen, und die Netzwerkports im Pool müssen als "aktivierter SNMP-Status" konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="1fc37-209">To ensure that the spooler redirects jobs to the next available printer in the pool (when the print job is not printed within the set time), the port monitor must support SNMP and the network ports in the pool must be configured as "SNMP status enabled."</span></span> <span data-ttu-id="1fc37-210">Der Port Monitor, der SNMP unterstützt, ist der TCP/IP-Port Monitor (Standard).</span><span class="sxs-lookup"><span data-stu-id="1fc37-210">The port monitor that supports SNMP is Standard TCP/IP port monitor.</span></span>

<span data-ttu-id="1fc37-211">In Windows 7 und höheren Versionen von Windows werden Druckaufträge, die an einen Druckserver gesendet werden, standardmäßig auf dem Client gerendert.</span><span class="sxs-lookup"><span data-stu-id="1fc37-211">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="1fc37-212">Das Client seitige Rendering von Druckaufträgen kann konfiguriert werden, indem *pkeyname* auf "printerdriverdata" und *pvaluename* auf den Einstellungs Wert in der folgenden Tabelle festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1fc37-212">Client-side rendering of print jobs can be configured by setting *pKeyName* to "PrinterDriverData" and *pValueName* to the setting value in the following table.</span></span>



| <span data-ttu-id="1fc37-213">Einstellung</span><span class="sxs-lookup"><span data-stu-id="1fc37-213">Setting</span></span>                      | <span data-ttu-id="1fc37-214">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1fc37-214">Data type</span></span>      | <span data-ttu-id="1fc37-215">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1fc37-215">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc37-216">**EMF despoolingsetting**</span><span class="sxs-lookup"><span data-stu-id="1fc37-216">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="1fc37-217">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="1fc37-217">**REG_DWORD**</span></span> | <span data-ttu-id="1fc37-218">Der Wert 0 (null), oder wenn dieser Wert nicht in der Registrierung vorhanden ist, aktiviert das Client seitige Standard Rendering von Druckaufträgen.</span><span class="sxs-lookup"><span data-stu-id="1fc37-218">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="1fc37-219">Der Wert 1 deaktiviert das Client seitige Rendering von Druckaufträgen.</span><span class="sxs-lookup"><span data-stu-id="1fc37-219">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="1fc37-220">**Forceclientsiderderdering**</span><span class="sxs-lookup"><span data-stu-id="1fc37-220">**ForceClientSideRendering**</span></span> | <span data-ttu-id="1fc37-221">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="1fc37-221">**REG_DWORD**</span></span> | <span data-ttu-id="1fc37-222">Der Wert 0 oder, wenn dieser Wert nicht in der Registrierung vorhanden ist, bewirkt, dass die Druckaufträge auf dem Client gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="1fc37-222">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="1fc37-223">Wenn ein Druckauftrag nicht auf dem Client gerendert werden kann, wird er auf dem Server gerendert.</span><span class="sxs-lookup"><span data-stu-id="1fc37-223">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="1fc37-224">Wenn ein Druckauftrag nicht auf dem Server gerendert werden kann, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="1fc37-224">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="1fc37-225">Bei einem Wert von 1 werden Druckaufträge auf dem Client ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="1fc37-225">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="1fc37-226">Wenn ein Druckauftrag nicht auf dem Client gerendert werden kann, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="1fc37-226">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1fc37-227">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1fc37-227">Requirements</span></span>



| <span data-ttu-id="1fc37-228">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1fc37-228">Requirement</span></span> | <span data-ttu-id="1fc37-229">Wert</span><span class="sxs-lookup"><span data-stu-id="1fc37-229">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc37-230">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1fc37-230">Minimum supported client</span></span><br/> | <span data-ttu-id="1fc37-231">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1fc37-231">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1fc37-232">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1fc37-232">Minimum supported server</span></span><br/> | <span data-ttu-id="1fc37-233">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1fc37-233">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1fc37-234">Header</span><span class="sxs-lookup"><span data-stu-id="1fc37-234">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fc37-235"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fc37-235"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1fc37-236">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1fc37-236">Library</span></span><br/>                  | <dl> <span data-ttu-id="1fc37-237"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fc37-237"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="1fc37-238">DLL</span><span class="sxs-lookup"><span data-stu-id="1fc37-238">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fc37-239"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="1fc37-239"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="1fc37-240">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="1fc37-240">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1fc37-241">**Setprinterdataexw** (Unicode) und **setprinterdataexa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1fc37-241">**SetPrinterDataExW** (Unicode) and **SetPrinterDataExA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="1fc37-242">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fc37-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fc37-243">Drucken</span><span class="sxs-lookup"><span data-stu-id="1fc37-243">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1fc37-244">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="1fc37-244">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="1fc37-245">**Getprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="1fc37-245">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="1fc37-246">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="1fc37-246">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="1fc37-247">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="1fc37-247">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="1fc37-248">**PRINTER_INFO_7**</span><span class="sxs-lookup"><span data-stu-id="1fc37-248">**PRINTER_INFO_7**</span></span>](printer-info-7.md)
</dt> </dl>

 

