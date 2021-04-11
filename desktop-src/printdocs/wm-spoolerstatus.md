---
description: Die WM- \_ spoolerstatus-Nachricht wird vom Druck-Manager gesendet, wenn ein Auftrag der Druck-Manager-Warteschlange hinzugefügt oder daraus entfernt wird.
ms.assetid: 6140c9d8-0e5b-49f2-a4a6-cc1f2a0bed0a
title: WM_SPOOLERSTATUS Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 460e36e44f219bcbe6f514d7d368accddae46b83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131801"
---
# <a name="wm_spoolerstatus-message"></a><span data-ttu-id="d6042-103">WM- \_ spoolerstatus-Meldung</span><span class="sxs-lookup"><span data-stu-id="d6042-103">WM\_SPOOLERSTATUS message</span></span>

<span data-ttu-id="d6042-104">Die **WM- \_ spoolerstatus** -Nachricht wird vom Druck-Manager gesendet, wenn ein Auftrag der Druck-Manager-Warteschlange hinzugefügt oder daraus entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d6042-104">The **WM\_SPOOLERSTATUS** message is sent from Print Manager whenever a job is added to or removed from the Print Manager queue.</span></span>

<span data-ttu-id="d6042-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d6042-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="d6042-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6042-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6042-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d6042-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6042-108">Das PR- \_ Jobstatus-Flag.</span><span class="sxs-lookup"><span data-stu-id="d6042-108">The PR\_JOBSTATUS flag.</span></span>

</dd> <dt>

<span data-ttu-id="d6042-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6042-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6042-110">Mit dem nieder wertigen Wort wird die Anzahl der verbleibenden Aufträge in der Druck-Manager-Warteschlange angegeben.</span><span class="sxs-lookup"><span data-stu-id="d6042-110">The low-order word specifies the number of jobs remaining in the Print Manager queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6042-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6042-111">Return value</span></span>

<span data-ttu-id="d6042-112">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d6042-112">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6042-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6042-113">Remarks</span></span>

<span data-ttu-id="d6042-114">Diese Meldung dient nur zu Informationszwecken.</span><span class="sxs-lookup"><span data-stu-id="d6042-114">This message is for informational purposes only.</span></span> <span data-ttu-id="d6042-115">Diese Meldung ist eine Empfehlung und weist keine garantierte Übermittlungs Semantik auf.</span><span class="sxs-lookup"><span data-stu-id="d6042-115">This message is advisory and does not have guaranteed delivery semantics.</span></span> <span data-ttu-id="d6042-116">Anwendungen sollten nicht davon ausgehen, dass Sie eine WM- \_ spoolerstatus-Meldung für jede Änderung des spoolerstatus erhalten.</span><span class="sxs-lookup"><span data-stu-id="d6042-116">Applications should not assume that they will receive a WM\_SPOOLERSTATUS message for every change in spooler status.</span></span>

<span data-ttu-id="d6042-117">Die WM- \_ spoolerstatus-Nachricht wird nach Windows XP nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d6042-117">The WM\_SPOOLERSTATUS message is not supported after Windows XP.</span></span> <span data-ttu-id="d6042-118">Wenn Sie über Änderungen am Status der Druck Warteschlange benachrichtigt werden möchten, können Sie [**findfirstprinterchangenotifizierung**](findfirstprinterchangenotification.md) und [**findnextprinterchangenotifiken**](findnextprinterchangenotification.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="d6042-118">To be notified of changes to the print queue status, you can use [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) and [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6042-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6042-119">Requirements</span></span>



| <span data-ttu-id="d6042-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6042-120">Requirement</span></span> | <span data-ttu-id="d6042-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d6042-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6042-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6042-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d6042-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6042-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d6042-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6042-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d6042-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6042-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d6042-126">Header</span><span class="sxs-lookup"><span data-stu-id="d6042-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6042-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d6042-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6042-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6042-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6042-129">Drucken</span><span class="sxs-lookup"><span data-stu-id="d6042-129">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d6042-130">Druck Spooler-API-Meldungen</span><span class="sxs-lookup"><span data-stu-id="d6042-130">Print Spooler API Messages</span></span>](printing-and-print-spooler-messages.md)
</dt> <dt>

[<span data-ttu-id="d6042-131">**Findfirstprinterchangenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="d6042-131">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="d6042-132">**Findnextprinterchangenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="d6042-132">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> </dl>

 

