---
description: Die Funktion "Write Printer" benachrichtigt den Druck Spooler, dass Daten in den angegebenen Drucker geschrieben werden sollen.
ms.assetid: 9411b71f-d686-44ed-9051-d410e5ab228e
title: Funktion "Write Printer" (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WritePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 490221b15ed1e3c7dad3a4cb523c15e9ec484b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358916"
---
# <a name="writeprinter-function"></a><span data-ttu-id="d549a-103">Funktion "Write Printer"</span><span class="sxs-lookup"><span data-stu-id="d549a-103">WritePrinter function</span></span>

<span data-ttu-id="d549a-104">Die Funktion " **Write Printer** " benachrichtigt den Druck Spooler, dass Daten in den angegebenen Drucker geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d549a-104">The **WritePrinter** function notifies the print spooler that data should be written to the specified printer.</span></span>

> [!Note]  
> <span data-ttu-id="d549a-105">" **Write Printer** " unterstützt nur den GDI-Druck und darf nicht für den XPS-Druck verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d549a-105">**WritePrinter** only supports GDI printing and must not be used for XPS printing.</span></span> <span data-ttu-id="d549a-106">Wenn der Druckauftrag den XPS-oder den openxps-Druckpfad verwendet, verwenden Sie die [XPS-Druck-API](/windows/desktop/printdocs/xps-printing).</span><span class="sxs-lookup"><span data-stu-id="d549a-106">If your print job uses the XPS or the OpenXPS print path, then use the [XPS Print API](/windows/desktop/printdocs/xps-printing).</span></span> <span data-ttu-id="d549a-107">Das Senden von XPS-oder openxps-Druckaufträgen an den Spooler mithilfe von " **Write Printer** " wird nicht unterstützt und kann zu unbestimmten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="d549a-107">Sending XPS or OpenXPS print jobs to the spooler using **WritePrinter** is not supported and can result in undetermined results.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d549a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d549a-108">Syntax</span></span>


```C++
BOOL WritePrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten
);
```



## <a name="parameters"></a><span data-ttu-id="d549a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d549a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d549a-110">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d549a-110">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d549a-111">Ein Handle für den Drucker.</span><span class="sxs-lookup"><span data-stu-id="d549a-111">A handle to the printer.</span></span> <span data-ttu-id="d549a-112">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="d549a-112">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="d549a-113">*PBUF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d549a-113">*pBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d549a-114">Ein Zeiger auf ein Bytearray, das die Daten enthält, die in den Drucker geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d549a-114">A pointer to an array of bytes that contains the data that should be written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="d549a-115">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d549a-115">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d549a-116">Die Größe des Arrays in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d549a-116">The size, in bytes, of the array.</span></span>

</dd> <dt>

<span data-ttu-id="d549a-117">*pcwritten* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d549a-117">*pcWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d549a-118">Ein Zeiger auf einen Wert, der die Anzahl der Daten Bytes empfängt, die an den Drucker geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="d549a-118">A pointer to a value that receives the number of bytes of data that were written to the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d549a-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d549a-119">Return value</span></span>

<span data-ttu-id="d549a-120">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d549a-120">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d549a-121">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="d549a-121">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d549a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d549a-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d549a-123">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d549a-123">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d549a-124">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="d549a-124">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d549a-125">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="d549a-125">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d549a-126">Die Reihenfolge für einen Druckauftrag lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d549a-126">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="d549a-127">Zum Starten eines Druckauftrags aufrufen Sie [**StartDocPrinter**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="d549a-127">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="d549a-128">Um jede Seite zu starten, aufrufen Sie [**startpageprinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="d549a-128">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="d549a-129">Um Daten auf eine Seite zu schreiben, müssen Sie " **Write-Printer**" anrufen.</span><span class="sxs-lookup"><span data-stu-id="d549a-129">To write data to a page, call **WritePrinter**.</span></span>
4.  <span data-ttu-id="d549a-130">Um jede Seite zu beenden, nennen Sie [**endpageprinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="d549a-130">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="d549a-131">Wiederholen Sie den Vorgang 2, 3 und 4 für beliebig viele Seiten.</span><span class="sxs-lookup"><span data-stu-id="d549a-131">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="d549a-132">Um den Druckauftrag zu beenden, nennen Sie [**enddocprinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="d549a-132">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="d549a-133">Wenn ein Dokument auf hoher Ebene (z. b. eine Adobe PDF-oder Microsoft Word-Datei) oder andere Druckerdaten (z. b. PCL, PS oder HPGL) direkt an einen Drucker gesendet werden, werden die im Dokument definierten Druckeinstellungen im Vergleich zu den Windows-Druckeinstellungen Vorrang haben.</span><span class="sxs-lookup"><span data-stu-id="d549a-133">When a high-level document (such as an Adobe PDF or Microsoft Word file) or other printer data (such PCL, PS, or HPGL) is sent directly to a printer, the print settings defined in the document take precedent over Windows print settings.</span></span> <span data-ttu-id="d549a-134">Dokumente, die ausgegeben werden, wenn der Wert des *pdatatype* -Members der [**doc \_ Info \_ 1**](doc-info-1.md) -Struktur, die im *pdocinfo* -Parameter des [**StartDocPrinter**](startdocprinter.md) -Aufrufes aufgerufen wurde, "RAW" ist, muss die Einstellungen des Druckauftrags im [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)-Stil in der von der Hardware erkannten Sprache vollständig beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d549a-134">Documents output when the value of the *pDatatype* member of the [**DOC\_INFO\_1**](doc-info-1.md) structure that was passed in the *pDocInfo* parameter of the [**StartDocPrinter**](startdocprinter.md) call is "RAW" must fully describe the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)-style print job settings in the language understood by the hardware.</span></span>

<span data-ttu-id="d549a-135">Wenn in Windows-Versionen vor Windows XP eine Seite in einer Spooldatei ungefähr 350 MB überschreitet, kann Sie nicht gedruckt werden, und es wird keine Fehlermeldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="d549a-135">In versions of Windows prior to Windows XP, when a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="d549a-136">Dies kann z. b. vorkommen, wenn große EMF-Dateien gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="d549a-136">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="d549a-137">Die Seitengrößen Beschränkung in Windows-Versionen vor Windows XP hängt von vielen Faktoren ab, z. b. von der Menge des verfügbaren virtuellen Arbeitsspeichers, von der durch den Aufruf von Prozessen belegten Arbeitsspeicher Menge und von der Fragmentierung im Prozess Heap.</span><span class="sxs-lookup"><span data-stu-id="d549a-137">The page size limit in versions of Windows prior to Windows XP depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span> <span data-ttu-id="d549a-138">In Windows XP und höheren Versionen von Windows müssen EMF-Dateien 2 GB oder weniger groß sein.</span><span class="sxs-lookup"><span data-stu-id="d549a-138">In Windows XP and later versions of Windows, EMF files must be 2GB or less in size.</span></span> <span data-ttu-id="d549a-139">Wenn zum Schreiben von nicht-EMF-Daten (z. b. Drucker bereite PDL) **der Schreibschutz** verwendet wird, wird die Dateigröße nur durch den verfügbaren Speicherplatz beschränkt.</span><span class="sxs-lookup"><span data-stu-id="d549a-139">If **WritePrinter** is used to write non EMF data, such as printer-ready PDL, the size of the file is limited only by the available disk space.</span></span>

## <a name="examples"></a><span data-ttu-id="d549a-140">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d549a-140">Examples</span></span>

<span data-ttu-id="d549a-141">Ein Beispielprogramm, das diese Funktion verwendet, finden [Sie unter Gewusst wie: Drucken mit der GDI-Druck-API](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="d549a-141">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d549a-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d549a-142">Requirements</span></span>



| <span data-ttu-id="d549a-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d549a-143">Requirement</span></span> | <span data-ttu-id="d549a-144">Wert</span><span class="sxs-lookup"><span data-stu-id="d549a-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d549a-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d549a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d549a-146">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d549a-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d549a-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d549a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d549a-148">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d549a-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d549a-149">Header</span><span class="sxs-lookup"><span data-stu-id="d549a-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="d549a-150"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d549a-150"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d549a-151">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d549a-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="d549a-152"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d549a-152"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d549a-153">DLL</span><span class="sxs-lookup"><span data-stu-id="d549a-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d549a-154"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d549a-154"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="d549a-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d549a-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d549a-156">Drucken</span><span class="sxs-lookup"><span data-stu-id="d549a-156">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d549a-157">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d549a-157">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d549a-158">**Enddocprinter**</span><span class="sxs-lookup"><span data-stu-id="d549a-158">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="d549a-159">**Endpageprinter**</span><span class="sxs-lookup"><span data-stu-id="d549a-159">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="d549a-160">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="d549a-160">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="d549a-161">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="d549a-161">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="d549a-162">**Startpageprinter**</span><span class="sxs-lookup"><span data-stu-id="d549a-162">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="d549a-163">**"Write Printer"**</span><span class="sxs-lookup"><span data-stu-id="d549a-163">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

