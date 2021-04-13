---
description: Die setform-Funktion legt die Formularinformationen für den angegebenen Drucker fest.
ms.assetid: 05d5d495-952c-4a1d-8694-1004d0c2bcf6
title: Setform-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetForm
- SetFormA
- SetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 93848afa0f36032bb972f8f4a7c6c3d5eb8c42ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345279"
---
# <a name="setform-function"></a><span data-ttu-id="def10-103">Setform-Funktion</span><span class="sxs-lookup"><span data-stu-id="def10-103">SetForm function</span></span>

<span data-ttu-id="def10-104">Die **setform** -Funktion legt die Formularinformationen für den angegebenen Drucker fest.</span><span class="sxs-lookup"><span data-stu-id="def10-104">The **SetForm** function sets the form information for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="def10-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="def10-105">Syntax</span></span>


```C++
BOOL SetForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName,
  _In_ DWORD  Level,
  _In_ LPTSTR pForm
);
```



## <a name="parameters"></a><span data-ttu-id="def10-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="def10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="def10-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="def10-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def10-108">Ein Handle für den Drucker, für den die Formularinformationen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="def10-108">A handle to the printer for which the form information is set.</span></span> <span data-ttu-id="def10-109">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="def10-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="def10-110">*pformname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="def10-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def10-111">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Formular Namen angibt, für den die Formularinformationen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="def10-111">A pointer to a null-terminated string that specifies the form name for which the form information is set.</span></span>

</dd> <dt>

<span data-ttu-id="def10-112">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="def10-112">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def10-113">Die Version der-Struktur, auf die *pform* zeigt.</span><span class="sxs-lookup"><span data-stu-id="def10-113">The version of the structure to which *pForm* points.</span></span> <span data-ttu-id="def10-114">Dieser Wert muss 1 oder 2 sein.</span><span class="sxs-lookup"><span data-stu-id="def10-114">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="def10-115">*pform* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="def10-115">*pForm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def10-116">Ein Zeiger auf das [**Formular \_ Info \_ 1**](form-info-1.md) oder die [**Form \_ Info \_ 2**](form-info-2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="def10-116">A pointer to a [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="def10-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="def10-117">Return value</span></span>

<span data-ttu-id="def10-118">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="def10-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="def10-119">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="def10-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="def10-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="def10-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="def10-121">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="def10-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="def10-122">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="def10-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="def10-123">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="def10-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="def10-124">**Setform** kann für ein vorhandenes [**Formular \_ Info \_ 2**](form-info-2.md)mehrmals aufgerufen werden. bei jedem Aufruf werden zusätzliche Paare von **pdisplayname** -und **wlangid** -Werten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="def10-124">**SetForm** can be called multiple times for an existing [**FORM\_INFO\_2**](form-info-2.md), each call adding additional pairs of **pDisplayName** and **wLangId** values.</span></span> <span data-ttu-id="def10-125">Alle Sprachversionen des Formulars erhalten die Werte **size** und **imageablearea** im **Formular \_ Info \_ 2** im letzten Aufrufen von **setform**.</span><span class="sxs-lookup"><span data-stu-id="def10-125">All languages versions of the form will get the **Size** and **ImageableArea** values of the **FORM\_INFO\_2** in the most recent call to **SetForm**.</span></span>

<span data-ttu-id="def10-126">Wenn der Aufrufer Remote und die *Ebene* 2 ist, kann der **StringType** -Wert der [**Formular \_ Info \_ 2**](form-info-2.md) nicht String \_ muidll sein.</span><span class="sxs-lookup"><span data-stu-id="def10-126">If the caller is remote and the *Level* is 2, the **StringType** value of the [**FORM\_INFO\_2**](form-info-2.md) cannot be STRING\_MUIDLL.</span></span>

## <a name="requirements"></a><span data-ttu-id="def10-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="def10-127">Requirements</span></span>



| <span data-ttu-id="def10-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="def10-128">Requirement</span></span> | <span data-ttu-id="def10-129">Wert</span><span class="sxs-lookup"><span data-stu-id="def10-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="def10-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="def10-130">Minimum supported client</span></span><br/> | <span data-ttu-id="def10-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="def10-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="def10-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="def10-132">Minimum supported server</span></span><br/> | <span data-ttu-id="def10-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="def10-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="def10-134">Header</span><span class="sxs-lookup"><span data-stu-id="def10-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="def10-135"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="def10-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="def10-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="def10-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="def10-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="def10-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="def10-138">DLL</span><span class="sxs-lookup"><span data-stu-id="def10-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="def10-139"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="def10-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="def10-140">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="def10-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="def10-141">**Setformw** (Unicode) und **setforma** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="def10-141">**SetFormW** (Unicode) and **SetFormA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="def10-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="def10-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def10-143">Drucken</span><span class="sxs-lookup"><span data-stu-id="def10-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="def10-144">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="def10-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="def10-145">**GetForm**</span><span class="sxs-lookup"><span data-stu-id="def10-145">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="def10-146">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="def10-146">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="def10-147">**Formular \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="def10-147">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="def10-148">**Formular \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="def10-148">**FORM\_INFO\_2**</span></span>](form-info-2.md)
</dt> </dl>

 

 




