---
description: Die enumforms-Funktion Listet die Formulare auf, die vom angegebenen Drucker unterstützt werden.
ms.assetid: b13b515a-c764-4a80-ab85-95fb4abb2a6b
title: Enumforms-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumForms
- EnumFormsA
- EnumFormsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 18cd9ad6f8e0491700d5618e29a0a629e8045366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345299"
---
# <a name="enumforms-function"></a><span data-ttu-id="48037-103">Enumforms-Funktion</span><span class="sxs-lookup"><span data-stu-id="48037-103">EnumForms function</span></span>

<span data-ttu-id="48037-104">Die **enumforms** -Funktion Listet die Formulare auf, die vom angegebenen Drucker unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="48037-104">The **EnumForms** function enumerates the forms supported by the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="48037-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="48037-105">Syntax</span></span>


```C++
BOOL EnumForms(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="48037-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="48037-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48037-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48037-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48037-108">Handle für den Drucker, für den die Formulare aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="48037-108">Handle to the printer for which the forms should be enumerated.</span></span> <span data-ttu-id="48037-109">Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.</span><span class="sxs-lookup"><span data-stu-id="48037-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="48037-110">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48037-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48037-111">Gibt die Version der-Struktur an, auf die *pform* zeigt.</span><span class="sxs-lookup"><span data-stu-id="48037-111">Specifies the version of the structure to which *pForm* points.</span></span> <span data-ttu-id="48037-112">Dieser Wert muss 1 oder 2 sein.</span><span class="sxs-lookup"><span data-stu-id="48037-112">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="48037-113">*pform* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="48037-113">*pForm* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48037-114">Zeiger auf eine oder mehrere [**Formular \_ Info \_ 1**](form-info-1.md) -Strukturen oder auf mindestens eine [**Formular \_ Info \_ 2**](form-info-2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="48037-114">Pointer to one or more [**FORM\_INFO\_1**](form-info-1.md) structures or to one or more [**FORM\_INFO\_2**](form-info-2.md) structures.</span></span> <span data-ttu-id="48037-115">Alle-Strukturen haben dieselbe Ebene.</span><span class="sxs-lookup"><span data-stu-id="48037-115">All the structures will have the same level.</span></span>

</dd> <dt>

<span data-ttu-id="48037-116">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48037-116">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48037-117">Gibt die Größe des Puffers in Bytes an, auf den *pform* zeigt.</span><span class="sxs-lookup"><span data-stu-id="48037-117">Specifies the size, in bytes, of the buffer to which *pForm* points.</span></span>

</dd> <dt>

<span data-ttu-id="48037-118">*pcbbenötigte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="48037-118">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48037-119">Ein Zeiger auf eine Variable, die die Anzahl der Bytes empfängt, die in das Array kopiert werden, auf das *pform* zeigt (wenn der Vorgang erfolgreich ist), oder die Anzahl der erforderlichen Bytes (wenn Sie fehlschlägt, da *cbbuf* zu klein ist).</span><span class="sxs-lookup"><span data-stu-id="48037-119">Pointer to a variable that receives the number of bytes copied to the array to which *pForm* points (if the operation succeeds) or the number of bytes required (if it fails because *cbBuf* is too small).</span></span>

</dd> <dt>

<span data-ttu-id="48037-120">*pkreturned* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="48037-120">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48037-121">Ein Zeiger auf eine Variable, die die Anzahl der in das Array kopierten Strukturen erhält, auf die *pform* zeigt.</span><span class="sxs-lookup"><span data-stu-id="48037-121">Pointer to a variable that receives the number of structures copied into the array to which *pForm* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48037-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48037-122">Return value</span></span>

<span data-ttu-id="48037-123">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="48037-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="48037-124">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="48037-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="48037-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48037-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="48037-126">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="48037-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="48037-127">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="48037-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="48037-128">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="48037-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="48037-129">Wenn der Aufrufer Remote ist und die *Ebene* 2 ist, ist der **StringType** -Wert der zurückgegebenen [**Formular \_ Informationen \_ 2**](form-info-2.md) -Strukturen immer **String \_ langpair**.</span><span class="sxs-lookup"><span data-stu-id="48037-129">If the caller is remote, and the *Level* is 2, the **StringType** value of the returned [**FORM\_INFO\_2**](form-info-2.md) structures will always be **STRING\_LANGPAIR**.</span></span>

<span data-ttu-id="48037-130">In Windows Vista werden die von **enumforms** zurückgegebenen Formulardaten aus einem lokalen Cache abgerufen, wenn sich *hprinter* auf einen Remote Druckserver oder einen Drucker bezieht, der von einem Druckserver gehostet wird, und mindestens eine geöffnete Verbindung mit einem Drucker auf dem Remote Drucker Server vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="48037-130">In Windows Vista, the form data returned by **EnumForms** is retrieved from a local cache when *hPrinter* refers to a remote print server or a printer hosted by a print server and there is at least one open connection to a printer on the remote print server.</span></span> <span data-ttu-id="48037-131">In allen anderen Konfigurationen werden die Formulardaten vom Remote Druckserver abgefragt.</span><span class="sxs-lookup"><span data-stu-id="48037-131">In all other configurations, the form data is queried from the remote print server.</span></span>

## <a name="requirements"></a><span data-ttu-id="48037-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48037-132">Requirements</span></span>



| <span data-ttu-id="48037-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48037-133">Requirement</span></span> | <span data-ttu-id="48037-134">Wert</span><span class="sxs-lookup"><span data-stu-id="48037-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48037-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48037-135">Minimum supported client</span></span><br/> | <span data-ttu-id="48037-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48037-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="48037-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48037-137">Minimum supported server</span></span><br/> | <span data-ttu-id="48037-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48037-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="48037-139">Header</span><span class="sxs-lookup"><span data-stu-id="48037-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="48037-140"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48037-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="48037-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="48037-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="48037-142"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48037-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="48037-143">DLL</span><span class="sxs-lookup"><span data-stu-id="48037-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48037-144"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="48037-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="48037-145">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="48037-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="48037-146">**Enumformsw** (Unicode) und **enumformsa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="48037-146">**EnumFormsW** (Unicode) and **EnumFormsA** (ANSI)</span></span><br/>                                             |



## <a name="see-also"></a><span data-ttu-id="48037-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48037-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48037-148">Drucken</span><span class="sxs-lookup"><span data-stu-id="48037-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="48037-149">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="48037-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="48037-150">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="48037-150">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="48037-151">**Formular \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="48037-151">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="48037-152">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="48037-152">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




