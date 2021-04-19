---
description: Mit der Funktion "SetDefaultPrinter" wird der Druckername des Standard Druckers für den aktuellen Benutzer auf dem lokalen Computer festgelegt.
ms.assetid: 55eec548-577f-422b-80e3-8b23aa4d2159
title: SetDefaultPrinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDefaultPrinter
- SetDefaultPrinterA
- SetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 346d356aea3d806284823541aa219699e51c2187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348141"
---
# <a name="setdefaultprinter-function"></a><span data-ttu-id="369ec-103">SetDefaultPrinter-Funktion</span><span class="sxs-lookup"><span data-stu-id="369ec-103">SetDefaultPrinter function</span></span>

<span data-ttu-id="369ec-104">Mit der Funktion " **SetDefaultPrinter** " wird der Druckername des Standard Druckers für den aktuellen Benutzer auf dem lokalen Computer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="369ec-104">The **SetDefaultPrinter** function sets the printer name of the default printer for the current user on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="369ec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="369ec-105">Syntax</span></span>


```C++
BOOL SetDefaultPrinter(
  _In_ LPCTSTR pszPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="369ec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="369ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="369ec-107">*pszprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="369ec-107">*pszPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="369ec-108">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Standarddrucker Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="369ec-108">A pointer to a null-terminated string containing the default printer name.</span></span> <span data-ttu-id="369ec-109">Bei einer Remote Druckerverbindung lautet das Namensformat **\\\\** _Server_- *_\\_* _Druckername_.</span><span class="sxs-lookup"><span data-stu-id="369ec-109">For a remote printer connection, the name format is **\\\\**_server_*_\\_*_printername_.</span></span> <span data-ttu-id="369ec-110">Bei einem lokalen Drucker lautet das Namensformat " *Druckername*".</span><span class="sxs-lookup"><span data-stu-id="369ec-110">For a local printer, the name format is *printername*.</span></span>

<span data-ttu-id="369ec-111">Wenn dieser Parameter **null** ist oder eine leere Zeichenfolge ist, d. h. "", wählt **SetDefaultPrinter** einen Standarddrucker von einem der installierten Drucker aus.</span><span class="sxs-lookup"><span data-stu-id="369ec-111">If this parameter is **NULL** or an empty string, that is, "", **SetDefaultPrinter** will select a default printer from one of the installed printers.</span></span> <span data-ttu-id="369ec-112">Wenn bereits ein Standarddrucker vorhanden ist, kann der Standarddrucker durch Aufrufen von **SetDefaultPrinter** mit **null** oder einer leeren Zeichenfolge in diesem Parameter geändert werden.</span><span class="sxs-lookup"><span data-stu-id="369ec-112">If a default printer already exists, calling **SetDefaultPrinter** with a **NULL** or an empty string in this parameter might change the default printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="369ec-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="369ec-113">Return value</span></span>

<span data-ttu-id="369ec-114">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="369ec-114">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="369ec-115">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="369ec-115">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="369ec-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="369ec-116">Remarks</span></span>

<span data-ttu-id="369ec-117">Wenn Sie diese Methode verwenden, müssen Sie einen gültigen Drucker, Treiber und Port angeben.</span><span class="sxs-lookup"><span data-stu-id="369ec-117">When using this method, you must specify a valid printer, driver, and port.</span></span> <span data-ttu-id="369ec-118">Wenn Sie ungültig sind, schlagen die APIs nicht fehl, aber das Ergebnis ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="369ec-118">If they are invalid, the APIs do not fail but the result is not defined.</span></span> <span data-ttu-id="369ec-119">Dies könnte dazu führen, dass andere Programme den Drucker auf den vorherigen gültigen Drucker zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="369ec-119">This could cause other programs to set the printer back to the previous valid printer.</span></span> <span data-ttu-id="369ec-120">Mit [**enumdruckern**](enumprinters.md) können Sie den Drucker Namen, den Treiber Namen und den Portnamen aller verfügbaren Drucker abrufen.</span><span class="sxs-lookup"><span data-stu-id="369ec-120">You can use [**EnumPrinters**](enumprinters.md) to retrieve the printer name, driver name, and port name of all available printers.</span></span>

> [!Note]  
> <span data-ttu-id="369ec-121">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="369ec-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="369ec-122">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="369ec-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="369ec-123">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="369ec-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="369ec-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="369ec-124">Requirements</span></span>



| <span data-ttu-id="369ec-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="369ec-125">Requirement</span></span> | <span data-ttu-id="369ec-126">Wert</span><span class="sxs-lookup"><span data-stu-id="369ec-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="369ec-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="369ec-127">Minimum supported client</span></span><br/> | <span data-ttu-id="369ec-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="369ec-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="369ec-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="369ec-129">Minimum supported server</span></span><br/> | <span data-ttu-id="369ec-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="369ec-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="369ec-131">Header</span><span class="sxs-lookup"><span data-stu-id="369ec-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="369ec-132"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="369ec-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="369ec-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="369ec-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="369ec-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="369ec-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="369ec-135">DLL</span><span class="sxs-lookup"><span data-stu-id="369ec-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="369ec-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="369ec-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="369ec-137">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="369ec-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="369ec-138">**Setdefaultprinterw** (Unicode) und **setdefaultprintera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="369ec-138">**SetDefaultPrinterW** (Unicode) and **SetDefaultPrinterA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="369ec-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="369ec-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="369ec-140">Drucken</span><span class="sxs-lookup"><span data-stu-id="369ec-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="369ec-141">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="369ec-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="369ec-142">**Enumdrucker**</span><span class="sxs-lookup"><span data-stu-id="369ec-142">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="369ec-143">**GetDefaultPrinter**</span><span class="sxs-lookup"><span data-stu-id="369ec-143">**GetDefaultPrinter**</span></span>](getdefaultprinter.md)
</dt> </dl>

 

 




