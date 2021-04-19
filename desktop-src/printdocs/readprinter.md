---
description: Die Funktion "Read Printer" Ruft Daten vom angegebenen Drucker ab.
ms.assetid: d7c3f186-c53e-424b-89bf-6742babb998f
title: Funktion "Read Printer" (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ddbdfc03b80557583c60f461f0c7e3a6fe2473fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362556"
---
# <a name="readprinter-function"></a><span data-ttu-id="6dd66-103">Funktion "leserprinter"</span><span class="sxs-lookup"><span data-stu-id="6dd66-103">ReadPrinter function</span></span>

<span data-ttu-id="6dd66-104">Die Funktion "read **Printer** " Ruft Daten vom angegebenen Drucker ab.</span><span class="sxs-lookup"><span data-stu-id="6dd66-104">The **ReadPrinter** function retrieves data from the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dd66-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6dd66-105">Syntax</span></span>


```C++
BOOL ReadPrinter(
  _In_  HANDLE  hPrinter,
  _Out_ LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pNoBytesRead
);
```



## <a name="parameters"></a><span data-ttu-id="6dd66-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6dd66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dd66-107">*hprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6dd66-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dd66-108">Ein Handle für das Drucker Objekt, für das Daten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6dd66-108">A handle to the printer object for which to retrieve data.</span></span> <span data-ttu-id="6dd66-109">Verwenden Sie die [**OpenPrinter**](openprinter.md) -Funktion, um ein Drucker Objekt Handle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6dd66-109">Use the [**OpenPrinter**](openprinter.md) function to retrieve a printer object handle.</span></span> <span data-ttu-id="6dd66-110">Verwenden Sie das Format: PrinterName, Job xxxx.</span><span class="sxs-lookup"><span data-stu-id="6dd66-110">Use the format: Printername, Job xxxx.</span></span>

</dd> <dt>

<span data-ttu-id="6dd66-111">*PBUF* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6dd66-111">*pBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dd66-112">Ein Zeiger auf einen Puffer, der die Druckerdaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="6dd66-112">A pointer to a buffer that receives the printer data.</span></span>

</dd> <dt>

<span data-ttu-id="6dd66-113">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6dd66-113">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dd66-114">Die Größe (in Bytes) des Puffers, auf den *PBUF* zeigt.</span><span class="sxs-lookup"><span data-stu-id="6dd66-114">The size, in bytes, of the buffer to which *pBuf* points.</span></span>

</dd> <dt>

<span data-ttu-id="6dd66-115">*pnobytesread* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6dd66-115">*pNoBytesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dd66-116">Ein Zeiger auf eine Variable, die die Anzahl der Daten Bytes empfängt, die in das Array kopiert werden, auf das *PBUF* zeigt.</span><span class="sxs-lookup"><span data-stu-id="6dd66-116">A pointer to a variable that receives the number of bytes of data copied into the array to which *pBuf* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dd66-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6dd66-117">Return value</span></span>

<span data-ttu-id="6dd66-118">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6dd66-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="6dd66-119">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="6dd66-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dd66-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6dd66-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6dd66-121">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6dd66-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6dd66-122">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="6dd66-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6dd66-123">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="6dd66-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="6dd66-124">" **Leseprinter** " gibt einen Fehler zurück, wenn das Gerät oder der Drucker nicht bidirektional ist.</span><span class="sxs-lookup"><span data-stu-id="6dd66-124">**ReadPrinter** returns an error if the device or the printer is not bidirectional.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dd66-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6dd66-125">Requirements</span></span>



| <span data-ttu-id="6dd66-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6dd66-126">Requirement</span></span> | <span data-ttu-id="6dd66-127">Wert</span><span class="sxs-lookup"><span data-stu-id="6dd66-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dd66-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6dd66-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6dd66-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6dd66-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6dd66-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6dd66-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6dd66-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6dd66-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6dd66-132">Header</span><span class="sxs-lookup"><span data-stu-id="6dd66-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dd66-133"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6dd66-133"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6dd66-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6dd66-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="6dd66-135"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6dd66-135"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6dd66-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6dd66-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dd66-137"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dd66-137"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="6dd66-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6dd66-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dd66-139">Drucken</span><span class="sxs-lookup"><span data-stu-id="6dd66-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6dd66-140">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="6dd66-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6dd66-141">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="6dd66-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




