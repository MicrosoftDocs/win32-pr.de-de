---
title: WM_ACTIVATE Meldung (Winuser. h)
description: Wird an das Fenster gesendet, das aktiviert wird, und das Fenster wird deaktiviert.
ms.assetid: a62bb9f7-f286-4d0d-a1ca-370950c188b2
keywords:
- Tastatur-und Maus Eingaben für WM_ACTIVATE Nachricht
topic_type:
- apiref
api_name:
- WM_ACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec28662aa2219ee9b3ad2e8cc8efac861d292f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103407"
---
# <a name="wm_activate-message"></a><span data-ttu-id="3944c-104">WM- \_ Aktivierungs Nachricht</span><span class="sxs-lookup"><span data-stu-id="3944c-104">WM\_ACTIVATE message</span></span>

<span data-ttu-id="3944c-105">Wird an das Fenster gesendet, das aktiviert wird, und das Fenster wird deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3944c-105">Sent to both the window being activated and the window being deactivated.</span></span> <span data-ttu-id="3944c-106">Wenn in den Fenstern dieselbe Eingabe Warteschlange verwendet wird, wird die Nachricht synchron gesendet, zuerst an die Fenster Prozedur des Fensters der obersten Ebene, die deaktiviert wird, und dann an die Fenster Prozedur des Fensters der obersten Ebene, das aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="3944c-106">If the windows use the same input queue, the message is sent synchronously, first to the window procedure of the top-level window being deactivated, then to the window procedure of the top-level window being activated.</span></span> <span data-ttu-id="3944c-107">Wenn in den Fenstern verschiedene Eingabe Warteschlangen verwendet werden, wird die Nachricht asynchron gesendet, sodass das Fenster sofort aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="3944c-107">If the windows use different input queues, the message is sent asynchronously, so the window is activated immediately.</span></span>


```C++
#define WM_ACTIVATE                     0x0006
```



## <a name="parameters"></a><span data-ttu-id="3944c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3944c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3944c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3944c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3944c-110">Mit dem nieder wertigen Wort wird angegeben, ob das Fenster aktiviert oder deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="3944c-110">The low-order word specifies whether the window is being activated or deactivated.</span></span> <span data-ttu-id="3944c-111">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="3944c-111">This parameter can be one of the following values.</span></span> <span data-ttu-id="3944c-112">Das höchst wertige Wort gibt den minimierten Zustand des Fensters an, das aktiviert oder deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="3944c-112">The high-order word specifies the minimized state of the window being activated or deactivated.</span></span> <span data-ttu-id="3944c-113">Ein Wert ungleich NULL gibt an, dass das Fenster minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="3944c-113">A nonzero value indicates the window is minimized.</span></span>



| <span data-ttu-id="3944c-114">Wert</span><span class="sxs-lookup"><span data-stu-id="3944c-114">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="3944c-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3944c-115">Meaning</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WA_ACTIVE"></span><span id="wa_active"></span><dl> <span data-ttu-id="3944c-116"><dt>**WA \_ Aktiv**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3944c-116"><dt>**WA\_ACTIVE**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="3944c-117">Wird von einer anderen Methode als einem Mausklick aktiviert (z. b. durch einen aufzurufenden Befehl der [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) -Funktion oder durch Verwendung der Tastaturschnittstelle zum Auswählen des Fensters).</span><span class="sxs-lookup"><span data-stu-id="3944c-117">Activated by some method other than a mouse click (for example, by a call to the [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) function or by use of the keyboard interface to select the window).</span></span><br/> |
| <span id="WA_CLICKACTIVE"></span><span id="wa_clickactive"></span><dl> <span data-ttu-id="3944c-118"><dt>**WA \_ Clickactive**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3944c-118"><dt>**WA\_CLICKACTIVE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="3944c-119">Aktiviert durch einen Mausklick.</span><span class="sxs-lookup"><span data-stu-id="3944c-119">Activated by a mouse click.</span></span><br/>                                                                                                                                                                     |
| <span id="WA_INACTIVE"></span><span id="wa_inactive"></span><dl> <span data-ttu-id="3944c-120"><dt>**WA \_ Inaktiv**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3944c-120"><dt>**WA\_INACTIVE**</dt> <dt>0</dt></span></span> </dl>          | <span data-ttu-id="3944c-121">Deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3944c-121">Deactivated.</span></span><br/>                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="3944c-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3944c-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3944c-123">Ein Handle für das Fenster, das aktiviert oder deaktiviert wird, abhängig vom Wert des *wParam* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="3944c-123">A handle to the window being activated or deactivated, depending on the value of the *wParam* parameter.</span></span> <span data-ttu-id="3944c-124">Wenn das nieder wertige Wort von *wParam* in der **WA \_ inaktiven** Reihenfolge ist, ist *LPARAM* das Handle für das Fenster, das aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="3944c-124">If the low-order word of *wParam* is **WA\_INACTIVE**, *lParam* is the handle to the window being activated.</span></span> <span data-ttu-id="3944c-125">Wenn das nieder wertige Wort von *wParam* auf **WA \_ Active** oder **WA \_ clickactive** festgelegt ist, ist *LPARAM* das Handle für das Fenster, das deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="3944c-125">If the low-order word of *wParam* is **WA\_ACTIVE** or **WA\_CLICKACTIVE**, *lParam* is the handle to the window being deactivated.</span></span> <span data-ttu-id="3944c-126">Dieses Handle kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="3944c-126">This handle can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3944c-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3944c-127">Return value</span></span>

<span data-ttu-id="3944c-128">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3944c-128">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3944c-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3944c-129">Remarks</span></span>

<span data-ttu-id="3944c-130">Wenn das Fenster aktiviert wird und nicht minimiert ist, legt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion den Tastaturfokus auf das Fenster fest.</span><span class="sxs-lookup"><span data-stu-id="3944c-130">If the window is being activated and is not minimized, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets the keyboard focus to the window.</span></span> <span data-ttu-id="3944c-131">Wenn das Fenster durch einen Mausklick aktiviert wird, wird auch eine WM- [**\_ mouseaktivierungs**](wm-mouseactivate.md) -Meldung empfangen.</span><span class="sxs-lookup"><span data-stu-id="3944c-131">If the window is activated by a mouse click, it also receives a [**WM\_MOUSEACTIVATE**](wm-mouseactivate.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3944c-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3944c-132">Requirements</span></span>



| <span data-ttu-id="3944c-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3944c-133">Requirement</span></span> | <span data-ttu-id="3944c-134">Wert</span><span class="sxs-lookup"><span data-stu-id="3944c-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3944c-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3944c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3944c-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3944c-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3944c-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3944c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3944c-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3944c-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3944c-139">Header</span><span class="sxs-lookup"><span data-stu-id="3944c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="3944c-140"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="3944c-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3944c-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3944c-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="3944c-142">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="3944c-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3944c-143">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="3944c-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="3944c-144">**"Fenster"**</span><span class="sxs-lookup"><span data-stu-id="3944c-144">**SetActiveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-setactivewindow)
</dt> <dt>

[<span data-ttu-id="3944c-145">**WM- \_ moueinaktivierung**</span><span class="sxs-lookup"><span data-stu-id="3944c-145">**WM\_MOUSEACTIVATE**</span></span>](wm-mouseactivate.md)
</dt> <dt>

[<span data-ttu-id="3944c-146">**WM- \_ ncaktivierung**</span><span class="sxs-lookup"><span data-stu-id="3944c-146">**WM\_NCACTIVATE**</span></span>](/windows/desktop/winmsg/wm-ncactivate)
</dt> <dt>

<span data-ttu-id="3944c-147">**Licher**</span><span class="sxs-lookup"><span data-stu-id="3944c-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3944c-148">Tastatureingabe</span><span class="sxs-lookup"><span data-stu-id="3944c-148">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

