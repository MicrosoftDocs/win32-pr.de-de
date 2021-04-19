---
description: Wird gesendet, wenn ein Fenster, das zu einer anderen Anwendung als das aktive Fenster gehört, aktiviert wird. Die Nachricht wird an die Anwendung gesendet, deren Fenster aktiviert wird, und an die Anwendung, deren Fenster deaktiviert wird.
ms.assetid: fc3626ac-8f19-4aa6-8fe9-5020d00c09db
title: WM_ACTIVATEAPP Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2d64b90426e004a3c18fdc60538fd21862c42f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363595"
---
# <a name="wm_activateapp-message"></a><span data-ttu-id="c5da7-104">WM \_ activateapp-Meldung</span><span class="sxs-lookup"><span data-stu-id="c5da7-104">WM\_ACTIVATEAPP message</span></span>

<span data-ttu-id="c5da7-105">Wird gesendet, wenn ein Fenster, das zu einer anderen Anwendung als das aktive Fenster gehört, aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="c5da7-105">Sent when a window belonging to a different application than the active window is about to be activated.</span></span> <span data-ttu-id="c5da7-106">Die Nachricht wird an die Anwendung gesendet, deren Fenster aktiviert wird, und an die Anwendung, deren Fenster deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="c5da7-106">The message is sent to the application whose window is being activated and to the application whose window is being deactivated.</span></span>

<span data-ttu-id="c5da7-107">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c5da7-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ACTIVATEAPP                  0x001C
```



## <a name="parameters"></a><span data-ttu-id="c5da7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5da7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5da7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5da7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5da7-110">Gibt an, ob das Fenster aktiviert oder deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="c5da7-110">Indicates whether the window is being activated or deactivated.</span></span> <span data-ttu-id="c5da7-111">Dieser Parameter ist **true** , wenn das Fenster aktiviert wird. der Wert ist **false** , wenn das Fenster deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="c5da7-111">This parameter is **TRUE** if the window is being activated; it is **FALSE** if the window is being deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="c5da7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5da7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5da7-113">Der Threadbezeichner.</span><span class="sxs-lookup"><span data-stu-id="c5da7-113">The thread identifier.</span></span> <span data-ttu-id="c5da7-114">Wenn der *wParam* -Parameter **true** ist, ist *LPARAM* der Bezeichner des Threads, der das Fenster besitzt, das deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="c5da7-114">If the *wParam* parameter is **TRUE**, *lParam* is the identifier of the thread that owns the window being deactivated.</span></span> <span data-ttu-id="c5da7-115">Wenn *wParam* den Wert **false** hat, ist *LPARAM* der Bezeichner des Threads, der das Fenster besitzt, das aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="c5da7-115">If *wParam* is **FALSE**, *lParam* is the identifier of the thread that owns the window being activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5da7-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5da7-116">Return value</span></span>

<span data-ttu-id="c5da7-117">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="c5da7-117">Type: **LRESULT**</span></span>

<span data-ttu-id="c5da7-118">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c5da7-118">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5da7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5da7-119">Requirements</span></span>



| <span data-ttu-id="c5da7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5da7-120">Requirement</span></span> | <span data-ttu-id="c5da7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c5da7-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5da7-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5da7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c5da7-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5da7-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c5da7-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5da7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c5da7-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5da7-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c5da7-126">Header</span><span class="sxs-lookup"><span data-stu-id="c5da7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5da7-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c5da7-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5da7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5da7-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="c5da7-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c5da7-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c5da7-130">**WM \_ aktivieren**</span><span class="sxs-lookup"><span data-stu-id="c5da7-130">**WM\_ACTIVATE**</span></span>](../inputdev/wm-activate.md)
</dt> <dt>

<span data-ttu-id="c5da7-131">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c5da7-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c5da7-132">Windows</span><span class="sxs-lookup"><span data-stu-id="c5da7-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
