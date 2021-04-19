---
description: Die resetprinter-Funktion gibt die Werte für Datentyp und Geräte Modus an, die zum Drucken von Dokumenten verwendet werden, die von der StartDocPrinter-Funktion gesendet werden. Diese Werte können überschrieben werden, indem die Funktion setjob verwendet wird, nachdem der Druck von Dokumenten begonnen wurde.
ms.assetid: 9efc6629-dbb7-4320-90b9-07c66f0add47
title: Resetprinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResetPrinter
- ResetPrinterA
- ResetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8bdfef0229a646e802878a96370d27d49a6bfc2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362497"
---
# <a name="resetprinter-function"></a><span data-ttu-id="9d45f-104">Resetprinter-Funktion</span><span class="sxs-lookup"><span data-stu-id="9d45f-104">ResetPrinter function</span></span>

<span data-ttu-id="9d45f-105">Die **resetprinter** -Funktion gibt die Werte für Datentyp und Geräte Modus an, die zum Drucken von Dokumenten verwendet werden, die von der [**StartDocPrinter**](startdocprinter.md) -Funktion gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d45f-105">The **ResetPrinter** function specifies the data type and device mode values to be used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="9d45f-106">Diese Werte können überschrieben werden, indem die Funktion [**setjob**](setjob.md) verwendet wird, nachdem der Druck von Dokumenten begonnen wurde.</span><span class="sxs-lookup"><span data-stu-id="9d45f-106">These values can be overridden by using the [**SetJob**](setjob.md) function after document printing has started.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d45f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d45f-107">Syntax</span></span>


```C++
BOOL ResetPrinter(
  _In_ HANDLE             hPrinter,
  _In_ LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a><span data-ttu-id="9d45f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d45f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d45f-109">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d45f-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d45f-110">Handle für den Drucker.</span><span class="sxs-lookup"><span data-stu-id="9d45f-110">Handle to the printer.</span></span> <span data-ttu-id="9d45f-111">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="9d45f-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="9d45f-112">*pdefault* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d45f-112">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d45f-113">Zeiger auf eine [**Drucker \_ Standard**](printer-defaults.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="9d45f-113">Pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span>

<span data-ttu-id="9d45f-114">Die **resetprinter** -Funktion ignoriert den **desiredAccess** -Member der [**Drucker \_ Standard**](printer-defaults.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="9d45f-114">The **ResetPrinter** function ignores the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="9d45f-115">Legen Sie diesen Member auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="9d45f-115">Set that member to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d45f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d45f-116">Return value</span></span>

<span data-ttu-id="9d45f-117">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9d45f-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="9d45f-118">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="9d45f-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d45f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d45f-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9d45f-120">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9d45f-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9d45f-121">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="9d45f-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9d45f-122">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="9d45f-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9d45f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d45f-123">Requirements</span></span>



| <span data-ttu-id="9d45f-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d45f-124">Requirement</span></span> | <span data-ttu-id="9d45f-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9d45f-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d45f-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d45f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9d45f-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d45f-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9d45f-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d45f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9d45f-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d45f-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9d45f-130">Header</span><span class="sxs-lookup"><span data-stu-id="9d45f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d45f-131"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d45f-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9d45f-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9d45f-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="9d45f-133"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d45f-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9d45f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9d45f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d45f-135"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="9d45f-135"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="9d45f-136">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="9d45f-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9d45f-137">**Resetprinterw** (Unicode) und **resetprintera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9d45f-137">**ResetPrinterW** (Unicode) and **ResetPrinterA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="9d45f-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d45f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d45f-139">Drucken</span><span class="sxs-lookup"><span data-stu-id="9d45f-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9d45f-140">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9d45f-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9d45f-141">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="9d45f-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="9d45f-142">**Drucker \_ Standardwerte**</span><span class="sxs-lookup"><span data-stu-id="9d45f-142">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="9d45f-143">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="9d45f-143">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="9d45f-144">**Setjob**</span><span class="sxs-lookup"><span data-stu-id="9d45f-144">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

 




