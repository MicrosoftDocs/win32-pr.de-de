---
description: Die enummonitors-Funktion Ruft Informationen zu den Port Monitoren ab, die auf dem angegebenen Server installiert sind.
ms.assetid: 4d4fbed2-193f-426c-8463-eeb6b1eaf316
title: Enummonitors-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMonitors
- EnumMonitorsA
- EnumMonitorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 1154cae0864b9d034ff356657d689cd3a768186f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756402"
---
# <a name="enummonitors-function"></a><span data-ttu-id="7bb9a-103">Enummonitors-Funktion</span><span class="sxs-lookup"><span data-stu-id="7bb9a-103">EnumMonitors function</span></span>

<span data-ttu-id="7bb9a-104">Die **enummonitors** -Funktion Ruft Informationen zu den Port Monitoren ab, die auf dem angegebenen Server installiert sind.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-104">The **EnumMonitors** function retrieves information about the port monitors installed on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bb9a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bb9a-105">Syntax</span></span>


```C++
BOOL EnumMonitors(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pMonitors,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="7bb9a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bb9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bb9a-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7bb9a-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bb9a-108">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Servers angibt, auf dem sich die Monitore befinden.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-108">A pointer to a null-terminated string that specifies the name of the server on which the monitors reside.</span></span> <span data-ttu-id="7bb9a-109">Wenn dieser Parameter **null** ist, werden die lokalen Monitore aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-109">If this parameter is **NULL**, the local monitors are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="7bb9a-110">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7bb9a-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bb9a-111">Die Version der Struktur, auf die von *pmonitors* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-111">The version of the structure pointed to by *pMonitors*.</span></span>

<span data-ttu-id="7bb9a-112">Dieser Wert kann 1 oder 2 sein.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-112">This value can be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="7bb9a-113">*pmonitors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7bb9a-113">*pMonitors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7bb9a-114">Ein Zeiger auf einen Puffer, der ein Array von-Strukturen empfängt.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-114">A pointer to a buffer that receives an array of structures.</span></span> <span data-ttu-id="7bb9a-115">Der Puffer muss groß genug sein, um die von den Strukturmembern referenzierten Zeichen folgen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-115">The buffer must be large enough to store the strings referenced by the structure members.</span></span>

<span data-ttu-id="7bb9a-116">Um die erforderliche Puffergröße zu ermitteln, müssen Sie **enummonitors** mit der Festlegung von *cbbuf* auf NULL aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-116">To determine the required buffer size, call **EnumMonitors** with *cbBuf* set to zero.</span></span> <span data-ttu-id="7bb9a-117">" **Enummonitors** " schlägt fehl, " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " gibt einen fehlerhaften \_ Puffer zurück \_ , und der *pcbrequired* -Parameter gibt die Größe (in Bytes) des Puffers zurück, der für das Array von Strukturen und deren Daten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-117">**EnumMonitors** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

<span data-ttu-id="7bb9a-118">Der Puffer erhält ein Array von [**Monitor \_ Info \_ 1**](monitor-info-1.md) -Strukturen, wenn die *Ebene* 1 ist, oder [**Monitor \_ Info \_ 2**](monitor-info-2.md) -Strukturen, wenn die *Ebene* 2 ist.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-118">The buffer receives an array of [**MONITOR\_INFO\_1**](monitor-info-1.md) structures if *Level* is 1, or [**MONITOR\_INFO\_2**](monitor-info-2.md) structures if *Level* is 2.</span></span>

</dd> <dt>

<span data-ttu-id="7bb9a-119">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7bb9a-119">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bb9a-120">Die Größe (in Bytes) des Puffers, auf den *pmonitors* zeigt.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-120">The size, in bytes, of the buffer pointed to by *pMonitors*.</span></span>

</dd> <dt>

<span data-ttu-id="7bb9a-121">*pcbbenötigte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7bb9a-121">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7bb9a-122">Ein Zeiger auf eine Variable, die die Anzahl der kopierten Bytes empfängt, wenn die Funktion erfolgreich ausgeführt wird, oder die Anzahl der Bytes, die erforderlich sind, wenn *cbbuf* zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-122">A pointer to a variable that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> <dt>

<span data-ttu-id="7bb9a-123">*pkreturned* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7bb9a-123">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7bb9a-124">Ein Zeiger auf eine Variable, die die Anzahl der Strukturen erhält, die im Puffer zurückgegeben wurden, auf den *pmonitors* zeigt.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-124">A pointer to a variable that receives the number of structures that were returned in the buffer pointed to by *pMonitors*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bb9a-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7bb9a-125">Return value</span></span>

<span data-ttu-id="7bb9a-126">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="7bb9a-126">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="7bb9a-127">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-127">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bb9a-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7bb9a-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7bb9a-129">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-129">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="7bb9a-130">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-130">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="7bb9a-131">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="7bb9a-131">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7bb9a-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bb9a-132">Requirements</span></span>



| <span data-ttu-id="7bb9a-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7bb9a-133">Requirement</span></span> | <span data-ttu-id="7bb9a-134">Wert</span><span class="sxs-lookup"><span data-stu-id="7bb9a-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bb9a-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7bb9a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7bb9a-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7bb9a-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7bb9a-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7bb9a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7bb9a-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7bb9a-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7bb9a-139">Header</span><span class="sxs-lookup"><span data-stu-id="7bb9a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bb9a-140"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7bb9a-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7bb9a-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7bb9a-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="7bb9a-142"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7bb9a-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="7bb9a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="7bb9a-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bb9a-144"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="7bb9a-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="7bb9a-145">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="7bb9a-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7bb9a-146">**Enummonitorsw** (Unicode) und **enummonitorsa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7bb9a-146">**EnumMonitorsW** (Unicode) and **EnumMonitorsA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="7bb9a-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bb9a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bb9a-148">Drucken</span><span class="sxs-lookup"><span data-stu-id="7bb9a-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7bb9a-149">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="7bb9a-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="7bb9a-150">**Überwachen von \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="7bb9a-150">**MONITOR\_INFO\_1**</span></span>](monitor-info-1.md)
</dt> <dt>

[<span data-ttu-id="7bb9a-151">**Überwachen von \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="7bb9a-151">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

