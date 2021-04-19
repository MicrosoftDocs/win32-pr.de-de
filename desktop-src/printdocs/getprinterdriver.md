---
description: Die getprinterdriver-Funktion ruft Treiber Daten für den angegebenen Drucker ab. Wenn der Treiber nicht auf dem lokalen Computer installiert ist, wird er von getprinterdriver installiert.
ms.assetid: 93f859b4-1005-4359-8029-9536d6eeb7e7
title: Getprinterdriver-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver
- GetPrinterDriverA
- GetPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a67a77a8167bf207231d2f3f6f063ed7636e201f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369845"
---
# <a name="getprinterdriver-function"></a><span data-ttu-id="063be-104">Getprinterdriver-Funktion</span><span class="sxs-lookup"><span data-stu-id="063be-104">GetPrinterDriver function</span></span>

<span data-ttu-id="063be-105">Die **getprinterdriver** -Funktion ruft Treiber Daten für den angegebenen Drucker ab.</span><span class="sxs-lookup"><span data-stu-id="063be-105">The **GetPrinterDriver** function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="063be-106">Wenn der Treiber nicht auf dem lokalen Computer installiert ist, wird er von **getprinterdriver** installiert.</span><span class="sxs-lookup"><span data-stu-id="063be-106">If the driver is not installed on the local computer, **GetPrinterDriver** installs it.</span></span>

## <a name="syntax"></a><span data-ttu-id="063be-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="063be-107">Syntax</span></span>


```C++
BOOL GetPrinterDriver(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="063be-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="063be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="063be-109">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="063be-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="063be-110">Ein Handle für den Drucker, für den die Treiber Daten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="063be-110">A handle to the printer for which the driver data should be retrieved.</span></span> <span data-ttu-id="063be-111">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="063be-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="063be-112">nach-oben  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="063be-112">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="063be-113">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt (z. b. Windows x86, Windows ia64 oder Windows x64).</span><span class="sxs-lookup"><span data-stu-id="063be-113">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="063be-114">Wenn dieser Parameter **null** ist, wird die aktuelle Umgebung der aufrufenden Anwendung und des Client Computers (nicht der Zielanwendung und des Druck Servers) verwendet.</span><span class="sxs-lookup"><span data-stu-id="063be-114">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="063be-115">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="063be-115">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="063be-116">Die Druckertreiber Struktur, die im *pdriverinfo* -Puffer zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="063be-116">The printer driver structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="063be-117">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="063be-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="063be-118">Wert</span><span class="sxs-lookup"><span data-stu-id="063be-118">Value</span></span>                                                                                                | <span data-ttu-id="063be-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="063be-119">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="063be-120"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="063be-120"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="063be-121">**Treiber \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="063be-121">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="063be-122"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="063be-122"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="063be-123">**Treiber \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="063be-123">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="063be-124"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="063be-124"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="063be-125">**Treiber \_ Info \_ 3**</span><span class="sxs-lookup"><span data-stu-id="063be-125">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="063be-126"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="063be-126"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="063be-127">**Treiber \_ Info \_ 4**</span><span class="sxs-lookup"><span data-stu-id="063be-127">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="063be-128"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="063be-128"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="063be-129">**Treiber \_ Informationen \_ 5**</span><span class="sxs-lookup"><span data-stu-id="063be-129">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="063be-130"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="063be-130"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="063be-131">**Treiber \_ Info \_ 6**</span><span class="sxs-lookup"><span data-stu-id="063be-131">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="063be-132"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="063be-132"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="063be-133">**Treiber \_ Informationen \_ 8**</span><span class="sxs-lookup"><span data-stu-id="063be-133">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="063be-134">*pdriverinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="063be-134">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="063be-135">Ein Zeiger auf einen Puffer, der eine-Struktur mit Informationen über den Treiber empfängt, wie von Level angegeben.</span><span class="sxs-lookup"><span data-stu-id="063be-135">A pointer to a buffer that receives a structure containing information about the driver, as specified by Level.</span></span> <span data-ttu-id="063be-136">Der Puffer muss groß genug sein, um die Zeichen folgen zu speichern, auf die von den Strukturmembern verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="063be-136">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="063be-137">Um die erforderliche Puffergröße zu ermitteln, müssen Sie **getprinterdriver** aufrufen, wobei *cbbuf* auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="063be-137">To determine the required buffer size, call **GetPrinterDriver** with *cbBuf* set to zero.</span></span> <span data-ttu-id="063be-138">**Getprinterdriver** schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen fehlerhaften \_ Puffer zurück \_ , und der *pcbrequired* -Parameter gibt die Größe (in Bytes) des Puffers zurück, der für das Array von Strukturen und deren Daten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="063be-138">**GetPrinterDriver** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="063be-139">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="063be-139">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="063be-140">Die Größe (in Bytes) des Arrays, bei dem *pdriverinfo* zeigt.</span><span class="sxs-lookup"><span data-stu-id="063be-140">The size, in bytes, of the array at which *pDriverInfo* points.</span></span>

</dd> <dt>

<span data-ttu-id="063be-141">*pcbbenötigte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="063be-141">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="063be-142">Ein Zeiger auf einen Wert, der die Anzahl der kopierten Bytes empfängt, wenn die Funktion erfolgreich ausgeführt wird, oder die Anzahl der Bytes, die erforderlich sind, wenn *cbbuf* zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="063be-142">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="063be-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="063be-143">Return value</span></span>

<span data-ttu-id="063be-144">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="063be-144">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="063be-145">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="063be-145">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="063be-146">Bei einem nicht vorhandenen Treiber gibt die Funktion den Fehler \_ unbekannten \_ Druckertreiber zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="063be-146">For a non-existent driver, the function returns ERROR\_UNKNOWN\_PRINTER\_DRIVER.</span></span>

## <a name="remarks"></a><span data-ttu-id="063be-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="063be-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="063be-148">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="063be-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="063be-149">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="063be-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="063be-150">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="063be-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="063be-151">Die Strukturen " [**Treiber Info \_ \_ 2**](driver-info-2.md)", " [**Driver \_ Info \_ 3**](driver-info-3.md)", "Driver Info [**\_ \_ 4**](driver-info-4.md)", "Driver Info [**\_ \_ 5**](driver-info-5.md)" und " [**Driver \_ Info \_ 6**](driver-info-6.md) " enthalten den Dateinamen oder den vollständigen Pfad und Dateinamen des Druckertreibers im **pdriverpath** -Member.</span><span class="sxs-lookup"><span data-stu-id="063be-151">The [**DRIVER\_INFO\_2**](driver-info-2.md), [**DRIVER\_INFO\_3**](driver-info-3.md), [**DRIVER\_INFO\_4**](driver-info-4.md), [**DRIVER\_INFO\_5**](driver-info-5.md), and [**DRIVER\_INFO\_6**](driver-info-6.md) structures contain the file name or the full path and file name of the printer driver in the **pDriverPath** member.</span></span> <span data-ttu-id="063be-152">Eine Anwendung kann den Pfad und den Dateinamen verwenden, um einen Druckertreiber zu laden, indem die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion aufgerufen und der Pfad und der Dateiname als einzelnes Argument bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="063be-152">An application can use the path and file name to load a printer driver by calling the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function and supplying the path and file name as the single argument.</span></span>

## <a name="requirements"></a><span data-ttu-id="063be-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="063be-153">Requirements</span></span>



| <span data-ttu-id="063be-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="063be-154">Requirement</span></span> | <span data-ttu-id="063be-155">Wert</span><span class="sxs-lookup"><span data-stu-id="063be-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="063be-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="063be-156">Minimum supported client</span></span><br/> | <span data-ttu-id="063be-157">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="063be-157">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="063be-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="063be-158">Minimum supported server</span></span><br/> | <span data-ttu-id="063be-159">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="063be-159">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="063be-160">Header</span><span class="sxs-lookup"><span data-stu-id="063be-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="063be-161"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="063be-161"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="063be-162">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="063be-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="063be-163"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="063be-163"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="063be-164">DLL</span><span class="sxs-lookup"><span data-stu-id="063be-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="063be-165"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="063be-165"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="063be-166">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="063be-166">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="063be-167">**Getprinterdriverw** (Unicode) und **getprinterdrivera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="063be-167">**GetPrinterDriverW** (Unicode) and **GetPrinterDriverA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="063be-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="063be-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="063be-169">Drucken</span><span class="sxs-lookup"><span data-stu-id="063be-169">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="063be-170">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="063be-170">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="063be-171">**Addprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="063be-171">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="063be-172">**Treiber \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="063be-172">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="063be-173">**Treiber \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="063be-173">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="063be-174">**Treiber \_ Info \_ 3**</span><span class="sxs-lookup"><span data-stu-id="063be-174">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="063be-175">**Treiber \_ Info \_ 4**</span><span class="sxs-lookup"><span data-stu-id="063be-175">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="063be-176">**Treiber \_ Informationen \_ 5**</span><span class="sxs-lookup"><span data-stu-id="063be-176">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="063be-177">**Treiber \_ Info \_ 6**</span><span class="sxs-lookup"><span data-stu-id="063be-177">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="063be-178">**Enumprinterdrivers**</span><span class="sxs-lookup"><span data-stu-id="063be-178">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="063be-179">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="063be-179">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

