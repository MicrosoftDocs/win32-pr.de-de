---
description: Die enumprintprocessordatatypes-Funktion Listet die Datentypen auf, die ein angegebener Druck Prozessor unterstützt.
ms.assetid: 27b6e074-d303-446b-9e5f-6cfa55c30d26
title: Enumprintprocessordatatypes-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessorDatatypes
- EnumPrintProcessorDatatypesA
- EnumPrintProcessorDatatypesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 39742aff1fce73b6dac138e77f2f8c794428ff3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529000"
---
# <a name="enumprintprocessordatatypes-function"></a><span data-ttu-id="3ea45-103">Enumprintprocessordatatypes-Funktion</span><span class="sxs-lookup"><span data-stu-id="3ea45-103">EnumPrintProcessorDatatypes function</span></span>

<span data-ttu-id="3ea45-104">Die **enumprintprocessordatatypes** -Funktion Listet die Datentypen auf, die ein angegebener Druck Prozessor unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ea45-104">The **EnumPrintProcessorDatatypes** function enumerates the data types that a specified print processor supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ea45-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ea45-105">Syntax</span></span>


```C++
BOOL EnumPrintProcessorDatatypes(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pPrintProcessorName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDatatypes,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="3ea45-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ea45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ea45-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ea45-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea45-108">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Servers angibt, auf dem sich der Druck Prozessor befindet.</span><span class="sxs-lookup"><span data-stu-id="3ea45-108">A pointer to a null-terminated string that specifies the name of the server on which the print processor resides.</span></span> <span data-ttu-id="3ea45-109">Wenn dieser Parameter **null** ist, werden die Datentypen für den lokalen Druck Prozessor aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="3ea45-109">If this parameter is **NULL**, the data types for the local print processor are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="3ea45-110">*pprintprocessorname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ea45-110">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea45-111">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druck Prozessors angibt, dessen Datentypen aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="3ea45-111">A pointer to a null-terminated string that specifies the name of the print processor whose data types are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="3ea45-112">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ea45-112">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea45-113">Der Typ der Informationen, die im Puffer *pdatatypes* zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3ea45-113">The type of information returned in the *pDatatypes* buffer.</span></span> <span data-ttu-id="3ea45-114">Dieser Parameter muss 1 sein.</span><span class="sxs-lookup"><span data-stu-id="3ea45-114">This parameter must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="3ea45-115">*pdatatypes* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3ea45-115">*pDatatypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea45-116">Ein Zeiger auf einen Puffer, der ein Array von [**Datatypes- \_ Informationen \_ 1**](datatypes-info-1.md) -Strukturen empfängt.</span><span class="sxs-lookup"><span data-stu-id="3ea45-116">A pointer to a buffer that receives an array of [**DATATYPES\_INFO\_1**](datatypes-info-1.md) structures.</span></span> <span data-ttu-id="3ea45-117">Jede Struktur beschreibt einen verfügbaren Datentyp.</span><span class="sxs-lookup"><span data-stu-id="3ea45-117">Each structure describes an available data type.</span></span> <span data-ttu-id="3ea45-118">Der Puffer muss groß genug sein, um das Array von Strukturen und Zeichen folgen oder andere Daten zu erhalten, auf die die Strukturmember zeigen.</span><span class="sxs-lookup"><span data-stu-id="3ea45-118">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="3ea45-119">Um die erforderliche Puffergröße zu ermitteln, müssen Sie **enumprintprocessordatatypes** aufrufen, wobei *cbbuf* auf 0 (null) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3ea45-119">To determine the required buffer size, call **EnumPrintProcessorDatatypes** with *cbBuf* set to zero.</span></span> <span data-ttu-id="3ea45-120">**Enumprintprocessordatatypes** schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen fehlerhaften \_ Puffer zurück \_ , und der *pcbrequired* -Parameter gibt die Größe (in Bytes) des Puffers zurück, der für das Array von Strukturen und deren Daten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3ea45-120">**EnumPrintProcessorDatatypes** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="3ea45-121">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ea45-121">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea45-122">Die Größe (in Bytes) des Puffers, auf den *pdatatypes* zeigt.</span><span class="sxs-lookup"><span data-stu-id="3ea45-122">The size, in bytes, of the buffer pointed to by *pDatatypes*.</span></span>

</dd> <dt>

<span data-ttu-id="3ea45-123">*pcbbenötigte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3ea45-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea45-124">Ein Zeiger auf eine Variable, die die Anzahl von Bytes empfängt, die in den *pdatatypes* -Puffer kopiert werden, wenn die Funktion erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ea45-124">A pointer to a variable that receives the number of bytes copied to the *pDatatypes* buffer if the function succeeds.</span></span> <span data-ttu-id="3ea45-125">Wenn der Puffer zu klein ist, schlägt die Funktion fehl, und die Variable erhält die erforderliche Anzahl von Bytes.</span><span class="sxs-lookup"><span data-stu-id="3ea45-125">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="3ea45-126">*pkreturned* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3ea45-126">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea45-127">Ein Zeiger auf eine Variable, die die Anzahl der im *pdatatypes* -Puffer zurückgegebenen Strukturen empfängt.</span><span class="sxs-lookup"><span data-stu-id="3ea45-127">A pointer to a variable that receives the number of structures returned in the *pDatatypes* buffer.</span></span> <span data-ttu-id="3ea45-128">Dies ist die Anzahl der unterstützten Datentypen.</span><span class="sxs-lookup"><span data-stu-id="3ea45-128">This is the number of supported data types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ea45-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ea45-129">Return value</span></span>

<span data-ttu-id="3ea45-130">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="3ea45-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="3ea45-131">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="3ea45-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ea45-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ea45-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3ea45-133">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3ea45-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="3ea45-134">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="3ea45-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="3ea45-135">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="3ea45-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="3ea45-136">v</span><span class="sxs-lookup"><span data-stu-id="3ea45-136">v</span></span>

<span data-ttu-id="3ea45-137">Ab Windows Vista werden die Datentyp Informationen von Remote Druckservern aus einem lokalen Cache abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3ea45-137">Starting with Windows Vista, the data type information from remote print servers is retrieved from a local cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ea45-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ea45-138">Requirements</span></span>



| <span data-ttu-id="3ea45-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ea45-139">Requirement</span></span> | <span data-ttu-id="3ea45-140">Wert</span><span class="sxs-lookup"><span data-stu-id="3ea45-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ea45-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ea45-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3ea45-142">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ea45-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3ea45-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ea45-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3ea45-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ea45-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3ea45-145">Header</span><span class="sxs-lookup"><span data-stu-id="3ea45-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ea45-146"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ea45-146"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3ea45-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3ea45-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ea45-148"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ea45-148"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="3ea45-149">DLL</span><span class="sxs-lookup"><span data-stu-id="3ea45-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ea45-150"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="3ea45-150"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="3ea45-151">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="3ea45-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3ea45-152">**Enumprintprocessordatatypesw** (Unicode) und **enumprintprocessordatatypesa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3ea45-152">**EnumPrintProcessorDatatypesW** (Unicode) and **EnumPrintProcessorDatatypesA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="3ea45-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ea45-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ea45-154">Drucken</span><span class="sxs-lookup"><span data-stu-id="3ea45-154">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3ea45-155">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="3ea45-155">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="3ea45-156">**Datatypes- \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="3ea45-156">**DATATYPES\_INFO\_1**</span></span>](datatypes-info-1.md)
</dt> <dt>

[<span data-ttu-id="3ea45-157">**Enumprintprozessoren**</span><span class="sxs-lookup"><span data-stu-id="3ea45-157">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> </dl>

 

