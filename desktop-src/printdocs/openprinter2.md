---
description: Ruft ein Handle für den angegebenen Drucker, Druckserver oder andere Typen von Handles im Druck Subsystem ab, während einige der Druckeroptionen festgelegt werden.
ms.assetid: e2370ae4-4475-4ccc-a6f9-3d33d1370054
title: OpenPrinter2-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter2
- OpenPrinter2A
- OpenPrinter2W
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 46788d7ad810ef623cd77793a72ab6c046b73590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865868"
---
# <a name="openprinter2-function"></a><span data-ttu-id="9f947-103">OpenPrinter2-Funktion</span><span class="sxs-lookup"><span data-stu-id="9f947-103">OpenPrinter2 function</span></span>

<span data-ttu-id="9f947-104">Ruft ein Handle für den angegebenen Drucker, Druckserver oder andere Typen von Handles im Druck Subsystem ab, während einige der Druckeroptionen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9f947-104">Retrieves a handle to the specified printer, print server, or other types of handles in the print subsystem, while setting some of the printer options.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f947-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f947-105">Syntax</span></span>


```C++
BOOL OpenPrinter2(
  _In_  LPCTSTR            pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault,
  _In_  PPRINTER_OPTIONS   pOptions
);
```



## <a name="parameters"></a><span data-ttu-id="9f947-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f947-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f947-107">*pprintername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f947-107">*pPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f947-108">Ein Zeiger auf eine Konstante mit NULL endender Zeichenfolge, die den Namen des Druckers oder Druck Servers, das Drucker Objekt, den xcvmonitor oder den xcvport angibt.</span><span class="sxs-lookup"><span data-stu-id="9f947-108">A pointer to a constant null-terminated string that specifies the name of the printer or print server, the printer object, the XcvMonitor, or the XcvPort.</span></span>

<span data-ttu-id="9f947-109">Verwenden Sie für ein Drucker Objekt: PrinterName, Job xxxx.</span><span class="sxs-lookup"><span data-stu-id="9f947-109">For a printer object, use: PrinterName,Job xxxx.</span></span> <span data-ttu-id="9f947-110">Verwenden Sie für einen xcvmonitor Folgendes: Servername, xcvmonitor Monitorname.</span><span class="sxs-lookup"><span data-stu-id="9f947-110">For an XcvMonitor, use: ServerName,XcvMonitor MonitorName.</span></span> <span data-ttu-id="9f947-111">Verwenden Sie für einen xcvport: Servername, xcvport PORTNAME.</span><span class="sxs-lookup"><span data-stu-id="9f947-111">For an XcvPort, use: ServerName,XcvPort PortName.</span></span>

<span data-ttu-id="9f947-112">**Windows Vista:** Wenn der Wert **null** ist, wird der lokale Drucker Server angegeben.</span><span class="sxs-lookup"><span data-stu-id="9f947-112">**Windows Vista:** If **NULL**, it indicates the local print server.</span></span>

</dd> <dt>

<span data-ttu-id="9f947-113">*phprinter* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9f947-113">*phPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f947-114">Ein Zeiger auf eine Variable, die ein Handle für den geöffneten Drucker oder das Druckserver Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="9f947-114">A pointer to a variable that receives a handle to the open printer or print server object.</span></span>

</dd> <dt>

<span data-ttu-id="9f947-115">*pdefault* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f947-115">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f947-116">Ein Zeiger auf eine [**Drucker \_ Standard**](printer-defaults.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="9f947-116">A pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="9f947-117">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="9f947-117">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9f947-118">*poptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f947-118">*pOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f947-119">Ein Zeiger auf eine [**Drucker \_ options**](printer-options.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="9f947-119">A pointer to a [**PRINTER\_OPTIONS**](printer-options.md) structure.</span></span> <span data-ttu-id="9f947-120">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="9f947-120">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f947-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f947-121">Return value</span></span>

<span data-ttu-id="9f947-122">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9f947-122">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="9f947-123">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="9f947-123">If the function fails, the return value is zero.</span></span> <span data-ttu-id="9f947-124">Für erweiterte Fehlerinformationen aufrufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="9f947-124">For extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="9f947-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f947-125">Remarks</span></span>

<span data-ttu-id="9f947-126">Diese Methode darf nicht in [**DllMain**](/windows/desktop/Dlls/dllmain)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9f947-126">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="9f947-127">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9f947-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9f947-128">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="9f947-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9f947-129">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="9f947-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="9f947-130">Die ANSI-Version dieser Funktion ist nicht implementiert und gibt einen Fehler zurück, der \_ nicht \_ unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="9f947-130">The ANSI version of this function is not implemented and returns ERROR\_NOT\_SUPPORTED.</span></span>

<span data-ttu-id="9f947-131">Mit dem *pdefault* -Parameter können Sie die Werte für Datentyp und Geräte Modus angeben, die zum Drucken von Dokumenten verwendet werden, die von der [**StartDocPrinter**](startdocprinter.md) -Funktion übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="9f947-131">The *pDefault* parameter enables you to specify the data type and device mode values that are used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="9f947-132">Sie können diese Werte jedoch überschreiben, indem Sie die Funktion [**setjob**](setjob.md) verwenden, nachdem ein Dokument gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="9f947-132">However, you can override these values by using the [**SetJob**](setjob.md) function after a document has been started.</span></span>

<span data-ttu-id="9f947-133">Sie können die **OpenPrinter2** -Funktion aufrufen, um ein Handle für einen Druckserver zu öffnen oder um die Client Zugriffsrechte für einen Druckserver zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="9f947-133">You can call the **OpenPrinter2** function to open a handle to a print server or to determine client access rights to a print server.</span></span> <span data-ttu-id="9f947-134">Geben Sie hierzu den Namen des Drucker Servers im *pprintername* -Parameter an, legen Sie die **pdatatype** -und **pdevmode** -Member der [**\_ Standard**](printer-defaults.md) Struktur der Drucker Standards auf **null** fest, und legen Sie für das **desiredAccess** -Element einen Server Zugriffs Maskenwert fest, wie z \_ . b. Zugriff auf den Server \_ .</span><span class="sxs-lookup"><span data-stu-id="9f947-134">To do this, specify the name of the print server in the *pPrinterName* parameter, set the **pDatatype** and **pDevMode** members of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to **NULL**, and set the **DesiredAccess** member to specify a server access mask value such as SERVER\_ALL\_ACCESS.</span></span> <span data-ttu-id="9f947-135">Wenn Sie mit dem Handle fertig sind, übergeben Sie es an die [**closeprinter**](closeprinter.md) -Funktion, um es zu schließen.</span><span class="sxs-lookup"><span data-stu-id="9f947-135">When you are finished with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="9f947-136">Verwenden Sie das **desiredAccess** -Mitglied [**der \_ Drucker Standard**](printer-defaults.md) Struktur, um die erforderlichen Zugriffsrechte anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9f947-136">Use the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to specify the necessary access rights.</span></span> <span data-ttu-id="9f947-137">Die Zugriffsrechte können eines der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="9f947-137">The access rights can be one of the following.</span></span>



| <span data-ttu-id="9f947-138">Gewünschter Zugriffs Wert</span><span class="sxs-lookup"><span data-stu-id="9f947-138">Desired Access value</span></span>                        | <span data-ttu-id="9f947-139">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9f947-139">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f947-140">Drucker \_ Zugriffs \_ Verwaltung</span><span class="sxs-lookup"><span data-stu-id="9f947-140">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="9f947-141">Zum Ausführen administrativer Aufgaben, wie z. b. die von [**SetPrinter**](setprinter.md)bereitgestellten.</span><span class="sxs-lookup"><span data-stu-id="9f947-141">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="9f947-142">Drucker \_ Zugriffs \_ Verwendung</span><span class="sxs-lookup"><span data-stu-id="9f947-142">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="9f947-143">Zum Ausführen grundlegender Druckvorgänge.</span><span class="sxs-lookup"><span data-stu-id="9f947-143">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="9f947-144">Drucker \_ \_ Zugriff</span><span class="sxs-lookup"><span data-stu-id="9f947-144">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="9f947-145">Zum Ausführen aller Verwaltungsaufgaben und grundlegenden Druckvorgänge außer synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="9f947-145">To perform all administrative tasks and basic printing operations except SYNCHRONIZE.</span></span> <span data-ttu-id="9f947-146">Siehe [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="9f947-146">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                         |
| <span data-ttu-id="9f947-147">Drucker \_ Zugriff \_ mit \_ eingeschränkter Verwaltung</span><span class="sxs-lookup"><span data-stu-id="9f947-147">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="9f947-148">Zum Ausführen administrativer Aufgaben, wie z. b. die von [**SetPrinter**](setprinter.md) und [**setprinterdata**](setprinterdata.md)bereitgestellten.</span><span class="sxs-lookup"><span data-stu-id="9f947-148">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="9f947-149">Dieser Wert ist ab Windows 8.1 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9f947-149">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="9f947-150">generische Sicherheitswerte, z. b. \_ DAC schreiben</span><span class="sxs-lookup"><span data-stu-id="9f947-150">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="9f947-151">, Um bestimmte Zugriffsrechte für das Steuerelement zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="9f947-151">To allow specific control access rights.</span></span> <span data-ttu-id="9f947-152">Siehe [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="9f947-152">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

<span data-ttu-id="9f947-153">Wenn ein Benutzer nicht über die Berechtigung zum Öffnen eines angegebenen Druckers oder Druck Servers mit dem gewünschten Zugriff verfügt, schlägt der **OpenPrinter2** -Befehl fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Wert für den Fehler \_ Zugriff \_ verweigert zurück.</span><span class="sxs-lookup"><span data-stu-id="9f947-153">If a user does not have permission to open a specified printer or print server with the desired access, the **OpenPrinter2** call will fail, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the value ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="9f947-154">Wenn " *pprintername* " ein lokaler Drucker ist, ignoriert **OpenPrinter2** alle Werte der **dwFlags** , auf die die Struktur der Druckeroptionen mithilfe von *poptions* zeigt, mit Ausnahme der Option "Client Änderung für Drucker [**\_ Optionen**](printer-options.md) " \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9f947-154">When *pPrinterName* is a local printer, then **OpenPrinter2** ignores all values of the **dwFlags** that the [**PRINTER\_OPTIONS**](printer-options.md) structure pointed to using *pOptions*, except PRINTER\_OPTION\_CLIENT\_CHANGE.</span></span> <span data-ttu-id="9f947-155">Wenn Letzteres erfolgreich ist, gibt **OpenPrinter2** die Fehlermeldung " \_ Zugriff \_ verweigert" zurück.</span><span class="sxs-lookup"><span data-stu-id="9f947-155">If the latter is passed, then **OpenPrinter2** will return ERROR\_ACCESS\_DENIED.</span></span> <span data-ttu-id="9f947-156">Dementsprechend bietet **OpenPrinter2** beim Öffnen eines lokalen Druckers keinen Vorteil gegenüber [**OpenPrinter**](openprinter.md).</span><span class="sxs-lookup"><span data-stu-id="9f947-156">Accordingly, when opening a local printer, **OpenPrinter2** provides no advantage over [**OpenPrinter**](openprinter.md).</span></span>

<span data-ttu-id="9f947-157">**Windows Vista:** Die von **OpenPrinter2** zurückgegebenen Druckerdaten werden aus einem lokalen Cache abgerufen, es sei denn, die **\_ Druckeroption \_ kein \_ Cache** -Flag wird im **dwFlags** -Feld der [**Drucker \_ options**](printer-options.md) Struktur festgelegt, auf die durch *poptions* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9f947-157">**Windows Vista:** The printer data returned by **OpenPrinter2** is retrieved from a local cache unless the **PRINTER\_OPTION\_NO\_CACHE** flag is set in the **dwFlags** field of the [**PRINTER\_OPTIONS**](printer-options.md) structure referenced by *pOptions*.</span></span>

## <a name="examples"></a><span data-ttu-id="9f947-158">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f947-158">Examples</span></span>

<span data-ttu-id="9f947-159">In diesem Beispiel schlägt **OpenPrinter2** fehl, wenn der Drucker \_ Zugriffs \_ Verwaltung \_ Limited an die [**Drucker \_ Standard**](printer-defaults.md) Struktur übermittelt wird und der Benutzer nicht über die entsprechende Berechtigung verfügt.</span><span class="sxs-lookup"><span data-stu-id="9f947-159">In this example, **OpenPrinter2** fails when PRINTER\_ACCESS\_MANAGE\_LIMITED is passed to the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure, and the user does not have the appropriate permission.</span></span>


```C++
// Specify the limited management permission.
PRINTER_DEFAULTS defaults = {};
defaults.DesiredAccess = PRINTER_ACCESS_MANAGE_LIMITED;

// Open a printer to which the user has no administrative rights.
HANDLE printer = nullptr;
assert(!OpenPrinter2(L QueueWithNoAdminRights , // Queue name
                     &printer,                  // Printer handle
                     &defaults,                 // Printer defaults
                     nullptr));                 // Printer options

assert(GetLastError() == ERROR_ACCESS_DENIED);

if (printer)
{
    ClosePrinter(printer);
}
```



<span data-ttu-id="9f947-160">Ein Beispielprogramm, das zeigt, wie diese Funktion verwendet wird, finden Sie unter Gewusst [wie: Drucken mit der GDI-Druck-API](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="9f947-160">For a sample program that shows how to use this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f947-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f947-161">Requirements</span></span>



| <span data-ttu-id="9f947-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f947-162">Requirement</span></span> | <span data-ttu-id="9f947-163">Wert</span><span class="sxs-lookup"><span data-stu-id="9f947-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f947-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f947-164">Minimum supported client</span></span><br/> | <span data-ttu-id="9f947-165">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f947-165">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9f947-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f947-166">Minimum supported server</span></span><br/> | <span data-ttu-id="9f947-167">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f947-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9f947-168">Header</span><span class="sxs-lookup"><span data-stu-id="9f947-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f947-169"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f947-169"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9f947-170">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9f947-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f947-171"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f947-171"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9f947-172">DLL</span><span class="sxs-lookup"><span data-stu-id="9f947-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f947-173"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f947-173"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="9f947-174">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="9f947-174">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9f947-175">**OpenPrinter2W** (Unicode) und **OpenPrinter2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9f947-175">**OpenPrinter2W** (Unicode) and **OpenPrinter2A** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="9f947-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f947-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f947-177">Drucken</span><span class="sxs-lookup"><span data-stu-id="9f947-177">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9f947-178">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9f947-178">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9f947-179">**Closeprinter**</span><span class="sxs-lookup"><span data-stu-id="9f947-179">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="9f947-180">**Drucker \_ Standardwerte**</span><span class="sxs-lookup"><span data-stu-id="9f947-180">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="9f947-181">**Drucker \_ Optionen**</span><span class="sxs-lookup"><span data-stu-id="9f947-181">**PRINTER\_OPTIONS**</span></span>](printer-options.md)
</dt> <dt>

[<span data-ttu-id="9f947-182">**Setjob**</span><span class="sxs-lookup"><span data-stu-id="9f947-182">**SetJob**</span></span>](setjob.md)
</dt> <dt>

[<span data-ttu-id="9f947-183">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="9f947-183">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="9f947-184">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="9f947-184">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="9f947-185">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="9f947-185">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

