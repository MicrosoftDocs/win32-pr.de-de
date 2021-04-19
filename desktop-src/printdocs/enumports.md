---
description: Die enumports-Funktion Listet die Ports auf, die für den Druck auf einem angegebenen Server verfügbar sind.
ms.assetid: 72ea0e35-bf26-4c12-9451-8f6941990d82
title: Enumports-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPorts
- EnumPortsA
- EnumPortsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 2f4cceb6b6915f92139d8919b74f62ba4392381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356293"
---
# <a name="enumports-function"></a><span data-ttu-id="2d5bd-103">Enumports-Funktion</span><span class="sxs-lookup"><span data-stu-id="2d5bd-103">EnumPorts function</span></span>

<span data-ttu-id="2d5bd-104">Die **enumports** -Funktion Listet die Ports auf, die für den Druck auf einem angegebenen Server verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-104">The **EnumPorts** function enumerates the ports that are available for printing on a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d5bd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d5bd-105">Syntax</span></span>


```C++
BOOL EnumPorts(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPorts,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="2d5bd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d5bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d5bd-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d5bd-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d5bd-108">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Servers angibt, dessen Druckerports Sie auflisten möchten.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-108">A pointer to a null-terminated string that specifies the name of the server whose printer ports you want to enumerate.</span></span>

<span data-ttu-id="2d5bd-109">Wenn *PName* den Wert **null** hat, listet die Funktion die Drucker Anschlüsse des lokalen Computers auf.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-109">If *pName* is **NULL**, the function enumerates the local machine's printer ports.</span></span>

</dd> <dt>

<span data-ttu-id="2d5bd-110">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d5bd-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d5bd-111">Der Typ der Informationen, die im *pports* -Puffer zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-111">The type of information returned in the *pPorts* buffer.</span></span> <span data-ttu-id="2d5bd-112">Wenn *Level* gleich 1 ist, empfängt *pports* ein Array von [**Port \_ Info \_ 1**](port-info-1.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-112">If *Level* is 1, *pPorts* receives an array of [**PORT\_INFO\_1**](port-info-1.md) structures.</span></span> <span data-ttu-id="2d5bd-113">Wenn *Level* gleich 2 ist, empfängt *pports* ein Array von [**Port \_ Info \_ 2**](port-info-2.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-113">If *Level* is 2, *pPorts* receives an array of [**PORT\_INFO\_2**](port-info-2.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="2d5bd-114">*pports* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2d5bd-114">*pPorts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d5bd-115">Ein Zeiger auf einen Puffer, der ein Array von [**Port \_ Info \_ 1**](port-info-1.md) -oder [**Port \_ Info \_ 2**](port-info-2.md) -Strukturen empfängt.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-115">A pointer to a buffer that receives an array of [**PORT\_INFO\_1**](port-info-1.md) or [**PORT\_INFO\_2**](port-info-2.md) structures.</span></span> <span data-ttu-id="2d5bd-116">Jede Struktur enthält Daten, die einen verfügbaren Druckerport beschreiben.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-116">Each structure contains data that describes an available printer port.</span></span> <span data-ttu-id="2d5bd-117">Der Puffer muss groß genug sein, um die Zeichen folgen zu speichern, auf die von den Strukturmembern verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-117">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="2d5bd-118">Um die erforderliche Puffergröße zu ermitteln, nennen Sie **enumports** , bei denen *cbbuf* auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-118">To determine the required buffer size, call **EnumPorts** with *cbBuf* set to zero.</span></span> <span data-ttu-id="2d5bd-119">**Enumports** schlagen fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt fehlerhaften \_ Puffer zurück \_ , und der *pcbrequired* -Parameter gibt die Größe (in Bytes) des Puffers zurück, der für das Array von Strukturen und deren Daten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-119">**EnumPorts** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="2d5bd-120">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d5bd-120">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d5bd-121">Die Größe (in Bytes) des Puffers, auf den *pports* zeigt.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-121">The size, in bytes, of the buffer pointed to by *pPorts*.</span></span>

</dd> <dt>

<span data-ttu-id="2d5bd-122">*pcbbenötigte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2d5bd-122">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d5bd-123">Ein Zeiger auf eine Variable, die die Anzahl von Bytes empfängt, die in den *pports* -Puffer kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-123">A pointer to a variable that receives the number of bytes copied to the *pPorts* buffer.</span></span> <span data-ttu-id="2d5bd-124">Wenn der Puffer zu klein ist, schlägt die Funktion fehl, und die Variable erhält die erforderliche Anzahl von Bytes.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-124">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="2d5bd-125">*pkreturned* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2d5bd-125">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d5bd-126">Ein Zeiger auf eine Variable, die die Anzahl von [**Port \_ Info \_ 1**](port-info-1.md) -oder [**Port \_ Info \_ 2**](port-info-2.md) -Strukturen empfängt, die im *pports* -Puffer zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-126">A pointer to a variable that receives the number of [**PORT\_INFO\_1**](port-info-1.md) or [**PORT\_INFO\_2**](port-info-2.md) structures returned in the *pPorts* buffer.</span></span> <span data-ttu-id="2d5bd-127">Dies ist die Anzahl der Drucker Anschlüsse, die auf dem angegebenen Server verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-127">This is the number of printer ports that are available on the specified server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d5bd-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d5bd-128">Return value</span></span>

<span data-ttu-id="2d5bd-129">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2d5bd-129">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="2d5bd-130">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-130">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d5bd-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d5bd-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2d5bd-132">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-132">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="2d5bd-133">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-133">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="2d5bd-134">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-134">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="2d5bd-135">Die **enumports** -Funktion kann auch dann erfolgreich ausgeführt werden, wenn der durch *PName* angegebene Server keinen Drucker definiert hat.</span><span class="sxs-lookup"><span data-stu-id="2d5bd-135">The **EnumPorts** function can succeed even if the server specified by *pName* does not have a printer defined.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d5bd-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d5bd-136">Requirements</span></span>



| <span data-ttu-id="2d5bd-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d5bd-137">Requirement</span></span> | <span data-ttu-id="2d5bd-138">Wert</span><span class="sxs-lookup"><span data-stu-id="2d5bd-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d5bd-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d5bd-139">Minimum supported client</span></span><br/> | <span data-ttu-id="2d5bd-140">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d5bd-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2d5bd-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d5bd-141">Minimum supported server</span></span><br/> | <span data-ttu-id="2d5bd-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d5bd-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2d5bd-143">Header</span><span class="sxs-lookup"><span data-stu-id="2d5bd-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d5bd-144"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d5bd-144"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2d5bd-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2d5bd-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="2d5bd-146"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d5bd-146"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="2d5bd-147">DLL</span><span class="sxs-lookup"><span data-stu-id="2d5bd-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d5bd-148"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="2d5bd-148"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="2d5bd-149">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="2d5bd-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2d5bd-150">**Enumportsw** (Unicode) und **enumportsa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2d5bd-150">**EnumPortsW** (Unicode) and **EnumPortsA** (ANSI)</span></span><br/>                                             |



## <a name="see-also"></a><span data-ttu-id="2d5bd-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d5bd-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d5bd-152">Drucken</span><span class="sxs-lookup"><span data-stu-id="2d5bd-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2d5bd-153">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="2d5bd-153">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="2d5bd-154">**AddPort**</span><span class="sxs-lookup"><span data-stu-id="2d5bd-154">**AddPort**</span></span>](addport.md)
</dt> <dt>

[<span data-ttu-id="2d5bd-155">**DeletePort**</span><span class="sxs-lookup"><span data-stu-id="2d5bd-155">**DeletePort**</span></span>](deleteport.md)
</dt> <dt>

[<span data-ttu-id="2d5bd-156">**Port \_ Info \_ 1**</span><span class="sxs-lookup"><span data-stu-id="2d5bd-156">**PORT\_INFO\_1**</span></span>](port-info-1.md)
</dt> <dt>

[<span data-ttu-id="2d5bd-157">**Port \_ Info \_ 2**</span><span class="sxs-lookup"><span data-stu-id="2d5bd-157">**PORT\_INFO\_2**</span></span>](port-info-2.md)
</dt> </dl>

 

