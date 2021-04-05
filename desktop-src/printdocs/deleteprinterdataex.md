---
description: Die deleteprinterdataex-Funktion löscht einen angegebenen Wert aus den Konfigurationsdaten für einen Drucker.
ms.assetid: bcc9cdb3-0fbf-40b6-9de2-1479c3c0ff55
title: Deleteprinterdataex-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDataEx
- DeletePrinterDataExA
- DeletePrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 07cf6262db0a1e3a3c4c098ee26e03b3fdad4002
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757387"
---
# <a name="deleteprinterdataex-function"></a><span data-ttu-id="e76ea-103">Deleteprinterdataex-Funktion</span><span class="sxs-lookup"><span data-stu-id="e76ea-103">DeletePrinterDataEx function</span></span>

<span data-ttu-id="e76ea-104">Die **deleteprinterdataex** -Funktion löscht einen angegebenen Wert aus den Konfigurationsdaten für einen Drucker.</span><span class="sxs-lookup"><span data-stu-id="e76ea-104">The **DeletePrinterDataEx** function deletes a specified value from the configuration data for a printer.</span></span> <span data-ttu-id="e76ea-105">Die Konfigurationsdaten eines Druckers bestehen aus einem Satz benannter und typisierter Werte, die in einer Hierarchie von Registrierungs Schlüsseln gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="e76ea-105">A printer's configuration data consists of a set of named and typed values stored in a hierarchy of registry keys.</span></span> <span data-ttu-id="e76ea-106">Die-Funktion löscht einen angegebenen Wert unter einem angegebenen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="e76ea-106">The function deletes a specified value under a specified key.</span></span>

<span data-ttu-id="e76ea-107">Wie die [**deleteprinterdata**](deleteprinterdata.md) -Funktion kann **deleteprinterdataex** Werte löschen, die von der [**setprinterdata**](setprinterdata.md) -Funktion gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e76ea-107">Like the [**DeletePrinterData**](deleteprinterdata.md) function, **DeletePrinterDataEx** can delete values stored by the [**SetPrinterData**](setprinterdata.md) function.</span></span> <span data-ttu-id="e76ea-108">Außerdem kann **deleteprinterdataex** Werte löschen, die unter einem angegebenen Schlüssel von der [**setprinterdataex**](setprinterdataex.md) -Funktion gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="e76ea-108">In addition, **DeletePrinterDataEx** can delete values stored under a specified key by the [**SetPrinterDataEx**](setprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e76ea-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e76ea-109">Syntax</span></span>


```C++
DWORD DeletePrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName
);
```



## <a name="parameters"></a><span data-ttu-id="e76ea-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e76ea-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e76ea-111">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e76ea-111">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e76ea-112">Ein Handle für den Drucker, für den die Funktion einen Wert löscht.</span><span class="sxs-lookup"><span data-stu-id="e76ea-112">A handle to the printer for which the function deletes a value.</span></span> <span data-ttu-id="e76ea-113">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="e76ea-113">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="e76ea-114">*pkeyname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e76ea-114">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e76ea-115">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Schlüssel mit dem zu löschenden Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="e76ea-115">A pointer to a null-terminated string that specifies the key containing the value to delete.</span></span> <span data-ttu-id="e76ea-116">Verwenden Sie den umgekehrten Schrägstrich ( \\ ) als Trennzeichen, um einen Pfad anzugeben, der über mindestens einen Unterschlüssel verfügt.</span><span class="sxs-lookup"><span data-stu-id="e76ea-116">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="e76ea-117">Wenn *pkeyname* **null** oder eine leere Zeichenfolge ist, gibt **deleteprinterdataex** einen \_ ungültigen \_ Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="e76ea-117">If *pKeyName* is **NULL** or an empty string, **DeletePrinterDataEx** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="e76ea-118">*pvaluename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e76ea-118">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e76ea-119">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des zu löschenden Werts angibt.</span><span class="sxs-lookup"><span data-stu-id="e76ea-119">A pointer to a null-terminated string that specifies the name of the value to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e76ea-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e76ea-120">Return value</span></span>

<span data-ttu-id="e76ea-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e76ea-121">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="e76ea-122">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Systemfehler Code.</span><span class="sxs-lookup"><span data-stu-id="e76ea-122">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e76ea-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e76ea-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e76ea-124">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e76ea-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e76ea-125">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="e76ea-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e76ea-126">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="e76ea-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e76ea-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e76ea-127">Requirements</span></span>



| <span data-ttu-id="e76ea-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e76ea-128">Requirement</span></span> | <span data-ttu-id="e76ea-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e76ea-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e76ea-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e76ea-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e76ea-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e76ea-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e76ea-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e76ea-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e76ea-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e76ea-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e76ea-134">Header</span><span class="sxs-lookup"><span data-stu-id="e76ea-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e76ea-135"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e76ea-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e76ea-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e76ea-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="e76ea-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e76ea-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e76ea-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e76ea-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e76ea-139"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="e76ea-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e76ea-140">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="e76ea-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e76ea-141">**Deleteprinterdataexw** (Unicode) und **deleteprinterdataexa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e76ea-141">**DeletePrinterDataExW** (Unicode) and **DeletePrinterDataExA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="e76ea-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e76ea-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e76ea-143">Drucken</span><span class="sxs-lookup"><span data-stu-id="e76ea-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e76ea-144">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e76ea-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e76ea-145">**Deleteprinterkey**</span><span class="sxs-lookup"><span data-stu-id="e76ea-145">**DeletePrinterKey**</span></span>](deleteprinterkey.md)
</dt> <dt>

[<span data-ttu-id="e76ea-146">**Enumprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="e76ea-146">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="e76ea-147">**Enumprinterkey**</span><span class="sxs-lookup"><span data-stu-id="e76ea-147">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="e76ea-148">**Getprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="e76ea-148">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="e76ea-149">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="e76ea-149">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="e76ea-150">**Setprinterdataex**</span><span class="sxs-lookup"><span data-stu-id="e76ea-150">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




