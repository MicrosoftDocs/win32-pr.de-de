---
description: Wird an ein Fenster gesendet, wenn das Fenster ausgeblendet oder angezeigt wird.
ms.assetid: dea7c9aa-eba7-4b93-a4c5-9b2d36999780
title: WM_SHOWWINDOW Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbca6cbb4c73ff1cad31754b1b581e0c892970e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345569"
---
# <a name="wm_showwindow-message"></a><span data-ttu-id="2af55-103">WM- \_ Show Window-Meldung</span><span class="sxs-lookup"><span data-stu-id="2af55-103">WM\_SHOWWINDOW message</span></span>

<span data-ttu-id="2af55-104">Wird an ein Fenster gesendet, wenn das Fenster ausgeblendet oder angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2af55-104">Sent to a window when the window is about to be hidden or shown.</span></span>

<span data-ttu-id="2af55-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="2af55-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SHOWWINDOW                   0x0018
```



## <a name="parameters"></a><span data-ttu-id="2af55-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2af55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2af55-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2af55-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2af55-108">Gibt an, ob ein Fenster angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2af55-108">Indicates whether a window is being shown.</span></span> <span data-ttu-id="2af55-109">Wenn *wParam* den Wert **true** hat, wird das Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2af55-109">If *wParam* is **TRUE**, the window is being shown.</span></span> <span data-ttu-id="2af55-110">Wenn *wParam* den Wert **false** hat, wird das Fenster ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="2af55-110">If *wParam* is **FALSE**, the window is being hidden.</span></span>

</dd> <dt>

<span data-ttu-id="2af55-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2af55-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2af55-112">Der Status des Fensters, das angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2af55-112">The status of the window being shown.</span></span> <span data-ttu-id="2af55-113">Wenn *LPARAM* gleich NULL ist, wurde die Nachricht aufgrund eines Aufrufes der [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) -Funktion gesendet. Andernfalls ist *LPARAM* einem der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="2af55-113">If *lParam* is zero, the message was sent because of a call to the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function; otherwise, *lParam* is one of the following values.</span></span>



| <span data-ttu-id="2af55-114">Wert</span><span class="sxs-lookup"><span data-stu-id="2af55-114">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="2af55-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2af55-115">Meaning</span></span>                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="SW_OTHERUNZOOM"></span><span id="sw_otherunzoom"></span><dl> <span data-ttu-id="2af55-116"><dt>**SW \_ Otherunzoom**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2af55-116"><dt>**SW\_OTHERUNZOOM**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="2af55-117">Das Fenster wird angezeigt, weil ein maximiertes Fenster wieder hergestellt oder minimiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2af55-117">The window is being uncovered because a maximize window was restored or minimized.</span></span><br/> |
| <span id="SW_OTHERZOOM"></span><span id="sw_otherzoom"></span><dl> <span data-ttu-id="2af55-118"><dt>**SW \_ Otherzoom**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2af55-118"><dt>**SW\_OTHERZOOM**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="2af55-119">Das Fenster wird von einem anderen Fenster abgedeckt, das maximiert ist.</span><span class="sxs-lookup"><span data-stu-id="2af55-119">The window is being covered by another window that has been maximized.</span></span><br/>             |
| <span id="SW_PARENTCLOSING"></span><span id="sw_parentclosing"></span><dl> <span data-ttu-id="2af55-120"><dt>**SW \_ Abschließende**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2af55-120"><dt>**SW\_PARENTCLOSING**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="2af55-121">Das Fenster Besitzer Fenster wird minimiert.</span><span class="sxs-lookup"><span data-stu-id="2af55-121">The window's owner window is being minimized.</span></span><br/>                                      |
| <span id="SW_PARENTOPENING"></span><span id="sw_parentopening"></span><dl> <span data-ttu-id="2af55-122"><dt>**SW \_ Element Opening**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2af55-122"><dt>**SW\_PARENTOPENING**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="2af55-123">Das Fenster Besitzer Fenster wird wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="2af55-123">The window's owner window is being restored.</span></span><br/>                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2af55-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2af55-124">Return value</span></span>

<span data-ttu-id="2af55-125">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="2af55-125">Type: **LRESULT**</span></span>

<span data-ttu-id="2af55-126">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2af55-126">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2af55-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2af55-127">Remarks</span></span>

<span data-ttu-id="2af55-128">Mit der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion wird das Fenster ausgeblendet oder angezeigt, wie in der Meldung angegeben.</span><span class="sxs-lookup"><span data-stu-id="2af55-128">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function hides or shows the window, as specified by the message.</span></span> <span data-ttu-id="2af55-129">Wenn ein Fenster während der Erstellung das [**\_ sichtbare WS**](window-styles.md) -Format aufweist, empfängt das Fenster diese Nachricht, nachdem Sie erstellt wurde, aber bevor Sie angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2af55-129">If a window has the [**WS\_VISIBLE**](window-styles.md) style when it is created, the window receives this message after it is created, but before it is displayed.</span></span> <span data-ttu-id="2af55-130">Ein Fenster empfängt diese Meldung auch dann, wenn der Sichtbarkeits Zustand von der [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) -oder [**showownedpopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) -Funktion geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2af55-130">A window also receives this message when its visibility state is changed by the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) or [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) function.</span></span>

<span data-ttu-id="2af55-131">Die **WM- \_ Show Window** -Meldung wird unter den folgenden Umständen nicht gesendet:</span><span class="sxs-lookup"><span data-stu-id="2af55-131">The **WM\_SHOWWINDOW** message is not sent under the following circumstances:</span></span>

-   <span data-ttu-id="2af55-132">Wenn ein überlappendes Fenster der obersten Ebene mit der [**WS- \_ Maximierung**](window-styles.md) oder dem **WS- \_ Minimierungs** Stil erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2af55-132">When a top-level, overlapped window is created with the [**WS\_MAXIMIZE**](window-styles.md) or **WS\_MINIMIZE** style.</span></span>
-   <span data-ttu-id="2af55-133">Wenn das " **SW \_ shownormal** "-Flag im Aufrufe der [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) -Funktion angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2af55-133">When the **SW\_SHOWNORMAL** flag is specified in the call to the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2af55-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2af55-134">Requirements</span></span>



| <span data-ttu-id="2af55-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2af55-135">Requirement</span></span> | <span data-ttu-id="2af55-136">Wert</span><span class="sxs-lookup"><span data-stu-id="2af55-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2af55-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2af55-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2af55-138">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2af55-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2af55-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2af55-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2af55-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2af55-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2af55-141">Header</span><span class="sxs-lookup"><span data-stu-id="2af55-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="2af55-142"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="2af55-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2af55-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2af55-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="2af55-144">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="2af55-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2af55-145">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="2af55-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="2af55-146">**Showownedpopups**</span><span class="sxs-lookup"><span data-stu-id="2af55-146">**ShowOwnedPopups**</span></span>](/windows/win32/api/winuser/nf-winuser-showownedpopups)
</dt> <dt>

[<span data-ttu-id="2af55-147">**ShowWindow**</span><span class="sxs-lookup"><span data-stu-id="2af55-147">**ShowWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-showwindow)
</dt> <dt>

<span data-ttu-id="2af55-148">**Licher**</span><span class="sxs-lookup"><span data-stu-id="2af55-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2af55-149">Windows</span><span class="sxs-lookup"><span data-stu-id="2af55-149">Windows</span></span>](windows.md)
</dt> </dl>

 

 
