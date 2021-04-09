---
description: Die Funktion findcloseprinterchangenotifischließt ein Änderungs Benachrichtigungs Objekt, das durch Aufrufen der findfirstprinterchangenotifizierungsfunktion erstellt wurde.
ms.assetid: 2b4758f8-af0a-494b-8f1b-8ea6ee73c79b
title: Findcloseprinterchangenotifi-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindClosePrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 8040944d5890aa521681827bef786201a35da039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042214"
---
# <a name="findcloseprinterchangenotification-function"></a><span data-ttu-id="1d2f2-103">Findcloseprinterchangenotifi-Funktion</span><span class="sxs-lookup"><span data-stu-id="1d2f2-103">FindClosePrinterChangeNotification function</span></span>

<span data-ttu-id="1d2f2-104">Die Funktion **findcloseprinterchangenotifischließt** ein Änderungs Benachrichtigungs Objekt, das durch Aufrufen der [**findfirstprinterchangenotifizierungsfunktion**](findfirstprinterchangenotification.md) erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-104">The **FindClosePrinterChangeNotification** function closes a change notification object created by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span> <span data-ttu-id="1d2f2-105">Der Drucker oder Druckserver, der dem Änderungs Benachrichtigungs Objekt zugeordnet ist, wird nicht mehr von diesem Objekt überwacht.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-105">The printer or print server associated with the change notification object will no longer be monitored by that object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d2f2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d2f2-106">Syntax</span></span>


```C++
BOOL FindClosePrinterChangeNotification(
  _In_ HANDLE hChange
);
```



## <a name="parameters"></a><span data-ttu-id="1d2f2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d2f2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d2f2-108">*hchange* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d2f2-108">*hChange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d2f2-109">Ein Handle für das Änderungs Benachrichtigungs Objekt, das geschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-109">A handle to the change notification object to be closed.</span></span> <span data-ttu-id="1d2f2-110">Dies ist ein Handle, das durch Aufrufen der [**findfirstprinterchangenotifi-**](findfirstprinterchangenotification.md) Funktion erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-110">This is a handle created by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d2f2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d2f2-111">Return value</span></span>

<span data-ttu-id="1d2f2-112">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1d2f2-112">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="1d2f2-113">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-113">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d2f2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d2f2-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1d2f2-115">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-115">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="1d2f2-116">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-116">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="1d2f2-117">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-117">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="1d2f2-118">Nachdem Sie die **findcloseprinterchangenotifi-** Funktion aufgerufen haben, können Sie das *hchange* -Handle nicht in nachfolgenden Aufrufen von [**findfirstprinterchangenotifizierung**](findfirstprinterchangenotification.md) oder [**findnextprinterchangenotifizierung**](findnextprinterchangenotification.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="1d2f2-118">After calling the **FindClosePrinterChangeNotification** function, you cannot use the *hChange* handle in subsequent calls to either [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) or [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d2f2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d2f2-119">Requirements</span></span>



| <span data-ttu-id="1d2f2-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d2f2-120">Requirement</span></span> | <span data-ttu-id="1d2f2-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1d2f2-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d2f2-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d2f2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1d2f2-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d2f2-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1d2f2-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d2f2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1d2f2-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d2f2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1d2f2-126">Header</span><span class="sxs-lookup"><span data-stu-id="1d2f2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d2f2-127"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1d2f2-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1d2f2-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="1d2f2-129"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="1d2f2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1d2f2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d2f2-131"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d2f2-131"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="1d2f2-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d2f2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d2f2-133">Drucken</span><span class="sxs-lookup"><span data-stu-id="1d2f2-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1d2f2-134">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="1d2f2-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="1d2f2-135">**Findfirstprinterchangenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="1d2f2-135">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="1d2f2-136">**Findnextprinterchangenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="1d2f2-136">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> </dl>

 

 




