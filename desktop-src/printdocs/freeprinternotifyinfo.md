---
description: Die Funktion "freprinternotifyinfo" gibt einen vom System zugewiesenen Puffer frei, der von der findnextprinterchangenotifi-Funktion erstellt wurde.
ms.assetid: e50d4718-3682-486b-9d07-ddddd0b284dc
title: Freprinternotifyinfo-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePrinterNotifyInfo
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 8d2cc22971c2645af250a9e92872b89959387163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347351"
---
# <a name="freeprinternotifyinfo-function"></a><span data-ttu-id="d3b72-103">Freprinternotifyinfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="d3b72-103">FreePrinterNotifyInfo function</span></span>

<span data-ttu-id="d3b72-104">Die Funktion " **freprinternotifyinfo** " gibt einen vom System zugewiesenen Puffer frei, der von der [**findnextprinterchangenotifi-**](findnextprinterchangenotification.md) Funktion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d3b72-104">The **FreePrinterNotifyInfo** function frees a system-allocated buffer created by the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3b72-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3b72-105">Syntax</span></span>


```C++
BOOL FreePrinterNotifyInfo(
  _In_ PPRINTER_NOTIFY_INFO pPrinterNotifyInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d3b72-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3b72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3b72-107">*pprinternotifyinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3b72-107">*pPrinterNotifyInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3b72-108">Zeiger auf einen [**Drucker \_ Benachrichtigungs \_**](printer-notify-info.md) Puffer, der von einem aufrufsbefehl der [**findnextprinterchangenotifi-**](findnextprinterchangenotification.md) Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d3b72-108">Pointer to a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) buffer returned from a call to the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span> <span data-ttu-id="d3b72-109">" **Freiprinternotifyinfo** " hebt die Zuordnung dieses Puffers auf.</span><span class="sxs-lookup"><span data-stu-id="d3b72-109">**FreePrinterNotifyInfo** deallocates this buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3b72-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3b72-110">Return value</span></span>

<span data-ttu-id="d3b72-111">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d3b72-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d3b72-112">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="d3b72-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3b72-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3b72-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d3b72-114">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d3b72-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d3b72-115">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="d3b72-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d3b72-116">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="d3b72-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d3b72-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3b72-117">Requirements</span></span>



| <span data-ttu-id="d3b72-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3b72-118">Requirement</span></span> | <span data-ttu-id="d3b72-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d3b72-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b72-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3b72-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d3b72-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3b72-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d3b72-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3b72-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d3b72-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3b72-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d3b72-124">Header</span><span class="sxs-lookup"><span data-stu-id="d3b72-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3b72-125"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3b72-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d3b72-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d3b72-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="d3b72-127"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3b72-127"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d3b72-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d3b72-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3b72-129"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3b72-129"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="d3b72-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3b72-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3b72-131">Drucken</span><span class="sxs-lookup"><span data-stu-id="d3b72-131">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d3b72-132">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d3b72-132">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d3b72-133">**Findnextprinterchangenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="d3b72-133">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="d3b72-134">**Drucker \_ Benachrichtigungs \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="d3b72-134">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> </dl>

 

 




