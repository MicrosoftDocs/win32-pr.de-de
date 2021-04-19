---
description: Die GetForm-Funktion Ruft Informationen zu einem angegebenen Formular ab.
ms.assetid: 10b25748-6d7c-46ab-bd2c-9b6126a1d7d1
title: GetForm-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetForm
- GetFormA
- GetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6b6ea9753e1b335936778e17562f6f26467b3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348097"
---
# <a name="getform-function"></a><span data-ttu-id="ec867-103">GetForm-Funktion</span><span class="sxs-lookup"><span data-stu-id="ec867-103">GetForm function</span></span>

<span data-ttu-id="ec867-104">Die **GetForm** -Funktion Ruft Informationen zu einem angegebenen Formular ab.</span><span class="sxs-lookup"><span data-stu-id="ec867-104">The **GetForm** function retrieves information about a specified form.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec867-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec867-105">Syntax</span></span>


```C++
BOOL GetForm(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pFormName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="ec867-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec867-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec867-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec867-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec867-108">Ein Handle für den Drucker.</span><span class="sxs-lookup"><span data-stu-id="ec867-108">A handle to the printer.</span></span> <span data-ttu-id="ec867-109">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="ec867-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="ec867-110">*pformname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec867-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec867-111">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Formulars angibt.</span><span class="sxs-lookup"><span data-stu-id="ec867-111">A pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="ec867-112">Um die Namen der vom Drucker unterstützten Formulare abzurufen, nennen Sie die [**enumforms**](enumforms.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="ec867-112">To get the names of the forms supported by the printer, call the [**EnumForms**](enumforms.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="ec867-113">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec867-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec867-114">Die Version der-Struktur, auf die *pform* zeigt.</span><span class="sxs-lookup"><span data-stu-id="ec867-114">The version of the structure to which *pForm* points.</span></span> <span data-ttu-id="ec867-115">Dieser Wert muss 1 oder 2 sein.</span><span class="sxs-lookup"><span data-stu-id="ec867-115">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="ec867-116">*pform* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ec867-116">*pForm* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec867-117">Ein Zeiger auf ein Bytearray, das die initialisierte [**Form \_ Info \_ 1**](form-info-1.md) oder die [**Form \_ Info \_ 2**](form-info-2.md) -Struktur empfängt.</span><span class="sxs-lookup"><span data-stu-id="ec867-117">A pointer to an array of bytes that receives the initialized [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ec867-118">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec867-118">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec867-119">Die Größe des *pform* -Arrays in Bytes.</span><span class="sxs-lookup"><span data-stu-id="ec867-119">The size, in bytes, of the *pForm* array.</span></span>

</dd> <dt>

<span data-ttu-id="ec867-120">*pcbbenötigte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ec867-120">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec867-121">Ein Zeiger auf einen-Wert, der die Anzahl der kopierten Bytes angibt, wenn die Funktion erfolgreich ist, oder die Anzahl der Bytes, die erforderlich sind, wenn *cbbuf* zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="ec867-121">A pointer to a value that specifies the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec867-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec867-122">Return value</span></span>

<span data-ttu-id="ec867-123">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ec867-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="ec867-124">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="ec867-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec867-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec867-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ec867-126">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ec867-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ec867-127">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="ec867-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ec867-128">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="ec867-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="ec867-129">Wenn der Aufrufer Remote ist und die *Ebene* 2 ist, ist der **StringType** -Wert der zurückgegebenen [**Formular \_ Informationen \_ 2**](form-info-2.md) immer String \_ langpair.</span><span class="sxs-lookup"><span data-stu-id="ec867-129">If the caller is remote, and the *Level* is 2, the **StringType** value of the returned [**FORM\_INFO\_2**](form-info-2.md) will always be STRING\_LANGPAIR.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec867-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec867-130">Requirements</span></span>



| <span data-ttu-id="ec867-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec867-131">Requirement</span></span> | <span data-ttu-id="ec867-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ec867-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec867-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec867-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ec867-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec867-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ec867-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec867-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ec867-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec867-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ec867-137">Header</span><span class="sxs-lookup"><span data-stu-id="ec867-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec867-138"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec867-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ec867-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ec867-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="ec867-140"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec867-140"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ec867-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ec867-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec867-142"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="ec867-142"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="ec867-143">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="ec867-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ec867-144">**Getformw** (Unicode) und **getforma** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ec867-144">**GetFormW** (Unicode) and **GetFormA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="ec867-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec867-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec867-146">Drucken</span><span class="sxs-lookup"><span data-stu-id="ec867-146">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ec867-147">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ec867-147">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ec867-148">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="ec867-148">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="ec867-149">**Deleteform**</span><span class="sxs-lookup"><span data-stu-id="ec867-149">**DeleteForm**</span></span>](deleteform.md)
</dt> <dt>

[<span data-ttu-id="ec867-150">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="ec867-150">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="ec867-151">**Setform**</span><span class="sxs-lookup"><span data-stu-id="ec867-151">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

 




