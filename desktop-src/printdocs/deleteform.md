---
description: Die deleteform-Funktion entfernt einen Formular Namen aus der Liste der unterstützten Formulare.
ms.assetid: a2d0345f-2469-46ab-935f-777f2b33b621
title: Deleteform-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteForm
- DeleteFormA
- DeleteFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 70ead5026c3b5cf21b28d230f79819bf71eeaf10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042248"
---
# <a name="deleteform-function"></a><span data-ttu-id="56e38-103">Deleteform-Funktion</span><span class="sxs-lookup"><span data-stu-id="56e38-103">DeleteForm function</span></span>

<span data-ttu-id="56e38-104">Die **deleteform** -Funktion entfernt einen Formular Namen aus der Liste der unterstützten Formulare.</span><span class="sxs-lookup"><span data-stu-id="56e38-104">The **DeleteForm** function removes a form name from the list of supported forms.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e38-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="56e38-105">Syntax</span></span>


```C++
BOOL DeleteForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName
);
```



## <a name="parameters"></a><span data-ttu-id="56e38-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56e38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56e38-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="56e38-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56e38-108">Gibt das öffnende Drucker Handle an, auf dem diese Funktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="56e38-108">Indicates the open printer handle that this function is to be performed upon.</span></span> <span data-ttu-id="56e38-109">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="56e38-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="56e38-110">*pformname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="56e38-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56e38-111">Ein Zeiger auf den zu entfernenden Formular Namen.</span><span class="sxs-lookup"><span data-stu-id="56e38-111">Pointer to the form name to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56e38-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56e38-112">Return value</span></span>

<span data-ttu-id="56e38-113">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="56e38-113">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="56e38-114">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="56e38-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="56e38-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56e38-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="56e38-116">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="56e38-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="56e38-117">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="56e38-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="56e38-118">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="56e38-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="56e38-119">**Deleteform** kann nur Formular Namen löschen, die mithilfe der [**AddForm**](addform.md) -Funktion hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="56e38-119">**DeleteForm** can only delete form names that were added by using the [**AddForm**](addform.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="56e38-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56e38-120">Requirements</span></span>



| <span data-ttu-id="56e38-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56e38-121">Requirement</span></span> | <span data-ttu-id="56e38-122">Wert</span><span class="sxs-lookup"><span data-stu-id="56e38-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56e38-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56e38-123">Minimum supported client</span></span><br/> | <span data-ttu-id="56e38-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56e38-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="56e38-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56e38-125">Minimum supported server</span></span><br/> | <span data-ttu-id="56e38-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56e38-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="56e38-127">Header</span><span class="sxs-lookup"><span data-stu-id="56e38-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="56e38-128"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56e38-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="56e38-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="56e38-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="56e38-130"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56e38-130"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="56e38-131">DLL</span><span class="sxs-lookup"><span data-stu-id="56e38-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56e38-132"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="56e38-132"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="56e38-133">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="56e38-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="56e38-134">**Deleteformw** (Unicode) und **deleteforma** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="56e38-134">**DeleteFormW** (Unicode) and **DeleteFormA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="56e38-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56e38-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56e38-136">Drucken</span><span class="sxs-lookup"><span data-stu-id="56e38-136">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="56e38-137">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="56e38-137">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="56e38-138">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="56e38-138">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="56e38-139">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="56e38-139">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




