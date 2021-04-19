---
description: Die GetDefaultPrinter-Funktion Ruft den Drucker Namen des Standard Druckers für den aktuellen Benutzer auf dem lokalen Computer ab.
ms.assetid: 8ec06743-43ce-4fac-83c4-f09eac7ee333
title: GetDefaultPrinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDefaultPrinter
- GetDefaultPrinterA
- GetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8db5b2aef859ea5d8247fc203611af74c8daddd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348599"
---
# <a name="getdefaultprinter-function"></a><span data-ttu-id="3a40c-103">GetDefaultPrinter-Funktion</span><span class="sxs-lookup"><span data-stu-id="3a40c-103">GetDefaultPrinter function</span></span>

<span data-ttu-id="3a40c-104">Die **GetDefaultPrinter** -Funktion Ruft den Drucker Namen des Standard Druckers für den aktuellen Benutzer auf dem lokalen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="3a40c-104">The **GetDefaultPrinter** function retrieves the printer name of the default printer for the current user on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a40c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a40c-105">Syntax</span></span>


```C++
BOOL GetDefaultPrinter(
  _In_    LPTSTR  pszBuffer,
  _Inout_ LPDWORD pcchBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="3a40c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a40c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a40c-107">*pszbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a40c-107">*pszBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a40c-108">Ein Zeiger auf einen Puffer, der eine NULL-terminierte Zeichenfolge mit dem Standarddrucker Namen empfängt.</span><span class="sxs-lookup"><span data-stu-id="3a40c-108">A pointer to a buffer that receives a null-terminated character string containing the default printer name.</span></span> <span data-ttu-id="3a40c-109">Wenn dieser Parameter **null** ist, schlägt die Funktion fehl, und die Variable, auf die von *pcchBuffer* verwiesen wird, gibt die erforderliche Puffergröße in Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="3a40c-109">If this parameter is **NULL**, the function fails and the variable pointed to by *pcchBuffer* returns the required buffer size, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="3a40c-110">*pcchBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3a40c-110">*pcchBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a40c-111">Gibt bei der Eingabe die Größe des *pszbuffer* -Puffers in Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="3a40c-111">On input, specifies the size, in characters, of the *pszBuffer* buffer.</span></span> <span data-ttu-id="3a40c-112">Bei der Ausgabe empfängt die Größe der Drucker Namen Zeichenfolge in Zeichen, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="3a40c-112">On output, receives the size, in characters, of the printer name string, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a40c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a40c-113">Return value</span></span>

<span data-ttu-id="3a40c-114">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich NULL, und die Variable, auf die von *pcchBuffer* verwiesen wird, enthält die Anzahl der Zeichen, die in den *pszbuffer* -Puffer kopiert werden, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="3a40c-114">If the function succeeds, the return value is a nonzero value and the variable pointed to by *pcchBuffer* contains the number of characters copied to the *pszBuffer* buffer, including the terminating null character.</span></span>

<span data-ttu-id="3a40c-115">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="3a40c-115">If the function fails, the return value is zero.</span></span>



| <span data-ttu-id="3a40c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3a40c-116">Value</span></span>                       | <span data-ttu-id="3a40c-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3a40c-117">Meaning</span></span>                                                                                                                        |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a40c-118">Fehler \_ beim \_ Puffer.</span><span class="sxs-lookup"><span data-stu-id="3a40c-118">ERROR\_INSUFFICIENT\_BUFFER</span></span> | <span data-ttu-id="3a40c-119">Der *pszbuffer* -Puffer ist zu klein.</span><span class="sxs-lookup"><span data-stu-id="3a40c-119">The *pszBuffer* buffer is too small.</span></span> <span data-ttu-id="3a40c-120">Die Variable, auf die von *pcchBuffer* verwiesen wird, enthält die erforderliche Puffergröße in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3a40c-120">The variable pointed to by *pcchBuffer* contains the required buffer size, in characters.</span></span> |
| <span data-ttu-id="3a40c-121">Fehler \_ Datei \_ nicht \_ gefunden.</span><span class="sxs-lookup"><span data-stu-id="3a40c-121">ERROR\_FILE\_NOT\_FOUND</span></span>     | <span data-ttu-id="3a40c-122">Es ist kein Standarddrucker vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3a40c-122">There is no default printer.</span></span>                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="3a40c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a40c-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3a40c-124">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a40c-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="3a40c-125">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="3a40c-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="3a40c-126">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="3a40c-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3a40c-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a40c-127">Requirements</span></span>



| <span data-ttu-id="3a40c-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a40c-128">Requirement</span></span> | <span data-ttu-id="3a40c-129">Wert</span><span class="sxs-lookup"><span data-stu-id="3a40c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a40c-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a40c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3a40c-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a40c-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3a40c-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a40c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3a40c-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a40c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3a40c-134">Header</span><span class="sxs-lookup"><span data-stu-id="3a40c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a40c-135"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a40c-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3a40c-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3a40c-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="3a40c-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a40c-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="3a40c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3a40c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a40c-139"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="3a40c-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="3a40c-140">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="3a40c-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3a40c-141">**Getdefaultprinterw** (Unicode) und **getdefaultprintera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3a40c-141">**GetDefaultPrinterW** (Unicode) and **GetDefaultPrinterA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="3a40c-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a40c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a40c-143">Drucken</span><span class="sxs-lookup"><span data-stu-id="3a40c-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3a40c-144">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="3a40c-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="3a40c-145">**Methode SetDefaultPrinter auf**</span><span class="sxs-lookup"><span data-stu-id="3a40c-145">**SetDefaultPrinter**</span></span>](setdefaultprinter.md)
</dt> </dl>

 

 




