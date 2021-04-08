---
description: Die spfilenotify-warteschlangenbenachrichtigungsinteschlange \_ \_ wird von setupscanfilequeue für jeden Knoten in der Kopier unter Warteschlange der Datei Warteschlange an eine Rückruf Routine gesendet.
ms.assetid: 293e63f9-9567-4ea7-b7e5-e5046c8a704b
title: SPFILENOTIFY_QUEUESCAN_EX Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e18cf1cdb1cd007dcf46793d2d018dedd80037
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864191"
---
# <a name="spfilenotify_queuescan_ex-message"></a><span data-ttu-id="f79db-103">Spfilenotify \_ queuescan \_ Ex-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f79db-103">SPFILENOTIFY\_QUEUESCAN\_EX message</span></span>

<span data-ttu-id="f79db-104">Die **spfilenotify \_ \_** -warteschlangenbenachrichtigungsinteschlange wird von [**setupscanfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) für jeden Knoten in der Kopier unter Warteschlange der Datei Warteschlange an eine Rückruf Routine gesendet.</span><span class="sxs-lookup"><span data-stu-id="f79db-104">The **SPFILENOTIFY\_QUEUESCAN\_EX** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="f79db-105">Dies ist nur der Fall, wenn die **setupscanfilequeue** -Funktion aufgerufen wurde, wobei das Flag SPQ \_ Scan \_ use \_ callbackex angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f79db-105">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACKEX.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN_EX
  Param1 = (PFILEPATHS) Filepaths;
            
```



## <a name="parameters"></a><span data-ttu-id="f79db-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f79db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f79db-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="f79db-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="f79db-108">Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f79db-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="f79db-109">Das **Zielmember** ist der Dateiname der Zieldatei im System.</span><span class="sxs-lookup"><span data-stu-id="f79db-109">The **Target** member is the filename of the target file on the system.</span></span> <span data-ttu-id="f79db-110">Der **Quell** Member ist der erwartete Pfad der Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="f79db-110">The **Source** member is the expected path of the source file.</span></span> <span data-ttu-id="f79db-111">Der **Win32Error** -Member ist der Signatur Fehler.</span><span class="sxs-lookup"><span data-stu-id="f79db-111">The **Win32Error** member is the signing error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f79db-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f79db-112">Return value</span></span>

<span data-ttu-id="f79db-113">Die Rückruf Routine sollte einen [Systemfehler Code](/windows/desktop/Debug/system-error-codes)zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f79db-113">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="f79db-114">Wenn die Rückruf Routine keinen Fehler zurückgibt \_ , wird der Warteschlangen Scan fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="f79db-114">If the callback routine returns NO\_ERROR, the queue scan continues.</span></span> <span data-ttu-id="f79db-115">Wenn die Routine einen anderen Fehlercode zurückgibt, wird der Warteschlangen Scan abgebrochen und [**setupscanfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f79db-115">If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns FALSE.</span></span>

> [!Note]  
> <span data-ttu-id="f79db-116">Diese Benachrichtigung wird nicht von der [**setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) -Funktion verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f79db-116">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f79db-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f79db-117">Requirements</span></span>



| <span data-ttu-id="f79db-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f79db-118">Requirement</span></span> | <span data-ttu-id="f79db-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f79db-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f79db-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f79db-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f79db-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f79db-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f79db-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f79db-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f79db-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f79db-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f79db-124">Header</span><span class="sxs-lookup"><span data-stu-id="f79db-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f79db-125"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f79db-125"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f79db-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f79db-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f79db-127">Übersicht</span><span class="sxs-lookup"><span data-stu-id="f79db-127">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="f79db-128">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="f79db-128">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="f79db-129">**Setupscanfilequeue**</span><span class="sxs-lookup"><span data-stu-id="f79db-129">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

