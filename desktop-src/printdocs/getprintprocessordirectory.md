---
description: Die getprintprocessordirectory-Funktion Ruft den Pfad zum Druck Prozessor Verzeichnis auf dem angegebenen Server ab.
ms.assetid: a2443cfd-e5ba-41c6-aaf4-45051a3d0e26
title: Getprintprocessordirectory-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintProcessorDirectory
- GetPrintProcessorDirectoryA
- GetPrintProcessorDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: a105025ba22c7e188b8dd20df67f5e8ad28fce01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868536"
---
# <a name="getprintprocessordirectory-function"></a><span data-ttu-id="cb191-103">Getprintprocessordirectory-Funktion</span><span class="sxs-lookup"><span data-stu-id="cb191-103">GetPrintProcessorDirectory function</span></span>

<span data-ttu-id="cb191-104">Die **getprintprocessordirectory** -Funktion Ruft den Pfad zum Druck Prozessor Verzeichnis auf dem angegebenen Server ab.</span><span class="sxs-lookup"><span data-stu-id="cb191-104">The **GetPrintProcessorDirectory** function retrieves the path to the print processor directory on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb191-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb191-105">Syntax</span></span>


```C++
BOOL GetPrintProcessorDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="cb191-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb191-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb191-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb191-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb191-108">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Servers angibt.</span><span class="sxs-lookup"><span data-stu-id="cb191-108">A pointer to a null-terminated string that specifies the name of the server.</span></span> <span data-ttu-id="cb191-109">Wenn dieser Parameter **null** ist, wird ein lokaler Pfad zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cb191-109">If this parameter is **NULL**, a local path is returned.</span></span>

</dd> <dt>

<span data-ttu-id="cb191-110">nach-oben  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb191-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb191-111">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt (z. b. Windows x86, Windows ia64 oder Windows x64).</span><span class="sxs-lookup"><span data-stu-id="cb191-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="cb191-112">Wenn dieser Parameter **null** ist, wird die aktuelle Umgebung der aufrufenden Anwendung und des Client Computers (nicht der Zielanwendung und des Druck Servers) verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb191-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="cb191-113">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb191-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb191-114">Die Struktur Ebene.</span><span class="sxs-lookup"><span data-stu-id="cb191-114">The structure level.</span></span> <span data-ttu-id="cb191-115">Dieser Wert muss 1 sein.</span><span class="sxs-lookup"><span data-stu-id="cb191-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="cb191-116">*pprintprocessorinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cb191-116">*pPrintProcessorInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb191-117">Ein Zeiger auf einen Puffer, der den Pfad empfängt.</span><span class="sxs-lookup"><span data-stu-id="cb191-117">A pointer to a buffer that receives the path.</span></span> <span data-ttu-id="cb191-118">Beachten Sie, dass für Betriebssysteme vor Windows Server 2003 SP 1 der Pfad im lokalen Format für den Server und nicht das tatsächliche Remote Format vorliegt.</span><span class="sxs-lookup"><span data-stu-id="cb191-118">Note that, for operating systems prior to Windows Server 2003 SP 1, the path is in the local format for the server, not the true remote format.</span></span> <span data-ttu-id="cb191-119">Der Pfad wird beispielsweise als "% windir% \\ system32 \\ Spool \\ prtprocs \\ % Environment%" anstelle von " \\ \\ Servername \\ Print $ \\ prtprocs \\ % Environment%" angegeben, auch wenn er für einen Remote Server aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cb191-119">For example, the path is given as "%Windir%\\System32\\Spool\\Prtprocs\\%Environment%" instead of "\\\\ServerName\\Print$\\Prtprocs\\%Environment%", even when called for a remote server.</span></span> <span data-ttu-id="cb191-120">Für die Betriebssysteme Windows Server 2003 SP 1 und höher wird der echte Remote Pfad zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cb191-120">For the operating systems Windows Server 2003 SP 1 and later, the true remote path is returned.</span></span>

</dd> <dt>

<span data-ttu-id="cb191-121">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb191-121">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb191-122">Die Größe des Puffers, auf den von *pprintprocessorinfo* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cb191-122">The size of the buffer pointed to by *pPrintProcessorInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="cb191-123">*pcbbenötigte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cb191-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb191-124">Ein Zeiger auf einen-Wert, der die Anzahl der Bytes angibt, die beim Erfolg der Funktion kopiert werden, oder die Anzahl der Bytes, die erforderlich sind, wenn *cbbuf* zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="cb191-124">A pointer to a value that specifies the number of bytes copied if the function succeeds, or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb191-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb191-125">Return value</span></span>

<span data-ttu-id="cb191-126">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="cb191-126">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="cb191-127">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="cb191-127">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb191-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb191-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cb191-129">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cb191-129">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="cb191-130">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="cb191-130">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="cb191-131">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="cb191-131">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cb191-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb191-132">Requirements</span></span>



| <span data-ttu-id="cb191-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb191-133">Requirement</span></span> | <span data-ttu-id="cb191-134">Wert</span><span class="sxs-lookup"><span data-stu-id="cb191-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb191-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb191-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cb191-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb191-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cb191-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb191-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cb191-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb191-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cb191-139">Header</span><span class="sxs-lookup"><span data-stu-id="cb191-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb191-140"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb191-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="cb191-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cb191-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="cb191-142"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb191-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="cb191-143">DLL</span><span class="sxs-lookup"><span data-stu-id="cb191-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb191-144"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="cb191-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="cb191-145">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="cb191-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cb191-146">**Getprintprocessordirectoren** (Unicode) und **getprintprocessordirector ya** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cb191-146">**GetPrintProcessorDirectoryW** (Unicode) and **GetPrintProcessorDirectoryA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="cb191-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb191-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb191-148">Drucken</span><span class="sxs-lookup"><span data-stu-id="cb191-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="cb191-149">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="cb191-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="cb191-150">**Addprintprocessor**</span><span class="sxs-lookup"><span data-stu-id="cb191-150">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> </dl>

 

 




