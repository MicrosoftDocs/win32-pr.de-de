---
description: Die deleteprinterdata-Funktion löscht die angegebenen Konfigurationsdaten für einen Drucker. Ein Drucker Konfigurationsdaten besteht aus einem Satz benannter und typisierter Werte. Die deleteprinterdata-Funktion löscht einen dieser Werte, der durch den Wert Namen angegeben wird.
ms.assetid: 03c0bd75-d6de-46e3-b8e9-5a55df5135ea
title: Deleteprinterdata-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterData
- DeletePrinterDataA
- DeletePrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a88df8484d367ae2cc50f4a465b5db1dcd53c355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345309"
---
# <a name="deleteprinterdata-function"></a><span data-ttu-id="19907-105">Deleteprinterdata-Funktion</span><span class="sxs-lookup"><span data-stu-id="19907-105">DeletePrinterData function</span></span>

<span data-ttu-id="19907-106">Die **deleteprinterdata** -Funktion löscht die angegebenen Konfigurationsdaten für einen Drucker.</span><span class="sxs-lookup"><span data-stu-id="19907-106">The **DeletePrinterData** function deletes specified configuration data for a printer.</span></span> <span data-ttu-id="19907-107">Die Konfigurationsdaten eines Druckers bestehen aus einem Satz von benannten und typisierten Werten.</span><span class="sxs-lookup"><span data-stu-id="19907-107">A printer's configuration data consists of a set of named and typed values.</span></span> <span data-ttu-id="19907-108">Die **deleteprinterdata** -Funktion löscht einen dieser Werte, der durch den Wert Namen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="19907-108">The **DeletePrinterData** function deletes one of these values, specified by its value name.</span></span>

<span data-ttu-id="19907-109">Das Aufrufen von **deleteprinterdata** entspricht dem Aufrufen der [**deleteprinterdataex**](deleteprinterdataex.md) -Funktion, wobei der *pkeyname* -Parameter auf "printerdriverdata" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="19907-109">Calling **DeletePrinterData** is equivalent to calling the [**DeletePrinterDataEx**](deleteprinterdataex.md) function with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="19907-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="19907-110">Syntax</span></span>


```C++
DWORD DeletePrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName
);
```



## <a name="parameters"></a><span data-ttu-id="19907-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="19907-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19907-112">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19907-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19907-113">Ein Handle für den Drucker, dessen Konfigurationsdaten gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="19907-113">A handle to the printer whose configuration data is to be deleted.</span></span> <span data-ttu-id="19907-114">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="19907-114">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="19907-115">*pvaluename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19907-115">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19907-116">Ein Zeiger auf den null-terminierten Namen des zu löschenden Konfigurationsdaten Werts.</span><span class="sxs-lookup"><span data-stu-id="19907-116">A pointer to the null-terminated name of the configuration data value to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19907-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19907-117">Return value</span></span>

<span data-ttu-id="19907-118">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="19907-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="19907-119">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Systemfehler Code.</span><span class="sxs-lookup"><span data-stu-id="19907-119">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="19907-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19907-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="19907-121">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="19907-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="19907-122">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="19907-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="19907-123">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="19907-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="19907-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19907-124">Requirements</span></span>



| <span data-ttu-id="19907-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19907-125">Requirement</span></span> | <span data-ttu-id="19907-126">Wert</span><span class="sxs-lookup"><span data-stu-id="19907-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19907-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19907-127">Minimum supported client</span></span><br/> | <span data-ttu-id="19907-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19907-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="19907-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19907-129">Minimum supported server</span></span><br/> | <span data-ttu-id="19907-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19907-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="19907-131">Header</span><span class="sxs-lookup"><span data-stu-id="19907-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="19907-132"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19907-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="19907-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="19907-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="19907-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19907-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="19907-135">DLL</span><span class="sxs-lookup"><span data-stu-id="19907-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19907-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="19907-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="19907-137">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="19907-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="19907-138">**Deleteprinterdataw** (Unicode) und **deleteprinterdataa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="19907-138">**DeletePrinterDataW** (Unicode) and **DeletePrinterDataA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="19907-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19907-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19907-140">Drucken</span><span class="sxs-lookup"><span data-stu-id="19907-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="19907-141">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="19907-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="19907-142">**Enumprinterdata**</span><span class="sxs-lookup"><span data-stu-id="19907-142">**EnumPrinterData**</span></span>](enumprinterdata.md)
</dt> <dt>

[<span data-ttu-id="19907-143">**Getprinterdata**</span><span class="sxs-lookup"><span data-stu-id="19907-143">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="19907-144">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="19907-144">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="19907-145">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="19907-145">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="19907-146">**Setprinterdata**</span><span class="sxs-lookup"><span data-stu-id="19907-146">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> </dl>

 

 




