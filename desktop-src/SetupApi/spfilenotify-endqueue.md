---
description: Die spfilenotify- \_ Benachrichtigung zur endwarteschlange wird an die Rückruf Routine gesendet, wenn alle in der Warteschlange befindlichen Vorgänge abgeschlossen wurden.
ms.assetid: f4540ab6-edea-4f84-b7eb-4ab3f774068b
title: SPFILENOTIFY_ENDQUEUE Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3ed2ca896f91ec09cb49f89731b41c5d099465
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960747"
---
# <a name="spfilenotify_endqueue-message"></a><span data-ttu-id="2ac24-103">Spfilenotify- \_ endwarteschlangen-Nachricht</span><span class="sxs-lookup"><span data-stu-id="2ac24-103">SPFILENOTIFY\_ENDQUEUE message</span></span>

<span data-ttu-id="2ac24-104">Die **spfilenotify-Benachrichtigung zur \_ endwarteschlange** wird an die Rückruf Routine gesendet, wenn alle in der Warteschlange befindlichen Vorgänge abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="2ac24-104">The **SPFILENOTIFY\_ENDQUEUE** notification is sent to the callback routine when all of the queued operations have been completed.</span></span>


```C++
SPFILENOTIFY_ENDQUEUE
  Param1 = (UINT) Result;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="2ac24-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ac24-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ac24-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="2ac24-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="2ac24-107">**True** , wenn die Warteschlange erfolgreich verarbeitet wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="2ac24-107">**TRUE** if the queue was processed successfully, **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="2ac24-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="2ac24-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="2ac24-109">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ac24-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ac24-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ac24-110">Return value</span></span>

<span data-ttu-id="2ac24-111">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2ac24-111">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ac24-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ac24-112">Requirements</span></span>



| <span data-ttu-id="2ac24-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ac24-113">Requirement</span></span> | <span data-ttu-id="2ac24-114">Wert</span><span class="sxs-lookup"><span data-stu-id="2ac24-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ac24-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ac24-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2ac24-116">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ac24-116">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2ac24-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ac24-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2ac24-118">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ac24-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ac24-119">Header</span><span class="sxs-lookup"><span data-stu-id="2ac24-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ac24-120"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ac24-120"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ac24-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2ac24-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ac24-122">Übersicht</span><span class="sxs-lookup"><span data-stu-id="2ac24-122">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="2ac24-123">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="2ac24-123">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="2ac24-124">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="2ac24-124">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="2ac24-125">**Setupdefaultqueuecallback**</span><span class="sxs-lookup"><span data-stu-id="2ac24-125">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




