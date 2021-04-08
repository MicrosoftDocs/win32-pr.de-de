---
description: Die Funktion enumprintprozessoren listet die auf dem angegebenen Server installierten Druck Prozessoren auf.
ms.assetid: 98c9185c-c89d-4b4e-8c1e-7e22b315f188
title: Enumprintprocessor-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessors
- EnumPrintProcessorsA
- EnumPrintProcessorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0c446c39cdfc37ae7c578f5123afe57d61519704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960089"
---
# <a name="enumprintprocessors-function"></a><span data-ttu-id="086e5-103">Enumprintprozessoren-Funktion</span><span class="sxs-lookup"><span data-stu-id="086e5-103">EnumPrintProcessors function</span></span>

<span data-ttu-id="086e5-104">Die Funktion **enumprintprozessoren** listet die auf dem angegebenen Server installierten Druck Prozessoren auf.</span><span class="sxs-lookup"><span data-stu-id="086e5-104">The **EnumPrintProcessors** function enumerates the print processors installed on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="086e5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="086e5-105">Syntax</span></span>


```C++
BOOL EnumPrintProcessors(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="086e5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="086e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="086e5-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="086e5-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="086e5-108">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Servers angibt, auf dem sich die Druck Prozessoren befinden.</span><span class="sxs-lookup"><span data-stu-id="086e5-108">A pointer to a null-terminated string that specifies the name of the server on which the print processors reside.</span></span> <span data-ttu-id="086e5-109">Wenn dieser Parameter **null** ist, werden die lokalen Druck Prozessoren aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="086e5-109">If this parameter is **NULL**, the local print processors are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="086e5-110">nach-oben  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="086e5-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="086e5-111">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt (z. b. Windows x86, Windows ia64 oder Windows x64).</span><span class="sxs-lookup"><span data-stu-id="086e5-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="086e5-112">Wenn dieser Parameter **null** ist, wird die aktuelle Umgebung der aufrufenden Anwendung und des Client Computers (nicht der Zielanwendung und des Druck Servers) verwendet.</span><span class="sxs-lookup"><span data-stu-id="086e5-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="086e5-113">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="086e5-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="086e5-114">Der Typ der Informationen, die im *pprintprocessorinfo* -Puffer zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="086e5-114">The type of information returned in the *pPrintProcessorInfo* buffer.</span></span> <span data-ttu-id="086e5-115">Dieser Parameter muss 1 sein.</span><span class="sxs-lookup"><span data-stu-id="086e5-115">This parameter must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="086e5-116">*pprintprocessorinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="086e5-116">*pPrintProcessorInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="086e5-117">Ein Zeiger auf einen Puffer, der ein Array von [**PrintProcessor \_ Info \_ 1**](printprocessor-info-1.md) -Strukturen empfängt.</span><span class="sxs-lookup"><span data-stu-id="086e5-117">A pointer to a buffer that receives an array of [**PRINTPROCESSOR\_INFO\_1**](printprocessor-info-1.md) structures.</span></span> <span data-ttu-id="086e5-118">Jede Struktur beschreibt einen verfügbaren Druck Prozessor.</span><span class="sxs-lookup"><span data-stu-id="086e5-118">Each structure describes an available print processor.</span></span> <span data-ttu-id="086e5-119">Der Puffer muss groß genug sein, um das Array von Strukturen und Zeichen folgen zu erhalten, auf die die Strukturmember zeigen.</span><span class="sxs-lookup"><span data-stu-id="086e5-119">The buffer must be large enough to receive the array of structures and any strings to which the structure members point.</span></span>

<span data-ttu-id="086e5-120">Um die erforderliche Puffergröße zu ermitteln, muss **enumprintprocessor** aufgerufen werden, wobei *cbbuf* auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="086e5-120">To determine the required buffer size, call **EnumPrintProcessors** with *cbBuf* set to zero.</span></span> <span data-ttu-id="086e5-121">**Enumprintprocessor** schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen fehlerhaften \_ Puffer zurück \_ , und der *pcbrequired* -Parameter gibt die Größe (in Bytes) des Puffers zurück, der für das Array von Strukturen und deren Daten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="086e5-121">**EnumPrintProcessors** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="086e5-122">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="086e5-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="086e5-123">Die Größe (in Bytes) des Puffers, auf den *pprintprocessorinfo* zeigt.</span><span class="sxs-lookup"><span data-stu-id="086e5-123">The size, in bytes, of the buffer pointed to by *pPrintProcessorInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="086e5-124">*pcbbenötigte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="086e5-124">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="086e5-125">Ein Zeiger auf eine Variable, die die Anzahl von Bytes empfängt, die in den *pprintprocessorinfo* -Puffer kopiert werden, wenn die Funktion erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="086e5-125">A pointer to a variable that receives the number of bytes copied to the *pPrintProcessorInfo* buffer if the function succeeds.</span></span> <span data-ttu-id="086e5-126">Wenn der Puffer zu klein ist, schlägt die Funktion fehl, und die Variable erhält die erforderliche Anzahl von Bytes.</span><span class="sxs-lookup"><span data-stu-id="086e5-126">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="086e5-127">*pkreturned* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="086e5-127">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="086e5-128">Ein Zeiger auf eine Variable, die die Anzahl der im *pprintprocessorinfo* -Puffer zurückgegebenen Strukturen empfängt.</span><span class="sxs-lookup"><span data-stu-id="086e5-128">A pointer to a variable that receives the number of structures returned in the *pPrintProcessorInfo* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="086e5-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="086e5-129">Return value</span></span>

<span data-ttu-id="086e5-130">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="086e5-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="086e5-131">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="086e5-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="086e5-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="086e5-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="086e5-133">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="086e5-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="086e5-134">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="086e5-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="086e5-135">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="086e5-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="086e5-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="086e5-136">Requirements</span></span>



| <span data-ttu-id="086e5-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="086e5-137">Requirement</span></span> | <span data-ttu-id="086e5-138">Wert</span><span class="sxs-lookup"><span data-stu-id="086e5-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="086e5-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="086e5-139">Minimum supported client</span></span><br/> | <span data-ttu-id="086e5-140">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="086e5-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="086e5-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="086e5-141">Minimum supported server</span></span><br/> | <span data-ttu-id="086e5-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="086e5-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="086e5-143">Header</span><span class="sxs-lookup"><span data-stu-id="086e5-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="086e5-144"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="086e5-144"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="086e5-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="086e5-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="086e5-146"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="086e5-146"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="086e5-147">DLL</span><span class="sxs-lookup"><span data-stu-id="086e5-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="086e5-148"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="086e5-148"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="086e5-149">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="086e5-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="086e5-150">**Enumprintprocessorsw** (Unicode) und **enumprintprocessorsa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="086e5-150">**EnumPrintProcessorsW** (Unicode) and **EnumPrintProcessorsA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="086e5-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="086e5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="086e5-152">Drucken</span><span class="sxs-lookup"><span data-stu-id="086e5-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="086e5-153">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="086e5-153">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="086e5-154">**Addprintprocessor**</span><span class="sxs-lookup"><span data-stu-id="086e5-154">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> <dt>

[<span data-ttu-id="086e5-155">**Enumprintprocessordatatypes**</span><span class="sxs-lookup"><span data-stu-id="086e5-155">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> <dt>

[<span data-ttu-id="086e5-156">**PrintProcessor \_ Info \_ 1**</span><span class="sxs-lookup"><span data-stu-id="086e5-156">**PRINTPROCESSOR\_INFO\_1**</span></span>](printprocessor-info-1.md)
</dt> </dl>

 

