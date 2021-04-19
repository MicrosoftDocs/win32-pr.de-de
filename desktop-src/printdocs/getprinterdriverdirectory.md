---
description: Die getprinterdriverdirectory-Funktion Ruft den Pfad des druckertreiberverzeichnisses ab.
ms.assetid: 69c9cc87-d7e3-496a-b631-b3ae30cdb3fd
title: Getprinterdriverdirectory-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverDirectory
- GetPrinterDriverDirectoryA
- GetPrinterDriverDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 7acc68f99f9791ba4231bcfea2b1788cfb37011c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362712"
---
# <a name="getprinterdriverdirectory-function"></a><span data-ttu-id="9fad6-103">Getprinterdriverdirectory-Funktion</span><span class="sxs-lookup"><span data-stu-id="9fad6-103">GetPrinterDriverDirectory function</span></span>

<span data-ttu-id="9fad6-104">Die **getprinterdriverdirectory** -Funktion Ruft den Pfad des druckertreiberverzeichnisses ab.</span><span class="sxs-lookup"><span data-stu-id="9fad6-104">The **GetPrinterDriverDirectory** function retrieves the path of the printer-driver directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fad6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fad6-105">Syntax</span></span>


```C++
BOOL GetPrinterDriverDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverDirectory,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="9fad6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fad6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fad6-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fad6-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fad6-108">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Servers angibt, auf dem sich der Druckertreiber befindet.</span><span class="sxs-lookup"><span data-stu-id="9fad6-108">A pointer to a null-terminated string that specifies the name of the server on which the printer driver resides.</span></span> <span data-ttu-id="9fad6-109">Wenn dieser Parameter **null** ist, wird der Pfad des lokalen Treiber Verzeichnisses abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9fad6-109">If this parameter is **NULL**, the local driver-directory path is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="9fad6-110">nach-oben  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fad6-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fad6-111">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt (z. b. Windows x86, Windows ia64 oder Windows x64).</span><span class="sxs-lookup"><span data-stu-id="9fad6-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="9fad6-112">Wenn dieser Parameter **null** ist, wird die aktuelle Umgebung der aufrufenden Anwendung und des Client Computers (nicht der Zielanwendung und des Druck Servers) verwendet.</span><span class="sxs-lookup"><span data-stu-id="9fad6-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="9fad6-113">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fad6-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fad6-114">Die Struktur Ebene.</span><span class="sxs-lookup"><span data-stu-id="9fad6-114">The structure level.</span></span> <span data-ttu-id="9fad6-115">Dieser Wert muss 1 sein.</span><span class="sxs-lookup"><span data-stu-id="9fad6-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="9fad6-116">*pdriverdirectory* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9fad6-116">*pDriverDirectory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fad6-117">Ein Zeiger auf einen Puffer, der den Pfad empfängt.</span><span class="sxs-lookup"><span data-stu-id="9fad6-117">A pointer to a buffer that receives the path.</span></span>

</dd> <dt>

<span data-ttu-id="9fad6-118">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fad6-118">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fad6-119">Die Größe des Puffers, auf den *pdriverdirectory* verweist.</span><span class="sxs-lookup"><span data-stu-id="9fad6-119">The size of the buffer to which *pDriverDirectory* points.</span></span>

</dd> <dt>

<span data-ttu-id="9fad6-120">*pcbbenötigte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9fad6-120">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fad6-121">Ein Zeiger auf einen-Wert, der die Anzahl der Bytes angibt, die beim Erfolg der Funktion kopiert werden, oder die Anzahl der Bytes, die erforderlich sind, wenn *cbbuf* zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="9fad6-121">A pointer to a value that specifies the number of bytes copied if the function succeeds, or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fad6-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9fad6-122">Return value</span></span>

<span data-ttu-id="9fad6-123">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9fad6-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="9fad6-124">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="9fad6-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fad6-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fad6-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9fad6-126">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9fad6-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9fad6-127">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="9fad6-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9fad6-128">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="9fad6-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9fad6-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fad6-129">Requirements</span></span>



| <span data-ttu-id="9fad6-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9fad6-130">Requirement</span></span> | <span data-ttu-id="9fad6-131">Wert</span><span class="sxs-lookup"><span data-stu-id="9fad6-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fad6-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9fad6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9fad6-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fad6-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9fad6-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9fad6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9fad6-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fad6-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9fad6-136">Header</span><span class="sxs-lookup"><span data-stu-id="9fad6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fad6-137"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9fad6-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9fad6-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9fad6-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="9fad6-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fad6-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9fad6-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9fad6-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fad6-141"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="9fad6-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="9fad6-142">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="9fad6-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9fad6-143">**Getprinterdriverdirectoren** (Unicode) und **getprinterdriverdirector ya** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9fad6-143">**GetPrinterDriverDirectoryW** (Unicode) and **GetPrinterDriverDirectoryA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="9fad6-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fad6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fad6-145">Drucken</span><span class="sxs-lookup"><span data-stu-id="9fad6-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9fad6-146">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9fad6-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9fad6-147">**Addprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="9fad6-147">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> </dl>

 

 




