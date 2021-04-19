---
description: Die spfilenotify- \_ Warteschlangen Benachrichtigung wird von setupscanfilequeue für jeden Knoten in der Kopier unter Warteschlange der Datei Warteschlange an eine Rückruf Routine gesendet. Dies tritt nur dann auf, wenn die Funktion setupscanfilequeue aufgerufen wurde, die das Flag SPQ \_ Scan \_ use \_ Callback angibt.
ms.assetid: 8aacc6c0-b6fe-4b4a-bbe4-a0351baf1f30
title: SPFILENOTIFY_QUEUESCAN Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66202a398f7e3f4e1121782f9469d2d6f299452c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363293"
---
# <a name="spfilenotify_queuescan-message"></a><span data-ttu-id="79ba1-104">Spfilenotify- \_ queuescan-Nachricht</span><span class="sxs-lookup"><span data-stu-id="79ba1-104">SPFILENOTIFY\_QUEUESCAN message</span></span>

<span data-ttu-id="79ba1-105">Die **spfilenotify- \_ Warteschlangen** Benachrichtigung wird von [**setupscanfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) für jeden Knoten in der Kopier unter Warteschlange der Datei Warteschlange an eine Rückruf Routine gesendet.</span><span class="sxs-lookup"><span data-stu-id="79ba1-105">The **SPFILENOTIFY\_QUEUESCAN** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="79ba1-106">Dies tritt nur dann auf, wenn die Funktion **setupscanfilequeue** aufgerufen wurde, die das Flag SPQ \_ Scan \_ use \_ Callback angibt.</span><span class="sxs-lookup"><span data-stu-id="79ba1-106">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACK.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN
  Param1 = (UINT) TargetPath;
  Param2 = (UINT) DelayFlag;
            
```



## <a name="parameters"></a><span data-ttu-id="79ba1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="79ba1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79ba1-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="79ba1-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="79ba1-109">NULL-terminierte Zeichenfolge, die die Ziel Pfadinformationen für die Datei angibt, die im aktuellen Knoten in die Warteschlange gestellt wurde</span><span class="sxs-lookup"><span data-stu-id="79ba1-109">Null-terminated string that specifies the target path information for the file queued in the current node.</span></span>

</dd> <dt>

<span data-ttu-id="79ba1-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="79ba1-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="79ba1-111">Wenn die Datei im aktuellen Knoten der Warteschlange verwendet wird, nimmt *Param2* den Wert der verzögerten SPQ- \_ Kopie an \_ .</span><span class="sxs-lookup"><span data-stu-id="79ba1-111">If the file in the current node of the queue is in use, *Param2* takes the value SPQ\_DELAYED\_COPY.</span></span> <span data-ttu-id="79ba1-112">Wenn die Datei nicht verwendet wird, ist der Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="79ba1-112">If the file is not in use, the value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79ba1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79ba1-113">Return value</span></span>

<span data-ttu-id="79ba1-114">Die Rückruf Routine sollte einen [Systemfehler Code](/windows/desktop/Debug/system-error-codes)zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="79ba1-114">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="79ba1-115">Wenn die Rückruf Routine keinen Fehler zurückgibt \_ , wird der Warteschlangen Scan fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="79ba1-115">If the callback routine returns NO\_ERROR, the queue scan continues.</span></span> <span data-ttu-id="79ba1-116">Wenn die Routine einen anderen Fehlercode zurückgibt, wird der Warteschlangen Scan abgebrochen und [**setupscanfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="79ba1-116">If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="79ba1-117">Diese Benachrichtigung wird nicht von der [**setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) -Funktion verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="79ba1-117">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="79ba1-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79ba1-118">Requirements</span></span>



| <span data-ttu-id="79ba1-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79ba1-119">Requirement</span></span> | <span data-ttu-id="79ba1-120">Wert</span><span class="sxs-lookup"><span data-stu-id="79ba1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79ba1-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79ba1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="79ba1-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79ba1-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="79ba1-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79ba1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="79ba1-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79ba1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79ba1-125">Header</span><span class="sxs-lookup"><span data-stu-id="79ba1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="79ba1-126"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="79ba1-126"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79ba1-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="79ba1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79ba1-128">Übersicht</span><span class="sxs-lookup"><span data-stu-id="79ba1-128">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="79ba1-129">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="79ba1-129">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="79ba1-130">**Setupscanfilequeue**</span><span class="sxs-lookup"><span data-stu-id="79ba1-130">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

