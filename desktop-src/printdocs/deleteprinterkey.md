---
description: Die deleteprinterkey-Funktion löscht einen angegebenen Schlüssel und alle zugehörigen Unterschlüssel für einen angegebenen Drucker.
ms.assetid: 0bd81b43-5c1e-4989-8350-2ec0dc215f28
title: Deleteprinterkey-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterKey
- DeletePrinterKeyA
- DeletePrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 4be073f7832f647e156dbd3b5e12d23ffe6acc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757747"
---
# <a name="deleteprinterkey-function"></a><span data-ttu-id="f4494-103">Deleteprinterkey-Funktion</span><span class="sxs-lookup"><span data-stu-id="f4494-103">DeletePrinterKey function</span></span>

<span data-ttu-id="f4494-104">Die **deleteprinterkey** -Funktion löscht einen angegebenen Schlüssel und alle zugehörigen Unterschlüssel für einen angegebenen Drucker.</span><span class="sxs-lookup"><span data-stu-id="f4494-104">The **DeletePrinterKey** function deletes a specified key and all its subkeys for a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4494-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4494-105">Syntax</span></span>


```C++
DWORD DeletePrinterKey(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName
);
```



## <a name="parameters"></a><span data-ttu-id="f4494-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4494-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4494-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4494-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4494-108">Ein Handle für den Drucker, für den die Funktion einen Schlüssel löscht.</span><span class="sxs-lookup"><span data-stu-id="f4494-108">A handle to the printer for which the function deletes a key.</span></span> <span data-ttu-id="f4494-109">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="f4494-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="f4494-110">*pkeyname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4494-110">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4494-111">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den zu löschenden Schlüssel angibt.</span><span class="sxs-lookup"><span data-stu-id="f4494-111">A pointer to a null-terminated string that specifies the key to delete.</span></span> <span data-ttu-id="f4494-112">Verwenden Sie den umgekehrten Schrägstrich ( \\ ) als Trennzeichen, um einen Pfad mit einem oder mehreren unter Schlüsseln anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f4494-112">Use the backslash ( \\ ) character as a delimiter to specify a path with one or more subkeys.</span></span>

<span data-ttu-id="f4494-113">Wenn *pkeyname* eine leere Zeichenfolge ("") ist, löscht **deleteprinterkey** alle Schlüssel unter dem Schlüssel der obersten Ebene für den Drucker.</span><span class="sxs-lookup"><span data-stu-id="f4494-113">If *pKeyName* is an empty string (""), **DeletePrinterKey** deletes all keys below the top-level key for the printer.</span></span> <span data-ttu-id="f4494-114">Wenn *pkeyname* **null** ist, gibt **deleteprinterkey** einen \_ ungültigen \_ Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="f4494-114">If *pKeyName* is **NULL**, **DeletePrinterKey** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4494-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4494-115">Return value</span></span>

<span data-ttu-id="f4494-116">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f4494-116">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="f4494-117">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Systemfehler Code.</span><span class="sxs-lookup"><span data-stu-id="f4494-117">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4494-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4494-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f4494-119">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f4494-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f4494-120">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="f4494-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f4494-121">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="f4494-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f4494-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4494-122">Requirements</span></span>



| <span data-ttu-id="f4494-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4494-123">Requirement</span></span> | <span data-ttu-id="f4494-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f4494-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4494-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4494-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f4494-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4494-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f4494-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4494-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f4494-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4494-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f4494-129">Header</span><span class="sxs-lookup"><span data-stu-id="f4494-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4494-130"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4494-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f4494-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f4494-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="f4494-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4494-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f4494-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f4494-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4494-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="f4494-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="f4494-135">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="f4494-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f4494-136">**Deleteprinterkeyw** (Unicode) und **deleteprinterkeya** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f4494-136">**DeletePrinterKeyW** (Unicode) and **DeletePrinterKeyA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="f4494-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4494-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4494-138">Drucken</span><span class="sxs-lookup"><span data-stu-id="f4494-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f4494-139">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="f4494-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f4494-140">**Deleteprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="f4494-140">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="f4494-141">**Enumprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="f4494-141">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="f4494-142">**Enumprinterkey**</span><span class="sxs-lookup"><span data-stu-id="f4494-142">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="f4494-143">**Getprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="f4494-143">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="f4494-144">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="f4494-144">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="f4494-145">**Setprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="f4494-145">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




