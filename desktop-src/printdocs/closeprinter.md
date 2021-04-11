---
description: Die closeprinter-Funktion schließt das angegebene Drucker Objekt.
ms.assetid: 95cc3eca-e65c-4fa6-8975-479e8e728dca
title: Closeprinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClosePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: bd21268b86a07357065d4f33b60d1af4b05fa019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218109"
---
# <a name="closeprinter-function"></a><span data-ttu-id="41a13-103">Closeprinter-Funktion</span><span class="sxs-lookup"><span data-stu-id="41a13-103">ClosePrinter function</span></span>

<span data-ttu-id="41a13-104">Die **closeprinter** -Funktion schließt das angegebene Drucker Objekt.</span><span class="sxs-lookup"><span data-stu-id="41a13-104">The **ClosePrinter** function closes the specified printer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="41a13-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="41a13-105">Syntax</span></span>


```C++
BOOL ClosePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="41a13-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="41a13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41a13-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41a13-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41a13-108">Ein Handle für das Drucker Objekt, das geschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="41a13-108">A handle to the printer object to be closed.</span></span> <span data-ttu-id="41a13-109">Dieses Handle wird von der [**OpenPrinter**](openprinter.md) -Funktion oder der [**addprinter**](addprinter.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="41a13-109">This handle is returned by the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41a13-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41a13-110">Return value</span></span>

<span data-ttu-id="41a13-111">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="41a13-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="41a13-112">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="41a13-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="41a13-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41a13-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="41a13-114">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="41a13-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="41a13-115">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="41a13-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="41a13-116">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="41a13-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="41a13-117">Wenn die **closeprinter** -Funktion zurückgibt, ist der Handle- *hprinter* ungültig, unabhängig davon, ob die Funktion erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="41a13-117">When the **ClosePrinter** function returns, the handle *hPrinter* is invalid, regardless of whether the function has succeeded or failed.</span></span>

## <a name="examples"></a><span data-ttu-id="41a13-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="41a13-118">Examples</span></span>

<span data-ttu-id="41a13-119">Ein Beispielprogramm, das diese Funktion verwendet, finden [Sie unter Gewusst wie: Drucken mit der GDI-Druck-API](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="41a13-119">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="41a13-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41a13-120">Requirements</span></span>



| <span data-ttu-id="41a13-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41a13-121">Requirement</span></span> | <span data-ttu-id="41a13-122">Wert</span><span class="sxs-lookup"><span data-stu-id="41a13-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41a13-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41a13-123">Minimum supported client</span></span><br/> | <span data-ttu-id="41a13-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41a13-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="41a13-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41a13-125">Minimum supported server</span></span><br/> | <span data-ttu-id="41a13-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41a13-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="41a13-127">Header</span><span class="sxs-lookup"><span data-stu-id="41a13-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="41a13-128"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41a13-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="41a13-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="41a13-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="41a13-130"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41a13-130"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="41a13-131">DLL</span><span class="sxs-lookup"><span data-stu-id="41a13-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41a13-132"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41a13-132"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="41a13-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41a13-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41a13-134">Drucken</span><span class="sxs-lookup"><span data-stu-id="41a13-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="41a13-135">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="41a13-135">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="41a13-136">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="41a13-136">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="41a13-137">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="41a13-137">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




