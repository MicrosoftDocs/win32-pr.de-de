---
description: Die addprinter-Funktion fügt der Liste der unterstützten Drucker für einen angegebenen Server einen Drucker hinzu.
ms.assetid: ffc4fee8-46c6-47ad-803d-623bf8efdefd
title: Addprinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinter
- AddPrinterA
- AddPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 51416ed59bc1c6df1d2c69de87d61bdecab522f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215866"
---
# <a name="addprinter-function"></a><span data-ttu-id="bd71d-103">Addprinter-Funktion</span><span class="sxs-lookup"><span data-stu-id="bd71d-103">AddPrinter function</span></span>

<span data-ttu-id="bd71d-104">Die **addprinter** -Funktion fügt der Liste der unterstützten Drucker für einen angegebenen Server einen Drucker hinzu.</span><span class="sxs-lookup"><span data-stu-id="bd71d-104">The **AddPrinter** function adds a printer to the list of supported printers for a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd71d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd71d-105">Syntax</span></span>


```C++
HANDLE AddPrinter(
  _In_ LPTSTR *pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="bd71d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd71d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd71d-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd71d-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd71d-108">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, auf dem der Drucker installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd71d-108">A pointer to a null-terminated string that specifies the name of the server on which the printer should be installed.</span></span> <span data-ttu-id="bd71d-109">Wenn diese Zeichenfolge **null** ist, wird der Drucker lokal installiert.</span><span class="sxs-lookup"><span data-stu-id="bd71d-109">If this string is **NULL**, the printer is installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="bd71d-110">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd71d-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd71d-111">Die Version der-Struktur, auf die *pprinter* zeigt.</span><span class="sxs-lookup"><span data-stu-id="bd71d-111">The version of the structure to which *pPrinter* points.</span></span> <span data-ttu-id="bd71d-112">Dieser Wert muss 2 sein.</span><span class="sxs-lookup"><span data-stu-id="bd71d-112">This value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="bd71d-113">*pprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd71d-113">*pPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd71d-114">Ein Zeiger auf eine [**\_ Druckerinfo- \_ 2**](printer-info-2.md) -Struktur, die Informationen über den Drucker enthält.</span><span class="sxs-lookup"><span data-stu-id="bd71d-114">A pointer to a [**PRINTER\_INFO\_2**](printer-info-2.md) structure that contains information about the printer.</span></span> <span data-ttu-id="bd71d-115">Sie müssen Werte ungleich **null** für die Member **pprintername**, **pportname**, **pdrivername** und **pprintprocessor** dieser Struktur angeben, bevor Sie **addprinter** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bd71d-115">You must specify non-**NULL** values for the **pPrinterName**, **pPortName**, **pDriverName**, and **pPrintProcessor** members of this structure before calling **AddPrinter**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd71d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd71d-116">Return value</span></span>

<span data-ttu-id="bd71d-117">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Handle (nicht Thread sicher) für ein neues Drucker Objekt.</span><span class="sxs-lookup"><span data-stu-id="bd71d-117">If the function succeeds, the return value is a handle (not thread safe) to a new printer object.</span></span> <span data-ttu-id="bd71d-118">Wenn Sie mit dem Handle fertig sind, übergeben Sie es an die [**closeprinter**](closeprinter.md) -Funktion, um es zu schließen.</span><span class="sxs-lookup"><span data-stu-id="bd71d-118">When you are finished with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="bd71d-119">Wenn die Funktion fehlschlägt, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="bd71d-119">If the function fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd71d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd71d-120">Remarks</span></span>

<span data-ttu-id="bd71d-121">Diese Methode darf nicht in [**DllMain**](/windows/desktop/Dlls/dllmain)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bd71d-121">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="bd71d-122">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bd71d-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="bd71d-123">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="bd71d-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="bd71d-124">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="bd71d-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="bd71d-125">Der [Aufrufer muss über die SeLoadDriverPrivilege-Berechtigung](/windows/desktop/SecAuthZ/authorization-constants)verfügen.</span><span class="sxs-lookup"><span data-stu-id="bd71d-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="bd71d-126">Das zurückgegebene Handle ist nicht Thread sicher.</span><span class="sxs-lookup"><span data-stu-id="bd71d-126">The returned handle is not thread safe.</span></span> <span data-ttu-id="bd71d-127">Wenn Aufrufer Sie gleichzeitig für mehrere Threads verwenden müssen, müssen Sie den benutzerdefinierten Synchronisierungs Zugriff auf das Drucker Handle mithilfe der [Synchronisierungs Funktionen](/windows/desktop/Sync/synchronization-functions)bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="bd71d-127">If callers need to use it concurrently on multiple threads, they must provide custom synchronization access to the printer handle using the [Synchronization Functions](/windows/desktop/Sync/synchronization-functions).</span></span> <span data-ttu-id="bd71d-128">Um das Schreiben von benutzerdefiniertem Code zu vermeiden, kann die Anwendung bei Bedarf ein Drucker Handle für jeden Thread öffnen.</span><span class="sxs-lookup"><span data-stu-id="bd71d-128">To avoid writing custom code the application can open a printer handle on each thread, as needed.</span></span>

<span data-ttu-id="bd71d-129">Im folgenden sind die Elemente der [**\_ Druckerinfo- \_ 2**](printer-info-2.md) -Struktur aufgeführt, die vor dem Aufrufen der **addprinter** -Funktion festgelegt werden können:</span><span class="sxs-lookup"><span data-stu-id="bd71d-129">The following are the members of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure that can be set before the **AddPrinter** function is called:</span></span>

-   <span data-ttu-id="bd71d-130">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="bd71d-130">**Attributes**</span></span>
-   <span data-ttu-id="bd71d-131">**pprintprocessor**</span><span class="sxs-lookup"><span data-stu-id="bd71d-131">**pPrintProcessor**</span></span>
-   <span data-ttu-id="bd71d-132">**DefaultPriority**</span><span class="sxs-lookup"><span data-stu-id="bd71d-132">**DefaultPriority**</span></span>
-   <span data-ttu-id="bd71d-133">**Priority**</span><span class="sxs-lookup"><span data-stu-id="bd71d-133">**Priority**</span></span>
-   <span data-ttu-id="bd71d-134">**pcomment**</span><span class="sxs-lookup"><span data-stu-id="bd71d-134">**pComment**</span></span>
-   <span data-ttu-id="bd71d-135">**psecuritydescriptor**</span><span class="sxs-lookup"><span data-stu-id="bd71d-135">**pSecurityDescriptor**</span></span>
-   <span data-ttu-id="bd71d-136">**pdatatype**</span><span class="sxs-lookup"><span data-stu-id="bd71d-136">**pDatatype**</span></span>
-   <span data-ttu-id="bd71d-137">**psepfile**</span><span class="sxs-lookup"><span data-stu-id="bd71d-137">**pSepFile**</span></span>
-   <span data-ttu-id="bd71d-138">**pdevmode**</span><span class="sxs-lookup"><span data-stu-id="bd71d-138">**pDevMode**</span></span>
-   <span data-ttu-id="bd71d-139">**psharename**</span><span class="sxs-lookup"><span data-stu-id="bd71d-139">**pShareName**</span></span>
-   <span data-ttu-id="bd71d-140">**pLocation**</span><span class="sxs-lookup"><span data-stu-id="bd71d-140">**pLocation**</span></span>
-   <span data-ttu-id="bd71d-141">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="bd71d-141">**StartTime**</span></span>
-   <span data-ttu-id="bd71d-142">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="bd71d-142">**pParameters**</span></span>
-   <span data-ttu-id="bd71d-143">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="bd71d-143">**UntilTime**</span></span>

<span data-ttu-id="bd71d-144">Die Member " **Status**", " **cjobs**" und " **AveragePPM** " der Struktur " [**Printer \_ Info \_ 2**](printer-info-2.md) " sind für die Verwendung durch die Funktion " [**GetPrinter**](getprinter.md) " reserviert.</span><span class="sxs-lookup"><span data-stu-id="bd71d-144">The **Status**, **cJobs**, and **AveragePPM** members of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure are reserved for use by the [**GetPrinter**](getprinter.md) function.</span></span> <span data-ttu-id="bd71d-145">Sie dürfen nicht vor dem Aufrufen von **addprinter** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bd71d-145">They must not be set before calling **AddPrinter**.</span></span>

<span data-ttu-id="bd71d-146">Wenn **psecuritydescriptor** den Wert **null** hat, weist das System dem Drucker eine Standard Sicherheits Beschreibung zu.</span><span class="sxs-lookup"><span data-stu-id="bd71d-146">If **pSecurityDescriptor** is **NULL**, the system assigns a default security descriptor to the printer.</span></span> <span data-ttu-id="bd71d-147">Die Standard Sicherheits Beschreibung verfügt über die folgenden Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="bd71d-147">The default security descriptor has the following permissions.</span></span>



| <span data-ttu-id="bd71d-148">Wert</span><span class="sxs-lookup"><span data-stu-id="bd71d-148">Value</span></span>                          | <span data-ttu-id="bd71d-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd71d-149">Description</span></span>                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd71d-150">Administratoren und Hauptbenutzer</span><span class="sxs-lookup"><span data-stu-id="bd71d-150">Administrators and Power Users</span></span> | <span data-ttu-id="bd71d-151">Vollständige Steuerung der Druck Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="bd71d-151">Full control on the print queue.</span></span> <span data-ttu-id="bd71d-152">Dies bedeutet, dass Mitglieder dieser Gruppen die Warteschlange drucken, verwalten können (kann die Warteschlange löschen, beliebige Einstellungen der Warteschlange ändern, einschließlich der Sicherheits Beschreibung) und die Druckaufträge aller Benutzer verwalten (löschen, anhalten, fortsetzen, Aufträge neu starten). Beachten Sie, dass Hauptbenutzer nicht vor Windows XP Professional vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="bd71d-152">This means members of these groups can print, manage the queue (can delete the queue, change any setting of the queue, including the security descriptor), and manage the print jobs of all users (delete, pause, resume, restart jobs).Note that Power Users do not exist before Windows XP Professional.</span></span><br/> |
| <span data-ttu-id="bd71d-153">Ersteller/Besitzer</span><span class="sxs-lookup"><span data-stu-id="bd71d-153">Creator/Owner</span></span>                  | <span data-ttu-id="bd71d-154">Kann eigene Aufträge verwalten.</span><span class="sxs-lookup"><span data-stu-id="bd71d-154">Can manage own jobs.</span></span> <span data-ttu-id="bd71d-155">Dies bedeutet, dass Benutzer, die Aufträge übermitteln, ihre eigenen Aufträge verwalten (löschen, anhalten, fortsetzen, neu starten) können.</span><span class="sxs-lookup"><span data-stu-id="bd71d-155">This means that user who submit jobs can manage (delete, pause, resume, restart) their own jobs.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="bd71d-156">Jeder</span><span class="sxs-lookup"><span data-stu-id="bd71d-156">Everyone</span></span>                       | <span data-ttu-id="bd71d-157">Execute-und Standard-Lese Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="bd71d-157">Execute and standard read control.</span></span> <span data-ttu-id="bd71d-158">Dies bedeutet, dass Mitglieder der Gruppe "jeder" die Eigenschaften der Druck Warteschlange drucken und lesen können.</span><span class="sxs-lookup"><span data-stu-id="bd71d-158">This means that members of the everyone group can print and read properties of the print queue.</span></span>                                                                                                                                                                                                                     |



 

<span data-ttu-id="bd71d-159">Nachdem eine Anwendung ein Drucker Objekt mit der **addprinter** -Funktion erstellt hat, muss Sie die [**printerproperties**](printerproperties.md) -Funktion verwenden, um die korrekten Einstellungen für den Druckertreiber anzugeben, der dem Drucker Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bd71d-159">After an application creates a printer object with the **AddPrinter** function, it must use the [**PrinterProperties**](printerproperties.md) function to specify the correct settings for the printer driver associated with the printer object.</span></span>

<span data-ttu-id="bd71d-160">Die **addprinter** -Funktion gibt einen Fehler zurück, wenn bereits ein Drucker Objekt mit demselben Namen vorhanden ist, es sei denn, das Objekt ist als ausstehende Löschung markiert.</span><span class="sxs-lookup"><span data-stu-id="bd71d-160">The **AddPrinter** function returns an error if a printer object with the same name already exists, unless that object is marked as pending deletion.</span></span> <span data-ttu-id="bd71d-161">In diesem Fall wird der vorhandene Drucker nicht gelöscht, und die **addprinter** -Erstellungs Parameter werden verwendet, um die vorhandenen Druckereinstellungen zu ändern (als ob die Anwendung die [**SetPrinter**](setprinter.md) -Funktion verwendet hätte).</span><span class="sxs-lookup"><span data-stu-id="bd71d-161">In that case, the existing printer is not deleted, and the **AddPrinter** creation parameters are used to change the existing printer settings (as if the application had used the [**SetPrinter**](setprinter.md) function).</span></span>

<span data-ttu-id="bd71d-162">Verwenden Sie die [**enumprintprocessor**](enumprintprocessors.md) -Funktion, um den Satz von Druck Prozessoren aufzulisten, die auf einem Server installiert sind.</span><span class="sxs-lookup"><span data-stu-id="bd71d-162">Use the [**EnumPrintProcessors**](enumprintprocessors.md) function to enumerate the set of print processors installed on a server.</span></span> <span data-ttu-id="bd71d-163">Verwenden Sie die [**enumprintprocessordatatypes**](enumprintprocessordatatypes.md) -Funktion, um den Satz von Datentypen aufzulisten, den ein Druck Prozessor unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd71d-163">Use the [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) function to enumerate the set of data types that a print processor supports.</span></span> <span data-ttu-id="bd71d-164">Verwenden Sie die [**enumports**](enumports.md) -Funktion, um den Satz verfügbarer Ports aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="bd71d-164">Use the [**EnumPorts**](enumports.md) function to enumerate the set of available ports.</span></span> <span data-ttu-id="bd71d-165">Verwenden Sie die [**enumprinterdrivers**](enumprinterdrivers.md) -Funktion, um die installierten Druckertreiber aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="bd71d-165">Use the [**EnumPrinterDrivers**](enumprinterdrivers.md) function to enumerate the installed printer drivers.</span></span>

<span data-ttu-id="bd71d-166">Der Aufrufer der **addprinter** -Funktion muss über Server \_ Zugriffsberechtigungen \_ für den Server verfügen, auf dem der Drucker erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd71d-166">The caller of the **AddPrinter** function must have SERVER\_ACCESS\_ADMINISTER access to the server on which the printer is to be created.</span></span> <span data-ttu-id="bd71d-167">Das Handle, das von der Funktion zurückgegeben wird, verfügt über die \_ \_ Berechtigung für den Drucker Zugriff und kann verwendet werden, um administrative Vorgänge auf dem Drucker auszuführen.</span><span class="sxs-lookup"><span data-stu-id="bd71d-167">The handle returned by the function will have PRINTER\_ALL\_ACCESS permission, and can be used to perform administrative operations on the printer.</span></span>

<span data-ttu-id="bd71d-168">Wenn der **drvprinterevent** -Funktion das \_ druckerereignisflag kein UI-Flag übermittelt wird \_ \_ \_ , sollte der Treiber während **drvprinterevent** keinen UI-Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="bd71d-168">If the **DrvPrinterEvent** function is passed the PRINTER\_EVENT\_FLAG\_NO\_UI flag, the driver should not use a UI call during **DrvPrinterEvent**.</span></span> <span data-ttu-id="bd71d-169">Zum Ausführen von UI-bezogenen Aufträgen sollte das Installationsprogramm entweder den **vendorsetup** -Eintrag in der INF-Datei des Druckers verwenden, oder für Plug & Play Geräte kann das Installationsprogramm einen gerätespezifischen Co-Installer verwenden.</span><span class="sxs-lookup"><span data-stu-id="bd71d-169">To do UI-related jobs, the installer should either use the **VendorSetup** entry in the printer's .inf file or, for Plug and Play devices, the installer can use a device-specific co-installer.</span></span> <span data-ttu-id="bd71d-170">Weitere Informationen zu **vendorsetup** finden Sie im Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="bd71d-170">For more information about **VendorSetup**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

<span data-ttu-id="bd71d-171">Die Internetverbindungs Firewall (ICF) blockiert standardmäßig die Druckerports, aber eine Ausnahme für die Datei-und Druckfreigabe ist aktiviert, wenn Sie **addprinter** ausführen.</span><span class="sxs-lookup"><span data-stu-id="bd71d-171">The Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing is enabled when you run **AddPrinter**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd71d-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd71d-172">Requirements</span></span>



| <span data-ttu-id="bd71d-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd71d-173">Requirement</span></span> | <span data-ttu-id="bd71d-174">Wert</span><span class="sxs-lookup"><span data-stu-id="bd71d-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd71d-175">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd71d-175">Minimum supported client</span></span><br/> | <span data-ttu-id="bd71d-176">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd71d-176">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bd71d-177">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd71d-177">Minimum supported server</span></span><br/> | <span data-ttu-id="bd71d-178">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd71d-178">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bd71d-179">Header</span><span class="sxs-lookup"><span data-stu-id="bd71d-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd71d-180"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd71d-180"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bd71d-181">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bd71d-181">Library</span></span><br/>                  | <dl> <span data-ttu-id="bd71d-182"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd71d-182"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="bd71d-183">DLL</span><span class="sxs-lookup"><span data-stu-id="bd71d-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd71d-184"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="bd71d-184"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="bd71d-185">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="bd71d-185">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bd71d-186">**Addprinterw** (Unicode) und **addprintera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bd71d-186">**AddPrinterW** (Unicode) and **AddPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="bd71d-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd71d-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd71d-188">Drucken</span><span class="sxs-lookup"><span data-stu-id="bd71d-188">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bd71d-189">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="bd71d-189">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="bd71d-190">**Closeprinter**</span><span class="sxs-lookup"><span data-stu-id="bd71d-190">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="bd71d-191">**Deleteprinter**</span><span class="sxs-lookup"><span data-stu-id="bd71d-191">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="bd71d-192">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="bd71d-192">**EnumPorts**</span></span>](enumports.md)
</dt> <dt>

[<span data-ttu-id="bd71d-193">**Enumprinterdrivers**</span><span class="sxs-lookup"><span data-stu-id="bd71d-193">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="bd71d-194">**Enumprintprozessoren**</span><span class="sxs-lookup"><span data-stu-id="bd71d-194">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> <dt>

[<span data-ttu-id="bd71d-195">**Enumprintprocessordatatypes**</span><span class="sxs-lookup"><span data-stu-id="bd71d-195">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> <dt>

[<span data-ttu-id="bd71d-196">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="bd71d-196">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="bd71d-197">**Drucker \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="bd71d-197">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="bd71d-198">**Printerproperties**</span><span class="sxs-lookup"><span data-stu-id="bd71d-198">**PrinterProperties**</span></span>](printerproperties.md)
</dt> <dt>

[<span data-ttu-id="bd71d-199">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="bd71d-199">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

