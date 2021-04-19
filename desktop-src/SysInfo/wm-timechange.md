---
description: Eine Meldung, die gesendet wird, wenn die Systemzeit geändert wird.
ms.assetid: 94b5b6f7-04bb-4e0a-848b-e2b31ffc2938
title: WM_TIMECHANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d43bb5cd4284813c45ab074a93a9cd9699883aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349788"
---
# <a name="wm_timechange-message"></a><span data-ttu-id="16bb6-103">WM- \_ Zeit Änderungs Meldung</span><span class="sxs-lookup"><span data-stu-id="16bb6-103">WM\_TIMECHANGE message</span></span>

<span data-ttu-id="16bb6-104">Eine Meldung, die gesendet wird, wenn die Systemzeit geändert wird.</span><span class="sxs-lookup"><span data-stu-id="16bb6-104">A message that is sent whenever there is a change in the system time.</span></span>

<span data-ttu-id="16bb6-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="16bb6-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // message identifier
  WPARAM wParam,   // not used; must be zero
  LPARAM lParam    // not used; must be zero
);
```



## <a name="parameters"></a><span data-ttu-id="16bb6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="16bb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16bb6-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="16bb6-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="16bb6-108">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="16bb6-108">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="16bb6-109">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="16bb6-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="16bb6-110">**WM \_ Timechange** -Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="16bb6-110">**WM\_TIMECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="16bb6-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="16bb6-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16bb6-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="16bb6-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="16bb6-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="16bb6-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16bb6-114">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="16bb6-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16bb6-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16bb6-115">Return value</span></span>

<span data-ttu-id="16bb6-116">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="16bb6-116">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="16bb6-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16bb6-117">Remarks</span></span>

<span data-ttu-id="16bb6-118">Eine Anwendung sollte diese Nachricht nicht übertragen, da das System diese Meldung überträgt, wenn die Systemzeit von der Anwendung geändert wird.</span><span class="sxs-lookup"><span data-stu-id="16bb6-118">An application should not broadcast this message, because the system will broadcast this message when the application changes the system time.</span></span>

## <a name="requirements"></a><span data-ttu-id="16bb6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16bb6-119">Requirements</span></span>



| <span data-ttu-id="16bb6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16bb6-120">Requirement</span></span> | <span data-ttu-id="16bb6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="16bb6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16bb6-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16bb6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="16bb6-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16bb6-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="16bb6-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16bb6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="16bb6-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16bb6-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="16bb6-126">Header</span><span class="sxs-lookup"><span data-stu-id="16bb6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="16bb6-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="16bb6-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16bb6-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16bb6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16bb6-129">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="16bb6-129">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

