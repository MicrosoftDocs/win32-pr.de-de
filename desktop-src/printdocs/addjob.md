---
description: Die AddJob-Funktion fügt der Liste der Druckaufträge, die vom Druck Spooler geplant werden können, einen Druckauftrag hinzu. Die-Funktion Ruft den Namen der Datei ab, die Sie verwenden können, um den Auftrag zu speichern.
ms.assetid: cfafa874-6022-4bf4-bf3d-096213eb0c98
title: AddJob-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddJob
- AddJobA
- AddJobW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab21b98036975934c00e28d0be1d5670d4c0742c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756409"
---
# <a name="addjob-function"></a><span data-ttu-id="fda51-104">AddJob-Funktion</span><span class="sxs-lookup"><span data-stu-id="fda51-104">AddJob function</span></span>

<span data-ttu-id="fda51-105">Die **AddJob** -Funktion fügt der Liste der Druckaufträge, die vom Druck Spooler geplant werden können, einen Druckauftrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="fda51-105">The **AddJob** function adds a print job to the list of print jobs that can be scheduled by the print spooler.</span></span> <span data-ttu-id="fda51-106">Die-Funktion Ruft den Namen der Datei ab, die Sie verwenden können, um den Auftrag zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fda51-106">The function retrieves the name of the file you can use to store the job.</span></span>

> [!NOTE]
> <span data-ttu-id="fda51-107">In Windows 8 und höheren Betriebssystemen wird die Verwendung von **AddJob** nicht direkt empfohlen, da es Fälle gibt (z. b. das Drucken in eine Warteschlange mithilfe von file: oder portprompt:) bei **AddJob** tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="fda51-107">In Windows 8 and later operating systems, we do not recommended using **AddJob** directly because there are cases (such as printing to a queue using File: or PORTPROMPT:) where **AddJob** will fail.</span></span> <span data-ttu-id="fda51-108">Stattdessen empfiehlt es sich, abhängig vom Druck Szenario [GDI-Druck-API](gdi-printing.md), [XPS-Druck-API](xps-printing.md), [**StartDocPrinter**](startdocprinter.md)oder die entsprechende Methode aus dem [**Windows. Graphics. Printing**](/uwp/api/Windows.Graphics.Printing) -Namespace zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fda51-108">Instead, you are advised to use [GDI Print API](gdi-printing.md), [XPS Print API](xps-printing.md), [**StartDocPrinter**](startdocprinter.md), or the appropriate method from the [**Windows.Graphics.Printing**](/uwp/api/Windows.Graphics.Printing) namespace, depending on the print scenario.</span></span>
>
> <span data-ttu-id="fda51-109">Wenn Sie versuchen, in einer Warteschlange mithilfe von **file:** oder **portprompt:** zu drucken, gibt **AddJob** den nicht \_ unterstützten Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="fda51-109">If you try to print to a queue using **File:** or **PORTPROMPT:**, **AddJob** will Return the NOT\_SUPPORTED error.</span></span>

## <a name="syntax"></a><span data-ttu-id="fda51-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="fda51-110">Syntax</span></span>

```C++
BOOL AddJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```

## <a name="parameters"></a><span data-ttu-id="fda51-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fda51-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fda51-112">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fda51-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fda51-113">Ein Handle, das den Drucker für den Druckauftrag angibt.</span><span class="sxs-lookup"><span data-stu-id="fda51-113">A handle that specifies the printer for the print job.</span></span> <span data-ttu-id="fda51-114">Dabei muss es sich um einen lokalen Drucker handeln, der als Druck Drucker konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="fda51-114">This must be a local printer that is configured as a spooled printer.</span></span> <span data-ttu-id="fda51-115">Wenn *hprinter* ein Handle für eine Remote Druckerverbindung ist oder wenn der Drucker für den direkten Druck konfiguriert ist, tritt bei der **AddJob** -Funktion ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="fda51-115">If *hPrinter* is a handle to a remote printer connection, or if the printer is configured for direct printing, the **AddJob** function fails.</span></span> <span data-ttu-id="fda51-116">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="fda51-116">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="fda51-117">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fda51-117">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fda51-118">Die Version der Datenstruktur der Druckauftrags Informationen, die die Funktion im Puffer speichert, auf die von *pData* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="fda51-118">The version of the print job information data structure that the function stores into the buffer pointed to by *pData*.</span></span> <span data-ttu-id="fda51-119">Legen Sie diesen Parameter auf einen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="fda51-119">Set this parameter to one.</span></span>

</dd> <dt>

<span data-ttu-id="fda51-120">*pData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fda51-120">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fda51-121">Ein Zeiger auf einen Puffer, der eine Datenstruktur vom Typ [**AddJob \_ Info \_ 1**](addjob-info-1.md) und eine Pfad Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="fda51-121">A pointer to a buffer that receives an [**ADDJOB\_INFO\_1**](addjob-info-1.md) data structure and a path string.</span></span>

</dd> <dt>

<span data-ttu-id="fda51-122">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fda51-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fda51-123">Die Größe (in Bytes) des Puffers, auf den *pData* zeigt.</span><span class="sxs-lookup"><span data-stu-id="fda51-123">The size, in bytes, of the buffer pointed to by *pData*.</span></span> <span data-ttu-id="fda51-124">Der Puffer muss groß genug sein, um eine [**AddJob \_ Info \_ 1**](addjob-info-1.md) -Struktur und eine Pfad Zeichenfolge zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="fda51-124">The buffer needs to be large enough to contain an [**ADDJOB\_INFO\_1**](addjob-info-1.md) structure and a path string.</span></span>

</dd> <dt>

<span data-ttu-id="fda51-125">*pcbbenötigte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fda51-125">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fda51-126">Ein Zeiger auf eine Variable, die die Gesamtgröße der Datenstruktur von [**AddJob \_ Info \_ 1**](addjob-info-1.md) in Bytes und die Pfad Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="fda51-126">A pointer to a variable that receives the total size, in bytes, of the [**ADDJOB\_INFO\_1**](addjob-info-1.md) data structure plus the path string.</span></span> <span data-ttu-id="fda51-127">Wenn dieser Wert kleiner oder gleich *cbbuf* ist und die Funktion erfolgreich ist, ist dies die tatsächliche Anzahl von Bytes, die in den Puffer geschrieben werden, auf den *pData* zeigt.</span><span class="sxs-lookup"><span data-stu-id="fda51-127">If this value is less than or equal to *cbBuf* and the function succeeds, this is the actual number of bytes written to the buffer pointed to by *pData*.</span></span> <span data-ttu-id="fda51-128">Wenn diese Zahl größer als *cbbuf* ist, ist der Puffer zu klein, und Sie müssen die Funktion mit einer Puffergröße, die mindestens so groß wie \* *pcbbenöist*, erneut aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="fda51-128">If this number is greater than *cbBuf*, the buffer is too small, and you must call the function again with a buffer size at least as large as \**pcbNeeded*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fda51-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fda51-129">Return value</span></span>

<span data-ttu-id="fda51-130">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="fda51-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="fda51-131">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="fda51-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fda51-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fda51-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fda51-133">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fda51-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="fda51-134">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="fda51-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="fda51-135">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="fda51-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="fda51-136">Sie können die Funktion "-Funktion" aufrufen, um die Spooldatei zu öffnen, die vom **path** -Member der [**AddJob \_ Info \_ 1**](addjob-info-1.md) -Struktur angegeben wird, und dann [**die Funktion "**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile) " aufrufen, um Druckauftrags Daten in die Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="fda51-136">You can call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open the spool file specified by the **Path** member of the [**ADDJOB\_INFO\_1**](addjob-info-1.md) structure, and then call the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function to write print job data to it.</span></span> <span data-ttu-id="fda51-137">Nachdem dies geschehen ist, wird die [**schedulejob**](schedulejob.md) -Funktion aufgerufen, um den Druck Spooler zu benachrichtigen, dass der Druckauftrag jetzt vom Spooler für den Druck geplant werden kann.</span><span class="sxs-lookup"><span data-stu-id="fda51-137">After that is done, call the [**ScheduleJob**](schedulejob.md) function to notify the print spooler that the print job can now be scheduled by the spooler for printing.</span></span>

## <a name="requirements"></a><span data-ttu-id="fda51-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fda51-138">Requirements</span></span>



| <span data-ttu-id="fda51-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fda51-139">Requirement</span></span> | <span data-ttu-id="fda51-140">Wert</span><span class="sxs-lookup"><span data-stu-id="fda51-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fda51-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fda51-141">Minimum supported client</span></span><br/> | <span data-ttu-id="fda51-142">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fda51-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fda51-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fda51-143">Minimum supported server</span></span><br/> | <span data-ttu-id="fda51-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fda51-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fda51-145">Header</span><span class="sxs-lookup"><span data-stu-id="fda51-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="fda51-146"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fda51-146"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fda51-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fda51-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="fda51-148"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fda51-148"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="fda51-149">DLL</span><span class="sxs-lookup"><span data-stu-id="fda51-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fda51-150"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="fda51-150"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="fda51-151">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="fda51-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fda51-152">**Addjobw** (Unicode) und **addjoba** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fda51-152">**AddJobW** (Unicode) and **AddJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="fda51-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fda51-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fda51-154">**AddJob- \_ Info \_ 1**</span><span class="sxs-lookup"><span data-stu-id="fda51-154">**ADDJOB\_INFO\_1**</span></span>](addjob-info-1.md)
</dt> <dt>

[<span data-ttu-id="fda51-155">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="fda51-155">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="fda51-156">GDI-Druck-API</span><span class="sxs-lookup"><span data-stu-id="fda51-156">GDI Print API</span></span>](gdi-printing.md)
</dt> <dt>

[<span data-ttu-id="fda51-157">Drucken</span><span class="sxs-lookup"><span data-stu-id="fda51-157">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fda51-158">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="fda51-158">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="fda51-159">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="fda51-159">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="fda51-160">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="fda51-160">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="fda51-161">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="fda51-161">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="fda51-162">**Windows. Graphics. Printing**</span><span class="sxs-lookup"><span data-stu-id="fda51-162">**Windows.Graphics.Printing**</span></span>](/uwp/api/Windows.Graphics.Printing)
</dt> <dt>

[<span data-ttu-id="fda51-163">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="fda51-163">**WriteFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-writefile)
</dt> <dt>

[<span data-ttu-id="fda51-164">XPS-Druck-API</span><span class="sxs-lookup"><span data-stu-id="fda51-164">XPS Print API</span></span>](xps-printing.md)
</dt> </dl>

 

