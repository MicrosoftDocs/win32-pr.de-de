---
description: Die GetPrinterDriver2-Funktion ruft Treiber Daten für den angegebenen Drucker ab. Wenn der Treiber nicht auf dem lokalen Computer installiert ist, installiert GetPrinterDriver2 ihn und zeigt eine beliebige Benutzeroberfläche für das angegebene Fenster an.
ms.assetid: 0d482d28-7668-4734-ba71-5b355c18ddec
title: GetPrinterDriver2-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver2
- GetPrinterDriver2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b0a9d2bfe7827a2c0e3db9fff9e8249b73bf5102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218226"
---
# <a name="getprinterdriver2-function"></a><span data-ttu-id="8a646-104">GetPrinterDriver2-Funktion</span><span class="sxs-lookup"><span data-stu-id="8a646-104">GetPrinterDriver2 function</span></span>

<span data-ttu-id="8a646-105">Die **GetPrinterDriver2** -Funktion ruft Treiber Daten für den angegebenen Drucker ab.</span><span class="sxs-lookup"><span data-stu-id="8a646-105">The **GetPrinterDriver2** function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="8a646-106">Wenn der Treiber nicht auf dem lokalen Computer installiert ist, installiert **GetPrinterDriver2** ihn und zeigt eine beliebige Benutzeroberfläche für das angegebene Fenster an.</span><span class="sxs-lookup"><span data-stu-id="8a646-106">If the driver is not installed on the local computer, **GetPrinterDriver2** installs it and displays any user interface to the specified window.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a646-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a646-107">Syntax</span></span>


```C++
BOOL GetPrinterDriver2(
  _In_opt_ HWND    hWnd,
  _In_     HANDLE  hPrinter,
  _In_opt_ LPTSTR  pEnvironment,
  _In_     DWORD   Level,
  _Out_    LPBYTE  pDriverInfo,
  _In_     DWORD   cbBuf,
  _Out_    LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="8a646-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a646-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a646-109">*HWND* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8a646-109">*hWnd* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a646-110">Ein Handle des Fensters, das als übergeordnetes Fenster einer beliebigen Benutzeroberfläche verwendet wird, z. b. ein Dialogfeld, das der Treiber während der Installation anzeigt.</span><span class="sxs-lookup"><span data-stu-id="8a646-110">A handle of the window that will be used as the parent window of any user interface, such as a dialog box, that the driver displays during installation.</span></span> <span data-ttu-id="8a646-111">Wenn der Wert dieses Parameters **null** ist, wird die Benutzeroberfläche des Treibers während der Installation weiterhin für den Benutzer angezeigt, aber es ist kein übergeordnetes Fenster vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8a646-111">If the value of this parameter is **NULL**, the driver's user interface will still be displayed to the user during installation, but it will not have a parent window.</span></span>

</dd> <dt>

<span data-ttu-id="8a646-112">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a646-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a646-113">Ein Handle für den Drucker, für den die Treiber Daten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8a646-113">A handle to the printer for which the driver data should be retrieved.</span></span> <span data-ttu-id="8a646-114">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="8a646-114">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="8a646-115">nach-oben  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8a646-115">*pEnvironment* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a646-116">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt (z. b. Windows x86, Windows ia64 oder Windows x64).</span><span class="sxs-lookup"><span data-stu-id="8a646-116">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="8a646-117">Wenn dieser Parameter **null** ist, wird die aktuelle Umgebung der aufrufenden Anwendung und des Client Computers (nicht der Zielanwendung und des Druck Servers) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a646-117">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="8a646-118">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a646-118">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a646-119">Die Druckertreiber Struktur, die im *pdriverinfo* -Puffer zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8a646-119">The printer driver structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="8a646-120">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="8a646-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="8a646-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8a646-121">Value</span></span>                                                                                                | <span data-ttu-id="8a646-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8a646-122">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="8a646-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="8a646-123"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="8a646-124">**Treiber \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="8a646-124">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="8a646-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="8a646-125"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="8a646-126">**Treiber \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="8a646-126">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="8a646-127"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="8a646-127"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="8a646-128">**Treiber \_ Info \_ 3**</span><span class="sxs-lookup"><span data-stu-id="8a646-128">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="8a646-129"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="8a646-129"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="8a646-130">**Treiber \_ Info \_ 4**</span><span class="sxs-lookup"><span data-stu-id="8a646-130">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="8a646-131"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="8a646-131"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="8a646-132">**Treiber \_ Informationen \_ 5**</span><span class="sxs-lookup"><span data-stu-id="8a646-132">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="8a646-133"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="8a646-133"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="8a646-134">**Treiber \_ Info \_ 6**</span><span class="sxs-lookup"><span data-stu-id="8a646-134">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="8a646-135"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="8a646-135"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="8a646-136">**Treiber \_ Informationen \_ 8**</span><span class="sxs-lookup"><span data-stu-id="8a646-136">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="8a646-137">*pdriverinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8a646-137">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a646-138">Ein Zeiger auf einen Puffer, der eine-Struktur mit Informationen über den Treiber empfängt, wie von *Level* angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a646-138">A pointer to a buffer that receives a structure containing information about the driver, as specified by *Level*.</span></span> <span data-ttu-id="8a646-139">Der Puffer muss groß genug sein, um die Zeichen folgen zu speichern, auf die von den Strukturmembern verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8a646-139">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="8a646-140">Um die erforderliche Puffergröße zu ermitteln, müssen Sie **GetPrinterDriver2** mit *cbbuf* auf 0 (null) festlegen.</span><span class="sxs-lookup"><span data-stu-id="8a646-140">To determine the required buffer size, call **GetPrinterDriver2** with *cbBuf* set to zero.</span></span> <span data-ttu-id="8a646-141">**GetPrinterDriver2** schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen **fehlerhaften \_ \_ Puffer** zurück, und der *pcbrequired* -Parameter gibt die Größe (in Bytes) des Puffers zurück, der für das Array von Strukturen und deren Daten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8a646-141">**GetPrinterDriver2** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="8a646-142">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a646-142">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a646-143">Die Größe (in Bytes) des Arrays, bei dem *pdriverinfo* zeigt.</span><span class="sxs-lookup"><span data-stu-id="8a646-143">The size, in bytes, of the array at which *pDriverInfo* points.</span></span>

</dd> <dt>

<span data-ttu-id="8a646-144">*pcbbenötigte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8a646-144">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a646-145">Ein Zeiger auf einen Wert, der die Anzahl der kopierten Bytes empfängt, wenn die Funktion erfolgreich ausgeführt wird, oder die Anzahl der Bytes, die erforderlich sind, wenn *cbbuf* zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="8a646-145">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a646-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a646-146">Return value</span></span>

<span data-ttu-id="8a646-147">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="8a646-147">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="8a646-148">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="8a646-148">If the function fails, the return value is zero.</span></span> <span data-ttu-id="8a646-149">Um den Rückgabestatus abzurufen, nennen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="8a646-149">To get the return status, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="8a646-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a646-150">Remarks</span></span>

<span data-ttu-id="8a646-151">Die [**Strukturen \_ Treiber \_ Info 2**](driver-info-2.md), [**Driver \_ Info \_ 3**](driver-info-3.md), [**Driver \_ Info \_ 4**](driver-info-4.md), [**Driver \_ Info \_ 5**](driver-info-5.md), [**Driver \_ Info \_ 6**](driver-info-6.md)und [**Driver \_ Info \_ 8**](driver-info-8.md) enthalten den Dateinamen oder den vollständigen Pfad und den Dateinamen des Druckertreibers im **pdriverpath** -Member.</span><span class="sxs-lookup"><span data-stu-id="8a646-151">The [**DRIVER\_INFO\_2**](driver-info-2.md), [**DRIVER\_INFO\_3**](driver-info-3.md), [**DRIVER\_INFO\_4**](driver-info-4.md), [**DRIVER\_INFO\_5**](driver-info-5.md), [**DRIVER\_INFO\_6**](driver-info-6.md), and [**DRIVER\_INFO\_8**](driver-info-8.md) structures contain the file name or the full path and file name of the printer driver in the **pDriverPath** member.</span></span> <span data-ttu-id="8a646-152">Eine Anwendung kann den Pfad und den Dateinamen verwenden, um einen Druckertreiber zu laden, indem die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion aufgerufen und der Pfad und der Dateiname als einzelnes Argument bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8a646-152">An application can use the path and file name to load a printer driver by calling the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function and supplying the path and file name as the single argument.</span></span>

<span data-ttu-id="8a646-153">Die ANSI-Version dieser Funktion, **GetPrinterDriver2A** wird nicht unterstützt und gibt einen Fehler zurück, der **\_ nicht \_ unterstützt** wird.</span><span class="sxs-lookup"><span data-stu-id="8a646-153">The ANSI version of this function, **GetPrinterDriver2A** is not supported and returns **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a646-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a646-154">Requirements</span></span>



| <span data-ttu-id="8a646-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a646-155">Requirement</span></span> | <span data-ttu-id="8a646-156">Wert</span><span class="sxs-lookup"><span data-stu-id="8a646-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a646-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8a646-157">Minimum supported client</span></span><br/> | <span data-ttu-id="8a646-158">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a646-158">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="8a646-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8a646-159">Minimum supported server</span></span><br/> | <span data-ttu-id="8a646-160">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a646-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8a646-161">Header</span><span class="sxs-lookup"><span data-stu-id="8a646-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a646-162"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a646-162"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8a646-163">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8a646-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="8a646-164"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a646-164"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8a646-165">DLL</span><span class="sxs-lookup"><span data-stu-id="8a646-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a646-166"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="8a646-166"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="8a646-167">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="8a646-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8a646-168">**GetPrinterDriver2W** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="8a646-168">**GetPrinterDriver2W** (Unicode)</span></span><br/>                                                               |



## <a name="see-also"></a><span data-ttu-id="8a646-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a646-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a646-170">Drucken</span><span class="sxs-lookup"><span data-stu-id="8a646-170">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8a646-171">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="8a646-171">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="8a646-172">**Addprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="8a646-172">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="8a646-173">**Treiber \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="8a646-173">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="8a646-174">**Treiber \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="8a646-174">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="8a646-175">**Treiber \_ Info \_ 3**</span><span class="sxs-lookup"><span data-stu-id="8a646-175">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="8a646-176">**Treiber \_ Info \_ 4**</span><span class="sxs-lookup"><span data-stu-id="8a646-176">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="8a646-177">**Treiber \_ Informationen \_ 5**</span><span class="sxs-lookup"><span data-stu-id="8a646-177">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="8a646-178">**Treiber \_ Info \_ 6**</span><span class="sxs-lookup"><span data-stu-id="8a646-178">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="8a646-179">**Enumprinterdrivers**</span><span class="sxs-lookup"><span data-stu-id="8a646-179">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="8a646-180">**Getprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="8a646-180">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="8a646-181">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="8a646-181">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

