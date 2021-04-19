---
description: Die AddForm-Funktion fügt der Liste der verfügbaren Formulare, die für den angegebenen Drucker ausgewählt werden können, ein Formular hinzu.
ms.assetid: 17b59019-f93a-4b57-86fb-91c61aecbac4
title: AddForm-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddForm
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2de3ddbdc57a5a41bac048a94a8175cd124df4ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349835"
---
# <a name="addform-function"></a><span data-ttu-id="0566b-103">AddForm-Funktion</span><span class="sxs-lookup"><span data-stu-id="0566b-103">AddForm function</span></span>

<span data-ttu-id="0566b-104">Die **AddForm** -Funktion fügt der Liste der verfügbaren Formulare, die für den angegebenen Drucker ausgewählt werden können, ein Formular hinzu.</span><span class="sxs-lookup"><span data-stu-id="0566b-104">The **AddForm** function adds a form to the list of available forms that can be selected for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0566b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0566b-105">Syntax</span></span>


```C++
BOOL AddForm(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pForm
);
```



## <a name="parameters"></a><span data-ttu-id="0566b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0566b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0566b-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0566b-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0566b-108">Ein Handle für den Drucker, der das Drucken mit dem angegebenen Formular unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0566b-108">A handle to the printer that supports printing with the specified form.</span></span> <span data-ttu-id="0566b-109">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="0566b-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="0566b-110">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0566b-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0566b-111">Die Ebene der-Struktur, auf die *pform* zeigt.</span><span class="sxs-lookup"><span data-stu-id="0566b-111">The level of the structure to which *pForm* points.</span></span> <span data-ttu-id="0566b-112">Dieser Wert muss 1 oder 2 sein.</span><span class="sxs-lookup"><span data-stu-id="0566b-112">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="0566b-113">*pform* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0566b-113">*pForm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0566b-114">Ein Zeiger auf das [**Formular \_ Info \_ 1**](form-info-1.md) oder die [**Form \_ Info \_ 2**](form-info-2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0566b-114">A pointer to a [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0566b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0566b-115">Return value</span></span>

<span data-ttu-id="0566b-116">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="0566b-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="0566b-117">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="0566b-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0566b-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0566b-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0566b-119">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0566b-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="0566b-120">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="0566b-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="0566b-121">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="0566b-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="0566b-122">Eine Anwendung kann ermitteln, welche Formulare für einen Drucker verfügbar sind, indem die [**enumforms**](enumforms.md) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0566b-122">An application can determine which forms are available for a printer by calling the [**EnumForms**](enumforms.md) function.</span></span>

<span data-ttu-id="0566b-123">Wenn *pform* auf das [**Formular \_ Info \_ 2**](form-info-2.md)zeigt, schlägt **AddForm** fehl, wenn entweder ein Formular mit dem angegebenen Namen bereits vorhanden ist oder der *pkeyword* -Wert der Struktur bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0566b-123">If *pForm* points to a [**FORM\_INFO\_2**](form-info-2.md), then **AddForm** will fail if either a form with the specified name already exists or the structure's *pKeyword* value already exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="0566b-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0566b-124">Requirements</span></span>



| <span data-ttu-id="0566b-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0566b-125">Requirement</span></span> | <span data-ttu-id="0566b-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0566b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0566b-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0566b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0566b-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0566b-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0566b-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0566b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0566b-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0566b-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0566b-131">Header</span><span class="sxs-lookup"><span data-stu-id="0566b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0566b-132"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0566b-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0566b-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0566b-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="0566b-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0566b-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="0566b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0566b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0566b-136"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0566b-136"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="0566b-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0566b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0566b-138">Drucken</span><span class="sxs-lookup"><span data-stu-id="0566b-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0566b-139">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="0566b-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="0566b-140">**Enumforms**</span><span class="sxs-lookup"><span data-stu-id="0566b-140">**EnumForms**</span></span>](enumforms.md)
</dt> <dt>

[<span data-ttu-id="0566b-141">**Formular \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="0566b-141">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="0566b-142">**Formular \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="0566b-142">**FORM\_INFO\_2**</span></span>](form-info-2.md)
</dt> <dt>

[<span data-ttu-id="0566b-143">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="0566b-143">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




