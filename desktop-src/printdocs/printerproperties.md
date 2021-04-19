---
description: Die Funktion "printerproperties" zeigt ein Eigenschaften Blatt "Druckereigenschaften" für den angegebenen Drucker an.
ms.assetid: 1d4c961b-178b-47af-b983-5b7327919f93
title: Printerproperties-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrinterProperties
api_type:
- DllExport
api_location:
- plotui.dll
- winspool.drv
ms.openlocfilehash: e7e2c8586c06b2cb64a0e499bd05a6b6016de0a6
ms.sourcegitcommit: c77ed4d933c9f30af0ca0e095a75ad2bdd4d8bf8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "106370894"
---
# <a name="printerproperties-function"></a><span data-ttu-id="9501f-103">Printerproperties-Funktion</span><span class="sxs-lookup"><span data-stu-id="9501f-103">PrinterProperties function</span></span>

<span data-ttu-id="9501f-104">Die Funktion " **printerproperties** " zeigt ein Eigenschaften Blatt "Druckereigenschaften" für den angegebenen Drucker an.</span><span class="sxs-lookup"><span data-stu-id="9501f-104">The **PrinterProperties** function displays a printer-properties property sheet for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9501f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9501f-105">Syntax</span></span>


```C++
BOOL PrinterProperties(
  _In_ HWND   hWnd,
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="9501f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9501f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9501f-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9501f-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9501f-108">Ein Handle für das übergeordnete Fenster des Eigenschaften Blatts.</span><span class="sxs-lookup"><span data-stu-id="9501f-108">A handle to the parent window of the property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="9501f-109">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9501f-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9501f-110">Ein Handle für ein Drucker Objekt.</span><span class="sxs-lookup"><span data-stu-id="9501f-110">A handle to a printer object.</span></span> <span data-ttu-id="9501f-111">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="9501f-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9501f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9501f-112">Return value</span></span>

<span data-ttu-id="9501f-113">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9501f-113">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="9501f-114">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="9501f-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9501f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9501f-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9501f-116">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9501f-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9501f-117">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="9501f-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9501f-118">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="9501f-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9501f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9501f-119">Requirements</span></span>



| <span data-ttu-id="9501f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9501f-120">Requirement</span></span> | <span data-ttu-id="9501f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9501f-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9501f-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9501f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9501f-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9501f-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9501f-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9501f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9501f-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9501f-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9501f-126">Header</span><span class="sxs-lookup"><span data-stu-id="9501f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9501f-127"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9501f-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9501f-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9501f-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="9501f-129"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9501f-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9501f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9501f-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9501f-131"><dt>winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="9501f-131"><dt>winspool.drv</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9501f-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9501f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9501f-133">Drucken</span><span class="sxs-lookup"><span data-stu-id="9501f-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9501f-134">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9501f-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9501f-135">**DocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="9501f-135">**DocumentProperties**</span></span>](documentproperties.md)
</dt> <dt>

[<span data-ttu-id="9501f-136">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="9501f-136">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




