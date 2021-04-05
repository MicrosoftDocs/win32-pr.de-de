---
description: Die enumprinterdrivers-Funktion Listet die Druckertreiber auf, die auf einem angegebenen Drucker Server installiert sind.
ms.assetid: fa3d8cf4-70bc-4362-833e-e4217ed5d43b
title: Enumprinterdrivers-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDrivers
- EnumPrinterDriversA
- EnumPrinterDriversW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: c5175daf0a59ac4231baa1a32772863a0017c45d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756396"
---
# <a name="enumprinterdrivers-function"></a><span data-ttu-id="5c4cf-103">Enumprinterdrivers-Funktion</span><span class="sxs-lookup"><span data-stu-id="5c4cf-103">EnumPrinterDrivers function</span></span>

<span data-ttu-id="5c4cf-104">Die **enumprinterdrivers** -Funktion Listet die Druckertreiber auf, die auf einem angegebenen Drucker Server installiert sind.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-104">The **EnumPrinterDrivers** function enumerates the printer drivers installed on a specified printer server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c4cf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c4cf-105">Syntax</span></span>


```C++
BOOL EnumPrinterDrivers(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="5c4cf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c4cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c4cf-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c4cf-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4cf-108">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Servers angibt, auf dem die Druckertreiber aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-108">A pointer to a null-terminated string that specifies the name of the server on which the printer drivers are enumerated.</span></span>

<span data-ttu-id="5c4cf-109">Wenn *PName* den Wert **null** hat, listet die Funktion die lokalen Druckertreiber auf.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-109">If *pName* is **NULL**, the function enumerates the local printer drivers.</span></span>

</dd> <dt>

<span data-ttu-id="5c4cf-110">nach-oben  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c4cf-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4cf-111">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt (z. b. Windows x86, Windows ia64, Windows x64 oder Windows NT R4000).</span><span class="sxs-lookup"><span data-stu-id="5c4cf-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, Windows x64, or Windows NT R4000).</span></span> <span data-ttu-id="5c4cf-112">Wenn dieser Parameter **null** ist, verwendet die Funktion die aktuelle Umgebung des Aufrufers/Clients (nicht des Ziels/Servers).</span><span class="sxs-lookup"><span data-stu-id="5c4cf-112">If this parameter is **NULL**, the function uses the current environment of the caller/client (not of the destination/server).</span></span>

<span data-ttu-id="5c4cf-113">Wenn in *der Zeichen* Folge "" die Zeichenfolge "All" angegeben ist, listet **enumprinterdrivers** Druckertreiber für alle auf dem angegebenen Server installierten Plattformen auf.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-113">If the *pEnvironment* string specifies "all", **EnumPrinterDrivers** enumerates printer drivers for all platforms installed on the specified server.</span></span>

</dd> <dt>

<span data-ttu-id="5c4cf-114">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c4cf-114">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4cf-115">Der Typ der Informationsstruktur, der im *pdriverinfo* -Puffer zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-115">The type of information structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="5c4cf-116">Dies kann einer der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="5c4cf-116">It can be one of the following.</span></span>



| <span data-ttu-id="5c4cf-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5c4cf-117">Value</span></span>                                                                                                | <span data-ttu-id="5c4cf-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5c4cf-118">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="5c4cf-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="5c4cf-119"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="5c4cf-120">**Treiber \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="5c4cf-120">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="5c4cf-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="5c4cf-121"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="5c4cf-122">**Treiber \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="5c4cf-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="5c4cf-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="5c4cf-123"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="5c4cf-124">**Treiber \_ Info \_ 3**</span><span class="sxs-lookup"><span data-stu-id="5c4cf-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="5c4cf-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="5c4cf-125"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="5c4cf-126">**Treiber \_ Info \_ 4**</span><span class="sxs-lookup"><span data-stu-id="5c4cf-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="5c4cf-127"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="5c4cf-127"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="5c4cf-128">**Treiber \_ Informationen \_ 5**</span><span class="sxs-lookup"><span data-stu-id="5c4cf-128">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="5c4cf-129"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="5c4cf-129"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="5c4cf-130">**Treiber \_ Info \_ 6**</span><span class="sxs-lookup"><span data-stu-id="5c4cf-130">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="5c4cf-131"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="5c4cf-131"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="5c4cf-132">**Treiber \_ Informationen \_ 8**</span><span class="sxs-lookup"><span data-stu-id="5c4cf-132">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="5c4cf-133">*pdriverinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5c4cf-133">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4cf-134">Ein Zeiger auf einen Puffer, der ein Array von Treiber \_ Informations \_ \* Strukturen empfängt, wie von *Level* angegeben.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-134">A pointer to a buffer that receives an array of DRIVER\_INFO\_\* structures, as specified by *Level*.</span></span> <span data-ttu-id="5c4cf-135">Jede Struktur enthält Daten, die einen verfügbaren Druckertreiber beschreiben.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-135">Each structure contains data that describes an available printer driver.</span></span> <span data-ttu-id="5c4cf-136">Der Puffer muss groß genug sein, um das Array von Strukturen und Zeichen folgen oder andere Daten zu erhalten, auf die die Strukturmember zeigen.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-136">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="5c4cf-137">Um die erforderliche Puffergröße zu ermitteln, muss **enumprinterdrivers** aufgerufen werden, wobei *cbbuf* auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-137">To determine the required buffer size, call **EnumPrinterDrivers** with *cbBuf* set to zero.</span></span> <span data-ttu-id="5c4cf-138">**Enumprinterdrivers** schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen fehlerhaften \_ Puffer zurück \_ , und der *pcbrequired* -Parameter gibt die Größe (in Bytes) des Puffers zurück, der für das Array von Strukturen und deren Daten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-138">**EnumPrinterDrivers** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="5c4cf-139">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c4cf-139">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4cf-140">Die Größe (in Bytes) des Puffers, auf den *pdriverinfo* zeigt.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-140">The size, in bytes, of the buffer pointed to by *pDriverInfo*</span></span>

</dd> <dt>

<span data-ttu-id="5c4cf-141">*pcbbenötigte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5c4cf-141">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4cf-142">Ein Zeiger auf eine Variable, die die Anzahl von Bytes empfängt, die in den *pdriverinfo* -Puffer kopiert werden, wenn die Funktion erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-142">A pointer to a variable that receives the number of bytes copied to the *pDriverInfo* buffer if the function succeeds.</span></span> <span data-ttu-id="5c4cf-143">Wenn der Puffer zu klein ist, schlägt die Funktion fehl, und die Variable erhält die erforderliche Anzahl von Bytes.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-143">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="5c4cf-144">*pkreturned* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5c4cf-144">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4cf-145">Ein Zeiger auf eine Variable, die die Anzahl der im *pdriverinfo* -Puffer zurückgegebenen Strukturen empfängt.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-145">A pointer to a variable that receives the number of structures returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="5c4cf-146">Dies ist die Anzahl der Druckertreiber, die auf dem angegebenen Drucker Server installiert sind.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-146">This is the number of printer drivers installed on the specified print server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c4cf-147">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c4cf-147">Return value</span></span>

<span data-ttu-id="5c4cf-148">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="5c4cf-148">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="5c4cf-149">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-149">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c4cf-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c4cf-150">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5c4cf-151">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-151">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="5c4cf-152">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-152">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="5c4cf-153">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="5c4cf-153">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5c4cf-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c4cf-154">Requirements</span></span>



| <span data-ttu-id="5c4cf-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c4cf-155">Requirement</span></span> | <span data-ttu-id="5c4cf-156">Wert</span><span class="sxs-lookup"><span data-stu-id="5c4cf-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c4cf-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c4cf-157">Minimum supported client</span></span><br/> | <span data-ttu-id="5c4cf-158">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c4cf-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5c4cf-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c4cf-159">Minimum supported server</span></span><br/> | <span data-ttu-id="5c4cf-160">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c4cf-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5c4cf-161">Header</span><span class="sxs-lookup"><span data-stu-id="5c4cf-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c4cf-162"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c4cf-162"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5c4cf-163">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5c4cf-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="5c4cf-164"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c4cf-164"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="5c4cf-165">DLL</span><span class="sxs-lookup"><span data-stu-id="5c4cf-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c4cf-166"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="5c4cf-166"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="5c4cf-167">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="5c4cf-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5c4cf-168">**Enumprinterdriversw** (Unicode) und **enumprinterdriversa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5c4cf-168">**EnumPrinterDriversW** (Unicode) and **EnumPrinterDriversA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="5c4cf-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c4cf-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c4cf-170">Drucken</span><span class="sxs-lookup"><span data-stu-id="5c4cf-170">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5c4cf-171">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="5c4cf-171">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="5c4cf-172">**Addprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="5c4cf-172">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="5c4cf-173">**Treiber \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="5c4cf-173">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="5c4cf-174">**Treiber \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="5c4cf-174">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="5c4cf-175">**Treiber \_ Info \_ 3**</span><span class="sxs-lookup"><span data-stu-id="5c4cf-175">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="5c4cf-176">**Treiber \_ Info \_ 4**</span><span class="sxs-lookup"><span data-stu-id="5c4cf-176">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="5c4cf-177">**Treiber \_ Informationen \_ 5**</span><span class="sxs-lookup"><span data-stu-id="5c4cf-177">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="5c4cf-178">**Treiber \_ Info \_ 6**</span><span class="sxs-lookup"><span data-stu-id="5c4cf-178">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="5c4cf-179">**Getprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="5c4cf-179">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

