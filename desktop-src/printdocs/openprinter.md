---
description: Die OpenPrinter-Funktion Ruft ein Handle für den angegebenen Drucker oder Druckserver oder andere Typen von Handles im Druck Subsystem ab.
ms.assetid: 96763220-d851-46f0-8be8-403f3356edb9
title: OpenPrinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter
- OpenPrinterA
- OpenPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 02cd6f6b5d56eec525bd00e2feef50f4d5f07734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349450"
---
# <a name="openprinter-function"></a><span data-ttu-id="e8783-103">OpenPrinter-Funktion</span><span class="sxs-lookup"><span data-stu-id="e8783-103">OpenPrinter function</span></span>

<span data-ttu-id="e8783-104">Die **OpenPrinter** -Funktion Ruft ein Handle für den angegebenen Drucker oder Druckserver oder andere Typen von Handles im Druck Subsystem ab.</span><span class="sxs-lookup"><span data-stu-id="e8783-104">The **OpenPrinter** function retrieves a handle to the specified printer or print server or other types of handles in the print subsystem.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8783-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8783-105">Syntax</span></span>


```C++
BOOL OpenPrinter(
  _In_  LPTSTR             pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a><span data-ttu-id="e8783-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8783-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8783-107">*pprintername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8783-107">*pPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8783-108">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckers oder Druck Servers, das Drucker Objekt, den xcvmonitor oder den xcvport angibt.</span><span class="sxs-lookup"><span data-stu-id="e8783-108">A pointer to a null-terminated string that specifies the name of the printer or print server, the printer object, the XcvMonitor, or the XcvPort.</span></span>

<span data-ttu-id="e8783-109">Verwenden Sie für ein Drucker Objekt: PrinterName, Job xxxx.</span><span class="sxs-lookup"><span data-stu-id="e8783-109">For a printer object use: PrinterName, Job xxxx.</span></span> <span data-ttu-id="e8783-110">Verwenden Sie für einen xcvmonitor Folgendes: Servername, xcvmonitor Monitorname.</span><span class="sxs-lookup"><span data-stu-id="e8783-110">For an XcvMonitor, use: ServerName, XcvMonitor MonitorName.</span></span> <span data-ttu-id="e8783-111">Verwenden Sie für einen xcvport: Servername, xcvport PORTNAME.</span><span class="sxs-lookup"><span data-stu-id="e8783-111">For an XcvPort, use: ServerName, XcvPort PortName.</span></span>

<span data-ttu-id="e8783-112">Wenn der Wert **null** ist, wird der lokale Drucker Server angegeben.</span><span class="sxs-lookup"><span data-stu-id="e8783-112">If **NULL**, it indicates the local printer server.</span></span>

</dd> <dt>

<span data-ttu-id="e8783-113">*phprinter* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e8783-113">*phPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8783-114">Ein Zeiger auf eine Variable, die ein Handle (nicht Thread sicher) für den geöffneten Drucker oder das Druckserver Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="e8783-114">A pointer to a variable that receives a handle (not thread safe) to the open printer or print server object.</span></span>

<span data-ttu-id="e8783-115">Der Parameter " *phprinter* " kann ein XCV-Handle für die Verwendung mit der XcvData-Funktion zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e8783-115">The *phPrinter* parameter can return an Xcv handle for use with the XcvData function.</span></span> <span data-ttu-id="e8783-116">Weitere Informationen zu XcvData finden Sie unter DDK.</span><span class="sxs-lookup"><span data-stu-id="e8783-116">For more information about XcvData, see the DDK.</span></span>

</dd> <dt>

<span data-ttu-id="e8783-117">*pdefault* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8783-117">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8783-118">Ein Zeiger auf eine [**Drucker \_ Standard**](printer-defaults.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="e8783-118">A pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="e8783-119">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e8783-119">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8783-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8783-120">Return value</span></span>

<span data-ttu-id="e8783-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e8783-121">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e8783-122">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="e8783-122">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8783-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8783-123">Remarks</span></span>

<span data-ttu-id="e8783-124">Diese Methode darf nicht in [**DllMain**](/windows/desktop/Dlls/dllmain)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e8783-124">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="e8783-125">Ein Handle, das für einen Remote Drucker durch einen **OpenPrinter** -aufrufbefehl für einen Remote Drucker abgerufen wird, greift über einen lokalen Cache im Druckspoolerdienst auf den Drucker zu.</span><span class="sxs-lookup"><span data-stu-id="e8783-125">A handle obtained for a remote printer by a call to **OpenPrinter** for a remote printer accesses the printer through a local cache in the print spooler service.</span></span> <span data-ttu-id="e8783-126">Dieser Cache ist nicht echt Zeit genau.</span><span class="sxs-lookup"><span data-stu-id="e8783-126">This cache isn't real-time accurate.</span></span> <span data-ttu-id="e8783-127">Um genaue Daten zu erhalten, ersetzen Sie den OpenPrinter-Befehl durch [**OpenPrinter2**](openprinter2.md) durch poptions. dwFlags, die auf Drucker \_ Option \_ kein Cache festgelegt sind \_ .</span><span class="sxs-lookup"><span data-stu-id="e8783-127">To obtain accurate data, replace the OpenPrinter call with [**OpenPrinter2**](openprinter2.md) with pOptions.dwFlags set to PRINTER\_OPTION\_NO\_CACHE.</span></span> <span data-ttu-id="e8783-128">Beachten Sie, dass nur OpenPrinter2W funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="e8783-128">Note that only OpenPrinter2W is functional.</span></span> <span data-ttu-id="e8783-129">Die-Funktion gibt ein Drucker Handle zurück, das andere Druck-API-Aufrufe verwendet und den lokalen Cache umgeht.</span><span class="sxs-lookup"><span data-stu-id="e8783-129">The function returns a printer handle that uses other Printing API calls and bypasses the local cache.</span></span> <span data-ttu-id="e8783-130">Diese Methode blockiert, während auf die Netzwerkkommunikation mit dem Remote Drucker gewartet wird, sodass Sie möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e8783-130">This method blocks while waiting for network communication with the remote printer, so it might not return immediately.</span></span> <span data-ttu-id="e8783-131">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="e8783-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e8783-132">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, wird die Anwendung möglicherweise nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="e8783-132">Calling this function from a thread that manages user interface interaction might make the application appear unresponsive.</span></span>

 

> [!Note]  
> <span data-ttu-id="e8783-133">Ein Handle, das durch einen **OpenPrinter** -Aufrufvorgang für einen Remote Drucker abgerufen wird, greift über einen lokalen Cache im Druckspoolerdienst auf den Drucker zu.</span><span class="sxs-lookup"><span data-stu-id="e8783-133">A handle obtained by a call to **OpenPrinter** for a remote printer will access the printer through a local cache in the print spooler service.</span></span> <span data-ttu-id="e8783-134">Bei diesem Cache handelt es sich nicht um echtzeitgenauigkeit.</span><span class="sxs-lookup"><span data-stu-id="e8783-134">This cache is, by design, not real time accurate.</span></span> <span data-ttu-id="e8783-135">Wenn Sie genaue Daten abrufen müssen, ersetzen Sie den **OpenPrinter** -Befehl durch [**OpenPrinter2**](openprinter2.md) durch " *poptions. dwFlags* ", der auf " [**Printer \_ Option \_ No \_ Cache**](printer-options.md)" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e8783-135">If you need to obtain accurate data, replace the **OpenPrinter** call with [**OpenPrinter2**](openprinter2.md) with *pOptions.dwFlags* set to [**PRINTER\_OPTION\_NO\_CACHE**](printer-options.md).</span></span> <span data-ttu-id="e8783-136">Beachten Sie, dass nur **OpenPrinter2W** funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="e8783-136">Note that only **OpenPrinter2W** is functional.</span></span> <span data-ttu-id="e8783-137">Dadurch gibt die Funktion ein Drucker Handle zurück, das andere Druck-API-Aufrufe ausführt, um den lokalen Cache zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="e8783-137">Doing so the function returns a printer handle that makes other Printing API calls to bypass the local cache.</span></span> <span data-ttu-id="e8783-138">Beachten Sie, dass diese Vorgehensweise beim Warten auf die Roundtrip-Netzwerkkommunikation mit dem Remote Drucker blockiert wird, sodass Sie möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e8783-138">Note that this approach will block while waiting for the round-trip network communication to the remote printer, so it may not return immediately.</span></span> <span data-ttu-id="e8783-139">Wie schnell diese Funktion zurückgibt, hängt von den Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Druckertreiber Implementierung: Faktoren, die beim Schreiben einer Anwendung schwer vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="e8783-139">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation - factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e8783-140">Wenn Sie diese Funktion aus einem Thread aufrufen, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte es vorkommen, dass die Anwendung nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="e8783-140">Therefore calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e8783-141">Das Handle, auf das von *phprinter* verwiesen wird, ist nicht Thread sicher.</span><span class="sxs-lookup"><span data-stu-id="e8783-141">The handle pointed to by *phPrinter* is not thread safe.</span></span> <span data-ttu-id="e8783-142">Wenn Aufrufer Sie gleichzeitig für mehrere Threads verwenden müssen, müssen Sie den benutzerdefinierten Synchronisierungs Zugriff auf das Drucker Handle mithilfe der [Synchronisierungs Funktionen](/windows/desktop/Sync/synchronization-functions)bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e8783-142">If callers need to use it concurrently on multiple threads, they must provide custom synchronization access to the printer handle using the [Synchronization Functions](/windows/desktop/Sync/synchronization-functions).</span></span> <span data-ttu-id="e8783-143">Um das Schreiben von benutzerdefiniertem Code zu vermeiden, kann die Anwendung bei Bedarf ein Drucker Handle für jeden Thread öffnen.</span><span class="sxs-lookup"><span data-stu-id="e8783-143">To avoid writing custom code the application can open a printer handle on each thread, as needed.</span></span>

<span data-ttu-id="e8783-144">Mit dem *pdefault* -Parameter können Sie die Werte für Datentyp und Geräte Modus angeben, die zum Drucken von Dokumenten verwendet werden, die von der [**StartDocPrinter**](startdocprinter.md) -Funktion übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="e8783-144">The *pDefault* parameter enables you to specify the data type and device mode values that are used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="e8783-145">Sie können diese Werte jedoch überschreiben, indem Sie die Funktion [**setjob**](setjob.md) verwenden, nachdem ein Dokument gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="e8783-145">However, you can override these values by using the [**SetJob**](setjob.md) function after a document has been started.</span></span>

<span data-ttu-id="e8783-146">Die [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Einstellungen, die in der [**Drucker \_ Standard**](printer-defaults.md) Struktur des *pdefault* -Parameters definiert sind, werden nicht verwendet, wenn der Wert des *pdatatype* -Members der [**doc \_ Info \_ 1**](doc-info-1.md) -Struktur, die im *pdocinfo* -Parameter des [**StartDocPrinter**](startdocprinter.md) -Aufrufes übergeben wurde, "RAW" lautet.</span><span class="sxs-lookup"><span data-stu-id="e8783-146">The [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) settings defined in the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure of the *pDefault* parameter are not used when the value of the *pDatatype* member of the [**DOC\_INFO\_1**](doc-info-1.md) structure that was passed in the *pDocInfo* parameter of the [**StartDocPrinter**](startdocprinter.md) call is "RAW".</span></span> <span data-ttu-id="e8783-147">Wenn ein Dokument auf hoher Ebene (z. b. eine Adobe PDF-oder Microsoft Word-Datei) oder andere Druckerdaten (z. b. PCL, PS oder HPGL) direkt an einen Drucker gesendet werden, bei dem *pdatatype* auf "RAW" festgelegt ist, muss das Dokument die Einstellungen des Druckauftrags im **DEVMODE**-Stil in der Sprache beschreiben, die von</span><span class="sxs-lookup"><span data-stu-id="e8783-147">When a high-level document (such as an Adobe PDF or Microsoft Word file) or other printer data (such PCL, PS, or HPGL) is sent directly to a printer with *pDatatype* set to "RAW", the document must fully describe the **DEVMODE**-style print job settings in the language understood by the hardware.</span></span>

<span data-ttu-id="e8783-148">Sie können die **OpenPrinter** -Funktion aufrufen, um ein Handle für einen Drucker Server zu öffnen oder um die Zugriffsrechte zu ermitteln, die ein Client auf einen Druckserver hat.</span><span class="sxs-lookup"><span data-stu-id="e8783-148">You can call the **OpenPrinter** function to open a handle to a print server or to determine the access rights that a client has to a print server.</span></span> <span data-ttu-id="e8783-149">Geben Sie hierzu den Namen des Drucker Servers im *pprintername* -Parameter an, legen Sie die **pdatatype** -und **pdevmode** -Member der [**\_ Standard**](printer-defaults.md) Struktur der Drucker Standards auf **null** fest, und legen Sie das **desiredAccess** -Element auf einen Server Zugriffs Maskenwert fest, wie z \_ . b. Zugriff auf den Server \_ .</span><span class="sxs-lookup"><span data-stu-id="e8783-149">To do so, specify the name of the print server in the *pPrinterName* parameter, set the **pDatatype** and **pDevMode** members of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to **NULL**, and set the **DesiredAccess** member to specify a server access mask value such as SERVER\_ALL\_ACCESS.</span></span> <span data-ttu-id="e8783-150">Wenn Sie mit dem Handle fertig sind, übergeben Sie es an die [**closeprinter**](closeprinter.md) -Funktion, um es zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e8783-150">When you finish with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="e8783-151">Verwenden Sie das **desiredAccess** -Mitglied [**der \_ Drucker Standard**](printer-defaults.md) Struktur, um die Zugriffsrechte anzugeben, die Sie für den Drucker benötigen.</span><span class="sxs-lookup"><span data-stu-id="e8783-151">Use the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to specify the access rights that you need to the printer.</span></span> <span data-ttu-id="e8783-152">Die Zugriffsrechte können eines der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="e8783-152">The access rights can be one of the following.</span></span> <span data-ttu-id="e8783-153">(Wenn *pdefault* den Wert **null** hat, sind die Zugriffsrechte Drucker \_ . Zugriffs \_ Verwendung.)</span><span class="sxs-lookup"><span data-stu-id="e8783-153">(If *pDefault* is **NULL**, then the access rights are PRINTER\_ACCESS\_USE.)</span></span>



| <span data-ttu-id="e8783-154">Gewünschter Zugriffs Wert</span><span class="sxs-lookup"><span data-stu-id="e8783-154">Desired Access value</span></span>                        | <span data-ttu-id="e8783-155">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e8783-155">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8783-156">Drucker \_ Zugriffs \_ Verwaltung</span><span class="sxs-lookup"><span data-stu-id="e8783-156">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="e8783-157">Zum Ausführen administrativer Aufgaben, wie z. b. die von [**SetPrinter**](setprinter.md)bereitgestellten.</span><span class="sxs-lookup"><span data-stu-id="e8783-157">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="e8783-158">Drucker \_ Zugriffs \_ Verwendung</span><span class="sxs-lookup"><span data-stu-id="e8783-158">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="e8783-159">Zum Ausführen grundlegender Druckvorgänge.</span><span class="sxs-lookup"><span data-stu-id="e8783-159">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="e8783-160">Drucker \_ \_ Zugriff</span><span class="sxs-lookup"><span data-stu-id="e8783-160">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="e8783-161">Zum Ausführen aller Verwaltungsaufgaben und grundlegenden Druckvorgänge mit Ausnahme von Synchronisierung (siehe [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights)).</span><span class="sxs-lookup"><span data-stu-id="e8783-161">To perform all administrative tasks and basic printing operations except for SYNCHRONIZE (see [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                     |
| <span data-ttu-id="e8783-162">Drucker \_ Zugriff \_ mit \_ eingeschränkter Verwaltung</span><span class="sxs-lookup"><span data-stu-id="e8783-162">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="e8783-163">Zum Ausführen administrativer Aufgaben, wie z. b. die von [**SetPrinter**](setprinter.md) und [**setprinterdata**](setprinterdata.md)bereitgestellten.</span><span class="sxs-lookup"><span data-stu-id="e8783-163">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="e8783-164">Dieser Wert ist ab Windows 8.1 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e8783-164">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="e8783-165">generische Sicherheitswerte, z. b. \_ DAC schreiben</span><span class="sxs-lookup"><span data-stu-id="e8783-165">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="e8783-166">, Um bestimmte Zugriffsrechte für das Steuerelement zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="e8783-166">To allow specific control access rights.</span></span> <span data-ttu-id="e8783-167">Siehe [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="e8783-167">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

<span data-ttu-id="e8783-168">Wenn ein Benutzer nicht berechtigt ist, einen angegebenen Drucker oder Druckserver mit dem gewünschten Zugriff zu öffnen, schlägt der **OpenPrinter** -Rückruf mit dem Rückgabewert NULL fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Wert für den Fehler \_ Zugriff verweigert zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="e8783-168">If a user does not have permission to open a specified printer or print server with the desired access, the **OpenPrinter** call will fail with a return value of zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the value ERROR\_ACCESS\_DENIED.</span></span>

## <a name="examples"></a><span data-ttu-id="e8783-169">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8783-169">Examples</span></span>

<span data-ttu-id="e8783-170">Ein Beispielprogramm, das diese Funktion verwendet, finden [Sie unter Gewusst wie: Drucken mit der GDI-Druck-API](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="e8783-170">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8783-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8783-171">Requirements</span></span>



| <span data-ttu-id="e8783-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8783-172">Requirement</span></span> | <span data-ttu-id="e8783-173">Wert</span><span class="sxs-lookup"><span data-stu-id="e8783-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8783-174">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8783-174">Minimum supported client</span></span><br/> | <span data-ttu-id="e8783-175">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8783-175">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e8783-176">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8783-176">Minimum supported server</span></span><br/> | <span data-ttu-id="e8783-177">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8783-177">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e8783-178">Header</span><span class="sxs-lookup"><span data-stu-id="e8783-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8783-179"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8783-179"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e8783-180">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e8783-180">Library</span></span><br/>                  | <dl> <span data-ttu-id="e8783-181"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8783-181"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e8783-182">DLL</span><span class="sxs-lookup"><span data-stu-id="e8783-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8783-183"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="e8783-183"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e8783-184">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="e8783-184">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e8783-185">**Openprinterw** (Unicode) und **openprintera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e8783-185">**OpenPrinterW** (Unicode) and **OpenPrinterA** (ANSI)</span></span><br/>                                         |



## <a name="see-also"></a><span data-ttu-id="e8783-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8783-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8783-187">Drucken</span><span class="sxs-lookup"><span data-stu-id="e8783-187">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e8783-188">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e8783-188">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e8783-189">**"Write Printer"**</span><span class="sxs-lookup"><span data-stu-id="e8783-189">**WritePrinter**</span></span>](writeprinter.md)
</dt> <dt>

[<span data-ttu-id="e8783-190">**Closeprinter**</span><span class="sxs-lookup"><span data-stu-id="e8783-190">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="e8783-191">**Drucker \_ Standardwerte**</span><span class="sxs-lookup"><span data-stu-id="e8783-191">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="e8783-192">**Setjob**</span><span class="sxs-lookup"><span data-stu-id="e8783-192">**SetJob**</span></span>](setjob.md)
</dt> <dt>

[<span data-ttu-id="e8783-193">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="e8783-193">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="e8783-194">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="e8783-194">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

