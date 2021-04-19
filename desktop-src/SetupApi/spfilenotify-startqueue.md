---
description: Die spfilenotify- \_ Benachrichtigung "startqueue" wird an die Rückruf Routine gesendet, wenn der Prozess für die Warteschlangen Verpflichtung gestartet wird.
ms.assetid: 682c2ce0-0c82-402c-a487-db5f2c377f3f
title: SPFILENOTIFY_STARTQUEUE Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090e3f97dceb1843d75934dd99cca500e6f93086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362857"
---
# <a name="spfilenotify_startqueue-message"></a><span data-ttu-id="2230d-103">Spfilenotify- \_ startqueue-Nachricht</span><span class="sxs-lookup"><span data-stu-id="2230d-103">SPFILENOTIFY\_STARTQUEUE message</span></span>

<span data-ttu-id="2230d-104">Die **spfilenotify-Benachrichtigung " \_ startqueue** " wird an die Rückruf Routine gesendet, wenn der Prozess für die Warteschlangen Verpflichtung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="2230d-104">The **SPFILENOTIFY\_STARTQUEUE** notification is sent to the callback routine when the queue commitment process starts.</span></span>


```C++
SPFILENOTIFY_STARTQUEUE
  Param1 = (UINT) OwnerWindow;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="2230d-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="2230d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2230d-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="2230d-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="2230d-107">Handle für das Fenster, das die von der Rückruf Routine generierten Dialogfelder besitzen soll.</span><span class="sxs-lookup"><span data-stu-id="2230d-107">Handle to the window that is to own the dialog boxes that the callback routine generates.</span></span>

</dd> <dt>

<span data-ttu-id="2230d-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="2230d-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="2230d-109">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2230d-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2230d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2230d-110">Return value</span></span>

<span data-ttu-id="2230d-111">Wenn ein Fehler auftritt, sollte die Rückruf Routine [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror)aufrufen und den Fehler angeben und dann 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2230d-111">If an error occurs, the callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), specifying the error, and then return zero.</span></span> <span data-ttu-id="2230d-112">Die [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) -Funktion gibt " **false** " zurück, und ein nachfolgendes Aufrufen von " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " gibt den von der Rückruf Routine festgelegten Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="2230d-112">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function will return **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the error code set by the callback routine.</span></span>

<span data-ttu-id="2230d-113">Wenn kein Fehler auftritt, sollte die Rückruf Routine einen Wert ungleich 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2230d-113">If no error occurs, the callback routine should return a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2230d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2230d-114">Requirements</span></span>



| <span data-ttu-id="2230d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2230d-115">Requirement</span></span> | <span data-ttu-id="2230d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="2230d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2230d-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2230d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2230d-118">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2230d-118">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2230d-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2230d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2230d-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2230d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2230d-121">Header</span><span class="sxs-lookup"><span data-stu-id="2230d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2230d-122"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2230d-122"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2230d-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2230d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2230d-124">Übersicht</span><span class="sxs-lookup"><span data-stu-id="2230d-124">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="2230d-125">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="2230d-125">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="2230d-126">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="2230d-126">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="2230d-127">**Setupdefaultqueuecallback**</span><span class="sxs-lookup"><span data-stu-id="2230d-127">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

